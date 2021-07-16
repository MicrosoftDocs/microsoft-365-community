---
title: Understanding Power Platform Licensing
author: bigpix2000
date: 7/9/2021
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfellerer
ms.service: power-platform
description: "Understanding Power Platform Licensing"
ms.collection: M365Community
---

# Understanding Power Platform Licensing

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## Overview

This article shall give a direct and easy to understand overview about licensing/pricing in Power Apps, Power Automate and Power Virtual Agents along with the key features and services associated with them. It won't replace all other material posted across docs.microsoft.com but gives you, the reader, a solid understanding as which licenses apply to your solutions. This article focuses on Core Licensing Concepts and Levers along with guidance and licensing scenarios. The goal is to provide the citizen developer with the bulk of the information to make decisions on the spot or mitigate the research effort and time to confirm nuance cases or specialized use cases.  

Please note that the scope of this article excludes Azure, Office 365 and Dynamics 365 products as well as other licensing associated with third party connectors or services.

## Core Concepts

The last iteration of this article attempted to break down the original licensing guide into key concepts where important topics ended up being separated into the main applications in the same manner as the document itself and effectively duplicating information that was subject to frequent changes.  Rather than repeat published documentation, this section imparts initial guidance based on topics that span the three main Power Platform systems diving into some detail where they have impact on the others.  

There are key levers that are covered in this document that point to whether or not payment for a license is required or if use is included with something else as well as points where costs would be incurred such as for additional capacity.

The Core Concepts are as follows:

### Main Levers for licensing

The following summarize the main areas where licensing kicks in:

- Use of a Premium Connector: Generally, any use of a premium connector triggers the need for a license based on the product being used but there are notable exceptions such as the use of Dataverse in the context of a Microsoft Team.
- How a Flow is triggered: Flows with a premium connector have various launching options which are called triggers.  Flows launched from Power Apps will use the Power Apps license required in that case but will otherwise look for the applicable Power Automate license needed
- Use of Dynamics 365 Premium option or a Third Party paid service: Beyond the license fees are additional feels that come with the use of premium products from Microsoft or Third-Parties which will usually require additional analysis specific to those services.  The caveat for Dynamics 365 Premium services is that the costs may also infer additional capacity or abilities that would normally require a separate license for Power Apps or Power Automate.
- Use of additional services:  This one is a straight forward lever that tends to affect the tenant as a whole versus the individual user in that taking on the monthly subscription cost for the feature such as AI Builder or additional Dataverse capacity, adds to the cost for the organization and should be analyzed by breaking down the value over utilization amongst the apps and flow creators along with the users.
- Trials Expirations:  Another clear area is when there is a specific trial for a service such that the costs begin when those are finished.  Although M365 features are diligent with notifications, it is the responsibility of the administrators to keep close track of this.
- Individual versus "Bulk" usage:  The cost to do more generally comes with a premium but the common theme is that one would get a lot more when moving from one level to another (e.g. in Power Apps, going from two Apps on a basic use license to unlimited apps for a price point about 4 times the basic level)  

### Review the definitive licensing guide published monthly

Before going through the guidance, it is important to refer to the ultimate authority on licensing which has been updated on a monthly basis for several years now.  The licensing document may be download via links in Power Apps, Power Automate and Power Virtual agents' main pages and have maintained the following URL to point to the most current version for your language or region:

- <https://go.microsoft.com/fwlink/?linkid=2085130>

There are two important things to note in that PDF download.  

First is that changes from the previous versions will be noted in Appendix C, the Change Log, and should be the first point of reference after reading through articles such as this one or asking questions related to Apps, Flow or Bot changes since their implementation.  

The second item to note is that one will never see prices here as those will always be region specific in addition to being subject to specific customer licenses in general and directly with Microsoft or through a third party vendor. Prices and changes in prices will always reflect the underlying information contained in the download but be aware that not all tenants' Billing administrations screens will have a clear association as those screens may, for various reasons, contain important references to previous or deprecated products.

### Seeded vs Standalone

