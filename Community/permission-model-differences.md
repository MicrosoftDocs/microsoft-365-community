---
title: Planning Permissions with Group-based SharePoint Sites... when you're used to Regular SharePoint Permissions.
ms.date: 07/01/2020
author: PatD
ms.reviewer:  Joanne Hendrickson
localization_priority: 
description: "Planning Permissions with Group-based SharePoint Sites... when you're used to Regular SharePoint Permissions."
ms.collection:  SPCommunity
---

# Planning Permissions with Group-based SharePoint Sites... when you're used to Regular SharePoint Permissions

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## Basic Idea

When you're a Site Owner of a SharePoint Site Collection, you should ask yourself - *Is this SharePoint site collection associated with a modern Office 365 Group*?

If it is associated with a Group, the permission model you're used to is going to be different. You can easily confuse users and expose content in a way they don't want to if you try and apply and manipulate traditional SharePoint permissions in a Group site.

> **A Cautionary Tale:**
> As Site Owner, you may want to discourage other Owners of the Group Site *not* to use the traditional Designer/Contributor/Reader SharePoint Levels. This can lead to a support nightmare.

## The Story So Far

As a SharePoint Site Owner, you should already be familiar with these permissions concepts:

* [SharePoint Permission Levels](https://docs.microsoft.com/sharepoint/understanding-permission-levels)
* [Creating and Editing Levels](https://docs.microsoft.com/sharepoint/how-to-create-and-edit-permission-levels)
* [Customizing SharePoint Permissions](https://docs.microsoft.com/sharepoint/customize-sharepoint-site-permissions)

This has been the model for On-Premises SharePoint Site Collections for some time.

## Where things are different with Office 365 Group-generated SharePoint Sites

It's hard *not* to spawn a SharePoint Site Collection when using the new Modern Office 365 tools like Teams, Planner, and Outlook. Make a new Team, and you get a Site Collection.  Membership, by default, is synced across these tools.

### Here's the breakdown

|Traditional SharePoint Site| Site Spawned from O365 Group  | Shared with Teams, Planner, Outlook, etc|
|--|--|--|
| Owners | Owners   | No
| Members | Members | Yes
| Designers| n/a | No
| Contributors | n/a | No
| Visitors | n/a| No
| Custom level | n/a | No

It is still possible to create a Modern SharePoint Site that *isn't* part of a group, and in that case you get the usual permission levels.

### Best Practices

* If you're adding users to a traditional SharePoint site, add them using the Gear Icon and *Site Permissions* link.
* If you're adding users to a Group-spawned SharePoint Site Collection - who need to participate in Teams, Planner, Outlook - add them with the *Members* link in the SharePoint Group Site, or add them in Teams, Planner, or Outlook.
* Don't add them in both places.
* Remember: In an Office 365 Group, a Member added to the associated Team, Planner, or Outlook instance is a Member in the SharePoint site.  The benefits of tool integration only works if your access is the same across the suite
* A **Visitor** really isn't a thing with a Group-spawned SharePoint Site - unless you add them into the SharePoint-generated 'Visitor' group via the Site Permissions link.
* A **Member** in a  Group-spawned Site SharePoint has considerable power.  That mission critical document library with beautifully crafted Views and Workflow?  Someone adding Planner Tasks can easily delete this library.

## Terminology

Product names overlap a little, so here are some stories describing common scenarios:

*My team needed to collaborate, so I signed into Teams and made a Team.  That also generated a Group SharePoint site, and a Planner Board!  When I add a user to the Team, they have access all over.*

*I had to add some read-only users to my legacy SharePoint Online Site. I went to Site Permissions and added them to the existing Azure Active Directory Visitors Group.  I didn't see a link that said 'Members' on the screen.*

*My boss told me to own our group's Planner board, so my IT department made me an Owner of this Office 365 Group! I can now add users to a SharePoint Group Site! And delete Planner Boards.*

### Further Reading

* [Groups in Microsoft 365 and Azure, and Which is Right for You](all-about-groups.md)
* [SharePoint Maven on O365 Groups vs SP Site 'Groups'](https://sharepointmaven.com/office-365-groups-or-sharepoint-team-sites/)
* [SharePoint Maven on Connecting a SP Site to an O365 Group](https://sharepointmaven.com/how-to-connect-a-sharepoint-site-to-an-office-365-group/)


---

Principal author: [Patrick M Doran](https://www.linkedin.com/in/patrickdoran/)
