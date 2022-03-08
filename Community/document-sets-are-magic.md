---
title: Document Sets for Fast Legacy Process Automation
ms.date: 11/21/2020
author: PatD
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: sharepoint-online
localization_priority:
description: A proven strategy for content classification in SharePoint libraries with the magic of no-code all-configuration content Document Sets.
ms.collection: M365Community
---

# Document Sets for Fast Legacy Process Automation

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

_Before you run, you should walk_

## Overview [tl;dr]

- Users use documents. Now, and forever.
- If there's one document, there are probably related documents.
- Users are too busy to apply your *beautiful* metadata scheme manually.
- Users benefit from good metadata and organization.
- Users blame *you*, the site owner, when they can't find a document.
- SharePoint Libraries have had an amazing tool to help your users classify, organize, and find documents - this whole time - called **Document Sets**.

You may be a site owner in a document-centric organization (Gov, Finance, Education). Your leadership craves the benefits of modernization, automation and process improvement. While the Microsoft 365 and SharePoint Online platform provide a wide array of solutions, a good first step low-overhead no-code option you should consider is the SharePoint *Document Sets*. The Document Set has been a part of SharePoint for years, both on premise (2007-2019) and Online.

The Document Set offers these great benefits:

- All the familiarity of putting related documents into a folder, while maintaining valuable SharePoint metadata capability
- For the non-technical user, it reduces the cognitive load of assigning complex metadata to documents
- For the power user, it allows for assigning complex metadata to documents, creating metadata driven views, and executing workflows on a bunch of files at once.

> **Build a bridge**:
> You, the site owner, live your life in views, Flows, metadata, lookup columns, and are always learning for new automation features. Your coworkers may not be. They may be working in legacy back office processing functions, handing paper or PDF documents. The Document Set is the bridge for them – it shows them the _possibilities_ and capabilities of SharePoint without a huge learning curve.

### Example _Document Set_ Use Case

The Contoso Insurance Agency has a legacy process where, for each new claim that&#39;s filed, several documents must be created, updated, and managed for auditing proposes. Contoso Insurance employees are new to process automation and have only recently began storing Word, PDF, and Excel documents in a SharePoint Library.

Multiple naming schemes have been tried but keeping the required 5-10 per-claim documents together has been a challenge. Their SharePoint Library now has 10,000 documents. Metadata columns were added, but staff grumbled at having to pick the same fields over and over for each document.

SharePoint Search is powerful but doesn't necessarily show related documents together the way your users want.

To turn this around, the Site Owner performed some old-fashioned process analysis of the work, identified a few helpful metadata columns (*Date of Claim* and *High Risk Customer*) and began the process of upgrading their library to support SharePoint Document Sets.

## What Document Sets Are _Not_

Document Sets **are not folders** (though they inherit from the Folder Content Type). They have icons that look like folders. They sure smell like folders – a container that holds files – but Document Sets are significantly more powerful.

> **Don't Folder where you Set**
> You _can_ have folders outside or inside a Document Set – but it is not a great user experience and can negate the clarity that Document Sets bring to a library. Best practice is to avoid mixing folders and Document Sets.

## What Document Sets Are

Document Sets are a _Content Type_, and you should read [What Is a Content Type?](/microsoft-365/community/what-is-content-type) to understand Content Types if you don't already. Content Types have metadata, inheritance, and can be set to show up in the [+New] menus within SharePoint and Teams tabs.

What's fundamentally different about the Document Set Content Type is that you can put another file inside the Document Set. The user experience is very similar to a folder (but it is certainly not a folder). Your user can easily make a new Document Set and drag and drop documents into it. They'll get it on the first try, just like they with folders.

The key advantage over a standard folder is inherited metadata. When you create a new Document Set, you **add metadata to the Set that is automatically passed down to the documents within**. And you can control which metadata is at the Set level, and what's shared with the individual document. This is the magic – it's free metadata, and free document organization. No code, light configuration.

> **The more you know**
> Read Microsoft's [Introductory Document Set documentation](https://support.microsoft.com/office/introduction-to-document-sets-3dbcd93e-0bed-46b7-b1ba-b31de2bcd234)

## Additional Benefits

With a Document Set enabled SharePoint library, it is still at the end of the day a SharePoint Library. Without any code, you still have Email notifications, Microsoft Power Automate Flow, custom Views, drag-n-drop files, web parts, sharing links, Content Types, bulk download, bulk property edits, filtering, versioning, and more.

You sacrifice nothing by enabling Document Sets and gain the advantage of a library with users who can find their stuff and get, maybe, a little more excited about the Microsoft 365 / SharePoint tool that IT has cast upon them.

