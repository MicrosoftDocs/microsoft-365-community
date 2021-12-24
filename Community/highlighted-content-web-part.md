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
- It&#39;s an out of the box web part, so style options are _Grid, List, Carousel,_ and _Filmstrip._ This article assumes you&#39;re a site owner and not looking to custom code your own solutions.
- The type of content - and where you query it from – change your HCWP configuration and filtering choices.
- HCWP filtering capabilities are more complex than most other web parts. You can use **KQL** , **CAML** , and/or **Managed Properties** to filter and display very specific results. We&#39;ll cover examples of that here.

---

 As a site owner making pages for SharePoint or Teams, you understand the benefits of rolling up content from multiple lists, libraries, and sites and displaying them on a page. Using built-in List or Library web parts work fine, but your end users never put things in _just one_ place. They&#39;re empowered to self-organize their content across multiple sites! The Highlighted Content Web Part can help here, automatically showing users the right content, regardless of its actual location.

## Modern pages, modern Web Parts

Site Owners _of a certain age_ will remember Classic web part pages and the content rollup web parts. The Highlighted Content Web Part is maybe the successor to the _Content Query_ and _Content Search_ web parts. The mental model of HCWPs is similar. HCWPs require Modern pages.

## What Should I Learn?

To dig into the real power of the HCWP you&#39;ll need to increase your knowledge in some specific SharePoint areas and technologies. Here&#39;s the learning path you should traverse:

