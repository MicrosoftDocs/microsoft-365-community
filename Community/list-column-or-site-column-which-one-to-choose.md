---
title: List columns or Site columns - Which one to choose?
ms.date: 3/3/2020
author: veronicageek
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: concept-article
ms.author: pamgreen
ms.service: microsoft-365
ms.custom: sharepoint-online
ms.localizationpriority: Low
description: "List columns or Site columns: Which one to choose?"
ms.collection: M365Community
---

# List columns or Site columns: Which one to choose?

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

We have two (2) types of columns in SharePoint:

- List columns
- Site columns

One is created at the list/library level (_list columns_), and the other one at the site level (_site columns_).

From a _functionality_ perspective, they do the exact same thing. From a _reusability_ perspective, not so much.

## List columns

If we take the example of SharePoint Online, we can now [create a column in a list or document library](https://support.office.com/article/create-a-column-in-a-sharepoint-list-or-library-2b0361ae-1bd3-41a3-8329-269e5f81cfa2) very easily. Hover between 2 columns, click on the "*+*" sign, and create your column.  

But by doing that, the column will only be created at the list/library level, and therefore, be of type _List column_.
  
### What does list column mean?

It means that your column will only be available to that particular list/library, and _not_ outside that boundary. If you wish to use that column outside of that list/library, you will have to recreate it at the new location.

Which brings us to Site columns!

## Site columns

As we've seen above, list columns are easy to create, but live in a "container" which is the list/library you create(d) it within.  

_Site columns_ on the other hand, are created at the site level, and available to reuse _from_ the site they're created in (as the starting point).  

### What does site column mean?

Well, this means that if you create a site column at the root of your site collection, the column will be available throughout the entire site collection. <br>
If you create a site column at the subsite level, this column will only be available for the subsite itself, and every other subsite(s) underneath. But not above.

Site columns are "shared" between sites, but only hierarchically.

## So which one should you choose?

If you're sure that the column will only need to be used/created in a particular list or library, then a _list column_ is easy and quick.<br>

If you're looking for reusability across list/library boundaries, then create a _site column_.

To be Search aware, another aspect to consider in your decision is, whether you are going to use Search to find existing content in the created column or, additionally, use the column in Search queries to find content.<br>
Creating a _site column_ will create a Search managed property (MP) automatically which you can use to Search for content. While with a _list column_ it won't create a MP, but you will still be able to Search for column contents.<br>

Say that _site column_ is MySiteColumn of type single line of text. After you add content to it, a new MP will be created with name MySiteColumnOWSTEXT ([How site columns become managed properties](/sharepoint/technical-reference/automatically-created-managed-properties-in-sharepoint)) which you can use to retrieve content in a Search query, like for example:

MySiteColumnOWSTEXT:contoso

This would return only items which column MySiteColumn contains "contoso".

However, if you opt to create a _list column_ you can accomplish the same later. The only difference is that with _site column_ it will be done automatically whereas with _list column_ you will have to go through extra steps which involves among others, creating a new custom MP.

---

**Principal author**: [Veronique Lengelle, MVP](https://www.linkedin.com/in/veronique-lengelle-48a71b31)

