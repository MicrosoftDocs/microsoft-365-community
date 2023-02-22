---
title: Versioning in SharePoint
ms.date: 7/01/2020
author: PatD
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: sharepoint-online
localization_priority: 
description: "Versioning in SharePoint"
ms.collection: M365Community
---

# Versioning in SharePoint

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## Basic Idea

Document collaboration, co-authoring, and List updates with human beings is much better with Versioning enabled. People make mistakes, and Versioning provides the safety net.

Emotionally, it reinforces the idea that SharePoint is a good place to store your work product.

SharePoint Lists items (data) and Library documents (files) have the ability to store, track, and *restore* the previous state of the item or document to how it was before a user changed it.

Versioning creates a historical record of all changes, with the date/time and indication of the user who made the change, on a per-file/list item basis. The end user can view, delete, and restore a version if they have the correct permissions in the library or list.

| To do this… | I need this permission… |
|:-----|:-----|
| View version history | Full Control, Contribute, Read |
| Restore a previous version | Full Control, Contribute |
| Delete a version | Full Control, Contribute |
| Un-publish a version | Full Control, Contribute |
| Recover deleted a deleted version | Full control and/or Contribute |

## Enabling Versioning

In SharePoint Online or On-Premises, versioning is enabled in the List Settings or Library Settings screens by clicking on the 'Versioning settings' link.  An interface is provided to let you control how many versions you'd like to retain. The user must have the Manage Lists permission capability to enable versioning.

## Disabling Versioning

If you can Enable versioning, you can Disable versioning. Disabling versioning doesn't delete the old versions. End users receive no notification of this change.

> [!Note]
> **A Cautionary Tale:**  As site owner, if you disable Versioning and *don't* tell your end users, they'll notify you. In person.

Note: Since No Versioning is removed from SharePoint Online，it can be enabled or disabled through PowerShell, SharePoint Designer, or by a developer using CSOM.

## Accessing Previous Versions

In SharePoint Online, select the list item or document, and in the Actions menu, select Version History.  You can also see a link to the version history in the details pane.

In SharePoint on-premises (2010, 2013, 2016, 2019) you can view version history by clicking on the link in the ribbon menu.

In both products, Version History opens in a modal dialog box, with options to View, Restore, or Delete the entry. If any SharePoint Metadata columns were changed, that column and its new value will be displayed.

## SharePoint Online vs SharePoint On-Premises

Historically, versioning is not enabled by default at the creation of a list or library.  Recently, SharePoint Online has started enabling it by default in libraries when they're created.

|What| Online| On-Premises|
|:------| :-----| :-----|
|Lists| Enabled at creation (and set to 50 versions)| Not enabled at creation |
|Libraries|Enabled at creation (and set to 500 versions)|Not enabled at creation|

> [!Note]
> **A Cautionary Tale:**
> As Site Owner, you're responsible for not exceeding your allotted space limit. 500 versions of an Excel file won't cause any trouble.  A 500-version library with hundreds of  300MB PDF documents might push the site over the limit and prevent users from working in the site.  Watch your Storage Metrics on storage libraries.

## Major Versus Minor Versions

Libraries can have both Major versions, which are represented with whole numbers (12.0), and Minor versions, which are represented with decimal numbers (12.3). If your library is configured to use Check In/Check Out, each change performed by a user with a checked-out document will create a minor version.

Lists usually only have Major versions.

> [!NOTE]
> All versions count against your SharePoint storage usage, as do files in the recycle bins and files preserved due to retention policies. In calculating the SharePoint storage usage, the full file size of each version counts towards the total usage. For example, if only metadata changes were made to a 10 MB file with no change to its file size, the total storage usage will be 10 MB (original version) + 10 MB (updated version) = 20 MB.

## Best Practices and Versioning Trivia

* The Version column in SharePoint Views is sometimes not a number column. If you sort it, version 12 shows up in between version 1 and 2.
* It is a best practice to enable Versioning in a *list* at creation and not set a limit of major versions. It takes up very little space, and your end users will thank you for it.
* In an average SharePoint On-Premises farm, setting document library versions up to 10 major and 10 minor has, in practice, been enough for any group that can't define how many versions they need.
* A deleted and then restored file/list item maintains its old versions.
* In a list with versioning enabled, attachment changes are not versioned.
* Limiting the number of versions is generally a good practice. It means you can conserve space on the server and reduce clutter for users. But, if your organization is required to save all versions for legal or other reasons, don’t apply any limits.
* As best practice PST files should not be uploaded on OneDrive for Business and SharePoint Online team site document libraries due to the impact on storage. If PST files are uploaded the service will retain versions for 30 days.

## Versioning with autosave and co-authoring

By default, SharePoint saves a version of a document every time a user clicks the "Save" button. However, if autosave is turned on, SharePoint will automatically save a version of the document every few minutes.

When co-authoring is enabled in SharePoint, multiple users can work on the same document simultaneously. Each user's changes are tracked and saved as a new version. When a user saves changes to a document that is being co-authored, SharePoint will save a new version of the document that includes all of the changes made by all co-authors.

It's important to note that co-authoring can have an impact on versioning in SharePoint. If multiple users are working on the same document at the same time, it can be difficult to keep track of who made which changes and when. SharePoint does its best to track changes and create new versions as needed, but it's still important for users to communicate and coordinate when co-authoring to ensure that changes are properly tracked and versioned.

### Further Reading

* Microsoft: [Planning Versioning, Content Approval](/sharepoint/governance/versioning-content-approval-and-check-out-planning) & [How does versioning work in a SharePoint list or library](https://support.office.com/article/how-does-versioning-work-in-a-sharepoint-list-or-library-0f6cd105-974f-44a4-aadb-43ac5bdfd247)
* Blog: [SharePoint Maven on Versioning](https://sharepointmaven.com/5-ways-users-can-benefit-versioning-sharepoint/)
* Blog: [ShareGate: SharePoint Version Control to the Rescue](https://sharegate.com/blog/sharepoint-version-control)

---

Principal author: [Patrick M Doran](https://www.linkedin.com/in/patrickdoran/)
