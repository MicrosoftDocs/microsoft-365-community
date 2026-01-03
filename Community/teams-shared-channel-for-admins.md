---
title: Teams Shared Channels for Admins
ms.date: 2/21/2025
author: JimmyHang
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: concept-article
ms.author: pamgreen
ms.service: microsoft-365
ms.custom: msteams
ms.localizationpriority: Low
description: "Teams Shared Channels for Admins"
ms.collection: M365Community
---

# Teams Shared Channels for Admins

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

A Teams "Shared Channel" is one of the greatest, if not THE Greatest new feature released to Teams in 2022.

## Enabling Shared Channels

To enable and understand more about this feature, follow one of the guides in the [Resources](#resources) section.

After you have enabled Shared Channels and created your first Shared Channel, there are a couple of things which are good to know.

## The difference between external "Guests" and "External" users

When you add a external user to your Team, you will see that the user is labeled as a "Guest".

:::image type="content" alt-text="Adding a guest to Teams" source="media/teams-shared-channel-for-admins/tsc01.png":::

When you add the same user to a Shared Channel, that external user will be labeled with "External", meaning there won't be a "conflict" related to the user for this channel.

:::image type="content" alt-text="Adding an external user to Teams" source="media/teams-shared-channel-for-admins/tsc02.png":::

After the External user is added, in their Teams client they will receive a notification and the External team will show up. This works almost instantly for the user.

This is also super sweet, as the users don't need to switch tenants.

:::image type="content" alt-text="Notification about external channel" source="media/teams-shared-channel-for-admins/tsc03.png":::

Collaborating in chats will show an "alert" with a message about the Shared Channel.

:::image type="content" alt-text="Alert about external sharing" source="media/teams-shared-channel-for-admins/tsc04.png":::

## Where is the "External" user?

As you may know, when you add a external user in a Microsoft Team, they exist as a "Guest", and the guest record will exist in your [Microsoft Entra ID](glossary.md#azure-active-directory-aad), meaning you can enforce policies, such as [Multi-Factor Authentication (MFA)](glossary.md#multi-factor-authentication-mfa) for the guest account.

But for Shared Channels, the "External" user only exists as an external user to that Shared Channel. Currently, there are three places where we can see those external users:

1. In the *Manage channel* settings for the channel
1. In the Teams Admin Center by drilling into the Team and the specific channel
1. In the Site permissions fro the backing SharePoint site

### Manage channel settings for the channel

In the Manage channel settings, you can see the external users in the Members section.

:::image type="content" alt-text="Manage channel settings" source="media/teams-shared-channel-for-admins/tsc08.png":::

### Teams Admin Center

In the Teams Admin Center, you can drill into the Team and the Shared Channel to see the Members.

:::image type="content" alt-text="Manage channel settings in the Teams Admin Center" source="media/teams-shared-channel-for-admins/tsc09.png":::

### SharePoint Site Permissions

In the SharePoint site which is created for the Shared Channel, you won't have a link option for "Site permissions" in the "Site settings" menu to check there, either.

:::image type="content" alt-text="Shared Channel site settings" source="media/teams-shared-channel-for-admins/tsc05.png":::

But it doesn't mean that the permission page is not there. Navigating to your Shared Channel site with the extra url `/_layouts/15/user.aspx` will take you to the classic permission page you're used to.

:::image type="content" alt-text="Shared Channel site permission settings" source="media/teams-shared-channel-for-admins/tsc06.png":::

Here, you can see your External users with their "ObjectId" and "HomeTenantId".

:::image type="content" alt-text="External user information" source="media/teams-shared-channel-for-admins/tsc07.png":::

## Tips and tricks before enabling Shared Channels for production

1. Review your user training, and make sure everyone knows the difference between "Guest" and "External" users.
2. Beware that the External user can't be managed outside the Teams Shared Channel settings.
3. If you plan to use Shared Channels, make sure you update your governance policies.

## Resources

* [Andrés Gorzelany - Enabling Teams Shared Channels 101](https://get-itips.capazero.net/posts/shared-channels-101)
* [Shared channels in Microsoft Teams (Preview)](/microsoftteams/shared-channels)
* [B2B direct connect overview (Preview)](/azure/active-directory/external-identities/b2b-direct-connect-overview)

---

**Principal author**: [Jimmy Hang, MCT, MCSE: Productivity](https://www.linkedin.com/in/jimmyhang/)

---
