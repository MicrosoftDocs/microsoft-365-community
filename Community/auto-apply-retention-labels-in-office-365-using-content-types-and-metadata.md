---
title: Auto Apply Retention Labels in Office 365 Using Content Types and Metadata
author: joannecklein
ms.date: 3/3/2020
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: O365-seccomp
localization_priority: 
description: "Auto Apply Retention Labels in Office 365 Using Content Types and Metadata"
ms.collection: M365Community
---
# Auto Apply Retention Labels in Office 365 Using Content Types and Metadata

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

I think we all agree automating as much retention as possible is a good thing. The less we have to rely on information workers to manually apply a retention label, the better. The information architecture you've diligently defined in your tenant can now be leveraged using auto-apply conditions to automatically set a Purview retention label.

> Microsoft continues to publish new machine learning trainable classifiers to help with the growing amount of corporate "dark data" (not within a well-defined information architecture). This will apply out-of-the-box and custom classifiers to intelligently apply retention across your tenant by classifying content based on meaning and context. These will not be covered in this post.

Licensing... the capability to auto-apply labels described in this post requires a license for each user who has permissions to edit content that's been automatically labeled in a site. Users who simply have read-only access do not require a license: 
* Microsoft 365 E5/A5/G5
* Microsoft 365 E5/A5/G5/F5 Compliance and F5 Security & Compliance
* Microsoft 365 E5/A5/F5/G5 Information Protection and Governance
* Office 365 E5/A5/G5

Retention labels can currently be auto-applied based on 4 conditions:

* apply label to content containing a sensitive information type (both out-of-the-box and custom)
* apply label to content containing keywords, phrases, or properties (i.e., content types and metadata)
* apply label to content matching a trainable classifier
* apply label to cloud attachments shared in Exchange and Teams (new)

This post describes the second option above to demonstrate the auto-apply behavior across several column data types and content types in SharePoint. Due to the fact that the retention label isn't applied immediately (controlled by a back-end process that may take up to 7 days to apply the label), this is not a quick test to do. I've spent the time testing this, so I'm sharing the results and learning with you! Please refer to the 'Important things to know' section at the end of this post for some key takeaways on this functionality. I will update the takeaways as I learn more.

#### Apply a Retention Label based on a Content Type

Content type called _Contract document_ has been added to a document library. Retention label called _Contract_ has been created and auto-applied based on the Keyword Query Language (KQL) condition below:

**ContentType:'Contract document'**

The result? Within a week, the _Contract_ retention label was applied to all documents with the content type of _Contract document_ on all SharePoint sites the retention label was published to.

#### Apply a Retention Label based on a Choice Metadata column

A choice metadata column, _ContractType_, has been added to a library. I want to use one of the choice values to set a retention label. The auto-generated managed property from the search schema cannot be used in the auto-apply condition. You must manually map the crawled property to a RefinableString property between 00 and 99 (this Refinable property is pre-built by Microsoft and has all of the correct settings to use it as a condition in an auto-apply policy). For this example, I've mapped the crawled property generated for metadata column, ContractType, to RefinableString00. Retention label called _Hardware_ has been created and auto-applied based on the condition below:

**RefinableString00:Hardware**

The result? Within a week, the _Hardware_ retention label applied to all documents with a choice value of 'Hardware' on the _ContractType_ metadata column on all SharePoint sites the retention label was published to.

#### Apply a Retention Label on a compound condition

What about combining conditions? You can do this too! This test combined a content type name of _Contract document_ with a choice value of _Software._ A retention label called _Software_ has been created and auto-applied based on the condition below:

**ContentType:'Contract document' AND RefinableString00:Software**

The result? Within a week, the _Software_ retention label applied to all documents with a content type of _Contract document_ and a choice value of 'Software' on the _ContractType_ metadata column on all SharePoint sites the retention label was published to.

#### Apply a Retention Label on a Date column <= Today

Can you include date logic in the condition? Yes. I have added an optional date column, _DateExpired_, to a library and want to apply the retention label once a date has been entered and is today or in the past. To filter on a date column, you must map it's crawled property to a _RefinableDate_ column (it's queryable), so in this case I mapped it to _RefinableDate01._ A retention label called _Expired Contract_ has been created and auto-applied based on the condition below:

**RefinableDate01<=TODAY**

The result? Within a week, the _Expired Contract_ retention label applied to all documents when a date either equal to today or in the past has been entered into the _DateExpired_ metadata column on all SharePoint sites the retention label was published to. Note: if a date isn't entered in the column OR a future date is entered in the column, a retention label is not applied.

## Important things to know

Here are some important things to understand:

1. The back-end process to apply the retention label can currently take up to 7 days. If it is your expectation that the label will be updated soon after the metadata or content type is updated, this is incorrect.
2. If a retention label is already applied on a document, the auto-apply process will NEVER override/replace the label even if an auto-apply condition is met. Example: if you set the column _Contract Type_ to Software and this auto-applied a label called 'Software', and then you subsequently change the _Contract Type_ to Hardware, the label will not change to 'Hardware' if you had an auto-apply condition set to that condition. The original label, _Software_, would remain.
3. The columns filled in when the label is auto-applied are: _Retention label, Retention label applied,_ and _Label setting._ The _Label applied by_ is filled in with _System Account_.
4. You can manually remove an automatically-applied retention label by editing the properties (except if the label is a record label, then only a site collection admin can remove it. If the label is a regulatory record label, it cannot be removed). If you remove the retention label, the next time the back-end process runs, it will re-assess the document based on the auto-apply conditions and, if met, re-apply the correct label.
5. A simple way to test your conditions before creating your label policies is to enter the query directly into the _Microsoft Search_ box thru the SharePoint UI. It will return the same results.
6. Although I've seen other posts where an auto-apply condition was based on a managed metadata term value, my testing only shows success when the managed metadata term set is from the tenant-level term store defined in the SharePoint Admin Center.

---

**Principal author**: [Joanne Klein, MVP](https://www.linkedin.com/in/joannecklein)
