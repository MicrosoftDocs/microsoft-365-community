---
title: Living Large with Large Lists and Large Libraries
ms.date: 7/16/2020
author: PatD
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: sharepoint-online
localization_priority:
description: Best practices and strategies for building and operating large SharePoint Lists and Libraries well above the 5000 item threshold.
ms.collection: M365Community
---

# Living Large with Large Lists and Large Libraries

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

Best practices and strategies for building and operating large SharePoint Lists and Libraries well above the item limit threshold.

## Summary

- List or Library above 5000 items is indeed possible with planning and some filtering/sorting compromises.
- If you can make it modern, you should. The modern experience improves over time; classic does not.
- Apply remedies *before* you hit 5000 items, though in some cases, you can make it to 20000. Procrastination will hurt you!
- **Your users don't care about this limitation one bit.**  Word doesn't limit you to 500 words. Excel doesn't limit you to 50 columns. As site owner, you need to be on top of this.
- If your List or Library is at 3500 items, fair chance it'll hit 5001 when you're on vacation.
  
## SharePoint Myths

There are couple of myths floating around in the world of SharePoint Lists and Libraries. One is that you shouldn't treat a List like a database (untrue - it is just fine for a power user to create a database). The other is that Lists and Libraries with more than 5000 items just won't work. Both of these are false. Here is guidance on how to own and operate a list or library from 5001 - 30 million items.

> **A Cautionary Tale:**
> As site owner, your end-users and power-users **will** hit this wall without careful planning and some monitoring. To them, the List/Library will appear broken and will reflect badly on you and the tool. They'll be given almost no warning that they're exceeding the threshold.

## What is the List View Threshold?

When the number of items or documents is so high that SharePoint displays an error instead of the content. For many years this was *5000*.

Behind the scenes. SharePoint is querying data from a database.  It, like all systems, can do but so much at a time, and the *Item Limit Threshold* is that limit of items that are displayed in a given view.  

If you've operated sites with SharePoint Lists or Libraries for any amount of time, you or one of your customers will trigger the Item Limit Threshold in a List or Library. Either they've published a 300,000 row Excel spreadsheet as a new List, or they decided Friday afternoon right-before-quitting-time is the perfect time to upload the entire network drive's contents to a single Library. Views break. Sorting and filtering (especially on-premises) fall apart. Users report *broken* sites and missing data.  

> **The Limit is only the View**
> As a Site Owner, keep in mind that when the threshold is exceeded, it's a problem with presenting the *View* and not the List/Library contents. All the data is still there, it just can't be displayed. Mentally, separate the (Items, Documents) from the presentation (Views) to help you pick the best solution.

It's easy to check the number of items or documents in a List or Library.  Either look in *Site Contents*, or look in the List/Library Settings.  A blue bar will appear there if the List/Library is getting close to the limit. 

## How can I predict which Libraries and Lists will exceed the threshold?

With experience, you'll be able to smell a List that'll grow to exceed the limit before the List is even created. This prediction experience comes from knowing your customers and their business processes. Generally, these are the smells for future threshold-busting Lists and Libraries:

- If the List or Library is considered to be an automation of a manual process, there's a good chance in time it'll go over the limit. Especially if the process has been in place for years when you bring it in to SharePoint. Always consider the lifecycle of the list or library.
- If it's a network-drive-to-SharePoint migration scenario, there's a good chance it'll go over the limit (but folders may make this a non-issue).
- If you're in a meeting and the customer says "*I have this Access database and...*"
- If the List is tied to a Flow, Workflow, or Timer Job - any scenario where the list is not updated by humans.  

> **Monitoring tools**
Your workplace may have some sort of fancy third-party monitoring tools to report on item/document totals.  If you're not so lucky, you as a Site Owner can set weekly Email Alert Notifications on the List/Library to keep an eye on things.  It's not true reporting, but you'll be able to see trends in Lists.

## Differences in the threshold between Modern versus Classic Lists/Libraries

They are different. Let's compare:

