--- 
title: How to Share Org-Wide Communications in Microsoft 365
ms.date: 8/13/2020 
author: eemancini
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: how-to
ms.author: pamgreen
ms.service: microsoft-365
ms.custom: sharepoint-online
ms.localizationpriority: Low
description: How to Share Org-Wide Communications in Microsoft 365
ms.collection: M365Community 
--- 


# How to Share Org-Wide Communication in Microsoft 365

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

Org-wide communication supports employees’ understanding of the organization, sharing timely updates, creating the company culture, driving employee engagement, sending crisis communications, and creating opportunities for discussion, innovation, and feedback. Relying on one communication channel - typically email - to get all these different messages across risks losing your audience to the deluge of emails in their inbox and reduced employee engagement. Within Microsoft 365, organizations have many communications channels to choose from (email, Teams, Viva Engage, SharePoint), and the best solution in each case will ultimately depend on:

- Company culture
- Company size
- Audience
- Persistence of the message
- Intent of communication
- Integration across Microsoft 365

The goal is to share the right information to the right people at the right time.

## Company Culture

The information a company chooses to circulate, and the way this information is shared greatly impacts the company culture. The core values and mission of your company should be taken into consideration as you determine the best solution for sharing different types of information.

### Open Communication

In a company that values transparency, updates come from multiple levels of the organization, and the focus is on enabling employees to share information independently.

#### SharePoint News

