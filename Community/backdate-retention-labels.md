---
title: Backdate Retention Labels
ms.date: 7/29/2025
author: stevegoodyear
ms.reviewer: stevegoodyear
manager: stevegoodyear
ms.author: stevegoodyear
ms.topic: article
ms.service: sharepoint-online
ms.localizationpriority: Low
description: Backdating Retention Labels by setting the retention label applied date property to a previous date to maintain the retention schedule for migrated files.
ms.collection: M365Community
---

# Backdate Retention Labels

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

With migrated documents, the document’s retention schedule may have begun in its old repository prior to the migration, but applying a retention label in its new SharePoint Online repository could essentially restart the retention schedule and retain the document for too long.

As part of migrating documents from an old system, it is crucial to ensure that they comply with organizational policies and regulatory requirements. One important aspect of this process is setting a records classification and retention schedule for each migrated document, which enforces compliance with records management and any regulatory requirements. This can involve including the existing records classification and retention schedule as part of the migration if it is already specified or identifying it if records management will be implemented as part of the migration.

In SharePoint Online, records management is implemented through retention labels in Microsoft Purview. However, when basing retention on a date, retention labels base the retention schedule on one of three dates you can configure as part of the retention label: the document created date, the last modified date, or the date the label was applied.

Sometimes the created or last modified date works well, in which cases maintaining metadata when migrating will maintain the retention schedule. However, often a records management solution will depend on the label applied date to start the retention schedule based on applying the retention label to change the document’s state as part of its records life cycle. The label applied date is often preferred because a document can become a record and initiate the retention schedule sometime after it was created or last modified, such as when a proposed document is approved and becomes official. Yet as mentioned, applying the retention label after the migration will essentially restart the retention schedule clock.

## How to Backdate Retention Labels

To backdate a retention label, apply the retention label using the setComplianceTagWithMetaInfo method on the List Item. This method is available in the CSOM API and available in PowerShell.

>To learn more about the ListItem.SetComplianceTagWithMetaInfo method, please see the documentation.
><https://learn.microsoft.com/dotnet/api/microsoft.sharepoint.client.listitem.setcompliancetagwithmetainfo>

The following PowerShell script provides an example using PnP PowerShell to backdate the retention label applied date for a document in the default Documents library. The document has the list item ID of 1 and will have a retention label called Technical Specification applied with the label applied date set to December 25, 2023. Note that method also accepts an email address that specifies the user for the Label Applied By property value.

```powershell
Connect-PnPOnline https://<TENANT>.sharepoint.com/sites/<SITE> -ClientId <GUID> -Interactive
$list = Get-PnPList "Documents"
$item = Get-PnPListItem -List $list -Id 1
$date = Get-Date -Year 2023 -Month 12 -Day 25 -Hour 13 -Minute 30 -Second 00

# Apply the retention label to the list item and backdate the label applied date
$item.setComplianceTagWithMetaInfo("Technical Specification", $false, $false, $date, "steve@contoso.com", $false, $false)
```

By backdating and setting the proper retention date, organizations can manage their documents more effectively, ensuring that they are retained for the appropriate duration and disposed of properly when no longer needed. This practice not only helps in maintaining an organized document repository but also ensures adherence to legal and regulatory standards.

---

**Principal author**: [Steve Goodyear](https://www.linkedin.com/in/SteveGoodyear)

---