|Platform| Threshold | Can I change threshold? | Automatic Indexing | Modern Experience | Threshold-free Hours
|--|--|--| --| --| --|
| Online |  5000 | No | Yes | Default | No
| On Prem SE   | 5000 | Yes* | Yes | Available | Available**
| On Prem 2019 | 5000 | Yes* | Yes | Available | Available**
| On Prem 2016 | 5000 | Yes* | Yes | No | Available**
| On Prem 2013 | 5000 | Yes* | No | No | No

\* *Someone with Central Admin access is needed to change this. And when you ask them to, you'll be given reasons why it's a bad idea.  That's their role - keep the databases performing well and sites up and running.  The smart play is to ask them to increase the limit for a very short amount time so you can fix your List/Library, and then return to the default threshold limit. Lists and Libraries can also have the limit disabled via PowerShell by setting the _EnableThrottling_ property to false. See the example below*.

 \** *Your admins can schedule a time when the threshold is lifted on a schedule- generally after hours.  Doing this during business hours will frustrate your users by created a mixed experience.*

```powershell
$web = Get-SPWeb https://sharepoint.contoso.com/sites/team
$list = $web.Lists["Example List"] #or library display name
$list.EnableThrottling = $false
$list.Update()
```

The most fundamental difference is that Modern will, over time, get new feature improvements to improve the experience of over-threshold Lists/Libraries.  Classic will stay the same.
  
## Should I build this probably-large List/Library into multiple Lists/Libraries?

You can, and that's an option to consider, especially if you can work in Content Types and Site Columns for data consistency.

