---
title: Query String URL Tricks for SharePoint and Microsoft 365
ms.date: 03/22/2022
author: PatD
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: sharepoint-online
localization_priority:
description: Creative ways to filter, embed, and change page content by learning the secrets of URL query strings.
ms.collection: M365Community
---
  
# Query String URL Tricks for SharePoint and Microsoft 365

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

The URL is a core tenet of our online lives. Despite all the apps, browsers, and tools that occasionally obfuscate it, behind the scenes the Internet is glued together in part by the Uniform Resource Locator (URL). The data that populates the Teams app on your phone wouldn't make it there without the URL of the Graph API endpoint.

As a site owner or Microsoft 365 admin, you'll see URLs all the time: SharePoint sites, Microsoft Forms, shared links, and even application shortcuts like `https://office.com/launch/onedrive`.

This article will cover some powerful parameters that you can stick on the tail end of a URL to change what's shown on the page... and to make your job easier. These URL parameters will give you more options for solving problems.

## Overview

### The thing about query strings is… they are everywhere

You know this URL brings you to a website:

`https://learn.microsoft.com`

And this one brings you to a specific _section_ of that same website:

`https://learn.microsoft.com/search/`

What about this URL?

`https://learn.microsoft.com/search/?terms=community%20content`

It has a **?** at the end with a key (_terms_) and a value (_community content_). This is a **query string**. Based on the key and value in it, we can infer that it might affect or influence the page to show different content.

In this example, we can change the value in our address bar (and hit _return_) and the page content may be different. Example:

`https://learn.microsoft.com/search/?terms=large%lists`

### Multiple filters

Here's an example of multiple filtering with two keys (_products_ and _languages_) with their corresponding values (_m365_ and _javascript_):

`https://learn.microsoft.com/samples/browse`

`https://learn.microsoft.com/samples/browse?products=m365&languages=javascript`

And here's that same page loads different content with different values (_ms-graph_ and _html_)

`https://learn.microsoft.com/samples/browse/?products=ms-graph&languages=html`

How does this mental modal of _URL-as-page-transformer_ work in Microsoft 365? Keep reading!

## Useful Query String Tricks

### Put a Modern SharePoint page into Edit mode

Any Modern SharePoint Online page can be placed into **Edit** Mode by adding this query string URL: `?Mode=Edit`

`https://<yoursite>.sharepoint.com/sites/<sitename>/SitePages/default.aspx`

`https://<yoursite>.sharepoint.com/sites/<sitename>/SitePages/default.aspx?Mode=Edit`

This isn't really _easier_ than clicking the button on the page, but it's a good example of changing a page's look or function dramatically with a query string URL.

> [!TIP]
> **Sharing (links) is caring** - The URL, like the one in your browser's address bar, usually support spaces. So something like `?terms=policy security` works just fine. Where it _might not_ work consistently is when you share the URL via Email, text or Teams by copying and pasting it. As a best practice, replace any space in your URL query string with a `%20`, like `?terms=policy%20security`.
>
>_Safety first_.

### Put a Modern SharePoint page into Maintenance mode

Any Modern SharePoint Online page, like:

`https://<yoursite>.sharepoint.com/sites/<sitename>/SitePages/home.aspx`

 … can be placed into _Maintenance Mode_ by adding this query string to the URL: `?maintenancemode=true`

`https://<yoursite>.sharepoint.com/sites/<sitename>/SitePages/home.aspx?maintenancemode=true`

This gives you a behind-the-scenes view of the web parts on the page, and the data being sent back and forth between the page and the browser. This is helpful for diagnosing issues with pages including those using the SharePoint Framework (SPFx).

Read the official documentation on this in the article [Maintenance mode for client-side web parts](/sharepoint/dev/general-development/client-side-web-parts-maintenance-mode)

### Put (Nearly) Anything in SharePoint into Focused Mode

In the _Classic_ SharePoint days, there was a way to create a focused view of just content by appending `isDLg=1` as a query string to your URL. Those days are in the rear-view, but there's an updated version for Modern SharePoint: `?env=Embedded`

This hides the main navigation, footer, side navigation (and App bar) on just about anything in your SharePoint site, including:

- Pages
- List views
- Site Contents
- Site Analytics
- Recycle Bin

For example in a list it would be:

`https://<yoursite>.sharepoint.com/sites/<sitename>/Lists/<yourlistname>/allitems.aspx?env=Embedded`

In a page it would be:

`https://<yoursite>.sharepoint.com/sites/<sitename>/SitePages/default.aspx?env=Embedded`

If your page or list are living on a Hub Site, you may notice the Hub Site navigation will remain when using `env=Embedded`. If this is not desirable, e.g. if you are embedding a page using the embed webpart, you can append `?env=WebView` instead.

**Note:** With SharePoint pages, the Org Chart Web Part does not support working with `?env=WebView`.

### Show Any SharePoint List as a _Microsoft Lists_ List

