---
title: Level Up Your Highlighted Content Web Parts
ms.date: 12/01/2021
author: PatD
ms.reviewer:
manager:
ms.topic: article
ms.author:
ms.service: sharepoint-online
localization_priority:
description: Advanced level querying and filtering scenarios for Highlighted Content Web Parts, with KQL, CAML and Managed Properties.
ms.collection: M365Community
---
  
# Level Up Your Highlighted Content Web Parts

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## Highlighted Content Web Part - tl;dr

- The Highlighted Content Web Part (HCWP) is used for displaying content from one or more _buckets_ – more than one list, library, or data source in a single place on a page.

- It's an out of the box web part, so style options are _Grid, List, Carousel,_ and _Filmstrip._ This article assumes you're a site owner and not looking to custom code your own solutions.

- The type of content - and where you query it from – change your HCWP configuration and filtering choices.
- HCWP filtering capabilities are more complex than most other web parts. You can use **KQL**, **CAML**, and/or **Managed Properties** to filter and display very specific results. We'll cover examples of that here.

---
As a site owner making pages for SharePoint or Teams, you understand the value of automatically rolling up content from multiple lists, libraries, and sites and displaying them on a page. Using built-in List or Library web parts work fine... but your end users never put things in _just one place_. They're empowered to self-organize their content across multiple sites! The Highlighted Content Web Part can help here, automatically showing users the right content, regardless of its actual location.

> **Modern pages, modern web parts**
>
> Site Owners of _a certain age_ will remember Classic web part pages and their content rollup web parts. The Highlighted Content Web Part is maybe the successor to the _Content Query_ and _Content Search_ web parts. The mental model is very similar.
> HCWPs require Modern pages.

## What Should I Learn?

To dig into the real power of the HCWP you'll need to increase your knowledge in key SharePoint areas and technologies. Here's the learning path you should traverse:

1. HCWP fundamentals
2. Managed Properties and SharePoint Search
3. KQL
4. Maybe CAML (But, maybe you don't have to?)

### 1. Fundamentals

If you're new to the Highlighted Content Web Part start by reading Microsoft's documentation. In fact, even if you _have_ used the HCWP before, this existing documentation is a must a read.

[Use the Highlighted content web part](https://support.microsoft.com/office/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd)

(This Community Docs article won't rehash what's already covered there.)

### 2. Managed Properties

Beyond the basic Filter options of the  (things like "Title includes" or "content includes" or dates) this web part allows more advanced filtering and sorting by a _Managed Property_.

For the HCWPs, the Managed Property is one of two things:

1. A built in property, no configuration required. `IsDocument` is an example - this one lets you include/exclude Documents in a query. Another built in Managed Property is `Author` which query content based on a M365 user.
2. A Site Column derived Managed Property - where a List/Library column is made available through Search as a Managed Property.

Managed Properties are available to filter and sort in HCWPs either through the regular Filter interface or via the more customizable KQL interface.  More on that later on.

#### Learn about Site Columns

Start your _Site Column_ learning with these Microsoft Community Docs articles:

- [What is a Site Column](https://docs.microsoft.com/microsoft-365/community/what-is-site-column)
  
- [List Colum or Site Columns - Which one to choose?](https://docs.microsoft.com/microsoft-365/community/list-column-or-site-column-which-one-to-choose)

#### Learn about Managed Properties

Start your _Managed Property_ learning with this [Microsoft Community Docs](https://docs.microsoft.com/microsoft-365/community/) article:

- [How do Site Columns Become Managed Properties for Search?](https://docs.microsoft.com/microsoft-365/community/how-do-site-columns-become-managed-properties-thus-available-for-search)

And more here with Microsoft's documentation:

- [Manage the search schema in SharePoint](https://docs.microsoft.com/sharepoint/manage-search-schema)
  
> [!TIP]
> Is your recently-configured _Managed Property_ ready for HCWP use yet? In SharePoint Online, sometimes it takes an hour once you've mapped the Crawled Property to the Managed Property. While you're waiting, test availability via regular SharePoint Search first. If you can search for results by a Managed Property there, you can filter content by that same Property in your HCWP

> [!TIP]
>It is fast and easy to make a new list – but if there's a chance you think you might need to filter by it via a HCWP, make that List Column into a _Site Column_ first. Taking an existing List Columns and converting them to a Site Column is a lot of manual work.

### 3. Using KQL to query, filter, and sort

Once you've added a HCWP to a page, you'll have to tell the web part _where_ to look, and _what_ to display. At first, the web part's basic filter and sort options seem like they should cover most situations. But as you progress further into more complex projects (and your customers realize the capability displaying very specific content on a page) you, site owner, will find yourself needing build out HCWPs with Custom Queries with KQL (Keyword Query Language) .

Good thing you set up all those _Managed Properties_ from _Site Columns_ already.  KQL is the payoff for that work.

KQL runs a search over a specific area of content and return result in your HCWP. A very basic KQL query in a HCWP might look like:

`author:"Patrick Doran"`

While a more complex one might look like:

`LastModifiedTime>=2021-06-01 AND LastModifiedTime<=2022-04-26`

This should include items modified between June 6th, 2021 until April 26th, 2022.

#### Learn about KQL

Start learning by reading Microsoft's reference for KQL:

- [KQL Syntax Reference](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-KQL-syntax-reference)

##### KQL Pro Tips

- **Spacing counts** – A space between a colon and a &quot; might return a very different result.

- **You _Path_ to success** – The _Path_ property is built in and can quickly narrow down scope if you know the list(s) and library(s) you want to get data from.

  `Path:"https://mytenantname.sharepoint.com/sites/HumanResources/Enrollment"`

Narrow it down further with the built-in Filetype property:

  `Path:"https://mytenantname.sharepoint.com/sites/HumanResources/Enrollment" AND Filetype:"XLSX"`

- **Many conditions** – If you have a lot of conditions, wrap statements in parentheses to make readability easier and enforce what should be AND versus OR.

  `Author:"Patrick Doran" OR "Sally SharePoint") AND (Filetype:"xlsx OR docx)`

#### Helpful Built In Managed Properties

So now you understand Managed Properties and KQL. Below are examples of helpful KQL are all built into SharePoint Online (and probably there for your SharePoint 2019 farm.) They're always-on, reliable, and save a lot of time on many HCWP scenarios.  Use these to filter and sort your content.

| Managed Property | Type | Note | Example |
| --- | --- | --- | --- |
| `IsDocument` | True or False | A document is something in a document or pages library. Everything else is not. | `IsDocument:"True"` |
| `Filetype` | File extension | An extension, like XLSX or DOCX or PDF | `filetype:xlsx` |
| `Author` | Someone's name, or the SharePoint property for the current user | This more or less equates to the SharePoint 'Created By' field. | `Author:"Tricia Teams"` or `Author:{User.Name}` |
| `Path` | A URL, or part of a URL | It might be a URL of a specific list, library, or everything in the whole tenant. | `Path:"https://mytenant.sharepoint.com/sites/demosite/Lists/"` |
| `ContentType` | Text | | |
| `ContentClass` | A search content type | An older way to search for things by _type_, but it works with HCWPs.  Usually stars with _STS__ like `STS_List`, `STS_ListItem`, `STS_Site`, or `STS_Web` | `ContentClass:STS_ListItem`, `ContentClass:STS_ListItem_Tasks`, `ContentClass:STS_ListItem_Events` |

### 4. Using CAML to query and filter

If your HCWP is displaying content from a _specific document or pages library_, you can use CAML. If you've ever seen an XML file or RSS feed, CAML looks a lot like that.

An example CAML statement to filter data in a HCWP might look like:

```XML
<Query>
  <Where>
    <Geq>
      <FieldRef Name="Expires"/>
      <Value Type="DateTime">
        <Today/>
      </Value>
    </Geq>
  </Where>
  <OrderBy>
    <FieldRef Name="Modified"/>
  </OrderBy>
</Query>
```

This is looking for a column called _Expires_, where the value is equal to _today or after_ and it's sort order is by Modified date.

Start learning CAML via Microsoft's documentation:
[Learn about CAML query schema](https://docs.microsoft.com/sharepoint/dev/schema/query-schema)

>[!NOTE]
>**CAML vs KQL: Which one do I use?**
>
>With two Custom Filter options for a Highlighted Content Web Part, picking one comes down to the type of data you're filtering. A HCWP scoped to a Document/Pages library only lets you filter with CAML, while others let you filter with KQL.
>
>In many scenarios, KQL  _might be able to do everything you need,_ and may be easier to read/write versus long, complex nested CAML queries. Just set the query to the site (rather than a particular library) and scope it with the `Path` managed property.

---

## Real-world examples

The rest of this article will provide scenarios and tested examples to show you some possibilities. Since it is part of the [Microsoft Community Docs](https://github.com/MicrosoftDocs/microsoft-365-community), you're encouraged to contribute your own! [_Thank you Emily Mancini for some of these!_]

### Scenario 1: Contract documents across siloed departments

In your organization, a new contract process required documents from different departments. The vendor qualification document sat in the _Quality_ team, the contract review doc was with _Legal_, and the vendor initiation worksheet was with _Purchasing_. These documents lived in each department's own separate Communications Sites but needed to be presented in on a single page.

This looks like a job for the Highlighted Content Web Part!

Your libraries:

- `https://mytenant.sharepoint.com/sites/Legal/Shared Documents/`
- `https://mytenant.sharepoint.com/sites/Quality/Shared Documents/`
- `https://mytenant.sharepoint.com/sites/Purchasing/Shared Documents/`

As the person setting up the HCWP:

- You'll use a HCWP to retrieve documents from 3 different sites in the same tenant. Each document will have a shared Site Column with a value applied. The HCWP's job is to return any documents with a matching value for this Site Column.
- You'll query based off a Site Column called "**Contracts**" and will be looking for a value of _Legal, Purchasing,_ or _Qualifications_
- You'll make sure the same **Site Column** is available in all three sites, in the three libraries.

>[!Note]
>Adding the Site Column is probably easiest if you can do it the SharePoint Admin Center. Don't forget to publish it!

#### Setup with regular Filtering (not a Custom Query)

1. Set your Content Source to be _All Sites_ or maybe a _Hub Site_ if you're using one. You could also pick 'Selected Sites' if are sure the documents you want to show will only come from _Legal, Quality,_ and _Purchasing._ libraries. Leave the _Type_ as _Documents_ and _Document Type_ as _Any_.

2. Under Filter, you could pick _Title includes the words_ and add one filter each for _Legal, Quality,_ and _Purchasing_ as long as those are the file titles. This option is a little riskier because someone could upload another file with those words in the title and they'd also appear in the web part.

    The safer call here is to use SharePoint metadata. Since you've already added the _Contracts_ column as a Site Column, and flagged each file as wither _Purchasing, Legal,_ or _Qualification_, let's use that instead.

In Site Settings, check to see if this column is already a Managed Property with a Crawled Property associated with it.

#### Setting up with _KQL_

Assuming you've set up Managed and Crawled properties for the _Contracts_ column in SharePoint Administration, you should now have a property like _ContractsOWSCHCS …_ though yours might be named differently.

In your HCWP, choose 'Custom Query' instead of 'Filter' and set the Source to be 'All Sites' or 'Hub Site' if you have it. Now enter this in the Query text (KQL) field, and click Apply

`isDocument=true AND (ContractsOWSCHCS: Legal OR ContractsOWSCHCS: Purchasing OR ContractsOWSCHCS: Qualification)`

#### Setting up with CAML

CAML wouldn't work in this scenario, since we're looking for documents across multiple sites. CAML only shows up as a HCWP option when you select 'A document library in this site' or 'A page library in this site' for the Query source

### Scenario 2: Showing the right content at the right time

  

Another common scenario might be Human Resources documents on an Intranet Communication Site. There are many supporting documents for medical, dental, vision, wellness, life insurance, etc that an employee might need to access. These benefits documents are changed each year at a very specific go-live date for open enrollment, but the structure of the Benefits site generally stays the same.

  

There is a short period of time where the current year and future year documents need to both be accessible as well.

  

Using metadata columns in libraries to indicate benefit type and year - paired with a HCWP - make for easy transitions as the HCWP query just needs to be updated.

  

In this scenario we'll assume:

  

- Our single HCWP will appear on a page in a communications site.

- A single SharePoint Document Library with two columns – a date one for year, and a choice one for benefit type.

- Since this is a formal process, we'll make a new Content Type and Site Columns up front

  

Library setup:

  

- Create a library

- Create Content Type

- Create site columns for _Year_ and _Benefit Type_ columnsand add to your Content Type

- Add the new Content Type to library. This should also add your site columns.

- In Site Collection search, map the Crawled Properties to Managed Properties for both site columns.

- Go get a coffee or a tea and wait for SharePoint Search to do its thing with your columns.

  

| **Name** | **Year** | **Benefit Type** | **Content Type** |

| --- | --- | --- | --- |

| Dental Doc for Annual Enrollment.pdf | 1/1/2023 | Dental | Enrollment |

| Life Insurance Enrollment Document.pdf | 1/1/2022 | Life Insurance | Enrollment |

| Medical Health Insurance Enrollment Form.pdf | 1/1/2023 | Medical | Enrollment |

| Vision Enrollment Employee Form.pdf | 1/1/2023 | Vision | Enrollment |

| Wellness Worksheet for Enrollment.xlsx | 1/1/2022 | Wellness | Enrollment |

  

#### Setting up with regular Filtering (not a Custom Query)

  

Add your HCWP to the page, pick Filter instead of Custom query, and set your source to be the document library with your content type and site columns.

  

Under Filter, pick Filtering by _Year_ which is a column you added. And because it's a date/time column, the HCWP will ask you to specify a range of time to filter. Before, After, or Between.

  

In this case – set _Year_ between 01/01/22 and 12/12/22. The HCWP will show only documents from that library for 2022.

  

_Setting up with KQL_

  

Add your HCWP and pick Custom Query, and set your source to be the entire Site. (If you select Document Library, the HCWP will default to CAML).

  

Find out the Managed Property name for the _Year_ column (it might be YearOWSDATE).

  

NOTE: DATE COLUMN FOR KQL

  

#### Setting up with CAML

  

\&lt;Query\&gt;

\&lt;Where\&gt;

  

\&lt;Geq\&gt;

  

\&lt;FieldRef Name=&quot;Expires&quot;/\&gt;

  

\&lt;Value Type=&quot;DateTime&quot;\&gt;

  

\&lt;Today/\&gt;

  

\&lt;/Value\&gt;

  

\&lt;/Geq\&gt;

  

\&lt;/Where\&gt;

  

\&lt;OrderBy\&gt;

  

\&lt;FieldRef Name=&quot;Modified&quot;/\&gt;

  

\&lt;/OrderBy\&gt;

  

\&lt;/Query\&gt;

  

### Scenario 3: Showing very specific, contextual list items

  

Often in SharePoint you'll have a list that becomes a database – a source of truth for many users. Often there is some criteria – &quot;top 10 highest grants this month&quot; or &quot;All the grants issued in Hawaii&quot; – that really matter. Those can be put in a page using a HCWP.

  

For our scenario, we have a large list (10k items) of grant applications that was imported from a spreadsheet. Customer wants to see cards on a page with just ones they've updated and just ones from their home territory of Idaho.

  

#### Setting up with regular Filtering (not a Custom Query)

  

This is probably the easiest approach. We'll use three filters to meet this customer's needs.

  

Set source to _All Sites._ First filter with be using the built-in Managed Property of _Path_.

  

![](RackMultipart20211224-4-1a6d1mj_html_fccbace099aed813.png)

  

![](RackMultipart20211224-4-1a6d1mj_html_768b4570c64e8ca2.png)

  

![](RackMultipart20211224-4-1a6d1mj_html_174d31aa03a8f6fd.png)

  

####

  

#### Setting up with CAML

  

CAML is off the table here – it only works for documents and pages.

  

####

  

Setting up with KQL

  

(Path:https://3zccvt.sharepoint.com/sites/DemoSite/Lists/Demo%20Grant%20List AND &quot;Idaho&quot; AND Author:{User.Name} AND IsDocument:&quot;False&quot; AND contentclass:STS\_ListItem)

  

### Pro HCWP Tips
- The built-in Managed Property _&quot;Path:&quot;_ has real power. It lets you specify scope all the way from a single list item to an entire tenant. No configuration required. With some wildcards and a little time, could can build some real specific KQL to bring back content you want.
- If you _can_ configure your Managed and Crawled Properties in the SharePoint admin center, you should.
- Once you get proficient at HCWPs, you might rely exclusively on Custom Queries with KQL for filtering. But if you _can_ use the built-in filters under _Filter and Sort_, maybe you should? The next person coming along to update your web part might not have read this article and built-in filters are a little easier to read if you're new.
- The built-in filtering guidance in Microsoft's documentation is worth remembering: "When you use multiple filters, your results will be based on OR operations for filters of the same type, and AND operations for filters of different types."_
- The _Trending_ sort and filter pulls from OneDrive, too. That may/may not be what you want.
- If you want to enable Audience Targeting in your HCWP, you need to also enable it in the list/library first.

## Further Reading

The time you invest in learning the HCWP will help you in other areas of the Microsoft 365 platform, especially with SharePoint search. Keep learning:

- [Modern SharePoint Web Parts: Highlighted Content Web Part](https://lightningtools.com/blog/modern-sharepoint-web-parts-highlighted-content-web-part) from Lightning Tools

- [Highlighted Content Web Part Custom Query](https://lightningtools.com/sharepoint/highlighted-content-web-part-KQL-caml) from Lighting Tools

- [Managed Properties in SharePoint Online](https://sharepointmaven.com/6-ways-to-benefit-from-managed-properties-in-sharepoint-online/) and [Crawled vs Managed Properties in SharePoint Online](https://sharepointmaven.com/crawled-vs-managed-properties-in-sharepoint-online/) from SharePoint Maven

- [SharePoint Online Highlighted Content Web Part](https://www.spguides.com/sharepoint-online-highlighted-content/) from SPGuides.com

- [CAML Query Examples in SharePoint](https://www.spguides.com/caml-query-builder/) from SPGuides.com

- [How Do Site Columns Become Managed Properties - Thus Available for Search](https://docs.microsoft.com/microsoft-365/community/how-do-site-columns-become-managed-properties-thus-available-for-search) from Microsoft Community Docs

- [Crawled and Managed Properties Overview](https://docs.microsoft.com/sharepoint/technical-reference/crawled-and-managed-properties-overview) from Microsoft

- [How to Display a list of sites on a Modern Web Part page](https://social.technet.microsoft.com/wiki/contents/articles/53252.sharepoint-how-to-display-a-list-of-sub-sites-on-a-modern-site-page.aspx) - TechNet

- [KQL Basics in SharePoint](https://www.techmikael.com/2014/03/s15e01-kql-basics.html) from Mikael Svenson

- [CAML Query Syntax](https://www.sharepointcafe.net/2015/06/caml-query-in-sharepoint.html) from SharePoint Cafe

---
**Principal author**: [Patrick M. Doran](https://www.linkedin.com/in/PatrickDoran)
