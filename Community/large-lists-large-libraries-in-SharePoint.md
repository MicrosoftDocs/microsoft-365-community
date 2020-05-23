---

title: Living Large with Large Lists and Libraries

ms.date: 5/21/2020

author: PatD

ms.reviewer: jhendr

localization_priority:

description: Best practices and strategies for building and operating large SharePoint Lists and Libraries well above the 5000 item threshold.

ms.collection: SPCommunity

---

  

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

  

# Living Large with Large Lists and Libraries

  

## Best practices and strategies for building and operating large SharePoint Lists and Libraries well above the 5000 item threshold.

  

### SharePoint Myths
There are couple of myths floating around in the world of SharePoint/Microsoft 365 Lists and Libraries. One is that you shouldn't treat a List like a database (untrue - it is just fine for a power user to create a database). The other is that Lists and Libraries with more than 5000 items just won't work. Both of these are false. Here is guidance on how to own and operate a list or library from 5001 - 30 million items.

  

>  **A Cautionary Tale:**
> As site owner, your end-users and power-users **will** hit this wall without careful monitoring. To them, the List/Library will appear broken and will reflect badly on you and the tool. They'll be given almost no warning that they're exceeding the threshold.

  

## The View Item Limit Threshold
If you've operated sites with SharePoint Lists or Libaries for any amount of time, you or one of your customers will trigger the Item Limit Threshold in a List or Library. Either they've published a 300,000 row Excel spreadsheet as a new List, or they decided Friday afternoon at 4pm is the right time to upload the entire network drive's contents to a single Library. Views break. Sorting and filtering (especially in on-premise) fall apart.

  

>  **The Limit is only the View**
> As a Site Owner, it's best to keep in mind that when the threshold is exceeded, it's a problem with the *View* and not the List/Library itself. All the data is still there, it just can't be displayed.  Mentally, separate the data (Items, Documents) from the presentation (Views).

  

### Predicting Libraries and Lists that will exceed the threshold

With experience, you'll be able to smell a list that'll grow to exceed the limit before the List is even created. This prediction experience comes from knowing your customers and their business processes. Generally, these are smells for future big Lists and Libraries:

* If the list or library is considered to be an automation of a manual process, there's a good chance in time it'll go over the limit. Especially if the process has been in place for years when you bring it in to SharePoint.

* If its a network-drive-to-SharePoint migration scenario, there's a good chance it'll go over the limit (but folders may make this a non-issue).

* If you're in a meeting and the customer says "*I have this Access database and...*"

* If the List is tied to a Flow, Workflow, or Timer Job - any scenario where the list is not updated by humans.

  
  

## Can I break this list/library into multiple lists/libraries?
You can, and that's an option to consider, especially if you can mix in Content Types and Site Columns for consistency. But is that what your customers want from a user experience perspective? Does it feel like having to update multiple spreadsheets? What if they want to do reporting on this data, and they have to deal with multiple Lists?

  

## Can SharePoint Search Help me?

Depending on your scenario, absolutely. SharePoint Search doesn't care about the Item Limit Threshold. If you're building a large flat Library with no folders and no metadata - and never need to sort/filter the documents in that library - SharePoint Search can still find and retreive those documents.

  

>  **Search-Only Example:**
> The article author currenty manages a folderless SharePoint Library with 450,000 PDF files in it. Those files are uploaded to the library through an external process. Each file has a meaningful file name, and the customer uses SharePoint Search to find just the document they need instantly. They'll never sort or filter the library, or edit the documents, so this scenario works just fine. No columns are indexed.

  
  
  

## An ounce of prevention - Indexed columns
Indexing columns - before the threshold limit is broken - is the most effective way to mitigate View pain. In an ideal situation, where the user knows the List or Library will be large, you'd index any and all columns you can. This is done by going to the List or Library settings, and indexing the columns one by one. You can add up to 20 indexes to a list or library. Choose wisely - what columns would you want to base a view on?

  
>  **Automatic Indexing:**
> SharePoint lists/libraries now have the capability to index columns automatically. But like all automated processes, it may not index the *right* column for your users.  Don't count on this to save you.

 
It's important to take this action early - SharePoint on premise (2013) won't let you create an Index past 5000 items, and SharePoint Online won't let you create on past 20,000 items. Once you cross those lines, it is difficult to correct. You have to delete lists items to get back down below the limit, and then index the columns.

  

### Supported Column Types
* Single line of text
* Choice (single value)
* Number
* Currency
* Date and Time
* Yes/No
* Lookup (Lookup)
* Person or Group (single value) (Lookup)
* Managed Metadata (Lookup)

  
  
  

## But *why* are we Indexing columns?
We index columns because those indexed columns can then be used to define Views that *do work* in Lists/Libraries above the threshold.

In fact, if the columns displayed in your List/Library View are all indexed columns, the View will function almost like a regular list/library view.



  
  
  
  
  
  

### Further Reading

  

* Microsoft: [Adding an index to a SharePoint column](https://support.microsoft.com/en-us/office/add-an-index-to-a-sharepoint-column-f3f00554-b7dc-44d1-a2ed-d477eac463b0)

* Microsoft: [Manage large lists and libraries in SharePoint](https://support.office.com/en-us/article/manage-large-lists-and-libraries-in-sharepoint-b8588dae-9387-48c2-9248-c24122f07c59)

* Blog: [Deleting a Very Large SharePoint List](https://sympmarc.com/2017/03/27/deleting-a-very-large-sharepoint-list/)

* Blog: [ShareGate: SharePoint Version Control to the Rescue](https://sharegate.com/blog/sharepoint-version-control)

  
  
  

---

  

**Principal author**: [Patrick M. Doran](http://www.linkedin.com/in/PatrickDoran)

  

---