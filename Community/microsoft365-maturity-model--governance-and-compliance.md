---
title: The Microsoft 365 Maturity Model – Governance, Risk, and Compliance Competency
ms.date: 12/10/2024
author: nikki-c
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: article
ms.author: pamgreen
ms.service: microsoft-365
ms.localizationpriority: Low
description: The Microsoft 365 Maturity Model – Governance, Risk, and Compliance Competency
ms.collection: SPCommunity
---

# The Microsoft 365 Maturity Model – Governance, Risk, and Compliance Competency

![Maturity Model for Microsoft 365](media/maturity-model-for-microsoft-365/M365MM.png)

## Overview of the Concepts [tl;dr]

Organizations face increasing complexity and change in regulatory environments, calling for a more structured approach for managing Governance, Risk, and Compliance (GRC). A key enabler of compliance success is Information Architecture (IA), ensuring that data and documents are properly categorized, tagged, and structured to enhance efficiency and control.

The Governance, Risk, and Compliance Competency is focused on helping an organization reduce risk and improve compliance effectiveness by implementing a framework for compliance and risk management.

### Governance, Risk and Compliance framework

:::image type="content" source="media/microsoft365-maturity-model--governance-and-compliance/grc-framework.png" alt-text="Governance, Risk and Compliance framework":::

## Definition of this competency

**Governance** is the system of rules, practices, and processes an organization uses to direct and control its activities. Many governance activities arise from external standards, obligations and expectations. It also provides a framework for attaining a company's objectives and encompasses most areas management, from action plans and internal controls to performance measurement and corporate disclosure.

**Risk** enables an organization to evaluate all relevant business and regulatory risks and controls and monitor mitigation actions in a structured manner.

**Compliance** refers to the country/region, state or federal laws or even multi-national regulations such as GDPR regulations that an organization must follow. These regulations define what types of data must be protected, what processes are required under the legislation, and what penalties are issued to organizations that fail to comply.

For Microsoft 365, this means implementing specific policies, operational processes, and technical controls to protect the data in Microsoft and cover some or all of using, storing, sharing, disclosing, erasing and destruction of data. The data should also be secured appropriately to guard against loss, theft and misuse.

A critical enabler of governance, risk, and compliance is **Information Architecture (IA)**, which ensures data and documents are structured, categorized, and governed effectively. IA supports compliance by:

- Giving **end users** a clear understanding of where information should be stored and how it should be classified.
- Enabling **information owners** to manage changes in governance frameworks and legal requirements effectively.
- Allowing **legal and compliance teams** to quickly gain an overview of risks and identify areas requiring immediate attention.
- Providing **management teams** with visibility into whether they are following established governance frameworks and where improvements are needed.
- Helping **IT and system owners** identify sensitive data, apply appropriate security measures, and align new technological solutions with organizational resilience strategies.

Without a structured Information Architecture, organizations face increased risks of compliance failures, inefficient data management, and security vulnerabilities. Unstructured or ad-hoc data storage results in poor findability, high costs for eDiscovery, and an inability to meet regulatory retention and privacy obligations. By embedding IA into their compliance strategies, organizations ensure that governance is predictable, scalable, and automated—reducing risk and improving operational efficiency.

Smaller organizations may only need to comply with the baseline general data protection rules that apply to every organization. Other organizations must comply with industry-specific and/ or country/region specific regulations which may overlap and/or conflict.

Example compliance regulations are:

- CCPA (California Consumer Privacy Act; USA)
- GDPR (General Data Protection Regulation; Europe)
- HIPAA (Health Insurance Portability and Accountability Act; USA)
- PCI DSS (Payment Card Industry Data Security Standard; international)
- SOX (Sarbanes–Oxley Act; US)

**Compliance** is not the same as **security**, but security should be considered when building your plan as effective security is frequently a compliance requirement. Compliance requires only that the legally mandated minimum standards are met whereas data security covers all the processes, procedures and technologies that define how you look after sensitive data and guard against breaches.

