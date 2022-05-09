---
title: Microsoft 365 Search Technologies
ms.date: 12/07/2021
author: davemehr
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: microsoft-365
localization_priority: 
description: "Content can be searched using various search technologies. The existing variants are based on the same search index, but differ in usage and configuration."
ms.collection: M365Community
---

# Microsoft 365 Search Technologies

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

In Microsoft 365, content can be searched for using various search technologies. The existing variants are based on the same search index, but differ in usage and configuration.

A distinction is made between the following possibilities:

- Microsoft search (Modern search)
- SharePoint search (Classic search with PnP Modern Search Web Parts)
- SharePoint search (Classic search)

## Microsoft Search (Modern search)

Microsoft Search is based on the Microsoft Search engine, which provides data using the Microsoft Graph and other sources. Microsoft Search uses AI components and the Bing algorithm to display the information and data in a more user-friendly way. In most Microsoft applications, the Microsoft Search Box is available at the top of the header. Results are displayed in the context of the application. In the Microsoft Productivity Apps (Word, Excel, PowerPoint, etc.) you can search for content as well as for functions, e.g. reusable slides. The contents of documents are full-text indexed and it is possible to search for metadata or content.

### Why use Microsoft Search?

Microsoft Search is a standardized search, which is constantly being further developed by Microsoft and enriched with new functions. The search box is enriched with AI components and brings the user to the center. The search results in the productivity applications (such as Word, Excel, PowerPoint) cannot be adjusted. Application-related functions and documents are displayed.

The Search verticals in Search from office.com and SharePoint online modern sites contain much-used content in SharePoint and OneDrive. It's possible to create your own search verticals with Microsoft Search. Custom connectors can also be added as verticals and are displayed for use in both Microsoft 365 and Microsoft Search in Bing. Some standard connectors are available, but these can also be added via third-party providers or through in-house development.

### When to use Microsoft Search?

You can consider using Microsoft Search in the following examples:

- Unified Search experience in M365 e.g. office.com, SharePoint Online, Office applications
- Standard functions, without adjustments and configuration, Microsoft Search can be used directly
- Use of AI components in the search box
- Standard, developed, or third-party connectors

## SharePoint Search (Classic Search with PnP Modern search Web Parts)

SharePoint Search is based on the index of the SharePoint Search Engine and contains content and documents from SharePoint as well as OneDrive. Content, lists, and their metadata can be searched. The PnP Modern Search WebParts can be added and configured on modern SharePoint pages. The SharePoint search engine or the Microsoft search engine can be used as the data source.

### Why use SharePoint Search (PnP Modern Search Web Parts)?

SharePoint Search is only available within SharePoint and not in the other Microsoft 365 applications or entry pages. To use SharePoint Search on modern sites and pages, the free [PnP Modern Search Web Parts solution](https://microsoft-search.github.io/pnp-modern-search/) must be installed and configured. The Web Parts can be used to configure search boxes, search verticals, search filters and search results. The Web Parts are configured so that the information is passed on to the respective Web Part. Likewise, the visualization of search results can be customized, several verticals can be integrated, and the filters can be adjusted.

### When to use SharePoint Search (PnP Modern Search Web Parts)?

With the PnP Modern Search Web Parts, SharePoint Search can be customized. Usage is limited to SharePoint or individual SharePoint sites. Scenarios for the use of SharePoint Search can be:

- SharePoint Search Center
- SharePoint application-related search
- Search driven application, with the use of dynamic parameters as Search Query
- Modern Search in an on premises farm

## SharePoint Search (Classic search)

SharePoint Search is configured in the SharePoint admin center. Content from SharePoint as well as OneDrive is indexed. The content is fully indexed, it can be searched for content as well as metadata. On classic SharePoint pages on-premises, the classic SharePoint Search Web Parts can be used. In SharePoint Online, the classic Search Web Parts are available, but it is an outdated technology and is not evolving.

### Why use SharePoint classic search?

In order to customize a search center on a classic SharePoint environment, SharePoint Search is used and adapted with the classic search Web Parts. The Web Parts for Search Box, Search Navigation, Search Results as well as refinements can be adapted and connected to each other so that the search results are adjusted based on the search input or filter.

### When to use SharePoint classic Search?

Classic search can be used on on-premises farms to implement enterprise-wide search centers. The Search Web Parts can be used in the following scenarios

- Classic Search in On-Premises Farm
- SharePoint Search Center
- SharePoint application-related search
- Search driven application, with the use of dynamic parameters as Search Query

## When to use which search technology?

- Microsoft Search: In Microsoft 365 for a cross-Microsoft 365 application search
- SharePoint Search (with PnP Modern search Web Parts): Customized SharePoint Search Center in Microsoft 365 or SharePoint on premises
- SharePoint Search (classic): Customized SharePoint Search Center on SharePoint on premises

---

**Principal author**: [David Mehr](https://www.linkedin.com/in/david-mehr-055b46181/)

---
