---
title: Power Automate - Send SharePoint files as attachments
ms.date: 03/04/2020
author: JimmyHang
ms.reviewer: jhendr
ms.author: jhendr
ms.service: sharepoint-online
localization_priority: 
description: "Power Automate - Send SharePoint files as attachments"
ms.collection: M365Community
---
# Power Automate - Send SharePoint files as attachments

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

Recently I've been working on a project where we need a bunch files in a SharePoint library need to be sent as attachments.
The solution to this is of course Power Automate and Flows.

## Scenario:
We have a library with a bunch of folders, and each of the folders have multiple files. These files needs to be sendt out as Attachment when needed. There is many usage cases for this function, the example in this article is related to contract management, and as you might have guessed these documents need to be sendt as attachments outside of the company. 

## What do you need:
* Power Automate, standard M365 licence
* SharePoint library, this could of course be a Teams connected library
* Mailbox in Exchange Online

> [!NOTE] 
> If you are new to Power Automate head over offical documentation to learn more: 
https://docs.microsoft.com/en-us/power-automate/


## The Steps:

	1. The flow is started by User
	2. User input recipient details
	3. Flow will locate the correct folder
	4. Flow will grab all the files
	5. Flow will attach all files as, and add these to an attachment array
	6. Flow will send the email with the attachments

In our SharePoint team site we have a Contracts folder, inside this folder we have our partners and customers as subfolders. 

![Contract folder in Library](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment01.png)

The contract files are located inside the customer/partner folder as below

![Files inside a contract](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment02.png)

Using the library menu | click Automate | Power Automate | Create a flow

![Creating a new Flow](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment03.png)

The flow we are building is an Instant Flow, in the dialog click "See your flows" to navigate to the Flow editor page

![Flow templates](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment04.png)

Choose to create a new flow | Instant - from blank

![Create a new Instant flow from blank](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment05.png)

Name your flow and choose to "For a selected file" as trigger then click Create

![Trigger action 'For a selected file'](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment06.png)


Whenever the flows runs we need some data from the end users, in this case "Recipient Name" and "Recipient Email" then we will create two variables:

    - Recipient Name
    - Recipient Email
	- FolderName | this is the folder we will grab the files from
	- AttachmentsArray | this is the array where we will put all files to be sent


![Trigger inputs](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment07.png)

The next step is to grab the data of the item that started the flow, that way we can verify if the "item" that started the workflow is either a file or a folder.

![Condition step to verify if item is folder](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment08.png)


If folder is "true", we will then append the folder name to our variable "FolderName", and use this in the next action to grab all the files properties in the current folder

![Append data to Folder Name variable, get all files in current folder](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment09.png)


We will then use "Apply to each" to append the files content to our Attachment array variable, the trick her is to append the right content, thanks to this guide at the Flow forums by Sunay Vaishnav, I finally managed to get this working. 
https://flow.microsoft.com/en-us/blog/multiple-attachments-single-email/

As pr. this writing, the working way to append SharePoint files to attachment array is:

```
{
  "Name": @{items('Apply_to_each')?['{FilenameWithExtension}']},
  "ContentBytes": @{body('Get_file_content')?['body']}
}
```
![Get each file content, and append to Attachments array variable](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment10.png)

The final action is the "Send email (V2)" action, you will need to populate the actions with the following input:

	- Recipient email | user input
	- Reipient name | user input
	- AttachmentArray | attchments form previous step
	- From (send as) | user who started the flow


![Send email action](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment11.png)


The whole Flow should look something like this:

![Final Flow with all steps](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment12.png)


All done Save, Test and Share with your users

The recipient should receive an email with the files attached

![The email sent to recipient](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment13.png)


---
**Principal author**: [Jimmy Hang, MCT, MCSE: Productivity](https://www.linkedin.com/in/jimmyhang/)
---
