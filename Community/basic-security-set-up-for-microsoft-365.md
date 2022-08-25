---
title: Basic Security Set Up for Microsoft 365
ms.date: 7/9/2020
author: helloitsliam
ms.reviewer: daisyfeller
manager: pamgreen-msft
ms.topic: article
ms.author: daisyfeller
ms.service: microsoft-365
localization_priority: 
description: Basic Security Set Up for Microsoft 365
ms.collection: M365Community
---

# Basic Security Set Up for Microsoft 365

[!INCLUDE [content-disclaimer](includes/content-disclaimer.md)]

## Security within Microsoft 365

Microsoft 365, as a service, contains many administration portals, options, and configuration settings focused solely on Security. Each service is protected predominantly by Azure Active Directory for Authentication, with each application authorizing users to access either the app itself content that resides within. Out of the box, newer tenants have the Security Defaults enabled that implement some necessary and best-practice capabilities. These are a great start; however, they shouldn't be the only configuration organizations should use. Organization-specific security controls and procedures should augment all out of the box configuration.

Security within Microsoft 365 is not just about enabling features and controls; it also involves the human side of teaching and guiding users to understand the restrictions and what they should be doing to help. Organization Security is a combination of Security Controls and Protection, combined with end-user training and guidance.

## Security Licensing

With all of the Microsoft 365 services, many-core security components come with the standard licensing. Features, such as the **Security Defaults**, are included in core licenses; however, most advanced Security capabilities are not. These features are either available as separate add-on licenses or bundled into the either the **Enterprise Mobility + Security E3/A3/G3**, **Enterprise Mobility + Security E5/A5/G5**, **Microsoft 365 E3/A3/G3**, **Microsoft 365 E5/A5/G5**, **Microsoft 365 E5/A5/G5 Security**, and **Microsoft 365 Business Premium**.

## Enabling the Security Defaults

The Security Defaults within Microsoft 365 reside within Azure Active Directory. By default, all Microsoft 365 Tenants, created on or after October 22nd, 2019, are equipped with these features. Tenants created previous to this date will not be enabled, though they may be available. These controls are available at no extra cost to the organizational license cost.

These defaults enable five of the most common security features and controls.

1. Enforcing Azure Multi-Factor Authentication registration for all users
2. Forcing Administrators to use Multi-Factor Authentication
3. Block Legacy Authentication protocols
4. Requiring all users to perform Multi-Factor Authentication when needed
5. Protect privilege access

A caveat to using these controls is that if you have custom created Conditional Access Policies, you cannot utilize them.

To enable the Security Defaults within your Microsoft 365 directory:

1. Sign in to the [Azure Portal](https://portal.azure.com) as either a Security Administrator, Conditional Access Administrator or Global Administrator
2. Click on **Azure Active Directory**, then click **Properties**
3. Select the link at the bottom labeled **Manage Security Defaults**
4. Set the **Enable Security Defaults** toggle to **Yes**
5. Select **Save**

You can also choose to disable these features and create your own set of security rules and controls, by either not enabling the Security Defaults or if they are enabled setting the Enable Security Defaults toggle to No. Learn more about the [Security Defaults provided out of the box](/azure/active-directory/fundamentals/concept-fundamentals-security-defaults#enabling-security-defaults).

## Custom Security Configuration

There is not a perfect configuration of Security controls or features that can meet every organizational need. There is not a single product that can achieve this, either. Best practice has mandated a mix of controls, features, services, and products to gain a better Security posture for a long time. Microsoft 365 security features are hierarchical, with Microsoft's highest level at the overall service level. Next is the Tenant level, which is then unique to your organization, with a core emphasis on Authentication and Authorization, including perimeter protection. Lastly, are the features available within each application and component, including shared options that span multiple components.

This design allows more granular control and protections that can cater to your organizational specific configuration. The advantage to this over the Security Defaults is that they are unique to what you need, and the level of risk you wish to accept.

## Accepting the Risk

The type of Security protections you might enable or deploy comes down to the level of risk you are willing to accept as an organization. Enabling or Disabling the Security Defaults will be precisely that. For example, when working within Microsoft 365 for Education, the Security Defaults are not the most efficient security controls to use. You may wonder why? If you remember, a core Security Default is forcing all users to register for Multi-Factor Authentication. If you are within a school, such as a High School, this will force all Students to register their Mobile Devices to access services. This approach forces all Students through the registration process, which would require extensive planning and support.

It then becomes a decision on assuming the risk. If you understand the risk, then the control for this becomes negated. Designing a Security plan for any organization will require this level of thinking and may not provide the security level that an organization needs.

## Basic Security Setup

Every Microsoft 365 Tenant needs a Security configuration. The out of the box capabilities provide the first line of defense at the service level. Even though Authentication controls are in place, they are not the only controls required.

There are ten core security controls and features, which will provide a solid foundation for other protections that can be applied as needed by the organization if enabled within all Tenants.

The following list of Security controls and features outlines the **Business and Security Risk**, **the Protection Features or Components**, and links for **How to Enable** the required protections.

### Multi-Factor Authentication

**Risk:** In nearly every Data and Security breach involving a compromised account, simply enabling Multi-Factor Authentication would have blocked the attack. Forcing every authentication request to validate a second factor, such as using an SMS or Token, will limit any malicious actors' ability to use the account.

**Protection:** Best practice dictates not to use SMS/Text messages where possible, as this has been under attack for a long time and is not as secure as it once was. Require end-users to install an Authentication app on their mobile devices that push the request to the device where they can approve as needed. These applications also provide in-time tokens that last a specific time and are available in situations where push notifications are not appropriate or cannot work.

Multi-Factor Authentication can be explicitly assigned to users or administrators or enforced using Conditional Access Policies. The preferred approach to implementing Conditional Access Policies. These policies provide more granularity when users need to provide the second factor, versus it having to be every time. Administrator Multi-Factor Authentication using Conditional Access Policies can be created and enabled for free, whereas end-user configuration does require every user to have a license that allows this to work.

**How:** To learn how to implement Administrator and User Multi-Factor Conditional Access Policies, use the links below.

* [Enable a Conditional Access Policy for Multi-Factor for Administrator Accounts](/azure/active-directory/conditional-access/howto-conditional-access-policy-admin-mfa#create-a-conditional-access-policy)
* [Enable a Conditional Access Policy for Multi-Factor for all User Accounts](/azure/active-directory/conditional-access/howto-conditional-access-policy-all-users-mfa#create-a-conditional-access-policy)

**NOTE:** Be aware that adding a single Azure Active Directory Premium (Plan 1 or Plan 2) for an Administrator will enable the features, but not license it for every user.

### Sign Out Inactive Users Automatically

**Risk:** Long or non-existent session timeouts leave sessions vulnerable to re-use by people other than the current user. Users of a public computer might close the browser, thinking that they would automatically log them out. An attacker might then re-open the browser some time afterward, re-entering the same session. An attacker with access to the user ID might be able to re-enter the session without re-authenticating.

**Protection:** The Idle session sign-out lets organizations specify when end-users receive a warning and automatically sign out of Microsoft 365. After the specified period of inactivity within SharePoint Online and OneDrive for Business, automatic sign-out occurs. This sign-out activity works using end-user requests sent to SharePoint Online or OneDrive for Business, not by moving the mouse in the browser when accessing either service.

Users will be signed out from all Microsoft 365 services with a time specified, not just SharePoint Online and OneDrive for Business unless they have selected to stay signed-in. The end-user experience is different if they are inactive in other browser tabs but not in a SharePoint Online or OneDrive for Business one; then, all tabs will stay signed in.

**How:** Learn how to [implement Idle Session Sign-out](/sharepoint/sign-out-inactive-users#specify-idle-session-sign-out-settings-in-the-new-sharepoint-admin-center).

### Block Legacy Authentication

**Risk:** Legacy authentication protocols use basic authentication. These protocols, such as POP, SMTP, IMAP, and MAPI, can't enforce any second-factor authentication, making them preferred entry points for malicious actors attacking the organization. More than 99 percent of all password spray attacks within Azure Active Directory, utilized legacy authentication. To add, more than 97 percent of all Credential Stuffing attacks against Azure Active Directory also used legacy authentication.

**Protection:** Though blocking legacy authentication is critical to the Microsoft 365 Tenant's Security, you need to ensure that all applications and mail protocols used to support the modern authentication approach and work without the legacy capabilities. Such applications and services that utilize legacy authentication are:

* *Authenticated*
* *SMTP*
* *Autodiscover (used by Outlook)*
* *Exchange ActiveSync*
* *Exchange Online PowerShell*
* *Exchange Web Services*
* *IMAP4*
* *MAPI over HTTP (used by Outlook 2010 and later)*
* *Offline Address Book*
* *Outlook Anywhere (RPC over HTTP)*
* *Outlook Service POP3*
* *Reporting Web Services*

To help identify legacy authentication used within your organization, you can filter the Azure Active Directory Sign-ins and validate that legacy is either required or can be disabled.

1. Sign in to the [Azure Portal](https://portal.azure.com) as either a Security Administrator, Conditional Access Administrator or Global Administrator
2. Click on **Azure Active Directory**, then click **Sign-ins**
3. Add the Client App column by clicking **Columns**, then **Client App**
4. Click **Add Filters**, then **Client App**
5. Select all **Legacy Authentication Protocols**, then click **Apply**

Filtering will only show you the attempted sign-ins that used legacy authentication protocols. To view the actual protocol used, you can click onto an entry, and it is displayed.

Blocking legacy authentication is performed by configuring conditional access policies.

**How:** Learn how to [block legacy authentication](/azure/active-directory/conditional-access/block-legacy-authentication).

### Set User Passwords to Never Expire

**Risk:** When enforcing periodic password resets, passwords become less secure. Users tend to pick a weaker password and vary it slightly for each reset. This type of behavior can often lead to the re-use of existing passwords, as well as malicious attackers, guessing the password. If a user creates a secure password (long, complicated, and without any pragmatic words present), it should remain as strong in 60 days as it is today.

**Protection:** It is now recommended by the National Institute of Standards and Technology (NIST) to disable password expiration. The guidance is only to force a change or update a password if an account is confirmed as compromised. Azure Active Directory provides the ability to set password expiration policies and disable it for specific users or all users.

There are two options for disabling expiration of passwords:

1. Disable password expiration either on a per-user or for the organization within Azure Active Directory
2. Sync passwords from On-premises Active Directory using Azure AD Connect. This sync includes password policies

**How:** Learn how to implement password expiration policies using the links below.

* [Set the password expiration policy for your organization](/microsoft-365/admin/manage/set-password-expiration-policy)
* [Set an individual user's password to never expire](/microsoft-365/admin/add-users/set-password-to-never-expire)

### Banned Password List

**Risk:** It is common practice for end-users to reuse existing passwords across multiple services, whether personal or business. It is also common for easy to discover passwords to be used. When accounts use either common or simple passwords, there is a higher chance of account breach.

**Protection:** Azure Active Directory includes a global banned password list, that protects all Microsoft 365 services. Azure Active Directory also provides organizations the ability to add a list of banned passwords. As users change their passwords in the cloud, if the new password matches any of the prohibited passwords, the end-user will be notified, and they will need to change the password they typed. The custom banned password feature is limited to 1000 words. It is not for blocking large lists of passwords.

**How:** Learn how to [implement a banned password list](/azure/active-directory/authentication/tutorial-configure-custom-password-protection)

### External Sharing

**Risk:** External sharing of content is always a risk for any organization. Due to how SharePoint assigns permissions and control access, data such as Personally Identifiable Information (PII) data might get shared externally with no protections, especially if any external email is allowed. *SharePoint External Sharing* is a top-level configuration setting which controls sharing content from SharePoint to anyone, including non-corporate accounts. This setting is available at the Tenant organization level, which is utilized at lower levels within Office 365 unless set explicitly at the application level.

**Protection:** Microsoft 365 provides external sharing settings at the tenant and application levels. The decision to modify these settings should be business-related. Setting this to **Only people in your organization**, limits external sharing capabilities. Content can then only be shared using accounts that already exist within the existing Azure Active Directory, whether internal users or external guest accounts. Adding external accounts then becomes a controlled process.

**How:** Learn how to [implement external sharing protections](/sharepoint/turn-external-sharing-on-or-off )

### Account Lockout Threshold

**Risk:** Many successful account compromises happen because simple protections aren't defined. The most common is the number of times a password can be entered incorrectly before locking the account. The higher the number, the more times a malicious actor has to **guess** the password freely.

**Protection:** Azure Active Directory Smart lockout uses cloud intelligence to lock out malicious actors trying to guess end-users passwords. The intelligence platform recognizes sign-ins from valid users and treats those differently from those that attackers and other unknown sources. The smart lockout can lock out the attackers yet still allow users to continue to access their accounts. Smart lockout is on by default within all Azure Active Directory instances; however, organizations can customize them as needed. The default setting is ten failed sign-ins, with the recommendation to set lower as required and in conjunction with the organization.

**How:** Learn how to [implement account lockout threshold](/azure/active-directory/authentication/howto-password-smart-lockout)

### Mobile Application Management Policy

**Risk:** When end-users connect mobile devices to Microsoft 365 if they are Bring-Your-Own-Devices (BYOD), they could sync OneDrive and SharePoint content locally off the corporate network and devices.

**Protection:** Microsoft 365 provides rules that ensure an organization's data remains safe or contained in a managed app. These policies can include rules that block the user's attempt to access or move *corporate* data or are a set of prohibited or monitored actions users can perform when in the app. Mobile application management policies are independent of a Mobile Device Management (MDM) solution and do not require enrollment of devices.

The core benefits of Mobile application management (MAM) policies are:

1. Protect organizational data at the app level
2. End-user productivity isn't affected
3. Policies don't apply when app use is in a personal context
4. App protection policies make sure that app protections are in place

Using Mobile application management (MAM) policies will require end-users to have a license for Microsoft Intune assigned to their Azure Active Directory account.

**How:** Learn how to [implement mobile application management policies](/mem/intune/apps/app-protection-policies)

### Block Client Forwarding Rules

**Risk:** Client Rules Forwarding Block lets you manage email auto-forwarding in your organization. Using client-side forwarding rules to exfiltrate data to external recipients is becoming an increasingly used vector for attackers.

**Protection:** Exchange Online provides the ability to enable client forwarding rules and disable them. There are three core options:

* **Remote Domains** - Set 'Allow automatic forwarding' to disable
* **Role-Based Access Control (RBAC)** - Use RBAC to limit the impact by creating a new management role that restricts forwarding and delivery
* **Transport Rules** - Implementing a Transport Rule can stop emails set to be Auto-Forwarded to an external address. These transport rules use 'IF' logic. The rule checks if the sender is located 'Inside the organization', along with if the recipient is located 'Outside the organization', and if the message type is 'Auto-Forward', then it rejects the message.

**How:** Learn how to [block and control client forwarding rules](https://support.microsoft.com/office/stop-auto-forwarding-emails-in-microsoft-365-f9d693ba-5c78-47c0-b156-8e461e062aa7)

### Do not allow users to grant consent to un-managed applications

**Risk:** Before an application can access organizational data, a end-user must grant the application permissions. By default, all users can consent to applications for permissions that don't require administrator consent. By allowing users to give apps access to data, users can easily acquire useful applications and be productive. However, this configuration can represent a risk if it's not monitored and controlled carefully. There is even a possibility of data exfiltration from the tenant. Attackers can maintain persistent access to services through these integrated apps, without relying on compromised accounts.

**Protection:** Azure Active Directory provides two core protections to mitigate the risk.

* Modify how end-user consent applications
* Enable the administrator consent workflow

When modifying how end-user consent applications, organizations can choose from three options:

Disable user consent - End-users cannot grant permissions to any apps.
Users can consent to apps - End-users can only consent to apps published by a verified publisher and registered in the tenant.
Users can consent to all apps - This option allows all end-users to consent to any permission, which doesn't require admin consent.

**How:** Learn how to manage end-user and administrator app consent, use the links below.

* [Configure how end-users consent to applications](/azure/active-directory/manage-apps/configure-user-consent)
* [Configure the admin consent workflow](/azure/active-directory/manage-apps/configure-admin-consent-workflow#enable-the-admin-consent-workflow)

## Security Considerations

With any security configuration, they are only as good as the attacks that are known. New attack types are surfacing almost daily, which could make these controls ineffective. To help mitigate Microsoft 365 provides multiple logging capabilities and reports. Some are straight reports or log entries; others provide feedback or even instruction on how to mitigate.

It is essential to continually monitor and review these reports and logs, not only to ensure they are working but also to implement further controls and capabilities as they are needed.

---

**Principal author**: [Liam Cleary](https://www.linkedin.com/in/liamcleary)
