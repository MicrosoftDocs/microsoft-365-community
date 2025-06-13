---
title:  Importing data into SharePoint
ms.date: 4/30/2020
author: nyoung30
ms.reviewer: pamgreen
ms.author: pamgreen
manager: pamgreen
ms.topic: how-to
ms.service: sharepoint-online
ms.localizationpriority: Low
description: Importing data into SharePoint
ms.collection: M365Community
---

# Importing data into SharePoint

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

This guide will help users understand the various options available to import files and data into SharePoint. We cover several different approaches:

| Method | Type of User |
| ------ | ------------ |
| [Document Libraries – Drag and drop files and folders](#document-libraries--drag-and-drop-files-and-folders-user)| End user|
| [Document Libraries – Upload files and folders](#document-libraries--upload-files-and-folders-user) | Power user |
| [Document Libraries – Copy to and Move to](#document-libraries--copy-to-and-move-to-power-user) | Power user |
| [Lists – Export Spreadsheet to SharePoint](#lists--export-spreadsheet-to-sharepoint-power-user) | Power user |
| [Lists – Import Spreadsheet to SharePoint](#lists--import-spreadsheet-to-sharepoint-power-user) | Power user |
| [Document Libraries – SharePoint Migration Tool](#document-libraries--sharepoint-migration-tool-power-user) | Power user |
| [Document Libraries – Sync](#document-libraries--sync-power-user) | Power user |

## Document Libraries – Drag and drop files and folders (User)

SharePoint document libraries support the *drag and drop* of files and folders from computer to site. With the target site and document library open:

- Select the source files / folders.

- Drag to the site and release.

![Drag and drop](media/importing-data/drag-drop-files-folders.png)

- The upload status can be monitored using the “Show progress” button on the document library menu.

![“Show progress” button while uploading](media/importing-data/drag-drop-show-progress.png)

- The “Show progress” button will notify you of any errors and when possible provide an intervention.

![“Show progress” button with intervention](media/importing-data/drag-drop-show-intervention.png)

- Example error image shown below:

![“Show progress” button with error](media/importing-data/drag-drop-show-error.png)

## Document Libraries – Upload files and folders (User)

Like the *drag and drop* of files and folders, SharePoint document libraries also support the direct uploading files and folders. With the target site and document library open:

- Click “Upload” and select “Files” or “Folder”.

![Upload of files and folders from computer to site](media/importing-data/upload-files-folders.png)

The **“Files”** option does not allow the uploading of folders. Similarly, the **“Folder”** option does not allow files.

- Select the source files / folders and click “Open”.

![Upload files](media/importing-data/upload-files.png)

- The “Show progress” button will notify you of any errors and when possible provide an intervention.

![“Show progress” button while copying](media/importing-data/upload-files-folders-show-progress.png)

## Document Libraries – Copy to and Move to (Power user)

SharePoint document libraries support the copying and moving of files / folders to new locations. New locations can include a different folder, document library or site, including OneDrive for Business.

The **“Copy to”** feature will copy the files / folders to the new location while leaving the source files / folders unchanged. With the target site and document library open:

- Select the source files / folders and click “Copy to”.

![Select the source files](media/importing-data/copy-to-files.png)

- Select the target location (i.e. “Your OneDrive”).

![Select the target location](media/importing-data/copy-to-files-target-location.png)

- Click “Copy here” to complete the file / folder copy.

![“Copy here” button](media/importing-data/copy-to-files-target-copy-here.png)

- The “Show progress” button will notify you of any errors and when possible provide an intervention.

![“Show progress” button copying files](media/importing-data/copy-to-files-show-progress.png)

The **“Move to”** feature will copy the files / folders to the new location and will move the source files / folders to the site “Recycle bin”. With the target site and document library open:

- Select the source files / folders and click “Move to”.

![Source folder](media/importing-data/move-to-folder.png)

- Select the target location (i.e. “Planning” document library).

![Target location moving files](media/importing-data/move-to-folder-target-location.png)

- Click the target site (i.e. “Human Resources” site) and then click the target document library (i.e. “Planning”).

![Target site and document library](media/importing-data/move-to-folder-target-site-library.png)

- Click “Move here” to complete the file / folder move.

!["Move here" button](media/importing-data/move-to-move-here.png)

- The “Show progress” button can also be used to view the progress of a copy or upload operation.

![“Show progress” progress bar](media/importing-data/move-to-show-progress.png)

## Lists – Export Spreadsheet to SharePoint (Power user)

*Microsoft Excel* supports the exporting of “Tables” from spreadsheets to new SharePoint lists. With the source spreadsheet open:

- Click “Table Design”.

- Click “Export” and select “Export Table to SharePoint List…”.

![Export Table to SharePoint list...](media/importing-data/excel-export-toolbar.png)

- Enter the target “Address”; provide a list name and click “Next”.

![Step 1 of 2 - Excel export](media/importing-data/excel-export-step1.png)

- Review the list design and click “Finish”.

![Step 2 of 2 - Excel export](media/importing-data/excel-export-step2.png)

- Click the URL to view the new SharePoint list. Click “OK” to exit the export wizard.

![Successful Excel export ok screen](media/importing-data/excel-export-ok.png)

- Example exported list shown below:

![Successful Excel export list view](media/importing-data/excel-export-list.png)

## Lists – Import Spreadsheet to SharePoint (Power user)

*SharePoint* supports the importing of “Tables” from spreadsheets to new SharePoint lists. From "Site contents":

- Click “New” and click "List".

- Click “From Excel”; provide a list name; upload a new spreadsheet or select an existing one and click "Next"

![Step 1 of 2 - Excel import](media/importing-data/excel-import-wizard-step1.png)

- Select the target "Table" from the spreadsheet; set the column types ("Single line of text", "Multiple lines of text", "Choice", "Title" or "Do not import") and click "Create"

![Step 2 of 2 - Excel import](media/importing-data/excel-import-wizard-step2.png)

- Example imported list shown below:

![Successful Excel import](media/importing-data/excel-import-list.png)

## Document Libraries – SharePoint Migration Tool (Power user)

The *SharePoint Migration Tool (SPMT)* can be used to import files into SharePoint. *SPMT* is especially useful when migrating a large volume of documents from a file share.
Detailed information about *SPMT* can be found on the [Download and install the SharePoint Migration Tool](/sharepointmigration/introducing-the-sharepoint-migration-tool) page.

From your *SPMT* computer:

- Open the “SharePoint Migration Tool”.
![Open the SharePoint Migration Tool](media/importing-data/spmt-windows-search.png)

- Click “Start your first migration”.
![Welcome screen](media/importing-data/spmt-welcome-screen.png)

- Click "File Share".
![Where's your content screen](media/importing-data/spmt-file-share.png)

- Click “Choose folder”.
![Select a source screen](media/importing-data/spmt-select-source.png)

- Select the source file share and click “OK”.
![Browse for folder screen](media/importing-data/spmt-browse-folder.png)

- Click “Choose folder” to select a specific sub-folder or click “Next” to continue.
![Choose folder or click next screen](media/importing-data/spmt-windows-choose-folder.png)

- Enter the destination site URL and document library. Click “Next”.
![Select a destination screen](media/importing-data/spmt-windows-select-destination.png)

- Name your migration if desired or click “Next” to continue.
![Review migration screen](media/importing-data/spmt-windows-review-migration.png)

- Update *SPMT* settings if required or click “Migrate” to continue. Detailed information on *SPMT* settings can be on the [SharePoint Migration Tool Settings](/sharepointmigration/spmt-settings) page.
![Choose your settings screen](media/importing-data/spmt-settings.png)

- Click “Save” to store the migration or click “No thanks” to continue.
![Save or no thanks](media/importing-data/spmt-save-migration.png)

- The summary screen will provide migration details and reports.
![Migration details](media/importing-data/spmt-summary.png)

## Document Libraries – Sync (Power user)

SharePoint document libraries support the syncing of files between computer and site using *Microsoft OneDrive*. The *OneDrive sync app* is especially useful when migrating a large volume of documents from computer to SharePoint document library.
Detailed information about OneDrive can be found on the [Sync SharePoint files with the new OneDrive sync app](https://support.office.com/article/sync-sharepoint-files-with-the-new-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88) page.

With the target site and document library open:

- Click “Sync”.

![Document library sync](media/importing-data/onedrive-sync.png)

- Click “Open” to the “Getting ready to sync...” prompt.

![Getting ready to sync...](media/importing-data/onedrive-getting-ready.png)

- Confirm you login account name and click “Sign in”.

![Sign in](media/importing-data/onedrive-signin.png)

- Click “Next”.

![Your folder](media/importing-data/onedrive-your-folder.png)

- Click through the “Welcome to OneDrive” screen and then click “Open my OneDrive folder”.

![Welcome to OneDrive](media/importing-data/onedrive-welcome.png)

Using Windows Explorer, open the source documents folder:

- Select the source files / folders.

- Drag to the destination sync document library and release.

![Drag and drop files and folders](media/importing-data/onedrive-drag-file-folders.png)

- Source folder and target document library will become synchronized.

![Source and target synchronized](media/importing-data/onedrive-synchronized-files-folders.png)

- See the OneDrive sync app in the system tray to view progress and any sync messages.
![OneDrive systray](media/importing-data/onedrive-systray.png)

---

Principal author: [Norm Young](https://www.linkedin.com/in/norm-young/)
