---
title:  Maturity Model for Microsoft 365 – Practitioners Calls Archive
ms.date: 5/18/2026
author: mrsbeata
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: overview
ms.author: pamgreen
ms.service: microsoft-365
ms.localizationpriority: Low
description:  Archive of Maturity Model for Microsoft 365 Practitioners Calls
ms.collection: M365Community
---

# Maturity Model for Microsoft 365 – Practitioners Calls Archive

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

![Diagram of the Maturity Model for Microsoft 365 logo representing the framework for organizational maturity assessment.](media/maturity-model-for-microsoft-365/M365MM.png)

## Overview

This page serves as an archive of all Maturity Model for Microsoft 365 Practitioners Calls. Each call features expert speakers discussing competencies, business cases, practical scenarios, and real-world implementations. Find recordings, presentation materials, and key takeaways from each session below.

---

[!INCLUDE [mm4m365-practitioners](includes/mm4m365-practitioners.md)]

---

## Table of Contents

- [April 2026 - Revisiting the Staff and Training Competency](#revisiting-the-staff-and-training-competency)
- [March 2026 - Security Competency](#security-competency)
- [February 2026 - AMA: AI, Governance and Organizational Maturity](#ama-ai-governance-and-organizational-maturity)
- [January 2026 - Maturity Model for Microsoft 365 Agent](#maturity-model-for-microsoft-365-agent)
- [November 2025 - Practical Scenario Copilot Adoption Level 300](#practical-scenario-copilot-adoption-level-300)
- [October 2025 - Revisiting the Communications Competency](#revisiting-the-communications-competency)
- [September 2025 - Business Process & Search Competency Update](#business-process--search-competency-update)
- [June 2025 - Process Improvement Practical Scenario - AMA](#process-improvement-practical-scenario---ama)
- [May 2025 - Security Culture](#security-culture)
- [April 2025 - Practical Scenario on Branding](#practical-scenario-on-branding)
- [March 2025 - Maturity Model and AI Agents](#maturity-model-and-ai-agents)
- [February 2025 - How to run a Maturity Model Workshop](#how-to-run-a-maturity-model-workshop)
- [January 2025 - Getting Leadership Buy In](#getting-leadership-buy-in)

---

## Practitioners Calls Archive

### Revisiting the Staff and Training Competency

April 2026 | Recording: <a href="https://www.youtube.com/watch?v=N8pQMUDLo5I" target="_blank">YouTube</a>

**Speaker(s):** Emily Mancini

**Summary:** Emily Mancini — one of the original authors of the maturity model, who wrote two of the first competencies — returned to present a substantial update to the Staff and Training Competency, first published around 2020. The world has moved on considerably: asynchronous online work is now the norm, and AI has fundamentally changed how organizations think about training and capability building.

Emily's central argument, which she called her "spicy opinion," was that effective AI enablement in an organization does not begin until the managed level (300) is reached. Below that, processes are inconsistent, training outcomes vary wildly by person, and there is no shared definition of what a good output looks like. She illustrated this with a classroom exercise where students drew rainbows under secret constraints — some could only use certain colors, some only outlines. The best rainbow came from the student with the fewest limitations. Using AI without foundational understanding is the same: you are working with a limited palette without knowing it.

The competency update reflects several important shifts since its first version. Training ownership has moved beyond IT — finance, HR, operations, and other business units increasingly lead training for tools they actually use. Champions programs and adoption leads now span the organization. The competency also explicitly addresses responsible AI fluency as a required capability, including understanding how large language models work, where they fail, and why humans must remain in the loop.

A key theme was the difference between performative AI use and actual behavior change. Activity dashboards — who has Copilot enabled, how many prompts per week — do not measure whether training is working. Emily outlined four categories worth measuring instead: productivity gains (time saved, reduction in after-hours work via Viva Insights), quality of outputs (fewer document revisions, faster approval cycles), reduction in manual work (automated meeting recaps, onboarding flows), and decision speed (time from meeting to completed action items). She noted that the time freed by AI itself should be reinvested in building these measurement frameworks — previously there was rarely time to measure training effectiveness at all.

The session included a pointed discussion on AI governance and training readiness. David highlighted the risk of AI becoming self-referential — "the snake eating its tail" — when humans stop validating outputs. Pia added that security training is essential for everyone regardless of maturity level, given increasingly sophisticated AI-generated phishing and deepfakes. A licensing question toward the end revealed a broader principle: the maturity model is not tied to specific Microsoft products. Organizations can reach level 300 without E5 licenses — the model describes capability levels, not product requirements.

`Staff & Training`, `AI & Cognitive Business`, `People & Communities` | [→ Back to top](#table-of-contents)

---

### Security Competency

March 2026 | Recording: <a href="https://www.youtube.com/watch?v=ZdoUMmEReXY" target="_blank">YouTube</a>

**Speaker(s):** <a href="https://www.linkedin.com/in/matswarnolf/" target="_blank">Mats Warnolf, MVP</a><br>Clément Betacorne

**Summary:** Mats Warnolf and Clément Betacorne presented the new Security Competency — a welcome addition to the maturity model that took over two years to develop. Their central premise challenged the most common approach to organizational security: it is not primarily a technology problem. While tools matter, the harder and more impactful challenges are people and culture — and that is precisely where most organizations struggle.

The competency is grounded in the NIST Cybersecurity Framework, structured around five functions: Identify, Protect, Detect, Respond, and Recover, with Governance as the overarching layer. Mats and Clément pointed out that most organizations focus almost entirely on protection — turning on tools, checking compliance boxes — while neglecting detection and response, which is where real damage is controlled.

The five maturity levels were walked through in practical detail. Level 100 organizations have no formal security role, run default settings, and typically learn about breaches from external parties. Level 200 introduces MFA for some accounts and a handful of policies, but creates a false sense of security — organizations feel they are done when significant risk remains. Level 300, illustrated through Swiss banking examples, applies standards consistently, introduces centralized logging (e.g., Microsoft Sentinel), regularly tests incident response procedures, and tracks security metrics. Level 400 turns security from reactive to predictive: conditional access on every login, automated threat response before users notice an issue, and a SIEM spanning all systems including third-party applications — with a reported 90% reduction in incidents requiring manual response. Level 500 brings full zero-trust implementation, AI-driven behavioral analytics including Insider Risk Management, external penetration testing, and active organizational contributions to broader industry security communities. Clément noted he has rarely seen an organization with all level 500 characteristics fully in place.

The session included realistic progression timelines: 100 to 200 takes roughly six months with basic tools and a part-time security coordinator; 200 to 300 takes about a year and requires a full-time security role and organization-wide user training; 300 to 400 takes up to two years and demands a dedicated security team and advanced tooling; 400 to 500 is a continuous journey with no fixed endpoint, requiring sustained cultural change and regular external audits.

A Q&A segment tackled Microsoft Purview: information protection and sensitivity labels belong at level 300, while Insider Risk Management is a level 400 capability. Both require a classification policy and user training before any tooling is deployed. Marc Anderson noted that rolling out Purview capabilities to a level 100 organization tends to lock things down in ways no one understands, causing people to work around the controls. On ownership, both presenters were clear: management holds ultimate responsibility for security — not IT. Mats used the seatbelt analogy to frame it: controls feel inconvenient at first, but become normalized practice. For those wanting to make the business case to leadership without drowning in technical detail, Mats recommended Bruce Schneier's *Secrets and Lies* as a foundational read.

`Security`, `Governance, Risk & Compliance`, `People & Communities` | [→ Back to top](#table-of-contents)

---

### AMA: AI, Governance and Organizational Maturity

February 2026 | Recording: <a href="https://www.youtube.com/watch?v=IdIrx_p0TSs" target="_blank">YouTube</a>

**Speaker(s):** <a href="https://www.linkedin.com/in/marcanderson" target="_blank">Marc D Anderson, MVP</a><br><a href="https://www.linkedin.com/in/simonjhudson/" target="_blank">Simon Hudson, MVP</a><br><a href="https://www.linkedin.com/in/sharonweaver/" target="_blank">Sharon Weaver</a><br><a href="https://www.linkedin.com/in/pialangenkrans/" target="_blank">Pia Langenkrans, MVP</a>

**Summary:** The February session was an open Ask Me Anything, giving the community space to surface real-world challenges and compare experiences across organizations at different maturity levels. Several rich threads emerged from the conversation.

Andress opened by describing a Copilot Chat rollout for 3,000 users across an enterprise where the data and security posture was not yet ready for full AI deployment. The team affirmed the approach of a department-by-department maturity assessment, emphasizing that readiness is an organizational question, not an individual one. Pia returned to her November session on Copilot adoption at level 300, noting the real-world example of a Swedish company whose AI consistently priced sales proposals using the Finland price list — surfacing ROT (redundant, obsolete, trivial) data as the silent killer of AI value. The consensus: managers, not IT, need to own their department's AI agents because they understand the business rules the agent will be trusted to apply.

Amy, Power Platform COE manager, raised a governance challenge that drew significant discussion: blind spots in personal Power BI workspaces (invisible to tenant admin APIs) and the risk of Power Automate flows or Copilot Studio agents moving data from secured systems into uncontrolled SharePoint locations. The team explored several responses. Simon Hudson argued that agent architecture must be designed from the start to respect governance boundaries — and that where possible, user-context queries should replace content-movement patterns. Sharon shared her practical approach: monthly internal user groups where people demonstrate what they're building, used to identify and guide rogue implementations before they become incidents. The key principle: blocking by policy makes violations invisible; monitoring first makes them fixable. Pia added that sensitivity label rollouts should begin with observation — one organization had to backpedal after labeling all contracts as internal, then realizing contracts by definition involve external parties.

Heather, new to a regulated organization about to enable Copilot for half its workforce, asked what to monitor first. Marc's framing cut through the anxiety: Copilot is a layer on top of what already exists. The things you should worry about are the same things you should have worried about before it was enabled — and what Copilot exposes are the governance gaps already present. Pia added that end-user training must acknowledge that many people still struggle with the basics of Windows and Office, let alone AI prompting.

Ralph raised the question of using AI to support M365 administration and maturity progression itself. Simon Hudson outlined a three-tier framework for working with AI: finding information quickly, doing things faster that you already know how to do, and extending competency into areas just beyond your reach — provided you know enough to recognize when the AI is going wrong. The warning was clear: asking open questions on topics you know nothing about leaves you unable to validate the answers. The session closed with the insight that asking AI to coach you through a problem — "ask me questions, I'll answer them" — is itself a legitimate and underused prompting strategy.

`AI & Cognitive Business`, `Governance, Risk & Compliance`, `People & Communities` | [→ Back to top](#table-of-contents)

---

### Maturity Model for Microsoft 365 Agent

January 2026 | Recording: <a href="https://www.youtube.com/watch?v=lJhBc9L4gbE" target="_blank">YouTube</a>

**Speaker(s):** <a href="https://www.linkedin.com/in/simondoy/" target="_blank">Simon Doy, MVP</a>

**Summary:** Simon Doy presented the Maturity Model for Microsoft 365 Agent — a Copilot Studio agent he built to help practitioners navigate and apply the maturity model content without having to read through the entire documentation set. The agent is grounded exclusively on Microsoft Learn MM4M365 content and does not draw from external sources or the model's own internal knowledge, keeping responses tightly scoped to what the community has actually written.

Simon demonstrated the agent live, walking through several scenarios: explaining the model's value to a developer audience, identifying a client's maturity level in the Communications competency, building a consulting narrative for a CIO conversation, and running a self-assessment checklist for the Collaboration competency. The demo surfaced useful early feedback — citations were not appearing correctly in responses despite being configured, and some yes/no assessment questions came back as open-ended rather than binary. Both were logged as issues to fix in the upcoming 1.005 release.

A live survey during the session collected audience views on what features they most wanted. Top requests included competency-specific knowledge improvements, road mapping support, and usage analytics. Feedback on challenges named accuracy of research, executive buy-in, and wanting a single place that consolidates everything maturity model related.

The agent is built as a managed Copilot Studio solution, deployable to Microsoft 365 Copilot for licensed users or as a standalone Teams app for organizations without Copilot licenses. Custom knowledge sources can be added — for example, internal IT policies or governance documents — making it possible to layer organizational context on top of the community content. The managed package format keeps the core instructions and grounding clean, while an unmanaged version will be made available for those who want to modify the agent's behavior directly.

Simon noted the agent would eventually migrate from his personal GitHub repo into the main MicrosoftDocs/microsoft-365-community repository as iteration stabilized. The session generated enthusiasm around using the agent as an internal assessment and improvement tool, as well as potential for community members to surface improvement requests through GitHub issues.

`AI & Cognitive Business`, `Customization & Development` | [→ Back to top](#table-of-contents)

---

### Practical Scenario Copilot Adoption Level 300

November 2025 | Recording: <a href="https://www.youtube.com/watch?v=V1BHHTVBjtQ" target="_blank">YouTube</a>

**Speaker(s):** <a href="https://www.linkedin.com/in/pialangenkrans/" target="_blank">Pia Langenkrans, MVP</a>

**Summary:** Pia presented a practical scenario for Copilot adoption focused on reaching maturity level 300. She challenged the common perception that many organizations at level 200 (with champions programs, some training, and limited licenses) are actually in a dangerous "honeymoon phase" that builds technical and organizational debt.

Referencing the Apoint report, she showed that 81.9% expect ROI within 12 months but 85.7% actually slow down their rollouts. The main problem isn't change management or AI training - it's poor data quality, inaccurate output, and hallucinations that hinder adoption.

Reaching level 300 requires parallel work across three core competencies: Business Processes (documented, measurable processes ready for automation), Staff and Training (HR-driven, mandatory training where managers must go first), and Management of Content (taxonomy, metadata, ROT cleanup, and lifecycle management). Pia emphasized that information architecture isn't something AI can help with - it's something AI needs to work.

She also argued forcefully that managers, not IT, will become "bosses" of agents in the future because they understand business processes, and that champions programs need to be structured with at least 4 hours monthly commitment to prevent burnout. The budget discussion revealed tension between IT budgets and business needs.

`Practical Scenario`, `Staff & Training`, `People & Communities`, `AI & Cognitive Business` | [→ Back to top](#table-of-contents)

---

### Revisiting the Communications Competency

October 2025 | Recording: <a href="https://www.youtube.com/watch?v=2c3tSHdf0cg" target="_blank">YouTube</a>

**Speaker(s):** <a href="https://www.linkedin.com/in/anokheetara/" target="_blank">Tara Saylor</a>

**Summary:** Tara Saylor presented an updated perspective on the Communications competency, bringing her unique experience as a corporate communications professional who moved to enterprise IT. She walked through the maturity levels with practical examples, emphasizing that Level 100 is ad hoc and demand-driven (appropriate for small organizations), Level 200 introduces distributed channels without coordination, Level 300 adds governance and repeatable processes with targeting and feedback, Level 400 involves sophisticated listening and adjustment (exemplified by her COVID task force work with weekly newsletters and Reddit scraping), and Level 500 treats internal communications like external marketing with personalized journeys.

She also explored how AI/Copilot fits into organizational communications at each level, from experimental (100-200) to approved tools with training (300) to predictable, trusted use (400) to mass customization (500).

The presentation reinforced that "technology needs the business to make communications work" - IT can build the infrastructure but requires content owners to make it useful. Tara emphasized that communications complexity should match the channel bandwidth (simple tactical messages via text, complex strategic messages face-to-face) and that regulation, localization, and cultural considerations add layers of complexity. A critical insight for AI adoption was "IIA before AI" (Information Architecture before Artificial Intelligence) - LLMs only work reliably when content is well-organized, properly secured, and metadata-rich.

She highlighted AI's strengths in accessibility (automatic transcripts, real-time translations, alt-text generation) and specific communication tasks like SharePoint's FAQ generation tool and summarization features, which work well because they operate within defined scopes. The shift from one-way CEO blogs to two-way employee-generated content (via Viva Engage/Yammer) represents a fundamental change in organizational communications, and AI's ability to provide mass customization lets end users reformat content to their preferences without burdening communicators.

`Communications` | [→ Back to top](#table-of-contents)

---

### Business Process & Search Competency Update

September 2025 | Recording: <a href="https://www.youtube.com/watch?v=-mReMv9HgTg" target="_blank">YouTube</a>

**Speaker(s):** <a href="https://www.linkedin.com/in/simonjhudson/" target="_blank">Simon Hudson, MVP</a>

**Summary:** Simon Hudson presented substantial rewrites to both the Business Process and Search competencies, modernizing them for the Copilot/AI era. Each competency received approximately 30 new or changed characteristics (excluding level 100 in Business Process, which "was already at the lowest possible maturity"). The Business Process competency now emphasizes user experience design, citizen development management, and the importance of Statistical Process Control (SPC). At level 500, it introduces concepts like enabling power users with governed freedom to adapt workflows rapidly, digital twins for simulating business processes, and innovative automation methods.

The Search competency underwent a conceptual shift from "search" to "discovery," with renewed emphasis on metadata and taxonomy despite Microsoft's attempts to downplay them. The session opened with the sobering news that core team member Simon Doy had suffered a heart attack at age 40 but was recovering well.

The updates reflect a fundamental rethinking of how AI interacts with traditional capabilities. For Search, Simon emphasized that the goal is helping people "know things" rather than just "find things," with AI-enhanced search providing digestible summaries and multimodal capabilities (text, voice, images, video) at higher maturity levels. However, the session reinforced that "Copilot is not pilot" - human review remains critical, and AI is not the answer for everything.

A compelling discussion emerged around content lifecycle management when Avashek shared how their 84-year-old manufacturing company discovered Copilot surfacing decades-old help desk numbers alongside current ones. Diego's discovery that Azure-generated image tags labeled healthcare workers as "sexy, attractive, gorgeous" highlighted AI's dangerous context failures and the continued importance of human-curated metadata. The consensus was that while AI enables powerful new capabilities, organizations need strong information architecture, metadata governance, and lifecycle management as prerequisites - echoing the earlier session's "IIA before AI" principle. Search-driven experiences still have distinct value versus AI-driven ones, and knowing when to use which approach is a critical skill.

`Business Process`, `Search` | [→ Back to top](#table-of-contents)

---

### Process Improvement Practical Scenario - AMA

June 2025 | Recording: <a href="https://www.youtube.com/watch?v=1nNP1CzgnAE" target="_blank">YouTube</a>

**Speaker(s):** Carol Zollinger

**Summary:** Carol Zollinger presented a detailed practical scenario showing how she transformed a chaotic timesheet correction process at a mental health residential facility from level 100 to approximately level 300. The original problem involved direct care workers on 24/7 shifts who couldn't fix their own timesheet errors, supervisors drowning in email requests (hundreds daily), and missed approval deadlines causing payroll chaos.

Carol built a ticketing system using Microsoft Lists, Power Automate (5 flows), and Forms with status-based automation (Open → Resolved/Escalated → Escalated to Payroll). The solution featured JSON-formatted clickable resolve/escalate buttons, automated daily reminders when tickets were open, and email notifications when tickets were resolved. She targeted four competencies: Business Process (clear workflow and visibility), Collaboration (any supervisor could fix any ticket), Employee Experience (simple mobile-friendly form), and Management of Content (standardized format and audit trail).

Carol's design philosophy centered on making compliance easy: "Here's what I want people to do. How can I make it easy for them to obey me?" She emphasized Mark's quote "tech cannot fix humans" - noting that supervisors initially found it easier not to enforce the process, but paid for it later. Her rollout strategy proved crucial: she trained supervisors first (who were "super excited"), and they rolled it out in their regular meetings, essentially doing the selling for her.

Success came quietly - when she heard nothing, she feared no one was using it, but checking the list showed people were simply using it without issues. She included inline documentation carefully calibrated for users who'd done the task once before (not introductory, not exhaustive). The session also featured Ralph demonstrating an M365 Copilot agent built for the maturity model itself, sparking discussion about using agents to help navigate the massive model content. A significant technical discussion emerged about upcoming MFA enforcement on service accounts in October 2024, with suggestions to use service principals with certificates instead of password-based service accounts for running Power Automate flows.

`Practical Scenario`, `Business Process`, `Collaboration`, `Employee Experience`, `Management of Content` | [→ Back to top](#table-of-contents)

---

### Security Culture

May 2025 | Recording: <a href="https://www.youtube.com/watch?v=Q0CaGHVmwR4" target="_blank">YouTube</a>

**Speaker(s):** <a href="https://www.linkedin.com/in/matswarnolf/" target="_blank">Mats Warnolf, MVP</a>

**Summary:** Mats presented on security culture, distinguishing it fundamentally from information security (systems, policies, controls like Defender for Endpoints and conditional access). He emphasized that while information security is about architecture and IT/cybersecurity working behind the scenes, security culture is about people, habits, and values - "behavior and habits, not checkboxes."

His core message: "compliance and culture are not the same thing" - compliance is about following rules, ticking boxes, and meeting minimums out of fear, while culture is about caring, understanding why rules exist, and following them when no one's watching. Mats presented the maturity model progression from Level 100 (no culture, security is IT's job, first instinct when something goes wrong: "I hope nobody noticed") through Level 300 (security normalized, integrated into processes, reporting is seen as normal not shameful) to Level 500 (adaptive living system where everyone shares responsibility, mistakes are discussed openly, and the question becomes "how do we stay curious and ready?").

Drawing on James Clear's *Atomic Habits*, Mats outlined five rules for building security habits: make it obvious (visibility through cues like sensitivity labels, login screens, posters), make it easy (one-click incident reporting, password managers), make it attractive (celebrate secure actions, "make heroes"), make it satisfying (instant feedback: "thanks for reporting this, you may have prevented a breach"), and anchor to identity ("we are a secure company," "we protect our customers"). The key insight: "people don't rise to the level of policies, they fall to the level of habits."

Leadership must be visibly involved - "culture is shaped by what leaders talk about and what they ignore." Creating psychological safety is paramount: "no blaming, no shaming" with the principle that people should be rewarded for doing the right thing rather than punished for accidentally doing wrong. Measuring culture requires multiple lenses: inspection (formal structures), surveys (employee perceptions), interviews (understanding the why behind behavior), observation (watch what they do not what they say), and testing (though phishing tests can create false security).

The rich discussion included Carol's story of an employee fooled by a compromised lawyer's email who immediately reported it, preventing data loss - this became a teaching moment about catching mistakes early. Simon warned about AI-driven voice phishing attacks ("very polite young Londoner"). Best practices emerged: public recognition in Viva Engage, leaderboards for catching phishing, automatic training enrollment for failures, and always providing auto-responders rather than letting people "report into the void."

`Security`, `People & Communities` | [→ Back to top](#table-of-contents)

---

### Practical Scenario on Branding

April 2025 | Recording: <a href="https://www.youtube.com/watch?v=b36ZFdLdnw8" target="_blank">YouTube</a>

**Speaker(s):** <a href="https://www.linkedin.com/in/simonjhudson/" target="_blank">Simon Hudson, MVP</a>

**Summary:** Simon Hudson presented a practical scenario on brand management, opening with the fundamental principle that "brands are absolutely not a logo and some colors" - that's level 100 thinking. True branding is about the method and stance you take on communicating to your preferred audience. He outlined six core principles: understanding your organizational tribe (target audience), differentiation, consistency across time and geographies, authenticity (who you really are, not who you'd like to be), emotional appeal that builds loyalty, and flexibility to adjust to market changes.

In a remarkably authentic move, Simon used his own newly-started company (only three weeks old) as a real-world example of being at level 100-200, noting "I wrote this scenario before I started the new company, so this is a very reflective exercise." The maturity progression moved from Level 100 (logo/colors exist, each department does its own marketing, weak brand identity) through Level 300 (detailed guidelines published, staff trained, senior management aligned, consistent across touchpoints) to Level 500 (multinational sophistication with global/regional variations, horizon scanning, brand moves dynamically with market changes).

Unlike most competencies, Simon noted "there are actually in the branding world quite a lot of 500 organizations" - exceptional brand maturity is achievable. The session revealed practical tools participants weren't aware of: Pia highlighted the Fluent UI Theme Designer (now integrated into SharePoint Brand Center), and Simon demonstrated the PowerPoint "golden template" Microsoft released that is Copilot-compatible, though he admitted "I don't like all of the layouts." A critical technical insight emerged about the fragmented branding landscape across Microsoft 365 - participants must visit 3-4 different locations: admin center's custom themes (navbar/suite bar colors), Power Platform logos, Stream/Clipchamp branding, and Viva Engage settings.

Sean Brown shared his organizational asset library challenge: categorizing templates for different regions (US, EU, Japan) without creating a mess, with suggestions to use permissions or content types. Simon's expertise showed when discussing his previous role as international brand manager for clinical products, where he managed six global brands and created "carefully crafted authentic stories" about wound healing - acknowledging it as "positive reinforcement manipulation to make sure people understand how great the things you do really are." The memorable quote: "Registering is trivial. That's just another form. Building your brand, finding the right combination of names and logos and domains... that's very very hard." Pia lamented her own struggle naming "Cruise Control 365" (trademark conflicts).

`Practical Scenario`, `Management of Content` | [→ Back to top](#table-of-contents)

---

### Maturity Model and AI Agents

March 2025 | Recording: <a href="https://www.youtube.com/watch?v=wI_452J6Trc" target="_blank">YouTube</a>

**Speaker(s):** <a href="https://www.linkedin.com/in/simondoy/" target="_blank">Simon Doy, MVP</a>

**Summary:** Simon Doy presented a new practical scenario on AI agents and how organizations can mature in their use of them. He defined AI agents as "junior team members" driven by large language models (LLM) that differ from Copilot by being able to be triggered by external events, not just user requests. Through a practical walkthrough of a sales process, he showed how agents can be introduced gradually - from manual Copilot use (researching companies in chat) to automated agents triggered when a lead enters the CRM system. The critical insight: "human in the loop" is essential - when agents create content, humans must review it before it proceeds. The maturity progression goes from Level 100 (experimenting in Copilot Chat/Studio, not in production) through Level 200 (piloting use cases with business teams) to Level 300 (guidelines for test/delivery, agents used daily) up to Level 400 (measurement, feedback, dashboard over agents) and Level 500 (agents across the organization improving performance).

The presentation identified five critical competencies for AI agent maturity: **Cognitive Business** (the transition from humans doing everything to humans+AI as a team), **Governance, Risk & Compliance** (AI strategy, responsible AI policies, managing "agent sprawl" that will resemble SharePoint sprawl), **Staff and Training** (users AND developers need training, managing fear that AI takes jobs), **Management of Content** (agents depend on high-quality content, archive old content outside scope), and **Customization and Development** (DevOps thinking with test/staging/prod environments). Terrence expressed concern about consumption-based cost models but suggested it might need to be expensive to discourage waste of computing power - he gave the example of someone building monstrous AI prompts for route planning instead of coding an elegant app. Pia emphasized that organizations must treat AI agents as real DevOps: "we can't just run and see when it breaks like we do with M365 admin - we need to think like real developers." David highlighted the problem of personal agents in document libraries becoming "orphaned" upon terminations. The discussion about responsible AI became intense when Simon mentioned an example from the Copilot Connection podcast about someone building an agent to profile people as potential psychopaths - Teams AI gave him a warning for using the word "psychopath." Terrence concluded by emphasizing the leadership vacuum: many organizations lack vision for AI and leave IT to "muddle through" while employees fear being replaced - leaders need to take a stand and communicate "we will not replace people with AI" (at least for now).

`Practical Scenario`, `AI & Cognitive Business`, `Governance, Risk & Compliance`, `Customization & Development` | [→ Back to top](#table-of-contents)

---

### How to run a Maturity Model Workshop

February 2025 | Recording: <a href="https://www.youtube.com/watch?v=lnZUcyzYcv0" target="_blank">YouTube</a>

**Speaker(s):** <a href="https://www.linkedin.com/in/marcanderson" target="_blank">Marc D Anderson, MVP</a><br><a href="https://www.linkedin.com/in/simonjhudson/" target="_blank">Simon Hudson, MVP</a><br><a href="https://www.linkedin.com/in/simondoy/" target="_blank">Simon Doy, MVP</a><br><a href="https://www.linkedin.com/in/sharonweaver/" target="_blank">Sharon Weaver</a><br><a href="https://www.linkedin.com/in/galenkeene/" target="_blank">Galen Keene</a><br><a href="https://www.linkedin.com/in/pialangenkrans/" target="_blank">Pia Langenkrans, MVP</a><br><a href="https://www.linkedin.com/in/matswarnolf/" target="_blank">Mats Warnolf, MVP</a>

**Summary:** Pia led a practical session on how to conduct a maturity model workshop using the fictional company "Pancom" - a communications agency with fragmented workflows, dissatisfied customers, and old systems. The core team created several role-play videos (which they themselves admitted were "method acting") where they played different characters: Mark as legal ("completely ignoring the rest of us - that is the best part"), Simon as a salesperson with local templates on his computer, and Pia as HR. The critical incident: "poor George" dropped his laptop on the train with sensitive data and two months of work - the laptop was too old for remote deletion, lacked cloud backup, and ran Windows 7 because "George he's an old guy he doesn't want to learn new things."

The workshop showed how to gradually get participants to realize where they actually are - from initial "I'm guessing we're 300 or so and we're better than some other people" to realistic assessment around 180-230. The key was to get ALL perspectives in the room (IT, HR, communications, facility, legal) and ask the right questions instead of giving answers directly.

The workshop's success depends on getting the right people in the room and managing different personalities - "there are people who are afraid, there are people who are pushy and not listening to other people in the room." Pia emphasized that the goal is not to measure but to create understanding: "when organizations start learning about these things they just get more stressed because they understand how much there is out there that they don't understand... so it's important to give them a roadmap." Mark made an important point about avoiding "boiling the ocean" - not everyone needs to be 500 everywhere: "few organizations have that NASA kind of critical mission maturity required all the time - if they get to level 300 on management of content they're more than happy, but security might need to be higher." Sharon mentioned that she interviews certain people separately and then presents the results. A critical discussion arose about Copilot maturity when Sean asked about his organization which "are like Windows one, not Windows 7, and they want to use Copilot" - the team emphasized that Copilot requires baseline maturity in several competencies (permissions must be in order otherwise Copilot finds "all kinds of things you didn't want it to find"). Simon Hudson pointed out that the maturity model is "technology agnostic" while Microsoft focuses on specific products - they try to achieve different goals. Pia also emphasized the importance of not expecting people to learn faster than is realistic: "we really hit the roof on that - we can't expect people just to learn this, we need more structure and order."

`Practical Scenario`, `Staff & Training` | [→ Back to top](#table-of-contents)

---

### Getting Leadership Buy In

January 2025 | Recording: <a href="https://www.youtube.com/watch?v=sE-u4Q94ZOw" target="_blank">YouTube</a>

**Speaker(s):** <a href="https://www.linkedin.com/in/pialangenkrans/" target="_blank">Pia Langenkrans, MVP</a>

**Summary:** Pia delivered a masterclass on securing leadership buy-in for maturity model initiatives, opening with the blunt truth: "Why is leadership buy-in so hard? Because we in IT are doing it wrong and yes it is our problem." She explained that IT professionals talk in technical details while leadership thinks in big picture terms - when IT comes complaining about "the oars and the wood isn't very good," leadership sees it as "a you problem."

The session centered around "Pancom," a fictional 80-person PR/communications agency where CEO Gail struggled to connect client complaints and internal frustrations until a crisis hit: senior consultant George left his computer on a train containing highly sensitive client data. The computer was too old for remote wipe, not enrolled in Intune, had no cloud backup training, and ran Windows 7 because "George is an old guy he doesn't want to learn new things." The crisis meeting itself "needed a crisis meeting" with everyone pointing fingers. This incident catalyzed a quick assessment workshop revealing an average maturity of 156 across eight competencies, with a 12-month target of 279 (an increase of 132 points). Pia emphasized: "Most of the time when leadership really listens is based on an incident - worst case scenario it's an incident you have internally, best case scenario you can build on someone else's mistake."

Pia provided a one-page leadership decision slide that she described as "atrocious for a PowerPoint slide, this is how they like to see things" - leadership takeaways focused on future competitiveness ("nobody wants to be obsolete"), employee empowerment (recruitment costs are huge), and AI-readiness. She stressed: "If you want management to listen, you can't send them long emails or Word documents - they do everything in PowerPoint." The psychological barriers include fear of appearing incompetent about technical matters ("imagine learning Japanese - if you teach hello and count to five they'll remember, but if you continue with complex conversations they remember nothing"), concerns about organizational disruption (people become paralyzed during changes), and anxiety about being accountable for failed decisions that cost millions.

Leadership resistance tactics include: deflection ("not my table"), analysis paralysis (endless requests for more information), token agreements (verbal support but no budget/people), silent sabotage (avoiding meetings), delegation without direction (sending junior people with no mandate), dismissive attitudes ("nice to have not must have"), and excessive risk aversion (in Sweden: "the cloud gives everything to the American military"). **Proactive strategies**: Use competitors' failures as cautionary tales ("this is the risk I'm proposing - here's what happened to someone who ignored it"), get management arguing with each other rather than with you (put sales next to legal: "if I do all that we don't sell anything" vs "these are compliance requirements"), gossip everything to everyone in one-on-ones before meetings so "everyone thinks everyone else is hearing it for the first time," and use the "management tripwire" trick - deliberately include one visible but insignificant error so managers feel they've contributed. Daniel raised the frustration of identifying risks at project start only to have them become realities at the end - Pia confirmed using storytelling works better than dry technical terms. The pong game analogy was brilliant: an IT manager showed leadership the old Pong game and said "our system was designed when this was popular."

`Practical Scenario`, `Staff & Training`, `People & Communities` | [→ Back to top](#table-of-contents)

---

**Maintained by:** Maturity Model for Microsoft 365 Community Team

---

[!INCLUDE [mm4m365-core-team](includes/mm4m365-core-team.md)]