## How to enable Document Sets

In your library settings, under advanced settings allow custom Content Types and then add the Document Set Content Type. It'll then show up on the [+New] menu in that library.

## Do Document Sets work in SharePoint Online?

They are great in SharePoint Online, with one caveat. Document Sets in SharePoint Online will occasionally drop into a *Classic* look and feel before returning to Modern. This occurs when you create a new Set. Everything else follows the new Modern UI standard. In this author's daily observed use, your users won't flinch at this.

## Can I use Document Sets in Teams?

Yes, with a similar caveat. Document Sets are available in the [+New] menu in the _Files_ tab of your Team. Working with the individual files within the Document Set works well in Teams. As of this article creation date (November 2020), creation of a new Document Set from Teams sends the user to their web browser and keeps them there.

> **Teams Tip**
It may be better to use the _Website_ tab in Teams for Document Set use. That will keep the work contained in a single Teams tab.

## Use case example: Configuration of a Document Set enabled Library

In the use case above, this was how Contoso Insurance set up their Document Set solution. No code was written, everything was configured by the site owner:
  
1. A new SharePoint Library called "Claims Auditing" created.
2. Major Versioning enabled. Minor versioning disabled. Check In/Out disabled. _New Folders_ disabled.
3. Library configured to support Content Types in Library Settings, under Advanced Settings
4. In the site collection Site Settings, the _Document Set_ feature was enabled.
5. The _Document Set_ Content Type was added to the new _Claims Auditing_ library, under Library Settings

    > So far so good. At this point, we've got a SharePoint Library with Document Sets, but we don't have the real value of it yet. Keep reading:

6. Add two new columns to the library, _Date of Claim_ (a date column) and _High-Risk Customer_ (a Y/N choice column). Set the _Date of Claim_ column to default to today's date, and _High-Risk Customer_ to default to _No._

    > At this stage, these 2 new columns are available in both the Document Set and the documents uploaded in the Sets.

7. Add another column called _Assigned Reviewer_ (person column) to the library.
8. In the Library Settings, under Content Type, choose 'Document Set', and then _Document Set Settings._ From here, under Shared Columns, check _Date of Claim_ and _High-Risk Customer._ But **not** _Assigned Reviewer._

If you've followed these steps, you now have a document library where a user can create a new Document Set for each claim. The _Date of Claim_ value is pre-populated with today's date and _High-Risk Customer_ is defaulted to *No*. Every document that is dragged-and-dropped into this Set will inherit those values! And, if you change the value in the Document Set, the documents in it will automatically update with those new values!

Since each document (within the Document Set) has a different person reviewing it, each document can have its own _Assigned Reviewer_ associated with it – because we didn't make it a _Shared_ in the Document Set settings.

## Epilogue

End users of the library rejoice – they're given a library that *appears* organized by folders (but of course, it's not a folder) and they can sort/filter by _Date of Claim_ and _High-Risk Customer_ at the Set level. They can create Views based on a date range or status. The default view went from 8000 individual documents to a thousand Document Sets.

Site Owners were took the silent satisfaction of watching the library thrive over the years, with users rising to become power users.

Document Sets enable easy out-of-the-box file organization and automatic classification using the tool you already own. SharePoint Document Sets are magic. 🗂

## Further Reading
  
- Microsoft: [Intro to Document Sets](https://support.microsoft.com/office/introduction-to-document-sets-3dbcd93e-0bed-46b7-b1ba-b31de2bcd234)
- Microsoft: [Create and Manage Document Sets](https://support.microsoft.com/office/create-and-manage-document-sets-c71d5796-d559-48de-b1b3-42383bdd13ea)
- Blog: SharePoint Maven: [Document sets – the hidden gem of SharePoint](https://sharepointmaven.com/document-sets-hidden-gem-sharepoint/)
- Blog: Marc Anderson: [A love for SharePoint Document Sets](https://sympmarc.com/2017/07/12/wherein-in-profess-my-love-for-document-sets-my-hatred-of-the-5000-item-limit-and-some-tips/)
- Blog: Ben Prins [Power Automate Flow and Document Sets](https://www.benprins.net/2020/07/10/power-automate-creating-and-updating-a-document-set-in-sharepoint/)
- Microsoft PnP: [Adding a Document Set with PnP](https://pnp.github.io/powershell/cmdlets/Add-PnPDocumentSet.html)

---

**Principal author**: [Patrick M. Doran](https://www.linkedin.com/in/PatrickDoran)

---
