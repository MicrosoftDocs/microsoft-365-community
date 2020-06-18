---
title: Understanding Power Platform Licensing
ms.date: 3/16/2020
author: bigpix2000
ms.reviewer:  Joanne Hendrickson
localization_priority: 
description: "Understanding Power Platform Licensing"
ms.collection:  SPCommunity
---
# Understanding Power Platform Licensing

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## Overview

### About this article

In October 2019 and just before Ignite, Microsoft initiated changes to the licensing plans for the systems known as the Power Platform applications.  The action led to some confusion among the community with administrators and users in Office 365 tenants even as those changes were not going to be immediate for many.  Understanding the full implications for many scenarios required in depth looks into the documentation that came along side it and in that time, there were few people outside of Microsoft who understood things enough to allay fears that the changes were going to up end usage or increase bills suddenly and significantly.  This article seeks to address that gap from the power user (usually referred to as the Citizen Developer) point of view.

### Scope of this article

The information covered here summarizes the information found in the official and definitive Licensing Guidance found here: [https://go.microsoft.com/fwlink/?linkid=2085130](https://go.microsoft.com/fwlink/?linkid=2085130).  The guide addresses Power Apps Power Automate and Power Virtual Agents and not nuances based on organizational or regional Enterprise Agreements (EA&#39;s) or contracts. It also does not cover pricing for Azure, Office 365 or Dynamics 365 products and services but it will discuss the effects of those services regarding understanding the topics included here.

### Importance of Licensing Information

From the point of view of the citizen developer or organization power user creating applications, flows or virtual agents, the cost of service could affect what they are able to do and to what extent.  Work with these systems occurs in the tenant shared with others and whether the solutions being built are for individual or broad use, it is important to understand the complete impact of operations in the same vein as performance or net benefits.

Unless the developer also has tenant administration access rights, they may have to request explicit permission to use things like premium connectors which may or may not entail license purchases depending on the context of their implementation.   Knowing these ahead of time makes it easier to make the request and justify it as well.

In the end, the goal of the developers work is to provide a solution that satisfies a requirement or need and just as selecting the appropriate elements and configuration settings, so too is selecting or requesting the appropriate license so that the solution can be implemented and utilized.

## Licensing Core information

### Preface to the information

It may appear counter intuitive for the licensing guide not to include prices but the main reason behind that is to provide a common set of information that is not associated with a specific region, EA license arrangement or individual contract. Prices will differ from region to region if at least with the default currency. Availability can also be an issue for certain agreement types such as Government or Education in addition to regions.  Though this guide will give a certain starting point using US dollars as the reference, it is recommended that the Power app, flow or virtual agent creator discuss first with tenant administration and the applicable stakeholders the licensing issues as part of appropriate governance procedures.

A major difference from before the change in October 2019 is how Data API Request limits were handled.  The old licensing model had monthly caps albeit allowing the purchase of additional capacity.  The new one no longer has monthly limits but instead caps daily use at numbers per day higher than the old monthly limits in some cases.  The ability to purchase capacity for the requests and for data storage is still available.

### Key links

The following key links will redirect to the top-level pricing summary for the three licensing groups:

- For Power Apps
  - [https://powerapps.microsoft.com/pricing/](https://powerapps.microsoft.com/pricing/)
- For Power Automate
  - [https://us.flow.microsoft.com/pricing/](https://us.flow.microsoft.com/pricing/)
- For Power Virtual Agents (new!)
  - [https://powervirtualagents.microsoft.com/](https://powervirtualagents.microsoft.com/)

You may be asked to sign into your tenant or live.com account to view the information which will reflect your region e.g. [https://powerapps.microsoft.com/pricing/](https://powerapps.microsoft.com/pricing/) for the USA.

The localized version of the licensing guide shown earlier in this article will be available as links from those pages.

Before moving into detail, it is important to keep in mind that it may be a combination of circumstances from the combination of apps with flow and in context with Office 365 or Dynamics to determine either the price or the choices available. Features such as Connectors, the Common Data Service (CDS), the AI builder and Dynamics entities will be discussed after the platforms.

## Licensing by Platform

### Power Apps

The core attribute of a Power Apps license is the &quot;run&quot; as in the cost to run the Power App.  The pricing comes in two main choices – Run Single Apps and Run Unlimited Apps. This distinction becomes pronounced when we discuss Power Automate.

For Licensing purposes, the pricing is affected by the concept of the &quot;Seeded&quot; app where its run in bundled or part of an activity involving Office 365 or Dynamics 365.

The following set of points discuss the license differences:

- &quot;Run Single Apps&quot; – Per User/Per App/Per Month (e.g.  US$ 10)
  - User with a license runs up to **two** specific apps
  - Sometimes referred to as the &quot;Per App&quot; Plan
  - Standard, Premium and Custom Connectors included
  - Access to 1 custom portal for each user
  - Access to on premises resources via a data gateway
  - Read Access to Dynamics 365 restricted entities
  - 50 MB CDS DB capacity
  - 400 MB CDS File capacity
  - 1000 Daily API Requests

- &quot;Run Unlimited Apps&quot; – Per User/Per Month (e.g. US$ 40)
  - User with a license can run unlimited number of apps
  - Also known simply as the &quot;Per User Plan&quot;
  - Standard, Premium and Custom Connectors included
  - Standard and Premium Connectors included
  - Unlimited Access to the (single) tenant portal
  - Access to on premises resources via a data gateway
  - Read Access to Dynamics 365 restricted entities
  - 250 MB CDS DB capacity shared with the tenant
  - 2 GB CDS File capacity shared with the tenant

- Seeded Power Apps
  - Bundled with Office 365 and Dynamics 365
  - Does not require a Per User/Per App or Unlimited Apps plan but there are limits on the with Office 365 and Power Automate side
    - Office 365 includes Standard connectors but not Premium Connectors
    - Office 365 include access to Office 365 features such as SharePoint directly but not via HTTP which is considered a Premium connector
    - Office 365 does not include CDS capacity
    - Office 365 does not include access to on premises services via the data gateway
    - Office 365 Data API limited to 2000 requests per day
  - Apps typically created to customize or extend Office 365 and Dynamics 365 features
    - e.g. Provisioning SharePoint Online Sites or Lists
  - Standard and Premium Connectors included only when in context of Office 365 or Dynamics
  - No Power Apps portal included
  - Access to on premises resources via a data gateway
  - Create, read, update Delete Access to Dynamics 365 restricted entities limited to 15 in basic Dynamics 365
  - CDS use and capacity included with Dynamics 365

The guide shows in various tables the details of for each of these plans along with footnotes providing specific detail or caveats.  For Power Apps, there is one note referring to &quot;Appendix B&quot; which is about Premium Connectors recently added.  The context for that information is not just to allow comparison against the old plan but to show what may have originally been considered standard as well as new items recently introduced.  A major item that is common to applications build by people familiar and comfortable with T-SQL and SQL Server for data as opposed to SharePoint lists or the CDS, is the SQL Connector which is noted now as Premium.  Appendix B should be consulted if you are seeing whether you need a license for an existing app.

The Power Apps Portal is discussed later in this article.

### Power Automate

Power Automate has two main concepts that determine pricing. The first is the ability to **Create** flows where the first main package allows an individual user to create and run unlimited flows for themselves. The second is the ability to **Implement** flows such as in the second pricing block allow for &quot;implementation&quot; of flows to serve unlimited users with the base bundle starting at 5 flows whether they are implemented or not.

The change from October 2019 insofar as API request limits has extra significance with Power Automate as the new pricing rewards heavy use over casual or limited implementation.  Power Automate also includes a Seeded App option in addition to the two main pricing packages. AI Builder was introduced along with Power Virtual Agents and in April 2020 attended RPA (Remote Processing Automation) was introduced as part of the Power Automate functionality adding an additional per user\per month level. Other plans can also use this functionality but would pay for them separately though all of them would still pay separately for unattended operations.   

An important concept is that of the &quot;child flow&quot; where one flow may call upon another as part of its business process.  Child flows do not count against flow capacity limits.

The following set of points discuss the license differences:

- &quot;Per User Plan&quot; – Per User/Per Month (e.g. US $15)
  - Individual users create and run unlimited flows
  - Considered a &quot;Standalone&quot; license
  - 5000 Daily API Requests for all flows (e.g. if there are 100 flows and assume all were running in a day, they would each be limited to 50 Daily API requests)
  - May execute workflows and business process flows
  - May use Standard, Premium and Connectors
  - Access to on premises data gateway
  - CDS included with Power Apps license
  - 50 MB CDS DB Capacity per user when separate from Power Apps
  - 200 MB CDS File Capacity per user when separate from Power Apps)
  
- &quot;Per User Plan with attended RPA &quot; – Per User/Per Month (e.g. US $40)
  - Individual users create and run unlimited flows
  - Considered a &quot;Standalone&quot; license
  - 5000 Daily API Requests for all flows (e.g. if there are 100 flows and assume all were running in a day, they would each be limited to 50 Daily API requests)
  - May execute workflows and business process flows
  - May use Standard, Premium and Connectors
  - Access to on premises data gateway
  - CDS included with Power Apps license
  - 50 MB CDS DB Capacity per user when separate from Power Apps
  - 200 MB CDS File Capacity per user when separate from Power Apps)
  - 1 attended RPA bot (unattended bot is still a separate cost)
  - 5000 AI Builder Service Credits
  
- &quot;Per Flow Plan&quot; – 5 Flows Per Month (e.g. US $500 and US $100 for each additional Flow.)
  - Implement Flows with reserved capacity
  - Serve unlimited users
  - Also considered a &quot;Standalone&quot; license
  - 5 flows minimum
  - 15000 Daily API requests per flow
  - May execute workflows and business process flows
  - May use Standard, Premium and Custom Connectors
  - Access to on premises data gateway
  - CDS included with Power Apps license
  - 50 MB CDS DB Capacity per flow instance when separate from Power Apps
  - 200 MB CDS File Capacity per flow instance when separate from Power Apps

- Seeded Power Automate
  - Bundled with Office 365 and Dynamics 365
  - Limits for Office 365
    - Office 365 includes Standard connectors but not Premium Connectors
    - Office 365 include access to Office 365 features such as SharePoint directly but not via HTTP which is considered a Premium connector
    - Office 365 does not include CDS capacity
    - Office 365 does not include access to on premises services via the data gateway
    - Office 365 Data API limited to 2000 requests per day
  - Flows typically created to customize or extend Office 365 and Dynamics 365 features
    - e.g. Provisioning SharePoint Online Sites or Lists
    - Unlimited Flows may be created and implemented for these if they do not directly or indirectly affect other systems requiring premium or custom connectors
  - Standard and Premium Connectors included only when in context of Office 365 or Dynamics
  - Access to on premises resources via a data gateway for Dynamics 365 only
  - Access to Dynamics 365 restricted entities related to Power Apps and Dynamics license in play
  - CDS use and capacity included with Dynamics 365
  


### Power Virtual Agents

Power Virtual Agents was just released at the start of the year as the latest Power Platform tool that the citizen developer can use to stand up AI chat bot solutions with no code.  As of this article, there are various solutions to integrate them into the Power Apps Portal, Power Automate flow but as far as licensing is concerned, the interaction does not have the same direct impact as the two previously discussed platforms with each other and the Office or Dynamics platform.  This should not be confused with AI Builder which is a separate add in covered in the next section.

The licensing comes in a single pricing model – 2000 session buckets per month (e.g. US $1000)

The licensing guidance document defines the session:

- A session is an interaction between the customer (essentially the user) and the bot
- A session represents one unit of consumption.
- A session begins when an authored topic is triggered.
- A session meeting the criteria is referred to as a &#39;billed session&#39; in the product.
- Sessions units are deducted for both testing and production usage.
- A session ends in one of the following scenarios:
  - When all the customer&#39;s questions are answered
  - When a customer intentionally ends or closes a chat session
  - When a bot is unable to answer adequately, and the interaction is escalated to a live agent

There are some very important aspects to the pricing that should be considered:

- Cost per month is for the minimum amount whether it is used or not.
- Flows called by PVA&#39;s do not count towards licensing restrictions in the Power Automate platform but integrations from Power Automate to Power Virtual Agents do
- Each license grants 2000 sessions as the way to add capacity
- Other entitlements given to the tenant for each license include:
  - 10 GB CDS DB Capacity
  - 20 GB CDS File Capacity
  - 2 GB CDS Log Capacity

Unlike the ability for a citizen developer to quickly create and deploy Power Apps or Power Automate Flows, the tenant administrator is required to enable the service. Once the service is on, there is no current limit to how many virtual agents can be created and used by how ever many people.  This means that the governance must be communicated broadly as there are yet as of this writing limited sets of reporting and auditing capabilities requiring an explicit effort by administrators and stakeholders.

### Add-ons and Additional Capacity

To complete the picture, it is important to understand that there are several additional features along with ways to increase capacity that will affect the cost.  They are discussed in this section.

#### Power Apps and Add-ons and Capacity

The following items can be added to Power Apps:

- Portal Login
  - The base limit starting at 100 logins per month for each portal site which do not carry over
  - Additional capacity can be purchased at groups of 100 logins (e.g.  US $200 for each additional set over 100)
- Portal Page Views
  - The base limit starts at 100,000 Page views per month for each portal site which also does not carry over
  - Additional capacity can be purchased at groups of 100,000 page views (e.g.   US $100 for each additional set over 100,000)
- AI Builder
  - new helper add-on that falls outside the Connector or App paradigms of the Power Platform systems
  - Not included with any combination and must be licensed separately
  - [https://powerapps.microsoft.com/ai-builder/](https://powerapps.microsoft.com/ai-builder/)
  - Base Unit = 1 million service credits per month (e.g. US $500)

An important note about service credits for the AI builder which applies also to Power Automate is that they are used at different rates depending on the type of activity they are doing such as prediction or forms processing.  Unfortunately, there is not currently a &quot;rate sheet&quot; published.  For now, the guidance is to audit the month&#39;s service credit rate burn down activity and correlate it against the activity types together.  Doing this over several months will at least allow for some capacity requirements prediction.  Potentially, very specific activities can be measured against the same burn down to elicit a rate, but this is not guaranteed to stay consistent from month to month or even with the same activity over time.  Citizen developers should work closely with tenant administrators and other stakeholders when leveraging this very powerful add-on.

#### Common Data Services Capacity Add-ons

Common data services are the backbone of Dynamics 365 and are also a resource for Power Apps and Power Automate as alternatives to SharePoint lists or explicit SQL Server database or other Data repository systems.  A premium connector is required to access CDS unless the connection is related to Dynamics 365 where it is included.  In various cases, the capacity included with the different plans are either tied to a specific entity such as the app or flow user or the Office 365 tenant.

Regardless of what base level is granted for each license, capacity can be added at 1 GB increments for each of three aspects:

- CDS DB e.g. US $40 per month per 1 GB
- CDS File e.g. US $2 per month per 1 GB
- CDS Log e.g. US $10 per month per 1 GB

These can only be added by tenant administrators with the licensing role.

#### RPA and AI Builder
An important distinction of the additional services is the integration with AI services and RPA.  AI Builder was noted as an Add-on for any service but Microsoft has included an opportunity to consolidate costs for this service by creating a license group on Power Automate that includes 5000 AI Builder credits as well as a attended bot.  It is important to understand the distinction between attended and unattended bots to determine the cost implications as well as to potentially drive the architecture choice for its use.  The definition in the license guide is included here for quick reference:

- Attended bot
  - Triggered by an explicit user action on their workstation, i.e. a local or remote desktop 
  - Must operate concurrently with the user on the same workstation
  - Can run more than one discrete process, but each process must be serialized to run sequentially 
- Unattended bot 
  - Runs autonomously without requiring user actuation o Can be deployed on a local or remote desktop, or other virtualized environment
  - Can run more than one discrete process, but each process must be serialized to run sequentially
  - Concurrent instances of a singular process require an additional unattended bot for each instance

In Power Automate, 5,000 personal (as in tied to the flow) service credits are included which is actually a small fraction of the additional capacity bundles which start at 1,000,000 credits for $500 a month at the tenant level (shared with the organization).   

The alternative to the solutions using RPA or AI builder items are programs developed directly in Azure using the underlying systems behind these features.  The cost may need to potentially be weighed against direct development efforts especially if there is already those projects in production.  Because the "rate" the service credits are used is not published or is likely to change, the best way to control or manage costs will involve observations over time leveraging the Power Platform Admin reports and adjusting capacity or license assignments based on that.  The new individual option makes for a cheaper "entry" point to make this determination of whether to go for tenant wide blocks of a million or individual blocks of 5 thousand.  


## Next Steps

### Practical considerations for licensing selections for Power Apps and Power Automate
Taken at face value, there has been a tendency to believe that the changes lead to significantly higher costs or loss of functionality should previously selected connectors fail to operate. Guidance in this area requires that the aspects behind Flows in Power Automate are understood in context of usage especially how a Flow is triggered.

#### Trigger Types
There are two types of triggers that affect usage:

- Automated Flow

A flow that is triggered by some sort of webhook or polling event is called an **Automated Trigger Flow**. This includes SharePoint created/updated, Exchange email received. When a flow is running with an automated trigger it can only access the flow owner's connections, so premium licenses required would be associated with that owner's account. In this mode flows run like Azure LogicApps. The &#39;HTTP Request trigger&#39; also is considered an automated trigger.

- Instant Flow

A flow that's triggered by the end user directly is called an **Instant Trigger Flow**. It runs in the context of the current user. This includes triggers such as "Flow Button", "Power Apps Trigger" and "SharePoint for selected item". When a new user first runs these flows, the dialog appears to ask the user to authenticate connections before running. This auth may be silent if pre-granted by administrator. This flow runs exclusively in that user's context.

With this information in context, the usage type may dictate the license required and/or most cost effective. 

#### Flow Licensing guidance

1. Use Standard connectors in Office 365 licenses when possible in all cases.  

2. For Automated Triggers - buy a full license for the Flow Owner (Flow Bundle or User) and watch number of runs in case additional API run capacity needs to be purchased. A goal here is to potentially limit the requires licenses to one or two at most. 

3. For Instant Triggers - buy a full license for each user that will invoke the specific flow if it requires a connector not included with the seeded applications (Office 365, Dynamics) or is premium. The choice point of per user versus Bundle flow will be the cost per flow. This can be the more complex decision as considerations must be made against the cost per user running up against the cost for Flow Bundles which start at 5 and increment by 1.  

4. In the case of the Power Apps Trigger (a type of Instant Trigger) - the most common Instant Trigger is the **Power Apps trigger**, but any Power App that calls a Power Apps Trigger must have premium license for the premium connector used in the Flow and the Power Apps premium license for the end user includes premium flows used as part of that Power App. In this particular case additional purchases of flow licensing are not necessary, since it must be included in the Power Apps premium license.

#### Nuances affecting the choices

It is important to understand that Flow is based on Azure LogicApps as alluded to earlier in this section.  Flow is &#39;consumption based&#39; but priced in a per-user basis while it also must bridge between the serverless products and other Cognitive based, cost/user systems like CDS.  

As Office 365 is per user based, the license considerations for Flow runs are vastly simplified thanks to the Seeded License described earlier.  Dynamics 365 licenses, for example, includes all premium connectors by virtue of its high per user costs effectively covering any remaining services not covered with Office 365.  

#### Practical application

A simple discussion of flow licensing without practical examples tends to over inflate flow licensing costs. In reality, flow license purchases should be based on specific environment needs as it will typically be a handful of premium accounts required to run the premium automated flows.

Simply put, if 5000 people write to a SharePoint list and there is a SharePoint automated trigger that runs a premium flow license, only 1 premium license is required on that flow.

#### The case for the Full/Premium License in Power Automate versus LogicApps

One premium flow license per month packs a lot more value than running multiple LogicApps that do the same thing. Automated trigger check polling of SharePoint lists is free in Flow but costs a small amount in LogicApps per trigger check.

There are other bigger reasons to get more premium flows. In the case AI Builder, for example, the bundle price may be appealing. When high numbers of flow runs are used API limits may be hit and the purchase of additional API capacity may be required. A best practice in a developer/test/production environment set is to use service accounts with premium licenses used by those flows.

Another important situation is for per-user license pieces such as CDS outside of Dynamics 365.  The Licensing Guide document mentions the concept of &#39;multiplexing&#39; which applies in the same manner as traditional licensing in SQL Server scenarios. So while technically 1 premium license could be used to write to CDS, it would be a multiplexing violation of the CDS license. Other products do not have this requirement.

In one more example, given that a citizen developer creates two Flows (Flow 1 and Flow 2) in an Office 365 E3 environment using a SharePoint form to trigger the first flow (Flow 1) and given that the flow uses the HTTP connector to trigger the second flow (Flow 2 e.g. Graph API REST call) where there are 10 users with permissions to run the form, **only the author** of the flow needs to have the premium\full license rather than a license for each of the 10 SharePoint form users.  If this was an approval workflow where a step included approvals, the people approving would also not need licenses as the flow is considered a single instance through its completion and is, in effect, already paid for.  


### Additional considerations

For the citizen developer, awareness of all aspects can make a big difference when creating and even justifying a solution in the same manner as for a regular developer or solutions architect.  As the saying goes, &quot;Nothing is for free&quot; but deep understanding in this case can at least mitigate much of those costs or at least help put a definitive price tag on those benefits derived from the effort.  It follows from this point and based on recent experience that one must keep up with changes in this area on the same level as changes in capability and functionality within the Power Platform suite.  Tenant administrators get the benefit of notification through the message system in their administration application while others would benefit from setting up alerts or reminders to the Power Platform docs and blogs here and in the community.

As a final note, recall early when it was noted that prices may vary from region to region as well as agreement to agreement.  Variations notwithstanding, the final arbiter of the price will be Microsoft and with that comes the opportunity to confirm arrangements with them directly or through your IT&#39;s Microsoft contact or representative. When dealing with Microsoft do consider that the major change between the older licensing scheme and the current one is that the customer is rewarded for using the system more that those who create the odd Power App or flow very infrequently.  It is the case of buying a car to only use it to bring the beloved pet to the Pet hospital once a quarter for their checkup or to go to work every day – on the latter, there may be wear and tear on the vehicle but there is also very measurable and significant return on investment for the benefit it brings to the household salary.

## Credits
Much of the information is based on various Ignite sessions as well as the key licensing document noted earlier.  Additional contributions include John Liu for putting into context they key guidance details that should always accompany any formal discussion of this topic as well as Charles Lamanna (@clamanna) Microsoft CVP for his confirmation response to @singhgurd used in the second example. 

This is living documentation with all updates, confirmations, clarifications, objections and sample scenario contributions welcome! 
 
---

**Principal author**: [Ralph Rivas](https://www.linkedin.com/in/ralphrivas/)
**Principal contributor**: [John Liu](https://www.linkedin.com/in/johnnliu/)


