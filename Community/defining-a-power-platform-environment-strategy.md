---
title: Defining a Power Platform Environment Strategy
ms.date: 8/08/2020
author: Aaron Rendell
ms.reviewer:  
localization_priority: 
description: "Defining a Power Platform Environment Strategy"
ms.collection:  SPCommunity
---

# What is a Power Platform environment?

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

The Power Platform is Microsoft’s answer to the growing need in business for a way to build and customise professional-grade business solutions quickly, with the ability to connect to over 200 data sources including, SharePoint Online, Azure SQL, Twitter and more.

An environment is a space to store, manage, and share your organization's business data, apps, and flows. It also serves as a container to separate apps that might have different roles, security requirements, or target audiences. How you choose to use environments depends on your organization and the apps you're trying to build. For example:

•	You can choose to only build your apps in a single environment.
•	You might create separate environments that group the test and production versions of your apps.
•	You might create separate environments that correspond to specific teams or departments in your company, each containing the relevant data and apps for each audience.
•	You might also create separate environments for different global branches of your company.

For some, the concept of an ‘Environment’ in Power Platform is brand new. Unless you have been told or you have done your research, you would not know any different to there being a single environment or multiple.

## What type of environments are there?

Environments are containers that administrators can use to manage apps, automations, connections, and other assets; along with permissions to allow organisation users to use the resources.

There are multiple types of environments. The type indicates the purpose of the environment and determines its characteristics. The following table summarises the current types of environments that you might encounter.

Environment Type	Purpose
Developer	Developer environments are created by users who have the Community Plan license. They're special environments intended only for use by the owner, and they can't be shared with other users. Provisioning developer environments can't be restricted unless through a support ticket.
Only a single user account with the Community Plan has access.

Trial	Trial environments are intended to support short-term testing needs and are automatically cleaned up after a short period of time. They expire after 30 days and are limited to one user. Provisioning trial environments can be restricted to admins.

Sandbox	These are non-production environments, which offer features like copy and reset. Sandbox environments are used for development and testing, separate from production. Provisioning sandbox environments can be restricted to admins (because production environment creation can be blocked), but converting from a production to a sandbox environment can't be blocked.

Non-production environments. Enables the typical ‘Development’ and ‘Test’ environment isolation.
Default	These are a special type of production environment. Each tenant has a default environment that's created automatically. Its characteristics are discussed in the following section, The default environment.

Production	This is intended to be used for permanent work in an organization. It can be created and owned by an administrator or anyone with a Power Apps license, provided there is 1 GB available database capacity. These environments are also created for each existing Common Data Service database when it is upgraded to version 9.0 or later. Production environments are what you should use for any environments on which you depend.

## Why is the Default Environment special?

A single default environment is automatically created by Power Apps for each tenant and shared by all users in that tenant. Whenever a new user signs up for Power Apps, they're automatically added to the Maker role of the default environment. The default environment is created in the region closest to the default region of the Azure AD tenant.
There is specific guidance for the Default environment to call out because of its unique nature:
•	It’s automatically created with the first user in the region closest to the Azure AD tenant
•	New users that sign up for PowerApps are automatically added to the Maker role
•	Users are not automatically added to the Environment Admin role
•	The default environment can’t be deleted, but you can rename it – e.g. Personal Productivity.

Note:
•	No users will be added to the Environment Admin role of the default environment automatically. More information: Administer environments in Power Apps
•	You can't delete the default environment.
•	The default environment is limited to 32 GB of storage capacity. In case you need to store more data, you can create a production environment. More information: Provisioning a new environment

The Default environment should not be used to host production solutions. It’s designed to be an open environment that allows users to extend Office 365 and trusted applications or to build personal productivity applications that don’t affect many people.

## Why do I need to define a strategy?

Developing an environment strategy means configuring environments and other layers of data security (DLP) in a way that supports the productive development in an organisation, while securing and organising resources.

To follow application lifecycle management (ALM) principles, you'll need separate environments for app development and production. Although you can perform basic ALM with only separate development and production environments, we recommend that you also maintain at least one test environment that's separate from your development and production environments. 

When you have a separate test environment, you can perform end-to-end validation that includes solution deployment and application testing. 
Some organizations might also need additional environments for user acceptance testing (UAT), systems integration testing (SIT), and training.

Environment scenarios
Scenario 1	The ‘Out of the Box’, default environment.
Scenario 2	Scenario 1 + Dedicated departmental environments
Scenario 3	Scenario 2 + Dedicated application environments
Scenario 4	Multi-Tenant ALM environment separation.

Scenario 1 – Personal Productivity (default environment)
 
Uses include: Personal Productivity Apps and Flows, Custom SharePoint Lists and Library forms.

Scenario 2 – Departmental
 
Uses include: Personal Productivity Apps and Flows, Custom SharePoint Lists and Library forms and dedicated department environments.

Scenario 3 – Departmental and Application
Uses include: Default environment, dedicated department environments and a dedicated environment(s) for a single application.

Scenario 4 – Multi-Tenant ALM Approach
 
Uses include: Separating Power Platform environments across physical tenants. Could be used to separate Production, Staging and Development environments, or could be used for geo-location reasons.

## Recommendations / Best Practices

Based on successful experience with other customer engagements, below is a list of additional recommendations that can help make managing environments easier.
•	Assign your admins the Power Platform service admin or Dynamics 365 service admin role.
•	Restrict the creation of net-new trial and production environments to admins
•	Rename the default environment to ‘Personal Productivity’
•	Provision a new Production environment for non-personal apps/flows
•	Define and implement your DLP policies for your environments
•	When establishing a DLP strategy, you may need multiple environments for the same department
•	When establishing your Power Platform environment strategy, based upon your licencing, you may find that you need to provision environments without a Dataflex Pro database and also use DLP policies to restrict the user of premium connectors.
•	Establish a process for requesting access or creation of environments
•	Dev/Test/Production environments for specific business groups or application
•	Individual-use environments for Proof of Concepts and training workshops
•	Use a service account to deploy production solutions
•	Reduce the number of shared development environments
•	Share resources with Azure AD Security Groups
•	Provision environments with CDS instances in the appropriate region.

## Further Reading

•	Microsoft: https://docs.microsoft.com/en-us/power-platform/admin/environments-overview

---

**Principal author**: [Aaron Rendell](hhttps://www.linkedin.com/in/aaron-rendell/)

---
