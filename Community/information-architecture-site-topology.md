---
title: Information Architecture - Site Topology
ms.date: 3/3/2020
author: hugoabernier
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: overview
ms.author: pamgreen
ms.service: microsoft-365
ms.custom: sharepoint-online
ms.localizationpriority: Low
description: "Information Architecture - Site Topology"
ms.collection: M365Community
---

# Information Architecture - Site Topology

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

With the advent of modern pages in SharePoint Online, the classic top-down site topology, as we know it, has evolved to a flat structure that is designed to adapt to your changing organizational structure and content.

## What we mean by *site topology*

When we say *site topology*, we mean how we arrange site collections and sites to create a SharePoint site structure.

We prefer the term *topology* over *hierarchy* or *navigation* because your hierarchy and navigation can be significantly different from how you create your site structure.

## Classic site topology and challenges

Long before SharePoint Online and modern sites became available, the common practice was to create a top-down site topology, with a single root and multiple subsites below it. For most organizations, the top-down structure mimics its organization structure. The topmost site (or root) represents the organization, with each subsite representing divisions, departments, projects, etc. Within division or department sites, organizations often create restricted access team or project subsites.

The classical top-down topology presents many challenges:

- **Company restructuring:** Changes to a company's organizational structure requires significant changes to the SharePoint site topology, often resulting in broken links, missing documents, duplicated or orphaned content. In some instances, organizations may choose to avoid the effort of moving sites, resulting in a discrepancy between the organization's structure and the SharePoint site structure.
- **Deleting sites:** If a site has one or more subsites below it, SharePoint prevents the site from being deleted. Before deleting a site, you must move all its subsites to another location.
- **Complex permissions:** With a top-down site topology, organizations often resort to using a mix of inherited and broken site permissions to protect information at each level adequately. The mixed security inheritance can often make it difficult to determine who has access to which content.
- **URL Length:** As the number of subsite levels increases, the URLs to each subsite's documents become longer. Longer URLs may cause issues with older desktop applications and operating systems, often manifesting itself as an error opening or saving a file. 
- **Difficulty discovering content:** SharePoint search allows users to find content regardless of how many layers deep it resides within a site topology. However, users who wish to discover content by navigating through a site may find it challenging to find the content they seek, requiring them to navigate up and down the site structure.

## The need for flat topologies

Office 365 provides users with self-service capabilities; by default, users can create their own SharePoint site collections, Office 365 Groups, or Microsoft Teams, for example.

Every new SharePoint site collection is created under the flat topology, with new site collections being placed either https://*tenantname*.sharepoint.com/sites/*sitename* or https://*tenantname*.sharepoint.com/teams/*sitename*, depending on the type of site (and the tenant site creation settings).

