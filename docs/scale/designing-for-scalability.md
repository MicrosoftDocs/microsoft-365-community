# Introduction

This article talks about scalability of your solutions, this refers to this scenario - you have built your solution and tested on a site or library, you have demoed to your boss, they are very happy and then he goes "Hey now, great solution, can you get this out to 1,000 sites please?". 

The requirement has changed - to note, it is best to ask this question early. So you have this new requirement, what kinds of points do you think about, when building your solution on this scale. 

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




## Security

Security should always be an important consideration in any solution￼, no matter how complex or how quick solutions is built. 

Understand who can access your data￼￼ - ask yourself does this data contain any personal information?￼Is the data business critical or sensitive?￼

In SharePoint there are three main models of security, one for users, SharePoint security groups and active directory groups. ￼

## Navigation



## Content Types

## Sites

## Manageability

## Maintainability

Maintainability refers to the ease of making changes to your app, updates or cleanup aspects of your solution - how easy this is to achieve. 

Consider your solution - you have deployed to 1000 sites and you boss goes, “Great app, but can you add a column to each list, I really need this.”

## Manual vs Deployment



## Classic and Modern SharePoint differ


# Tools that help you deploy for scale

Site designs

Power shell￼


# Examples


# Further Reading



---

**Principal author**: Paul Bullock
**LinkedIn**: [**http://www.linkedin.com/in/pkbullock**](http://www.linkedin.com/in/pkbullock)
**Website**: [**capacreative.co.uk**](https://capacreative.co.uk/)

---