If you've been building in Microsoft 365 for a while, you're probably used to working in SharePoint sites with pages, web parts, workflows, and navigations. Sometimes you just want to share the context of a single list or library within that site – and with a URL query string you can do just that.

Take your list, remove any existing query string on the end down to this:

`https://<yoursite>.sharepoint.com/sites/<sitename>/Lists/<yourlistname>/allitems.aspx`

 …and append this to the end of it:

`?env=WebViewList`

Like this:

`https://<yoursite>.sharepoint.com/sites/<sitename>/Lists/<yourlistname>/allitems.aspx?env=WebViewList`

That's it! Now your SharePoint list displays in Microsoft Lists. This is a great way to maximize screen real estate and help focus people during collaboration. This list remains housed in the original SharePoint site, but now with all the user interface polish of Microsoft Lists.

>[!TIP]
>**Filter your filters** - Sometimes you need to apply **two** or more query string filters to the same URL – two keys and two values. The format for that is generally to use the question mark (`?`) first, and the ampersand (`&`) for every additional key/value pair.
>
>Example:
> `page.aspx?mykey=myvalue&thisotherkey=someothervalue`

### Redirect users navigation from a List

You can redirect users navigation by including the `?Source=` query string in a list URL. This method could support all those use cases where a user is supposed to click on a link to add a new SharePoint list item. Without the `?Source=` query string, a user would "get stuck" in the the default list view, whereas this query string would help site owners control a user journey.

Example: users visit a SharePoint page containing a link/button/banner to let them fill out a form by adding a new SharePoint list item. The SharePoint page has the following URL: `https://<yoursite>.sharepoint.com/sites/<sitename>/SitePages/<yoursitepage.aspx>`

A SharePoint list uses an out-of-the-box .aspx page, to let users fill out a form and add a new item. For example: `https://<yoursite>.sharepoint.com/sites/<sitename>/Lists/<yourlistname>/NewForm.aspx`

After adding a new item, the `?Source=` query string will redirect users to the previous SharePoint page or any other web resource. A new item URL containing the `?Source=` query string would have a structure like this:

`https://<yoursite>.sharepoint.com/sites/<sitename>/Lists/<yourlistname>/NewForm.aspx?Source=https://<yoursite>.sharepoint.com/sites/<sitename>/SitePages/<yoursitepage.aspx>`

>[!NOTE]
> This method works even if a user clicks on the "Cancel" button of a list form! Therefore, a redirect to a "Thank you" page would lead to a misleading and inconsistent result, whereas an e-mail message from a Power Automate flow could be a better option, based on a new list item creation or not.

### Create a Link to a List or Library Search Result

Within the Modern user interface, the search bar sets its context (or scope) to the List, Library, or site you're in. When you perform a search from a list or library, it appends a query string of the search term to the URL. This link is sharable/bookmarkable.

Here's my example list:

`https://<greatsharepointsite>.sharepoint.com/sites/Lists/<ListName>/AllItems.aspx`

Here it is after a search for the phrase _tax documents_:

`https://<greatsharepointsite>.sharepoint.com/sites/Lists/<ListName>/AllItems.aspx?view=7&q=tax%20documents`

And if you change the value of the _q_ key in the URL query string, the results shown on the page will change:

`https://<greatsharepointsite>.sharepoint.com/sites/Lists/<ListName>/AllItems.aspx?view=7&q=consultants`

You can share this link, in a way that works almost like a SharePoint list view.

>[!TIP]
> Kick things up a notch by also adding the focused-mode query string filter in combination, like:
>
>`https://<greatsharepointsite>.sharepoint.com/sites/Lists/<ListName>/AllItems.aspx?view=7&q=engineering&env=Embedded`

### View search vertical immediately

After enabling or updating the search vertical, there is a delay of several hours before the changes can be seen on the search page. In that case, you can add `cacheClear=true` to the URL in SharePoint to view the changes immediately.

