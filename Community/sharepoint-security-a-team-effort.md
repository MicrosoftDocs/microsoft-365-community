---
title:  "Managing SharePoint Online Security: A Team Effort"
ms.date: 6/27/2020
author: veronicageek
ms.reviewer: efrene
manager: pamgreen-msft
ms.topic: article
ms.author: efrene
ms.service: sharepoint-online
localization_priority: 
description: "Managing SharePoint Online Security: A Team Effort"
ms.collection: M365Community
---

# Managing SharePoint Online Security: A Team Effort

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

Security has always been an important topic, and even more nowadays.
We want our users to securely access the environment, share files, and our IT team to sleep at night don't we?

In this article, we'll look at the _most important settings_ in Microsoft 365 to help you secure your SharePoint Online environment, and see how it involves more than SharePoint administrators!

>_Note: Details on how to configure each settings is out of scope of this article, but links to the official Microsoft documentation will be provided whenever possible._

## Tenant settings

This should be the **first** place to go before even getting the users into SharePoint. But unfortunately, most of the time the default settings remain untouched, and users start using the platform.

There are a few tenant settings to pay attention to however. **Sharing** settings are _extremely_ important. If left to default, they can have dramatic consequences and lead to data breaches. So let's start with this setting.

### Sharing settings

To access the Sharing settings (_tenant level_), navigate to the SharePoint Admin Center, under _Policies_, select _Sharing_.

The first thing that should make your heart beat faster at this stage is the slider for SharePoint and OneDrive being at the same level as the word "Anyone". Isn't it a scary thing to read that _**users can share files and folders using links that don't require sign-in**_ from the recipient? ANY recipient for that matter.

So unless you're absolutely sure that you want to keep it that way, slide down one level immediately!

![mmd](media\managing-sharepoint-online-security-a-team-effort\external-sharing-settings-default.png)

>_Note: You don't even need to know the exact company policy for OneDrive for Business at this point. The slider will also follow the SharePoint setting down one level. That's because you can't have a more permissive sharing policy for OneDrive for Business than you have for SharePoint._

When you know what the company policy is, you can choose the appropriate sharing settings between the following:

- New and existing guests
- Existing guests
- Only people in your organisation

### More external sharing settings

Again, we have a few options available to help securing a bit more if necessary. You can select them all or not. But it's not because you can that you should!

**Limit external sharing by domain**: If selected, you can _Allow_ or _Block_ specific domains. A common scenario would be collaborating with specific customers or partners. This setting is available at the _tenant_ level, as well as at the _site_ level.

>_Note: From the moment you choose to "Allow" one or more domains, the other ones will be blocked. If you decide to "Block" one or more domains, the other ones will be allowed._

**Allow only users in specific Security Groups to share externally**: If selected, members of the security group(s) will be the only ones capable of sharing externally.

