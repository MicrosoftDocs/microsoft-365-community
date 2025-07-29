---
title: "Understanding tenant display name usage"
description: "Understand where the tenant display name is used throughout M365"
ms.date: 01/01/2025
author: michaelblumenthal
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: concept-article
ms.author: pamgreen
ms.service: microsoft-365
ms.localizationpriority: Low
ms.collection: M365Community
---

# Understanding where your tenant's display name is used

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]
  
You can make changes to your organization profile, such as your organization name, but this change has far reaching implications as explained below. **You must be a global admin to update this information.**
For instructions on changing your organizational profile, see [this article](/microsoft-365/admin/manage/change-address-contact-and-more?view=o365-worldwide&preserve-view=true).
  
## Edit organization information

To change your company's display name:
  
1. In the admin center, go to the **Settings** / **[Org settings](https://go.microsoft.com/fwlink/p/?linkid=2053743)** page.
2. On the **Organization profile** tab, select **Organization information**.
3. Think long and hard about if you really want to change the display name.  The display name is used widely but consuming services often don't pick up this change.
4. Update your organization's information, then select **Save changes**. Be sure to fill in all required fields marked with an * to enable saving your changes.

## What does the name field mean?

| Field | Description |
|---------|---------|
|Name | The name entered here is the organization's name, also known as the tenant display name. |

## Impact of changing the organization's display name

The organization's name is used throughout Microsoft 365, including but not limited to:  

* Entra ID (formerly Azure Active Directory) Sign-in dialogs and multifactor authentication prompts. This includes multifactor authentication prompts provided by the Microsoft Authenticator app on iOS and Android devices.
* If your users have set up other Microsoft accounts with their business or school email address, they may see the organization name on the sign-in page. This helps them distinguish between their work or school account and their other accounts, so they can identify which one to use when they sign in.
* Viva Engage navigation
  * In Viva Engage, the organization name is used as the name of the home Engage network, and this shows up in the left navigation.  
* OneDrive Sync
  * The organization name is shown in File Explorer on Windows and Finder on Mac.
    * On Windows, in File Explorer, in the navigation pane, the blue cloud icon for OneDrive for your Microsoft 365 tenant is labeled:
    * On Windows 10: "OneDrive - \<organization name\>" (for example, "OneDrive - Contoso").
    * On Windows 11: "\< User first name \> - \<organization name\>" (for example, "Michael - Contoso").
    * When a user syncs a SharePoint library, it shows up in File Explorer under a node in the left navigation that bears a blue office building icon and the organization name.
  * The organization name is used in file paths:
    * The file path for the root of the OneDrive for that user defaults to C:\users\\<username\>\OneDrive - \<organization name\>\
    * The file path for SharePoint libraries that get synced is C:\users\\<username\>\\<organization name\>\
    * The file path for the Documents Known Folder is C:\users\\<username\>\OneDrive - \<organization name\>\Documents\
    * The file path for the Pictures Known Folder is C:\users\\<username\>\OneDrive - \<organization name\>\Pictures\
    * The file path for the Desktop Known Folder is C:\users\\<username\>\OneDrive - \<organization name\>\Desktop\
  * The organization name is shown in:
    * The OneDrive activity center
    * The tooltip of the OneDrive cloud icon
    * The OneDrive settings window, on the Accounts tab
  * Currently, updating the organization name does not update it for configured clients.
* Microsoft Teams
  * Tenant Switcher in Teams displays the organization name when a user participates in Teams in more than one tenant.
  * Organizations that are under a certain size [get an organization-wide team created automatically](/microsoftteams/create-an-org-wide-team). That team gets its name from the organization's name, but the team name does not change if the organization's Name field value changes.
* OneNote: End users may have a notebook named in this pattern: \<first name>@\<organization name>.
* Windows desktop applications for Word, Excel, and PowerPoint: The File Save and File Open screens display the organization name.  
* Mobile apps such as Word, Excel, PowerPoint, OneNote, Outlook, and the Microsoft 365 App may display the organization name on various screens, especially ones that let you pick files from Microsoft 365 services such as SharePoint and OneDrive.
* Power Platform: The default environment takes its name from the organization name. The organization name (referred to as the TenantName in [this article](/power-platform/guidance/adoption/secure-default-environment#rename-the-default-environment)) is the default environment name, but can be changed, though that is a manual step after a tenant rename.

Note that only Microsoft Teams will automatically detect the change to the organization name and reflect the change in the tenant switcher. Any teams, such as an organization-wide team named with the company name, will not update.

None of the other applications pick up the name change automatically. Mobile apps may require you to sign out and sign back in or reinstall them before they will display the new name.

[This script](/office/troubleshoot/activation/reset-office-365-proplus-activation-state) can help you force Office desktop applications to pick up the new name, but it forces the user to sign back into the Office desktop apps again.

If you change the organization name, OneDrive Sync will not automatically update the organization name it uses. The OneDrive Sync client will not notice the new name unless you [unlink OneDrive Sync client and re-link it](https://support.microsoft.com/office/unlink-and-re-link-onedrive-3c4680bf-cc36-4204-9ca5-e7b24cdd23ea) by signing in again. Note that you may need to do some file system cleanup after that. Also, you don't want to unlink your OneDrive Sync client if you have unsynced files. Make sure syncing has been completed before unlinking. Relinking will resync your OneDrive, but if you had previously synced SharePoint libraries that are listed under the blue office building in File Explorer, you would need to re-sync those libraries individually. A better alternative is to use the Add to OneDrive feature to add a shortcut in your OneDrive to a SharePoint library. With an Add to OneDrive shortcut, the folder contents syncs within your OneDrive blue cloud instead of your OneDrive blue office building and would automatically be included in syncing when relinking.

---

**Principal author**: [Michael Blumenthal](https://www.linkedin.com/in/michaelbblumenthal/)

---
