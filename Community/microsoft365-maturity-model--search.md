---
title: Maturity Model for Microsoft 365 – Search Competency
ms.date: 9/3/2020
author: simonjhudson
ms.author: daisyfeller
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.service: microsoft-365
localization_priority:
description: Maturity Model for Microsoft 365 - Search Competency
ms.collection: M365Community
---

# Maturity Model for Microsoft 365 - Search Competency

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

![Image of the Maturity Model for Microsoft 365 logo.](media/maturity-model-for-microsoft-365/M365MM.png)

## Overview of the Concepts [tl;dr]

People search for many reasons. Any effective search strategy and supporting technology needs to reflect this and include a person-centric and organization-scoped approach to helping people find the things they need. Great search is about discovery, not the search experience itself, i.e., search is only as good as its results.

With modern organizations creating huge volumes of content and data every year, a search experience where users can find what they want, when they want is essential.

A good search experience benefits the organization by reducing time to find knowledge in the organization. This becomes particularly powerful when users do not need to know where the content is stored. It helps reduce &quot;re-inventing the wheel&quot; and content duplication because the originals could not be found.

## Definition of this competency

Search is about enabling people to find the authoritative information within the organization easily using a set of keywords or search terms, or based in their activities. The results may come from the Microsoft 365 platform or other systems which have been connected into the search process.


## Evolution of this competency

See the [Maturity Model for Microsoft 365 - Introduction](/microsoft-365/community/microsoft365-maturity-model--intro) for definitions of the Maturity Model levels.

People search for many reasons:

- They know something exists, but don't know where to find it
- They know something exists, but don't know how to describe it
- Search is the more efficient or rapid means of completing an activity
- They need to find if information exists or what information exists
- They need to find someone who can offer advice or skills
- They want to see what the organization has or knows

The evolution of Search starts from the basic 'index card' concept, which tells you where to find the document etc. you are looking for, epitomized by the Dewey Decimal system found in libraries. As technology developed, it become possible to search limited metadata (filename) in file repositories, then other attributes and eventually search engines were able to index contents (Semantic analysis), file properties and metadata/tags across multiple repositories. In parallel, the user experience of the search, especially for creating the query and presenting results has improved from basic or cluttered to strongly structured with previews and interaction points, plus post-search filtering or refinement. In parallel, the technologies have become aware of security and governance, reporting and feedback, content weighting and relevance (e.g. headings are more important than text), context, relevancy and 'freshness' (more recent content is likely to be more useful) and can deal with advanced content management technologies.

Search provides two 'experiences' within Microsoft 365 – [classic and modern](/sharepoint/differences-classic-modern-search) - both of which use the same Search Index.

- Classic search, which is configured via the SharePoint Admin Centre and available through SharePoint Online.
- Modern search, which is also known as Microsoft Search.

Microsoft Search has evolved through the improvement of the search indexing and categorization processes using Microsoft Graph, Artificial Intelligence, and Bing algorithms to build results which are personalized for each user. This enables more insightful results based on understanding of the context, where the search is performed and importance of the content.

Today we are moving into AI driven search which understands the person and provides very context specific results based on who they are, where they search from. This is supplemented by AI driven interfaces, including voice and image search. We can expect to see AI increasingly pervade search experiences combined with greatly enhanced personalization based on a wide range of context types.

Search relies heavily on several other competencies including Collaboration and Information Architecture which enables more mature search capabilities within the organization.

### Level 100 - Initial

