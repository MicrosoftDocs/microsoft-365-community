---
title: Can Machine Learning be used to assign managed metadata attributes for items?
ms.date: 3/3/2020
author: sympmarc
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: concept-article
ms.author: pamgreen
ms.service: microsoft-365
ms.custom: sharepoint-online
ms.localizationpriority: Low
description: "Can Machine Learning be used to assign managed metadata attributes for items?"
ms.collection: M365Community
---

# Can Machine Learning be used to assign managed metadata attributes for items?

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

Metadata adoption is tough.  With the introduction of Machine Learning into the SharePoint ecosystem, Administrators and System Architects are asking if it can be leveraged to reduce our dependency on Users to assign metadata.  This article shares the results of an exploration into the technical capabilities of Machine Learning as it relates to SharePoint Managed Metadata.

## Basic Idea

Managed metadata is used to apply structure to unstructured data.  It adds information about the properties of items and their relationships to each other and to the business.  This information is usually not immediately available or easy to parse from the ‘human’ version of the item.  Managed metadata must be accurate and trustworthy, as it drives find-ability, workflow, data governance and lifecycle activities.

Machine learning uses algorithms to build a mathematical model based on sample data, known as "training data”.  It uses that model to make predictions or decisions without being explicitly programmed to perform the task.

In machine learning systems, metadata is often used as criteria in the algorithms.  Machine learning, therefore, uses a foundation of managed metadata to work.

Unsupervised Learning techniques and Active Learning algorithms (outlined in the detail section of this article) may be applicable to informal folksonomy tagging.  However, due to the need for accurate selections, It is not a solution for assigning the more formal and authoritative managed metadata.

Machine learning is an emerging service where much advancement and evolution are expected over the next few years.

## The Details

### Metadata Schema

Your Schema is your metadata organization model, it is the language of your business.  It is the lists and terms needed, what you’ll call them, their hierarchy and what the options are.  The Schema allows you to identify relationships between an item and the organization.

Our Managed Metadata Schema allows us to describe how these entities are connected, and to define their properties. It is a map of the business that gets applied to information, so people know the context of what they’re looking at.

### Machine Learning / AI

A metadata schema is a foundation for Machine Learning/AI.  Without a schema there is no authoritative structure to your business.  Without a schema, machine learning and other emerging and future systems, processes and software don’t understand the relationships of things or how they relate to the business.

### The Purpose of Metadata

With Managed Metadata, you can “talk to the search engine and to your Users.  You can tell them a lot about what the piece of content/item/file/data is about.  This provides important context that relates the information to the business.  People and search engines grasp it instantly.

Context examples include:

* How does this piece of information pertain to my business structure, which divisions or business units is it relevant to.
* What department, titles or people does it relate to.
* Which of my products or customers is it relevant to.
* Where in our workflow and processes does this piece of information have meaning.
* And within each of these criteria’s lifecycles; where is the item today.

## Extra Detail

### Machine Learning (as it relates to managed metadata)

Machine learning algorithms build a mathematical model based on sample data, known as "training data", in order to make predictions or decisions without being explicitly programmed to perform the task.

A few machine learning approaches that relate to Metadata:

* **Supervised learning** maps an input to an output based on example input-output pairs.
  * The algorithm builds a mathematical model from a set of data that contains both the inputs and the desired outputs.
  * Example:
    * Task to determine whether an image contained a certain object
    * Training data would include images with and without that object (the input)
    * Each training image would have a label (the output) designating whether it contained the object.

* **Classification algorithms** identify which set of categories a new item belongs.  They are used when the outputs are restricted to a limited set of values.
  * Examples:
    * Task that filters emails
      * Input would be an incoming email
      * Output would be the name of the folder in which to file the email.
    * Task that identifies spam emails
      * Output would be the prediction of either "spam" or "not spam"

* **Unsupervised learning** is also known as **self-organization**, or **spontaneous order**. Is a process where some form of overall order arises from mathematical cluster analysis.
  * Its primary use is in data analysis
  * The algorithm builds a mathematical model from a set of data which contains only inputs and no desired output labels.
  * Finds structure in the data, like grouping or clustering of data points.
  * Discovers patterns in the data, and can group the inputs into categories.

* **Active learning** algorithms are a special interactive case of machine learning where possible results are presented to a human user for selection.
  * Its most common uses:
    * Predict choice selections from long lists and present a narrowed-down list to the user.
    * Unlabeled data is abundant but manual labeling is expensive—such as during technical migrations.
  * May be a useful way to narrow-down long managed metadata selection lists.

* **Specialized** algorithms are mostly experimental today and have not found standard interpretation.
  * One such algorithm is **Meta learning**, where the main goal is to use metadata to improve the performance of existing algorithms or to invent the learning algorithm itself.
  
## Summary
  
People need managed metadata to find, work with, synthesize and make decisions about or with an item.  Systems need it too, as does workflow.  This information must be accurate and is critical to, among other things, effectively manage and administer data.  For example, you have to understand what the item is in order to decide if it should be retired/archived.

Your Schema is your metadata organization model, it is the language of your business.  The Schema allows you to identify relationships between an item and the organization.  A metadata schema is a foundation for Machine Learning/AI.  Without a schema there is no authoritative structure to your business data.

Businesses should focus on developing a schema that is complete and accurately represents all aspects of the business.  Applying that schema to items with managed metadata selections is a human-based activity.  It may be possible for advanced techniques in machine learning to reduce the choices of longer selection lists, however human action is required.

While this article has focused on technical capabilities, the information outlined does align with statements Microsoft has published about their strategic position for AI.  The following is from their AI product page.  (**emphasis is mine**)
  *"We believe that, **when designed with people at the center, AI can extend your capabilities**, free you up for more creative and strategic endeavors, and help you or your organization achieve more."*
  
 ---

Principal author: [Beth Hall](https://www.linkedin.com/in/beth-hall-stm)

---
