---
title: Use the Government Cloud for SharePoint and Microsoft 365
ms.date: 10/30/2022
author: PatD
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: sharepoint-online
localization_priority: 
description: "A quick knowledge primer for site owners and Microsoft 365 experts on working in the M365 government cloud."
ms.collection: M365Community
---
# Use the Government Cloud for SharePoint and Microsoft 365

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

Working for the government can be a privilege, a job that comes with a feeling of pride and satisfaction in working on behalf of your fellow citizen. If you're a SharePoint site owner or Microsoft 365 expert who's working in the United States government (Federal, state, local or Tribal) you may be working in the _government cloud._ Read on to learn about what that means to you and to your customers.

## Why have a government cloud?

**Regulatory compliance!** The governing agencies of the United States have different rules and policies than the private sector. Microsoft 365's `GCC`, `GCC-High`, and `DOD` cloud offerings were purpose-built to meet these compliance requirements… all while still giving you a modern collaboration, document storage, and development space.

[Microsoft's landing page](https://www.microsoft.com/microsoft-365/government) on the topic describes it like this:
>_"Federal, State, and Local U.S. Government agencies, as well as commercial companies, holding controlled unclassified information, criminal justice information, and export-controlled data will find that Microsoft 365 Government offers the most robust set of capabilities while meeting necessary regulatory controls."_

Also worth noting:

- Your SharePoint and M365 content is kept separate from commercial tenant content, and is stored within the United States.

- Microsoft personnel who can access your tenant are restricted to those screened for it.

## Am I working in the government cloud?

It might be hard to tell by _looking_ at a SharePoint site or Microsoft Team that you're in the government cloud. If you're a Microsoft 365 expert or SharePoint site owner who's been handed a site or a Team to manage, the easiest way to tell is to check your account license. If it starts with a "**G**" then you're in the government cloud.

To check, head to [https://portal.office.com/account/](https://portal.office.com/account/) and click on 'View Subscriptions'. If you're working in the government cloud, you should see something like `Microsoft 365 G3 GCC` or `Microsoft 365 G5 GCC-High`. That means that you're a user who is licensed to work in a government cloud tenant.

For more context on licenses, review the [Microsoft Government Cloud License Types](https://www.microsoft.com/microsoft-365/government/compare-office-365-government-plans) chart.

## Working on it - new features

One the benefits of having SharePoint and Microsoft 365 in the cloud is that new features and tools show up regularly. This is true in the government cloud as well... with the caveat that many new features must be vetted and approved for compliance before you get access to them.

Not every feature that's available in the commercial M365 offerings will be available in the government cloud on day one, and those that do become available might involve waiting a bit longer to get.

In order to maintain compliance, _new_ features and functionality need to be certified for your government cloud instance. This certification might mean waiting six months to a year or more for new functionally or occasionally not getting the new feature at all (especially in `GCC-High` and `DOD`).

- For high level availability context, check out the [Microsoft Government Cloud Feature Availability](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#platform-features) table.

- For monthly updates, bookmark the [Microsoft Business Applications Product and Feature Experience Parity](https://aka.ms/BAPFunctionalParity) PDF report.

### The waiting is the hardest (web)part

Be prepared for some frustration from your end-users about waiting for new features – they'll read about the latest new Teams capability or Power Automate Connector and expect to see it in your government cloud environment on launch day. More likely than not, the task will land on _you_ to share context about the feature availability difference between commercial and government clouds.

To stay up to date on what's headed your way:

1. Bookmark the [Microsoft 365 Road Map](https://www.microsoft.com/microsoft-365/roadmap?rtc=1&filters=DoD%2CGCC%2CGCC%20High%2CIn%20development%2CRolling%20out) and tune it to to the government cloud.

2. Set the _Cloud Instance_ to match your tenant (`GCC`, `GCC-High`, or `DOD`) and toggle "In development" or "rolling out". Remember that the dates provided are _estimates._

3. The Road Map has an [_RSS feed_](https://www.microsoft.com/microsoft-365/RoadmapFeatureRSS/) so you can stay up to date and changes.

## Watch your URLs

Another sign that you're working in the cloud – some of your M365 URLs might be different than the commercial M365 equivalents. This means paying a little more attention to the documentation and tutorials you share with your customers. Customers may get confused if they try to log in to a commercial tenant URL with their government cloud credentials.

For example, while your friends in the banking sector might build their Power Apps at the commercial tenant URL of [https://make.powerapps.com](https://make.powerapps.com/), you'd be making yours at [https://make.gov.powerapps.us](https://make.gov.powerapps.us/) (`GCC`), [https://make.high.powerapps.us](https://make.high.powerapps.us/) (`GCC-High`), or maybe even in [https://make.apps.appsplatform.us](https://make.apps.appsplatform.us/) (`DOD`).

## Work with support staff, trainers, and vendor partners

When seeking out support in your government cloud tenant, be it formally with a service provider or informally on social media and forums, you'll have a better time if you mention that your Microsoft 365 tenant is in the government cloud. (You can even share this article to get them up to speed!).

Specifying your specific government cloud type (`GCC`, `GCC-High`, `DOD`) will help align support guidance with your environment.

Vendors selling web parts, support, training content, and Teams apps won't always be fully aware of the differences in the government cloud. Insist they demonstrate awareness and understanding of the Microsoft 365 government cloud before making a purchase.

## Government cloud developers

If you've got development chops in the Microsoft space, you should understand how working in the government cloud will impact your code and applications. Tokens, registration of apps, and endpoint URLs could be different. Your specific government agency may have unique requirements for deploying apps. Documentation written for the commercial tenants might not apply to you.

Here are some resources to help guide you:

- [Microsoft Graph Powershell examples for government](https://github.com/microsoft/Federal-Business-Applications/tree/main/demos/powershell-gov-samples#microsoft-graph-powershell)

- [Microsoft National Cloud Deployments guide](/graph/deployments)

- [Azure government cloud documentation](/azure/azure-government/documentation-government-welcome)

- [DOD endpoints](/microsoft-365/enterprise/microsoft-365-u-s-government-dod-endpoints)

- [GCC-High endpoints](/microsoft-365/enterprise/microsoft-365-u-s-government-gcc-high-endpoints)

- [GCC (and worldwide) endpoints](/microsoft-365/enterprise/urls-and-ip-address-ranges)

## Buying your own government cloud tenant

Unlike a personal or business M365 subscription, you can't decide one afternoon to buy your own government cloud M365 tenant. You'll need to work with Microsoft to demonstrate that _yes, you are part of a government entity._ [Learn How to buy Microsoft 365 Government
](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/microsoft-365-government-how-to-buy#how-do-i-buy-microsoft-365-government).

### Planning your deployment

If you're starting from scratch with a new tenant, these guides for each type will help you roll out your first government cloud deployment.

- [Plan for Microsoft 365 Government - GCC deployments](/microsoftteams/plan-for-government-gcc)
- [Plan for Microsoft 365 Government - GCC-High deployments](/microsoftteams/plan-for-government-gcc-high)
- [Plan for Microsoft 365 Government - DOD deployments](/microsoftteams/plan-for-government-dod)

### Detailed learning

When you're ready to learn more, start with the **Service Description**, as it details what it means to operate Microsoft 365 in the government cloud. [Office 365 Government](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#about-office-365-government-environments).

Then for specific guidance, review the [SharePoint for US governments](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/sharepoint), [OneDrive for US governments](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/onedrive), and [Teams for governments](/microsoftteams/expand-teams-across-your-org/teams-for-government-landing-page) guides.

>[!NOTE]
>Government cloud offerings might not be the right call for **educational** customers. Learn more about M365 educational offerings here: [Office 365 Education](/office365/servicedescriptions/office-365-platform-service-description/office-365-education)

## Community support and learning

A shared affinity for public service helps technologists, developers, site owners, and M365 experts working in the government cloud to support one another. These resources can get you answers quickly from people with similar government cloud configurations.

- [Microsoft Public Sector Community](https://techcommunity.microsoft.com/t5/public-sector/ct-p/PublicSector)

- [Microsoft Public Sector Blog](https://techcommunity.microsoft.com/t5/public-sector-blog/bg-p/PublicSectorBlog) [[RSS](https://techcommunity.microsoft.com/plugins/custom/microsoft/o365/custom-blog-rss?tid=336335429204089405&board=PublicSectorBlog&size=25)]

- [Social media – mention your government cloud instance with these hash tags](/microsoft-365/community/microsoft-365-on-social-media)

- [M365 User Group of Washington DC](https://www.meetup.com/m365dc/)

- [Government Community Call – AvePoint Public Sector](https://www.youtube.com/playlist?list=PLyJFOtpJV3wNOExhHa6Uo5XLieb0RC_EW)

Thanks to these community members for article input: _Adrienne Andrews, Ed Bellman, Sean Bugler, Jason Byrd, Nate Chamberlain, Joseph Dunn, Christophe Humbert, Naveen Karla, Matt Wade, Fred Yano_.

---

**Principal author**: [Patrick M. Doran](https://www.linkedin.com/in/PatrickDoran)
