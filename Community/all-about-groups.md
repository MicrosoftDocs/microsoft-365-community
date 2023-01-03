---
title: Groups in Microsoft 365 and Azure, and Which is Right for You
ms.date: 8/31/2020
author: ToddKlindt
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: microsoft-365
localization_priority: 
description: "There are a lot of groups in Azure and Microsoft 365. They can be confusing. This article explains them so you can figure out which one is best for you."
ms.collection: M365Community
---

# Groups in Microsoft 365 and Azure, and Which is Right for You

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## What's With All These Groups?

Azure and Microsoft 365 are the culmination of decades of technical evolution and the desire to be as backwards compatible as possible. While those are noble and righteous goals, they do come with some baggage. In this case that baggage is many object types in Azure Active Directory and Microsoft 365 that are "groups" and it's not entirely obvious what each group is or isn't, and which group you should use for any given scenario. In this article we hope to unravel that mystery some and provide you with the tools you need to make the right choice. We will cover [Azure AD Security Groups](#azure-ad-security-groups), [Microsoft 365 Groups](#microsoft-365-groups), and [SharePoint Groups](#sharepoint-groups).

## Azure AD Security Groups

### What are Azure AD Security Groups?

Azure AD Security Groups are analogous to Security Groups in on-prem Windows Active Directory. They are Security Principals, which means they can be used to secure objects in Azure AD. They can be created natively in Azure AD, or synced from Windows AD with [Azure AD Connect](/azure/active-directory/cloud-sync/what-is-cloud-sync). Their membership can be static, or it can be [generated dynamically](/azure/active-directory/users-groups-roles/groups-create-rule) with rules.

### Who can manage Azure AD Security Groups?

There are several groups of people that can manage Azure AD Security Groups. If the group is synced from on premises Windows AD they cannot be managed in Azure AD. They must be managed on-prem with tools like the Active Directory Users and Computers. Changes made there will sync up to Azure AD with Azure AD Connect. In the Azure AD Portal synced Security Groups will have a Source of "Windows server AD."

Azure AD Security Groups that are cloud-only can be managed by users in the tenant that have the appropriate [admin roles](/azure/active-directory/users-groups-roles/directory-assign-admin-roles). This includes, but is not limited to, Global Administrator, Directory Writers, Groups Administrator, Privileged Role Administrator, SharePoint Administrator, and User Administrator.

### How do they manage Azure AD Security Groups?

Because Azure has good, well documented APIs, there are a variety of ways to manage them. The most common way to manage them with a UI is the [Azure Portal](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal). The Azure Portal is fully featured, so users with the appropriate roles can create, edit, view, and delete Azure AD Security Groups from there.

PowerShell can also be used to manage Azure AD Security Groups with the [Azure AD Module](/azure/active-directory/users-groups-roles/groups-settings-v2-cmdlets). This module does not work with .Net Core, so it requires a Windows PowerShell 5.x host.

### How are Azure AD Security Groups used?

Azure AD Security Groups aren't used much in Microsoft 365. They can be used to [apply licenses to users](/azure/active-directory/users-groups-roles/licensing-groups-assign) based on their group membership. This can be part of an onboarding process to automate licensing a user to Microsoft 365. Azure AD Security Groups can also be added to SharePoint Groups to grant access to SharePoint resources. The risk with that approach is that the SharePoint Site Owners and Administrators don't necessarily have exposure to who is a member of that Azure AD Security Group, so they don't know who can access their SharePoint Site.

## Microsoft 365 Groups

### What are Microsoft 365 Groups?

[Microsoft 365 Groups](/microsoft-365/admin/create-groups/office-365-groups) are a membership object in Microsoft 365 that eases the task of ensuring a group of people have consistent permissions to a group of related resources. You may see them referred to as Microsoft 365 Groups or Unified Groups. The group of related resources varies slightly depending on where the Microsoft 365 Group is created. For example, if a user creates a Groups connected Team site in SharePoint, a Microsoft 365 Group will be created in the background. Along with the SharePoint site, Microsoft 365 will also create a shared mailbox and calendar in Outlook, a Planner Plan, and a Power BI Workspace. Any user given access to any of those resources will be granted the same permission to the rest of the resources in the Microsoft 365 Group. If a team is created in Teams, that team is part of a newly created Microsoft 365 Group, and all of the other resources are created for that Group.

Microsoft 365 Groups have two roles, Owner and Member. Owners can change the settings and the membership of the Group. Members can remove themselves, add members to a Public Group, and recommend Guest users be invited. Notably, Microsoft 365 Groups do not have a way to grant a user read only access to resources.

### Who can manage Microsoft 365 Groups?

By default, any user in a tenant can create a Microsoft 365 Group by creating a new resource in a Group supported app. Tenant Administrators do have the option of [restricting who can create Microsoft 365 Groups](/microsoft-365/solutions/manage-creation-of-groups). Group Owners can manage Group membership and settings. Users that have the appropriate administrative roles at the tenant level can also create and manage Groups, including ones they are not members of. If a Group's [Privacy level](https://support.microsoft.com/office/make-microsoft-365-groups-public-or-private-c0a991b3-9c56-48b8-bf0f-05530f836b1b) is set to Public then any user in the tenant can add themselves to it.

### How do they manage Microsoft 365 Groups?

Group Owners can manage Group membership in any of the Group supported applications. For instance, they can add a member to a Group from the SharePoint site, Outlook, Outlook Online, the Teams app, and so on. Changes to the Group made in any app are reflected in all of the apps that Group supports. The management experience is not the same between apps, so an Owner may have to go to a specific app for a specific task. For instance, to change a Group's Privacy policy you have to use Outlook or Outlook online. That setting can't be changed in SharePoint. Users that have the appropriate administrative roles can also create Microsoft 365 Groups from the Azure Portal or PowerShell. They can also manage Group membership and settings from those same interfaces.

### How are Microsoft 365 Groups used?

Microsoft has made it clear that Microsoft 365 Groups are the future of resource permissioning in Microsoft 365. They allow Microsoft 365 users to take advantage of the entire suite of Microsoft 365 applications with minimal administrative overhead. This gives Group owners one pane of glass to look through when seeing what their group is doing. The group's files are in SharePoint, the real time collaboration is in Teams, the email discussions are in Exchange, but they're all secured and managed as a Microsoft 365 Group.

## SharePoint Groups

### What are SharePoint Groups?

These are the same SharePoint Groups we know and love from on premises SharePoint server. They are a collection of SharePoint users that are given the same permissions. They are scoped at the SharePoint site collection level, so a SharePoint Group created in one site collection doesn't exist in any other site collections. Note that modern SharePoint sites are actually site collections under the covers.

### Who can manage SharePoint Groups?

Anyone with the "Create Groups" and "Manage Permissions" permissions in the SharePoint site can manage SharePoint Groups. Since this not an Azure AD object, having elevated roles in Azure AD does not allow someone to manage SharePoint Groups. A user with the SharePoint admin Role could grant themselves Administrator permissions to a SharePoint site, then they could manage that site's SharePoint Groups.

### How do they manage SharePoint Groups?

SharePoint groups are primarily managed in the SharePoint interface by navigating to the "Site Permissions" and "Advanced Site Permissions" application page (/_layouts/15/user.aspx). They can also be managed in PowerShell with either the [Microsoft SharePoint Online](https://www.powershellgallery.com/packages/Microsoft.Online.SharePoint.PowerShell) or the [PnP PowerShell modules](https://www.powershellgallery.com/packages/SharePointPnPPowerShellOnline/).

### How are SharePoint Groups used?

SharePoint Groups are how permissions were applied to groups of users, both in on-prem SharePoint Server, and earlier in SharePoint Online. SharePoint has individual Permissions like, "Create Groups" and "Add items" that are included in Permission Levels such as "Full Control" and "Read." When a SharePoint Group is created it is assigned one or more Permission Level. Users that are place placed in that SharePoint Group have the permissions that are selected in the Permission Levels the SharePoint Group has. SharePoint has three Groups by default; Members, Owners, and Visitors. Site Owners can use those SharePoint Groups, or they can create their own.

SharePoint Permissions should be handled with Microsoft 365 Groups. Native SharePoint permissions should be avoided when possible. SharePoint sites can be [Groupified](/sharepoint/dev/features/groupify/groupify-overview) later if the site isn't part of a group, but that should be done sparingly. Communications sites are mostly read only by nature, and they do not support Microsoft 365 Groups.

---

**Principal author**: [Todd Klindt, MVP](https://www.linkedin.com/in/toddklindt/)

---
