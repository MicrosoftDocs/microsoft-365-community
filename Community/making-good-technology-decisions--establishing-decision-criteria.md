---
title: "Making Good Technology Decisions Establishing Decision Criteria"
ms.date: 3/29/2021
author: sympmarc
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: microsoft-365
localization_priority: 
description: "Making Good Technology Decisions: Establishing Decision Criteria"
ms.collection: M365Community
---

# Making Good Technology Decisions: Establishing Decision Criteria

* Part 1: Microsoft 365 - Making Good Technology Decisions: Establishing Decision Criteria (this article)
* Part 2: [Microsoft 365 - Making Good Technology Decisions: Data Storage](making-good-technology-decisions--data-storage.md)
* Part 3: [Microsoft 365 - Making Good Technology Decisions: Front End](making-good-technology-decisions--front-end.md)

[!INCLUDE [cc-data-platform-banner](includes/cc-data-platform-banner.md)]

The longer I work in technology, the more I realize that few things are absolute. In fact, I often say “All absolute statements are wrong.” When people think about building solutions in the Microsoft 365 ecosystem, they tend to think about the ways they’ve solved problems in the past. If you’re a SharePoint person, you’re likely to think about using a bunch of SharePoint lists. If you’re a Dynamics person you’re going to think about using Dataverse. If you’re an old school database developer, you might think about using SQL. The point isn’t that any one of those is wrong, it’s that it’s important to consider the various options you have available to you within the Microsoft ecosystem. The requirements for the thing you are trying to build should drive your decision-making, not just what you already know.

But beyond the technical choices, there are many different criteria that are important to consider when you plan to build a solution. Reading through these criteria, it may sound a bit like the classic “it depends” that comes from many consultants, but the reason many consultants use that phrase is because it’s true. In the list below I attempt to provide a list of some of the important factors a technical architect should consider when planning a solution.

But it’s not just important to the technical architect. If you work somewhere in the rest of the organization and are having conversations with the technical folks about a solution you need, understanding these criteria will help those conversations go better.

## Decision Criteria

Some of these decision criteria are discrete; others are continuous. It’s possible to come up with a scorecard-like approach to measure each of your solutions against but understand that some of the criteria may be more subjective. However, using these criteria can also be part of the way to manage your portfolio of solutions: to see how your full range of solutions compare to each other.

Knowing where your organization sits in the technology adoption life cycle is one way to think about things, but there’s much more to it if you go a layer deeper.

![Rogers’ bell curve from Wikipedia](media\making-good-technology-decisions--establishing-decision-criteria\MarcAnderson-TechDecisions-01-01.png)

Figure 1: Rogers' bell curve from Wikipedia

## Technical Fit

Usually technologists think of technical fit as the main and perhaps only reason to make a choice about how to build a solution. However, there are often multiple options which each provide a decent technical fit but may not be perfect for the solution. Perfection is a luxury; we may realize that there is a perfect technology to build a particular solution, but that solution will never be built in time, or that that solution will never be used by enough people to justify using the perfect technology. A good technical architect will understand how to sand the corners in these decisions, considering some of the other factors listed below.

## Maturity of Technology

Some technologies may look perfect on paper or sound perfect if you listen to the marketing messages. But oftentimes the technology is not mature enough to do all the things that people claim it can do. We sometimes joke that version 3 of a product is when it gets good enough to consider. It’s not always that extreme, but in today’s world of Minimum Viable Products (MVPs), Previews, and even the now old-fashioned betas, understanding where a technology sits in its lifecycle is important. The fact that a technology is early in its lifecycle doesn’t have to be a bad thing, but if you don’t know that’s the case, it can be a very bad thing, leading to project delays and even rework.

The importance of the solution and the skills of the organization may mean that choosing a technology that is not mature is much riskier. It may be that your organization is very technically savvy and is often a leader in using new technologies; it may be part of your strategy. The maturity of any product is important as it can have a huge impact on solution success.

## Skills Required

Sometimes you look at the way you would like to build a solution and realize that you don’t have the skills in-house to build it well. At this point you have an option: you can either train your people or hire an outside consultant. Sometimes the mix of skills that you do have in-house may cause you to choose a solution path that is less orthodox or less optimal. That may or may not be a bad thing. If you want to build a solution that your staff can support, sometimes you must cut corners. There is purity in building things the supposed right way, but there’s reality in building them in a way that you can both get it done and support the result. If you decide to bring in skills from the outside, be very clear about what sort of knowledge transfer you expect from them. You should also build that knowledge transfer cost into the project budget.

## Time to Market

Some solutions must be there, and they must be there fast. This may mean that there simply isn’t time to build something robust, scalable, and with exactly the right technologies. If there is a long runway, we may have the luxury of being able to stand back look at all the options, all the skills, all the variables, and choose the best approach because we are not time constrained. In many cases, we can’t take all that time.

It’s important to have a true sense of the solutions time to market requirements. In many cases the answer is yesterday when in fact it may not be the case at all. Non-technology people – especially if they have had bad experiences with technical teams in the past – may decide they need to use every single inch of runway because they expect many things will go wrong. In other cases, the must-have date is arbitrary and not tied to any specific business driver. Open and honest conversations about time to market is extremely important so no one is surprised.

