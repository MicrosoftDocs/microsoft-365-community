---
title: The Microsoft 365 Maturity Model – Customization and Development Competency
ms.date: 2/25/2021
author: simondoy
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: microsoft-365
localization_priority:
description: The Microsoft 365 Maturity Model - Customization and Development Competency
ms.collection: SPCommunity
---

# The Microsoft 365 Maturity Model - Customization and Development Competency

![Maturity Model for Microsoft 365](media/maturity-model-for-microsoft-365/M365MM.png)

## Overview of the Concepts [tl;dr]

Traditionally, there has been a reliance on 'deep' or 'pro' development to build business solutions. Any gaps in availability of these skills have commonly been filled by 'shadow IT' approaches and unmanaged applications.

Over the years as platforms have evolved, it became increasingly possible for viable business applications to be delivered without code. Today there is a continuum from out of the box, through configuration (No Code), to citizen developer (Low Code) and finally 'proper' development (Pro Code). The separation between these stages can be highly porous; artificially segregating them is frequently meaningless and often counter-productive. Management tools traditionally associated with Pro Code development are gradually providing an opportunity to wrap development rigor around the No Code and Low Code approaches and to introduce many of the effective development operations (DevOps) techniques and tools.

:::image type="content" source="media/microsoft365-maturity-model--customization-and-development/development-spectrum.png" alt-text="Development spectrum":::

At the same time, even nominally out-of-the-box products and services often support options for customization and extension. The ways of achieving this vary widely, including interaction via Application Programming Interfaces (APIs), 'overlay' coding of UI, deep configuration, Add-ins and more.

Increasingly, Machine Learning and AI based solutions operate in the same way as software solution development, also providing a continuous path through configuration, Low Code and Data Science driven professional development. As such, this competency applies equally to this technology

## Definition of this competency

This competency considers the management and governance processes required for different approaches to solution development and how to blend those different approaches effectively.

The concepts of customization and development have evolved over the lifespan of Microsoft 365 and the IT landscape in general. In the early days of SharePoint, for example, almost all organizations found themselves developing Pro Code solutions to make the platform work well for them. Fast forward to today, and Microsoft 365 offers a wide variety of apps and services that meet many needs right out of the box or with minimal configuration.

Our ability to extend the platform has changed significantly as well. Rather than writing code that is packaged and deployed to the server, almost all custom development for Microsoft 365 is done using client-side scripting, extensions via SaaS platforms like Microsoft Azure, or some combination. The SharePoint Framework (SPFx) allows us to build solutions for SharePoint, Microsoft Teams, Microsoft Outlook, and potentially other products in the future, potentially extending to other products in the Microsoft stack. Further the Office Add-In model also uses client-side scripting methods to extend Office applications. And finally, the Microsoft Graph gives us an API layer that exposes much of the Microsoft 365 landscape to help build robust and integrated solutions across the workloads.

These days, the question is as much *whether* to customize as it is *how* to customize. Custom coding absolutely has its place in Microsoft 365, but in many cases the platform provides robust tools which only require some configuration to meet your needs.

The reality is that there has always been a dynamic equilibrium between what can be delivered with different technologies by people with a range of skill sets. Perhaps unexpectedly, increasing maturity is less about a progression from Out-of-the-Box and No Code to Pro Code; it is more about how organizations coordinate and integrate this continuum.


## Evolution of this competency

### Level 100 - Initial

The customization and development continuum are poorly understood, unmanaged and chaotic. Staff are frustrated with poor functionality but have no mechanism for requesting or implementing change. Development is characterized by building in live without going through a release process where development is tested before being put live.

