---
title: Maturity Model for Microsoft 365 Practical Scenarios – Microsoft 365 Service Change Management
ms.date: 10/9/2023
author: michaelblumenthal
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: article
ms.author: pamgreen
ms.service: microsoft-365
ms.localizationpriority: Low
description: Maturity Model for Microsoft 365 Practical Scenarios – Microsoft 365 Service Change Management
ms.collection: M365Community
---

# Practical Scenarios – Microsoft 365 Service Change Management

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

The [Maturity Model for Microsoft 365](microsoft365-maturity-model--intro.md) is a useful tool for considering high level business capabilities and competencies, providing benchmarking, and planning guidance. However, practical application of the Maturity Model to specific tasks and needs is not addressed in the Competency or Elevate documents. The Practical Scenarios documents seek to address this, providing easily digestible guidance and strategy for focused topics.

This Practical Scenarios document covers service change management as surfaced in the [Microsoft 365 Admin Center](https://admin.cloud.microsoft/?source=applauncher#/homepage), specifically in the Message Center. Frequent review of Message Center Messages should be a key practice in operational management of Microsoft 365 (including Power Platform).

Note that we distinguish Service *Change* Management from Service *Health* Management.  Service *Change* Management is about planned change, including the arrival of new features and capabilities and the departure via deprecation of exisitng features and communication about these changes. Service *Health* Management is about unplanned service failures and outages and communication about service health incidents.

## Introduction to Service Change Management

There are many ways to learn about upcoming changes.  There is the M365 Product Roadmap, there are blogs, there are announcements at conferences, there are podcasts and webinars, and more! The most direct communication, however, about what changes are coming to your specific tenant and approximately when is via [Message Center](https://admin.cloud.microsoft/?source=applauncher#/MessageCenter).  Message Center lives in the Microsoft Admin Center web app and the mobile Microsoft 365 Admin app. Both are accessible only to users [who have been granted access](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/message-center?view=o365-worldwide#frequently-asked-questions). 

![Messages in the Microsoft 365 Admin Center](media/maturity-model-microsoft365-servicing-microsoft365-service-change-management\advisories.jpg)

![Messages in the Microsoft 365 Admin Center mobile app](media/maturity-model-microsoft365-servicing-microsoft365-service-change-management\advisories-mobile.jpg)

Microsoft makes planned service changes to the M365 services daily, resulting in over 1400 change announcements per year. Effective IT operations will maintain awareness of current and future changes and assess their impacts on the organization and its people and processes. These changes are primarily announced via the [Message Center](https://admin.cloud.microsoft/?source=applauncher#/MessageCenter), with support from the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap) and supporting Microsoft official blogs.

Service Change management for Microsoft 365 involves triaging the change announcements (messages in the Message Center) and determining what action is required, if any.

## Applying the Maturity Model to Service Change Management

## Level 100 - Initial

- No-one in the organization is explicitly responsible for reviewing these messages and they are ignored.
- Announced changes take the organization by surprise.
- New features and capabilities are not taken advantage of.
- Unexpected deprecations disrupt business processes and harm the business.

## Level 200 – Managed

- Someone in the organization reviews the message services on an infrequent, reactive basis.
- Changes are communicated, acted upon and tracked inconsistently. Communication is not always timely or effective and many staff do not review, understand or act on the information provided.
- Little or no planning takes place to introduce or mitigate the effects of changes organizationally, though some teams may be effective at taking local action.

## Level 300 – Defined

- Relevant staff review Message Center updates. This may be via email or by scheduled reviews of Message Center messages in Message Center 
- Messages about relevant services are filtered via Preferences in Message Center.
- Relevant IT staff meet regularly, perhaps weekly, to discuss the latest Message Center messages. 
- For tasks identified from that review, task status (Not started, in progress, or closed) is tracked in some basic way, perhaps a spreadsheet. At this level, accountabiliy for task completion may be weak.
- End users may be notified of changes.  Effectiveness of communication is not measured.
- Change announcements that are unclear or have a negative impact are given a Thumbs Down feedback in Message Center. Support tickets with Microsoft may be opened as a result of Message Center posts.
- Reviewed and acted on messages may not be consistently archived.

## Level 400 - Managed (Capable)

- Message Center is configured to pump announcements to Planner as Tasks. Each week, relevant IT staff meet to review the new tasks and assess if action is required or not.
- Task status (Not started, in progress, or closed) is monitored and reprioritized and impact of actions taken is reviewed.
- As a result of the tasks identified, meetings take place between relevant IT staff and selected business staff.  For example, IT staff might meet with the business owner of the intranet, department representatives, roles responsible for employee experience, internal communications, and/or learning and professional development.
- The length of time that tasks remain open and the effect of actions taken is tracked and reported on.
- Effectiveness of change communications is measured.
- Change announcements that are unclear or have a negative impact are given a Thumbs Down feedback in Message Center. Support tickets may be opened as a result of Message Center posts. If the organization has the benefit of a having a dedicated proactive support team (sometimes refered to as a support pod) from Microsoft as part of their support agreement with Microsoft, message center announcements that cause concern or question are brought to that team weekly for investigation.
- Selected changes are brought into the organization's existing change management processes, such as being brought before a Change Review Board. Bringing changes from Message Center or Planner into the enterprise change management tool that the Change Review Board and Change Owners use is a manual process at this level.
- Other sources of change information such as the following are also reviewed at an appropriate (weekly, bi-weekly, monthly, or annually) cadence, including:

-- The Book of News published on the first day of the Microsoft Ignite and Microsoft Build conferences
-- Posts about product announcements from Microsoft staff and Microsoft MVPs on social networks such as X or LinkedIn 
-- The monthly Technical Update Briefing that Microsoft can provide to its customers that have paid for access to a proactive support team
-- The [product roadmap](https://www.microsoft.com/microsoft-365/roadmap) for Microsoft 365
-- The [Message Center Show on YouTube](https://www.youtube.com/@365MCS) 
-- Internal business conditions, projects, and priorities

## Level 500 - Optimizing (Efficient)

- At Level 500, the organization has invested in a change management solution that goes beyond what Planner can offer. This solution is aware of who in the organization is responsible for managing what workload and is designed to streamline all processes for managing these changes. This process may be enterprise-wide, so that its scope is to manage application change announcements across all applications in use in the enterprise, not just M365 applications.
- Workflows and communications processes are in place to automatically notify appropriate staff of forthcoming changes. Communications are as targeted as possible.   Effectiveness of communications is measured and feeds into continuous improvement efforts. 
- Some staff across the business are engaged in preview activities such as Insider programs and use these collaboratively assess impacts and make recommendations. These feed into strategic technology and business change activities.
- Impacts of changes are actively monitored, and new ways of working are introduced and updated in response to feedback and analysis.
- The organization actively provides feedback to Microsoft around the changes and requests changes via the Microsoft Feedback portal and their Microsoft acount team (if they have one).
- Support staff actively maintain their knowledge of current and forthcoming technologies and are prepared when incidents or staff needs arise from these.
- IT staff are engaged in preview activities such as Insider programs and use these to assess impacts and make recommendations.
---

**Principal author**: [Michael Blumenthal](https://www.linkedin.com/in/michaelbblumenthal/)

---
