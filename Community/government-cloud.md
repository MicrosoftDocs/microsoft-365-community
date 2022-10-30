---
title:  Working in the Government Cloud with SharePoint and Microsoft 365
ms.date: 10/30/2022
author: PatD
ms.reviewer: 
manager: 
ms.topic: article
ms.author: 
ms.service: sharepoint-online
localization_priority: 
description: "A quick knowledge primer for site owners and Microsoft 365 experts on working in the M365 government cloud."
ms.collection: M365Community
---
# Working in the Government Cloud with SharePoint and Microsoft 365

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

Working for the government can be a privilege, a job that comes with a feeling of pride and satisfaction in working on behalf of your fellow citizen. If you're a SharePoint site owner or Microsoft 365 expert who's working in the United States government (Federal, State, Local or Tribal) you may be working in the _government cloud._ Read on to learn about what that means to you and to your customers.

## Why do we have a government cloud?

**Regulatory compliance!** The governing agencies of the United States have different rules and policies than the private sector. Microsoft 365's GCC, GCC-High, and DOD cloud offerings were purpose-built to meet these compliance requirements… all while still giving you a modern collaboration and development space.

[Microsoft's landing page](https://www.microsoft.com/en-us/microsoft-365/government) on the topic describes it like this:
_"Federal, State, and Local U.S. Government agencies, as well as commercial companies, holding controlled unclassified information, criminal justice information, and export-controlled data will find that Microsoft 365 Government offers the most robust set of capabilities while meeting necessary regulatory controls."_

**Required reading:** The Service Description goes into detail on what it means to operate Microsoft 365 in the government cloud.

[https://learn.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#about-office-365-government-environments
](https://learn.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#about-office-365-government-environments)

Also worth noting:

- Your SharePoint and M365 content is kept separate from commercial tenant content, and is stored within the United States.

- Microsoft personnel who can access your tenant are restricted to those screened for it.


**Back to school:** Government cloud offerings might not be the right call for educational customers. Learn more about educational offerings here: [https://learn.microsoft.com/en-us/office365/servicedescriptions/office-365-platform-service-description/office-365-education](https://learn.microsoft.com/en-us/office365/servicedescriptions/office-365-platform-service-description/office-365-education)

## Am I working in the government cloud?

It might be hard to tell by just _looking_ at a SharePoint site or Team that you're in the government cloud. If you're a Microsoft 365 expert or SharePoint site owner who's been handed a site or a Team to manage, the easiest way to tell is to check your account license. If it starts with a "G" then you're in the government cloud. If it starts with another letter, you're probably not.

To check, head to [https://portal.office.com/account/](https://portal.office.com/account/) and click on 'View Subscriptions'. If you're working in the government cloud, you should see something like "Microsoft 365 G3 GCC" or "Microsoft 365 G5 GCC-High". That means that you are a user who is licensed to work in a government cloud tenant.

**Recommended Reading:** To compare the different government cloud license types check out this comparison chart: [https://www.microsoft.com/en-us/microsoft-365/government/compare-office-365-government-plans](https://www.microsoft.com/en-us/microsoft-365/government/compare-office-365-government-plans)

## The waiting is the hardest (web) part

One the benefits of having SharePoint and Microsoft 365 in the cloud is that new features and tools show up regularly. This is true on the government cloud as well, but with the caveat that many new features must be vetted for compliance before you get them. Not every feature that's available in the commercial M365 offerings will be available in the government cloud, and those that are available might involve waiting a bit longer to get.

Recommended reading: Government Cloud Feature Availability chart
[https://learn.microsoft.com/en-us/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#platform-features](https://learn.microsoft.com/en-us/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#platform-features)

In order to maintain compliance, new features and functionality need to be certified for your government cloud instance. This certification might mean waiting six months to a year or more) for new functionally or – occasionally -never getting it at all (especially in GCC-High and DOD).

Be prepared for some frustration from your end users about this – they'll read about the latest new Teams functionality or Power Automate Connector and expect to see it in your environment on launch day.

**Recommended Reading:** The Microsoft 365 Road Map, tuned to the government cloud
 Set the Cloud Instance to match your type (GCC, GCC-High, or DOD) and toggle "In development" or "rolling out" to see what's headed your way. Remember that the dates provided are _estimates._
[https://www.microsoft.com/en-us/microsoft-365/roadmap?rtc=1&filters=DoD%2CGCC%2CGCC%20High%2CIn%20development%2CRolling%20out](https://www.microsoft.com/en-us/microsoft-365/roadmap?rtc=1&filters=DoD%2CGCC%2CGCC%20High%2CIn%20development%2CRolling%20out)

_Pro tip: The road map has an_ [_RSS feed_](https://www.microsoft.com/en-us/microsoft-365/RoadmapFeatureRSS/)_! If your Power Automate setup includes the RSS connector, create a flow that emails or Teams-messages you when updates are made._

## URLs matter

Another sure-fire sign that you're working in the cloud – some of your M365 URLs might be different than the private sector ones. This means paying a little more attention to the documentation and tutorials you share with your customers. They may get confused if they try to log in to a commercial tenant M365 URL with their government cloud credentials.

While your friends in the banking sector might build their Power Apps in the commercial tenant URL of [https://make.powerapps.com](https://make.powerapps.com/), you might be making yours in [https://make.gov.powerapps.us](https://make.gov.powerapps.us/) (GCC), [https://make.high.powerapps.us](https://make.high.powerapps.us/) (GCC-High), or even in [https://make.apps.appsplatform.us](https://make.apps.appsplatform.us/) (DOD).

## Government cloud developers

If you've got development chops in the Microsoft space, you should understand how that impacts your code and applications. Tokens, registration of apps, and endpoint URLs might be different. Your specific government agency may have unique requirements for deploying apps. Documentation written for the commercial tenants might not apply to you.

Here are some resources to help guide you:

- Microsoft Graph Powershell examples for government
[https://github.com/microsoft/Federal-Business-Applications/tree/main/demos/powershell-gov-samples#microsoft-graph-powershell](https://github.com/microsoft/Federal-Business-Applications/tree/main/demos/powershell-gov-samples#microsoft-graph-powershell)


- National Cloud Deployments
[https://learn.microsoft.com/en-us/graph/deployments
](https://learn.microsoft.com/en-us/graph/deployments)

- Azure government cloud documentation
[https://learn.microsoft.com/en-us/azure/azure-government/documentation-government-welcome
](https://learn.microsoft.com/en-us/azure/azure-government/documentation-government-welcome)

- DOD endpoints
[https://learn.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-u-s-government-dod-endpoints
](https://learn.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-u-s-government-dod-endpoints)

- GCC-High endpoints
[https://learn.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-u-s-government-gcc-high-endpoints
](https://learn.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-u-s-government-gcc-high-endpoints)

- GCC (and worldwide) endpoints
[https://learn.microsoft.com/en-us/microsoft-365/enterprise/urls-and-ip-address-ranges](https://learn.microsoft.com/en-us/microsoft-365/enterprise/urls-and-ip-address-ranges)

## Working with support staff, trainers, and vendor partners

When working with support, be it formally with a service/support provider or informally on social media and forums, you'll have a better time if you mention that your Microsoft 365 tenant is in the government cloud. (You can even share this article to get them up to speed!). Specifying your specific government cloud type (GCC, GCC-High, DOD) will help align support guidance with your environment.

Vendors selling web parts, training content, and Teams apps won't always be fully aware of the differences in the government cloud. Insist they demonstrate awareness and understanding of the government cloud differences before making a purchase.

## Getting started: Buying your own government cloud tenant

Unlike a personal or business M365 subscription, you can't decide one afternoon to buy your own government cloud M365 tenant. You'll need to work with Microsoft to demonstrate that _yes, you are part of a government entity._ Learn about the process here:

[https://learn.microsoft.com/en-us/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/microsoft-365-government-how-to-buy#how-do-i-buy-microsoft-365-government
](https://learn.microsoft.com/en-us/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/microsoft-365-government-how-to-buy#how-do-i-buy-microsoft-365-government)

**Recommended Reading:** Planning your deployment.
 These guides for each tier will help you roll out your first government cloud deployment.

[https://learn.microsoft.com/en-us/microsoftteams/plan-for-government-gcc

](https://learn.microsoft.com/en-us/microsoftteams/plan-for-government-gcc)[https://learn.microsoft.com/en-us/microsoftteams/plan-for-government-gcc-high

](https://learn.microsoft.com/en-us/microsoftteams/plan-for-government-gcc-high)[https://learn.microsoft.com/en-us/microsoftteams/plan-for-government-dod](https://learn.microsoft.com/en-us/microsoftteams/plan-for-government-dod)

##
 Community support and learning

A shared affinity for public service helps technologists, developers, site owners, and M365 experts working in the government cloud to support one another. These resources can get you answers quickly from people with similar government cloud configurations.

- Microsoft Public Sector Community
[https://techcommunity.microsoft.com/t5/public-sector/ct-p/PublicSector
](https://techcommunity.microsoft.com/t5/public-sector/ct-p/PublicSector)

- Microsoft Public Sector Blog
[https://techcommunity.microsoft.com/t5/public-sector-blog/bg-p/PublicSectorBlog](https://techcommunity.microsoft.com/t5/public-sector-blog/bg-p/PublicSectorBlog) [[RSS](https://techcommunity.microsoft.com/plugins/custom/microsoft/o365/custom-blog-rss?tid=336335429204089405&board=PublicSectorBlog&size=25)]


- Social media – mention your government cloud instance with these hash tags
[https://learn.microsoft.com/en-us/microsoft-365/community/microsoft-365-on-social-media
](https://learn.microsoft.com/en-us/microsoft-365/community/microsoft-365-on-social-media)

- M365 User Group of Washington DC
[https://www.meetup.com/m365dc/
](https://www.meetup.com/m365dc/)

- Government Community Call – AvePoint Public Sector
[https://www.youtube.com/playlist?list=PLyJFOtpJV3wNOExhHa6Uo5XLieb0RC\_EW](https://www.youtube.com/playlist?list=PLyJFOtpJV3wNOExhHa6Uo5XLieb0RC_EW)

---

**Principal author**: [Patrick M. Doran](https://www.linkedin.com/in/PatrickDoran)