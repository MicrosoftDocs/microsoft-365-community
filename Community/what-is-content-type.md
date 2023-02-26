---
title: What is a content type?
ms.date: 3/3/2020
author: sympmarc
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: sharepoint-online
localization_priority: 
description: "What is a content type?"
ms.collection: M365Community
---

# What is a Content Type?

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## Basic Idea

The easy answer here is a Content Type is a type of content, but that isn't very helpful. A Content Type is like a business object: something that you move around your desk or computer every day.

SharePoint comes with some out of the box Content Types which represent generic things - like Item and Document - and some others which may be the same as what we use - like Event. When we create a new Content Type in SharePoint, we inherit from one of these generic Content Types and embellish it to represent the object we work with.

## Real World Example

You work with Content Types at home every day. You probably have grocery lists, bills, and maybe a mortgage around your house right now. Each of these objects are second nature to you; you don't think about what they are or what to call them.

For sake of discussion, let's say you do have a mortgage and you've put it into a manila folder in your drawer.

![Document in a manila folder](media/what-is-content-type/folder.png)

Wouldn't it be useful if you wrote some things on the outside of the folder so you could identify what was inside more easily? Maybe you'd add the date the mortgage was signed, the mortgage company, their phone number, and how much the mortgage was for.

![Document in a manila folder with metadata](media/what-is-content-type/folder-with-metadata.png)

Now, you may wonder why we're looking at a folder at all. Folders are supposed to be bad! But the analogy holds up: the folder is like the skin of the document, and we've added metadata on the outside to help us make sense of it.

## Back to Work

Now imagine you work at a mortgage company. Instead of one (or maybe two) mortgages, you're responsible for thousands. The Content Type becomes even more important, and you may want some additional metadata, like maybe the mortgage originator, the servicing company, and the mortgage due date.

![Document in a manila folder with metadata](media/what-is-content-type/folder-with-more-metadata.png)

We don't add these metadata columns just for fun. We decide to collect the metadata which will enable the use cases we want, but not too much more than that. For example, if we'd like to have a view which shows all the mortgages which are going to be due in the next month, we need the Content Type = Mortgage and the mortgage due date >= [Today] and mortgage due date <= [Today+30]. We can't satisfy that use case unless we've made the document a Mortgage and added the mortgage due date metadata column - and populated it!

## Extra Detail

Content Types can be defined in an individual site, in the Content Type Hub, or using Site Templates. We make this choice based on the *scope* where we want to use the Content Type. We may have a Content Type which only makes sense in the context of a single site, like perhaps a Benefits Description in the Human Resources site. Other Content Types may have utility across the tenant, like perhaps a Contract, if we want each department to store and manage their Contracts in their own sites.

## Summary

With Content Types, we can define the business objects which matter to us in our daily jobs. In many cases - whenever a piece of content matters to our organization - we want to create our own Content Types based on one of the generic ones to represent how we do our real work. The metadata we collect with each instance of the Content Type enables us to do our jobs better.

---

Principal author: [Marc D Anderson, MVP](https://www.linkedin.com/in/marcanderson/)
