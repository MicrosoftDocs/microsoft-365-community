
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

  

  

# Living Large with Large Lists and Large Libraries

## Best practices and strategies for building and operating large SharePoint Lists and Libraries well above the item limit threshold.


#### tl;dr

 - Above 5000 is possible with planning and some feature restrictions.
 - If you can make it Modern, you should.
 - Apply remedies *way before* 5000 items.
 - The best-case architecture of any SharePoint List or Library is to keep it under 5000 items.  **Your users don't care about this one bit.**  Word doesn't limit you to 500 words. Excel doesn't limit you to 50 columns. As site owner, you need to be on top of this.   
 - If your List or Library is at 3500 items, fair chance it'll hit 5001 when you're on vacation.
  
### SharePoint Myths
There are couple of myths floating around in the world of SharePoint/Microsoft 365 Lists and Libraries. One is that you shouldn't treat a List like a database (untrue - it is just fine for a power user to create a database). The other is that Lists and Libraries with more than 5000 items just won't work. Both of these are false. Here is guidance on how to own and operate a list or library from 5001 - 30 million items.

  

  

>  **A Cautionary Tale:**
> As site owner, your end-users and power-users **will** hit this wall without careful planning and some monitoring. To them, the List/Library will appear broken and will reflect badly on you and the tool. They'll be given almost no warning that they're exceeding the threshold.

  

  

## What is the View Item Limit Threshold?

If you've operated sites with SharePoint Lists or Libraries for any amount of time, you or one of your customers will trigger the Item Limit Threshold in a List or Library. Either they've published a 300,000 row Excel spreadsheet as a new List, or they decided Friday afternoon at right-before-quitting-time is the right time to upload the entire network drive's contents to a single Library. Views break. Sorting and filtering (especially in on-premise) fall apart. Users report broken sites and missing data.  



>  **The Limit is only the View**
> As a Site Owner, it's best to keep in mind that when the threshold is exceeded, it's a problem with presenting the *View* and not the List/Library contents. All the data is still there, it just can't be displayed. Mentally, separate the (Items, Documents) from the presentation (Views) to help you pick the best solution.

  

  

## How can I predict which Libraries and Lists will exceed the threshold?

  

With experience, you'll be able to smell a list that'll grow to exceed the limit before the List is even created. This prediction experience comes from knowing your customers and their business processes. Generally, these are smells for future threshold-busting Lists and Libraries:

  

* If the list or library is considered to be an automation of a manual process, there's a good chance in time it'll go over the limit. Especially if the process has been in place for years when you bring it in to SharePoint.

  

* If its a network-drive-to-SharePoint migration scenario, there's a good chance it'll go over the limit (but folders may make this a non-issue).

  

* If you're in a meeting and the customer says "*I have this Access database and...*"

  

* If the List is tied to a Flow, Workflow, or Timer Job - any scenario where the list is not updated by humans.

  

## Are things different with Modern versus Classic Lists/Libraries?
They are.  Let's compare:

|Platform| Threshold | Can I change threshold? | Automatic Indexing | Modern Experience | Threshold-free Hours
|--|--|--| --| --| --|
| Online |  5000 | No | Yes | Default | No
| On Prem 2013 | 5000 | Yes* | No | No | No
| On Prem 2016 | 5000 | Yes* | Yes | No | Available**
| On Prem 2019 | 5000 | Yes* | Yes | Available | Available**

\* *Someone with Central Admin access is needed to change this. And when you ask them to, you'll be given reasons why it's a bad idea.  That's their role - keep the databases performant and sites up and running. 
 \** *Your admins can schedule a time when the threshold is lifted - generally after hours.  Doing this during business hours will frustrate your users by created a mixed experience.* 


  

## Should I build this probably-large List/Library into multiple Lists/Libraries?

You can, and that's an option to consider, especially if you can mix in Content Types and Site Columns for data consistency. 

But is that what your customers *want* from a user experience perspective? Does it feel like having to update multiple spreadsheets? What if they want to do reporting on this data, and they have to deal with multiple Lists?
> **Spoiler**
>  When you implement this multiple-list-same-columns solution, one of your users will absolutely break the threshold in one of the lists.  So then you'll have to break that list into two more.  And so on. 
  

  