To address the gap between compliance and security many organizations also follow compliance and regulatory frameworks, such as COBIT, ISO 27001, or ITIL. These provide guidelines and best practices to meet regulatory requirements, improve processes, strengthen security, and achieve other business objectives (such as adopting a ‘cloud-first’ strategy).

## Evolution of this competency

:::image type="content" source="media/microsoft365-maturity-model--governance-and-compliance/grc-competency-overview.png" alt-text="Governance, Risk, and Compliance Competency Levels":::

See the [Maturity Model for Microsoft 365 - Introduction](microsoft365-maturity-model--intro.md) for definitions of the Maturity Model levels.

> [!NOTE]
> Some characteristics should, perhaps, be addressed a little more urgently than others; these have been marked with the 'Sparkles' emoji: ✨

### Level 100 - Initial

At level 100 maturity an organization does not believe that governance and compliance is important to its overall objectives.

Management does not consider investing in the Governance, Risk, and Compliance (GRC) related systems necessary for the overall business strategies. In addition, the organization does not assess the business impact of its vulnerabilities and it does not understand the risks involved due to these vulnerabilities.

Organizations at level 100 maturity pay little attention to compliance and are characterized by the absence of policies and procedures for information/ data compliance of governance.

The organization addresses compliance in a reactive mode — doing assessments when forced to. There is no ownership or monitoring of GRC. Management does not invest in a compliance framework, technology controls, or employee training to meet baseline standards for managing risks and remaining compliant with regulations and standards.