The most important concept that potentially simplified most licensing questions is the one of "Is it included with my Office 365/Dynamics 365 License?".

"Seeded" in this case relates specifically for "inclusion" to another license type even though, technically, Power Platform systems will always run in context of a Microsoft 365 tenant and have "limited use rights" which is a specification of what may be done at that level.  "Standalone" in this case means the license is not reliant on the other license type and it typically infers access to many more services that what is included with the main tenant.  

Since the rules for the tenant license type may change, it is recommended that a monthly review of Appendix B in the latest version of the license guide should be checked.  On that note, guidance offered as of this publication is that there has not been a significant change in the license types that are counted for inclusion and as of March 2021, the following license types are the main exceptions for general, limited use rights:

- Microsoft 365 F1
- Windows 10 Pro
- Windows Enterprise E3
- Windows Enterprise E5

Dynamics 365 licenses, as a rule, have always counted for at least "limited use rights" while more premium services where noted in the guide are more powerful and inclusive of some but not all premium features.

The biggest and most significant change in 2020 was the introduction of Dataverse (formerly Common Data Service or CDS) in Microsoft Teams as a separate and size limited environment where its use is considered included with the Seeded license rather than a Premium service requiring the Standalone license or premium Dynamics 365 seat.  This change is made even more significant because now Power Virtual Agents, a service that requires the use of Dataverse, now has a scenario free of additional charge outside of its monthly, capacity based cost.  

 The conclusion of this core concept is that answering the "is it Seeded" question is one where at a glance, the cost for use may be immediately clear especially if usage revolves around Microsoft Teams.  From here, the levers for determination become a case of applying layers of nuance from the specific seat licenses, to ways of running the solutions and then through more direct elements such as capacity and features.

### Standard versus Premium Data Connectors

If there is a main point of guidance that may be delivered at this stage, it is the one recommending the design of solutions to "make the most" of what comes out of box or included with Office 365 or the basic level of Dynamics 365 which includes considering Microsoft Teams as the lynch pin application.  This may mean making compromises for some usability or convenience but consider that the "cost" for avoiding the financial obligation for the organization or the users.

With that noted, business requirements and necessity will always drive the solution that is eventually used and the next question after the decision to use a Premium Connector will become the next nuance group around the scale of use by the specific Power Platform component. Also, keep in mind that some premium connectors, especially to third parties, may include their own costs for subscriptions or access.

### Power Apps "per app" versus "per user"

The question of scale in Power Apps is the difference of accommodating a single user to utilize a single app or unlimited apps. In the United States, the price point difference on a monthly basis is 4 times ($10/month/"one" app  versus $40/month/unlimited apps before October 2021 and $5/month/single app  versus $20/month/unlimited apps volume discounts notwithstanding). Although there is a capacity limited which will be discussed later, there is a key nuance that will be eliminated after October 2021 which is the case of "one app" package being two apps in any combination of canvas or model applications for the "single app" per use license. 

Although technically the price change reflects the same price for the single app, they key change to consider is that the unlimited version implies a signigicant price decrease when scaling out the usage and even for small groups to implement features such as the Center of Excellent Start Kit in its proper, non-trial form.  The choice of per app per user versus umlimited per user becomes easier to distinguish when the nuance is removed and limits the rest of the choices to decisions about capacity or services such as being able to access an "unlimited number" of custom portals or having more Dataverse space and make more API requests in a day.  The latest licensing guide will always clarify those differences as well as any new included features.  

It is important to remember that per app or per user does not limit the number of premium connectors that may be used but costs specific to those connectors will still apply.

### Power App with Power Automate

In the original introduction of the new licensing and as a consequence of the older model, it was thought that a separate license would be required for a Power App to use a Power Automate Flow when, in fact, it is only the cost of the Power App that will apply even if the Premium connector is only accessed via the flow.  The key guidance here is to understand the use case of the flow itself whether it is created to service the app or if it is the type that is expected to be shared or used outside of the application as it will then be a case of selecting the appropriate Power Automate license.

### Dataverse

