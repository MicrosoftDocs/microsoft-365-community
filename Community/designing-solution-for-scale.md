---
title: Designing your solution for scale
ms.date: 3/3/2020
author: pkbullock
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: concept-article
ms.author: pamgreen
ms.service: microsoft-365
ms.custom: sharepoint-online
ms.localizationpriority: Low
description: "Designing your solution for scale"
ms.collection: M365Community
---
# Designing your solution for scale

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## Introduction

This article refers to design considerations of scaling your solutions, for example, in this scenario - you have built your solution and tested on a site or library, you have demoed to your boss, they are very happy and then he goes "Hey now, great solution, can you get this out to 1,000 sites please?"

The requirement has changed - to note, it is best to ask this question early. So you can plan for this and determine what kinds of points do you think about, when building your solution on this scale.

To note, SharePoint Online supports 2,000,000 site collections (Nov 19) to give you context to how large implementations can in theory support.

You now have your solution, so lets go through the kind of aspects of the solution you should consider, to see if you need to make amendments, or think about its design.

## Centralised, Decentralisation or Both

First question to ask yourself, do you need to deploy this solution 1,000 times or can you place a navigation link on 1000 sites referring to a single location? The decision on your approach can be determined by the following points:

- Initial deployment, where do my assets live? How many times do I need to repeat the steps for deployment? The approach depends variances for each department or instance for example, can you get away with a settings file instead?
- Maintainability, as changes occur, you may need to repeat deployment?
- Security, is there a solid reason to keep the solution separate?
- Technical limits of the product, will SharePoint allow you to centralise?

### Centralisation

Centralisation refers to a single point in which assets and solution is referred to.

For example, if you have a JavaScript based solution, consider locating the files into one place, not near the instance but somewhere within you farm or tenant that is readable to all. Changes to the central point reflect on all areas of usage.

A scenario where this may apply e.g. if you have 1 Intranet each with 1000+ pages within. You deploy once rather than all 1000 times.

### Partial Centralisation

Partial centralisation is an option too, not all solutions can be centralised so look at the components of your design and see what can be centralised.

A scenario where this may apply e.g. if you have 10 departments each with 100 sites within. You deploy 10 times rather than all 1000. Ideally, getting this number down will make your life easier - the less "copies" of your solution the better.

### Decentralisation

Decentralised solutions can only be deployed one to one with their instance. In this scenario, you deploy 1000 times.

The goals change to reduce the implementation steps and how can I make this easier to deploy. Should I consider a scripted deployment?when considering you approach, is the effort of learning how to script deployment vs the actual deployment time.

## Information Architecture

When designing for scale you will need to consider how this affects information architecture approach.

With large scale deployments, there are several factors to consider:

### Naming convention

Clear naming of SharePoint artefacts provide context to the user that is visiting the site, library and metadata they are expected to complete.

There is a separate article coming soon for naming conventions.

### Columns and Content Types

What level do you define columns and content types e.g. list, web, site, enterprise. The goal should be to keep things simple and use inheritance where possible. Although, modern SharePoint makes it very easy to break from this model.

There is a great article about the types of column: [List column or Site Column - Which one to choose](list-column-or-site-column-which-one-to-choose.md)

### Sites

How you structure your sites, does your solution require lots of subsites? Typically, Microsoft is driving a flat architectural model and you should consider using multiple site collections grouped locally by hub sites.

There is more detail on site typology in this article: [Information architecture - site topology](information-architecture-site-topology.md)

## Security

Security should always be an important consideration in any solution, no matter how complex or how quick solutions is built.

Understand who can access your data - ask yourself does this data contain any personal information? Is the data business critical or sensitive?

In SharePoint, there are three main models of security, one for users, SharePoint security groups and active directory groups.

This will go into more detail in a later article.

## Multiple Environments

Multiple environments such as separate site collection, web application (on-premises) or tenant add a layer of protection for solution builders to ensure their solution works as expected. The number of environments is up to you, consider these factors in determining if A, you need a separate environment or B, if you do - how many.

- Does your solution need to involve training users? Ideally having a separate environment to contain the "test" data that will be introduced during these. Filling up production with test data, may reduce search effectiveness if the test content contains enough keywords in be prominent in the results.

- Development isolation from live data. In development, certain aspects maybe required elevated permissions to setup or create the solution. You may outsource the development to a 3rd party in which you want to limit the access to the data in the tenant. I always recommend a developer tenant where possible, they can be obtained easily from [Microsoft 365 Developer Program](https://developer.microsoft.com/microsoft-365/dev-program) if a developer inadvertently causes problems in the tenant, it is contained away from production.

- Do you need a UAT or test environment? Allowing the business owners or stakeholders to review the work and play with it. This ideally should be a almost realistic version of production with similar configuration, this will allow you to assess solution impact, test any downtime and your deployment strategies.

The number of environments is up to you, there are additional overheads with having multiple tenants but if you weigh up the cost for your organisation against an incident on production it will be worth the effort.

## Maintainability

Maintainability refers to the ease of making changes to your app, updates or cleanup aspects of your solution - how easy this is to achieve.

Consider your solution - you have deployed to 1000 sites and you boss goes, "Great app, but can you add a column to each list, I really need this." You now need to figure out updates to each of the 1000 sites.

## Manual vs Deployment

Deployment strategy is worth planning ahead of rollout of your new features, there are a number of factors to consider, in larger scale implementations:

- Are you going to click 1000 times with a 10 step process or weigh up the effort to  learn PowerShell script to automate this. Personally, I consider the PowerShell route if a process goes beyond a few steps or if I get a sense the deployment will be repeated multiple times.
- Not all requirements are correctly articulated by the business or interpreted by the implementer which introduces change to the scope or what features are deployed, especially after the first deployment.
- Introduce test environments and UAT to validate the requirements have been met.
- Measure the time it takes to deploy your solution in a single location, then estimate the total time for the number of times you would repeat the same steps.
- Outage, will the solution be disruptive to staff or users, is out of hours deployment required?

### Manual

If you prefer manual, there are some ways to reduce time to manually deploy your solution. Such as:

- Choose the centralisation approach, as mentioned above, is there a way to setup your solution to be deployed from one location.
- Know your URLs, such as _layout/15/XX links to settings, site contents, for manual deployments aim to jump directly to the page where the setting occurs, avoid navigating through SharePoint, extra clicks will slow you down.
- Keep a log of your progress, so for very large implementations, you can pause and come back, refer to a list of how much of the deployment you have done - this can also serve as your checklist if you have a multi-step deployment.

### Script

For scripting, I highly recommend looking into PnP PowerShell library, there a lot of cmdlets design to work online and on-premises, there is plenty of blogs, examples or community members that can help you to get you started.

Please refer to this article for more detail [Benefits of using PowerShell with SharePoint](benefits-of-using-powershell-with-sharepoint.md)

### Site Designs

Now there is Site Designs feature in SharePoint Online, which opens up a new way to deploy features.  These can create libraries, set permissions, branding and headings in Modern interfaces and call Flows containing more advanced scenarios.

## Further Reading

Many related articles are in the works to go into each section in more detail. Watch here for updates.

---

**Principal author**: [Paul Bullock](https://www.linkedin.com/in/pkbullock)
