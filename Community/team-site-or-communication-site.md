---
title: Team Site vs. Communication Site -  Which one should I choose?
ms.date: 2/4/2025
author: SusanHanley
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: concept-article
ms.author: pamgreen
ms.service: microsoft-365
ms.custom: sharepoint-online
ms.localizationpriority: Low
description: "Team Site vs. Communication Site: Which one should I choose?"
ms.collection: M365Community
---
# Team Site vs. Communication Site: Which one should I choose?

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

Choosing between a [team site](https://support.microsoft.com/office/what-is-a-sharepoint-team-site-75545757-36c3-46a7-beed-0aaa74f0401e) and a [communication site](https://support.microsoft.com/article/what-is-a-sharepoint-communication-site-94a33429-e580-45c3-a090-5512a8070732) should start with your intent and desired business outcomes. Though there are nuances to explore, at the most basic, think about these two use cases:

- **Connect, Collaborate, Create:** When you want to create a place where the members of a work group or project team can collaborate on project deliverables, plan an event, track status, or exchange ideas, you want a **Team Site**. In a Team Site, **all members are content authors** where we jointly create and edit content. Think of team sites as a place where work gets done. My project team needs a place to collaboratively work on deliverables. Even though we have individual assignments, we're collectively collaborating to create one or more assets. Our project team needs a Team Site.

- **Showcase, Share, Story:** When you want to &quot;broadcast&quot; a message, tell a story, share content for viewing (but not editing) to a large audience or the entire organization, or showcase services or people, you want a **Communication Site**. In a Communication Site, there will most often be a small number of content authors and a much larger number of content readers or consumers. Think about your corporate intranet. Even if you have collaborative _parts_ of the intranet, the primary purpose of your intranet is to communicate a story such as corporate news or showcase services and information such as your benefits and policies. Your intranet sites are examples of Communication Sites.

- **Create, Store, Use, Permissions, Apps:** When you use a store for SharePoint libraries and lists, without M365 groups services, you want a Team Site (not groups connected). With Teams Sites (not groups connected) you can use a store for all SharePoint based elements like documents, list items, news, docsets, and many more. You will not compete with the concepts of groups and SharePoint permissions. Any you can choose, where you want to see the SharePoint site navigation, on top or on left side. Use this kind of Team Site, when you create SharePoint based Apps with libraries, lists and other SharePoint topics or for a SharePoint list based Microsoft Power Apps.

## When should I create a team site?

**Create a team site for each discrete group of people or unit of work**.

If you're a long-time user of SharePoint, you might be thinking that &quot;team site equals sub-site.&quot; Resist the temptation to create team sites as sub-sites! Many governance decisions (for example, the ability to share content outside the organization and who has permission to invite new members to the team) are **scoped to the site collection**. For the most flexibility both today and in the future, each team should get their own site collection—which is exactly what happens when you create an [Microsoft 365 Group](https://support.microsoft.com/office/learn-about-microsoft-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2) or a team site from the SharePoint start page, assuming that your organization has enabled &quot;self-service&quot; site creation. When you provision a new [Microsoft Teams](https://support.microsoft.com/article/video-what-is-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d) or [team site](https://support.microsoft.com/article/what-is-a-sharepoint-team-site-75545757-36c3-46a7-beed-0aaa74f0401e) in Microsoft 365, you get a new _site collection_ in your tenant.

If you do this right, you'll have **many team sites**. Why? Because you have a lot of projects and work teams—and each one of your projects or work teams will likely have different access and information management requirements. Even if the same work team works on lots of projects, you should still provision a unique team site for each unique project.

**Collaborating with people outside the organization? Create a team site for each customer or partner.**

Keeping in mind that many governance and security boundaries are scoped to the _site collection_, **create a new team site for each of your different customers or partners** if you have an extranet environment. This ensures that Customer or Partner A doesn't accidentally &quot;see&quot; any content or information from Customer or Partner B. By default, team sites are enabled with **external sharing turned on**. This can be changed by the SharePoint administrator in the Admin Center.

**Each member has the same permissions.**

While your team site has one or more Owners, typically every Member of the team has the same privileges in the site.

**The SharePoint start page and the app bar bring your team sites together**

Don't panic about how your users will possibly keep track of all of these team sites, because the [SharePoint start page](https://support.microsoft.com/office/6b85097a-87e0-4611-a29a-dfd49b1a1220) and the [app bar](https://support.microsoft.com/office/b2ab82d5-9af7-445e-ad24-236c5a86b5f8) have got your back!

The SharePoint start page in Microsoft 365 brings together, for each individual person, news from all of the team sites in which they're a member (and sites they're following), sites they visit frequently, and other news suggested by the Microsoft Graph. It also shows the most recent activity in the sites each person visits frequently.

The app bar's **My sites** shows each user's frequent and followed sites.

Together, these two navigation options provide personalized navigation for each user based on their own interests and activity - including all their team sites.

**Examples of team site scenarios.**

- Project team working together to complete deliverables and manage tasks.
- Holiday party planning committee planning the annual get-together. If you have work locations in multiple geographies, you may have many holiday party committees and each party committee team site might be in a different language.
- Human Resources team members—everyone who works in HR.
- Executive Committee—different leadership groups within the organization.
- Extranet site to work with Partner A.
- A different extranet site to work with Partner B.

## When should I create a communication site?

**Create a communication site to showcase, share, or tell a story.**

