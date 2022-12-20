---
title: Using Shared Channels (Teams Connect) for Internal Collaboration
ms.date: 12/19/2022
author: dfrancoeur
ms.author: daisyfeller
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.service: microsoft-365
localization_priority: 
description: A short guide on setting up Shared Channels for Internal Collaboration within your Tenant.
ms.collection: M365Community
---

# Using Shared Channels (Teams Connect) for Internal Collaboration

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

One of the most exciting [announcements](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/what-s-new-in-microsoft-teams-microsoft-ignite-2021/ba-p/2118226) from **Ignite 2021** was that of **Shared Channels (Microsoft Teams Connect)** which seemingly promised to finally resolve the considerable friction involved with cross-tenant collaboration (collaborating with other organizations using Microsoft365). The idea of Shared Channels was simple, yet powerful. Instead of moving between Tenants to access information, allow for that same information to be available within your home tenant! Now that we've been able to see it in action in the Public Preview, what do we think? Has it realized the hype from last year?

## What Are Shared Channels

At its simplest, a Shared Channel is essentially a 'collaboration space' that can be re-used in multiple places. Because it is reused, it implies that it can be accessed by different users than those who are in the Team. Only members of the Shared Channel can access it.

There are a few ways these channels can be re-used:

1. **Reused in multiple Teams across tenants** ([see this article for details](using-shared-channels-for-external-collaboration.md)) so that users from multiple organizations can work together in the same 'space' without needing to switch tenants.
2. **Reused in multiple Teams in the same tenant** (this article) so that users from multiple Teams can work together in the same space without needing access to the same Teams

## Shared Channel Limitations

While Shared Channels offer most of the same functionalities available within other channels, there are a few features that are not supported, including:

- Only Azure AD work or school accounts are supported for external participants. **Guests cannot be added to Shared Channels (see [Guests and shared channels in Teams](https://support.microsoft.com/office/guests-and-shared-channels-in-teams-612de4ce-e7a3-4579-b086-bb8ff9f2d11e)).**
- Shared channels support tabs except for Stream, Planner, and Forms.
- LOB apps, bots, connectors, and message extensions are not supported.
- When you create a team from an existing team, any shared channels in the existing team won't be copied over.
- You cannot remove a shared channel from the parent team within which it was first created
- Notifications from shared channels are not included in missed activity emails.
- No Loop Components
- Not supported in Class Teams

For more details see [here](/microsoftteams/shared-channels).

## Potential Benefits for Internal Collaboration

Interestingly, while it was not the focus of early demos and previews from Microsoft, there is one very interesting use case for Shared Channels that does not require the need for external security decisions. In fact, it doesn't even relate to collaboration with external organizations. Though counter-intuitive to its original premise, there is a very real use case for Shared Channels within an organization to streamline knowledge management and sharing! Rather than needing to create such spaces as separate 'communities', traditionally entire Teams, we can now create these as re-usable channels and add them wherever we need - a much more flexible and modular approach.

It is important to note that some organizations are already using Yammer for some of these use cases, and we do not intend to imply this is a bad approach. Yammer has fantastic community-based functionality with its great Q+A features and much more. That being said, for organizations not ready or willing to introduce another tool into the mix, there is now an option available within Teams that can simplify information management, and streamline communication without adding considerable new layers of complexity.

**Some benefits we see of this internal use case include:**

- Access to useful information within the context of an existing Team, such as a project
- Reduced Teams proliferation
- Fewer Teams that must be made Public, or that require inviting huge swaths of the organization as users
- Single Source of Truth
- Better retention of knowledge and simpler knowledge management
- Better visibility and 'findability' of important information

## Potential Challenges

One issue we see with Shared Channels is just how confusing the whole experience seems to be for end-users. Firstly now users have a choice of 3 types of channels that they can create:

![Shared Channel Challenges 1](media/using-shared-channels-for-internal-collaboration\sharedchannels2_1.png)

This can be confusing as users rarely know the different channel type (Public vs Private) but now there is another one in the mix. This will require significant knowledge on behalf of users to understand the subtle difference.

Also when sharing a Shared Channel the options are even more strange and confusing:

![Shared Channel Challenges 2](media/using-shared-channels-for-internal-collaboration\sharedchannels2_2.png)

The options are confusing to many users. While the choice of 'People' is straightforward, selecting a 'Team' actually prompts the user to find a Team Owner, not a Team. This Team Owner will decide where the Channel will be placed. Again this leads to all sort of confusion to what exactly a Shared Channel is, who is a member and who can access it.

## How to Set It Up

1. Ensure Shared Channel creation is enabled in Teams Admin > Teams Policies
2. Locate the Team that will serve as the permanent host
3. Click Add Channel, give the channel a Name, then select Shared Channel for Privacy
4. Once the channel is created, click Manage Channel for the new Shared Channel
5. Using the button at the top right, click Share with a Team (for a team owned by someone else), or Share with a Team You Own (for a team you own
    - If Sharing with a Team You Own, find the Team from the list and click Done.
    - If Sharing with a Team (i.e., Sharing with a Team you do not own) locate the Team **Owner** and click Send Invite. This will send the invite to the Team Owner to approve and they will select where to use this Channel. Once they have Accepted, a notification will arrive prompting you to to Approve where they have placed it. If you cannot locate the notification, return to Manage the Channel and view Sent Invites.

**The result:**

![Shared Channel Result](media/using-shared-channels-for-internal-collaboration\sharedchannels2_3.png)

---

**Principal author**: [David Francoeur](https://www.linkedin.com/in/dfrancoeur/)

---
