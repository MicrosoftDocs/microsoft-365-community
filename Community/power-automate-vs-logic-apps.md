---
title: Power Automate vs Logic Apps
ms.date: 10/28/2020
author: pkbullock
ms.author: daisyfeller
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.service: power-platform
localization_priority: 
description: "Power Automate vs Logic Apps"
ms.collection:  SPCommunity
---

# Power Automate vs Logic Apps

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## What are these services

Power Automate and Azure Logic Apps are workflow services that can automate your processes, business, or system and integrate with Microsoft and 3rd party services with over 300 connectors. These powerful services are designed to get you going quickly, building the workflow between business services providing that familiarity without having the steep learning curve.

**Power Automate** provides a user-friendly and focused experience within Office 365 that can easily get end-users going once assigned an appropriate license.

**Azure Logic Apps** provide a user-friendly designer surface similar to Power Automate with the option to build complex integration solutions, utilise advanced development tools, DevOps and monitoring, if required.

Both options aim to significantly reduce the effort and quickly build and automate processes between services, allowing you to focus on higher-value tasks.

## Highlight key differences between Logic Apps and Power Automate

Whilst Power Automate is built on top of Azure Logic Apps, there are differences in terms of the environments they are used from, e.g. Office 365 and Azure, which provides unique features and optional methods of construction. Here are some of the following key differences:

| Description | Power Automate | Logic Apps |
|-------------|----------------|------------|
| Focus    | End Users and Makers in Office 365   | IT Pros, Developers, Admins using Office 365 and Azure Services |
| Licensing Model* | Per-User License in Office 365 | Consumption-Based or Fixed Pricing Model via an Azure Subscription |
| Flow Creation | Web-Based Designer, Web and Mobile UI | Visual Studio, JSON Definition and Web-Based Designer |
| Restricting Connectors | [Data Loss Prevention](/power-platform/admin/wp-data-loss-prevention) | [Azure Policy](/azure/logic-apps/block-connections-connectors) |
|Error Handling| Flow Checker - providing a list of errors within the Flow | Save Failed - highlighting errors  |
|Trigger Types | Automated, Instant, Scheduled, UI Flow, Business Process  | HTTP (Automated), WebHook, Scheduled, HTTP Call (Manual)  |

> *Check out the license plan details for each of the services, this article only serves as a guide not pricing information.  