Read the official documentation on [View the vertical in the search result page](/microsoftsearch/manage-verticals#view-the-vertical-in-the-search-result-page).

### Debug SharePoint Framework Web Parts and Extensions

You can troubleshoot a SharePoint page to see if there is a SharePoint Framework (SPFx) extension or web part causing trouble. Add this `?disable3PCode` to the end of the URL to disable loading anything SPFx-related:

`https://<yoursite>.sharepoint.com/sites/<sitename>/SitePages/default.aspx?disable3PCode`

Read the official documentation on [Disable SPFx web parts and extensions](/sharepoint/dev/general-development/client-side-web-parts-maintenance-mode#disable-spfx-web-parts-and-extensions).

## Filtering and sorting modern SharePoint and Microsoft Lists views

Built into Modern SharePoint and Microsoft Lists and Libraries are some powerful filtering and sorting query string URLs. Below are some examples.

>[!TIP]
> While the syntax here will help show you the way, you can also build and discover your own query string URLs by using the View's filtering pane. As you toggle boxes for columns in the pane, observe how the URL changes. These query string URLs are bookmarkable and sharable!

### Sort List and Library views in SharePoint and Microsoft Lists

Within any view, you can add a query string to the URL to sort by a column.  Here's an example, where the column name _Complete_ is sorted ascending:

`https://<yoursite>.sharepoint.com/sites/Lists/mylist/AllItems.aspx?sortField=Complete&isAscending=true`

The `sortField` key is your internal column name, and `isAscending` determines the sort direction (_true_ for ascending, _false_ for descending).

### Filter Lists and Library views by column values with FilterField and FilterValue

Views can be filtered by specific column values with a query string URL. This could let you have a URL that filters by a status column value, or shows only items where some column value is _true_.

Filtering like this means never having to wait for search. SharePoint Search can sometimes take a few minutes to pick up on a change, but this filtering is immediate.

In a list or library, the minimum needed for this type of filter is:

`AllItems.aspx?useFiltersInViewXml=1&FilterField1=<internalFieldName>&FilterValue1=<value>`

(No `<` `>` brackets, you'd type the actual column value.)

- `?useFiltersInViewXml=1` tells the List or Library view that you're appending filtering criteria.
- `FilterField1=` is the _key_ and the value needs to be the internal name of the list/library column you want to filter by. (If you rename 'Title' to 'Product' in your list, you'll need to use 'Title' in your query string URL.)
- When filtering yes/no columns, use the number `0` for _no_ and the number `1` for _yes_.
- You can filter by multiple keys/values by incrementing the number pairs (up to 10), like this:
`?useFiltersInViewXml=1&FilterField1=<internalFieldName>&FilterValue1=<valueA>&FilterField2=<internalFieldName2>&FilterValue2=<valueB>&FilterField3=<internalFieldName3>&FilterValue3=<valueC>`

>[!TIP]
>You can find out the internal column name by going to List Settings, choosing the column, and looking after the `&Field=` key in the URL. That's using a query string URL to help you make a query string URL!

**Example Scenario using FilterField**
_You might have a Power Automate Flow set to email a List view status report URL based about a product in a list… with hundreds of possible products. You wouldn't want to make separate views for each product._

To solve this, you start with your All Items view and append URL query strings to create dynamic URLs for your Flow emails:
`https://<mytenant>.sharepoint.com/Lists/mylist/AllItems.aspx`

Here's that same List view, showing only items where the _Product_ column is equal to _Tacos_:
`https://<mytenant>.sharepoint.com/Lists/mylist/AllItems.aspx?useFiltersInViewXml=1&FilterField1=Product&FilterValue1=Tacos`

That same List view, showing only items where the _Product_ column are equal to _Pizza_... and now with a second filter to show where the _Tasty_ column is set to _Yes_:
`https://<mytenant>.sharepoint.com/Lists/mylist/AllItems.aspx?useFiltersInViewXml=1&FilterField1=Product&FilterValue1=Pizza&FilterField2=Tasty&FilterValue2=1`

Your boss wants it sorted newest to oldest, so go ahead and add the query string to sort by _Created_ date.

`https://<mytenant>.sharepoint.com/Lists/mylist/AllItems.aspx?sortField=Created&isAscending=false&useFiltersInViewXml=1&FilterField1=Product&FilterValue1=Pizza&FilterField2=Tasty&FilterValue2=1`

### FilterField for multiple values

With a choice column, its possible to return multiple list items/library files from a single query string URL.  Replace `FilterValue1` with `FilterValues1` and list each choice out separated by `%3B%23`

Here's an example of a query string URL on a list view that returns any items where the _Status_ field is set to either _Better_ or _Awesome_:

`https://<mytenant>.sharepoint.com/Lists/mylist/AllItems.aspx?useFiltersInViewXml=1&FilterFields1=Status&FilterValues1=Better%3B%23Awesome`

## Further view filter reading from the experts

The list/library view filtering capabilities are extensive. These articles go into further detail, including filtering with managed metadata.

- Nate Chamberlain: [How to filter a SharePoint list or library using URL parameters](https://natechamberlain.com/2020/05/09/how-to-filter-a-sharepoint-list-or-library-using-url-parameters/)

- Piyush K Singh: [Generate Modern List Filter URL: Managed Metadata](https://piyushksingh.com/2019/05/24/generate-modern-list-filter-url-managed-metadata/)

## Conclusion ?article=done

This article has hopefully given you awareness of the hidden power of query string URLs, and how they can let the platform do some of the work for you.

If you know of other useful query strings like these, you should consider contributing them to these Microsoft Community Content documents. You can open an issue in the [GitHub](https://github.com/MicrosoftDocs/microsoft-365-community) repo, or submit your own pull request!

---

**Principal author**: [Patrick M. Doran](https://www.linkedin.com/in/PatrickDoran)

---
