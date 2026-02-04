---
title: Elevating Security
ms.date: 01/19/2026
author: matswarnolf
ms.reviewer: pamgreen
manager: pamgreen
ms.topic: concept-article
ms.author: pamgreen
ms.service: microsoft-365
ms.localizationpriority: Low
description: Elevating Security - How to progress through security maturity levels in Microsoft 365
ms.collection: M365Community
---

# Elevating Security

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## Introduction

The [Security Competency](microsoft365-maturity-model--security.md) article provides an overview of security concepts and details each of the five security maturity levels from Initial to Optimizing (100 through 500). It adopts a broadly technology-agnostic approach to the business characteristics of security plus expected benefits.

This article explores how organizations at any level could use the Microsoft 365 suite (and associated technologies) to reach a higher maturity level. Understanding how organizations evolve through security maturity helps you identify where to focus improvement efforts and what resources you'll need.

---

## How to Move from Initial to Managed (Level 100 to 200)

**The Shift:** Moving from ignorance to awareness. Someone in the organization (usually after an incident, audit finding, or customer requirement) recognizes that default settings and informal practices are inadequate. Security moves from "not our problem" to "we should probably do something about this."

### What Changes

#### People

- First security responsibilities are assigned, even if part-time or added to existing IT roles
- Some employees receive initial security training, though attendance and retention vary

#### Process

- Basic security policies are written and communicated
- An initial incident prompts documentation of what went wrong and how to prevent recurrence
- Password requirements are established on paper

#### Technology

- Basic security tools are purchased and partially deployed—antivirus software, some MFA for administrators, basic encryption for specific sensitive files
- Microsoft Secure Score is discovered but not actively managed

### Investment Required

- **Minimal** – Primarily licensing costs for basic security tools already included in Microsoft 365
- May require one part-time security coordinator role
- Budget for initial policy development (may use templates or consultants)
- Time investment for initial training programs

### Typical Timeframe

3-6 months if driven by a compelling event (breach, audit failure, customer requirement); longer if driven only by gradual awareness.

### Common Barriers

- Leadership views security spending as unproductive overhead
- "We've never had a problem before" mentality
- Limited budget and competing priorities
- Lack of expertise to know where to start

### Quick Wins to Progress

| Action | Impact |
|--------|--------|
| Enable MFA for all administrators immediately | Prevents most admin account compromises |
| Implement Security Defaults in Microsoft Entra | Baseline protection with single setting |
| Run organization-wide phishing simulation | Demonstrates vulnerability to leadership |
| Document one major incident | Shows the cost of inadequate security |

### Microsoft 365 Technologies to Consider

- **Security Defaults** – Enable with a single setting for immediate baseline protection
- **Microsoft Authenticator** – Free MFA app for all users
- **Microsoft Secure Score** – Review recommendations to understand gaps
- **Exchange Online Protection** – Ensure anti-spam/anti-malware is properly configured

---

## How to Move from Managed to Defined (Level 200 to 300)

**The Shift:** Moving from inconsistent, checkbox compliance to organization-wide standards. Security becomes "how we do things here" rather than an afterthought. Leadership commits to consistent enforcement and dedicated resources.

### What Changes

#### People

- Security roles become formal with clear responsibilities and adequate time allocation
- Training becomes mandatory and regular for all employees, not just IT
- Security coordinators are designated in each department or business unit

#### Process

- Policies are documented, approved by leadership, consistently enforced, and regularly reviewed
- Incident response procedures are tested
- Risk assessments become routine rather than event-driven

#### Technology

- Security controls are standardized across the organization
- MFA is required for everyone
- Centralized logging and monitoring provide visibility
- Data classification begins with automated default labels
- Microsoft Secure Score is actively managed with systematic remediation

### Investment Required

- **Moderate** – Enhanced Microsoft 365 licensing (typically E3 or E5) to access advanced security features
- Consulting or external expertise to design standardized policies and configurations
- Organization-wide training programs (may include specialized security awareness platforms)
- Dedicated security personnel (at least one full-time role in most organizations)
- Time investment for cultural change management

### Typical Timeframe

6-12 months; requires cultural change management and cannot be rushed.

### Common Barriers

- Resistance from departments who see standardization as reducing flexibility
- "But we're different" arguments from business units
- Difficulty enforcing policies when executives want exceptions
- Insufficient staff to implement and maintain consistent standards
- Budget constraints for necessary licensing upgrades