Dataverse (previously known as Common Data Services / CDS) is one of the Premium connectors that is not seeded in Microsoft 365 licenses and requires a Power Apps or Power Automate Standalone license. Dataverse is also required when using Power Virtual Agents as well as data features in Dynamics 365 and, is in fact, originally the data storage solution introduced with Dynamics.  

Dataverse was intended to fulfill many requirements behind the support of business data with minimal data developer interaction.  Dataverse tables come with built in fields and automated processes supported by Microsoft to alleviate may of the day to day Database Administrator (DBA) duties one would find in an organization using MS SQL Server or other database platform.  In its original form, it came ready to support the productivity and business information in Dynamics and may now be used by the organization for their own data requirements.  It's use was considered PREMIUM in the same manner as connecting to a SQL Server connector due to the power afforded by the access.

The Premium connector designation resulted in a barrier when it came to power platform design decisions for data access. The seeded license aspect tended to drive data to SharePoint Lists or Excel Files which did not support data management best practices in the manner of a true database platform. SharePoint Lists could not be linked and joined in relationships as natively as a database table and data in Excel are potentially locked when being accessed by an application or process. The difference was not just a case of paying for convenience but also in accommodating critical business requirements in appropriate and well-performing ways. In those cases, the choice to not use the Power Platform over another custom solution because of cost was quite common.

Microsoft has recognized this blocker and has chosen to leverage Microsoft Teams as their own "starter" environments to promote usage and to consequently further adoption and perhaps innovation as the entry point for implementation now aligns with the same entry point for other Power Apps and Power Automate solutions even bringing in Power Virtual Agents which itself starts at a fairly steep monthly charge.  This core concept becomes important because not only can guidance now point to more appropriate solutions but because adoption will certainly drive the need to handle cases where more capacity and scale will be required but this time in the same context as other storage and capacity decisions covered here.

### Power Automate "per flow" versus "per user"

There is a major distinction in Power Automate over Power Apps when looking at the licensing unit.  Where Apps look at usage in all cases, Flow licenses are split between the permission to CREATE unlimited flows per use or to Implement specific flows to SERVE unlimited users.  These are two very different bases where the first effectively gives a single user the "All you can Eat" power for the main licence while the other is the case of a SET of Flows packaged for the organization to be used anywhere and in any and all context.

The manner of how a Flow is TRIGGERED potentially makes the decision.  Flows triggered from a Power App are included in all cases as it assumes the premium connector will be part of the app itself.  Flows that do not touch premium connectors or who are triggered from non premium sources such as SharePoint lists and MS Forms will also not count for extra cost.  If none of these conditions apply, it is now a case of the person who created the flow as the designated licensee where the act of getting licensed effectively allows that user to create any number of flows they wish assuming the flows only serve the purpose of the user and is not shared with others.

A common question is if a Flow is created for a SharePoint List and many users interact with that list, will there be a cost for all the users.  The answer is if the Flow uses a premium connector such as call to a Dataverse table in a non-Teams or non-Development plan environment, the cost of the flow must either be for each user or a per flow license is used so that all users of the list may be serviced by it. Conversely, if there are no premium connectors being called, there is no additional cost as the Flow is included with the users' Office 365 seat as a case of having a "seeded license" noted earlier.     

As a guidance for the "per flow" cases, remember that the initial license starts with 5 flows and may be increase one flow at a time at a cost about 7 times to cost for an individual license.  The expectation is that larger organizations or solutions that affect many will benefit from the fixed monthly cost versus a comparable per use cost in a pure Azure function.

### Additional Power Automate Flow licensing guidance

1. Use Standard connectors in Office 365 licenses when possible in all cases.  

2. For Automated Triggers - buy a full license for the Flow Owner (Flow Bundle or User) and watch number of runs in case additional API run capacity needs to be purchased. A goal here is to potentially limit the requires licenses to one or two at most.

3. For Instant Triggers - buy a full license for each user that will invoke the specific flow if it requires a connector not included with the seeded applications (Office 365, Dynamics) or is premium. The choice point of per user versus Bundle flow will be the cost per flow. This can be the more complex decision as considerations must be made against the cost per user running up against the cost for Flow Bundles which start at 5 and increment by 1.  