>_Note: This option is only available if your sharing settings (tenant) are set to "New and Existing Guests" or "Anyone". For more information, please refer to the official Microsoft documentation: [Manage Security Groups](https://docs.microsoft.com/sharepoint/manage-security-groups)._

**Guests must sign in using the same account to which sharing invitations are sent**: This adds an extra layer of security to make sure that the user accessing the file(s) is the one you expect to. Selecting this option is highly recommended when possible.

**People who use a verification code must reauthenticate after this many days [number of days]**: New method where guests will authenticate using a one-time passcode for the number of days you configured.

For more information about this feature, please refer to the official Microsoft documentation: [Secure external sharing recipient experience](https://docs.microsoft.com/sharepoint/what-s-new-in-sharing-in-targeted-release).

## Site settings

SharePoint permissions... A vast topic, which most of the time, ends up in hair pulling and sleepless nights. And things are not getting better when sites are group-connected!

See the permissions as _crescendo_. We start at the top (site level), and going down in a granular fashion, we can assign them to items (documents).

### SharePoint Groups

Regardless of the type of site (_group-connected or not_), when you create a site (_although it depends on the template_), by default 3x SharePoint groups are created:

- Owners
- Members
- Visitors  

Each (built-in) group has a _permission level_ assigned to it. Use those ones first, but if they don't fit your needs, **_create a new SharePoint group_**, and assign your own custom permission level to it.

You can copy a permission level, and select or deselect options for your requirements.

> _Best Practice: If necessary, create your own SharePoint group and permission level, and avoid modifying or deleting the built-in groups. For more information, please refer to the official Microsoft documentation about the [Default SharePoint Groups](https://docs.microsoft.com/sharepoint/default-sharepoint-groups)._

### Active Directory (AD) Groups

Most organizations already have an on-premises Active Directory, which is synchronized to Microsoft 365. When assigning permissions to a SharePoint site, the recommended approach is to **_add security groups to those SharePoint groups_**.

However, it's entirely possible to create Microsoft 365 security groups directly in the admin center, and add those to your SharePoint site as well!

Active Directory groups are different from SharePoint groups. When you create a SharePoint group, it will only be available within the site where it's been created.

>_Best Practice: Add security groups to your SharePoint groups for easy management. Although it's possible to add users individually to sites, it will be harder to manage down the line._

### Breaking permission inheritance

Sometimes, you might need to share only a library or a document with a user, and not the entire site. That's where we can break permission inheritance. This is more a _Site Owner_ responsibility, rather than for a site member responsibility.

When you create a site and then start creating libraries, lists, and upload documents, all users accessing the site also have access to those libraries and documents. Remember the _crescendo_ thing? 😉

When breaking permission inheritance **_after_** creating the library or list, the default SharePoint groups (_i.e.: Owners, Members, Visitors_) will still appear under the _site permissions_ settings.
Add your account (to keep access), then _remove_ the default SharePoint groups, and _add_ whoever needs access to this library, which has now unique permissions.

### Site Sharing

Site sharing will differ if your site is connected to a Microsoft 365 Group or not. The modern interface allows for a more comprehensive way to control permissions, and offers more granularity when sharing.

#### Sites _not connected_ to Microsoft 365 groups

If your site is _not_ connected to a group, then not much has changed really. Despite the modern interface, SharePoint aficionados will still recognize how to share a site, or be familiar with the _Advanced Permissions Settings_.

![mmd](media\managing-sharepoint-online-security-a-team-effort\share-site-not-connected.png)

#### Sites _connected_ to Microsoft 365 groups

When connected to a group, you still have the possibility to **share the _Site Only_**. Meaning that you don't have to share other resources associated with a Microsoft 365 group (_i.e.: shared mailbox, Planner, etc..._).

If however, you wish to share the site as well as including the user(s) within all the resources provisioned with the Microsoft 365 group, then you need to select **Invite people** >> **Add members to group**. The choice is yours! 😉

![mmd](media\managing-sharepoint-online-security-a-team-effort\sharing-site-connected-to-group.png)

#### Change how members can share

Something else that might also mitigate how sharing occurs, is the possibility to select between the following 3 options:

- Site owners and members can share files, folders, and the site. People with Edit permissions can share files and folders.

- Site owners and members, and people with Edit permissions can share files and folders, but only site owners can share the site.

- Only site owners can share files, folders, and the site.

With regards to first 2 bullet points, the difference is that in option 2, only the site owner will be able to share the site. Members will not. I have to admit, it confused me at first, and I had to read it a few times!

While the 3rd bullet point is self explanatory, we can imagine that it might prevent users from performing their tasks? What if you need to share something with a colleague or a customer? And this will also add more work for the site owner...

This option could be used if your users are new to SharePoint, pending training for them to be more confident in sharing, or simply because you really want to prevent them from sharing.

![mmd](media\managing-sharepoint-online-security-a-team-effort\how-members-can-share.png)

### Access Requests

If you observed the screenshot above, we also had _Access Requests_ turned on by default. What is this?

This feature has been around for a while, and is better that the dreaded "Access denied" message with no possible interaction whatsoever! Although there is more configuration to be done in SharePoint on-premises, everything is ready to go in SharePoint Online!
We don't have to worry about anything else than choosing who should receive those requests, add a custom message for the requestor, and review the pending requests.

Two options for who should receive Access Requests:

- Site Owners
- Specific email

To know more about how to configure Access Requests, have a look at the official Microsoft documentation: [Set up and manage access requests](https://support.microsoft.com/office/set-up-and-manage-access-requests-94b26e0b-2822-49d4-929a-8455698654b3).

## Other Security Features To Consider

### Multi-Factor Authentication (MFA)

The first that springs to mind, and not only related to SharePoint, is MFA to secure your identities. A few years back, we were only thinking about applying MFA to (at least) Global Admins, but really it should be applied on all accounts whenever possible.

### Security and Compliance

After securing SharePoint as an environment, we'd also like to secure the _data_ hosted in SharePoint, right?

So we'll hear about **Sensitivity labels**, **Retention labels and policies**, **Data Loss Prevention (DLP)**, **Sensitive info types**... But where are those? Well, they are managed in the _Security and Compliance Center_.

Should I _manage and create_ those as a SharePoint Administrator? Probably not. This will require someone with permissions to the Security and Compliance center, as well as the knowledge to create labels and policies.

Ideally, this should be directed by company requirements, thoughtfully planned, and carefully implemented.

>_Note: Depending on your current Microsoft 365 licensing subscription(s), and the way features evolve quickly, please refer to the official Microsoft documentation: [Microsoft 365 compliance](https://docs.microsoft.com/microsoft-365/compliance/?view=o365-worldwide)_.

### Devices Accessing SharePoint Data

More options are available within the SharePoint Online Admin Center, but may rely on an Azure subscription.

![mmd](media\managing-sharepoint-online-security-a-team-effort\access-control.png)

The following documentation is very interesting to help understand how Microsoft is protecting the SharePoint and OneDrive for Business data, as well as providing other links for your reference: [How SharePoint and OneDrive safeguard your data in the cloud](https://docs.microsoft.com/sharepoint/safeguarding-your-data).

## Conclusion

As we've seen throughout this article, SharePoint security is not only a matter of having SharePoint admin permissions. It definitely is a team effort where so many other roles are involved!

---

**Principal author**: [Veronique Lengelle, MVP](https://www.linkedin.com/in/veronique-lengelle-48a71b31)