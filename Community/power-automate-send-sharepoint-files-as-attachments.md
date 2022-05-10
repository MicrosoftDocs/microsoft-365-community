---
title: Power Automate - Send SharePoint files as attachments
ms.date: 03/04/2020
author: JimmyHang
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: power-platform
localization_priority: 
description: "Power Automate - Send SharePoint files as attachments"
ms.collection: M365Community
---

# Power Automate - Send SharePoint files as attachments

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## Scenario

We have a library with a number of folders, and each of the folders contains multiple files. These files need to be sent out as attachments, when needed. There are many use cases for this capability, but the example in this article is related to contract management. As you might have guessed, these documents need to be sent as attachments outside of the company.

## What do you need

* Power Automate, standard M365 license
* SharePoint library - this could of course be a Teams connected library
* Mailbox in Exchange Online

> [!NOTE]
> If you are new to Power Automate head over to the [official documentation](/power-automate/) to learn more.

## The Steps

1. The flow is started by the user
2. The user inputs the recipient's details
3. Flow will locate the correct folder
4. Flow will collect all the files
5. Flow will add the files to an attachment array
6. Flow will send the email with the attachments

In our SharePoint team site we have a Contracts folder and inside this folder we have our partners and customers as sub-folders.

![Contract folder in Library](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment01.png)

The contract files are located inside the customer/partner folder as below

![Files inside a contract](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment02.png)

Using the library menu | click Automate | Power Automate | Create a flow

![Creating a new Flow](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment03.png)

The flow we are building is an Instant Flow, so in the dialog click "See your flows" to navigate to the Flow editor page.

![Flow templates](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment04.png)

Choose to create a new flow | Instant-from blank.

![Create a new Instant flow from blank](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment05.png)

Name your flow, choose to "For a selected file" as trigger, and then click Create.

![Trigger action 'For a selected file'](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment06.png)

Whenever the flow runs we need some data from the end user. In this case "Recipient Name" and "Recipient Email". We will create two variables:

* Recipient Name
* Recipient Email
* FolderName | this is the folder we will grab the files from
* AttachmentsArray | this is the array where we will put all files to be sent

![Trigger inputs](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment07.png)

The next step is to grab the data for the item that started the flow. That way we can verify if the "item" that started the workflow is a file or a folder.

![Condition step to verify if item is folder](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment08.png)

If folder is "true", we will then append the folder name to our variable "FolderName", and use this in the next action to grab all the files properties in the current folder.

![Append data to Folder Name variable, get all files in current folder](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment09.png)

We will then use "Apply to each" to append the files' content to our Attachment array variable. The trick here is to append the right content. Thanks to [this guide](https://flow.microsoft.com/blog/multiple-attachments-single-email/) at the Flow forums by Sunay Vaishnav, I finally managed to get this working.

As of this writing, the best way to append SharePoint files to an attachment array is:

``` javascript
{
  "Name": @{items('Apply_to_each')?['{FilenameWithExtension}']},
  "ContentBytes": @{body('Get_file_content')?['body']}
}
```

![Get each file content, and append to Attachments array variable](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment10.png)

The final action is the "Send email (V2)" action. You will need to populate the action with the following inputs:

* Recipient email | user input
* Recipient name | user input
* AttachmentArray | attachments form previous step
* From (send as) | user who started the flow

![Send email action](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment11.png)

The whole Flow should look something like this:

![Final Flow with all steps](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment12.png)

When you are all done, click Save, Test, and Share with your users

The recipient should receive an email with the files attached.

![The email sent to recipient](media/power-automate-send-sharepoint-files-as-attachments/powerautomate-sendasattachment13.png)

---

**Principal author**: [Jimmy Hang, MCT, MCSE: Productivity](https://www.linkedin.com/in/jimmyhang/)

---
