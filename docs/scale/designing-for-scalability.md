# Introduction

This article talks about scalability of your solutions, this refers to this scenario - you have built your solution and tested on a site or library, you have demoed to your boss, they are very happy and then he goes "Hey now, great solution, can you get this out to 1,000 sites please?". 

The requirement has changed - to note, it is best to ask this question early. So you can plan for this and determine what kinds of points do you think about, when building your solution on this scale. 

To note, SharePoint Online supports 2,000,000 site collections (Nov 19) to give you context to how large implementations can in theory support. 

# Considerations when building solutions at scale

You now have your solution, so lets go through aspects of the solution you should ask of your solution, to see if you need to make amendments, or think about its design.

## Centralised, Decentralisation or Both

First question to ask yourself, do you need to deploy this solution 1,000 times or can you place a navigation link on 1000 sites referring to a single location? 

### Centralisation 

Centralisation refers to a single point in which assets and solution is referred to. 

For example, if you have a JavaScript based solution, consider locating the files into one place, not near the instance but somewhere within you farm or tenant that is readable to all. Changes to the central point reflect on all areas of usage. 

A scenario where this may apply e.g. if you have 1 Intranet each with 1000+ pages within. You deploy once rather than all 1000 times.

### Partial Centralisation

Partial centralisation is an option too, not all solutions can be centralised so look at the components of your design and see what can be centralised. 

A scenario where this may apply e.g. if you have 10 departments each with 100 sites within. You deploy 10 times rather than all 1000. Ideally, getting this number down will make your life easier - the less “copies” of your solution the better. 

### Decentralisation 

Decentralised solutions can only be deployed one to one with their instance. In this scenario, you deploy 1000 times. 

The goals change to reduce the implementation steps and how can I make this easier to deploy. Should I consider a scripted deployment?when considering you approach, is the effort of learning how to script deployment vs the actual deployment time. 

## Information Architecture

When designing for scale you will need to consider how this affects information architecture￼ approach. 

￼With large scale deployments, there are several factors to consider:
- consistent naming convention￼
- what level do you define columns e.g. list, web, site, ￼enterprise
- utilising inheritance
- deployment methods
- Usability are you using too much metadata? Is it affecting productivity?
- Multilingual configuration
- Describing the columns purpose and use in descriptions. 
- Form customisations

## Security

Security should always be an important consideration in any solution￼, no matter how complex or how quick solutions is built. 

Understand who can access your data￼￼ - ask yourself does this data contain any personal information?￼Is the data business critical or sensitive?￼

In SharePoint, there are three main models of security, one for users, SharePoint security groups and active directory groups. ￼

## Navigation




## Sites



## Multiple Environments



## Maintainability

Maintainability refers to the ease of making changes to your app, updates or cleanup aspects of your solution - how easy this is to achieve. 

Consider your solution - you have deployed to 1000 sites and you boss goes, “Great app, but can you add a column to each list, I really need this.”

## Manual vs Deployment

Deployment strategy is worth planning ahead of rollout of your new features, there are a number of factors to consider, in larger scale implementations:

-  Are you going to click 1000 times with a 10 step process or weigh up the effort to  learn PowerShell script to automate this. Personally, I consider the PowerShell route if a process goes beyond a few steps or if I get a sense the deployment will be repeated multiple times.
-  Not all requirements are correctly articulated by the business or interpreted by the implementer which introduces change to the scope or what features are deployed, especially after the first deployment.
- Introduce test environments and UAT to validate the requirements have been met.
- Measure the time it takes to deploy your solution in a single location, then estimate the total time for the number of times you would repeat the same steps.
- Outage, will the solution be disruptive to staff or users, is out of hours deployment required?

### Manual

If you prefer manual, there are some ways to reduce time to manually deploy your solution. Such as:
 - Choose the centralisation approach, as mentioned above, is there a way to setup your solution to be deployed from one location.
 - Know your URLs, such as _layout/15/XX links to settings, site contents, for manual deployments aim to jump directly to the page where the setting occurs, avoid navigating through SharePoint, extra clicks will slow you down.
 - Keep a log of your progress, so for very large implementations, you can pause and come back, refer to a list of how much of the deployment you have done - this can also serve as your checklist if you have a multi-step deployment.

### Script

For scripting, I highly recommend looking into PnP PowerShell library, there a lot of cmdlets design to work online and on-premises, there is plenty of blogs, examples or community members that can help you to get you started.

### Site Designs

Now there is Site Designs feature in SharePoint Online, which opens up a new way to deploy features.  These can create libraries, set permissions, branding and headings in Modern interfaces and call Flows containing more advanced scenarios


# Further Reading

Many related articles are in the works to go into each section in more detail. Watch here for updates. 

---

**Principal author**: Paul Bullock
**LinkedIn**: [**http://www.linkedin.com/in/pkbullock**](http://www.linkedin.com/in/pkbullock)
**Website**: [**capacreative.co.uk**](https://capacreative.co.uk/)

---