**[Initial level](microsoft365-maturity-model--intro.md#level-100---initial)** characteristics include:

#### People and Culture (100)

- The leadership team do not believe that compliance is fundamental to their overall objectives. It is a means to an end.
- Compliance obligations and risks are not understood.
- No individual or department is responsible for governance, risk and compliance, nor is it clear where these activities are taking place on a devolved basis
- Roles, training, and competencies needed for compliance are not developed. Employees are not aware of how compliance impacts their daily work.
- No training on technology usage—Users lack understanding of metadata, labels, and retention policies, leading to chaotic, inconsistent content classification.
- No defined roles for information governance—Managers and business owners do not take responsibility for structuring information.

#### Process (100)

- No process for keeping up with regulations that may affect their market and industry.
- GRC processes and controls are either absent or ad hoc or out of date.
- Risks assessments not undertaken.
- Compliance and governance obligations are not reviewed or monitored
- There is ad-hoc implementation and response to incidents (reactive).
- Compliance controls and evidence is ad hoc or does not exist.
- External sharing is unmanaged—users freely share content externally via email attachments, Teams invites, SharePoint sharing, and calendar invitations without oversight or tracking.

#### Information Architecture (100)
- No naming conventions for Teams, SharePoint sites, or documents.
- No metadata strategy—content is stored without categorization or retention considerations.
- Unclear ownership—anyone can create and share content without oversight.
- Lack of Governance Policies—Absence of policies and principles governing information management, leading to user overwhelm and inefficient content handling.

#### Technology (100)

- No standardized storage location for documentation, records and supporting evidence.
- No technical controls in place to support compliance.


#### Impacts (100)

Due to the lack of policies, controls and user training to support information/ data compliance in Microsoft 365 the organization is at risk of:

- Overlooking changes and/or additions to existing compliance requirements.
- Employees accidentally exposing sensitive data to third parties.
- Employees stealing information of value, such as customer lists or proprietary trade secrets.
- Consequences such as data breaches, erosion of customer trust, severe fines and other penalties due to non-compliance with regulations.
- Elevated eDiscovery costs.
- Lack of structured information leads to inefficiency—users spend excessive time searching for documents.
- Shadow IT emerges as employees create their own document storage solutions outside IT oversight.
- Unclear accountability for information governance, leading to uncontrolled site sprawl and data loss risks.

### Level 200 - Managed

At level 200 maturity an organization tends to believe governance and compliance is a series of boxes to check.

At this maturity level organizations acknowledge compliance regulations and standards. However, organizations may take a ‘tick box’ approach to Governance, Risk and Compliance (GRC). Policies have been written, intended to avoid the damages that level 100 organizations can face, but the polices are not enforced in the organization.

**[Managed level](microsoft365-maturity-model--intro.md#level-200---managed)** characteristics include:

#### People and Culture (200)

- Leadership understands and accepts the importance of governance and compliance but has not driven it into the organization nor recognized it as a business enabler.
- Some policies have been written but are not enforced or comprehensively adopted.
- No formal compliance roles in place or roles have been allocated but without suitable training or assessment of competence. Governance, Risk and Compliance relies on individuals being responsible for actions and approaches in their own areas.
- No formal GRC training; communication is ad hoc or occurs in response to a GRC event. Most employees are not aware of how governance, risk and compliance impact their daily work.
- Training for information owners (e.g., managers)—Organizations begin training leaders to understand the importance of structured information, how data should be classified, and why governance matters.
- Discussions on metadata and retention policies begin but are not widely adopted.
- Ownership roles identified (e.g., Site Owners, Data Stewards), but not enforced.

#### Process (200)

- Governance and compliance management is local, uncoordinated or sporadic It is dependent on individual people to action and monitor.
- ✨ Processes exist but are manual and lack standardization, making it hard to measure their effectiveness, enforce them or obtain an overview of activity and status.
- Limited collaboration between compliance and operational teams. Often compliance is an afterthought.
- Response to incidents is reactive /ad hoc, lacking consistency, formality and may result in ineffective actions.
- Risk management is perceived as a process.
- External sharing awareness emerges—the organization begins discussions on what should be shared externally but without formalized governance.
- Basic restrictions on external sharing—some organizations introduce guidelines but lack enforcement.

#### Information Architecture (200)
- Initial metadata framework is introduced, but usage is inconsistent across the organization.
- Basic site and document structure discussions begin, but they are not standardized.
- Ownership roles for content management are identified (e.g., Site Owners, Data Stewards), but they are not strictly enforced.
- Discussions on content categorization and retention policies emerge, but adoption is limited.

#### Technology (200)

- ✨ Basic technical controls may exist but may not be appropriately implemented to ensure compliance.
- ✨ Technical controls to manage retention and deletion exist, however there are minimal processes to implement these effectively; retention and deletion is largely a manual, ad hoc activity, though there may be reminders and triggers in processes to act as prompts.
- Storage locations for documentation and supporting evidence are inconsistent and fragmented.
- There is a tendency to focus on email rather than a wider view of content and processes that need to be compliant.
- Basic metadata framework begins, but users are not required to follow structured tagging.

#### Impacts (200)

At this level you can expect the following:

- Employees see compliance as painful and "extra" to their day job.
- The organization is unaware of new and changing compliance laws and regulations so unaware of any new, increasing, or decreasing compliance risks.
- Organizations do not know what sensitive data they have, where it is, who can access it, and its risk of exposure. This makes it difficult to apply effective policies and controls to protect the most critical data assets. Organizations will retain nothing or everything ‘just in case’.
  - Information clutter and duplication degrades productivity.
  - The organization remains at risk from both deleted/lost information and from ‘over-retained’ information
- Action is only taken after a major violation or ‘near miss’ has occurred, to show they are trying to meet compliance standards. Even then, it is implemented as a tactical response to a serious problem, rather than a strategy for permanent improvement.
- Discovery exercises are costly and complex as no specialist tools are used.
- Limited metadata adoption leads to difficulty in organizing and finding information.
- Some compliance improvement, but retention policies are not systematically enforced.
- Growing awareness of external sharing risks, but lack of standardization creates security gaps.

### Level 300 - Defined

At level 300 maturity, an organization believes compliance is essential to the business. They begin to affect a ‘top-down’ cultural change in working to incorporate governance, risk and compliance-led practices. It’s understood that it is the job of executives to enforce adoption and training among managers, and the job of managers to do so with their staff.

A baseline compliance framework is implemented with a standardized set of policies and controls.

Processes measured and controlled

**[Defined level](microsoft365-maturity-model--intro.md#level-300---defined)** characteristics include:

#### People and Culture (300)

- ✨ The leadership team see compliance as essential to business continuity and may value the rigor as a business improvement tool.
- ✨ Compliance roles and responsibilities are assigned to accountable individuals, who have been trained but may lack expertise and experience. They understand the importance of the role and will reach out, reactively to legal and other experts for guidance and counsel.
- ✨ A Compliance framework, in some form, has been documented and communicated to process owners. However, the implementation decisions are left to local business and system owners so GRC initiatives are managed in silos.
- ✨ Training, education, and awareness are run annually. Staff have a broad awareness of their responsibilities.
- Compliance activities are frequently event driven, such as an audit or a regulatory deadline.
- Where GRC sits across multiple departments and activities in the organization individuals with those roles will coordinate their activities, possibly through a Compliance committee or similar mechanism.
- The organization invests significant time on stakeholder education, ensuring that the new ways of working together and the value of risk and adopting compliant processes are understood. However, commitment to upholding standards varies across the organization.
- Archivist Role Introduced—responsible for organizational storage governance, retention enforcement, and lifecycle management.
- Core processes and all sensitive data are clearly defined—Information owners take responsibility for defining and structuring their critical data.
- Formalized training for all users—Users are trained on metadata, labels, retention policies, and how misuse can impact security and compliance.

#### Process (300)

- ✨ There are staff with a role that includes monitoring regulatory updates and translating them into new company policies. In large organizations or those in industries with strong compliance needs, example roles may include Director of Compliance, General Counsel, Senior Information Risk Officer, Data Protection Officer). In smaller organizations it is likely to sit with members of the executive team or the functional head of departments with strong compliance alignment. This is seperate from or in addition to staff dedicated to security measures (for example a Chief Information Security Officer).
- ✨ Risk level is periodically reviewed & updated.
- ✨ Limited information and records are available for audit, these are generally specific to the function rather than providing an aggregated or holistic vie.
- There is limited or misplaced confidence that all governance and compliance risks are known and managed.
- ✨ There are systems, tools and processes for managing the Governance, Risk and Compliance processes. While these vary according to the standards and requirements imposed, they may include: training and knowledge content; risk, issue and status logs; asset and impact lists; action plans; processes for reviews and updates; systematic audits and assessments, staff training and competency logs.
- ✨ Strong content management tools and processes that include effective lifecycle management are in place.
- The organization measures and assesses controls and activity, but largely at an individual or devolved level.
- External sharing policies are defined and controlled—who can share what, with whom, and under what conditions.
- External users in Teams and SharePoint require approval before access is granted.
- Email attachments containing sensitive data trigger a review process before sending.

#### Information Architecture (300)
- A structured metadata framework is widely used, improving consistency across document management, but enforcement is not yet mandatory across all areas.
- Standardized site and document structures are implemented, reducing redundant storage and improving findability.
- Ownership of content is clearly defined, with formalized processes for maintaining document integrity.
- Retention policies are systematically applied to content types, ensuring compliance with governance requirements.
- Clear categorization of sensitive and critical business data, with guidelines on storage and protection.
- Formal metadata schema is applied to:
  - Identify personal data.
  - Define retention requirements—how long data should be stored.
  - Clarify the purpose of storage and regulatory requirements.
  - Apply disposition policies—deletion and archival timelines.
  - Defined Trigger Dates (when rules start to apply based on laws, regulations, or company policies) such as signing date, decision date, publish date, employee exit date, purchase date.
- A structured metadata framework is widely used, improving consistency across document management, but enforcement is not yet mandatory across all areas.
- Standardized site and document structures are implemented, reducing redundant storage and improving findability.
- Ownership of content is clearly defined, with formalized processes for maintaining document integrity.
- Retention policies are systematically applied to content types, ensuring compliance with governance requirements.
- Clear categorization of sensitive and critical business data, with guidelines on storage and protection.

#### Technology (300)

- ✨ Technical controls to manage retention and deletion are in use and are generally effective for recognized classes of content (e.g. finance and HR files). A degree of automation supports this, reducing user burden and driving some level of consistency.
- There is a central (digital) system of record for compliance. However, usage varies across the organization and local solutions may be in use.
- Software solutions are used but typically in a tactical manner, without a thought for a broader set of requirements. This results in multiple systems to manage individual governance, risk and compliance initiatives, each operating in its own silo.
- Governance, risk and compliance controls are implemented but are reliant on the user to apply the right controls to the right content.
- Use of automated tagging, sensitivity labelling and policies is not broadly or well implemented, though it may be being piloted.
- Standardized Information Architecture Models—Adoption of consistent IA models and examples to ensure uniformity across sites and improve user experience.
- In-Place Records Management is introduced, ensuring documents remain in their original location while being classified as records.
- Enhanced Metadata Usage—Leveraging metadata over folders to facilitate easier filtering and searching of content.

#### Impacts (300)

At this level:

- ✨ The organization starts to build a compliance culture with roles and responsibilities being defined.
- ✨ Employees start to understand the impact of non-compliance in their job roles.
- ✨ There are processes for dealing with finding, breaches and risks, however there are gaps and a tendency to be reactive.
- A Governance, Risk and Compliance framework, consisting of strategy, policies, processes, controls, technologies and staff competence, is implemented. However, implementation is uncoordinated and siloed.
- eDiscovery investigations are still complex and costly as multiple versions of data exist
- Not all Governance, Risk and Compliance risks are addressed and there are frequently unknown risks.
- Standardized site and document structures reduce redundant storage and improve findability.
- Clear categorization of sensitive and critical business data enhances data protection measures.


### Level 400 - Predictable

At level 400 maturity an organization’s approach to governance and compliance becomes more well defined and acts as a foundation for activity, the focus shifts from extensive written procedures to empowering individual employees to make informed decisions to reinforce the company’s compliance culture. This occurs as a by-product of establishing a culture with high compliance awareness.
The Compliance framework is now tailored to include an up-to-date and accurate catalog of information and data laws, regulations, and policies by country/region and is readily accessible to all relevant employees.
An overarching Governance, Risk, and Compliance process, through control, definition, enforcement, and monitoring, has the ability to coordinate and integrate these initiatives.
Proactive rather than reactive.

**[Predictable level](microsoft365-maturity-model--intro.md#level-400---predictable)** characteristics include:

#### People and Culture (400)

- ✨ The leadership team sees value in continuously improving the governance, risk and compliance program. Governance, risk and compliance are factored into all business decisions and GRC is represented at board level.
- ✨ Dedicated teams and individuals are in place with clearly defined roles and responsibilities. The limits of competency are understood, with supporting metrics, and reflected in defined decision making authority for accountable individuals. Processes are in place to support GRC decision making when these limits are reached, with defined access to legal and other expert external advisors.
- ✨ Compliance and operations teams work in partnership to assess risk and compliance. 
- ✨ Training, education, and awareness includes annual training matched to business needs. Who has been trained in what is tracked.
- Compliance workloads are reduced through standardization, process improvements and use of technology.
- Policy communications are routine and semi-automated. Most employees understand the importance of risk and compliance and their role in protecting the organization.
- Regular training needs analysis for compliance training is undertaken to identity gaps and improve content.
- Ongoing governance training for employees—users receive continuous education to keep up with evolving policies and risks.
- Archivist Role Expanded—takes on a more automated approach, working with AI and compliance tools to manage document storage lifecycle.

#### Process (400)

- ✨ Conversations about risks and compliance are held at all levels of the organization and compliance is embedded into business processes.
- ✨ Organization wide processes and policies are streamlined & simplified, they are reviewed and updated as needed according to an approved schedule.
- ✨ Process metrics are in place, controls monitored, and compliance is measured.
- ✨ Feedback processes are used to improve consistency.
- ✨ There are mechanisms to continuously assess compliance control and process gaps to prevent compliance failures.
- ✨ Business continuity planning and disaster recovery plans are well developed, maintained and tested.
- A data architecture has been implemented to govern which data is collected, how it is used, where it is stored, how long it is stored when it is destroyed  
- External sharing policies are fully automated, ensuring only approved users can share externally through predefined workflows.
- Teams meeting policies regulate external guests, requiring pre-approval for access to certain types of meetings.
- External sharing of SharePoint files is restricted based on sensitivity labels and automated rules.

#### Information Architecture (400)
- A structured metadata framework is enforced across all systems, ensuring compliance and consistency in document management.
- Automated metadata tagging is introduced to classify and protect sensitive information.
- Ownership of content is fully established, with clear accountability for document governance.
- Retention policies are systematically enforced through automation, ensuring regulatory compliance.
- Formal metadata schema is fully applied to:
  - Identify personal data.
  - Define retention requirements—how long data should be stored.
  - Clarify the purpose of storage and regulatory requirements.
  - Apply disposition policies—deletion and archival timelines.
  - Set Trigger Dates (when rules start to apply based on laws, regulations, or company policies) such as signing date, decision date, publish date, employee exit date, purchase date.


#### Technology (400)

- ✨ There is a central digital system of record to manage compliance program and to store evidence.
- ✨ Content can be shared across organizational boundaries enabling efficient and secure collaboration with partners, clients, and other third parties without loss of control or governance.
- ✨ Integrated dashboards, balanced scorecards etc. are available to executives and across the organization as needed.
- Compliance specific solutions are purchased to manage compliance requirements.
- There is an auditable history of data activities with an understanding of how it can help support effective Governance, Risk and Compliance.
- Productivity and analytical tools are in place to make tracking tasks, reporting and collaboration easy.
- Compliance controls are automated and tailored to different usage scenarios.
- Automated metadata tagging is introduced to classify and protect sensitive information.
- Azure AD Naming Policies (or equivalent) are enforced for Teams and sites.
- Retention and compliance systematically enforced, ensuring regulatory alignment.
- Automatic archiving of documents based on predefined lifecycle management rules tied to content types or equivalent.
- Implementation of an eArchive that:
  - Adheres to international standards for long-term preservation, such as PDF/A.
  - Automates document archiving based on lifecycle policies.
  - Ensures accessibility and compliance with regulatory requirements.
  - Expands archiving beyond SharePoint to include CRM, logistics, finance, and other document repositories.
- Automated Archiving with Power Automate—workflows move records to designated archive locations as part of the lifecycle policy.

#### Impacts (400)

At this level

- Everyone in the company at all levels shares accountability for following a higher standard.
- Compliance is embedded in the culture of the organization so all employees understand the importance of compliance and their role in protecting the organization. Policies are understood and the reasons behind the policies are clearly explained. Engagement is high at this level because all members of the organization are now responsible for the success of the program.
- Data investigation become simpler due to advanced tools and only the right data being retained.
- Automated processes ensure consistent application of retention policies, reducing the risk of non-compliance.
- Ownership of content is fully established, with clear accountability for document governance.

### Level 500 - Optimizing

At level 500 maturity, an organization believes that taking a strategic approach to governance and compliance will actively support business goals as opposed to serving merely as a function of risk mitigation.

Metrics are reviewed regularly & updated as needed; results monitored & processes continuous improvement.

Compliance is embedded in the organization and business activities are ‘compliant by design’.

Organizations at this level use technology strategically to gain operational efficiencies, greater visibility into their operations, reduce risks, and drive down compliance costs. Tools are integrated in order to monitor controls and gain insights into their governance, risk and compliance program.

**[Optimizing level](microsoft365-maturity-model--intro.md#level-500---optimizing)** characteristics include:

#### People and Culture (500)

- ✨ The leadership team sees value in achieving compliance as providing a strategic advantage to the organization.
- ✨ The dedicated compliance team now includes a focus on strategy, is future looking, proactively identifying emerging  regulation and market change to understand the impact, risks and opportunities for the business; these are fed into the board as a basis for strategic decision making. Process improvement and continuous professional development for the accountable people is embedded int eh GRC and executive functions.
- ✨ There is a pervasive compliance culture where all employees understand the importance of compliance and their role in protecting the organization.
- ✨ Collaboration occurs between the compliance team, security team, operations teams, and system owners to ensure systems (e.g., data storage and processing systems) are secure and compliant by design.
- Compliance workload shifts from administrative to strategic (due to automation).
- ✨ Decision-makers becoming risk seeking rather than risk adverse, knowing that they can and must manage the risks they identify.
- AI-assisted training and coaching for users—real-time feedback helps prevent labeling/tagging mistakes before they create compliance risks.
- Archivist Role is fully AI-assisted—predictive content governance ensures retention, compliance, and access rules are continuously optimized.


#### Process (500)

- Compliance and risk are coordinated across upstream and downstream processes / requirements to ensure consistency.
- ✨ The organization proactively reviews and updates risk and compliance metrics to address gaps and prevent compliance failures. Results are monitored & used for continuous improvement.
- Processes and controls and reporting are automated and centralized
- ✨ Independent information security compliance standards such as ISO/IEC 27001 are used to benchmark best practice and align security and compliance.
- ✨ Metrics are used to measure and improve collaboration outcomes and these metrics are clearly connected to business strategy.
- Compliance is embedded in strategic planning as well as in daily strategic and tactical decision-making.
- ✨ Business continuity planning and disaster recovery are regularly tested.
- Compliance processes and practices are externally audited.
- External sharing is seamlessly integrated with B2B connections and trusted relationships, ensuring secure collaboration across organizations while maintaining compliance and governance.
- Automated identity verification for external users—guest access is dynamically adjusted based on trust level and previous engagements.
- Adaptive external sharing policies—real-time risk analysis adjusts sharing permissions dynamically based on user behavior and external access trends.

#### Information Architecture (500)

- AI-driven metadata classification dynamically applies and refines metadata structures based on document usage and context.
- Intelligent document lifecycle management—automation ensures content is archived, retained, or deleted based on AI-driven insights.
- Risk-based metadata tagging adapts dynamically to evolving compliance needs and security risks.
- Formal metadata schema is continuously optimized through AI to:
  - Identify personal data dynamically.
  - Automate retention adjustments based on regulatory updates.
  - Ensure compliance with evolving legal requirements.
  - Proactively manage disposition policies with predictive analytics.
  - Trigger automated governance actions based on organizational rules and real-time changes.

#### Technology (500)

- ✨ Compliance and DLP rules are comprehensively applied and enforced.
- Controls are automated and subject to continuous improvement
- ✨ Tailored compliance controls with policy enforcement are implemented to provide different levels of protection during collaboration depending on sensitivity, risk, and environment.
- The organization invests in compliance management solutions that encompass multiple systems.
- Full AI-driven governance—content classification and tagging handled dynamically by AI (e.g., Syntex, Copilot).
- Intelligent site lifecycle management—Teams, sites, and documents are automatically archived, extended, or deleted based on usage patterns.
- Risk-based access and retention policies—sensitive information is managed with adaptive security controls.
- Automated compliance auditing—AI-driven monitoring ensures policy adherence without manual intervention.
- Enterprise-Wide Archiving Strategy—compliance-driven archiving covers all document storage locations, ensuring long-term preservation and regulatory adherence across the entire organization.
- AI-Driven Information Management—Deployment of AI technologies to dynamically organize, classify, and manage content, leading to predictive content delivery and enhanced user engagement.

#### Impacts (500)

At this level, the governance, risk and compliance controls are aligned to the organizations risk appetite. Employees, managers, and executives understand their responsibility to the organization to ensure the success of the compliance program. Honesty, accountability, respect, and leadership are principles of these organizations, and transparency is a default.
- Compliance maturity is benchmarked against industry best practice.
- AI-driven classification enables predictive governance, reducing administrative workload.
- Seamless compliance and security integration, with dynamic risk-based policies.
- Improved data-driven decision-making, as AI continuously optimizes metadata structures.
- Business agility is maximized, with self-regulating information flows that support innovation.
- Information governance is fully automated, allowing teams to focus on strategic initiatives rather than administrative tasks.

## Scenarios

<!--- TBD --->

## Cost & benefit

Many characteristics can be delivered using the M365 platform to develop Governance and Compliance solutions and processes, especially using SharePoint, Microsoft Teams, Power Automate etc. available with any Business or Enterprise license. The native compliance capabilities of M365, such as those in the Compliance Center, do depend on the Microsoft 365 licensing level. While there is not a direct mapping, a useful guide is provided below. Some functionality requires additional licenses.

:::image type="content" source="media/microsoft365-maturity-model--governance-and-compliance/grc-technical-controls.png" alt-text="Governance, Risk, and Compliance technical controls":::

Download the [Microsoft 365 Comparison table](https://go.microsoft.com/fwlink/?linkid=2139145) to see which security and compliance features are available with each option.

## Common toolsets

Organizations have different compliance needs depending on the national, regional and industry-specific standards they need to comply with. Microsoft 365 provides a set of integrated capabilities that you can use to help you manage end-to-end compliance scenarios. The 4 groups of compliance and risk management capabilities are listed in the following section. Capabilities that require an E5 license are marked with an asterisk (*). SharePoint Advanced Management (SAM) can be required for some functionality, and is now a Pay-as-you-go model. 

### Information protection

- Customer key*
- Data Loss prevention
- Data Loss prevention for Teams DLP*
- Hold your own key*
- Message encryption
- Advanced message encryption*
- Multi geo (extra)
- Sensitive information types*
- Sensitivity labels
- Sensitivity labels for automated labelling*

### Information governance

- Records management*
- Retention labels
- Retention labels for automated labelling*
- Retention policies
- Retention policies for rules based policies*
- Expiration policies for inactive sites and OneDrives (SAM)
- Access reviews and policy enforcement for SharePoint Online (SAM)
- Site access insights and external sharing monitoring (SAM)

### Insider risk management

- Communications compliance*
- Customer lock box*
- Information barriers*
- Insider risk management*
- Privacy Management*
- Privileged access management*

### eDiscovery and Audit

- Audit* for Advanced Audit
- Cloud app discovery
- Compliance Manager
- Compliance Manager custom assessments*
- eDiscovery for Advanced eDiscovery*
- Litigation hold
- Microsoft Defender for Cloud Apps (MCAS)*
- Search
- Advanced sharing insights for SharePoint and OneDrive (SAM)
- External user expiration policies (SAM)
- Improved logging and audit capabilities for compliance tracking (SAM)

The available compliance capabilities in your tenant will depend on your Microsoft 365 licensing. Some of the functionality requires additional licenses. Download the [Microsoft 365 Comparison table](https://go.microsoft.com/fwlink/?linkid=2139145) to see what security and compliance features you have with your licensing.

## Resources to learn more

- [Microsoft 365 compliance documentation | Microsoft Docs](/microsoft-365/compliance/)
- [Microsoft 365 guidance for security & compliance - Service Descriptions | Microsoft Docs](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#advanced-audit)
- [Get started with the Microsoft Service Trust Portal - Microsoft 365 Compliance | Microsoft Docs](/microsoft-365/compliance/get-started-with-service-trust-portal)
- [Microsoft Purview compliance portal](https://compliance.microsoft.com/)

## Conclusion

Achieving compliance is not a project. It is an ongoing process that needs embedding into the culture of the organization. Regulations continually change, your environment is always changing, and the operating effectiveness of a control may break down. Regular monitoring and reporting are a must, and guidance on exactly what “regular monitoring” entails is also outlined within each framework.

---

**Principal authors**:

- [Nikki Chapple](https://www.linkedin.com/in/nikkichapple/)
- [Simon Hudson, MVP](https://www.linkedin.com/in/simonjhudson/)
- [Mike Cox](https://www.linkedin.com/in/michaelgeoffreycox/)
- [Pia Langenkrans](https://www.linkedin.com/in/pialangenkrans/)

---

[!INCLUDE [mm4m365-core-team](includes/mm4m365-core-team.md)]