Here's a way to think about the difference between a team site and a communication site. A team site is where the sausage is made—it's behind the counter and typically private. A communication site is where the sausage is sold—where it's visible to all our &quot;customers&quot; and where they come to buy our sausage. Typically, our customers don't want to know how we make the sausage (or how many times we had to edit that document to get it &quot;ready to share&quot;). They just want to get the finished product.

**Communication sites have two distinct user personas.**

Most often, a communication site has a small number of people with permission to author content and many people who only have permission to read content. While team sites usually use Microsoft 365 Groups for permissions, communication sites use SharePoint groups.

**Think about your team sites as where you**  **collaborate**  **and your communication sites as where you _communicate_.**

As an example, consider your Human Resources (HR) department. Typically, HR has at least one team site where the members of the HR team can work on defining a new benefits program or crafting the announcement about an organizational restructuring. During the process of creation, the HR team works _privately_ on a team site open just to the members of HR (or individual &quot;friends of HR&quot; who contribute to one or more specific documents). Once all the back and forth about the message or document or program is complete, the HR team is ready to _share_ the information with the rest of the company.

When they're ready to _share_, the HR team moves the document to or writes the story in a **communication site** that is open to the entire organization. They use a communication site to share &quot;team to organization&quot; or &quot;organization to employees&quot; information. While in some cases they may solicit feedback on the information shared in their communication site (for example, with comments on the page), the content itself is typically editable only by a small number of authorized users.

**Examples of communication site scenarios.**

- "Official" corporate news.
- HR team communicating benefits and compensation information.
- Travel team publishing guidelines about corporate travel.
- Policies and procedures.

## When should I create a team site which is not group connected?

When an administrator creates a new team site, they can choose not to connect it to a Microsoft 365 Group. While the general advice is to use Microsoft 365 Groups for team site membership management, there are some useful exceptions.

**Create a team site which is not group connected to create, store, and use SharePoint elements and items**

A team site (not group connected) is in a way a legacy SharePoint site type - one which you may be familiar with from working with SharePoint on-prem. It's more similar to a communication site, as it's not a Team Site connected with with Microsoft 365 services: it's a SharePoint site only.

**Differences from communication sites**

- We can choose the location for the site navigation on the top or the left
- There is a default OneNote files stored in the site and available initially through the site navigation as Notebook
- A team site - especially one without a Microsoft 365 Group - should not a SharePoint landing page. For that, use a Communication Site.
- You can "groupify" or "teamify" a team site. Groupify a team site (not group connected) to a groups connected team site and teamify to a Microsoft Teams. These actions do not change the underlying site template, however, so these site will always be "a little bit different".

**Differences from team sites which are group connected**

- The site is not connected with other Microsoft 365 services like Exchange or Planner, nor does it have an Entra ID object for a Microsoft 365 Group
- Team site permissions based on Microsoft 365 Groups, with Members and Owners
- Use SharePoint groups for permissions, not M365 groups with members and owners. You can use Entra ID groups in SharePoint groups.

**Work with SharePoint elements and items**

Your SharePoint site can have all of the different SharePoint elements and items, granular permissions, news, themes, and the site navigation on top or on left side and many more, all are based on native SharePoint, without Exchange or other Microsoft 365 services.

**Different SharePoint lists and libraries can have different permissions**

A Team site (not group connected) is the perfect store to use SharePoint lists and libraries with different permissions. You can use different permission levels on different elements and also use approvals or other Microsoft Power Automate Flows in your SharePoint site. You can use SharePoint groups or security groups for permissions on sites or other SharePoint elements and set permissions on different levels like sites, lists/libraries, folders, or items. When you use Power Apps based on data in a SharePoint site, a non-group connected site may be a good alternative.

**So when should I create a team site (not group connected)?**

Use it when you need a SharePoint site but you don't need Microsoft 365 Groups or other services. It's the place to create, work, and use SharePoint elements and items, native, without Microsoft 365 Groups. You can define your own permissions and you do not come into conflict with Microsoft 365 group permissions.

**Examples of team sites (not group connected) scenarios**

- I need "only" a SharePoint site, without groups services
- Sites to contain data for SharePoint based apps, also for Power Apps
- A site with lists and libraries with a lot of different permissions

## Feature Comparison

| Feature | Team Site | Communication Site | Team Site (not groups connected)
| --- | --- | --- | ---
| Who creates the site? | Site Owner (or Admins) | Site Owner (or Admins) | Site Owner (or Admins)
| Who creates content? | **All members are content authors** who jointly create and edit content. | **Small number of content authors** and a much larger number of content readers or consumers. | **A defined group of members are content authors** also different SharePoint lists and libraries can have different permissions
| Security | Microsoft 365 Groups | SharePoint Groups | SharePoint Groups
| Default Setting for External Sharing | External Sharing Enabled (but can be disabled by the SharePoint Admin) | External Sharing Disabled (but can be enabled by the SharePoint Admin) | External Sharing Disabled (but can be enabled by the SharePoint Admin)
| Default Navigation | Left | Top | Left (but can be changed to Top)
|Multilingual features? | Yes | Yes | Yes
| When you create, you ALSO get … | Planner board, OneNote notebook, Email address for the group, Shared Calendar, shared mailbox, opportunity to connect with a Microsoft Team  (if the site wasn't created as part of provisioning a Microsoft Team) | NOTHING but a SharePoint communication site! | OneNote notebook

---

**Principal author**: [Susan Hanley, MVP](https://www.linkedin.com/in/susanhanley)
