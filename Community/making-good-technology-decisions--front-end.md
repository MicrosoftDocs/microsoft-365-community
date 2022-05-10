---
title: "Making Good Technology Decisions: Front End"
ms.date: 3/29/2021
author: sympmarc
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: microsoft-365
localization_priority: 
description: "Making Good Technology Decisions: Front End"
ms.collection: M365Community
---

# Making Good Technology Decisions: Front End

* Part 1: [Microsoft 365 - Making Good Technology Decisions: Establishing Decision Criteria](making-good-technology-decisions--establishing-decision-criteria.md)
* Part 2: [Microsoft 365 - Making Good Technology Decisions: Data Storage](making-good-technology-decisions--data-storage.md)
* Part 3: Microsoft 365 - Making Good Technology Decisions: Front End (this article)

[!INCLUDE [cc-data-platform-banner](includes/cc-data-platform-banner.md)]

In the prior two articles in this series, I’ve gone over how to evaluate your organizational readiness and what criteria to use to make decisions [Decision Criteria] as well as where to store the underlying data for your solution [Data Storage]. In this installment, I will go through some of the front-end options available to you, providing some of the plusses and minuses for each.

## SharePoint List Forms

SharePoint list forms often are pooh-poohed even by the people who use them. The best thing about them is that when we set up a list, we get those forms for “free”. The forms will ensure that you are entering the right data types and handle all the CRUD operations. The forms are even Content Type aware (and I am a big Content Type fan!); if you change the Content Type, the forms automagically adjust to reflect the appropriate metadata. If you have a list which stands alone with relatively straightforward input needs, the out of the box forms are probably all you will ever need.

A shortcoming of these forms in modern SharePoint is that you cannot build conditional logic between any two or more columns as things currently stand. We used to add JavaScript and CSS to the out of the box forms in classic SharePoint (huzzah, SPServices?), but this is not possible in modern SharePoint. If you are still in classic and you are customizing forms with JavaScript and CSS, read on…

## Customized List Forms with Power Apps (Canvas Apps)

Power Apps canvas apps are a way to customize the forms in a list context even if it is just a simple conditional display of a column or a cascading dropdown. The general approach here is to build out the list architecture first, and then customize the forms with a canvas app. There is much confusion about the licensing implications of using canvas apps, but all Microsoft 365 licenses include usage of the Power Platform for the purpose of customizing and extending Microsoft 365 applications; this means canvas apps for list forms does not require any additional licensing.

Embedding a canvas app in the context of a single list does not limit us to interacting with only that single list. For example, if we have a parent/child relationship between two lists, the canvas app embedded in the parent list can also interact with the child list. At this point, your canvas app can start to feel more like a small application.

Power Apps are billed as end user tools, but still require the right mindset to build something with any complexity and be successful. Much like InfoPath before them, canvas apps provide supposedly “low code” capabilities, but that only holds true if the form is relatively straightforward.

## Standalone Power Apps (Canvas Apps)

Embedding canvas apps in the context of a single list is often just the ticket, but in other cases, you want an app which stands separate from the data storage mechanisms. Standalone canvas apps are one way to do this. Contrary to what I believed for quite some time; this also falls under your Microsoft 365 licensing.

With a standalone canvas app, you might have two or more underlying SharePoint lists for data storage, or even Dataverse or some other storage mechanisms. By moving to this level of abstraction, your end users really do not know where the data lives, nor do they need to. The data is somewhere, and the app you build provides the ways to interact with it and perhaps the entirety of the ways to review and report on it.

Using canvas apps this way, you can use the Microsoft Power Apps (Preview) Web Part to embed the app right in any SharePoint page (where there is ample page real estate for it realistically to live). Alternatively, you can send your users via a link (perhaps a Quick Link) to the Power Apps environment where your app is hosted. Again, they do not need to know where the app lives, just how to get to it.

## Power Apps (Model Driven)

If you have decided to use Dataverse for your data storage, you can choose to use canvas apps (via a premium connector, thus with a licensing cost) or model driven apps. To say that Power Apps have two flavors (canvas apps and model driven apps) is rather disingenuous. The two types of Power Apps could not be more different to build or to use. Because both tool sets were built by the Dynamics 365 folks, they are under the same marketing name, but the skills to build with them are quite different.

Model driven apps provide a very different way to think about app building. With model driven apps, the data structures – entities in Dataverse, primarily – determine most of the possibilities for the front end. This is not a bad thing, but it can feel stranger than canvas driven apps, where it feels more comfortable taking an iterative app building approach. Note that my prior article was about data storage: I’ve found over the years that getting your data model right up front (the 80/20 rule applies) makes building solutions on top of it much easier, anyway. Model driven apps take that a step further, requiring the data model first. Iteration is possible, but the further down the path you go, the harder it is to change your data model.

## SharePoint Framework (SPFx) Solution

Coder’s gotta code, right? Well, in some cases, coding is just the right answer. When we need unique functionality and we have the skills and resources to support it, creating custom SPFx solution can be a great idea. Whichever data storage solutions we have chosen – even if we need to utilize external data sources – as long as that data is offered up via some sort of modern Web interface (most often REST), we can incorporate it into an SPFx solution.

SPFx solutions allow us to add functionality to SharePoint and Microsoft Teams (so far). In SharePoint, we can create Web Parts or Extensions. Extensions include (with simplified explanations):

* Application Customizers – think header and footer replacements with dynamic logic
* Field customizers – think customized list views
* Command Sets – think buttons in toolbars

In many cases, these SPFx entry points allow you to provide consistent and powerful capabilities in single pages or across pages in a tenant.

## SharePoint Framework (SPFx) Single Page App Parts

The last specific option I will outline here is an SPFx Single Page App Part. This way of creating a solution is different almost purely because it allows us to take over a full page (mostly) much like we would with a single page app (SPA). (I have had some vigorous debates with some people about what a SPA really is. To me, it just means an app that uses most of the page and does not interact with any chrome around it. Some will disagree.) This type of SPFx solution also reduces the surface area where the user might interact with its settings or placement. This means it is not a capability a user adds to a page, it is a capability developer deploys to the user base as a page. (In a sense, this is like a standalone Power App.)

## Everything Else!

Of course, there will always be enterprises which decide some other front-end building tool is the cat’s meow and thus should take the place of all the above. Microsoft 365 is generally a modern Web environment and many services offer up well-documented APIs which this crowd can use. To me, this is often folly as trying to get two different technologies to work together can become a war of vendors, but it is certainly possible, and lots of people find great success here. As for me, I prefer to stick with the Microsoft 365 ecosystem.

## Summary

We have a plethora of options for our front ends. But do not think you need to pursue only one of these options. Different types of solutions lend themselves to different front-end building tools. A departmental solution might be perfectly built with canvas apps where an enterprise-wide solution may make more sense with model driven apps – or vice versa. If you have thought through your decision criteria and data storage for the solution, in many cases the front-end tool set will logically be obvious.

To some degree, this series of articles has given you a laundry list of options you might choose as you are making your architectural decisions. Understanding each option more fully is important for you to make good decisions. Unfortunately, there are different worlds across the ecosystem that do not often intersect, whether it is the people or the technologies. By trying to think about the various options on the spectrum, we can better serve our constituents by making better informed architecture decisions for our solutions.

---

Principal author: [Marc D Anderson, MVP](https://www.linkedin.com/in/marcanderson)

This article was originally published as a part of the "Microsoft 365 - Making Good Technology Decisions" series, written by Microsoft MVP Marc D. Anderson for [CollabMagazine](https://www.collabmagazine.com/).

---
