---
title: Maturity Model for Microsoft 365 Practical Scenarios – Microsoft 365 Service Health Management
ms.date: 12/16/2024
author: michaelblumenthal
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: article
ms.author: pamgreen
ms.service: microsoft-365
ms.localizationpriority:  Low
description: Maturity Model for Microsoft 365 Practical Scenarios – Microsoft 365 Service Health Management
ms.collection: M365Community
---

# Practical Scenarios – Microsoft 365 Service Health Management

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

The [Maturity Model for Microsoft 365](microsoft365-maturity-model--intro.md) is a useful tool for considering high level business capabilities and competencies, providing benchmarking, and planning guidance. However, practical application of the Maturity Model to specific tasks and needs is not addressed in the Competency or Elevate documents. The Practical Scenarios documents seek to address this, providing easily digestible guidance and strategy for focused topics.

This Practical Scenarios document covers service heal management as surfaced in the [Microsoft 365 Admin Center](https://admin.cloud.microsoft/?source=applauncher#/homepage), specifically in the Service Health Dashboard. Use of the Service Health Dashboard should be a key practice in operational management of Microsoft 365 (including Power Platform).

Note that we distinguish Service Health Management from Service Change Management. Service Health Management is about unplanned service failures and outages and communication about service health incidents.
Service Change Management is about planned change, including the arrival of new features and capabilities and the departure via deprecation of existing features and communication about these changes. 
Note that planned outages, such as for a Power Platform service upgrade, are communicated via the Message Center.
 
## Introduction to Service Health Management

The [Microsoft 365 Admin Center](https://admin.cloud.microsoft/#/homepage) provides the Service Health Dashboard, the Message Center, and an API through which service health and message center data can be accessed.

## Applying the Maturity Model to Service Health Management

## Level 100 - Initial

- No one in the organization is explicitly responsible for reviewing the Service Health Dashboard and health incidents and advisories are ignored.
- Service interruptions take the organization by surprise. They disrupt business processes and harm the business.
- Service outages are not recognized and staff time is wasted attempting to resolve issues within their environment, when it is actually Microsoft's responsibility to resolve the problem.

## Level 200 – Managed

-The Service Health Dashboard is reviewed only when incidents are reported to the organization's HelpDesk.
- No formal incident response plan has been created.
- Service desk or support roles review health advisories reactively in response to user reports.

## Level 300 – Defined

- Relevant staff receive incident notifications via email
- Someone in the organization reviews the Service Health Dashboard, perhaps as often as daily.
- The organization has documented a formal incident response plan.
- Relevant end-user-impacting advisories  are communicated to key roles and may be posted to the intranet, the HelpDesk ticketing system's landing page, Teams and via email.
- Service desk staff are briefed on Service Health issues as needed.

## Level 400 - Managed (Capable)

- Service Health issues are assessed for impact and communicated appropriately and across multiple communication channels, with flagging of impact and severity. Staff heed notifications when issued. Mitigation options and advice are provided/implemented.
- Service desk staff are involved in developing responses (usually workarounds as it's usually Microsoft's responsibility to fix the issue) to Service Health issues and are prepared to support staff as needed.
- Staff are advised when incidents are resolved and supported with any remediation needs.
- Incident response and disaster recovery plans are documented and tested on a regular basis, at least annually.  Many of the steps are manual.

## Level 500 - Optimizing (Efficient)

- Incident response and disaster recovery plans are documented and tested on a regular basis, at least annually. Much of the response is automated and the organization is seeking to continuously improve its response and maximize the level of automation.
- When a service goes down, a well-rehearsed plan is put into action.
- Service Health status and incident data is monitored through automated systems using the API 

---

**Principal author**: [Michael Blumenthal](https://www.linkedin.com/in/michaelbblumenthal/)

---