## Can SharePoint Search Help me?

  

Depending on your scenario, absolutely. SharePoint Search doesn't care about the Item Limit Threshold. If you're building a large Library or List and don't need custom views or complex filtering/sorting  - SharePoint Search can be used to give your users access to the items/documents they need.

  

  

>  **Search-Only Example:**
> The article author currently manages a folderless SharePoint Library with 450,000 PDF files in it. Those files are uploaded to the library through an external process. Each file has a meaningful file name, and the customer uses SharePoint Search to find just the document they need instantly. They'll never sort or filter the library, or edit the documents, so this scenario works just fine. No columns are indexed.

## Can Grouped-By Filtered Views help me here?
Not in a consistently helpful way.  There are too many variables here to make a solid recommendation either way.  Read Joanne Klein's excellent [deep-dive](https://joannecklein.com/2017/07/25/sharepoint-online-list-view-threshold/) into this for more information.
  

  

## All my internet research keeps pointing to Indexed Columns - what's that all about?

Indexing columns - before the threshold limit is broken - is the most effective way to mitigate View pain. In an ideal situation, where the user knows the List or Library will be large, you'd index any and all columns you can. This is done by going to the List or Library settings, and indexing the columns one by one. You can add up to 20 indexes to a list or library. Choose wisely - what columns would you want to base a view on?

  

>  **Automatic Indexing:**
> SharePoint lists/libraries now have the capability to index columns automatically. But like all automated processes, it may not index the *right* column for your users. Don't count on this to save you. Plan ahead.

 
It's important to take this action early - SharePoint on premise (2013) won't let you create an Index past 5000 items, and SharePoint Online won't let you create on past 20,000 items. Once you cross those lines, it is difficult to correct. You have to delete lists items to get back down below the limit, and then index the columns. (See linked article below for guidance on that)

### Column types that can be Indexed

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


In fact, if the columns displayed in your List/Library View are *all* indexed columns, the View will function almost like a regular list/library view.


### Indexed columns pair well with a Filtered View
Your default view in this large List or Library should ideally be composed of only Indexed columns.  If not, it should be filtered first by an Indexed column.  



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


  In this scenario, we've created a SharePoint List that will work great right to 30 million items.  Default view is bullet-proof in Classic or Modern. 

Your users can create Personal Views that show just their Created By entries.  Business analysts can create reports based on *Likes Cats* preference.  
  
  The *Biography* column - best case - isn't displayed in any views.  Only viewed/edited when the user interacts with the item.
  

### Example 2: Indexing Scenario for a Large Library
*Sorted by Created, Descending. Batches of 100.*
This library has 25,000 documents in it.  Each day a **folder** is created and seven regional sales reports are added to it.   The business has solemnly-sworn to follow this model.

| Column | Type | Index it? 
|--|--|--|
| Title | Single Line | Yes|
| Name | File Name | No, Can't |
| Sales Region  | Choice (single) | Yes |
| Likes Dogs | Yes/No | Yes |
| Created | Date | Yes
| Created By | Person | Yes   



The model will work great for years.  Each folder acts as sort of a reset on the Item Limit Threshold for the default view.   New folderless flat-Views can easily be created using the columns you've indexed.
> **Folders, Document Sets**
>Remember, folders count as items when calculating the threshold.






### Further Reading

  

  

* Microsoft: [Adding an index to a SharePoint column](https://support.microsoft.com/en-us/office/add-an-index-to-a-sharepoint-column-f3f00554-b7dc-44d1-a2ed-d477eac463b0)

  

* Microsoft: [Manage large lists and libraries in SharePoint](https://support.office.com/en-us/article/manage-large-lists-and-libraries-in-sharepoint-b8588dae-9387-48c2-9248-c24122f07c59)

  
* Blog: [SHAREPOINT ONLINE LIST VIEW THRESHOLD](https://joannecklein.com/2017/07/25/sharepoint-online-list-view-threshold/)

* Blog: [Deleting a Very Large SharePoint List](https://sympmarc.com/2017/03/27/deleting-a-very-large-sharepoint-list/)

  
  

  

---

  

  

**Principal author**: [Patrick M. Doran](http://www.linkedin.com/in/PatrickDoran)

  

  

---