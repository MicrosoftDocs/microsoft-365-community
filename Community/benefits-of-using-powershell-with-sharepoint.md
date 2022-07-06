---
title: Benefits of using PowerShell with SharePoint
ms.date: 3/3/2020
author: veronicageek
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: sharepoint-powershell
localization_priority: 
description: "Benefits of using PowerShell with SharePoint"
ms.collection: M365Community
---

# Benefits of using PowerShell with SharePoint

## What is PowerShell?

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

[PowerShell](/windows-server/administration/windows-commands/powershell) is an automation scripting language from Microsoft, which was originally only available on Windows devices, and built on top of the .NET Framework.
Since 2016, we also have [PowerShell Core](https://github.com/PowerShell/PowerShell) which is open-source, cross-platform, and built on top of .NET Core.

The version that ships on Windows devices is called **Windows PowerShell**, and the cross-platform version is called **PowerShell Core** and is also available on Windows.

## PowerShell for SharePoint

In the SharePoint world, we have multiple [modules](/powershell/module/microsoft.powershell.core/about/about_modules) available, and which one to use mostly depends on your SharePoint infrastructure. Is it SharePoint on-premises? Is it SharePoint Online?

Let's have a look at all the different modules currently available for SharePoint.

### Client-Side Object Model (CSOM)

The _Client-Side Object Model_ is more intended for developers, as they will use it to build applications by accessing many SharePoint functionalities. But it can be used by administrators when native PowerShell cmdlets don't exist, or to create scripts.

### SharePoint PowerShell Snapin

Whenever we use PowerShell, we usually install the required module, and run ```Import-Module```. However, with _SharePoint on-premises_, before you can access the cmdlets (except if you're on the pre-loaded SharePoint Management Shell), you need to run ```Add-PSSnapin Microsoft.SharePoint.PowerShell```. Not a big deal, but something to know.

There's a lot of possibilities to manage your environment with the SharePoint on-premises cmdlets, as the module contains approx. 840 cmdlets.

### SharePoint Online Module (by Microsoft)

Microsoft also created a [module for SharePoint Online](https://www.microsoft.com/download/details.aspx?id=35588), however it contains approx. 162 cmdlets (late 2019).

That's a big drop from the on-premises version, isn't it? But when you think about it, it makes sense. With SharePoint Online, as you may know, there's a lot Microsoft is taking care of, therefore there's no need for us to manage databases, Service Applications, or even Web Applications as a few examples.

### PnP PowerShell (Patterns & Practices)

[PnP PowerShell](https://github.com/pnp/powershell) is a Community initiative/effort and is available on Github.
It combines complex CSOM cmdlets in the background, and gives us the look and feel of native PowerShell that we are familiar with. PnP.PowerShell (latest version) supports SharePoint Online only. For those using on-premises SharePoint, [PnP-PowerShell](https://github.com/pnp/PnP-PowerShell) (legacy version) works with SharePoint 2013, 2016, 2019 and SharePoint Online but is no longer being maintained.

Currently (late 2019), and depending on the SharePoint version, there are approx. 400 cmdlets, and 4 modules available for:

- SharePoint Online
- SharePoint 2019
- SharePoint 2016
- SharePoint 2013

### CLI for Microsoft 365

Also part of the PnP initiative is the [CLI for Microsoft 365](https://pnp.github.io/cli-microsoft365/). This allows you to manage your Microsoft 365 tenant and SharePoint Framework projects on any platform.

No matter if you're on _Windows_, _macOS_ or _Linux_, using Bash, Cmder or PowerShell, using the CLI for Microsoft 365 you can configure Microsoft 365, manage SharePoint Framework projects and build automation scripts.

## So why should I use PowerShell?

As mentioned at the beginning, PowerShell is an automation scripting language. Therefore, most of the tasks that require many 'clicks' or are repetitive _should_ be automated.
PowerShell is used primarily for **bulk actions**, or complex automation tasks mixed with other files format like .csv, .json, or .XML, and will **reduce most time consuming efforts** in the long run.

_If you need to create only one site collection, using PowerShell wouldn't really be beneficial._

### Real world scenario

Imagine it's Friday 4.00pm, you are just tasked to create 100 Site Collections, and you can't be late for a very important appointment that day. Do you think you can achieve that manually, (very) quickly so you can leave early? :cold_sweat:

Chances are... you're going to miss your appointment.

If you use PowerShell, it's likely to take less than 5 mins, and off you go!

### Anything else?

Sure, you have other purposes for using PowerShell in SharePoint of course.
Other than creating things, you can change/remove them all at once on multiple sites, extract information like Users/Groups/Permissions, and even integrate with other platforms like [Azure](https://azure.microsoft.com/) to automate your most complex tasks!

More examples where PowerShell is used:

- [Site Scripts & Site Designs](/sharepoint/dev/declarative-customization/site-design-overview)
- [WPF Applications](/dotnet/framework/wpf/getting-started/) (Graphical User Interfaces)
- [Reports on Site Collection Inventory](https://veronicageek.com/2019/get-nested-folders-files-count-folder-size/)

## Who should know PowerShell?

This question might be a bit tricky for some.

- **Administrators** should definitely know PowerShell. No question about that.
- **Site Owners** mostly delegate to administrators if there's a lot of activities to perform on their site(s).
- **End-Users** are unlikely to need PowerShell unless it's one of their interest.

PowerShell Development is also a known skill and usually coupled with other ones like C#, or SQL Server to only name a few.

## Why is it so important?

Managing SharePoint on-premises or online effectively and efficiently is crucial. This also applies to other platforms like Active Directory, Microsoft Exchange, or Systems Administration.

**_You don't need to be called a 'developer' to run a few cmdlets or create scripts_**.

If you live within the Microsoft ecosystem on a daily basis, you will likely use PowerShell at some point.

---

**Principal author**: [Veronique Lengelle, MVP](https://www.linkedin.com/in/veronique-lengelle-48a71b31)

---