### Quick Wins to Progress

| Action | Impact |
|--------|--------|
| Conduct organization-wide risk assessment | Identifies critical gaps and priorities |
| Implement MFA for all users (not just admins) | Dramatically reduces account compromise risk |
| Standardize configurations using Microsoft baselines | Consistent protection across the organization |
| Create executive dashboard showing security metrics | Maintains leadership visibility and support |
| Document and communicate one policy thoroughly | Demonstrates the new standard |

### Microsoft 365 Technologies to Consider

- **Conditional Access** – Implement policies for common scenarios (require MFA for external access, block untrusted locations)
- **Microsoft Defender for Office 365 (Plan 1)** – Safe Attachments, Safe Links, anti-phishing
- **Sensitivity Labels** – Start with 3-4 labels and train users
- **Unified Audit Log** – Enable comprehensive logging across services
- **Microsoft 365 Compliance Center** – Centralized policy management
- **Attack Simulation Training** – Regular phishing simulations

---

## How to Move from Defined to Predictable (Level 300 to 400)

**The Shift:** Moving from manual enforcement to automated protection and from reactive response to predictive prevention. Security teams stop spending time on routine tasks and start focusing on strategic threats. The organization moves from "are we compliant?" to "are we ahead of threats?"

### What Changes

#### People

- Security becomes a partnership between dedicated security teams and business units
- Professional development keeps skills current
- Employees actively report threats rather than waiting for IT to discover them
- Security workload shifts from administrative (applying policies) to analytical (identifying emerging risks)

#### Process

- Security performance is measured with clear metrics
- Continuous risk assessment replaces periodic reviews
- Policies are tested regularly and refined based on data
- Security considerations are embedded in project planning and change management processes

#### Technology

- Advanced tools including SIEM systems, Conditional Access policies that evaluate risk in real-time, automated threat detection and response, comprehensive DLP across all platforms, end-to-end encryption, and integrated dashboards

### Investment Required

- **Substantial** – Premium Microsoft 365 licensing (typically E5 or equivalent) for advanced security capabilities
- Advanced security tools and SIEM platforms
- Specialized security staff with expertise in threat detection, incident response, and security architecture
- Ongoing training and professional certification for security teams
- Integration and automation projects requiring significant time investment

### Typical Timeframe

12-24 months; requires mature Level 300 processes as foundation—cannot skip ahead.

### Common Barriers

- Significant cost increase for premium licensing and tools
- Skills gap—difficulty hiring or developing expertise in advanced security
- Complexity of configuring and maintaining advanced systems
- Integration challenges with existing tools and processes
- Change fatigue from continuous security improvements

### Quick Wins to Progress

| Action | Impact |
|--------|--------|
| Implement Conditional Access for high-risk scenarios | Dynamic protection for external access, privileged accounts |
| Automate response to one common threat type | Immediate remediation without manual intervention |
| Deploy Microsoft Defender for Office 365 Plan 2 | Automated phishing detection and remediation |
| Create executive metrics dashboard | Shows time-to-detect and time-to-respond |
| Pilot automated DLP for one high-risk data type | Prevents credit card numbers in external emails |

### Microsoft 365 Technologies to Consider

- **Microsoft Sentinel** – Cloud-native SIEM for centralized security monitoring
- **Microsoft Defender for Endpoint** – Endpoint detection and response (EDR)
- **Microsoft Defender for Office 365 (Plan 2)** – Automated investigation and response
- **Microsoft Defender for Cloud Apps** – CASB for shadow IT discovery and control
- **Advanced Data Loss Prevention** – Comprehensive DLP across all services
- **Privileged Identity Management (PIM)** – Just-in-time privileged access
- **Microsoft 365 Defender** – Unified XDR portal

---

## How to Move from Predictable to Optimizing (Level 400 to 500)

**The Shift:** Moving from "security is important" to "security is how we think." Security becomes organizational DNA rather than a program to manage. The organization treats security as a continuous journey requiring ongoing evolution, not a destination to reach.

### What Changes

#### People

- Security considerations naturally precede every business decision without needing formal checkpoints
- All employees understand security as enabling business objectives, not hindering them
- Security teams focus on strategy, innovation, and staying ahead of emerging threats
- Risk-aware decision-making replaces risk avoidance

