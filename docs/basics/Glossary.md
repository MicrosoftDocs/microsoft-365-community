# SharePoint Usage Glossary

As with any technology, there are lots of terms we toss around to explain things. Just understanding what each term means can be half the battle. Whether you are entirely new to SharePoint or have been using it for a decade, there are always new terms to learn. The fact that Microsoft uses common English words for many capabilities can add an additional layer of confusion.

This Glossary is an attempt to demystify some of the terms and acronyms we use every day in working with the platform. See one missing? Feel free to add an Issue with what you want added.

[A](#A) [B](#B) [C](#C) [D](#D) [E](#E) [F](#F) [G](#G) [H](#H) [I](#I) [J](#K) [K](#K) [L](#L) [M](#M) [N](#N) [O](#O) [P](#P) [Q](#Q) [R](#R) [S](#S) [T](#T) [U](#U) [V](#V) [W](#W) [X](#X) [Y](#Y) [Z](#Z)

## A

### App

An App is a term in SharePoint that means a packaged extension or customization that you can add to a site. An app can simply be a list that you add to a site to store information, or it can be a package that installs web parts that are available to use on pages, customizations that give you extra functionality within existing lists and libraries, or it could be an entire application that runs outside of SharePoint but has the ability to read and write back to your SharePoint site.

### Application Customizer

See [SharePoint Framework](#sharepoint-framework)

## B

## C

### CAML (Collaborative Application Markup Language)

An XML fragment used by SharePoint to define the internal structure of sites, lists, fields, views and content types, declaratively, also used to query data in SharePoint lists to selectively retrieve data.

### Classic SharePoint

Classic SharePoint refers to the user interface (UI) that was available starting in SharePoint 2013 - what you might think of as the blue and white UI. Classic SharePoint uses master pages and page layouts for content structuring. These capabilities were built on the .NET framework.

### Column Formatting

Column Formatting is a SharePoint feature that allows users to customize the display of fields in Document Libraries and Lists. Colors, icons, images and other elements are used to highlight content and improve the user experience. Links are used to make content actionable. 

Some columns types, like Date and Choice, include ready made design templates. All column types allow for advanced formatting using JSON code.  

### Command Set

See [SharePoint Framework](#sharePoint-framework)

### Communication Site

A Communication Site is generally used to communicate from a smaller group to a larger group. For this reason, Communication Sites are often used in Intranets.

### Content Query Web Part

The Content Query Web Part (CQWP) is a web part available in Classic SharePoint that allows rolling up of content across lists and sub sites. The content returned is limited to only the site collection the web part is in. This web part has been replaced by the Highlighted Content web part in Modern SharePoint which gets around the site collection limitation.

### Crawled Property

A Crawled Property is one of the basic units of the Search Schema. They are created automatically by the SharePoint Search Indexer (or Crawler) when it is discovering content that can be searched. The information stored in Crawled Properties is made available in queries by mapping them to Managed Properties.

### Customization

Improving specific aspects of SharePoint functionality by changing settings through the end user interface. See also [SharePoint Framework](#sharepoint-framework)

## D

### Disaster Recovery (DR)

The planning and practice of ensuring systems are available when a disaster occurs or that they can be restored as quickly as possible.

## E

### Enterprise Content Types

Content Types and Site Columns that are defined in the Content Type Hub, then published to all sites collections in the tenant.

## F

### Farm

A set of servers that hosts the SharePoint Application, including SQL servers that host the SharePoint databases. A Farm can be single server or multi-tiered architecture containing multiple servers.

### Field Customizer

See [SharePoint Framework](#sharePoint-framework)

### First Release

Deprecated - please see [Targeted Release](#targeted-release).

## G

### Governance

### Group

A Group in SharePoint can generally refer to one of three things. It may mean:

- SharePoint Group

  - A container to organize users and other security groups. A SharePoint group can be assigned permission levels on an object such as a site, a library or library, a folder or a document (or page, or item). Generally only a Site Owner can manage who is in a SharePoint Group.

- Office Group

  - An Office 365 Group is a concept within Office 365 that allows users can be members of, which has it's own e-mail address, and can be associated to a Microsoft Teams team, or a SharePoint Site. A Microsoft Teams Team automatically creates an Office 365 Group. These can be public where anyone can join, or Private when you need to be invited or given a code to join. Permissions are simplified to only "Owners" or "Members".
  
 - Security Group
 
  - A security group is a container of users defined in Active Directory, one or more of these can be added to SharePoint Groups. Adding users in the security groups applies permissions in SharePoint.

## H

### Hub Site

A Hub Site is a SharePoint site that can have other sites associated to it. This allows you to group sites by department, region, or project etc. Features such as News and Highlight Content can be used to produce a roll up view of content like pages and documents from the associated sites on a page on the Hub Site.

## I

### Inheritance

Inheritance refers to the cascading of default site permission levels (i.e. Owner, Member and Visitor) to site Document Libraries, Lists, Site Pages etc. 

Inheritance can be "broken" to allow for [unique permissions](#Unique-Permissions).

## J

## K

### Known Folder Move (KFM)

Known Folder Move (KFM) allows you to automatically backup/redirect your Windows client's Desktops, Documents, and Pictures folders to OneDrive for Business. It gives you a transparent way to ensure your local files are never lost.

## L

### Library

A library, typically used as a Document Library is a type of list where documents or other files are added as items, but no further file attachments can be added to the document item. Other files are added as separate entries in the library.

### Licensing

Office 365 offers multiple licensing options (Kiosk, F1, E1, etc.), each of which turns on a different basket of capabilities for the user to whom the license is assigned.

### List

A List in SharePoint is a table used to store information in a SharePoint site. A list has columns that can be used to store different types of information, and each row in a list is known as an "Item". SharePoint attempts you to very carefully design lists if you attempt to store "large" amounts of data (more than 5,000 items), including things like limiting the number of "Lookup Columns" that can be used. Therefore, if you are planning on storing more than a few thousand items, be sure to follow Microsoft guidelines on storing large amounts of data in lists.

An item in a list can have multiple file attachments added. This is useful if you use a custom list as an Issue Tracker for example, and want to be able to add screenshots to an item in.

A library is a type of list where documents or other files are added as items, but no further file attachments can be added.

## M

### Managed Metadata

Managed Metadata is a SharePoint feature that allows the business to create a hierarchy of terms that can be used in SharePoint Sites to tag content. This is used by creating the hierarchy using Term Groups and Term Sets, then adding a column to a list of type "Managed Metadata" and setting the Term Set to use for tagging. When an item is added to that list or library, the new column is used to tag that item or document.

### Managed Property

A Managed Property is one of the basic units of the SharePoint Search Schema. It's an entry in the Schema that you refer to when doing search queries that use specific properties, or when specifying which information you want to return.

Managed Properties can be created (if you have the appropriate permissions), although SharePoint automatically creates Managed Properties that are useful for a wide range of scenarios.

### Modern SharePoint

Modern SharePoint refers to the user interface (UI) that has been available in SharePoint Online to larger and larger degrees starting in about 2016. Some aspects of the modern UI are also available in SharePoint 2019 (on premises). Modern SharePoint does not use many of the underpinnings of classic SharePoint, such as master pages and page layouts. It is built using more current Web development tools and practices than classic SharePoint.

## N

## O

### On premises

On premises refers to running servers yourself, whether they are in your physical building, a data center where you rent space, or at a hosting company that runs servers specifically for you.

### Out of the box

Capabilities included with SharePoint without writing any code or doing heavy lifting. Depending on who you talk to, this definition probably includes a level of [customization](#Customization) including things like creating new sites, lists, and libraries.

## P

### Patterns and Practices

Patterns and Practices is an open-source initiative coordinated by SharePoint engineering. This community controls SharePoint development documentation, samples, reusable controls, and other relevant open-source initiatives related to SharePoint development.

### Permission Level

A Permission Level is a set of specific permissions such as "Add an item" or "Edit Lists". SharePoint comes with a set of Permission Levels as standard, such as "Contribute" or "Design", which have different capabilities.

Custom Permission Levels can be created for business-specific scenarios, such as "Can add documents but not delete" by choosing the correct options, and applied to a User or Group.

### PnP

See [Patterns and Practices](#patterns-and-practices)

### PowerShell

[PowerShell](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/powershell) is an automation scripting language from Microsoft, which was originally only available on Windows devices, and built on top of the .NET Framework. Since 2016, we also have [PowerShell Core](https://github.com/PowerShell/PowerShell) which is open-source, cross-platform, and built on top of .NET Core.

The version that ships on Windows devices is called Windows PowerShell, and the cross-platform version is called PowerShell Core, and is also available on Windows.

## Q

## R

### Roll up

### Root Site

The base address in a web application or tenant for the first SharePoint Site collection. Typically, defined without use of managed paths ("/sites/" or "/teams/"), for example https://mytenant.sharepoint.com or http://sharepoint

## S

### Search Schema

The Search Schema refers to the customizable data dictionary used by SharePoint Search to allow users to query for and return specific information from SharePoint using the available Search tools, such as the Search Results web part in Classic SharePoint or the Search REST API.

### Site

### Site Collection

A Site collection is a group of websites that have the same owner and share administrative settings.

- In *SharePoint Online*, site collections are the top level available to admins, and visible in the SharePoint Admin Center under "Active Sites".
- In *SharePoint on-premises*, site collections are created within a Web Application, which is a level higher.

When you create a site collection, a top-level site is automatically created in the site collection (called root site). You can then create one or more subsites below the top-level site. The entire structure of the top-level site and all its subsites is called a site collection.

### Standard Release

### Style Library

The Style Library is a document library in the Root Web of a SharePoint site that is used mainly in Classic SharePoint Sites. One of the purposes of this library is as a recognized "secure location" to store XSL Templates that are used by the Content Query Web Part (XSL templates outside of the Style Library cannot be used in Content Query Web Parts).

### SharePoint Framework

The SharePoint Framework (also known as SPFx) is a way for developers to extend SharePoint online, Microsoft Teams and in a slightly more limited way SharePoint 2019 and SharePoint 2016. This framework provides a scaffold for developers to build client-side custom extensions which may include:

- Web Parts - functionality that can be added to a page. Web parts can also be extended as tabs in Microsoft Teams.
- Application Customizers - which are extensions that run on every page of a site and allow the developer to add visible or non-visible content to the page via the top or bottom placeholder
- Field Customizers - which allow the developer to build modified renderings of fields in a list.
- Command Sets - which extend the command surface in lists to provide custom actions.

### Subsite

A Site is a container that has lists, libraries, pages, apps, and sites (as children). A site that is a child of another site is a subsite.

Subsites tend to be less common on Modern SharePoint, as Microsoft recommend the use of Hub Sites to group together related sites.

## T

### Targeted Release

Targeted Release is an option to receive updates to the platform earlier than with Standard Release. Targeted Release should *not* be used in production tenants (you need to decide how you define this), as there are occasions where Target Release functionality is buggy or is withdrawn. Consider it similar to the old term "beta".

Targeted Release can be enabled in two ways: per tenant and per user. The two different ways of setting this preference result in different changes. Some updates only make sense in the context of a tenant (e.g., Communication sites) and others can make sense in the context of a person. Giving users Targeted Release does *not* mean they will see all updates sooner, only those which make sense in a person context.

Finally, once you have Targeted Release turned on, it is very hard to go back. Your users will be used to new functionality, and you would be removing it. Thus the warning above about not using Targeted Release in a production tenant is also relevant from a change management perspective..

### Taxonomy

### Team Site

Team Sites are generally used to facilitate teamwork. It generally has a set of people with permissions to work on content collaboratively, though not all people can create or edit content in all cases.

### Tenant

## U

### Unique Permissions

Unique Permissions do not [inherit](#Inheritance) default site permission levels and are applied to site Document Libraries, Lists, Site Pages etc.

### User experience (UX)

The user experience (UX) is how people react to and feel about the user interface as they use it. Web pages can be straightforward and easy to use (good UX) or complex and confusing (bad UX). Think of UX as the feelings and emotions people have about the solutions you give them as and after they use them.

### User interface (UI)

The user interface (UI) is what you see on the screen: the layout of the page, the controls you can use to accomplish things (like Web Parts), and where the text and images sit.

## V

### View

A View is a way to show data stored in a list or library. It consists of a set of columns that are shown, and a way to pre-filter and sort the information. A View can be considered as a rudimentary "Query" against a list that is used when visiting the list or library.

The most common settings we use in views allow us to:

- Choose which columns are displayed and in which order
- Filter the items based on the values in any of the columns
- Group items based on the value of most column types

### View Formatting

View Formatting is a SharePoint feature that allows users to customize the display of rows in Lists using JSON code. Like [Column Formatting](#Column-Formatting), colors, icons, images and other elements are used to highlight content and improve the user experience. 

## W

### Web Part

A web part is a consolidated piece of functionality that can be added one or more times to a page. Web parts can be first-party, those created and maintained by Microsoft or third-party being those created by developers in your own organization, the community via the PnP, or by a consulting service.

Also see [SharePoint Framework](#sharePoint-framework)

## X

## Y

## Z