**[Initial level](microsoft365-maturity-model--intro.md#level-100---initial)** characteristics include:

#### 100 Governance, Risk, Compliance & Security

- Out of the box search experience, the quality of results varies wildly with users often unable to find what they are looking without knowing the terms to search for.
- No formal process to curate search results or analyze search patterns.
- End users are often unaware of search and have had no training.
- The danger of search finding inappropriate content is not well understood.
- Search often does not respect user privileges and access rights.

#### 100 Technology

- Search may be restricted to File System search and a few specific applications.
- Default out of the box configuration is in place; often with very limited capabilities (filename, title, date).
- No customizations have been made to Microsoft Search.
- Search indexes a small volume of organization content.
- There is no customized search experience to support specific business requirements.
- No enhancements are made to the search experience to aid the user.
- Configuration of authoritative data sources have not been configured to help relevance ranking.

#### 100 User Experience

- The user experience is basic.
- User's may not always find content that they want without knowing the right search terms.
- User confusion with the different ways of searching.

- Search is scoped to the current application; there is no global search, the search experience, presentation, and features vary widely according to the current application. Many systems have no search capability at all.

- Users use search as a last resort after asking someone browsing and other forms of discovery.
- Search requires users to know how to ask the right question, possibly with very specific syntax, query structure and case sensitivity.
- Users turn to search by default because the information architecture (navigation, site topology, taxonomy, etc.) don't assist them to find relevant content.

#### 100 Impact

Users rarely rely on search; accessing known documents in known places (which are potentially superseded); they rely on browsing rather than search (failing to find the correct document); asking colleagues (consuming their time and attention) or creating new versions of content that already exists. Users frequently make copies of documents so that they 'know' where they are.

Most users turn to external search engines to search for information that probably exists in the organization.

In many instances Microsoft 365 usage is primarily focused on use of email. This content is unstructured, has minimal and frequently inaccurate document metadata beyond the filename and the content. User expectations are of a 'Google' search without context, scope, or organizational awareness.

At this level, the organization is using the out of box search experience which gives varied results and often leaves the user with difficulty finding the content that they are looking for. The search corpus is small with only a fraction of the organization's content being made searchable.

Users don't really trust search as they are unable to find the content that they are looking for, they find duplicate or out of date material and are not assured what they discover is authoritative. Worse, they may find the wrong content and consider it authoritative.

Some individuals are key knowledge sources, impeding their work and/or becoming 'single points of failure'.

Productivity is compromised; compliance activities are weak; organizational and colleague knowledge are poorly leveraged and there is a pervasive frustration at the inability to find things.

### Level 200 - Managed

**[Managed level](microsoft365-maturity-model--intro.md#level-200---managed)** characteristics include:

#### 200 Governance, Risk, Compliance & Security

- Some search tools respect user access rights, but inconsistencies exist, and inappropriate content may be surfaced.
- Some effort is made to promote or identify current or authoritative versions, but with limited consistency.
- Filenames are used as a substitute for metadata.
- There is no overall search governance and strategy plan.
- Users are not encouraged to use Search instead of legacy approaches.
- No role defined to administer and refine search experience.

#### 200 Technology

- There are some search-based point solutions which have enhanced configuration to improve user experience.
- Some custom specific organization search results have been configured.
- Microsoft Search may be enabled within Bing for Business, however most users bypass this and open other search engines.
- There are efforts to standardize search interfaces from system to system, however this tends to be limited to the presentation, not the format of the underlying business logic.
- Re-indexing is automated and typically occurs overnight. As such new content isn't initially findable.
- Different search syntax exists between applications.

#### 200 User Experience

- Users have basic awareness of search, do use it for some tasks and in some systems, but rely on other methods of finding the majority of what they need. Most users are unaware of advanced search features or even the availability of search in some applications.
- Results layouts are somewhat consistent but lack refinements and high value content is not promoted to the top of the results. Result layout and features do vary between applications.
- Search tools do find content; however, this can be slow.
- Some standardization is attempted for terms, metadata, naming conventions etc. However, this is not enforced and does not apply to legacy content.
- Users frequently cannot find the content they need and fall back to other methods to confirm that they are using the correct document etc.
- Some signposting is in place, i.e. there are visual or text devices to assist the user to navigate to the correct content or location.

#### 200 Impact

At this level, search usage is not ubiquitously or consistently present throughout the organization but is more popular as employees see the benefits of being able to find content. However, the search experience differs depending on where the search takes place. There may have been the migration of file content from file servers into SharePoint; it becomes possible to search across all content stored in platforms, such as Microsoft 365.

There is an increase in usage of search in general, as users find out more about the benefits of search within the organization. Users begin using search when they don't know where a specific document or item is, however, differences between search experiences confuses staff and they avoid using search in systems they are less familiar with. Colleagues remain a primary source of information or signposting to where to look. Lack of immediacy in search ensures duplicate creation remains commonplace, especially across different teams.

Productivity and compliance remain compromised; and frustration at the inability to find things persists.

### Level 300 - Defined

**[Defined level](microsoft365-maturity-model--intro.md#level-300---defined)** characteristics include:

#### 300 Governance, Risk, Compliance & Security

- User access rights are consistently applied, and processes exist to manage access.

#### 300 Technology

- Commonly searched keywords are configured with tailored results.
- An enterprise search exists that is connected to other file repositories and line of business applications to break down information silos and allow search across the enterprise. (This could be hybrid, Salesforce etc.). This may not be consistently available nor address all the needs of users, however.
- Search is applied consistently across services.
- 'Search verticals', which provide scopes focused on specific topics, business functions, file types and more are available, specific to the business and aim to improve precision and findability for key business functions.
- Search results are customized for key organization assets to improve findability and discovery of useful assets.
- Search is used in business applications to access large volumes of content quickly and efficiently. This gives users access to information in a way that they have not had before.
- The business is using modern search web parts to enhance the user interface and search experience.
- People are understood as information assets. Skills and expertise are captured and returned in response to search queries.

#### 300 User Experience

- Users are educated on search and how to make best use of it.
- Search boxes are presented consistently and provide guidance.
- Search results are consistently laid out and provide content summaries and previews.

#### 300 Impact

Search actively adds value to organizations, releasing staff time, improving compliance, and creating confidence that correct versions of documents, etc. are in use. Staff can locate some physical assets, skills.

At this level, Search becomes an asset to the organization. This has been recognized as an enabler that develops more efficient and effective employees. The capabilities of search are harnessed to improve the experience of businesses applications.

### Level 400 - Predictable

**[Predictable level](microsoft365-maturity-model--intro.md#level-400---predictable)** characteristics include:

#### 400 Governance, Risk, Compliance & Security

- A role exists in the organization to manage enterprise search, to review keywords, feedback and search metrics with a view to ensuring effectiveness.
- Processes are in place to ensure staff maintain their profiles, including skills and expertise.

- Search is used to identify records and other artifacts that should be tagged.
- Centrally managed thesauri and term sets are used across search scopes that understand synonyms.
- Search is be used to assist compliance processes such as subject access request and, legal eDiscovery.
- There are tools and processes to ensure staff maintain their profiles and update content to improve findability.

#### 400 Technology

- Search usage is analyzed and used to improve search results.
- Contextual search is embedded in line of business systems.
- Most systems and workplace tools provide consistent access to the enterprise search.
- Information is stored in such a way as to enhance findability.
- Search extends beyond files and information to locations, physical assets, relationships and more.
- Content discovery emerges as a business tool that exposes content to users who might not have known about it, by displaying information related to the search items.
- Prospective search is used to display content without the need to enter a search term, such as commonly viewed news, article documents; context drives the relevancy of this.
- Predictive search begins suggesting matches to search terms as the user enters the search query.
- Advanced queries can be created using a defined query language.
- Frequency of content indexing is appropriate to the periodicity (&quot;freshness&quot;) of change of different repositories and business processes.

#### 400 User Experience

- Users are skilled at discovery of content, information, and skills across the organization.
- Search results provide previews across most content types; offer interaction (such as email, save for later), and display useful information dependent on content.
- Users can access search from most applications and elements of their digital workspace, including mobile.
- Common queries can be saved by users and notifications relating to new results are possible.
- Recommended content and [common bookmarks](/microsoftsearch/manage-bookmarks) to standard or 'best bet' results are proactively published by the organization.
- Users are frequently unaware that search is used to retrieve information within their workspace.
- External and public domain content is included in content activities, such as finding appropriate images.

#### 400 Impact

This level sees Search being managed throughout the organization. Processes are in place to add new content, search verticals and search result layouts and Microsoft Search configuration.

Search is a key business information tool that enables most processes. It is widely seen as the most effective means of discovering, retrieving, and confirming business information, for identifying skills and expertise across the business and integrating knowledge from multiple systems. Most staff update profiles and participate in appropriate tagging

Search results can be relied on; the current versions are reliably returned; inappropriate or incorrect content is rare.

### Level 500 - Optimizing

**[Optimizing level](microsoft365-maturity-model--intro.md#level-500---optimizing)** characteristics include:

Search is part of everyday life for an employee at the organization. New innovative ways of exposing content are investigated. Search metrics are used to analyze user behavior and understand gaps in the information that is being returned.

#### 500 Governance, Risk, Compliance & Security

- The organization seeks to continually enhance all aspects of the search process and experience; extending scopes, optimizing results and linking related information based on continual feedback
- Advanced analytics are used to understand search usage and this provides further insights into activities across the company
- Search is actively used to identify potential threats to information governance, security and legal obligations.
- Automated tagging and other metadata are in use
- Context (staff profiles, locations etc.) is integrated with source processes such as Joiners-Leavers, in order to maintain high quality of data

#### 500 Technology

- The search corpus is broadened with search being available across bespoke and line of business systems.
- The search corpus is used to enhance knowledge management tools such as Project Cortex.
- Opportunities to enhance search are looked for to ensure data is surfaced to improve productivity based on effective analysis.
- Effective search is ubiquitous and uniformly available across desktop, mobile and other experiences.
- External resources are included in the search scope.
- Staff profile updates are monitored and automated to ensure accuracy and completeness.
- Search is used to discover and auto-tag content.
- Users are highly skilled at finding information using tools and new staff are trained in the tools for their role.
- Automated classifiers are used to add tags to all content types, including image, audio and video, in order to ensure it is discoverable.
- SEO approaches are applied to content.

#### 500 User Experience

- Custom Search Results are created to augment key information in the search results to support improved discovery and findability. These are monitored and a process exists for updating search scopes, presentation, filters etc. as the business needs evolve.
- Search is ubiquitous; users can access search consistently from all applications and locations within their digital workspace, including mobile and voice.
- Users can proactively provide feedback on search results, to drive improvements.
- AI is used to enhance search based on deeper knowledge of the user context and business activity.
- Search experiences are embedded in business processes and in many cases, users aren't even aware that search is supporting their work.

#### 500 Impact

Search technologies are considered critical business systems, carefully managed with designed-in resilience. They are a key tool for ensuring compliance; it also unpins staff and process effectiveness.

Staff are committed to the content processes that maintain search; at the same time search is highly automated and 'invisible' delivering insights and finding knowledge without user input. Search itself provides management key insights into the health, activities, and productivity of the business.

## Scenarios

- A project manager looking for similar projects to the one that they are just about to start and then needing to recruit an appropriately skilled team.
- A salesperson searches for similar proposals to use when creating a new proposal.
- A junior member of staff needing to find the company tax number.
- Staff searching for internal and market news relating to an insight or innovation they are considering. An engineer researching a solution to a manufacturing failure, who needs to collate procedure, machine manuals, line SPC data and actions alongside reports of similar events outside the company.
- The legal team finds contracts which will expire soon and can work on renewals where appropriate.

### Cost & benefit

The following benefits can be achieved as the Search Competency increases in maturity:

- Reduced user frustration when trying to find content they know is available.
- Reduced time wastage finding information or the right person ([commonly upwards of 20 minutes per person per day at level 100](https://www.cottrillresearch.com/various-survey-statistics-workers-spend-too-much-time-searching-for-information/)
- Increased innovation.
- Increased awareness of useful information and knowledge. Improvement in employee engagement.
- Increased sharing of knowledge and best practice.
- Decentralized management of content but with centralized consumption.

A modern Search experience is part of a modern digital workspace which can attract the right workforce.

Benefits are found in sharing stories, knowledge and understanding but are difficult to quantify and measure.

## Resources to learn more

- [Classic vs Modern Microsoft Search](/sharepoint/differences-classic-modern-search)
- [Building Custom Microsoft Search Connectors](https://github.com/microsoftgraph/msgraph-search-connector-sample/tree/master/PartsInventoryConnector)
- [Search bookmarks](/microsoftsearch/manage-bookmarks)
- [Creating custom search results pages in SharePoint Online](https://techcommunity.microsoft.com/t5/microsoft-search-blog/creating-custom-search-results-pages-in-sharepoint-online/ba-p/1141515)

## Conclusion

Organizations that implement a successful Search strategy will see direct impacts to the bottom line. Employees being able to &quot;discover&quot; information which leads to innovation within the organization, reduced costs and time efficiencies can have a huge impact on worker productivity. The cost benefit in users not duplicating work and finding corporate knowledge are difficult to quantity but exist.

Search enhances the other competencies and is a great way to begin reaping rewards from the Microsoft 365 platform.

Organizations should capture success stories to provide examples of the benefits to ensure that this essential service gets the attention and resources that is required for it to be a successful resource.

## Common Microsoft 365 Search technologies

- Microsoft Search (using Microsoft Graph)
  - Office search
  - Microsoft Search in Bing
  - SharePoint Modern Search
  - Modern Search Web Parts
  - Delve
  - Search Connectors
- Bing
- SharePoint Search
  - Classic/Enterprise Search
- SQL Search
- Business Data Services (BDS)
- Cortana
- Power BI Q&A
- Managed Metadata/Term Stores
- eDiscovery and audit (Compliance Centre)
- 
## Resources

[!INCLUDE [mm4m365-practitioners](includes/mm4m365-practitioners.md)]

---

**Principal authors**:

- [Simon Doy](https://www.linkedin.com/in/simondoy)
- [Simon Hudson, MVP](https://www.linkedin.com/in/simonjhudson)

**Contributing authors**:

- [Marc D Anderson, MVP](https://www.linkedin.com/in/marcanderson)
- [Emily Mancini, MVP, UXMC](https://www.linkedin.com/in/eemancini)
- [Sadie Van Buren](https://www.linkedin.com/in/sadalit)

---

[!INCLUDE [mm4m365-core-team](includes/mm4m365-core-team.md)]
