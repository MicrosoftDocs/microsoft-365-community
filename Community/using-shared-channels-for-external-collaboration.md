---
title: Using Shared Channels (Teams Connect) for External Collaboration
ms.date: 12/19/2022
author: dfrancoeur
ms.author: daisyfeller
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.service: microsoft-365
localization_priority: 
description: A short guide on setting up Shared Channels for Cross-Tenant (External) Collaboration.
ms.collection: M365Community
---

# Using Shared Channels (Teams Connect) for External Collaboration

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

One of the most exciting [announcements](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/what-s-new-in-microsoft-teams-microsoft-ignite-2021/ba-p/2118226) from **Ignite 2021** was that of **Shared Channels (Microsoft Teams Connect)** which seemingly promised to finally resolve the considerable friction involved with cross-tenant collaboration (collaborating with other organizations using Microsoft 365). The idea of Shared Channels was simple, yet powerful. Instead of moving between Tenants to access information, allow for that same information to be available within your home tenant! Now that we've been able to see it in action in the Public Preview, what do we think? Has it realized the hype from last year?

## What Are Shared Channels

At its simplest, a Shared Channel is essentially a 'collaboration space' that can be re-used in multiple places. Because it is reused, it implies that it can be accessed by different users than those who are in the Team. Only members of the Shared Channel can access it.

There are a few ways these channels can be re-used:

1. **Reused in multiple Teams across tenants** (this article) so that users from multiple organizations can work together in the same 'space' without needing to switch tenants.
2. **Reused in multiple Teams in the same tenant** ([see this article for details](using-shared-channels-for-external-collaboration.md)) so that users from multiple Teams can work together in the same space without needing access to the same Teams

## Shared Channel Limitations

While Shared Channels offer most of the same functionalities available within other channels, there are a few features that are not supported, including:

- Only Azure AD work or school accounts are supported for external participants. **Guests cannot be added to Shared Channels (see [here](https://support.microsoft.com/office/guests-and-shared-channels-in-teams-612de4ce-e7a3-4579-b086-bb8ff9f2d11e)).**
- Shared channels support tabs except for Stream, Planner, and Forms.
- Line of business (LOB) apps, bots, connectors, and message extensions are not supported.
- You cannot remove a shared channel from the parent team within which it was first created
- When you create a team from an existing team, any shared channels in the existing team won't be copied over.
- Notifications from shared channels are not included in missed activity emails.
- No Loop Components
- Not supported in Class Teams

For more details see [Shared channels in Microsoft Teams](/microsoftteams/shared-channels).

## Potential Benefits for External Collaboration

Shared Channels promised to resolve a list of common challenges with effective collaboration between organizations, including:

- **No more painful tenant switching**: By seeing cross-tenant channels as Shared Channels within our own environment, the lines between organizations become blurred and work can take place unhindered
- **Avoid over-sharing information**: By allowing for privacy of content at the channel level, we avoid the risk of users seeing content elsewhere within the Team and Microsoft365 Group.
- **Reduce Team proliferation**: Instead of creating a long list of barebones and shallow Teams, merely to support a sharing across organizations, we can now facilitate fewer but 'architecturally deeper' Teams
- **Improve visibility of information and reduce duplication of content**: By allowing for centralized channels, we can reduce and eliminate channels created for the same purposes but spread across multiple teams, and reduce them with a single source of truth which also simplifies the management and monitoring of information within the channel

![Shared Channel Benefits](media/using-shared-channels-for-external-collaboration\sharedchannels1_1.png)

## Potential Challenges

Without getting into the technical details, Teams Connect (Shared Channels) relies on something called Azure B2B Direct Connect, which is different than B2B Collaboration used for External Collaboration (Guests). The big difference is that this requires organizations to trust one another's security (essentially to 'federate' identities) in order for this feature to be available.

The key portion here is that B2B Direct Connect requires **a mutual trust relationship between two Azure AD organizations** to allow access to each other's resources. Both the resource organization and the external organization need to mutually enable B2B Direct Connect in their cross-tenant access settings. While this may not seem like the end of the world, it does seem counter to the well-known concept in Cyber Security of Zero Trust, especially its well-known adage 'never trust, always verify.'

![Shared Channel Mutual Trust](media/using-shared-channels-for-external-collaboration\sharedchannels1_2.png)

A more 'trusting' security stance may be possible for organizations with subsidiaries, or companies that all operate under shared ownership, we feel this is going to be a massive challenge for most organizations, especially those with strict security policies. This is hugely disappointing and we've heard this sentiment echoed by many clients and partners with whom we've discussed the topic.

## How To Set It Up

1. Access Azure AD > Identity Governance > Cross-tenant Access Settings
2. Add an organization to enable B2B Direct Connect
3. Find an organization by domain or Azure ID
4. Setup Default Inbound/Outbound Settings  (Host Tenant)
5. Have other tenant admin perform these steps for their organization (Recipient Tenant)
6. Setup Shared Channel (Host Tenant)
7. Send Channel Share Request (Host Tenant)
8. Accept Shared Channel (Recipient Tenant) and select Team for it to reside in
9. Approve Shared Channel Placement (Host Tenant)

**The result:**

![Shared Channel Result](media/using-shared-channels-for-external-collaboration\sharedchannels1_3.png)

Note: This sample opened up bi-directional sharing for all users in both organizations. Microsoft allows further granular controls on B2B direct connect and many additional security settings.

---

**Principal author**: [David Francoeur](https://www.linkedin.com/in/dfrancoeur/)

---
