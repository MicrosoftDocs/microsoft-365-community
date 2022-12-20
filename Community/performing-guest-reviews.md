---
title: Performing Guests Reviews with Azure Identity Governance
ms.date: 12/19/2022
author: dfrancoeur
ms.reviewer: sympmarc
manager: 
ms.topic: article
ms.author: 
ms.service: microsoft-365
localization_priority: 
description: A short guide on performing Guests Reviews using Azure P2 and its Identity Governance features.
ms.collection: M365Community
---

# Performing Guests Reviews with Azure Identity Governance

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

Throughout conversations with many organizations using Microsoft 365, we’ve heard a consistent refrain about Guest Management – for most, it’s simply not a “manageable” task to oversee guests with the tools they have. Most administrators feel ill-equipped to get a full understanding of the extent of Guest Access within their Tenant, let alone make decisions on whether current Guests and their access are still legitimate, or not. As collaboration scenarios grow in complexity, organizations mature in their usage patterns of the M365 platform, and digital security becomes an increasingly scrutinized part of the enterprise – the challenge of managing Guests is reaching a tipping point where it can no longer be ignored.

## Why Review Guests?

There are a host of reasons justifying the need to review an organization’s Guest accounts, but a short summary will serve the purposes of this article. Some of these reasons include:

- Guests are easily “forgotten” and retain lingering access to Teams, Sites, Apps, and Content long after they need it. This presents a significant possible security risk, especially as new users join the workspaces and begin to add content to workspaces they assumed were private.
- We often know little to nothing about Guest accounts, meaning it is easy for users to share the wrong content with the wrong person. This again presents a significant possible security risk. 
- Many organizations do not archive or decommission workspaces that are no longer active. For internal users, this amounts to noise, but for guest users who retain their access, this can have more serious consequences.
- Many guests never even redeem their invitation to collaborate with your tenant, but by virtue of being invited, they exist in your Azure Active Directory and can be selected again as a Guest via search.
- Lack of controls and governance policies at the Tenant or Group levels may have led Guests to be inadvertently granted access to more than the sender realized.
- In the vast majority of cases, there is a lack of a “reporting structure” for guests, meaning no one within an organization is assigned the role of managing/sponsoring/overseeing a particular Guest. This general lack of responsibility and accountability often means disorder.
- Even once Guest policies are put in effect (e.g., Guest Group Setting in PowerShell, or Sensitivity Labels), existing Guest users are left behind in these workspaces. 

## What Is Required to Set Up a Guest Review Process

The Features discussed below required Azure AD Premium P2 licenses. 

See the following resources:
- [What are access reviews | Microsoft Learn](https://learn.microsoft.com/en-us/azure/active-directory/governance/access-reviews-overview) 
- [MAU billing model for Azure AD External Identities | Microsoft Learn](https://learn.microsoft.com/en-us/azure/active-directory/external-identities/external-identities-pricing).

## How to Set Up A Guest Review Process

1. Navigate to Portal.Azure.com.  
2. Locate **Identity Governance** under Services.  
![GuestReviews1](media\performing-guest-reviews\guestreviews1.png)

3. Navigate to **Access Reviews** and click **New Access Review**.  
![GuestReviews2](media\performing-guest-reviews\guestreviews2.png)

4. Under the *Review Type* tab, select the Type of Review being created (Teams + Groups, or Applications).  
![GuestReviews3](media\performing-guest-reviews\guestreviews3.png)

5. Configure the **Review Scope** and if desired, choose whether to include only Inactive Users and specify an inactivity day threshold (e.g., 30 days).  
![GuestReviews4](media\performing-guest-reviews\guestreviews4.png)

6. Under the Reviews tab, select the way the Reviews shall be carried out. For the purposes of this blog, I will begin a review immediately on all workspaces with Guests, and subsequently, repeat the process on a Quarterly basis. I’ve opted for a multi-stage review (Note: Multi-Stage access reviews are currently in Preview) where my first stage will ask Guests to perform a Self-Review, followed by a second stage performed by Team Owners. I also specify a Fallback Reviewer (Adele Vance) if a Team Owner cannot be found. 
![GuestReviews5](media\performing-guest-reviews\guestreviews5.png)

7. At the bottom of the tab, select the scenarios that can progress from Stage 1 to Stage 2. In my case any guest that has decided during the self-review that their access can be removed need not continue to the second stage – only guests who believe they still need access or did not provide an authoritative answer should proceed to the second stage. 
![GuestReviews6](media\performing-guest-reviews\guestreviews6.png)

8. Under **Settings**, determine whether you wish to use ‘Decision Helpers’ and what should occur if reviewers do not respond to the process. 
![GuestReviews7](media\performing-guest-reviews\guestreviews7.png)

9. On the Confirmation Screen, confirm and Create the Access Review. 

## What Participants will Receive

Participants in a Guest Review process will receive an email from Microsoft and direct them to the My Access portal to action the review. The user experience is not bad, but is likely to require some adoption and change management efforts to be successful.
![GuestReviews8](media\performing-guest-reviews\guestreviews8.png)
![GuestReviews9](media\performing-guest-reviews\guestreviews9.png)
![GuestReviews10](media\performing-guest-reviews\guestreviews10.png)
![GuestReviews11](media\performing-guest-reviews\guestreviews11.png)

## Monitoring A Guest Review Process
To monitor an ongoing Access Review, the Access Review can be opened, and individual Groups can then be expanded. This can be quite challenging when done at scale and it is difficult to get an overall sense of individual guests and their current access reviews across the environment.
![GuestReviews12](media\performing-guest-reviews\guestreviews12.png)
![GuestReviews13](media\performing-guest-reviews\guestreviews13.png)
![GuestReviews14](media\performing-guest-reviews\guestreviews14.png)
![GuestReviews15](media\performing-guest-reviews\guestreviews15.png)

---

**Principal author**: [David Francoeur](https://www.linkedin.com/in/dfrancoeur/)

---
