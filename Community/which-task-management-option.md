---
title: What task management platform is best for me?
ms.date: 12/19/2022
author: dfrancoeur
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: microsoft-365
localization_priority: 
description: "A short guide on the many (many) options for managing tasks in M365 and how they stack up."
ms.collection: M365Community
---

# Which Task Management Tool is Right For Me

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

There are a crazy number of ways to manage tasks in Microsoft 365, some of which overlap, while others don’t. Where are all the places we can create tasks?

![Task-oriented apps](media/task-management-options/Tasks1.png)

## Why are there so many options?

Microsoft has offered a variety of tools to address different use cases for task management, from personal to enterprise. They have also created a number of overlapping user experiences without providing clarity around which tools communicate with one another, and which do not. This creates a huge amount of confusion for end users, in knowing what tool to use when and finding a way to see a holistic view of all their tasks.

The reality is there is no single **“best way”** to manage tasks, and we are still seeing more options being added (e.g., Loop), without a real coherent strategy to tie these options together.

## Microsoft Planner

![Microsoft Planner](media/task-management-options/Tasks2.png)

### Pros - Planner

- The Kanban “task board” is a tried and tested approach that many recognize and Planner has implemented it well
- Planner Tasks integrate well with our views in To Do, Teams, and Outlook
- Support for buckets, progress, labels, assignees, dates, priority, sub-tasks, attachments, comments
- Multiple ways to view information (by plan, by bucket, by progress)
- Tasks can be assigned to multiple people
- Useful filtering to find what you need
- Tasks can be copied or moved to other plans
- Respects underlying group membership
- Support for checklist within a task

### Cons - Planner

- Has seen some minor updates but nothing significant in quite some time
- No consolidation across planner plans
- Little to no extensibility or customization beyond out of the box configuration
- The API is very poor
- Ability to create automation of tasks through Power Automate

## Microsoft Lists

![Microsoft Lists](media/task-management-options/Tasks3.png)

### Pros - Lists

- Can be customized with endless additional metadata that your task list may require, and it is extremely flexible in terms of layout
- The Kanban “task board” is a tried and tested approach that many recognize
- Support for attachments, and comments (with @mentions)
- Can create multiple ways to view information (by plan, by bucket, by progress, or any other metadata you create)
- Tasks can be assigned to multiple people
- Useful filtering to find what you need
- Extremely flexible in terms of layout
- Respects underlying site/group membership
- Ability to centralize tasks across lists with minor customization (using things like Modern PnP Search web part or Highlighted Content web part)
- Ability to create automation of tasks through Power Automate

### Cons - Lists

- No built-in integration with other applications (e.g., Planner) therefore the assignment of tasks can easily get lost and end users have no way to see a holistic view of all their tasks across individual Lists (without additional configuration)
- Sub-tasks are not built-in and could be challenging to implement

## Microsoft To Do

![Microsoft ToDo](media/task-management-options/Tasks4.png)

### Pros - To Do

- Provides a consolidated view of Personal Tasks from To Do and Outlook, as well as Team Tasks from Planner Plans
- Allows for the creation of Shared Task Lists outside Planner Plans
- Support for lists, categories (web only), hashtags, assignees, dates, importance, sub-tasks, attachments
- Useful searching to find what you need
- Built-in notifications
- Tasks can be moved to other lists

### Cons - To Do

- The app’s benefits skew towards Personal Tasks rather than Planner Plans 
- Little to no extensibility or customization beyond out of the box configuration
- Can view Planner Plan tasks and “complete” them, but cannot interact with Planner Plans in more meaningful ways (e.g., add new tasks, view tasks by Plan, etc.)
- Personal tasks remain somewhat limited compared to other modern offerings due in large part to the unchanged underling infrastructure
- View of information remains quite rigid

## Tasks by Planner and To Do (Teams App)

![Tasks by Planner and To Do (Teams App)](media/task-management-options/Tasks5.png)

### Pros - Tasks by Planner and To Do (Teams App)

- Provides a consolidated view of Personal Tasks from To Do and Outlook, as well as Team Tasks from Planner Plans 
- Allows for the creation of Shared Task Lists and Planner Plans within existing Channels
- Support for categories (web only), assignees, dates, importance, sub-tasks, attachments
- Better navigation of Planner Plans, their attached Task Lists, and tasks
- Access to same views within Planner including List, Board, Charts and Schedule
- Support for creating new tasks, and reorganizing Planner Plans just like within Planner
- Notifications in Teams are useful