**[Initial level](microsoft365-maturity-model--intro.md#level-100---initial)** characteristics include:

#### 100 No Code

- Configurable platforms and products are generally used in their default state.
- There is little appreciation of the capabilities of platforms to meet business needs more closely.
- There is no systematic review of platform capabilities, feature road map or application of features sets to unaddressed business needs.

#### 100 Low Code

- Individuals use the skills and tools they have, developing solutions to local needs without oversight, review or recognition of the impact or interaction with wider strategic needs and activities.
- The solutions are not backed up, documented, publicized, or resilient.
- People creating solutions use hacks and inefficient approaches.
- Code is often copied from the Web with little understanding of its effects.
- No security or governance design or impact assessment.
- Solutions are not backed up in source control.
- Solutions are not documented.
- There is no formal support; the citizen developer may be unavailable to provide fixes, enhancements, or guidance.

#### 100 Pro Code

- Developers don't know the platform, so write code instead of using native features. (This is sometimes called the &quot;code first mentality&quot;.) Code is written to build components which reinvent the wheel due to lack of understanding of what is available out of the box with the platform.
- IT are insular and internally focused. There is little support for department or process driven needs.
- The IT function often has no development capability at all. Equally, IT may be inflexible in their approach, all developments are treated as 'enterprise-level' activities, making many solution-needs non-viable (too expensive, too slow, overly technical expectations from stakeholders).
- No development tools, such as source control and test methodologies are in use.
- Systems are developed which use Microsoft 365 services as a data store but the user interface is held outside of Microsoft 365.
- Systems are designed and built with little thought, on the Microsoft 365 services that can be glued together to deliver the system.

#### 100 Governance, Risk, Compliance and Security

- There are no agreed development platforms, tools, languages, etc.
- There is a lack of ownership of development on behalf of the organization.
- No standards have been considered or published. User Interfaces, branding, coding standards and quality, platforms and security are left to the knowledge and skill of staff members.
- There is no capture of development needs at a granular level and no visibility of (local) solutions that have been put in place.
- Teams and departments commission their own developments with third party contractors and developers, without procurement standards, contract reviews, or data and security agreements.
- No source control is used to hold the code repository.
- Development is frequently performed on the live environment, with no release management.
- Systems are delivered with no documentation of how they are administered or used (for example, User Guides and Admin Guides).
- There are no separate environments, such as Dev, QA, Production, so, changes are made to Production/Live. (With understanding, this may not be a bad thing; without understanding it is.)
- Systems that run in the organization are not known about by IT. These shadow systems are discovered when things go wrong.
- There is no DevOps process which takes the solution built by the developer for deployment in a controlled manner. DevOps
- Systems are built without thinking of how the system will be supported and maintained.

#### 100 Impacts

At this level you can expect the following:

- Inconsistent looking systems and solutions.
- The organization risks systems breaking due to misconfiguration and/or setup problems.
- The organization risks not being able to rebuild a solution if it is corrupted.
- Money is wasted on development when other approaches using low-code or no-code could be used to achieve similar results.

### Level 200 - Managed

Different types of development are recognized as occurring, but there are tensions between parts of the organization adopting different approaches. Shadow development continues to occur or is prohibited without providing alternatives.

Staff are frustrated with poor functionality but have no mechanism for requesting or implementing change.

Development is characterized by _build to live, though there may be some testing and control within that environment._

**[Managed level](microsoft365-maturity-model--intro.md#level-200---managed)** characteristics include:

#### 200 No Code

- Customized business solutions are developed using no-code technologies; however, these are done with limited knowledge of good practice. Solutions are modelled on existing practice, using superficial capabilities and generally avoid use of deeper platform features.
- Solutions tend to be built 'on the fly', without a clear deliverable and specification. There is no documentation around the design and build process.
- Users are shown how to use the system and core documentation may exist, within the process or procedure documents.
- Updates and changes are ad-hoc. There is no equivalent of source control.
- A small number of people have some expertise with configuring the platform. Maintenance and support of the solutions are dependent on the availability of these people. The 'experts' maintain their knowledge of platform capabilities, road map etc. out of personal interest.

#### 200 Low Code

- Some Power Platform projects have consistent color standards and make use of components.
- Some low-code solutions are exported to basic source control.
- Some low code solutions have separate environments for development, user acceptance testing, and production.
- There is some guidance on the decision to use low-code approaches and who to engage to do the development, for instance a citizen developer or an external partner.

#### 200 Pro Code

- Source Control is used for some projects. However, the source control system is not standardized across the organization. There are multiple repositories and multiple source control systems in use.
- Deployment processes are ad hoc and unreliable, frequently requiring roll back.
- Projects start to use Microsoft 365 design standards when delivering systems.
- Development approaches and best practice start to be understood and are adopted by members of the project team. However, they are not enforced.

#### 200 Governance, Risk, Compliance and Security

- Developers don't know the platform, so write code instead of using native features which often creates unnecessary technical debt and confusion.
- Some projects deliver systems with user guides and administration guides.
- Release Management is considered, and the delivery of a system and its upgrades are announced before deployment. However, there are no testing environments which the deployment is released to first.
- The organization's Microsoft 365 community start to share wins and stories via ad hoc discussions.
- There are no development standards shared between projects.
- Solutions are often developed, especially using no-code and low-code, without having a related plan for deployment, support and management and without assessment of impact on other processes and solutions.
- Basic Source Control maybe used, with multiple source control systems in use.
- Some projects make use of Cloud platforms such as Microsoft Azure.
- There are little in the way of DevOps Practices.

#### 200 Impacts

At this level you can expect the following:

- Money is wasted on development when other approaches using low-code or no-code could be used to achieve similar results.
- Inconsistent delivery approaches.
- The quality of developed solutions is low, and those solutions struggle for adoption.
- There are issues when deployments occur as deployments are not repeatable and cannot be practiced.

### Level 300 - Defined

There is an appreciation of the limits of the no-code approach, low-code and pro-code approaches and some effort to introduce standards, guidance, and collaboration to structure the co-existence of different approaches against different business needs. Attempts are made to bring all approaches under some form of oversight.

Staff are generally satisfied with functionality but struggle to consistently get non-critical feature gaps, inconsistencies and updates rolled out. Support is generally available.

**[Defined level](microsoft365-maturity-model--intro.md#level-300---defined)** characteristics include:

#### 300 No Code

- Steps to create customized business solutions are captured with some form of specification, setup is documented, and a final solution description exists.
- Developers are aware of and use some normal development methodologies or hybrids of them.
- Legacy approaches are modified to take advantage of platform capabilities and some business processes are actively redesigned to deliver improvement based on these.
- Updates and enhancement should be scheduled, planned, and executed, but exceptions to this are frequent.
- User documentation and training is appropriate to the system, though tends to lag updates. Documentation is still not seen as part of the deliverable.
- Solutions considered important to the business are recognized and some level of support has been implemented. Support staff are skilled up to maintain the platform and any solutions, reducing the reliance on 'solution experts'.
- There is some consolidation of no-code platforms; road maps and updates for standard platforms are actively tracked.
- Customization of live platforms is only carried out after consideration of impact on staff and other systems.

#### 300 Low Code

- Rigor is put in place around the documentation of low code solutions such as solutions built on the Power Platform.

- Low code solutions are backed up as solutions and stored in source control.
- Low code solutions have separate environments or equivalent for development, user acceptance testing, and production.

#### 300 Pro Code

- Source control is used for the majority of development projects.
- Systems are deployed mainly through manual processes but augmented with scripts for some of the steps.
- Solutions have separate environments or equivalent for development, user acceptance testing, and production.
- Continuous Integration and Continuous Deployment may be introduced alongside other approaches.
- Pro Code developers appreciate when not to develop solutions, only writing code when it is necessary and can make a difference. They begin to hand off to Low Code and configuration alternatives.

#### 300 Governance, Risk, Compliance and Security

- There is an appreciation of the limits of the no-code approach, low-code, and pro-code approaches. Needs that trigger a transition from one approach to another are often identified and options for delivering extended needs or features with pro code are understood. This is often based on business need with measurable return on investment.
- Good practice is understood by a core of experts and is used to guide solution development. There is a recognition of the roles of no-code and low-code alongside pro-code approaches. The 80/20 rule is increasingly applied, using out of the box functionality that is good enough to provide utility, often adapting a process to accommodate Out of the Box (OOTB) functionality rather than build customer solutions.
- Build is focused on solutions that represent the organization's &quot;special sauce&quot;, delivering the highest impact.
- There is understanding around technical debt and how to service it.
- Systems are delivered which are documented and can be managed, maintained, and supported.
- The pro development team and citizen developer community understand how to build solutions on the Microsoft 365 platform. Resources from Microsoft and the community are used to enhancing their knowledge. Pro developers and citizen developers support each other.
- Development at all levels starts to be underpinned by training and learning to improve skills. There may be formal certifications to support and demonstrate competence.
- Release Management processes are put in place but are manual.
- Standards for user interface (UI), themes and styling are created and shared. Design standards are published and allow a consistent approach for UI and functional behavior. Existing solutions may be updated in line with these.
- Source Control is standardized and used for Pro-code development but not for low code approaches.
- DevOps practices are being introduced, though non-Pro-code often are not included in these standards.
- User research employed to define requirements for some systems; there is some attempt to standardize approaches to capturing and defining requirements, such as user stories, etc.
- There is an emergence of a community of [M365 Champions](/microsoft-365/community/empowering-your-sharepoint-champions). This supports the need for governance, documentation, training, and development processes to support alignment of solutions to the strategic plan. Community members meet periodically to discuss problems citizen developers are trying to solve. These meet ups are part tech therapy and part continued training as Microsoft 365 is continually changing. There is management appreciation and support for these efforts.
- Separate environments or equivalent are available for Development, Test, and Production for Pro Code and, often to a limited extent, for other approaches.

#### 300 Impacts

At this level you can expect the following:

- Proponents of different development approaches show some appreciation for each other and openly discuss how to work together. Solutions emerge that combine customization, low code and pro code to create more capable, supportable solutions.
- Processes are introduced to encourage management, governance, and standardization, leading to easier development, adoption, and support.
- The organization has a forum for sharing systems and solutions that have been built.
- Improved release of systems as the structure, processes, and rigor for deployment is put in place, simplifying the IT estate, and reducing support burden and corporate risk.

### Level 400 - Predictable

There are clear processes and decision support for solution design and road-mapping consistent with business needs and impacts, encompassing the code-continuum. Standards exist, are functional, and reviewed and inconsistencies are actively eliminated. The portfolio of solutions is well understood and managed.

Staff are able to work efficiently across the spectrum of solutions and adopt new solutions readily due to their consistency and interoperability. Support-driven insights are used to proactively feedback to solution teams to drive improvements. Upcoming changes are communicated clearly and well in advance.

**[Predictable level](microsoft365-maturity-model--intro.md#level-400---predictable)** characteristics include:

#### 400 No Code

- Configurations are well documented and used as the basis for scripts and templates to automate site creation and updates. These are well managed and maintained via source control.
- Solutions are developed and tested against a set of good practice guidelines that include common layout based on good User Interface/User Experience (UI/UX) approaches, incorporating company branding and standards.
- No code developers have strong knowledge of the platform and are supported to maintain and extend their knowledge. They also know when to reach out for advice and guidance from colleagues with complementary development skills.
- Solution design and information architecture are carefully considered; constraints are understood and approaches to avoid these are implemented, including inclusion of or switch to low-code and pro-code development.
- Security, governance, management, and integration are considered as part of solution design and are included in the specification for important business solutions. These are therefore tested as part of the development lifecycle.
- The purpose, impact, and anticipated lifecycle and scale of the solution are considered, and appropriate development methodologies are applied accordingly.
- Solutions are reviewed to ensure they remain fit for purpose. Changes are managed appropriately.
- Changing platform capabilities are proactively applied to existing solutions.
- Important business solutions are actively managed and supported.
- The organization invests in a full range of platform skills against a broad development strategy that includes no-code, low code and pro-code standards and an integrated design and development approach.

#### 400 Low Code

- Solution design is carefully considered; constraints are understood and approaches to avoid or mitigate these are implemented.
- Low code solutions make use of source control to help manage the release process, where possible. The release process includes metrics which can be shared within the organization to show the benefit of the low code solutions.
- Low code solutions use metrics from tools such as Application Insights to measure adoption. This allows decisions to be made as to where to focus effort on successful applications and cancel or rework unsuccessful applications. These metrics are published and shared within the organization.
- There is an active process for testing and for user evaluation and feedback, which is used to drive a road map for ongoing enhancements.
- Lifecycle of the solutions is anticipated, and solution designs take this into consideration.
- Standardized User-Centric-Design processes ensure that the solution meets the needs of the users and is designed appropriately for the audience.
- The organization continues to invest in training for citizen developers and in the tools to support them.
- The organization has invested in the licensing to ensure that there is low friction and decisions are easier to make when building low code solutions.
- Pro code components are developed to extend low code solutions, as part of a well-understood, holistic 'systems' approach.
- Pro code methodologies are adopted wherever appropriate.

#### 400 Pro Code

- Pro code solutions make use of source control to help manage the release process. The release process includes metrics which be shared within the organization to show the benefit of the pro code solutions.
- Pro code solutions use metrics from tools such as Application Insights to show many users/applications are using them each day. This allows decisions to be made on the success of an application. A decision can be made as to which applications should be focused on. These metrics are shared within the organization.
- Low use solutions are regularly revisited to determine useful improvements to increase usage, where needed.
- Lessons learnt from the development of Pro code solutions are shared within the organization.
- APIs are proactively developed to allow No Code and Low Code to easily access sophisticated data sources, functions, and business automations.

#### 400 Governance, Risk, Compliance and Security

- Application usage is measured using tooling such as Application Insights.
- Applications are instrumented to detect errors and events using tools such as Application Insights.
- Development integration occurs across the code-continuum, pro code component, and solutions are built to be consumed by low code and no code solutions. Libraries of these 'extensions' and registers of where they are employed published and maintained.
- Statistics on the number of deployments and releases are provided by release management tools such as Azure DevOps.
- User research is employed to define requirements and provide metrics on usability, enhancements, and productivity.
- Design standards are applied consistently to ensure all applications meet staff expectations for UI and behavior.
- Source control is used effectively and consistently, some automated testing is in place.
- A Steering Committee is created to develop and oversee solution road maps.
- Code reviews occur to ensure code quality before being introduced into the codebase.

#### 400 Impacts

At this level you can expect the following:

- Higher quality applications and systems are delivered.
- Design standards mean that users can pick up the application more easily, boosting adoption.
- Applications meet the needs of their users due to the user centered design approach.

### Level 500 - Optimizing

Design decisions are routinely reviewed for effectiveness and learning is applied to continually refine and optimize solutions. Advanced tools are used to measure User Experience and solution efficacy and drive up the quality of all solutions. These are also used to proactively enhance standards and to help shape training of developers.

The effectiveness of solutions is continually assessed via a range of metrics to optimize staff productivity and to ensure agility for changing needs.

**[Optimizing level](microsoft365-maturity-model--intro.md#level-500---optimizing)** characteristics include:

#### 500 No Code

- The repository for customizations and templates which promotes solution reuse is actively maintained by the business and enhanced based on emerging technologies and business needs.
- Sophisticated no code solutions are easily created by extending them with low code and pro code extensions that operate in a similar way to the no code platform that staff are familiar with.
- Management processes actively look for opportunities to use no code to reduce costs and take advantage of platform feature roll out. The impact of these is assessed on an ongoing basis and used to refine the code transition points.

#### 500 Low Code

- The repository for components, modules and templates which promotes solution reuse is actively maintained by the business and enhanced based on emerging technologies and business needs.
- Low code citizen developers use the hooks and extension points built by the pro code developers, and provide enhancements to no code. These are standardized, with defined integration points and embedded monitoring elements.
- Compliance with standards is routinely assessed and used to improve the quality of the solution and the developer.

#### 500 Pro Code

- A Package Management feed (such as internal NuGet or NPM feed) is used for managing and promoting the reuse of components and patterns.
- Pro code develops extension points and components for no code/low code citizen developers to use. Examples include custom connectors for Power Platform or SPFx web parts for SharePoint and Teams.

Analytics on the use of APIs for data sources, functions and business automations is used to optimize their use and performance.

#### 500 Governance, Risk, Compliance and Security

- Development is proactively managed across the code-continuum; a dynamic equilibrium is maintained between the different code approaches, shifting to take advantage of changes in the technology and platform landscape. Active monitoring of the source technologies allows these changes to be anticipated and included in the development road maps.
- There is granular insight into the developed solution portfolio and code-continuum, with understanding of origination costs, technical debt, support costs, and benefits. These are integrated with user metrics. These are used to direct development strategies and investments.
- Application Insights metrics are used to measure adoption and are shared with the organization.
- Application Insights funnels and user flows are used to see how people are behaving and using the solutions.
- A/B Testing with usability metrics in place allow the organization to measure which approaches are best.
- Source control provides robust and highly automated testing, Continuous Integration / Continuous Delivery (CI/CD) techniques.
- A Centre of Excellence and Steering Committee is empowered to drive a road map to guide the extensibility points built with pro code for the no/Low code citizen developers.
- Solutions are designed and published to the organization's App Stores such as SharePoint and Microsoft Teams.

#### 500 Impacts

At this level you can expect the following:

- Innovation within the organization is actively supported with rapid deployment of tools that, in turn, improve the maturity of the new product, process, etc.
- An ability to rapidly develop solutions to new business needs at a pace that creates business advantage and then mature these to ensure compliance and supportability.
- A more productive workforce with users having the tools and information that they need when they need them.
- Seamless and invisible coordination of different approaches, leading to rapid staff adoption and improved productivity through consistency and standardization.
- Improved ROI as solutions can be reused throughout the organization.
- Promotion of best practice and lessons learned so the organization does not suffer the same problem time and time again.

## Scenarios

- Customer service representatives can easily answer common questions by customers, improving customer support and satisfaction.
- An electrical engineer can perform a site survey. They capture the required information with their mobile device so that the installation of the electricity point can be planned and executed successfully and minimize the cost.
- A salesperson can produce and send a quote to a customer in a consistent way which meets the quality standards of the organization.
- Employees can submit their ideas and suggestions to a panel via the corporate Intranet.
- A manufacturer can produce the required certificates and documentation to support the release of a new product in a managed way.
- Using Machine Learning to improve the efficiency in how a logistics company routes its delivery drivers.

### Cost &amp; benefit

When we talk about benefits of customization and development, it is easier to see the benefit and the ROI. Often only the time savings are used to quantify the ROI. When development enables a new capability within a business, the revenue that is realized with the new capability can drive previously unconsidered ROI.

Examples of benefit include:

- Reducing the time to achieve a common task.
- Reducing the error rate when copying information from one system to another system manually.
- Enabling insights to be gained by pulling data from one system and integrating it with another.
- Enhancing productivity by enabling the business to process more for less.
- Improving consistency when delivering content to customers.
- Enabling innovation within the organization.
- Increased employee satisfaction (employees get to work on the tasks that provide the most value that computers cannot deliver).
- Decreased &quot;time to productivity&quot; with new systems: reduced training costs and faster cycle times.
- Reducing corporate risk.

The cost of development is expensive and can be controlled by only embarking on projects that really need it and provide value. Additionally, moving development from pro code to low code when appropriate will help increase the value and innovation.

## Resources to Learn More

- Learn how to design awesome UIs by yourself using specific tactics explained from a developer's point-of-view: [Refactoring UI](https://refactoringui.com/)
- [Microsoft Developer Portal](https://developer.microsoft.com/)
- [Power Platform Centre of Excellence (CoE) Kit](/power-platform/guidance/coe/starter-kit)

## Conclusion

Customization and Development is an essential ingredient to get the most value from Microsoft 365. However, it is important that customization and development is not entered to lightly and there is an understanding of the commitment that is taken on. When customization and development is performed there will be a level of management and support required to ensure solutions continue to work as the platform evolves and unforeseen issues can be resolved.

Organizations should minimize customization and development unless it provides accompanying value. It should be used for essential business functions where the platform does not provide the required feature set. The activity should be measured and ensure that it provides significant return on investment.

Traditionally, organizations have treated no code and low code approaches as 'second class citizens' to pro code. In maturing organizations, however, each approach has a part to play, and the right blend can create an integrated approach to addressing business using a code-continuum. As silos and 'code-snobbery' are reduced, opportunities to improve standardization, development efficiency/assurance and to provide increased rapidity or cadence on delivery of solutions to the business improve.

When development is performed it needs to be done in a way which reduces the risk to the organization. So, implementing source code repositories to backup code and ensure that the developers are productive. This is important as too often there are stories where an organization has a solution which is used but they have lost the source code.

Customization and development can only contribute maximally to the organization if it is part of an overall view of organizational maturity which includes the other competencies as well. At the end of the day, technology is a set of tools, but people can use technology to accomplish their shared goals. Technology without focus on the people aspects rarely succeeds.

## Common Toolsets

- Artificial Intelligence / Machine Learning
- Azure DevOps
- Dataverse for Teams
- Microsoft Azure
- Microsoft Graph
- Microsoft PnP Frameworks
- Microsoft Teams App Source
- Power Platform
- SharePoint Framework (SPFx)
- Serverless Technologies

Customizable products and services

- Dynamics
- Microsoft 365 apps
- Microsoft Forms
- Microsoft Lists
- Microsoft Teams
- Outlook/Exchange Server
- Power BI
- Project
- SharePoint
- Visio

## Resources

[!INCLUDE [mm4m365-practitioners](includes/mm4m365-practitioners.md)]

---

**Principal authors**:

- [Simon Doy](https://www.linkedin.com/in/simondoy)
- [Simon Hudson, MVP](https://www.linkedin.com/in/simonjhudson/)

**Contributing authors**:

- [Emily Mancini, MVP, UXMC](https://www.linkedin.com/in/eemancini/)
- [Marc D Anderson, MVP](https://www.linkedin.com/in/marcanderson)
- [Sadie Van Buren](https://www.linkedin.com/in/sadalit/)

---

[!INCLUDE [mm4m365-core-team](includes/mm4m365-core-team.md)]