For a detailed comparison, check out: [Compare Power Automate and Azure Logic Apps](/azure/azure-functions/functions-compare-logic-apps-ms-flow-webjobs#compare-microsoft-power-automate-and-azure-logic-apps)

## What tools you can use to build each of them

Focusing on the Microsoft options, there are a variety of tools that can be used to create your Flows within both of the services.

### Web-Based Designer tool

Applies to: **Power Automate** and **Logic Apps**

Both tools have a rich web-based design tool to author the Flows, connect to services and monitor their usage. For example, the experience offers:

* Design Canvas for adding triggers (what starts your Flow), connectors (the services you integrate with)
* Expression editor for advanced manipulation of input/output values
* Flow Checker - these are presented differently but inform you that the Flow you have created contains an error that needs to be rectified before saving.
* History and Connector status  - after a Flow run provides useful information to see what information passed through a Flow

Since both tools have this, learning Power Automate can be easily transferrable to Logic Apps if your requirements are better suited in the other product.

**Power Automate - web based designer**
![Power Automate Web Designer.](media\power-automate-vs-logic-apps\power-automate-example.png)

**Azure Logic Apps - web based designer**
![Azure Logic Apps - web based designer](media\power-automate-vs-logic-apps\azure-logic-app-example.png)

Power Automate flows created before September 2020 can be exported to Logic Apps. If you are working with the Azure Portal it will require some knowledge of JSON, or for a friendlier experience using Visual Studio, check out the docs to consider your approach: [Export flows from Power Automate and deploy to Azure Logic Apps](/azure/logic-apps/export-from-microsoft-flow-logic-app-template)

### Mobile App

Applies to: **Power Automate**

For iOS and Android, there is a Power Automate app that can allow you to build Flows, quickly and control existing Flow settings. The app includes:

* a designer surface that will enable you to add and edit actions
* create from templates
* manage existing flows - if you want to quickly create a Flow on the move
* there isn't an expression builder or the ability to add parallel branches.

![Mobile view of Power Automate.](media\power-automate-vs-logic-apps\mobile.jpg)

### Visual Studio

Applies to: **Logic Apps**

Visual Studio is an enterprise grade integrated development environment that allows you to create cloud, ASP.NET C#, VB, Visual J#, Xamarin projects including Windows API, Forms, Windows Presentation Foundation apps even classic SharePoint On-Premises Farm & Sandbox solutions.

Visual Studio supports working with Azure solutions, including Logic Apps, that allows you to connect to a subscription and provides a logic app editor experience.

For further information on editing Logic apps with Visual Studio, please refer to [Manage logic apps with Visual Studio](/azure/logic-apps/manage-logic-apps-with-visual-studio).

### Visual Studio Code

Applies to: **Logic Apps**

Visual Studio Code is a free and open-source code editor with wide-range support for programming languages with IntelliSense, extensions to select the tools you work with extending the functionality of the tool as best fits the project you are working on.

![Visual Studio Code.](media\power-automate-vs-logic-apps\example-visual-studio-code.png)

You can install the extension (Azure Logic Apps for Visual Studio Code) from the Marketplace - [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-logicapps)

### Visio

Applies to: **Power Automate**

Visio Plan 2 offers the feature to create a Business Process Model and Notation (BPMN) diagrams and export for Power Automate.

For more details of this feature, visit the Power Automate announcement for more information [Export Visio diagrams to Microsoft Flow is now generally available](https://flow.microsoft.com/blog/export-visio-diagrams-to-microsoft-flow-is-now-generally-available/)

## Getting started and points to consider

### Who will create the Flows

When considering Power Automate and Logic Apps, who will create them? Is this intended for staff to develop on-demand quick flows, or will you this integrate into a series of backend services, that your ICT service needs to ramp up on?

#### Learning Power Automate

For users and staff, there is a set of courses on [Microsoft Learn training](/training/browse/?terms=Automate&products=power-platform) if you want to know more about building flows to gain more in-depth knowledge about the usage of the services.

#### Learning Azure Logic Apps

For ICT or SME users looking to improve their knowledge, there is a set of courses on [Microsoft Learn training](/training/browse/?products=azure&terms=Logic%20Apps) if you want to know more about Logic Apps to gain a deeper understanding about the usage of the services and how they can integrate with a range of connectors.

### Consider the cost of connectors

What services do you intend to connect with?, are they Office 365?, Azure or 3rd Party API.

This is quite important to work out ahead of time as different connectors bear a "Premium" or "Enterprise" (in the case of Logic Apps) which affect the overall cost of running the workflow in your decision-making process.

You may find that within your Office licenses you already have what you need to start building Flows with Power Automate - however for Premium connectors, additional licenses may be required.

For Logic Apps, you can use the [Azure Calculator](https://azure.microsoft.com/pricing/calculator/) to estimate the cost of your application. Bear in mind since Logic Apps act as a glue between services, ensure you include the cost of the services that the Logic Apps connect to, e.g. Azure Resources, Office 365, third-party APIs.

### Security

Security is an essential factor with considering the usage of these services, as these can connect to a range of 3rd Party sources internally and externally, you may want to consider implementing a Data Loss Prevention policy or Azure Policy to restrict the usage of connectors.

In both products, security should always be considered and determine an appropriate policy for your organization.

---

**Principal author** [Paul Bullock, MVP](https://www.linkedin.com/in/pkbullock)

I invite authors with their knowledge on this topic to contribute to this article, sharing their experience.

---