>**Lookup Columns and Calculated Columns**
>If your List or Library has Calculated columns (which can't be indexed) or Lookup Columns, you may want to consider the multiple List/Library route.  A List will struggle to reference a data in a Lookup column when the number of rows is over the threshold.

If it's a Document Library, consider using the [SharePoint Content Organizer](https://support.office.com/article/Configure-the-Content-Organizer-to-route-documents-B0875658-69BC-4F48-ADDB-E3C5F01F2D9A) to route your documents (based on a condition) to different libraries with the same metadata.

But is that what your customers *want* from a user experience perspective? Does it feel similar to having to update multiple spreadsheets? What if they want to do reporting on this data, and they have to deal with multiple Lists?  This scenario shouldn't be your first choice if you can avoid it.

## Can Search Help me?

Depending on your scenario, absolutely. Search doesn't care about the List View Item Threshold. If you're building a large Library or List and don't need custom views or complex filtering/sorting  - Search can be used to give your users access to the items/documents they need.

> **Search-Only Example:**
> The article author currently manages a folderless SharePoint Library with 450,000 PDF files in it. Those files are uploaded to the library through an external process. Each file has a meaningful file name, and the customer uses Search to find just the document they need instantly. They'll never sort or filter the library, or edit the documents, so this scenario works just fine. No columns are indexed. 

## Can Grouped-By Filtered Views help me here?

This one gets complex real fast - especially with views for Document Libraries with folders. Read Joanne Klein's excellent [deep-dive](https://joannecklein.com/2017/07/25/sharepoint-online-list-view-threshold/) into this for more information.
  
## All my internet research keeps pointing to Indexed Columns - what's that all about?

Indexing columns - *before the threshold limit is broken* - is the most effective way to mitigate View threshold pain. In an ideal situation, where the user knows the List or Library will be large, you'd index any and all columns you can.

A View that's over the threshold will generally only display if it's filtered by an indexed column *first* in the view, and that filter returns no more than 5000 unique values.

This is done by going to the List or Library settings, choosing the Indexed Columns link, and indexing the columns one by one. You can add up to 20 indexes to a list or library. Choose wisely - what columns would you or your users want to base a view on?

> **Automatic Indexing:**
> SharePoint lists/libraries in SharePoint Online now have the capability to index columns automatically. But like all automated processes, it may not index the *right* column for your users, and will not automatically create indexes for lists/libraries with more than 20,000 items. Don't count on this to save you. Plan ahead.

It's important to take this action early - SharePoint on-premises (2013) won't let you create an Index past 5000 items. It is uncertain if there is a hard limit in SharePoint Online, but once you cross those lines, it is difficult to correct. You have to delete lists items to get back down below the limit, and then index the columns. 

For the best user experience you should be proactively ensuring the appropriate columns for your lists/libraries are indexed, based on the columns used most frequently in views and/or filtered by your users. You can add indexes on up to 20 columns on a list or library.

### Column types that can be Indexed

- Single line of text
- Choice (single value)
- Number
- Currency
- Date and Time
- Yes/No
- Lookup (Lookup)
- Person or Group (single value) (Lookup)
- Managed Metadata (Lookup)

### Column types that cannot be Indexed

- Multiple lines of text
- Choice (multi-valued)
- Calculated
- Hyperlink or Picture
- Custom Columns
- Person or Group (multi-valued) (Lookup)
- External data
  
## But *why* are we indexing columns?

We index columns because those indexed columns can then be used to define Views that *do work* in Lists/Libraries above the threshold.

In fact, if the columns displayed in your List/Library View are *all* indexed columns, the View will function almost like a regular list/library view.

### Indexed columns pair well with a Filtered View

Your default view in this large List or Library should ideally be composed of only Indexed columns.  If not, it should be filtered first by an Indexed column.  

> **Pro Indexing Tip**
> If you can, always index by Title, Modified, Created, Modified By, and Created By columns.  You can piece together a viable view with this, and so can your users.

### Example Scenario 1: Indexing  for a Simple list

*Sorted by Created, Descending. Batches of 100.*

| Column | Type | Indexed | In Default View
|--|--|--|--|
| Title | Single Line | Yes| Yes |
| Favorite Sport | Choice (single) | Yes | Yes |
| Likes Cats | Yes/No | Yes | Yes |
| Biography | Multiline | No, can't | No |
| Created | Date | Yes | Yes |
| Created By | Person | Yes | Yes |

In this scenario, we've created a SharePoint List or Library that will work right to 30 million items.  Default view is bullet-proof in Classic or Modern. 

- Your users can create Personal Views that show just their Created By
   entries.  Business analysts can create reports based on *Likes Cats*
   preference.  
- The *Biography* column - best case - isn't displayed in any views.  Only viewed/edited when the user interacts with the item.
- It may be worth also indexing *Modified* here for **Power Automate Flow** users running the trigger for when SharePoint Items are Created or Modified.

### Example 2: Indexing Scenario for a Large Library

*Sorted by Created, Descending. Batches of 100.*
This library has 25,000 documents in it.  Each day a **folder** is created and seven regional sales reports are added to it.   The business has solemnly-sworn to follow this model.

| Column | Type | Index it?
|--|--|--|
| Title | Single Line | Yes|
| Name | File Name | No |
| Sales Region  | Choice (single) | Yes |
| Likes Dogs | Yes/No | Yes |
| Created | Date | Yes
| Created By | Person | Yes

The model will work great for years.  Each folder acts as sort of a reset on the Item Limit Threshold for the default view. New folderless flat-Views can easily be created using the columns you've indexed.

> **Folders, Document Sets**
>Remember, folders count as items when calculating the threshold.

### Further Reading

- Microsoft: [Adding an index to a SharePoint column](https://support.microsoft.com/office/add-an-index-to-a-sharepoint-column-f3f00554-b7dc-44d1-a2ed-d477eac463b0)
- Microsoft: [Manage large lists and libraries in SharePoint](https://support.office.com/article/manage-large-lists-and-libraries-in-sharepoint-b8588dae-9387-48c2-9248-c24122f07c59)
- Blog: [SharePoint Online List View Threshold](https://joannecklein.com/2017/07/25/sharepoint-online-list-view-threshold/)
- Blog: [Deleting a Very Large SharePoint List](https://sympmarc.com/2017/03/27/deleting-a-very-large-sharepoint-list/)
- Blog: [Predictive Indexing Comes to SharePoint](https://sympmarc.com/2017/11/08/predictive-indexing-comes-to-office-365-lists-and-libraries/)  
  
---

**Principal author**: [Patrick M. Doran](https://www.linkedin.com/in/PatrickDoran)

---
