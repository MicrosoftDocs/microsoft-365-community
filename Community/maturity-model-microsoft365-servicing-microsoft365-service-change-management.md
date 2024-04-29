---
title: Maturity Model for Microsoft 365 Practical Scenarios – Microsoft 365 Service Change Management
ms.date: 10/9/2023
author: michaelblumenthal
ms.reviewer: daisyfeller
manager: pamgreen
ms.topic: article
ms.author: daisyfeller
ms.service: microsoft-365
localization_priority:
description: Maturity Model for Microsoft 365 Practical Scenarios – Microsoft 365 Service Change Management
ms.collection: M365Community
---

# Practical Scenarios – Microsoft 365 Service Change Management

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

The [Maturity Model for Microsoft 365](microsoft365-maturity-model--intro.md) is a useful tool for considering high level business capabilities and competencies, providing benchmarking, and planning guidance. However, practical application of the Maturity Model to specific tasks and needs is not addressed in the Competency or Elevate documents. The Practical Scenarios documents seek to address this, providing easily digestible guidance and strategy for focused topics.

This Practical Scenarios document covers service change management as surfaced in the Microsoft 365 [Admin Center dashboard](https://admin.microsoft.com/?source=applauncher#/homepage), specifically Service Health advisories and Message Center. Interaction with these should be a key practice in operational management of M365.

## Introduction to Service Change Management

The [Microsoft 365 Admin Centre](https://admin.microsoft.com/#/homepage) provides 2 key service change tools: [Message Centre](https://admin.microsoft.com/?source=applauncher#/MessageCenter) and [Service Health](https://admin.microsoft.com/?source=applauncher#/servicehealth/advisories), available via the browser portal and the mobile Microsoft 365 Admin app. Both are accessible only to users who have been granted access.

![Advisories in the Microsoft 365 Admin Center](media/maturity-model-microsoft365-servicing-microsoft365-service-change-management\advisories.jpg)

![Mobile advisories in the Microsoft 365 Admin Center](media/maturity-model-microsoft365-servicing-microsoft365-service-change-management\advisories-mobile.jpg)

Microsoft makes planned service changes to the M365 services daily, resulting in over 1000 change announcements per year. Effective IT operations will maintain awareness of current and future changes and assess their impacts on the business. These changes are primarily announced via the [Message Center](https://admin.microsoft.com/?source=applauncher#/MessageCenter), with support from the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap) and supporting blogs.

This operates in conjunction with [Service Health](https://admin.microsoft.com/?source=applauncher#/servicehealth/advisories) advisory messages which describe active issues and the health status of all services that are available for your current subscriptions. Service Change management for Microsoft 365 involves monitoring the change announcements and determining what action is required, if any.

## Applying the Maturity Model to Service Change Management

## Level 100 - Initial

- No-one in the organization is explicitly responsible for reviewing these messages and they are ignored.
- Announced changes take the organization by surprise.
- New features and capabilities are not taken advantage of.
- Unexpected deprecations disrupt business processes and harm the business.
- Service outages are not recognized and staff time is wasted attempting to resolve issues within their environment.

## Level 200 – Managed

- Someone in the organization reviews the message services on an ad hoc or infrequent basis.
- Changes are communicated, acted upon and tracked based on their judgement. Communication is not always timely or effective and many staff do not review, understand or act on the information provided.
- Little or no planning takes place to introduce or mitigate the effects of changes organizationally, though some teams may be effective at taking local action.
- Service desk or support roles review health advisories reactively in response to user reports.

## Level 300 – Defined

- Relevant staff receive Message Center updates via email
- Relevant IT staff meet regularly, probably integrating it into a weekly meeting, to review the latest Message Center messages. The "What you need to do to prepare:" section is reviewed and acted on, usually by passively notifying staff. Tasks are manually added to Planner or its equivalent for tracking and collaboration on completion.
- Relevant services are filtered via Preferences in Message Center.
- Message Center is configured to pump announcements to Planner as Tasks. Each week, relevant IT staff meet to review the new tasks and assess if action is required or not. Task status (Not started, in progress, or closed) is tracked.
- Change announcements that are unclear or have a negative impact are given a Thumbs Down feedback in Message Center. Support tickets may be opened as a result of Message Center posts.
- Reviewed and acted on messages may not be consistently archived.
- Relevant Service Health notifications are emailed to key roles and may be posted to the intranet, Teams and via email.
- Service desk staff are briefed on Service Health issues.

## Level 400 - Managed (Capable)

- Message Center is configured to pump announcements to Planner as Tasks. Each week, relevant IT staff meet to review the new tasks and assess if action is required or not. Task status (Not started, in progress, or closed) is monitored and reprioritized and impact of actions taken is reviewed.
- Relevant staff receive email updates. These may also be pushed into a Teams as Posts in relevant channels.
- Message Center is configured to pump announcements to Planner as Tasks. Regular meetings take place involving relevant IT staff and selected business staff (for example, the business owner of the intranet, department representatives, roles responsible for employee experience or learning and professional development) meet to review the new tasks and assess if action is required or not. Task status (Not started, in progress, or closed) is monitored and reprioritized and impact of actions taken is reviewed.
- The length of time that tasks remain open and the effect of actions taken is tracked and reported on.
- Change announcements that are unclear or have a negative impact are given a Thumbs Down feedback in Message Center. Support tickets may be opened as a result of Message Center posts. If the organization has the benefit of a proactive support team from Microsoft as part of their enterprise agreement, message center announcements that cause concern or question are brought to that team weekly for investigation.
- Selected changes are brought into the organization's existing change management processes, such as being brought before a Change Review Board. Bringing changes from Message Center or Planner into the enterprise change management tool that the Change Review Board and Change Owners use is a manual process.
- Service Health issues are assessed for impact and communicated appropriately and across multiple communication channels, with flagging of impact and severity. Staff heed notifications when issued. Mitigation options and advice are provided/implemented.
- Service desk staff are involved in developing responses to Service Health issues and are prepared to support staff as needed.
- Staff are advised when incidents are resolved and supported with any remediation needs.
- IT staff are engaged in preview activities such as Insider programs and use these to assess impacts and make recommendations.
- Horizon scanning proactively occurs, with other sources of change information such as the following are also reviewed as appropriate (weekly, bi-weekly, monthly, or annually), including:

- The Book of News published on the first day of the Microsoft Ignite and Microsoft Build conferences
- The monthly Technical Update Briefing that Microsoft can provide to its customers that have paid for access to a proactive support team
- The [product roadmap](https://www.microsoft.com/microsoft-365/roadmap) for Microsoft 365
- Internal business conditions, projects, and priorities

## Level 500 - Optimizing (Efficient)

- At Level 500, the organization has invested in a change management solution that goes beyond what Planner can offer. This solution is aware of who in the organization is responsible for managing what workload and is designed to streamline all processes for managing these changes.
- Workflows and communications processes are in place to automatically notify appropriate staff of incidents, issues and forthcoming changes.
- Some staff across the business are engaged in preview activities such as Insider programs and use these collaboratively assess impacts and make recommendations. These feed into strategic technology and business change activities.
- Impacts of changes are actively monitored, and new ways of working are introduced and updated in response to feedback and analysis.
- The organization actively provides feedback to Microsoft around the changes and requests changes via the Microsoft Feedback portal.
- Support staff actively maintain their knowledge of current and forthcoming technologies and are prepared when incidents or staff needs arise from these.

---

**Principal author**: [Michael Blumenthal](https://www.linkedin.com/in/michaelbblumenthal/)

---
