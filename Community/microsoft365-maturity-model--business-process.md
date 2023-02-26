---
title: Maturity Model for Microsoft 365 – Business Process Competency
ms.date: 9/9/2020
author: sadalit
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: microsoft-365
localization_priority:
description: Maturity Model for Microsoft 365 - Business Process Competency
ms.collection: SPCommunity
---

# Maturity Model for Microsoft 365 - Business Process Competency

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

![Maturity Model for Microsoft 365](media/maturity-model-for-microsoft-365/M365MM.png)

## Overview of the Concepts [tl;dr]

The Business Process competency focuses on how users in an organization perform repetitive tasks in a systematic way, with structure provided by business rules. While there are many business processes that do not require automation or have not been technology-enabled, technology can make existing processes more efficient or allow operations that would not otherwise be possible or effective. The most valuable attributes for a well-running business process are repeatability, speed, standardization, compliance, reliability, measurability, and efficiency. Agility, flexibility, and auditability are also commonly involved, alongside human dimensions such as user experience and user interface. Business integration and whole-system thinking also play an important role.

## Definition of this competency

"Business Process" describes linked business activities with a defined trigger and outcomes, frequently standardized by a technology platform and/or custom automated workflow processes. Areas of focus include data (unstructured/structured), workflow, user security / roles, analytics and reporting, tracking / auditing, process modeling and simulation, and process optimization.

## Evolution of this competency

See the [Maturity Model for Microsoft 365 - Introduction](microsoft365-maturity-model--intro.md) for definitions of the Maturity Model levels.

### Level 100 - Initial

Organizations at this level are running their business processes in a manual, ad-hoc, "just do what it takes to get it done" manner. Their systems are not supporting them because there has been no investment in automation. There is widespread frustration and a sense that "we could be doing better" but there is no particular group or individual (e.g., certified Continuous Process Improvement expert) leading the charge to use technology to make improvements.

