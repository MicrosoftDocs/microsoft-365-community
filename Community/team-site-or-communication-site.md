---
title: Team Site vs. Communication Site -  Which one should I choose?
ms.date: 5/1/2020
author: SusanHanley
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: sharepoint-online
localization_priority: 
description: "Team Site vs. Communication Site: Which one should I choose?"
ms.collection: M365Community
---
# Team Site vs. Communication Site: Which one should I choose?

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

Choosing between a [team site](https://support.microsoft.com/office/what-is-a-sharepoint-team-site-75545757-36c3-46a7-beed-0aaa74f0401e) and a [communication site](https://support.microsoft.com/article/what-is-a-sharepoint-communication-site-94a33429-e580-45c3-a090-5512a8070732) should start with your intent and desired business outcomes. Though there are nuances to explore, at the most basic, think about these two use cases:

- **Connect, Collaborate, Create:** When you want to create a place where the members of a work group or project team can collaborate on project deliverables, plan an event, track status, or exchange ideas, you want a **Team Site**. In a Team Site, **all members are content authors** where we jointly create and edit content. Think of team sites as a place where work gets done. My project team needs a place to collaboratively work on deliverables. Even though we have individual assignments, we are collectively collaborating to create one or more assets. Our project team needs a Team Site.
- **Showcase, Share, Story:** When you want to &quot;broadcast&quot; a message, tell a story, share content for viewing (but not editing) to a large audience or the entire organization, or showcase services or people, you want a **Communication Site**. In a Communication Site, there will most often be a small number of content authors and a much larger number of content readers or consumers. Think about your corporate intranet. Even if you have collaborative _parts_ of the intranet, the primary purpose of your intranet is to communicate a story such as corporate news or showcase services and information such as your benefits and policies. Your intranet sites are examples of Communication Sites.

## When should I create a team site?

**Create a team site for each discrete group of people or unit of work**.

If you are a long-time user of SharePoint, you might be thinking that &quot;team site equals sub-site.&quot; Resist the temptation to create team sites as sub-sites! Many governance decisions (for example, the ability to share content outside the organization and who has permission to invite new members to the team) are **scoped to the site collection**. For the most flexibility both today and in the future, each team should get their own site collection – which is exactly what happens when you create an [Microsoft 365 Group](https://support.microsoft.com/office/learn-about-microsoft-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2) or a team site from the SharePoint start page, assuming that your organization has enabled &quot;self-service&quot; site creation. When you provision a new [Microsoft Teams](https://support.microsoft.com/article/video-what-is-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d) or [team site](https://support.microsoft.com/article/what-is-a-sharepoint-team-site-75545757-36c3-46a7-beed-0aaa74f0401e) in Microsoft 365, you will get a new _site collection_ in your tenant.

If you are doing this right, you will have **a lot of team sites**. Why? Because you have a lot of projects and work teams – and each one of your projects or work teams will likely have different access and information management requirements. Even if the same work team works on lots of projects, you should still provision a unique team site for each unique project.

**Collaborating with people outside the organization? Create a team site for each customer or partner.**

Keeping in mind that many governance and security boundaries are scoped to the _site collection_, **create a new team site for each of your different customers or partners** if you have an extranet environment. This will ensure that Customer or Partner A doesn&#39;t accidentally &quot;see&quot; any content or information from Customer or Partner B. By default, team sites are enabled with **external sharing turned on**. This can be changed by the SharePoint administrator in the Admin Center.

**Each member has the same permissions.**

While your team site will have one or more Owners, typically every Member of the team has the same privileges in the site.

**The SharePoint start page brings your team sites together**

Don&#39;t panic about how your users will possibly keep track of all of these team sites – because the SharePoint start page has got your back!

The [SharePoint start page](https://support.microsoft.com/office/discover-content-with-the-sharepoint-start-page-6b85097a-87e0-4611-a29a-dfd49b1a1220) in Microsoft 365 brings together, for each individual person, news from all of the team sites in which they are a member (and sites they are following), sites they visit frequently, and other news suggested by the Microsoft Graph. It also shows the most recent activity in the sites each person visits frequently.

**Examples of team site scenarios.**

- Project team working together to complete deliverables and manage tasks.
- Holiday party planning committee planning the annual get-together. If you have work locations in multiple geographies, you may have many holiday party committees and each party committee team site might be in a different language.
- Human Resources team members – everyone who works in HR.
- Executive Committee – different leadership groups within the organization.
- Extranet site to work with Partner A.
- A different extranet site to work with Partner B.

## When should I create a communication site?

**Create a communication site to showcase, share, or tell a story.**

Here&#39;s a way to think about the difference between a team site and a communication site. A team site is where the sausage is made – it&#39;s behind the counter and typically private. A communication site is where the sausage is sold – where it&#39;s visible to all our &quot;customers&quot; and where they come to buy our sausage. Typically, our customers don&#39;t want to know how we make the sausage (or how many times we had to edit that document to get it &quot;ready to share&quot;). They just want to get the finished product.

**Communication sites have two distinct user personas.**

Most often, a communication site has a small number of people with permission to author content and many people who only have permission to read content. Team sites use Microsoft 365 Groups for permissions. Communication sites use SharePoint groups.

**Think about your team sites as where you**  **collaborate**  **and your communication sites as where you**  **communicate****.**

As an example, consider your Human Resources (HR) department. Typically, HR will have at least one team site where the members of the HR team can work on defining a new benefits program or crafting the announcement about an organizational restructuring. During the process of creation, the HR team works _privately_ on a team site open just to the members of HR (or individual &quot;friends of HR&quot; who contribute to one or more specific documents). Once all the back and forth about the message or document or program is complete, the HR team is ready to _share_ the information with the rest of the company.

When they are ready to _share_, the HR team moves the document to or writes the story in a **communication site** that is open to the entire organization. They use a communication site to share &quot;team to organization&quot; or &quot;organization to employees&quot; information. While in some cases they may solicit feedback on the information shared in their communication site (for example, with comments on the page), the content itself is typically editable only by a small number of authorized users.

**Examples of communication site scenarios.**

- &quot;Official&quot; corporate news.
- HR team communicating benefits and compensation information.
- Travel team publishing guidelines about corporate travel.
- Policies and procedures.

## Feature Comparison

| **Feature**  | **Team Site** | **Communication Site** |
| --- | --- | --- |
| Who creates the site? | Site Owner (or Admins) | Site Owner (or Admins) |
| Who creates content? | **All members are content authors** who jointly create and edit content. | **Small number of content authors** and a much larger number of content readers or consumers. |
| Security | Microsoft 365 Groups | SharePoint Groups |
| Default Setting for External Sharing | External Sharing Enabled (but can be disabled by the SharePoint Admin) | External Sharing Disabled (but can be enabled by the SharePoint Admin) |
| Navigation | Left | Top |
|Multilingual features? | Yes | Yes |
| When you create, you ALSO get … | Planner board, OneNote notebook, Email address for the group, Shared Calendar, shared mailbox, opportunity to connect with a Microsoft Team  (if the site wasn&#39;t created as part of provisioning a Microsoft Teams) | NOTHING but a SharePoint communication site! |

---

**Principal author**: [Susan Hanley, MVP](https://www.linkedin.com/in/susanhanley)