#### Process

- Continuous improvement is embedded in everything
- Security metrics are directly connected to business strategy
- Independent standards (ISO 27001, NIST) are used for benchmarking
- External audits validate practices
- Lessons learned from incidents drive immediate improvements

#### Technology

- Cutting-edge implementation including comprehensive Zero Trust architecture, AI-driven behavioral analytics, pervasive automation, adaptive controls that adjust based on context and risk, and fully integrated security ecosystem

### Investment Required

- **Continuous and strategic** – Typically 2-5% of overall IT budget dedicated to security innovation
- Investment in emerging technologies and pilot programs
- Participation in security communities and information sharing
- Regular external assessments and penetration testing
- Sustained commitment to training and development at all levels

### Typical Timeframe

Continuous; most organizations never reach or sustain this level. Even organizations that achieve Level 500 must continuously invest to maintain it and can regress if commitment wavers.

### Common Barriers

- Very few organizations have the resources, commitment, and expertise to reach this level
- Requires sustained executive commitment over years, which can be disrupted by leadership changes
- Ongoing cost and complexity can be difficult to justify when "good enough" security exists at Level 400
- Rapidly changing threat landscape means continuous investment is never "done"
- Difficulty maintaining this level during periods of organizational change or budget pressure

### Characteristics of Organizations at This Level

- Often industry leaders who view security as competitive advantage
- May have experienced significant incidents that drove commitment to excellence
- Typically operate in highly regulated industries or handle extremely sensitive data
- Share their practices with industry peers and contribute to security community
- Maintain this level because it's embedded in culture, not just because of tools or policies

### Microsoft 365 Technologies to Consider

- **Microsoft Defender for Identity** – Identity threat detection and investigation
- **Insider Risk Management** – ML-based detection of insider threats
- **Information Barriers** – Ethical walls and communication controls
- **Privileged Access Management** – Granular just-in-time access
- **Communication Compliance** – Monitor communications for policy violations
- **Zero Trust architecture** – Full implementation across all access points
- **Microsoft Security Copilot** – AI-assisted security operations (when available)

> [!NOTE]
> Level 500 is not about quick wins—it's about sustained commitment to excellence. Organizations at this level continuously evaluate emerging technologies and threats, pilot innovative solutions, and refine based on continuous feedback and metrics.

---

## Scenarios

To illustrate the progression through security maturity levels, let's follow a hypothetical organization, "Contoso Ltd.," and its journey toward enhancing its security posture within Microsoft 365. Contoso is a mid-sized professional services firm with 250 employees, handling sensitive client data including financial records, strategic plans, and proprietary business information.

### Level 100 - Initial: The Wake-Up Call

#### Scenario

Contoso Ltd. operates without formal security policies. The IT team of two people focuses on keeping systems running—security is not part of their job description. Employees share passwords "to make collaboration easier," and the CEO's password is "Contoso2023" because it's easy to remember.

One Monday morning, the CFO clicks a link in an email that appears to be from their bank. Within hours, the attacker uses the compromised credentials to access SharePoint, downloading three years of customer contracts, financial statements, and the company's strategic pricing model. The breach isn't discovered for two weeks, and only when a competitor somehow knows Contoso's confidential bid for a major contract.

The breach costs Contoso the contract opportunity (worth $2M), requires expensive forensic investigation, triggers customer notification requirements, and results in two clients terminating their contracts. The total cost exceeds $500K.

#### Actions Taken

Shaken by the incident, Contoso's leadership finally acknowledges that security cannot be ignored. They begin drafting basic security policies and searching for someone who can help them "fix security."

#### Business Impact

- Direct financial loss from lost business and incident response
- Reputational damage affecting client relationships
- Recognition that current approach is unsustainable

---

### Level 200 - Managed: Checking Boxes

#### Scenario

Following the breach, Contoso invests in basic security improvements. They hire a part-time security coordinator, develop password policies, implement antivirus software, and enable MFA for administrators. Security policies are drafted and sent to all employees.

Six months later, problems persist beneath the surface:

- The sales team writes passwords on sticky notes
- Several employees still haven't enabled MFA because "it's too complicated"
- The executive team has exempted themselves from several policies
- An employee accidentally shares salary information externally, but nobody notices
- A phishing simulation test shows 60% of employees click malicious links