4. In the case of the Power Apps Trigger (a type of Instant Trigger) - the most common Instant Trigger is the **Power Apps trigger**, but any Power App that calls a Power Apps Trigger must have premium license for the premium connector used in the Flow and the Power Apps premium license for the end user includes premium flows used as part of that Power App. In this particular case additional purchases of flow licensing are not necessary, since it must be included in the Power Apps premium license.

### Purchasing Capacity and Storage

The Power Platform is made very viable through the option of "the Add-in" where storage and capacity may be purchased to fill gaps in those areas.  The main difference for this type of A la Carte service over platforms like Azure is that the extras are purchased as a package rather than a case of "pay as you go" or as usage charges.  Power Virtual Agents provide capacity in the same block as its initial monthly license cost.  Power Apps and Power Automate are optimized by preset support expectations such as a daily limit on API calls or a reserved storage area.

This concept is the impetus for guidance recommending the reviewing usage and capacity from the Power Platform administration areas and to be at least familiar with the reports and dashboards if not adding the review to the regular course of operations.

Storage and Capacity are considered tenant wide resources and when deciding cost impact, they should be considered in those terms as they can make a difference if the user case is to support a single user's application versus one for the larger organization. On that point, add ins such as AI Builder work in the same way where the ability is added at the tenant level and where the benefit could be seen as one for the whole organization being served or for the organization to serve a specific need.  

### Trials and Free Services

A question that has arisen for users who want to evaluate or learn elements of the Power Platform is how much that effort may cost and it may sometimes be a hindrance to those outside the people specifically licensed.  It is important to note that there are always trials and services provided by Microsoft to mitigate this from direct 30 day trials using the Power Platform to implementing a development environment via the technical community resources as well as to obtaining a personal Developer Tenant where the user has nearly all the power as an E5 tenant level organization.  The ability to move what has been learned or separately developed into the production organization is being enhanced constantly by Microsoft and the community, the latter of which provides not just samples but process knowledge and guidance. Checking in with a community contributor on whether a solution has a license impact is a good way to fast track decision making in this regard especially if significant time has passed since the contribution.

The important piece to note in this concept is that although there will always be ways to "try things out", those ways will have limitations, the least being time.  A Developer tenant user will still need to pay for the use of Power Platform after the specific trial period is over and even though the current policy for the tenant may be an automatic 90 day renewal based on usage.  Taking advantage of "free" services is certainly recommended but it is good to keep a close eye on articles like this to be prepared for costs that may have to be incurred.  

See the guidance section below on more information using the Developer Plan.

### The Power Virtual Agent Subscription

Outside of MS Teams, a major concept in Power Platform is the one of the subscription which is similar to storage, capacity and Add-ins in that they are at a tenant level billed to the organization as a whole and not by individual.  Just like storage and capacity, there is a limit to usage where going over can be accommodated by purchasing capacity or another license which stacks on to the original.  There is some uncertainty, however, for Power Virtual Agents as to the exact manner it uses that capacity and although the licensing guide is very clear on the units of use, there is no current map or list that directly assigns an activity by the underlying AI system to a specific number of units.  It is because of that that usage analysis is very important especially at the end of a trial or single month but, at least for this time, on an on going, monthly basis with an eye on the bot solutions themselves.

Guidance at this stage reiterates implementation via MS Teams if that is the appropriate delivery host but if it is not, guidance calls for making the most of the enabled feature to being down the ROI costs.  Refer to the guidance section here for more on cost comparisons.

Finally on this concept, when looking at the information in the licensing document, note that there are storage and capacity assumptions when implementing this in either production or in a MS Teams environment so be sure to include that information in design decisions.  

## Guidance

Some guidance has been covered as part of the Core Concepts discussions of the previous sessions.  This section covers additional as well as contributed guidance notes that underscore or clarify key points for decisions based on licensing.

### Do your Apps/flows in Teams wherever possible to be able to use Dataverse with no additional cost