Also, when a user creates a new Team in Microsoft Teams, Office 365 creates an associated SharePoint site collection (also located under https://*tenantname*.sharepoint.com/sites/*sitename* or https://*tenantname*.sharepoint.com/teams/*sitename*); Microsoft Teams uses the associated SharePoint site collection to store documents and other relevant information.

The same applies to Office 365 Groups from Outlook, Planner, or Viva Engage.

The flat topology helps support a self-service and cross-product architecture that would be practically impossible to manage in a top-down topology.

Using a flat topology, site owners can easily manage user permissions for their sites; because every site is a top-level site collection, there no inherited permissions to complicate things.  

In the event of a company's organizational restructuring, there is no need to move sites to match the organization structure, because every site is a top-level site collection.

## Designing for a flat topology

The key to designing a flat topology is to understand that content in SharePoint can exist across three different "dimensions":

- **Physical:** Where content is created and stored within a SharePoint topology.
- **Logical:** Where content appears within a topology -- regardless where it physically resides.
- **Metadata:** Information about sites and content that can be used to identify and find it, regardless of where it physically resides.

### Creating the physical topology

The physical structure is relatively straightforward: each site is physically created as a separate site collection just below the root of your SharePoint tenant, under https://*tenantname*.sharepoint.com/sites/*sitename* or https://*tenantname*.sharepoint.com/teams/*sitename*, regardless of whether you create a Team Site or Communication site.

When deciding how many sites you need to create, you should consider the following criteria:

- **Authors:** Design your physical site topology to cater to people who create and maintain content. Content should be stored where it is best managed.
- **Security and Policies:** Create a site topology that makes it easy to assign permissions; avoid creating sites that require a complex security matrix to determine who has permissions to which content, as it often results in difficulties maintaining sites. If in doubt, create two sites with different permissions. Also, keep in mind your organization's governance and compliance policies, such as retention, external sharing, quotas, and so on.
- **Lifecycle:** Design your physical site topology with your content lifecycle and workflows in mind.

For example:

- Should you create a single site for your Accounting department to store Accounts Receivable documents, Accounts Payable, and Financial Statements, or should you separate them into two (or more sites)? It ultimately depends on who should have permissions to what content.
- If you need to create an Annual Report every year, do you create a single site called Annual Report and change permissions every year, or do you create a new site every year? It depends on whether the people contributing to the annual report change every year.

Although your company's organizational structure may help to identify your physical site topology, do not limit yourself to replicating it.

For example, your *Human Resources* department may need a *team* site to store confidential information about employees, which can be accessed only by HR staff, *and* a *communication* site to store company-wide information about policies and benefits which is accessible to everyone in the organization.

### Creating the logical topology

While the *physical* topology caters to people who create content, your *logical* topology should cater to people who consume content. In other words, your logical topology is how you present content to your users in a way that makes sense to them, regardless of your physical topology.

For example, your HR department may have different sites for **Benefits**, **New Hires**, and **Recognition and Awards**; To make it for your employees to find content, you may wish to *logically* group under an **HR** site. To do so, you could create a *communication* site called **HR**, convert it to a *Hub Site*, and assign **Benefits**, **New Hires**, and **Recognition and Awards** to the **HR** hub site.  Although all 4 sites are *physically* at the same level, they *logically* appear to be in a hierarchical structure.

### The metadata topology

The best topology you could ever create would be one that is customized to suit the individual needs of every single person in your organization. While such a topology would be ideal, it would also be impractical to create and impossible for anyone to manage.

However, a computer can do precisely that; using machine learning, Office 365 and SharePoint can observe every user's activities, interests, and usage patterns to determine which sites to display on a user's SharePoint landing page.

When a user arrives at their SharePoint Home, SharePoint helps users find relevant content by showing relevant news and recent activities from sites that the user follows. It also shows sites that the user frequently visits, and makes recommendations based on the user's past activities and their peers' activities.

While you cannot control this behavior, you should be aware that your site topology can positively influence SharePoint's ability to deliver the right information to users.

For example, if you created a large, monolithic site that contained all of your company's content in a single place, SharePoint would be less able to highlight relevant content for users. The same site would always appear on the SharePoint Home page for every user, showing too many recent activities to help users make sense of what matters.

On the other hand, if you separate the content into smaller sites based on their purpose, SharePoint would be able to identify which sites were recently changed and highlight those changes to the relevant users.

After you consider your *physical* and *logical* site topology, take a look at the *metadata* topology.

## Naming conventions

As you develop your organization's site topology, you may wish to define a site collection naming convention. A naming convention can help users identify the function of a site collection, membership, geographic region, or who created the site collection.

As Office 365 allows users to create site collections, either directly in SharePoint, or via any other group workloads (Outlook, Microsoft Teams, Planner, or Viva Engage), the only 100% reliable way to enforce a naming convention is by enabling *group naming policies*.

Since all Office 365 group workloads automatically create SharePoint site collections, naming policies affect all group workloads -- not just SharePoint.

There are two types of policies

- **Prefix and/or Suffix:** You can define prefixes and/or suffixes to automatically add either a fixed string (e.g., **GRP_**) or a user attribute (e.g., **[Department]**) before or after the group name. For example, if you define a group naming policy with `GRP [GroupName] [Department],` and a user from the IT department wants to create a group called **My Group**, the complete group name will be **GRP My Group IT**.
- **Custom blocked words:** You can define a comma-separated list of words that you do not wish to allow in the group name. The words are case insensitive, and only whole word matches apply (i.e., no partial matching).

You can use custom blocked words to "reserve" keywords and prevent multiple users from creating multiple departmental sites. For example, you could define **HR** as a blocked word to prevent users from creating an HR site until you have created the appropriate topology.

The Office 365 Global Administrator and a few other administrator roles are exempted from these restrictions.  You can potentially apply the policies to prevent users from creating sites with blocked words without affecting your ability to create the site topology your organization needs.

To find out more about Group naming policies, and to learn to define them, visit the [Office 365 Groups naming policies documentation](/office365/admin/create-groups/groups-naming-policy).

---

**Principal author**: [Hugo Bernier](https://www.linkedin.com/in/bernierh)
