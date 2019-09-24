# SharePoint Usage Glossary

As with any technology, there are lots of terms we toss around to explain things. Just understanding what each term means can be half the battle. Whether you are entirely new to SharePoint or have been using it for a decade, there are always new terms to learn. The fact that Microsoft uses common English words for many capabilities can add an additional layer of confusion.

This Glossary is an attempt to demystify some of the terms and acronyms we use every day in working with the platform. See one missing? Feel free to add an Issue with what you want added.

[A](#A) [B](#B) [C](#C) [D](#D) [E](#E) [F](#F) [G](#G) [H](#H) [I](#I) [J](#K) [K](#K) [L](#L) [M](#M) [N](#N) [O](#O) [P](#P) [Q](#Q) [R](#R) [S](#S) [T](#T) [U](#U) [V](#V) [W](#W) [X](#X) [Y](#Y) [Z](#Z)

## <a name="A"></a>A

### App

An App is a term in SharePoint that means a packaged extension or customization that you can add to a site. An app can simply be a list that you add to a site to store information, or it can be a package that installs web parts that are available to use on pages, customizations that give you extra functionality within existing lists and libraries, or it could be an entire application that runs outside of SharePoint but has the ability to read and write back to your SharePoint site.

## <a name="B"></a>B

## <a name="C"></a>C

### Classic SharePoint

Classic SharePoint refers to the user interface (UI) that was available starting in SharePoint 2013 - what you might think of as the blue and white UI. Classic SharePoint uses master pages and page layouts for content structuring. These capabilities were built on the .NET framework.

### Communication Site

A Communication Site is generally used to communicate from a smaller group to a larger group. For this reason, Communication Sites are often used in Intranets.

### Content Query Web Part

The Content Query Web Part (CQWP) is a web part available in Classic SharePoint that allows rolling up of content across lists and sub sites. The content returned is limited to only the site collection the web part is in. This web part has been replaced by the Highlighted Content web part in Modern SharePoint which gets around the site collection limitation.

### Crawled Property

A Crawled Property is one of the basic units of the Search Schema. They are created automatically by the SharePoint Search Indexer (or Crawler) when it is discovering content that can be searched. The information stored in Crawled Properties is made available in queries by mapping them to Managed Properties.

### <a name="Customization"></a>Customization

Improving specific aspects of SharePoint functionality by changing settings through the end user interface.

## <a name="D"></a>D

## <a name="E"></a>E

## <a name="F"></a>F

### Farm

### First Release

Deprecated - please see [Targeted Release](#TargetedRelease).

## <a name="G"></a>G

### Governance

### Group

A Group in SharePoint can generally refer to one of two things. It may mean:

- Security Group

  - A container to organize users and other groups. A security group can be assigned permission levels on an object such as a site, a library or library, a folder or a document (or page, or item). Generally only a Site Owner can manage who is in a Security Group.

- Office Group

  - An Office 365 Group is a concept within Office 365 that allows users can be members of, which has it's own e-mail address, and can be associated to a Microsoft Teams team, or a SharePoint Site. A Microsoft Teams Team automatically creates an Office 365 Group. These can be public where anyone can join, or Private when you need to be invited or given a code to join. Permissions are simplified to only "Owners" or "Members".

## <a name="H"></a>H

### Hub Site

A Hub Site is a SharePoint site that can have other sites associated to it. This allows you to group sites by department, region, or project etc. Features such as News and Highlight Content can be used to produce a roll up view of content like pages and documents from the associated sites on a page on the Hub Site.


## <a name="I"></a>I

## <a name="J"></a>J

## <a name="K"></a>K

### Known Folder Move (KFM)

Known Folder Move (KFM) allows you to automatically backup/redirect your Windows client's Desktops, Documents, and Pictures folders to OneDrive for Business. It gives you a transparent way to ensure your local files are never lost.

## <a name="L"></a>L

### Library

A library, typically used as a Document Library is a type of list where documents or other files are added as items, but no further file attachments can be added to the document item. Other files are added as separate entries in the library.

### Licensing

Office 365 offers multiple licensing options (Kiosk, F1, E1, etc.), each of which turns on a different basket of capabilities for the user to whom the license is assigned.

### List

A List in SharePoint is a table used to store information in a SharePoint site. A list has columns that can be used to store differen types of information, and each row in a list is known as an "Item". SharePoint attempts you to very carefully design lists if you attempt to store "large" amounts of data (more than 5,000 items), including things like limiting the number of "Lookup Columns" that can be used. Therefore, if you are planning on storing more than a few thousand items, be sure to follow Microsoft guidelines on storing large amounts of data in lists.

An item in a list can have multiple file attachments added. This is useful if you use a custom list as an Issue Tracker for example, and want to be able to add screenshots to an item in.

A library is a type of list where documents or other files are added as items, but no further file attachments can be added.

## <a name="M"></a>M

### Managed Metadata

Managed Metadata is a SharePoint feature that allows the business to create a hierarchy of terms that can be used in SharePoint Sites to tag content. This is used by creating the hierarchy using Term Groups and Term Sets, then adding a column to a list of type "Managed Metadata" and setting the Term Set to use for tagging. When an item is added to that list or library, the new column is used to tag that item or document.

### Managed Property

A Managed Property is one of the basic units of the SharePoint Search Schema. It's an entry in the Schema that you refer to when doing search queries that use specific properties, or when specifying which information you want to return.

Managed Properties can be created (if you have the appropriate permissions), although SharePoint automatically creates Managed Properties that are useful for a wide range of scenarios.

### Modern SharePoint

Modern SharePoint refers to the user interface (UI) that has been available in SharePoint Online to larger and larger degrees starting in about 2016. Some aspects of the modern UI are also available in SharePoint 2019 (on premises). Modern SharePoint does not use many of the underpinnings of classic SharePoint, such as master pages and page layouts. It is built using more current Web development tools and practices than classic SharePoint.

## <a name="N"></a>N

## <a name="O"></a>O

### On premises

On premises refers to running servers yourself, whether they are in your physical building, a data center where you rent space, or at a hosting company that runs servers specifically for you.

## <a name="P"></a>P

### Permission Level

A Permission Level is a set of specific permissions such as "Add an item" or "Edit Lists". SharePoint comes with a set of Permission Levels as standard, such as "Contribute" or "Design", which have different capabilities.

Custom Permission Levels can be created for business-specific scenarios, such as "Can add documents but not delete" by choosing the correct options, and applied to a User or Group.

## <a name="Q"></a>Q

### Out of the box

Capabilities included with SharePoint without writing any code or doing heavy lifting. Depending on who you talk to, this definition probably includes a level of [customization](#Customization) including things like creating new sites, lists, and libraries.

## <a name="R"></a>R

### Roll up

### Root Site

## <a name="S"></a>S

### Search Schema

The Search Schema refers to the customizable data dictionary used by SharePoint Search to allow users to query for and return specific information from SharePoint using the available Search tools, such as the Search Results web part in Classic SharePoint or the Search REST API.

### Site

### Site Collection

### Standard Release

### Style Library

The Style Library is a document library in the Root Web of a SharePoint site that is used mainly in Classic SharePoint Sites. One of the purposes of this library is as a recognized "secure location" to store XSL Templates that are used by the Content Query Web Part (XSL templates outside of the Style Library cannot be used in Content Query Web Parts).

### Subsite

A Site is a container that has lists, libraries, pages, apps, and sites (as children). A site that is a child of another site is a subsite.

Subsites tend to be less common on Modern SharePoint, as Microsoft recommend the use of Hub Sites to group together related sites.

## <a name="T"></a>T

### <a name="TargetedRelease"></a>Targeted Release

### Taxonomy

### Team Site

Team Sites are generally used to facilitate teamwork. It generally has a set of people with permissions to work on content collaboratively, though not all people can create or edit content in all cases.

### Tenant

## <a name="U"></a>U

### User experience (UX)

The user experience (UX) is how people react to and feel about the user interface as they use it. Web pages can be straightforward and easy to use (good UX) or complex and confusing (bad UX). Think of UX as the feelings and emotions people have about the solutions you give them as and after they use them.

### User interface (UI)

The user interface (UI) is what you see on the screen: the layout of the page, the controls you can use to accomplish things (like Web Parts), and where the text and images sit.

## <a name="V"></a>V

### View

A View is a way to show data stored in a list or library. It consists of a set of columns that are shown, and a way to pre-filter and sort the information. A View can be considered as a rudimentary "Query" against a list that is used when visiting the list or library.

The most common settings we use in views allow us to:

- Choose which columns are displayed and in which order
- Filter the items based on the values in any of the columns
- Group items based on the value of most column types

## <a name="W"></a>W

## <a name="X"></a>X

## <a name="Y"></a>Y

## <a name="Z"></a>Z