If you need Dataverse, let your Power Automate flows and Power Apps live in Microsoft Teams, because this way you can use the power of Dataverse as Dataverse for Teams which means that the license is included in your Microsoft 365 license. You should pick Dataverse for Teams over other other premium connectors, especially in enterprise-scale applications, because it is the preferred way to store your data, see also [Considerations for optimized performance in Power Apps](https://powerapps.microsoft.com/blog/considerations-for-optimized-performance-in-power-apps/). When you are very experienced in Microsoft 365, you will probably consider to store data in SharePoint lists, also as SharePoint is a standard connector, which means that you don't need a Power Apps Standalone license, but Dataverse has more capability, is faster and doesn't have issues like "only 12 complex columns in one view", 5000 items threshold and more.

### To learn Power Platform, use the Developer Plan

There is a [free Developer Plan to learn Power Platform](https://powerapps.microsoft.com/developerplan/). This was formerly a community plan that was limited to personal use with the updated version geared to work with a small team albeit not allowed for use in production. With it, premium connectors are available but there will be specific limitations especially with capacity. This is demonstrated in attempts to install the Center of Excellence Starter Kit into an environment created with the developer plan where required starter flows will fail to run as the Power Apps licence, either as a true trial or as production will be required.  

Please note that you can use this plan in a free [Microsoft 365 developer tenant](https://developer.microsoft.com/microsoft-365/dev-program) but the caveats of capacity may require at least one paid license.

### Think Governance early with Center of Excellent Starter Kit (CoE)

The [Center Of Excellence (CoE)](https://powerapps.microsoft.com/en-us/developerplan/) Solution available from Microsoft and supported by the community is an excellent way to control and manage not just the solutions but the costs related to licensing.  As stated earlier, it requires a license to run because many of its functions exceed the limitations allowed by the "free" version of dataverse in teams or a developer plan environment. The features go well beyond tracking and management especially in medium to large organizations that want to mature in the use of the technology through adoption, fusion development and solution reusability. 

For the purposes of licensing guidance, key reports included specifically note active and inactive environmentments, applications, flows and license seats and the ability for admininstrators to quickly maintain things at the tenant level. Using the kit to the full potential or a similar system from the markateplace is highly recommended.  

For the purposes of learning the Power Platform in a Developer tenant by an individual, the license cost could be considered a very important decision.  Guidance suggests groups team up on a tenant to spread the cost or else weigh the current situation that a trial will give you only 30 days to work with the kit in a "live" environment.  Beyond that, it is a case of the more advanced Power Platform developer to leverage the kit's source code available in GitHub and make the changes to mitigate as much of the functionality as possible, e.g. changing data sources from Dataverse to SharePoint or throttling the data gathering purposely to fall within capacity limits.     

### Deciding to use Premium Connectors over Standard Connectors - Pricing your solution

As noted earlier, all efforts to work within the Standard Connector list or within Teams in the context of Dataverse is highly recommended but as highlighted by the change Microsoft itself made to make Dataverse more accessible via teams, there will be use cases where the work around is more painful and potentially more expensive through added user effort (their time is money) or delicate processes where small errors or lost time can affect direct financial impact.  

A case in point would be a case where the act of avoiding the premium HTTP API connector to get critical information from a third party service just to avoid the per user or per app fee when creating the custom application to put the information into a dashboard in teams or SharePoint might cost more to develop and maintain or even to run as a "pay as you go" service in Azure.  With that hypothetical scenario, the key point is to know how to price the competing solutions.  The Licensing guidance for Power Platform is direct at giving cost for the organization while tools such as the Azure Calculator will help pin down infrastructure level costs. The Wild card is now the development cost for either creating the Power Platform solution with rapid development tools and lower developer cost or the enterprise developer team using premium tooling and techniques that would need separate Service Level Agreements that are part of the Power Platform licenses.

In this last point, guidance calls for looking at the complete picture and not just the license effect of a single implementation and a note that the tools to do so are readily available.

## Other Important Licensing Links

The following key links will redirect to the top-level pricing summary for the three licensing groups:

- For Power Apps
  - [https://powerapps.microsoft.com/pricing/](https://powerapps.microsoft.com/pricing/)
- For Power Automate
  - [https://us.flow.microsoft.com/pricing/](https://us.flow.microsoft.com/pricing/)
- For Power Virtual Agents (new!)
  - [https://powervirtualagents.microsoft.com/](https://powervirtualagents.microsoft.com/)

You may be asked to sign into your tenant or live.com account to view the information which will reflect your region.

## Scenarios from the Field

This article is meant to be a living and growing document that includes contributions of the community to help with decisions and understanding.  Sometimes, in spite of core concepts and guidance, there are nuances that may be used to either drive home knowledge or give pause and provide additional even if nuanced factors for consideration. We welcome your contributions to help fill out this section while adding a last piece of guidance to return here as often as you need to update the main licensing document to stay ahead and on top of this topic.

### Practical Application from the field - The case of a SharePoint List and a Flow that uses a premium connector

SharePoint Lists online are very inviting to users who would automate work based on activity in the list but the worry tends to be whether or not licenses will be need to all the users who interact with the list or for the individual who created the flow.  

The first trigger is whether or not the flow touches a premium connector and, in this case we have agreed that one is being used.  The next trigger is the fact that the SharePoint list activity is the reason behind the run.  Looking at our guidance, we should see that running from the flow from SharePoint would not cost the users but the flow itself as created by the individual would require one as it touches a premium connector item.

Simply put, if 5000 people write to a SharePoint list and there is a SharePoint automated trigger that runs a premium flow license, only 1 premium license is required on that flow.

Taking this a step further, we take that user who created the single flow for that single list, do similar things to other SharePoint lists.  The guidance shows that once a user gets a license to create flows, they can make as many as they want for that single cost.

If that user shared their flow with another user who then leveraged it to make their own flow, then that new user would require a license.

If you were to analyze this versus the cost for a Logic App in Azure, consider that the trigger itself will already start incurring usage charges albeit in small amounts but will certainly add up each and every time the SharePoint list activity prompts the app whether or not the app "decision" mores things forward or not.  

A warning on this example is if the premium service in question talks to a system such as SQL server in a data center or "on-premise", the use of the single license may save money there but the organization would still need licenses for all the users likely to make the updates in a situation that is covered by multiplexing rules.  

The lessons we take away from this example are as follows:

- Keep things simple
- Avoid premium connectors if possible
- Limit Flow creation to one, a few users or a "service account" type user.
- Avoid multiplexing situations
- Logic Apps may not be cheaper

### The Case of the Power Automate Flow that calls another Flow

In this case, a user who creates a flow, needs to call another flow and does so via a HTTP connector. As the Premium Connector trigger comes in, the question may be whether the second flow that may not be created by the initial user, will require an additional license for that user and, in this case, there is a nuance in the licensing document that states that a "flow" counts as a single unit no matter how many times it hops from one to another. Essentially, the complete action is the flow and therefore the "single" activity.  

This scenario underscores the case where an organization may purchase a Flow pack for unlimited use by all or if they will be fine with the single user license.

The main take away from this example is that flows can be modularized rather than created as overly large and difficult to maintain projects just to save on license costs

### Approvals

For Apps or flows that require participation by users beyond the creator of the app or flow, would there be additional licenses required?  The general answer is no if the approval activity involves Power Automate flows which considers the activity as "standard" no matter how fancy the approval response request is.  Again, the regular triggers for a license such as a premium connector, come into play here and the nuance would be additional costs incurred by a third party system that may be part of the activity such as SAP or SQL Server.

As a point of guidance as of this writing, there are approval features now included with MS Teams that mitigate the need to even design these type of workflows and their inclusion with teams is more likely to end up with no additional licensing costs.

---

**Principal author**: [Ralph Rivas](https://www.linkedin.com/in/ralphrivas/)

**Principal contributor**: [Luise Freese](https://www.linkedin.com/in/luisefreese/)

---
