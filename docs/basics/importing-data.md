# Importing data into SharePoint

This guide will help users understand the various options available to import files and data into SharePoint. We cover several different approaches:

| Method | Type of User |
| ------ | ------------ |
| [Document Libraries – Drag and drop files and folders](#document-libraries--drag-and-drop-files-and-folders-user)| End user|
| [Document Libraries – SharePoint Migration Tool](#document-libraries--upload-files-and-folders-user) | Power user |
| [Lists – Export Spreadsheet to SharePoint](#lists--export-spreadsheet-to-sharepointpower-user) | Power user |
| [Document Libraries – SharePoint Migration Tool](#document-libraries--sharepoint-migration-tool-power-user) | Power user |

## Document Libraries – Drag and drop files and folders (User)

SharePoint document libraries support the *drag and drop* of files and folders from computer to site. With the target site and document library open:

- Select the source files / folders.

- Drag to the site and release.

![Drag and drop](../../images/importing-data/drag-drop-files-folders.png)

- The upload status can be monitored using the “Show progress” button on the document library menu.

![“Show progress” button](../../images/importing-data/drag-drop-show-progress.png)

- The “Show progress” button will notify you of any errors and when possible provide an intervention.

![“Show progress” button with intervention](../../images/importing-data/drag-drop-show-intervention.png)

- Example error image shown below:

![“Show progress” button with error](../../images/importing-data/drag-drop-show-error.png)

## Document Libraries – Upload files and folders (User)

Like the *drag and drop* of files and folders, SharePoint document libraries also support the direct uploading files and folders. With the target site and document library open:

- Click “Upload” and select “Files” or “Folder”.

![Upload of files and folders from computer to site](../../images/importing-data/upload-files-folders.png)
The **“Files”** option does not allow the uploading of folders. Similarly, the **“Folder”** option does not allow files.

- Select the source files / folders and click “Open”.

![Upload files](../../images/importing-data/upload-files.png)

- The “Show progress” button will notify you of any errors and when possible provide an intervention.

![“Show progress” button](../../images/importing-data/upload-files-folders-show-progress.png)

## Document Libraries – Copy to and Move to (Power user)

SharePoint document libraries support the copying and moving of files / folders to new locations. New locations can include a different folder, document library or site, including OneDrive for Business.

The **“Copy to”** feature will copy the files / folders to the new location while leaving the source files / folders unchanged. With the target site and document library open:

- Select the source files / folders and click “Copy to”.

![Source files](../../images/importing-data/copy-to-files.png)

- Select the target location (i.e. “Your OneDrive”).

![Target location](../../images/importing-data/copy-to-files-target-location.png)

- Click “Copy here” to complete the file / folder copy.

![“Copy here” button](../../images/importing-data/copy-to-files-target-copy-here.png)

- The “Show progress” button will notify you of any errors and when possible provide an intervention.

![“Show progress” button](../../images/importing-data/copy-to-files-show-progress.png)

The **“Move to”** feature will copy the files / folders to the new location and will move the source files / folders to the site “Recycle bin”. With the target site and document library open:

- Select the source files / folders and click “Move to”.

![Source folder](../../images/importing-data/move-to-folder.png)

- Select the target location (i.e. “Planning” document library).

![Target location](../../images/importing-data/move-to-folder-target-location.png)

- Click the target site (i.e. “Human Resources” site) and then click the target document library (i.e. “Planning”).

![Target site and document library](../../images/importing-data/move-to-folder-target-site-library.png)

- Click “Move here” to complete the file / folder move.

!["Move here" button](../../images/importing-data/move-to-move-here.png)

- The “Show progress” button can also be used to view the progress of a copy or upload operation.

![“Show progress” button](../../images/importing-data/move-to-show-progress.png)

## Lists – Export Spreadsheet to SharePoint(Power user)

*Microsoft Excel* supports the exporting of “Tables” from spreadsheets to new SharePoint lists. With the source spreadsheet open:

- Click “Table Design”.

- Click “Export” and select “Export Table to SharePoint List…”.

![Export Table to SharePoint list...](../../images/importing-data/excel-export-toolbar.png)

- Enter the target “Address”; provide a list name and click “Next”.

![Step 1 of 2](../../images/importing-data/excel-export-step1.png)

- Review the list design and click “Finish”.

![Step 2 of 2](../../images/importing-data/excel-export-step2.png)

- Click the URL to view the new SharePoint list. Click “OK” to exit the export wizard.

![Successful Excel export](../../images/importing-data/excel-export-ok.png)

- Example exported list shown below:

![Successful Excel export](../../images/importing-data/excel-export-list.png)

## Document Libraries – SharePoint Migration Tool (Power user)

The *SharePoint Migration Tool (SPMT)* can be used to import files into SharePoint. *SPMT* is especially useful when migrating a large volume of documents from a file share.
Detailed information about *SPMT* can be found on the [Download and install the SharePoint Migration Tool](https://docs.microsoft.com/en-us/sharepointmigration/introducing-the-sharepoint-migration-tool) page.

From your *SPMT* computer:
- Open the “SharePoint Migration Tool”.<br>
![Open the SharePoint Migration Tool](../../images/importing-data/spmt-windows-search.png)

- Click “Start your first migration”.
![Welcome screen](../../images/importing-data/spmt-welcome-screen.png)

- Click "File Share".
![Where's your content screen](../../images/importing-data/spmt-file-share.png)

- Click “Choose folder”.
![Select a source screen](../../images/importing-data/spmt-select-source.png)

- Select the source file share and click “OK”.
![Browse for folder screen](../../images/importing-data/spmt-browse-folder.png)

- Click “Choose folder” to select a specific sub-folder or click “Next” to continue.
![Choose folder or click next screen](../../images/importing-data/spmt-windows-choose-folder.png)

- Enter the destination site URL and document library. Click “Next”.
![Select a destination screen](../../images/importing-data/spmt-windows-select-destination.png)

- Name your migration if desired or click “Next” to continue.
![Review migration screen](../../images/importing-data/spmt-windows-review-migration.png)

- Update *SPMT* settings if required or click “Migrate” to continue. Detailed information on *SPMT* settings can be on the [SharePoint Migration Tool Settings](https://docs.microsoft.com/en-us/sharepointmigration/spmt-settings) page.
![Choose your settings screen](../../images/importing-data/spmt-settings.png)

- Click “Save” to store the migration or click “No thanks” to continue.
![Choose your settings screen](../../images/importing-data/spmt-save-migration.png)

- The summary screen will provide migration details and reports.
![Choose your settings screen](../../images/importing-data/spmt-summary.png)

---

Principal author: Norm Young

LinkedIn: https://www.linkedin.com/in/norm-young/

Blog: [normyoung.ca](https://normyoung.ca)
