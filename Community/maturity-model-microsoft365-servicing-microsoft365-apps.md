---
title: Maturity Model for Microsoft 365 Practical Scenarios – Servicing Microsoft 365 App
ms.date: 10/9/2023
author: michaelblumenthal
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: overview
ms.author: pamgreen
ms.service: microsoft-365
ms.localizationpriority: Low
description: Maturity Model for Microsoft 365 Practical Scenarios – Servicing Microsoft 365 Apps
ms.collection: M365Community
---

# Maturity Model for Microsoft 365 Practical Scenarios – Servicing Microsoft 365 Apps  

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

The [Maturity Model for Microsoft 365](microsoft365-maturity-model--intro.md) is a useful tool for considering high level business capabilities and competencies, providing benchmarking and planning guidance.  However, practical application of the Maturity Model to specific tasks and needs is not addressed in the Competency or Elevate documents. The Practical Scenarios documents seek to address this, providing easily digestible guidance and strategy for focused topics.

This Practical Scenarios document covers the servicing (frequent periodic upgrades) for the Office desktop apps (Word, Excel, PowerPoint, Outlook, OneNote, Access, Publisher and any others that appear in future), including those in Microsoft 365 plans, M365 Apps for Enterprise and any other plans that include desktop-installed applications.

## Introduction to Office Servicing

Microsoft releases a new version of Office every month or every six months depending on which update cadence you pick.  Each release is supported for a limited number of months, so you must plan to upgrade at least twice a year to maximize the security of the software and minimize the user impact of upgrading.

An organization may have Office desktop apps installed on most or all workstations (e.g. laptops and desktops) as well as servers.  Office mobile apps are separate apps and serviced separately.  Note that some servers running Office may not have internet access, which means that auto-upgrading as well as per-user license activation may not work.

Office Servicing can be a simple as letting machines automatically update each month, but that is often not feasible in enterprise environments due to the need to test them for compatibility with the organization’s standard desktop configurations and for compatibility with other line of business applications.

Organizations demonstrate increasingly mature Office servicing practices as follows. The key questions that a mature process should be able to answer include:

1. How many workstations run Office?
2. How many servers run Office?
3. What versions and builds of Office are in our environment?
      1. How does the version and build inventory break down by:
            1. Server
                1. What Server OS is on this server?
                2. Application Development lifecycle – Is this a Development, Test, QA, or Production server?
                      1. Are we servicing and validating Dev/Test/QA first, and Production last?
                3. Business unit
                4. Server owner / responsible party
                5. Application dependent on Office
                6. Which Office Apps are needed on which servers
            2. Workstation
                1. What workstation OS is on this machine
                2. Application dependent on Office
                3. Business unit
4. Can we map machines to users? Updates are deployed to machines, but communication about updates are sent to users.
5. How many machines have been upgraded in this upgrade cycle and in this reporting period? What is the percent complete?
6. When will we finish this upgrade cycle?
7. When does the currently installed version or build go out of support?
8. Do users know how to use the new features in the context of their daily business activities?

## Applying the Maturity Model to Service Change Management

### Level 100 - Initial

None of the questions are answerable. Many versions of Office are present in the environment and there is no ability to assess the inventory or its risks. Support incidents are frequent and time-consuming and a lack of subject matter expertise in the support process and staff is evident.

### Level 200 – Managed

The organization has begun its journey to process excellence. Efforts are made to collect the necessary data and report on the current state as well as to perform one upgrade a year. Some of the key questions can be answered, but keeping the data up to date is very challenging.

### Level 300 – Defined

The organization has established an upgrade cadence of either every 6 months or every month, depending on what is needed for their business. More of the key questions are answerable. Keeping the data up to date is challenging.

### Level 400 - Managed (Capable)

Most of the questions are answered, and a repeatable process is in place, but it is labor intense.

The Microsoft Roadmap is periodically reviewed and changes considered for both technical and staff impacts and benefits.

### Level 500 - Optimizing (Efficient)

All of the questions are answered, with answers frequently updated. Application compatibility testing is automated. Efforts are focused on process improvement rather than simply process execution.

---

**Principal author**: [Michael Blumenthal](https://www.linkedin.com/in/michaelbblumenthal/)

---