### Cons - Tasks by Planner and To Do (Teams App)

- The user interface can be very overwhelming and the app’s benefits skew towards Planner Plans rather than Personal Tasks
- The experience to view personal tasks is not as strong as To Do
- Little to no extensibility or customization beyond out of the box configuration
- Personal tasks remain somewhat limited compared to other modern offerings due in large part to the unchanged underling infrastructure
- View of information remains quite rigid

## Microsoft Loop

![Microsoft Loop](media/task-management-options/Tasks6.png)

### Pros - Microsoft Loop

- Quick and easy to get started which can be useful live in a meeting or in a Chat with Self
- Support for assignment and @mentions
- Tasks can be assigned to multiple people

### Cons - Microsoft Loop

- No built-in integration with other applications (e.g., Planner) therefore the assignment of tasks can easily get lost and end users have no way to see a holistic view of all their tasks across individual Lists.
- Cannot be used in Teams, only group chats and meetings
- Can be hard to find after they have been used
- Initially shared with specific people based on who the chat or meeting was with
- Sub-tasks are not supported

## Microsoft Outlook

![Microsoft Outlook](media/task-management-options/Tasks7.png)

### Pros - Microsoft Outlook

- If you like the web’s To Do interface, it’s another place to access it
- Allows for the creation of Shared Task Lists outside Planner Plans
- Support for lists (classic = folders), categories, assignees, dates, importance, sub-tasks, attachments
- Support for categories (web only), assignees, dates, importance, sub-tasks, attachments
- Useful searching to find what you need
- Tasks can be moved to other lists (folders)
- Built-in notifications

### Cons - Microsoft Outlook

- Seems redundant now even though the underlying tasks have not really evolved
- Odd old user interface (classic tasks) still available in desktop client
- Hashtags don’t work in classic
- Sub-tasks (steps) don’t work in classic

## OneNote

![OneNote](media/task-management-options/Tasks8.png)

### Notes - OneNote

- Can be used to assign tasks to yourself or others using the classic task interface
- Tasks show up in Outlook and To Do
- Only visible in desktop OneNote client
- Not very intuitive

## Office (Web) Comments

![ffice (Web) Comments](media/task-management-options/Tasks9.png)

### Notes - Office (Web) Comments

- Users can use the commenting feature within to now add “Tasks” to users
- Task does issue an email notification to the assignee
- Tasks are not integrated and are easily lost

## Azure Dev Ops (ADO)

![Azure Dev Ops (ADO)](media/task-management-options/tasks10.png)

### Notes - Azure Dev Ops (ADO)

- Geared towards development scenarios (dev and QA)
- Supports resource management
- Configurable to meet team needs
- Task does issue an email notification to the assignee
- Tasks are not integrated with other tasks and can mean multiple places to track

## Microsoft Project

![Microsoft Project](media/task-management-options/Tasks11.png)

### Notes - Microsoft Project

- Intended for more thorough project management including resources, schedule, budgets and timelines
- Provides a more modern visual experience, including Kanban view
- Supports enterprise portfolio management
- Integration with other task platforms is not great
- Requires additional licensing

## Dynamics 365 Project Operations

![Dynamics 365 Project Operations](media/task-management-options/Tasks12.png)

### Notes - Dynamics365 Project Operations

- Project Online features are embedded into Dynamics 365 Project Operations (D365 Project Service Automation)
- Expands capabilities pre-project into sales and quotes and post-project into expenses, invoicing and more
- Requires additional licensing

## Viva Goals

![Viva Goals](media/task-management-options/Tasks13.png)

### Notes - Viva Goals

- Viva Goals will support syncing of tasks from Azure Dev Ops, Project, and Planner to align daily tasks with organizational priorities

## What Option to Choose

For the time being, it is best to select an option that easily integrates (and communicates) easily with other Microsoft 365 solutions. However, each organization may need to handle tasks differently, based on their needs. The diagram below can be helpful in determining what task management solution to roll out at the personal level, but selecting a solution for enterprise project management or development projects will quite likely need to look beyond the confines of the defined safe space (i.e., the Task Hub).

![Task islands vs. task hubs](media/task-management-options/Tasks14.png)

---

**Principal author**: [David Francoeur](https://www.linkedin.com/in/dfrancoeur/)

---
