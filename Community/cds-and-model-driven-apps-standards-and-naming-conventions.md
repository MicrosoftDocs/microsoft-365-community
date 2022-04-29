---
title: Dataverse and Model-Driven Apps Standards and Naming Conventions
ms.date: 3/29/2021
author:  sympmarc
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: power-platform
ms.subservice: dataverse
localization_priority: 
description: "Dataverse and Model-Driven Apps Standards and Naming Conventions"
ms.collection: M365Community
---

# Dataverse and Model-Driven Apps Standards and Naming Conventions

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

[!INCLUDE [cc-data-platform-banner](includes/cc-data-platform-banner.md)]

In any technology or programming language, there are generally accepted better practices when it comes to naming conventions, thinking about data structures, etc. It's no different with the Power Platform. Even if you are the lone person working on a solution, future you will appreciate following some consistent standards. If you are a part of a team, then that team should agree on a set of standards.

This article outlines some suggested approaches to naming conventions and how to think about bringing that consistency to your solutions. Treat it as a set of suggestions which, when followed, will lead to more maintainable and consistent solutions. However, it's also a set of suggestions, so feel free to take this set of suggestions and adapt it for your own use.

## Overview

## Dataverse

### Solution Prefix

The solution prefix helps you identify columns which are custom for your solution.

### Entities

Entities are always nouns. Each table has a singular and a plural name.

This is similar to the way you should name Content Types in SharePoint: a Content Type name is singular, the place you store them is plural.

### Columns

Columns are attributes of Entities. They describe something about the Table. Examples might include: `CustomerName`, `IsConfirmed`, or `ReceivedOn`. Consistency and care in naming columns is important to both give clues about how they should be used as well as a clear way to understand what values they will contain. A column name like `a123_ColumnName17` provides no apparent value, whereas a column name like `Account: Address 1` does.

#### Related Columns

Related column logical names should be suffixed with `id`. As an example, a many-to-one relationship from an table called Measure to an table called Session might be `pub_sessionid`.

Relationship table names should be renamed to `pub_measure_N1_session`.

#### Date Columns

#### Boolean Columns

Boolean columns are either true or false; yes or no, 1 or 0. They have only two states. Name your boolean columns with a verb, such as `IsActive` or `HasSales`.

## Model-Driven Apps