**[Initial level](microsoft365-maturity-model--intro.md#level-100---initial)** characteristics include:

#### General

- Business processes are undefined or only loosely defined through user experience.
- There may be no use of process technology, instead relying on paper-based process and legacy technology such as email for notifications, hand-offs and approvals.
- Users of the system rely on institutional knowledge to get things done ("I know who can help me with this") rather than agreed-upon roles and business logic.
- Exceptions cause long delays (e.g., a key resource is out of the office, or the first time a new situation is encountered there is no method for defining what should happen).

#### Governance, Risk, Compliance and Security

- Processes are mostly undocumented and lack any form of governance, control or oversight such as an Integrated Project Team (IPT).
- Tracking of the state of the process or status of an activity within a process is not possible or not done. Reporting or analytics are absent.

#### Business Process

- Changes to the process are untested or tested in concept only.
- Exceptions and failures are not captured, tracked and addressed
- Processes have evolved from prior approaches. New needs and exceptions have been bolted on rather than engineered in.

#### Level 100 Impacts

At this level you can expect the following:

#### General

- If there is a known workflow, e.g., for request approvals, there can be long delays between steps because there are no system notifications, no status updates, and no consequences for inaction. This requires the requestor to chase down the person at the next step in the process.
- Transactions are very costly in terms of time spent and user frustration.
- Staff (and clients / customers) have limited confidence in the quality or timeliness of the process output.
- The team loses credibility and will be hard to get future buy in of new processes.
- Exceptions and priorities, troubleshooting and remedial intervention become a drain on resources and pose a risk to business outcomes.
- Basic questions can't be answered because there is no reliable data (e.g., "How long does it take us to process a typical invoice?")
- People feel stressed due to the lack of ability to plan and estimate how long a process will take.
- Deadlines are missed or require heroic effort to meet due to lack of transparency in business process.

#### Governance, Risk, Compliance and Security

- Compliance issues are a risk when processes are not done according to established business rules.

#### Business Process

- It's not possible for anyone to see the status of a particular request. Activities can stall or remain incomplete indefinitely.
- Activity owners invest their time in pushing activities through the process. Activity prioritization is ad hoc and not driven by business priority or objective value/risk

### Level 200 - Managed

Organizations at this level are evaluating or implementing technology to help automate some of their processes in a standardized way. As a result, some lines of business may be mapping their processes for the first time, and gaining a true sense of all the steps, dependencies, exceptions, and delays. There is momentum to manage particular processes based on business need and/or process owner enthusiasm. An understanding of the benefits of automation is developing. A particular line of business or department may have successfully leveraged technologies to manage processes and are evangelizing this to other departments.

**[Managed level](microsoft365-maturity-model--intro.md#level-200---managed)** characteristics include:

#### General

#### Governance, Risk, Compliance and Security

#### Business Process

- Business processes are documented / defined at the department level and communicated to the organization. Process maps exist for many processes but adopted technology solutions are weakly documented.
- Out of the box SharePoint workflows (approval, collect feedback) might be leveraged sporadically.
- A document library or list provides a central base of operations.
- Workflows tend to be document-centric or task-centric vs. application-centric.
- There is an understanding of the functionality within M365 to support business process automation.
- Some "no-code" workflows (e.g., Power Automate) may be implemented to handle simple business rules at the department level (decision-based routing).
- There may be inconsistency between the documented process and the deployed process, as individuals hold to the way they traditionally completed workflow tasks.
- Many processes are built solely at the role or department level, by citizen developers in response to business needs. They do not go through formal application development cycles and the development itself is undocumented (though the process may be)
- Processes lack governance, oversight, testing and control. Changes and improvements are ad hoc or responsive.
- There is some attempt to use feedback to enhance the process, though this lacks formality rigor or commitment.
- Business ownership to maintain the processes is not consistent; changes in business need may not be effectively reflected in the process.
- Business processes exist in isolation; typically solving point problems without integrating with a larger strategy.
- Reporting and tracking of activity through the process is attempted, but not always reliable or reflective of the business needs and often incurs further manual effort.
- Process development is not effectively coupled to process re-engineering, leading to faster/better completion of the process rather than creation of better processes.
- No strategy around automation, including standardization of technology platform and approach has been developed. Automation tasks are approached in different ways.
- There is often inconsistency between the documented process and the deployed process.

#### Level 200 Impacts

At this level you can expect the following:

- One department may have automated workflows while the rest do not, which creates an inconsistent experience for internal customers.
- A process may be automated in one geographic location but not in others, even within the same line of business.
- Single points of failure exist within the technology and within the expertise to maintain or improve it
- There is often disagreement or conflict between a company-wide approach vs. embedded capabilities in line of business systems

### Level 300 - Defined

Organizations at this level are using M365 to manage business process across multiple lines of business, and consistently across locations.

**[Defined level](microsoft365-maturity-model--intro.md#level-300---defined)** characteristics include:

#### General

- Individuals have transitioned from procedural document workflow to orchestration of dynamic business process.
- A business process automation technology platform has been selected and is the basis for new Business Process activities, though legacy solutions remain in use. Third party tools and/or custom Business Process Management tools are integrated to support more complex business rules and legacy systems.
- The organization has begun to develop business process skills, often in a central team and including process re-engineering and technical platform specialists. Training is available to both specialists and citizen developers
- There is a recognition of the pros and cons of citizen development and attempts are made to allow and manage these approaches
- There is minimal inconsistency between the documented process and the deployed process.

#### Governance, Risk, Compliance and Security

- There is recognition that different solutions are associated with different risk and compliance profiles and can be designed and managed accordingly
- Quality Systems incorporate key business process solutions, and the solutions are tested for compliance for processes that impact quality
- New solutions are designed with tracking, performance metrics and out of bounds notifications

#### Business Process

- A process is considered as a whole, rather than as an automation of discrete tasks. Process maps for the end-to-end process have been created and are maintained. Associated solution documentation is developed.
- Existing process automation solutions are reviewed, documented and attempts made to bring them under management. In some cases, solutions are redeveloped on the new platform.
- There is a method for dealing with exceptions, or the automation is explicitly scoped to meet the majority of situations.
- There are processes for identifying new automations and for modify existing solutions, though exceptions and 'shadow' development remain.
- Whole system approaches are attempted, and common-data sets and sources begin to be established.

#### Level 300 Impacts

At this level you can expect the following:

- Management and users can begin to feel confidence that processes and activities are compliant.
- Productivity / efficiency gains are observable if not yet fully measurable.
- Increased transparency supports better productivity and planning and lowers user stress.
- There is increasing employee confidence in following the processes because they provide better results than prior manual processes.
- The credibility of the team is improved, that helps user acceptance for new processes.

### Level 400 - Predictable

Organizations at this level have set goals for the process, such as reduced time between steps, lower cost, fewer errors, customer satisfaction, etc., and the process is being measured against these goals. The system is supporting and driving the business process rather than the individuals involved in the process. The results are predictable, and the users have come to depend on the system and no longer feel the need or desire to work around it.

**[Predictable level](microsoft365-maturity-model--intro.md#level-400---predictable)** characteristics include:

#### General
- Workflows on the platform may have connectivity to LOB systems.
- Users have access to process analytics and audit trails around the workflow. (e.g., a user can report on document approval (person, date and comments).
- There is greater transparency to the process at the end user level (e.g., a user can see the status of a particular request at any step)
- Collaboration happens in the context of a work item as part of a dynamic, nonlinear business process (the "case").
- There is a well understood continuum from citizen developed small scale, pilot and prototype business process solutions through intermediate to fully developed and managed approaches.
- The organization has a register of the BP solutions in use, with assessment of their risks, ownership, technology and interactions with other processes and systems.
- Process performance is monitored using established metrics.
- APIs and information sources are well established and made available for BP process development
- Technology standards are in place and adhered to.
- Development standards, including UI, UX, API, reporting, error trapping and exception monitoring are well established; there is support for implementing these in small scale developments.
- Staff are trained in the standard approaches and required to undertake training in these as well as the technology and process development methodologies. Business Process training is part of the training program for M365, with centralized documentation / resources.
- New processes and introduction of new line of business systems are considered against the strategy and standards in place to ensure they are compatible
- BP solution development is led by 'whole system thinking'
- All critical processes are designed for and assessed against compliance and quality needs. Formal documentation, methodologies, audit and review are applied to key systems.
- Process control such as SPC (Statistical Process Control) may be enabled
- Process outputs and metrics data are collected and used for business intelligence reporting
- All processes have clear ownership. Changes in staff and expertise are considered and processes are resilient to these changes

#### Level 400 Impacts

At this level you can expect the following:

- Users feel that a particular automated process is stable. They have come to rely on it and shudder at the thought of the "bad old days."
- The organization is looking for other places to automate processes, asking the question "is this a candidate for automation?"
- New insights gathered from process analytics support restructuring of business processes for continual process improvement, earlier identification of issues, and data to support additional headcount, where needed. (e.g., for headcount: showing long lead times in SharePoint project requests where the delay is due to limited headcount to build solutions)

### Level 500 - Optimizing

Organizations at this level are using the M365 platform optimally to automate their processes, and are focused on feedback and continuous improvement. The goals/metrics are being achieved on a regular basis, and there is both objective data and anecdotal evidence to support the success of the solution.

**[Optimizing level](microsoft365-maturity-model--intro.md#level-500---optimizing)** characteristics include:

#### General
- Power users can edit existing workflows to adapt them to changing business needs on the fly with an understanding of the implications of these changes.
- Standardized workflows, data sources, connectors, UI and process components exist for re-use and guidance
- Users leverage data from the business process management platform to optimize process, simulate on real data, clear bottlenecks, and balance work across workloads.
- Business processes may extend to external users.
- The enabling technology platform is being upgraded and managed proactively as an enterprise solution.
- Staff are highly skilled and engaged in the processes, providing feedback, ensuring compliance and adapting to edge cases as required
- All processes are well understood, managed and leveraged
- Processes reach outside the organization, to interact efficiently with 3rd parties including suppliers, clients and regulators

#### Governance, Risk, Compliance and Security
- There is an active and ongoing process of process review against operational and other objectives and processes and supporting technologies are re-engineered accordingly
- Processes drive and ensure compliance while also improving productivity.

#### Business Process
- Users have visibility into the process and can provide feedback to process improvements.
- Output metrics from business process solutions provide insights into business improvement and drive process enhancements at all levels. Impacts in one part of the process are understood up and down the event chain.
- Business Processes are continually measured as part of a whole-system approach and collectively improved or adapted to changing needs.
- Advanced tools are used to drive optimization, including AI, Statistical Process Control and cross industry benchmarking
- There is a high level of continuous process oversight and remodeling
- Innovative approaches are taken to automation of tasks; as new technologies and techniques emerge these are proactively introduced, freeing up time for staff to deal with complex cases and 'out of bounds' scenarios.

#### Level 500 Impacts

At this level you can expect the following:

- It's possible to plan innovations because the baseline of performance is well known and trusted.
- The organization can adapt its processes with less stress and more agility to respond to changing business conditions (e.g., mergers, acquisitions, new product lines, etc.)
- There is increased productivity across the organization as roles and responsibilities are focused on tasks that cannot be automated.
- There is an increase in employee engagement as mundane, repetitive tasks are automated and viewed as a competitive advantage for how the organization works.

## Scenarios

- Employees require manager approval for time off requests.
- Employees can request new hardware, equipment, or supplies which then follows an approval and procurement process.
- A subject matter expert updates a policy, which then requires multi-level review and approval.
- A proposal to a customer requires multiple areas of review and approval before it can be sent to the customer.
- A customer opens a support case which requires multiple steps and escalations to resolve.

## Cost & benefit

Business Process is one area where hard metrics are relatively easy to capture, and where ROI can be clearly shown. Examples of Business Process ROI include:

- Reduced time between steps in the process
- A positive change from process status unknown at any point to status clearly viewable by the users in the system
- Reduced cost when processes involving purchasing or expenses are standardized
- Improved discussion making
- Reduced risk of missing compliance deadlines or getting fined for not adhering to compliance and government regulations.

## Conclusion

Improving your Business Process maturity requires an investment in business process mapping, as well as an understanding of M365's functionality and how it can support your business processes. This investment in defining and educating will be repaid in clear, measurable ROI for the business processes that you modernize and automate on the M365 platform. This ROI can take the form of bottom-line cost and time savings, as well as more top-line advantages in terms of competitiveness and customer and employee satisfaction.

## Common Microsoft 365 Toolsets

- Connectors / Custom Connectors to access other line of business apps and services
- Dataverse
- Microsoft Forms
- Microsoft Lists
- Planner
- Power Apps
- Power Automate
- Power Virtual Agents
- Project Online
- Viva Goals
- Viva Sales

## Resources

[!INCLUDE [mm4m365-practitioners](includes/mm4m365-practitioners.md)]

## Related documents

- [Business process flows overview](/power-automate/business-process-flows-overview)
- [Defining a Power Platform Environment Strategy](defining-a-power-platform-environment-strategy.md)
- [The Power Platform Data Loss Prevention (DLP) policies you should be considering on Day 1](power-platform-dlp-policies-you-should-be-considering-on-day-1.md)

---

**Principal authors**:

- [Sadie Van Buren](https://www.linkedin.com/in/sadalit/)

**Contributing authors**:

- [Marc D Anderson, MVP](https://www.linkedin.com/in/marcanderson)
- [Simon Doy](https://www.linkedin.com/in/simondoy)
- [Simon Hudson, MVP](https://www.linkedin.com/in/simonjhudson)
- [Emily Mancini, MVP, UXMC](https://www.linkedin.com/in/eemancini)

---

[!INCLUDE [mm4m365-core-team](includes/mm4m365-core-team.md)]
