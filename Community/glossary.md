---
title: SharePoint Usage Glossary
ms.date: 9/2/2020
author: sympmarc
ms.reviewer:  Joanne Hendrickson
localization_priority: 
description: "SharePoint Usage Glossary"
ms.collection: SPCommunity
---

# Microsoft 365 Glossary

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

As with any technology, there are lots of terms we toss around to explain things. Just understanding what each term means can be half the battle. Whether you are entirely new to SharePoint or have been using it for a decade, there are always new terms to learn. The fact that Microsoft uses common English words for many capabilities can add an additional layer of confusion.

This Glossary is an attempt to demystify some of the terms and acronyms we use every day in working with the platform. See one missing? Feel free to add an Issue with what you want added.

[A](#a) [B](#b) [C](#c) [D](#d) [E](#e) [F](#f) [G](#g) [H](#h) [I](#i) [J](#j) [K](#k) [L](#l) [M](#m) [N](#n) [O](#o) [P](#p) [Q](#q) [R](#r) [S](#s) [T](#t) [U](#u) [V](#v) [W](#w) [X](#x) [Y](#y) [Z](#z)

## A

### App

An App is a term in SharePoint that means a packaged extension or customization that you can add to a site. An app can simply be a list that you add to a site to store information, or it can be a package that installs web parts that are available to use on pages, customizations that give you extra functionality within existing lists and libraries, or it could be an entire application that runs outside of SharePoint but has the ability to read and write back to your SharePoint site.

### Application Customizer

See [SharePoint Framework](#sharepoint-framework)

### Application Lifecycle Management (ALM)

Set of standards and processes to analyze, design, build, test and deploy a software solution. Modern ALM typically is an iterative process which allows for the incremental improvement and development and implementation of application features.

### Azure Information Protection (AIP)

A cloud solution that supports labeling of documents and emails to classify and protect information. Labeled items can be protected by encryption, marked with a watermark or restricted to specific actions or users and is bound to the item. This cloud based solution relies on Azure Rights Management Service (RMS) for enforcing restrictions.

## B

## C

### Camel Case

In programming, Camel case is the practice of naming variables or controls by capitalizing all words except the first, giving the name a look like a camel's hump. Examples: `iPad`, `intQuantity`, `myEmailAddress`.

See [Wikipedia](https://en.wikipedia.org/wiki/Camel_case). Also see [Pascal Case](#pascal-case)

### CAML (Collaborative Application Markup Language)

An XML fragment used by SharePoint to define the internal structure of sites, lists, fields, views and content types, declaratively, also used to query data in SharePoint lists to selectively retrieve data.

### Citizen Developer

A user whose job definition does not include any development activities and/or without formal software development training, but who nevertheless creates new business applications for consumption by others using development and runtime environments sanctioned by corporate IT.

### Classic SharePoint

Classic SharePoint refers to the user interface (UI) that was available starting in SharePoint 2013 - what you might think of as the blue and white UI. Classic SharePoint uses master pages and page layouts for content structuring. These capabilities were built on the .NET framework.

### Column Formatting

Column Formatting is a SharePoint feature that allows users to customize the display of fields in Document Libraries and Lists. Colors, icons, images and other elements are used to highlight content and improve the user experience. Links are used to make content actionable.

Some columns types, like Date and Choice, include ready made design templates. All column types allow for advanced formatting using JSON code.  

### Command Set

See [SharePoint Framework](#sharepoint-framework)

### Common Data Service

[Microsoft Common Data Service](https://powerplatform.microsoft.com/common-data-service/) is the premium data backbone that enables people to store their data in a scalable and secure environment dynamically. Common Data Service enables organizations to look at data as a service spun up on-demand to meet ever-changing business needs.

### Communication Site

A Communication Site is generally used to communicate from a smaller group to a larger group. For this reason, Communication Sites are often used in Intranets.

### Content Query Web Part

The Content Query Web Part (CQWP) is a web part available in Classic SharePoint that allows rolling up of content across lists and sub sites. The content returned is limited to only the site collection the web part is in. This web part has been replaced by the Highlighted Content web part in Modern SharePoint which gets around the site collection limitation.

### Crawled Property

A Crawled Property is one of the basic units of the Search Schema. They are created automatically by the SharePoint Search Indexer (or Crawler) when it is discovering content that can be searched. The information stored in Crawled Properties is made available in queries by mapping them to Managed Properties.

### Customization

Improving specific aspects of SharePoint functionality by changing settings through the end user interface. See also [SharePoint Framework](#sharepoint-framework)

## D

### Data Loss Prevention (DLP)

A set of policies for identifying, alerting and securing sensitive information types found in content across the Microsoft 365 platform.

### Disaster Recovery (DR)

The planning and practice of ensuring systems are available when a disaster occurs or that they can be restored as quickly as possible.

## E

### Enterprise Content Types

Content Types and Site Columns that are defined in the Content Type Hub, then published to all Site Collections in the tenant.

## F

### Farm

A set of on premises servers that hosts the SharePoint application, including SQL servers that host the SharePoint databases. A Farm can be single server or multi-tiered architecture containing multiple servers.

### Field Customizer

See [SharePoint Framework](#sharepoint-framework)

### First Release

Deprecated - please see [Targeted Release](#targeted-release).

## G

### Governance

The set of rules and practices which define how an organization chooses to build, publish, manage, and archive content and code in their environment. There is no one-size-fits-all approach, though there are often better practices to follow based on community experience.

### Group

A Group in SharePoint can generally refer to one of three things. It may mean:

#### SharePoint Group

  A container to organize users and other security groups. A SharePoint group can be assigned permission levels on an object such as a site, a list or library, a folder or a document (or page, or item). Generally only a Site Owner can manage who is in a SharePoint Group.

#### Microsoft 365 Group
  
A Microsoft 365 Groups is a concept which lets the members of the Group easily collaborate. It provides a collection of resources such as a shared Outlook mailbox including a shared calendar, a SharePoint [Team site](#team-site) with a document library and a Notebook, as well as a Planner Board, a Power BI workspace and a Stream Video portal.

A Group is the foundation of a Microsoft Teams Team. A Team gives users within that Group channels to collaborate in the context that is relevant to their work and the ability to have scheduled and ad-hoc meetings. Teams can be public (they can be accessed by everyone inside of the organization), private (users need to be invited explicitly) or org-wide (everyone in the organization is automatically a member of this team). Roles and permissions are simplified to Owner (create, delete, manage memberships), Member (collaborate, create channels and add tabs) and Guest. Guests are outside of the organization and need to be added explicitly as an External User, otherwise they can't see nor access a Team. They can only work in the structure provided to them, which means they can't add tabs, apps or channels.
  
#### Security Group

  A security group is a container of users defined in Active Directory, one or more of these can be added to SharePoint Groups. Adding users in the security groups applies permissions in SharePoint.

## H

### Highlighted Content Web Part

The Highlighted Content Web Part allows you to [roll up](#roll-up) content from allows you to specify content sources, sorting and filtering, and layout options.

As with all web parts in SharePoint, this we part will only display content which the current user has permission to see.

### Home Site

A Home Site is a special type of [Hub Site](#hub-site) with a few extra superpowers:

* The Home Site is the destination for the home icon in the SharePoint mobile app.

* The Home Site  provides an enterprise-wide search scope, making ALL content in your tenant findable.

Home sites are intended for use as the landing page for your organization. There is only one Home Site per tenant allowed.

### Hub Site

A Hub Site is a SharePoint site that can have other sites associated to it. This allows you to group sites by department, region, or project, etc. Features such as News, Events, and Highlighted Content can be used to produce rolled up views of content - like pages and documents from the associated sites - on a page on the Hub Site.

## I

### Idempotent

In a development sense, idempotent means that code you run more than once with the same inputs will always produce the same outputs. In other words, you can always expect the same effects, no matter how many times you do something.

### Inheritance

Inheritance refers to the cascading of default site permission levels (i.e. Owner, Member and Visitor) to site Document Libraries, Lists, Site Pages etc.

Inheritance can be "broken" to allow for [unique permissions](#unique-permissions).

## J

## K

### Known Folder Move (KFM)

Known Folder Move (KFM) allows you to automatically backup/redirect your Windows client's Desktops, Documents, and Pictures folders to OneDrive for Business. It gives you a transparent way to ensure your local files are never lost. Known Folder Move is now known as [OneDrive PC Folder Backup](#onedrive-pc-folder-backup).

## L

### Library

A library, typically used as a Document Library is a type of list where documents or other files are added as items, but no further file attachments can be added to the document item. Other files are added as separate entries in the library.

### Licensing

Microsoft 365 offers multiple licensing options (Kiosk, F1, E1, etc.), each of which turns on a different basket of capabilities for the user to whom the license is assigned.

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

### Multi-Factor Authentication (MFA)

Multi-factor authentication refer to an additional security layer beyond just username and password. One way it is described is the user name and password shows who you are based on something you **know**, and MFA shows who you are by something you **have**. The most common example of MFA is the code you get in a text on your phone when you are logging into sites like your bank or Github.

### Modern SharePoint

Modern SharePoint refers to the user interface (UI) that has been available in SharePoint Online to larger and larger degrees starting in about 2016. Some aspects of the modern UI are also available in SharePoint 2019 (on premises). Modern SharePoint does not use many of the underpinnings of classic SharePoint, such as master pages and page layouts. It is built using more current Web development tools and practices than classic SharePoint.

## N

### Namespace

A namespace refers to the conventions we use to determine major and minor names within a specific domain. For example, we need to use the /sites namespace carefully so we don't have collisions. If Harold Robinson wants to create a site at /sites/HRm, then Human Resources will have a problem.

In programming, namespaces can be far more complex - like List.Fields within Microsoft.SharePoint.Client - but we worry about namespacing in our day-to-day lives, too.  It wouldn't work very well if all our children were named Daryl.

## O

### On premises

On premises refers to running servers yourself, whether they are in your physical building, a data center where you rent space, or at a hosting company that runs servers specifically for you.

### OneDrive PC Folder Backup

This capability was originally called [Known Folder Move (KFM)](#known-folder-move-kfm). It allows you to automatically backup/redirect your Windows client's Desktops, Documents, and Pictures folders to OneDrive for Business. It gives you a transparent way to ensure your local files are never lost.

### Out of the box

Capabilities included with SharePoint without writing any code or doing heavy lifting. Depending on who you talk to, this definition probably includes a level of [customization](#customization) including things like creating new sites, lists, and libraries.

## P

### Pascal Case

In programming, Pascal case is the practice of naming variables or controls by capitalizing all words. Examples: `TotalQuantity`, `EmailAddress`, `ShippingPlant`.

See [Wikipedia](https://en.wikipedia.org/wiki/Camel_case). Also see [Camel Case](#camel-case)

### Patterns and Practices (PnP)

Patterns and Practices (PnP) is an open-source initiative coordinated by SharePoint engineering. This community controls SharePoint development documentation, samples, reusable controls, and other relevant open-source initiatives related to SharePoint development.

### Permission Level

A Permission Level is a set of specific permissions such as "Add an item" or "Edit Lists". SharePoint comes with a set of Permission Levels as standard, such as "Contribute" or "Design", which have different capabilities.

Custom Permission Levels can be created for business-specific scenarios, such as "Can add documents but not delete" by choosing the correct options, and applied to a User or Group.

### PnP

See [Patterns and Practices](#patterns-and-practices-pnp)

### Power Apps

PowerApps is a low-code/no-code development platform that provides a means for both Citizen Developers and Pro-Developers to build custom apps for your business needs.

Using PowerApps, you can quickly build custom business apps that connect to your business data stored either in the underlying data platform (Common Data Service) or in various online and on-premises data sources (SharePoint, Excel, Microsoft 365, Dynamics 365, SQL Server).

### Power Automate

Power Automate is a low-code/no-code workflow platform that helps you create automated workflows between your favorite apps and services to synchronize files, get notifications, collect data and more.

Power Automate provides a means to quickly automate your workflows, enable business logic to simplify app building, and model your processes across connected data sources and services.

### Power BI

Power BI is Microsoft's Business Intelligence and Reporting application. It allows you to connect and visualize any data using the unified, scalable platform for self-service and enterprise business intelligence (BI) that’s easy to use and helps you gain deeper data insight.

Power BI provides a simple, intuitive, easy to use experience for end users to create their own reports and dashboards.

### Power Platform Data Loss Prevention

A set of policies that can be applied to the Power Platform tenant or environment to prevent data leakage by grouping connectors deemed for business or personal use to be used together. Additionally, connectors can be blocked from any use and new connectors can be added by default to the business, personal, or blocked group as needed. Custom connectors can also be classified at the environment level.

### PowerShell

[PowerShell](https://docs.microsoft.com/windows-server/administration/windows-commands/powershell) is an automation scripting language from Microsoft, which was originally only available on Windows devices, and built on top of the .NET Framework. Since 2016, we also have [PowerShell Core](https://github.com/PowerShell/PowerShell) which is open-source, cross-platform, and built on top of .NET Core.

The version that ships on Windows devices is called Windows PowerShell, and the cross-platform version is called PowerShell Core, and is also available on Windows.

### Power Platform Environment

A Power Platform Environment is a container that administrators can use to manage apps, automations, connections, and other assets; along with permissions to allow organizational users to use the resources.

There are multiple types of environments that an organization can create (Developer, Sandbox, Production). The type indicates the purpose of the environment and determines its characteristics.

### Power Virtual Agents

Power Virtual Agents empowers organizations to create powerful bots using a guided, no-code graphical interface without the need for data scientists or developers.

Using Power Virtual Agents, you can:

* Empower your teams by allowing them to easily build bots themselves without needing intermediaries, or coding or AI expertise.
* Reduce costs by easily automating common inquiries and freeing human agent time to deal with more complex issues.
* Improve customer satisfaction by allowing customers to self-help and resolve issues quickly 24/7 using rich personalized bot conversations.

### Project Oakdale

[Project Oakdale](https://powerapps.microsoft.com/blog/introducing-microsoft-dataflex-a-new-low-code-data-platform-for-microsoft-teams/) is a built-in, low-code data platform for Microsoft Teams, and provides relational data storage, rich data types, enterprise grade governance, and one-click solution deployment for Power App solutions built for, and within Microsoft Teams.

Project Oakdale is built upon Common Data Service, and provides a 'lite' version equivalent, for free, under the existing licensing requirements of Microsoft 365.

## Q

## R

### Roll up

Rolling up content refer to the practice of consolidating a specific set of content from multiple locations. Common examples are:

* News from all sites associated with a [Hub Site](#hub-site)
* Events from all sites associated with a [Hub Site](#hub-site)

More complex roll ups are also possible using the [Highlighted Content Web Part](#highlighted-content-web-part) or custom code.

### Root Site

The base address in a web application or tenant for the first SharePoint Site collection. Typically, defined without use of managed paths ("/sites/" or "/teams/"), for example https://mytenant.sharepoint.com or http://sharepoint

## S

### Search Schema

The Search Schema refers to the customizable data dictionary used by SharePoint Search to allow users to query for and return specific information from SharePoint using the available Search tools, such as the Search Results web part in Classic SharePoint or the Search REST API.

### Sensitive information type

A defined pattern of data that can be identified in order to be protected by DLP or sensitivity labels. Common examples include social security numbers, credit card numbers but can also include any type of data considered sensitive by the organization that matches a pattern.

### Site

In modern SharePoint, a site refers to a modern site. (In classic SharePoint, the term was often used for both sites and sub-sites.)

To developers, a "Site" is a [Site Collection](#site-collection), whereas a "web" is a site. Confusing!

### SharePoint Home Page

Soon to be known as the SharePoint Start Page, this page (at /_layouts/15/sharepoint.aspx in your tenant) provides a personalized view of SharePoint based on who you are. You see:

* A rolled up collection of News based on the sites you are following

* Sites you are following

* Sites you frequently visit

* Sites you've visited recently

* Featured links, curated by your tenant admins

* Suggested sites based on your activity, powered by the Office Graph

### SharePoint Start Page

See [SharePoint Home Page](#sharepoint-home-page)

### Site Collection

A Site Collection is a group of websites that have the same owner and share administrative settings.

* In *SharePoint Online*, site collections are the top level available to admins, and visible in the SharePoint Admin Center under "Active Sites".
* In *SharePoint on-premises*, site collections are created within a Web Application, which is a level higher.

When you create a site collection, a top-level site is automatically created in the site collection (called root site). You can then create one or more sub-sites below the top-level site. The entire structure of the top-level site and all its sub-sites is called a site collection.

### Standard Release

Standard Release is an option to receive updates to the Microsoft 365 platform when they are broadly available to all customers. This is the default option for new tenants and can be modified later on.

As both Standard and [Targeted Release](#targeted-release) options can be applied to all or certain groups of users, it is a good practice to leave the majority of users in Standard Release and set the IT pros and power users in Targeted Release to evaluate new features and prepare teams to support business users and executives.

### Style Library

The Style Library is a document library in the Root Web of a SharePoint site that is used mainly in Classic SharePoint Sites. One of the purposes of this library is as a recognized "secure location" to store XSL Templates that are used by the Content Query Web Part (XSL templates outside of the Style Library cannot be used in Content Query Web Parts).

### SharePoint Framework

The SharePoint Framework (also known as SPFx) is a way for developers to extend SharePoint online, Microsoft Teams and in a slightly more limited way SharePoint 2019 and SharePoint 2016. This framework provides a scaffold for developers to build client-side custom extensions which may include:

* Web Parts - functionality that can be added to a page. Web parts can also be extended as tabs in Microsoft Teams.
* Application Customizers - which are extensions that run on every page of a site and allow the developer to add visible or non-visible content to the page via the top or bottom placeholder
* Field Customizers - which allow the developer to build modified renderings of fields in a list.
* Command Sets - which extend the command surface in lists to provide custom actions.

### Subsite

A Site is a container that has lists, libraries, pages, apps, and sites (as children). A site that is a child of another site is a subsite.

Subsites tend to be less common on Modern SharePoint, as Microsoft recommend the use of Hub Sites to group together related sites.

## T

### Targeted Release

Targeted Release is an option to receive updates to the platform earlier than with [Standard Release](#standard-release) Targeted Release should *not* be used in production tenants (you need to decide how you define this), as there are occasions where Target Release functionality is buggy or is withdrawn. Consider it similar to the old term "beta".

Targeted Release can be enabled in two ways: per tenant and per user. The two different ways of setting this preference result in different changes. Some updates only make sense in the context of a tenant (e.g., Communication sites) and others can make sense in the context of a person. Giving users Targeted Release does *not* mean they will see all updates sooner, only those which make sense in a person context.

Finally, once you have Targeted Release turned on, it is very hard to go back. Your users will be used to new functionality, and you would be removing it. Thus the warning above about not using Targeted Release in a production tenant is also relevant from a change management perspective..

### Taxonomy

### Team Site

Team Sites are generally used to facilitate teamwork. It generally has a set of people with permissions to work on content collaboratively, though not all people can create or edit content in all cases.

### Tenant

## U

### Unique Permissions

Unique Permissions do not [inherit](#inheritance) default site permission levels and are applied to site Document Libraries, Lists, Site Pages etc.

### User experience (UX)

The user experience (UX) is how people react to and feel about the user interface as they use it. Web pages can be straightforward and easy to use (good UX) or complex and confusing (bad UX). Think of UX as the feelings and emotions people have about the solutions you give them as and after they use them.

### User interface (UI)

The user interface (UI) is what you see on the screen: the layout of the page, the controls you can use to accomplish things (like Web Parts), and where the text and images sit.

## V

### View

A View is a way to show data stored in a list or library. It consists of a set of columns that are shown, and a way to pre-filter and sort the information. A View can be considered as a rudimentary "Query" against a list that is used when visiting the list or library.

The most common settings we use in views allow us to:

* Choose which columns are displayed and in which order
* Filter the items based on the values in any of the columns
* Group items based on the value of most column types

### View Formatting

View Formatting is a SharePoint feature that allows users to customize the display of rows in Lists using JSON code. Like [Column Formatting](#column-formatting), colors, icons, images and other elements are used to highlight content and improve the user experience.

## W

### Web Part

A web part is a consolidated piece of functionality that can be added one or more times to a page. Web parts can be first-party, those created and maintained by Microsoft or third-party being those created by developers in your own organization, the community via the PnP, or by a consulting service.

Also see [SharePoint Framework](#sharepoint-framework)

## X

## Y

## Z