1. HCWP Fundamentals
2. Managed Properties in SharePoint Search
3. KQL
4. CAML (But maybe you don&#39;t have to?)

### HCWP Fundamentals

If you&#39;re new to the Highlighted Content Web Part start by reading Microsoft&#39;s documentation. In fact, even if you _have_ used the HCWP before, this existing documentation is a must a read. This Community Docs article won&#39;t rehash what&#39;s already covered there.

[https://support.microsoft.com/office/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd](https://support.microsoft.com/office/use-the-highlighted-content-web-part-e34199b0-ff1a-47fb-8f4d-dbcaed329efd)

### Managed Properties

Beyond the basic Filter options of the HCWP (things like &quot;Title includes&quot; or &quot;content includes&quot; or dates) this web part allows more advanced filtering and sorting by a _Managed Property_. A _Managed Property_ is something you might need to configure, through SharePoint Search, maybe with a Site Column (that has been crawled, and you&#39;ve made searchable). Once you&#39;ve set it up, you can filter and sort your data with Managed Properties.

_Site Columns_
 To make your column something you can filter it by in a HCWP, this is the sequence:

Make a Site Column -\&gt; Make sure it&#39;s in use -\&gt; That site columns is a Crawled Property you need to map to a Managed Property -\&gt; Available in HCWP

Start your _Site Column_ learning with these Microsoft Community Docs articles:

[https://docs.microsoft.com/en-us/microsoft-365/community/what-is-site-column](https://docs.microsoft.com/en-us/microsoft-365/community/what-is-site-column)

[https://docs.microsoft.com/en-us/microsoft-365/community/list-column-or-site-column-which-one-to-choose](https://docs.microsoft.com/en-us/microsoft-365/community/list-column-or-site-column-which-one-to-choose)

Start your _Managed Property_ learning with this [Microsoft Community Docs](https://docs.microsoft.com/en-us/microsoft-365/community/) article: [https://docs.microsoft.com/en-us/microsoft-365/community/how-do-site-columns-become-managed-properties-thus-available-for-search](https://docs.microsoft.com/en-us/microsoft-365/community/how-do-site-columns-become-managed-properties-thus-available-for-search)

And more here with Microsoft&#39;s documentation [https://docs.microsoft.com/en-us/sharepoint/manage-search-schema](https://docs.microsoft.com/en-us/sharepoint/manage-search-schema)


_Pro Managed Property Tips:_

- Impatient? Is your Managed Property ready for HCWP use yet? In SharePoint Online, sometimes it takes _an hour_ once you&#39;ve mapped the Crawled Property to the Managed Property. While you&#39;re waiting, test it out with regular SharePoint Search first. If you can search for results by a Managed Property there, you can filter content in your HCWP.


- It is fast and easy to make a new list – but if there&#39;s _any_ chance you think you might need to filter by it via a HCWP, make a column a real _Site Column_ first. (Taking an existing list&#39;s columns and converting them to a Site Column is a lot of manual work.)

 Learn all about Site Columns from this [Microsoft Community Docs](https://docs.microsoft.com/en-us/microsoft-365/community/) article: [https://docs.microsoft.com/en-us/microsoft-365/community/what-is-site-column](https://docs.microsoft.com/en-us/microsoft-365/community/what-is-site-column)

### Using KQL to query, filter, and sort

Once you&#39;ve added a HCWP to a page, you&#39;ll have to tell the web part _where_ to look, and _what_ to display. At first, the web part&#39;s basic Filter and sort options seem like they should cover most situations. But as you progress further into more complex projects (and your customers realize the capability having very specific content on a page) you, site owner, will find yourself needing build out HCWP with Custom Queries with KQL.

Good thing you set up all those Managed Properties from Site Columns already.

**KQL** (Keyword Query Language) runs a search over a specific area of content and return result in your HCWP.

 A very basic KQL query in a HCWP might look like:
author:&quot;Patrick Doran&quot;

While a more complex one might look like:
LastModifiedTime\&gt;=2021-06-01 AND LastModifiedTime\&lt;=2022-04-26

(This should include items modified between June 6th, 2021 until April 26th, 2022.)

_Learn about KQL_

Start learning by reading Microsoft&#39;s reference for KQL: [https://docs.microsoft.com/en-us/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference](https://docs.microsoft.com/en-us/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)

#### KQL Pro Tips:

- **Spacing counts** – A space between a colon and a &quot; might return a very different result.

- **You Path to find things** – The Path property is built in and can quickly narrow down scope if you know the list(s) and library(s) you want to get data from.

Path:&quot;https://\&lt;mytenantname\&gt;.sharepoint.com/sites/HumanResources/Enrollment/&quot;

Narrow it down further with the built-in Filetype property:

Path:&quot;https://\&lt;mytenantname\&gt;.sharepoint.com/sites/HumanResources/Enrollment/&quot; AND Filetype:&quot;XLSX&quot;

- **Many conditions** – If you have a lot of conditions, wrap statements in parentheses to make readability easier and enforce what should be AND versus OR.

(author:&quot;Patrick Doran&quot; OR &quot;Sally SharePoint&quot;) AND (filetype:xlsx OR docx)

####

 Helpful Built In Managed Properties

So now you understand Managed Properties and KQL. Below are examples of helpful KQL are all built into SharePoint Online, and probably there for your SharePoint 2019 farm. They&#39;re always-on, reliable, and save a lot of time on many HCWP scenarios.

| Managed Property Name | Type | Note | Example |
| --- | --- | --- | --- |
| IsDocument | True or False | A document is something in a document or pages library. Everything else is not. | IsDocument:&quot;True&quot; |
| Author | Someone&#39;s name, or the SharePoint property for the current user | This more or less equates to the SharePoint &#39;Created By&#39; field. | Author:&quot;Vallerie Viva&quot;
Author:{User.Name} |
| ContentType | Text |
 |
 |
| ContentClass | A search content type | An older way to search for things by type, but it checks out. Might be &quot;STS\_List&quot; or &quot;STS\_ListItem&quot;, &quot;STS\_Site&quot;, &quot;STS\_Web&quot; | ContentClass:STS\_ListItem

 ContentClass:STS\_ListItem\_Events
ContentClass: STS\_ListItem\_Tasks |
| FileType | File extension | An extension, like XLSX or DOCX or PDF | filetype:xlsx |
| Path | A URL | Might be a URL of a specific list, library, or everything in the whole tenant. | Path:https://\&lt;mytenant\&gt;.sharepoint.com/sites/demosite/Lists/ |

###

 Using CAML to query and filter

If your HCWP is displaying content from a _specific document or pages library_, you can use CAML. If you&#39;ve ever seen an XML file or RSS feed, CAML looks a lot like that.

An example CAML statement to filter data in a HCWP might look like:

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

This is looking for a column called _Expires_, where the value is equal to _today or after_ and it&#39;s sort order is by Modified date.

 Start learning CAML via Microsoft&#39;s documentation: [https://docs.microsoft.com/en-us/sharepoint/dev/schema/query-schema](https://docs.microsoft.com/en-us/sharepoint/dev/schema/query-schema)

### CAML vs KQL: Which one do I use?

With two Custom filter options, picking one comes down to the type of data you&#39;re filtering. A HCWP scoped to a Document/Pages library only lets you filter with CAML, while others let you filter with KQL.

 In many scenarios, KQL _might be able to do everything you need,_ and may be easier to read/write versus long, complex nested CAML queries.

## Real-world examples

The rest of this article will provide scenarios and tested examples to show you some possibilities. Since it is part of the [Microsoft Community Docs](https://github.com/MicrosoftDocs/microsoft-365-community), you&#39;re encouraged to contribute your own! [Thank you Emily Mancini for some of these!]

### Scenario 1: Contract documents across siloed departments

In your organization, a new contract process required documents from different departments. The vendor qualification document sat in the _Quality_ team, the contract review doc was with _Legal_, and the vendor initiation worksheet was with _Purchasing_. These documents rightfully sat in each department&#39;s own separate Communications Sites but needed to be presented in on a single page.

[https://3zccvt.sharepoint.com/sites/Legal](https://3zccvt.sharepoint.com/sites/Legal)

[https://3zccvt.sharepoint.com/sites/Quality](https://3zccvt.sharepoint.com/sites/Quality)

[https://3zccvt.sharepoint.com/sites/Purchasing](https://3zccvt.sharepoint.com/sites/Purchasing)

As the person setting up the HCWP:

- You&#39;ll be using a HCWP to retrieve documents from 3 different sites in the same tenant. Each document will use a shared Site Column with a value applied. The HCWP&#39;s job is to return any documents with a matching value for this Site Column.

 In our example we&#39;ll call our Site Column &quot;_Contracts_&quot; and will be looking for a value of _Legal, Purchasing,_ or _Qualifications_


- Making sure the same **Site Column** was available in all three sites.
 This is probably easiest if you can access the SharePoint Admin Center and add a Content Type and Site Column there first. Don&#39;t forget to publish it!

 You&#39;ll spend some time _waiting_ for the site columns to publish to the libraries, and then a little more time for search to pick them up as managed properties.


#### Setting up with regular Filtering (not a Custom Query)


Set your Content Source to be _All Sites_ or maybe a _Hub Site_ if you&#39;re using one. You could also pick &#39;Selected Sites&#39; if are sure these will only come from _Legal, Quality,_ and _Purchasing._ Leave the _Type_ as _Documents_ and _Document Type_ as _Any_.

 Under Filter, you could pick _Title includes the words_ and add one filter each for _Legal, Quality,_ and _Purchasing_ as long as those are the file titles. This option is a little riskier because someone could upload another file with those words in the title and they&#39;d also appear in the web part.

Probably the right call here is to use SharePoint metadata. Since you&#39;ve already added the _Contracts_ column as a Site Column, and flagged each file as wither _Purchasing, Legal,_ or _Qualification, let&#39;s use that instead._

In Site Settings, check to see if this column is already a Managed Property with a Crawled Property associated with it.

_Setting up with KQL_

Assuming you&#39;ve set up Managed and Crawled properties for the _Contracts_ column in SharePoint Administration, you should now have a property like _ContractsOWSCHCS …_ though yours might be named differently.

In your HCWP, choose &#39;Custom Query&#39; instead of &#39;Filter&#39; and set the Source to be &#39;All Sites&#39; or &#39;Hub Site&#39; if you have it. Now enter this in the Query text (KQL) field, and click Apply

isDocument=true AND (ContractsOWSCHCS: Legal OR ContractsOWSCHCS: Purchasing OR ContractsOWSCHCS: Qualification)

 The _isDocument=true_ is a built-in Managed Property, and will exclude list items that share the Site Column _Contracts_.

#### Setting up with CAML

CAML wouldn&#39;t work in this scenario, since we&#39;re looking for documents across multiple sites. CAML only shows up as a HCWP option when you select &#39;A document library in this site&#39; or &#39;A page library in this site&#39; for the Query source

### Scenario 2: Showing the right content at the right time

Another common scenario might be Human Resources documents on an Intranet Communication Site. There are many supporting documents for medical, dental, vision, wellness, life insurance, etc that an employee might need to access. These benefits documents are changed each year at a very specific go-live date for open enrollment, but the structure of the Benefits site generally stays the same.

 There is a short period of time where the current year and future year documents need to both be accessible as well.

Using metadata columns in libraries to indicate benefit type and year - paired with a HCWP - make for easy transitions as the HCWP query just needs to be updated.

 In this scenario we&#39;ll assume:

- Our single HCWP will appear on a page in a communications site.
- A single SharePoint Document Library with two columns – a date one for year, and a choice one for benefit type.
- Since this is a formal process, we&#39;ll make a new Content Type and Site Columns up front

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

Under Filter, pick Filtering by _Year_ which is a column you added. And because it&#39;s a date/time column, the HCWP will ask you to specify a range of time to filter. Before, After, or Between.

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

Often in SharePoint you&#39;ll have a list that becomes a database – a source of truth for many users. Often there is some criteria – &quot;top 10 highest grants this month&quot; or &quot;All the grants issued in Hawaii&quot; – that really matter. Those can be put in a page using a HCWP.

For our scenario, we have a large list (10k items) of grant applications that was imported from a spreadsheet. Customer wants to see cards on a page with just ones they&#39;ve updated and just ones from their home territory of Idaho.

#### Setting up with regular Filtering (not a Custom Query)

This is probably the easiest approach. We&#39;ll use three filters to meet this customer&#39;s needs.

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

## Pro HCWP Tips


- The built-in Managed Property _&quot;Path:&quot;_ has real power. It lets you specify scope all the way from a single list item to an entire tenant. No configuration required. With some wildcards and a little time, could can build some real specific KQL to bring back content you want.


- If you _can_ configure your Managed and Crawled Properties in the SharePoint admin center, you should.


- Once you get proficient at HCWPs, you might rely exclusively on Custom Queries with KQL for filtering. But if you _can_ use the built-in filters under _Filter and Sort_, maybe you should? The next person coming along to update your web part might not have read this article and built-in filters are a little easier to read if you&#39;re new.


- The built-in filtering guidance in Microsoft&#39;s documentation is worth remembering: _&quot;When you use multiple filters, your results will be based on OR operations for filters of the same type, and AND operations for filters of different types.&quot;_


- The _Trending_ sort and filter pulls from OneDrive, too. That may/may not be what you want.


- If you want to enable Audience Targeting in your HCWP, you need to also enable it in the list/library first.

## Further Reading

- [Modern SharePoint Web Parts: Highlighted Content Web Part](https://lightningtools.com/blog/modern-sharepoint-web-parts-highlighted-content-web-part) from Lightning Tools
- [Highlighted Content Web Part Custom Query](https://lightningtools.com/sharepoint/highlighted-content-web-part-kql-caml) from Lighting Tools
- [Managed Properties in SharePoint Online](https://sharepointmaven.com/6-ways-to-benefit-from-managed-properties-in-sharepoint-online/) and [Crawled vs Managed Properties in SharePoint Online](https://sharepointmaven.com/crawled-vs-managed-properties-in-sharepoint-online/) from SharePoint Maven
- [SharePoint Online Highlighted Content Web Part](https://www.spguides.com/sharepoint-online-highlighted-content/) – Deep dive from SPGuides.com
- [CAML Query Examples in SharePoint](https://www.spguides.com/caml-query-builder/) - from SPGuides.com
- [How Do Site Columns Become Managed Properties - Thus Available for Search](https://docs.microsoft.com/en-us/microsoft-365/community/how-do-site-columns-become-managed-properties-thus-available-for-search) – From Microsoft Community Docs
- [Crawled and Managed Properties Overview](https://docs.microsoft.com/en-us/sharepoint/technical-reference/crawled-and-managed-properties-overview) - Microsoft
- [How to Display a list of sites on a Modern Web Part page](https://social.technet.microsoft.com/wiki/contents/articles/53252.sharepoint-how-to-display-a-list-of-sub-sites-on-a-modern-site-page.aspx) - TechNet
- [KQL Basics in SharePoint](https://www.techmikael.com/2014/03/s15e01-kql-basics.html) – from Mikael Svenson
- [CAML Query Syntax](https://www.sharepointcafe.net/2015/06/caml-query-in-sharepoint.html) – from SharePoint Cafe

Working:

Grant site

[https://3zccvt.sharepoint.com/sites/DemoSite/Lists/Demo%20Grant%20List/AllItems.aspx](https://3zccvt.sharepoint.com/sites/DemoSite/Lists/Demo%20Grant%20List/AllItems.aspx)

[https://3zccvt.sharepoint.com/sites/DemoSite/\_layouts/15/listmanagedproperties.aspx?level=sitecol](https://3zccvt.sharepoint.com/sites/DemoSite/_layouts/15/listmanagedproperties.aspx?level=sitecol)

[https://3zccvt.sharepoint.com/sites/DemoSite/SitePages/Highlighted-Content-Web-Parts.aspx](https://3zccvt.sharepoint.com/sites/DemoSite/SitePages/Highlighted-Content-Web-Parts.aspx)

[https://3zccvt.sharepoint.com/sites/DemoSite/\_layouts/15/search.aspx/siteall?q=GranteeCountyNameOWSTEXT%3A%20Polk](https://3zccvt.sharepoint.com/sites/DemoSite/_layouts/15/search.aspx/siteall?q=GranteeCountyNameOWSTEXT%3A%20Polk)

[https://admin.microsoft.com/Adminportal/Home?source=applauncher#/homepage](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/homepage)

Legal Docs
[https://3zccvt.sharepoint.com/\_layouts/15/search.aspx/sitefiles?q=ContractsOWSCHCS%3A%20Qualification](https://3zccvt.sharepoint.com/_layouts/15/search.aspx/sitefiles?q=ContractsOWSCHCS%3A%20Qualification)

[https://3zccvt.sharepoint.com/sites/Quality/Shared%20Documents/Forms/AllItems.aspx](https://3zccvt.sharepoint.com/sites/Quality/Shared%20Documents/Forms/AllItems.aspx)
  
---

**Principal author**: [Patrick M. Doran](https://www.linkedin.com/in/PatrickDoran)

---