During a client security assessment for a potential major contract, Contoso struggles to answer basic questions:

- "How do you monitor for data breaches?" (We don't.)
- "How do you classify sensitive data?" (We rely on employees to be careful.)

Contoso loses the $3M contract to a competitor who can demonstrate mature security practices.

#### Actions Taken

Contoso's leadership realizes that having policies isn't enough. They begin researching what "good security" actually looks like and engage consultants for a security assessment.

#### Business Impact

- Lost business opportunity due to inability to demonstrate security maturity
- Employee frustration with policies that seem arbitrary
- Recognition that checkbox compliance isn't enough

---

### Level 300 - Defined: Building the Foundation

#### Scenario

After losing the major contract, Contoso's leadership commits to building mature security practices. They upgrade to Microsoft 365 E3 licensing, hire a full-time Security Manager, and engage consultants to design comprehensive policies.

Over the next year, significant changes occur:

- MFA is required for everyone, no exceptions
- Security policies are formally documented and consistently enforced
- All employees complete mandatory security awareness training
- Microsoft Secure Score improves from 32% to 78%
- Centralized logging and monitoring are implemented
- Incident response procedures are documented and tested

Three months after implementing the new controls, the monitoring system detects unusual activity: an employee account is accessing large volumes of files at 3 AM. The Security Manager investigates and discovers the employee's credentials were compromised through password reuse on a gaming site.

Because of the monitoring and defined procedures, Contoso:

- Detects the compromise within hours instead of weeks
- Immediately locks the account and resets credentials
- Conducts rapid assessment showing only 50 files were accessed (DLP prevented external sharing)
- Notifies affected clients proactively

When Contoso pursues another major contract, they can demonstrate comprehensive security policies, regular training, monitoring capabilities, and measurable security posture. **Contoso wins the $3M contract**, with the client specifically citing "mature security practices" as a differentiator.

#### Business Impact

- Won major contract due to demonstrable security maturity
- Rapid detection and response prevented major breach
- Clear metrics demonstrate ROI of security investments

---

### Level 400 - Predictable: Automation and Prevention

#### Scenario

Building on their Level 300 foundation, Contoso upgrades to Microsoft 365 E5 and implements advanced security capabilities. They hire an additional security analyst and invest in Microsoft Sentinel.

The security team implements:

- Conditional Access policies that adjust authentication based on risk
- Microsoft Defender for Office 365 with automated remediation
- Comprehensive DLP policies
- Real-time dashboards showing security metrics to leadership

The impact is dramatic:

- Over six months, Defender automatically blocks 847 phishing attempts before employees see them
- Conditional Access prevents 23 high-risk sign-in attempts from unusual locations
- DLP prevents 12 incidents where employees attempted to share sensitive data inappropriately

When a ransomware campaign targets professional services firms, Contoso's automated threat detection identifies and isolates a compromised device within minutes—before encryption begins. Other firms suffer significant disruption; **Contoso experiences none**.

Contoso's security metrics show:

- 94% reduction in incidents requiring manual response
- Time-to-detect reduced from hours to minutes
- Zero successful phishing attacks in 12 months

When Contoso bids on an enterprise client, they provide real-time dashboards, comprehensive audit logs, and documented incident response with metrics. **Contoso wins the $10M multi-year contract**. The client's CISO privately shares that Contoso's security maturity exceeded most companies twice their size.

#### Business Impact

- Security automation dramatically reduces incidents
- Major contract wins cite security maturity as differentiator
- Security becomes competitive advantage rather than cost center

---

### Level 500 - Optimizing: Security as Organizational DNA

#### Scenario

Three years after the initial breach, Contoso has transformed security into organizational DNA. The security team has expanded to include strategic roles focused on emerging threats.

They've implemented:

- Comprehensive Zero Trust architecture
- AI-driven End-User Behavioral Analytics (EUBA)
- Adaptive security controls
- Integration with industry threat intelligence communities
- Regular external security audits and penetration testing

Recent examples of how this works:

**Insider Threat Detection:** EUBA tools notice a project manager suddenly starts working unusual hours and accessing hundreds of files outside their project scope. Investigation reveals the employee accepted a job with a competitor and was attempting to steal client lists. Early detection allows legal action before information leaves the organization.

**Adaptive Collaboration:** When Contoso begins a joint venture, adaptive security controls automatically adjust: external sharing is permitted for specific projects with automatic encryption and access expiration. When the project ends, all access automatically expires.

**Proactive Risk Management:** The security team monitors threat intelligence and notices a new attack technique targeting their industry. Before any attacks occur, they adjust detection rules and implement additional controls. When competitors are hit two weeks later, **Contoso experiences zero impact**.

Contoso now:

- Publishes a security white paper that clients can review
- Participates in industry security forums
- Is invited to speak at conferences
- Attracts talent who want to work where security is valued
- Wins contracts because clients trust Contoso to protect their most sensitive information

When the CEO reflects on their security journey: "Five years ago, a security breach nearly destroyed our company. Today, our security maturity is a cornerstone of our business strategy. Security isn't something we do—it's who we are."

#### Business Impact

- Security maturity as documented competitive advantage
- Industry recognition and thought leadership
- Culture where security considerations are natural, not forced

---

## Summary: Contoso's Journey

| Level | Investment | Timeframe | Key Outcome |
|-------|-----------|-----------|-------------|
| 100→200 | ~$75K | 6 months | Basic policies, still lost contract |
| 200→300 | ~$200K | 12 months | Won $3M contract, prevented breach |
| 300→400 | ~$350K | 18 months | Won $10M contract, 94% incident reduction |
| 400→500 | Ongoing ~5% IT budget | Continuous | Industry leadership, competitive advantage |

---

## Key Lessons from Contoso's Journey

1. **Progression takes time:** From Level 100 to Level 500 took five years of sustained effort
2. **Each level builds on the previous:** Maturity is progressive—you can't skip levels
3. **Business value increases at each level:** Each level enabled new opportunities and prevented threats
4. **Security becomes a differentiator:** What started as a cost center became strategic advantage
5. **Leadership commitment is essential:** Without sustained executive support, progression stalls
6. **Culture change is as important as technology:** Tools alone don't create security

---

## Your Next Steps

Regardless of where your organization is today, you can take action to improve security maturity:

### If You're at Level 100

- [ ] Conduct a security risk assessment to understand vulnerabilities
- [ ] Enable MFA for all users, starting with administrators
- [ ] Review Microsoft Secure Score and implement high-impact recommendations
- [ ] Assign someone responsibility for security
- [ ] Develop basic security policies for critical areas

### If You're at Level 200

- [ ] Assess gaps between written policies and actual practice
- [ ] Upgrade licensing if needed to access Conditional Access
- [ ] Implement organization-wide security awareness training
- [ ] Begin systematic review of Secure Score recommendations
- [ ] Establish incident response procedures and test them

### If You're at Level 300

- [ ] Implement automated threat detection with Defender for Office 365 and Endpoint
- [ ] Deploy comprehensive DLP policies across all channels
- [ ] Establish security metrics and regular reporting to leadership
- [ ] Begin planning for automation and integration
- [ ] Consider external security assessment to validate maturity

### If You're at Level 400

- [ ] Implement comprehensive SIEM capabilities (Microsoft Sentinel)
- [ ] Expand automation of threat detection and response
- [ ] Integrate security into all business processes
- [ ] Begin exploring Zero Trust architecture
- [ ] Share security practices externally as competitive differentiator

### If You're at Level 500

- [ ] Maintain vigilance—sustaining Level 500 requires continuous investment
- [ ] Continuously evaluate emerging technologies and threats
- [ ] Share lessons learned with industry peers
- [ ] Use security maturity as strategic business advantage
- [ ] Remember that security is a journey, not a destination

---

## Related Documents

- [Security Competency](microsoft365-maturity-model--security.md)
- [Maturity Model for Microsoft 365 - Introduction](microsoft365-maturity-model--intro.md)
- [How to Run a Maturity Model Workshop](microsoft365-maturity-model--run-workshop.md)
- [Governance, Risk, and Compliance Competency](microsoft365-maturity-model--governance-and-compliance.md)
- [Infrastructure Competency](microsoft365-maturity-model--infrastructure.md)

---

**Principal authors:**

- [Mats Warnolf](https://www.linkedin.com/in/matswarnolf/)
- [Clement Betacorne](https://www.linkedin.com/in/clément-betacorne-2411ba96/)

---

[!INCLUDE [mm4m365-core-team](includes/mm4m365-core-team.md)]