Sharing company updates through [SharePoint news](https://support.microsoft.com/office/create-and-share-news-on-your-sharepoint-sites-495f8f1a-3bef-4045-b33a-55e5abe7aed7) offers the ability to have many different contributors (based on Site Owner and Member permissions) across the organization. Since SharePoint news is a SharePoint page under the covers, you get all the benefits of a rich layout, ability to embed content from other Microsoft 365 apps, and discoverability within Microsoft Search.

Each department can share updates through SharePoint news on their own site. The intranet homepage can have a web part showing all news rolled up from all sites, increasing the visibility of these essential departmental updates and removing Corporate Communications or IT as the roadblock to post on the intranet homepage. Site owners benefit from decentralized content ownership with immediate access to share updates, and employees benefit from this centralization of updates by having one trusted place to check on the intranet homepage - just like they had when it was an email in their inbox. The news can also appear on each site’s homepage providing different ways to consume the content.

By default, comments are turned on for SharePoint news posts, inviting all employees to engage with the information which has been shared. Comments are connected to the page itself, eliminating the challenges with reply-all threads and aligning all responses in one location - much more straightforward than navigating multiple emails.

#### Viva Engage

[Viva Engage](https://www.microsoft.com/microsoft-viva/engage) excels at supporting serendipitous connections across your organization and creating communities for knowledge sharing, special interest groups, or communities of practice in an informal setting. Viva Engage communities are self-service and most successful when run independently by interested parties. In an organization with open communication, Viva Engage is an excellent place to socialize, crowd source ideas and solutions, informally share updates, increase communication between executives and employees, and break down silos initiating cross-department collaboration.

### Restricted Communication

In a company with formalized and restricted internal communications (often in heavily regulated industries where certain open communications introduce risk), the solutions for org-wide updates need much greater control over who can contribute.

#### SharePoint News: Organization News

SharePoint news can support situations where authors must be restricted. The news web part allows the selection of one site, multiple sites, or all sites associated with a hub, so you may choose only the sites where there is governance over the communications. Additionally, you may designate a site as [organization news](/sharepoint/organization-news-site). The organization news site will have a signifier in the site title - it appears in a highlighted box - helping these news posts to stand out as different visually.

#### Dynamic Distribution Groups

[Dynamic distribution groups](/Exchange/recipients/dynamic-distribution-groups/dynamic-distribution-groups) are mail-enabled Active Directory groups where the membership list is calculated each time a message is sent. These groups can replace your current company-wide email distribution list (which is typically manually maintained as employees join or leave the company). The dynamic distribution group can be created with a set of rules to control membership, and, most importantly, moderators may be added to control who can send messages to this list. Dynamic distribution groups support top-down communication and remove the ability for employees to reply-all and clog inboxes. Using a dynamic distribution group to email org-wide communications is the traditional method for sharing updates (with the added benefit of a dynamically updated distribution list), which may work best with organizations that have not launched an intranet.

## Company Size

What works for sharing information at a company of 6 may not be scalable for a company of 30,000.

### Small to Mid-Sized Companies

At a smaller company, you likely know every person that works there, and you understand their role in the organization. With fewer people, there is typically a lower volume of communication to keep up with. Your organization may not need a list of different communication channels to ensure the information is received, and employees feel comfortable sharing their feedback. Company updates via email can be sustainable at this size. Building better practices to centralize information in your intranet and sharing updates through SharePoint news can pay off greatly for an organization expecting growth.

#### Org-Wide Team

Within Microsoft Teams you can make an [org-wide team](/microsoftteams/create-an-org-wide-team) that supports up to 10,000 members. The org-wide team members will be automatically added and removed as individuals join or leave the company, like the dynamic distribution groups. While Teams are meant for collaboration, smaller organizations may find it useful to collaborate and communicate in the same place. Company updates may be shared in the associated SharePoint site and added as a tab to the org-wide Team or added as a connector, so the news posts appear in channels, notifying Teams members.

The persistent chat in channels supports threads allowing employees to dive deeper into conversations around the company updates in one place. It is possible to link to these threads, share a thread in Outlook, and save a thread for later (which you can [access in your Delve profile](https://support.microsoft.com/office/group-and-share-documents-in-office-delve-da0c5804-01ef-4edd-8b87-e576b19bef3e#:~:text=You%20can%20also%20keep%20track%20of%20documents%20in,with%20others.%20Remove%20a%20document%20from%20a%20board)). One of these company updates may prompt an action item. An employee can quickly grab the link to the thread, navigate to a different team, and post in that channel about the next steps. For companies small enough to sustain communication and collaboration on work in one place, using an org-wide Team can reduce the friction between receiving company updates to acting on them.

[Notification settings in Teams](https://support.microsoft.com/office/manage-notifications-in-teams-1cc31834-5fe5-412b-8edb-43fecc78413d) are available for the app, but not each Team. Be aware that these notifications are most useful when signifying to an employee there are action items to be completed in another Team related to getting work done. An overload of notifications in Teams will recreate the signal to noise ratio problem in email where there is no differentiation of something to be consumed versus something to be done.

### Large Company

At a larger company, you likely know your team and a small subset of the rest of the organization. New names are appearing in emails and your intranet daily without the context of who-does-what. Having all communications across the company in one channel (email) is incredibly overwhelming and could consume hours. There is a great benefit for larger organizations to divide their company updates between the intranet (and potentially also sent via email), collaboration to Teams, and social to Viva Engage to allow employees to focus on the tasks at hand. A typical morning may start with an employee navigating to the intranet to see the company news, then shifting to email and Teams to see action items to complete (which often appear within [To Do](https://support.microsoft.com/todo) or [Planner](https://support.microsoft.com/planner)). As timely work is completed, an employee may then navigate to Viva Engage to engage socially with colleagues, share knowledge, or engage in a special interest group.

## Audience

One of the most significant benefits of multiple communication channels is the ability to have a variety of audiences. Sending an email to the entire global company about region-specific Human Resources information adds noise to inboxes for employees outside that region and wastes employees’ time as they try to determine how this message applies to them. In the worst-case scenarios, the noise can become so loud employees stop trying to stay up to date on information and assume the critical messages will escalate enough to reach them.

Viva Engage, email, Teams, and SharePoint news (with [audience targeting](https://support.microsoft.com/office/overview-of-audience-targeting-in-modern-sharepoint-sites-68113d1b-be99-4d4c-a61c-73b087f48a81)) all support the ability to create different sets of people to target your communications better. Viva Engage, as an enterprise social network, is a natural place to connect with people outside your day-to-day teammates. Email can be targeted to one person or a variety of email distribution lists. Teams supports collaboration on work, which is a known set of individuals. SharePoint news audiences can range from a smaller group when connected to a team site or the whole company when connected to a communication site.

### Managing Audience

Once you identify who your message needs to reach, it is essential also to consider who can control the membership to this audience. Employees have access to create communities within Viva Engage. Many organizations allow self-service creation of Teams or SharePoint sites. Email distribution lists require IT (or other internal) support. If your audience is informal or dynamic and driven by employees, the self-service options will provide your communicators with the quickest path to sharing the right information to the right group. If the audience is company-wide or more formal, having IT (or other internal support) manage the membership puts controls in place and can help you formalize the process of adding or removing members. Consider the urgency in adding or removing members and what delays this may cause. For org-wide communication, dynamic distribution groups strike a balance between IT control and immediate updates as the organization’s members change over time.

## Persistence of Message

Each communication channel has a different lifespan for messages. Viva Engage threads last relatively long while Teams chat is meant for quick conversations to keep collaboration moving forward. Emails are only accessible to current employees, while SharePoint news supports new employees accessing previous updates. Companies may have limited retention policies deleting emails after a specific amount of time has passed. SharePoint news’ connection to the intranet gives it the longest lifespan of all the communication channels, as it is centered where employees frequently search for information and content to support their day-to-day work. SharePoint news also provides access for future employees to see historical company updates, speeding up their onboarding as they better understand the organization.

## Intent of Communication

Org-wide communication can have a variety of intents from an update on the business to a call-to-action for involvement in a project or a fun social engagement between colleagues. Each communication channel supports a different context of working, which should be used to support your message.

The ability for all employees to informally post makes Viva Engage an excellent place to source knowledge, share ideas, and engage with leadership. Employees can participate in these threads creating strong two-way communication. Most Viva Engage communities are open to the whole organization improving the discoverability of content.

Your colleagues are actively working and solving problems within Teams. Sharing project updates, action items, or discussing deliverables makes sense in this context of getting work done. Employees can engage in threads to clarify, discuss further, and come to decisions for the next steps.

SharePoint news supports more formal updates from a small number of authors to a broader audience, which is typically informative with no action items. The level of engagement is lower as people share reactions to the news shared in the comments and are not expanding the conversation.

Org-wide emails for a company update support urgent and timely messaging as most employees are in their inboxes all day. Emails are a good way to share one-way information where reactions, comments, or further discussion does not need to be captured. Email can also be a second way to share a SharePoint news post. This allows for rapid content updates and amendments within the news post as you receive feedback or additional questions.

## Integration Across Microsoft 365

Sharing org-wide information in one place might not be enough to support your message and amplify the visibility. The current adoption of the communication channel and company goals may influence how many places your message needs to appear for the correct level of engagement.

Viva Engage has a SharePoint web part and can be added as a tab in Teams. Embedding Viva Engage on your intranet homepage prioritizes social connection and removes friction for employees navigating to another app. Similarly, adding Viva Engage to Teams supports moving social conversations outside of channels meant for collaboration while keeping it easy to engage in another communication channel. Viva Engage notification settings can be customized to send employees emails for messages they missed.

Teams does not have a SharePoint web part, and channel conversations do not appear anywhere else in SharePoint. If a small to mid-sized organization chooses to  use an org-wide Team to replace Viva Engage for social interaction, there is no out of the box way to embed this in your intranet. This risks decreased engagement as employees adjust to sharing in a new platform. SharePoint Team Sites add a helpful link in the left navigation to Teams when a Team is first connected, which can help employees understand the connection with the SharePoint site. The files tab you see in Teams is the SharePoint document library, and there is a link here as well to navigate to the SharePoint site. Teams notification settings can also be customized to send employees emails for messages they missed.

Email appears in Outlook and the Outlook web application only. Individual emails can be sent to the [Microsoft 365 Group](/microsoft-365/admin/create-groups/compare-groups#microsoft-365-groups) that is connected to a Team. There are also email addresses for each channel within a Team. Individual emails may also be sent to Viva Engage communities, which also have a Microsoft 365 Group email address. Emails can be saved as a PDF to be added to SharePoint pages, or the content can be copied and pasted, though it is most effective to start org-wide communication as a SharePoint news post first and then email the news post to appropriate parts of the company.

## Conclusion

To make your org-wide communications more effective, engaging, and actionable, consider the best Microsoft 365 communication channel to support your needs. Evaluating the impacts of your company culture, size, and audience, the persistence of the message, the intent of the communication, and necessary integration across Microsoft 365 will help you navigate what to use when. What works for a small, transparent company will not work for a large, regulated global company. The variety of options ensures you will find a communication channel within Microsoft 365 that is a close fit for your needs.

## Resources

- [The Evolution of Company-wide Email Communication to SharePoint News](/microsoft-365/community/evolution-of-company-wide-email-communication-to-sharepoint-news)

---

**Principal author**: [Emily Mancini, MVP, UXMC](https://www.linkedin.com/in/eemancini/)

---
