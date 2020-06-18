---
title: Auto Apply Retention Labels in Office 365 Using Content Types and Metadata
author: joannecklein
ms.date: 3/3/2020
ms.reviewer:  Joanne Hendrickson
localization_priority: 
description: "Auto Apply Retention Labels in Office 365 Using Content Types and Metadata"
ms.collection:  SPCommunity
---
# Auto Apply Retention Labels in Office 365 Using Content Types and Metadata

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

I think we all agree automating as much retention as possible is a good thing. The less we have to rely on information workers to manually apply a retention label, the better. The information architecture you've diligently defined in your tenant can now be leveraged using auto-apply conditions to automatically set an Office 365 retention label.

> Microsoft has announced machine learning trainable classifiers to help with the growing amount of corporate "dark data" (not within a well-defined information architecture). This will apply out-of-the-box and custom classifiers to intelligently apply retention across your tenant by classifying content based on meaning and context. These will not be covered in this post.

Licensing... the capability to auto-apply labels described in this post requires an Office 365 Enterprise E5 license for each user who has permissions to edit content that's been automatically labeled in a site. Users who simply have read-only access do not require a license. If you don't have the license for the auto-apply functionality or you have advanced logic to determine if a retention label should be applied that can't be done in the auto-apply condition, refer to another post of mine where I show an alternative way to automatically set a Retention Label using Microsoft Flow: [Setting a Retention Label in SharePoint from Microsoft Flow](https://joannecklein.com/2019/05/06/setting-a-retention-label-in-sharepoint-from-microsoft-flow/). This provides a lot of flexibility to include any kind of logic you may require to set the label.

Retention labels can be auto-applied based on 3 conditions:

* sensitive information types (both out-of-the-box and custom)
* keywords
* content types and metadata

This post describes the third option above to demonstrate the auto-apply behavior across several column data types and content types in SharePoint. Due to the fact that the retention label isn't applied immediately (controlled by a back-end process that runs ~once per week), this is not a quick test to do. I've spent the time testing this, so I'm sharing the results and learning with you! Please refer to the 'Important things to know' section at the end of this post for some key takeaways on this functionality. I will update the takeaways as I learn more.

#### Apply a Retention Label based on a Content Type

Content type called _Contract document_ has been added to a document library. Retention label called _Contract_ has been created and auto-applied based on the condition below:

**ContentType:'Contract document'**

The result? Within a week, any SharePoint site the retention label is published to had the _Contract_ retention label applied to all documents with the content type of _Contract document._

#### Apply a Retention Label based on a Choice Metadata column

A choice metadata column, _ContractType_, has been added to a library. I want to use one of the choice values to set a retention label. The auto-generated managed property from the search schema cannot be used in the auto-apply condition. You must manually map the crawled property to a RefinableString property (it's queryable). For this example, I've mapped the crawled property generated for metadata column, ContractType, to RefinableString00. Retention label called _Hardware_ has been created and auto-applied based on the condition below:

**RefinableString00:Hardware**

The result? Within a week, any SharePoint site the retention label is published to had the _Hardware_ retention label applied to all documents with a choice value of 'Hardware' on the _ContractType_ metadata column.

#### Apply a Retention Label on a compound condition

What about combining conditions? You can do this too! This test combined a content type name of _Contract document_ with a choice value of _Software._ A retention label called _Software_ has been created and auto-applied based on the condition below:

**ContentType:'Contract document' AND RefinableString00:Software**

The result? Within a week, any SharePoint site the retention label is published to had the _Software_ retention label applied to all documents with a content type of _Contract document_ and a choice value of 'Software' on the _ContractType_ metadata column.

#### Apply a Retention Label on a Date column <= Today

Can you include date logic in the condition? Yes. I have added an optional date column, _DateExpired_, to a library and want to apply the retention label once a date has been entered and is today or in the past. To filter on a date column, you must map it's crawled property to a _RefinableDate_ column (it's queryable), so in this case I mapped it to _RefinableDate01._ A retention label called _Expired Contract_ has been created and auto-applied based on the condition below:

**RefinableDate01<=TODAY**

The result? Within a week, any SharePoint site the retention label is published to had the _Expired Contract_ retention label applied to all documents when a date either equal to today or in the past has been entered into the _DateExpired_ metadata column. Note: if a date isn't entered in the column OR a future date is entered in the column, a retention label is not applied.

## Important things to know

Through my testing, I learned a few things that are important to understand and communicate to the Information Management team:

1. The back-end timer process to update the retention labels only runs weekly. If it is your expectation that the label will be updated soon after the metadata or content type is updated, this is incorrect. In tenants I've tested with, the process runs in the early hours of the morning (UTC-6) on Friday or Saturday mornings.
2. If a retention label is already applied on a document, the auto-apply process will NOT override/replace the label even if an auto-apply condition is met. Example: if you set the column _Contract Type_ to Software and this auto-applied a label to 'Software', and then you subsequently change the _Contract Type_ to Hardware, the label will not change to 'Hardware' if you had an auto-apply condition set to that. The original label, _Software_, would remain.
3. The columns filled in when the label is auto-applied are: _Retention label, Retention label applied,_ and _Label setting._ The _Label applied by_ is not filled in.
4. You can still manually remove the retention label by editing the properties. If you do this, the next time the back-end process runs, it will re-assess the document based on the auto-apply conditions and, if met, re-apply the correct label.
5. A simple way to test out your conditions before creating your label policies is to enter the query directly in the _Microsoft Search_ box thru the SharePoint UI. It will return the same results.
6. Although I've seen other posts where an auto-apply condition was based on a managed metadata term value, I believe this currently only works if the managed metadata column has been published from a Content Type Hub.

---

**Principal author**: [Joanne Klein, MVP](https://www.linkedin.com/in/joannecklein)