Another important consideration can be whether some scheduled or known enhancement to the platform will bring the capability “for free”. In other words, if you don’t have to build it and waiting a few months to get it from the platform itself may make a lot more sense. Always try to find out whether something which is scheduled to arrive is truly scheduled or just on the road map as a “top of mind” item.

## Solution Scope

Some solutions have a very broad scope or they’re critical to your business path. For example, a bank would probably not build its ATM network software on an unproven technology. That set of solutions is simply too critical to the organization’s success to take any chances. Other times a solution may have a very narrow audience yet still be an important solution for the organization. We often think of these as departmental solutions or solutions which are simply used by a smaller number of people across disciplines inside the organization.

Solutions with narrow scope can often be built by citizen developers or power users – and in many cases should be. Those people have intimate knowledge of the requirements, the people involved, and can even have better technical skills that the technologists in your organization (but may have chosen a different career path). The fact that the people building the solution may not have formal development training does not mean that the solution can’t provide tremendous value to the organization.

## Solution Longevity

Some solutions don’t need to last very long. For instance, you may have a need to manage the company party logistics. The solution that you may decide on here may or may not be even be used again for next year’s party. Understanding how long the solution will last may drive some of your decision-making as well. In cases where the longevity is short there’s nothing wrong with deciding to use note cards or Excel spreadsheets. If the solution needs to last for months or years or potentially be reusable, you’ll want to be sure that you provide something that’s more bulletproof and can scale.

## Strategic Fit

A shared understanding of how important the solution is to the overall strategy of the organization is surprisingly rare. Often strategies are distilled into a mission statement or represented by a balanced scorecard. If there is a set of strategic goals of mission statement points you can compare the solution to, it can greatly change how you communicate about the solution as you build it. Saying you absolutely must have a meeting of 30 people to refine the solution for planning the cafeteria menu is likely not to stack up against a solution which can drive innovation or efficiency.

## Budget

While budget is implied in many of the aspects above, sometimes you just simply must deal with a fixed budget number. When budget is your primary concern, be very concerned. Driving your technical decisions purely based on budget often leads to project failure.

In an ideal situation, the design of the solution determines the budget, not the other way around. When you are thinking through this set of criteria, the most important thing you need to know is what constraints you have on the spend. While budgets are rarely unlimited, some projects get a bright green light due to their importance. Others may only grudgingly receive funding.

## Volume of Data

Some solutions require very little data; some require vast amounts of data. A high number of transactions – especially if they must occur in a short period of time – is very different than an occasional transaction with very little data storage. Sometimes this may be lumped into the technical fit thinking, but it’s important to be clear on how much data you expect and over what period.

Saying you expect to generate gigabytes of data over the next five years is different than generating gigabytes of data in the next week. If the solution will never generate more than a small amount of data, you need to acknowledge that fancy data storage mechanisms might just not be needed.

## Security

How important is the content you will be generating? This is usually the driver for security needs. Many organizations try to use a one-size-fits-all approach to security – everything is equally important and requires the same high-water mark of security – but this simply isn’t realistic. Understanding the actual security needs for the specific solution is extremely important.

Usually the most important factors are statutory or regulatory requirements, then organizational policies, then common sense – in that order. Be sure you don’t allow the security folks to apply the one-size-fits all rule. There is also a vast volume of material about the certifications and security features for Microsoft 365 available in the Trust Center. Don’t try to reinvent the wheel by trying to prove that the platform is secure. Mine that vast trove of content for the specific proof you need and reference it with your security folks. Almost more importantly, if the solution you’re proposing simply doesn’t need to be secure – sports league sign ups? – then acknowledge that right up front.

## Requirements

Yes, requirements are at the bottom of this list. That may seem backward, but the requirements for the specific solution ought to be framed using the considerations above. A good and experienced architect can sometimes just know how everything above fits the requirements, but it never hurts to be more explicit in your thinking and discussions. This can be especially helpful if you need to explain your decision-making process upward or to outside parties.

As consultants, we are often told how to build a solution with very little backup information about how that set of decisions was made. Sometimes that’s because the decisions weren’t well thought through, and other times it’s simply a matter of communication. Requirements also can’t just be a thick document in this modern era. It must be more a common understanding of the needs and goals for the solution.

## Now what?

But wait, you might say. At this point we haven’t even picked the technology! We don’t know what we are going to build! That may be true, but you’ll have a much better picture of what the solution is, how important it is to the organization, how much time to have to devote to it and to build it, who might do the works, etc.

In the next part of the series, I’ll write about some of the data storage mechanisms you have available to you on the Microsoft 365 platform. Using the thinking you have put into understanding the solution against the above criteria, you’re likely to make far better decisions than if you just decide to pick the technology first.

---

Principal author: [Marc D Anderson, MVP](https://www.linkedin.com/in/marcanderson)

This article was originally published as a part of the "Microsoft 365 - Making Good Technology Decisions" series, written by Microsoft MVP Marc D. Anderson for [CollabMagazine](https://www.collabmagazine.com/).

---
