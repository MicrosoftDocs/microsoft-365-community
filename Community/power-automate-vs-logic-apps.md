---
title: Power Automate vs Logic Apps
ms.date: 3/9/2020
author: pkbullock
ms.reviewer: Joanne Hendrickson
localization_priority: 
description: "Power Automate vs Logic Apps"
ms.collection:  SPCommunity
---
# Power Automate vs Logic Apps

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## What they are

Power Automate and Azure Logic apps are workflow services that can automate your processes business or system and integrate with Microsoft and 3rd party services with over 300 connectors - these powerful services are designed to get you going quickly building the workflow between business services providing that familiarity without having the steep learning curve.

**Power Automate** are built _on top of Azure Logic apps_ to provide both a user friendly and focused experience within Office 365 that can easy to get end-users going once assigned a appropriate license.

**Azure Logic apps** provide the same user friendly designer surface as Power Automate with the option to integrate on a more technical level with other services, advanced development tools and complex solutions, if required.

## Highlight key differences between logic apps and power automate

As the PowerAutomate and Azure Logic apps fundamentally use the same workflow engine, there are differences in terms of their environments they are used from e.g. Office 365 and Azure, which provides additional features in the related scope to staff. Here are some of the following key differences:

| Description | Power Automate | Logic Apps |
|-------------|----------------|------------|
| Focus    | End Users and Makers in Office 365   | IT Pros, Developers, Admins using Office 365 and Azure Services |
| Licensing Model* | Per-User License in Office 365 | Consumption Based or Fixed Pricing Model via an Azure Subscription |
| Flow Creation | Web Based Designer, Web and Mobile UI | Visual Studio, JSON Definition and Web Based Designer |
| Restricting Connectors | [Data Loss Prevention](https://docs.microsoft.com/en-us/power-platform/admin/wp-data-loss-prevention) | [Azure Policy](https://docs.microsoft.com/en-us/azure/logic-apps/block-connections-connectors) |
|Error Handing| Flow Checker - providing a list of errors within the Flow | Save Failed - highlighting errors  |
|Trigger Types | Automated, Instant, Scheduled, UI Flow, Business Process  | HTTP (Automated), WebHook, Scheduled, HTTP Call (Manual)  |

>> *Check out the license plan details for each of the services, this article only serves as a guide not pricing information.  

For a detailed comparison, check out: [https://docs.microsoft.com/en-us/azure/azure-functions/functions-compare-logic-apps-ms-flow-webjobs](https://docs.microsoft.com/en-us/azure/azure-functions/functions-compare-logic-apps-ms-flow-webjobs#compare-microsoft-power-automate-and-azure-logic-apps)

## What tools you can use to build each of them

Focusing on the Microsoft options, there are a variety of tools that can be used to create your Flows within both of the services

### Web Based Designer tool
Applies to: **PowerAutomate** and **Logic Apps**

Both tools have a rich web based design tool to author the flows, connect to services and monitor their usage. For example, the experience offers:

* Design Canvas for adding triggers (what starts your flow), connectors (the services you integrate with)
* Expression editor for advanced manipulation of input/output values
* Flow Checker - these are presented differently but inform you that the Flow you have created contains an error that needs to be rectified before saving.
* History and Connector status  - after a flow run provides useful information to see what information passed through a Flow

Since both tools have this, learning Power Automate can be easily transferrable to Logic Apps if your requirements are better suited in the other product.

**Power Automate - web based designer**
![Power Automate Web Designer](media\power-automate-vs-logic-apps\power-automate-example.png)

**Azure Logic Apps - web based designer**
![Mobile view of Power Automate](media\power-automate-vs-logic-apps\azure-logic-app-example.png)

**Did you know you can export from Power Automate into Azure Logic apps?** Yes, you can. If you are working with the Azure Portal it will require some knowledge of JSON, or for a more friendlier experience use Visual Studio, check out the docs to consider your approach: [https://docs.microsoft.com/en-us/azure/logic-apps/export-from-microsoft-flow-logic-app-template](https://docs.microsoft.com/en-us/azure/logic-apps/export-from-microsoft-flow-logic-app-template)

This is a great feature - giving you more flexibility - if you Flow evolves overtime or you realise that you need more integration options or a different licensing approach, you can port over to Azure Logic Apps.

### Mobile App
Applies to: **PowerAutomate**

For iOS and Android, there is a Power Automate app that can allow you to build Flows, quickly and control existing Flow settings. There is a designer surface that allows you to add and edit actions, create from templates, manage existing flows which is great if you want to quick create a Flow on the move - however there isn't an expression builder or the ability to add parallel branches.

![Mobile view of Power Automate](media\power-automate-vs-logic-apps\mobile.jpeg)

### Visual Studio
Applies to: **Logic Apps**

### Visual Studio Code
Applies to: **Logic Apps**

Visual Studio Code is a free and open-source code editor with a wide range support for programming languages with IntelliSense, extensions to select the tools you work with extending the functionality of the tool as best fits the project you are working on.

![Visual Studio Code](media\power-automate-vs-logic-apps\example-visual-studio-code.png)

You can install the extension (Azure Logic Apps for Visual Studio Code) from the market place - [https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-logicapps](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-logicapps)

### Visio
Applies to: **PowerAutomate**

Visio Plan 2 offers the feature to create diagrams for Power Automate


// COMPLETE //



## Use cases for choosing an approach

These services are designed to integrate on a range of services, there are a few deciding factors when considering which option to use:

### Audience

Are you intending for staff or technical resource to use the service?


### Connectors

What services do you intend to connect with?, are they Office 365?, Azure or 3rd Party API. This is quite important to work out ahead of time as difference connectors bear a "Premium" or "Enterprise" (in the case of Logic Apps) which affect the overall cost of running the workflow in your decision making process.

### Security

Security is an important factor with considering usage of these services, as these can connect to a range of 3rd Party sources internally and externally, you may want to consider implementing a Data Loss Prevention policy or Azure Policy to restrict the usage of connectors. In both cases, security should always be considered and its additional setup overhead if you haven't implemented this.

### Licensing



## What you need to get started

### Power Automate

There is a set of courses on [Microsoft Learn](https://docs.microsoft.com/en-us/learn/browse/?terms=Automate&products=power-platform) if you want to know more about building flows to gain deeper knowledge about the usage of the services.


### Azure Logic Apps


There is a set of courses on [Microsoft Learn](https://docs.microsoft.com/en-us/learn/browse/?products=azure&terms=Logic%20Apps) if you want to know more about Logic Apps to gain deeper knowledge about the usage of the services.


### Security Considerations


---

Principal author: [Paul Bullock, MVP](https://www.linkedin.com/in/pkbullock)