---
title: Should everyone create Teams - Low Code Provisioning solution
ms.date:  9/02/2020
author: LuiseFreese
ms.reviewer:  Joanne Hendrickson
localization_priority:
description: "Should everyone create Teams - Low Code Provisioning solution"
ms.collection: SPCommunity

---

# Should everyone create Teams?

This article shall shed a light on two aspects of Modern Workplace:

Teams Provisioning using a low-code solution while ensuring that Teams Owners are digitally literate enough to be responsible owners.

Uncle Ben was right: With great power comes great responsibility  —

If we give users great tools with great power, we also need to make sure to properly skill them up. We also need a lean process to deal with common asks.

Everyone wants to work with Teams as it provides us the collaborative workplace we need to be able to work from anywhere. And with Teams comes the relatively new concept (at least for an end-user) concept of ownership. Owning a Team empowers users to determine, how they want to collaborate, but we should also enable users to make wise decisions as they are literate enough to understand the implications.

Just blocking Group / Teams creation and have an established approval process owned by IT won't meet business needs as users will work around that and find shadow IT solutions. Just allowing everyone to create Groups and Teams will lead to over adoption: Too many Teams which should be channels, too many channels, which should be chats.

Key therefore is, to balance these extremes.

## Solution Overview

![LuiseFreese-LowCodeTeamsProvisioning-solution-overview](media/should-everyone-create-teams/solution-overview.png)

User asks in natural language a chatbot for a new team, a Power Automate flow picks up this information and checks if the user is already in an Azure AD security group called Educated Users. If the owner to be is already a member in this Educated Users security group, a second Power Automate flow gets the manager's approval and provisions the team. If the user is not a member of this group, user will be invited for training and test.

If the user passes the test, he /she will be added to the group of Educated Users ( which means that for the next team request, he/she doesn't need to pass a test again) and the second flow gets manager's approval and provisions the team.

If user doesn't pass the test OR if the manager doesn't approve, notifications will be sent and the process ends.

## What we need to build before we do the Chatbot

- 2 Security Groups in Azure AD for Educated Users and Uneducated Users
- Events for training in a calendar
- Form for training session invitations in Microsoft Forms
- Flow to send session invitations
- Form to test users
- Flow to log tests in a SharePoint list
- SharePoint list to calculate the result with a few calculated columns
- SharePoint list to log all teams requests

### 2 Security Groups in Azure AD

Go to portal.azure.com, click on GROUPS and then on NEW GROUP. Give the group names like "Educated" and "Uneducated".  Assign your users to the groups. By default, all users should be in the group of Uneducated Users.

### Form for training session invitations in Microsoft Forms

Go to forms.microsoft.com and ask in that form which training sessions the user wants to attend.

### Flow to send session invitations

Go to flow.microsoft.com and create a new flow without a template. Use the "when a new response is submitted" trigger from Forms, then the  "get the response details" of the form add a filter query to get the right event from the calendar, then update the event by adding the user to it.

![LuiseFreese-LowCodeTeamsProvisioning-flow-session-invitation](https://user-images.githubusercontent.com/49960482/91980043-f4cf7c00-ed26-11ea-89e5-32d96945e80f.png)

### Form to test users

Forms is able to do surveys (there are no correct answers) and quizzes (there ARE correct answers). Unfortunately, you can't use the score of a quiz in Power Automate to see if a user has passed the test, therefore create a normal survey and use a SharePoint list to calculate the result of the test.

### SharePoint list to calculate the result with a few calculated columns

Create a new list in SharePoint with these columns:

![LuiseFreese-LowCodeTeamsProvisioning-SP-List-columns](media/should-everyone-create-teams/demo-answers-to-quiz.png)

For the calculated columns:

![LuiseFreese-LowCodeTeamsProvisioning-SP-List-results](https://user-images.githubusercontent.com/49960482/91980948-61974600-ed28-11ea-8577-b8fef618d5e0.png)

### Flow to log tests in a SharePoint list

This Power Automate flow creates items in our SharePoint list. Go to flow.microsoft.com and click TEMPLATES, search for the "Record form responses in SharePoint" template.

### SharePoint list to log Teams requests

Create a new list and add columns Teamname, Description, Owner, Privacy, Status etc.

## Chatbot in Power Virtual Agents

We will now:

- create a  ChatBot in Power Virtual Agent
- create a Power Automate flow that's called from PVA
- create a 2nd Power Automate flow to provision a Team based on the information we got out of the first flow
- add our Bot as an App to Teams to publish it

### Create a Bot in Power Virtual Agent

Go to powerva.microsoft.com, create a new bot. Create a new topic and enter some trigger phrases. Don't try to be too formal, chatbot supports natural language understanding powered by LUIS.

Outline the conversation in the Authoring Canvas. Ask all the questions we need to get answered to provision a Team like team name, description, owner, and visibility. You can also already ask for the first members or channel names. Save all inputs as Variables and give them easily recognizable names like VarOwner or VarTeamName.

### A flow that's called from PVA

Click on the + sign to create the next node after your last question / message in Power Virtual Agent and click on CALL AN ACTION and then CREATE A FLOW

The PVA template will open up in a new browser tab. Save this template with a new name.

<img width="926" alt="LuiseFreese-LowCodeTeamsProvisioning-flow-from-pva" src="https://user-images.githubusercontent.com/49960482/91982264-46c5d100-ed2a-11ea-9f7c-26cadb7c5659.png">

Initialize your variables for all the information the user gives us so we can provision the team: team name, description, privacy, owner, members and first channel.

![LuiseFreese-LowCodeTeamsProvisioning-flow-initialize-vars](https://user-images.githubusercontent.com/49960482/91982515-a6bc7780-ed2a-11ea-99d4-59bdd8485d47.png)

After we took care of all variables we need to check the group membership of our owner.

The CHECK GROUP MEMBERSHIP action returns the string of the Group ID if a user is a member of the group and will return NULL if the user isn't member of that group.

![LuiseFreese-LowCodeTeamsProvisioning-flow-check-membership](https://user-images.githubusercontent.com/49960482/91982670-e3886e80-ed2a-11ea-83b6-56eb5fbbbfd5.png)

Expression: empty(null)

If he/ she is in the educated group, we can just log the request in the SharePoint list we already prepared.

![LuiseFreese-LowCodeTeamsProvisioning-flow-create-item](https://user-images.githubusercontent.com/49960482/91982835-19c5ee00-ed2b-11ea-97e2-655a08e7a6eb.png)

If the user is still in the Uneducated Group, we need to invite him/her to a training and test him/her — (and wait a bit so he/she can complete this).
![LuiseFreese-LowCodeTeamsProvisioning-flow-invite](https://user-images.githubusercontent.com/49960482/91982924-3a8e4380-ed2b-11ea-8915-d61e42802e52.png)

To invite the user to the training and link him/her to the test, we can use Adaptive Cards. If you never used Adaptive Cards before, just go to [https://adaptivecards.io/designer](https://adaptivecards.io/designer), select MICROSOFT TEAMS as host applications and replace the text of one of the samples with your text in the visual editor. Below, the Designer autogenerates some JSON for you — copy-paste this into a POST YOUR OWN ADAPTIVE CARD AS A FLOW BOT TO A USER action.

This is how our card looks then:

![LuiseFreese-LowCodeTeamsProvisioning-flow-AC](https://user-images.githubusercontent.com/49960482/91983040-68738800-ed2b-11ea-835e-eb87e0e4a015.png)

The clickable buttons link directly to the forms for training sessions (remember, we already built a flow to invite users automatically!) and the quiz (yet again, our flow logs the answers and SharePoint calculates the result for us!)

Now need to know if the user passed the test:

![LuiseFreese-LowCodeTeamsProvisioning-get-tested-user](https://user-images.githubusercontent.com/49960482/91983227-abcdf680-ed2b-11ea-9531-77870285b0f7.png)

If the user passes the test, he/she will be added to the Educated Group and we log the request in SharePoint. If the user doesn't pass, we will just send notifications and end the process.

![LuiseFreese-LowCodeTeamsProvisioning-flow-log-request](https://user-images.githubusercontent.com/49960482/91983245-b2f50480-ed2b-11ea-9895-4e592f733bb3.png)

### Create a 2nd flow to provision a Team based on the information we got out of the first flow

<img width="889" alt="LuiseFreese-LowCodeTeamsProvisioning-provisioningflow" src="https://user-images.githubusercontent.com/49960482/91983626-3e6e9580-ed2c-11ea-95b6-11d435738ef2.png">

**Microsoft Graph**
Power Automate doesn't provide an action "Create a Team". Therefore, we will call Microsoft Graph to create teams, add members, create channels, and a lot more, but we first need to authenticate to make this magic happen.

### Register an app in Azure AD

Go to portal.azure.com and click on APP REGISTRATIONS, and click NEW REGISTRATION. Give it a name and save the ID of your tenant and the ID of our App (Client) After that, click on API PERMISSIONS (use APPLICATION) and select MICROSOFT GRAPH. We need to add the Group.Read.Write.All permission and grant admin consent for that as well.
![LuiseFreese-LowCodeTeamsProvisioning-Application](https://user-images.githubusercontent.com/49960482/91985119-a7eea400-ed2c-11ea-8eb0-22e510a0f520.png)

To make it work, we also need an App Secret. Please, save this. In this minimal viable product, I just saved it in a variable, better to use Key Vault for that. Regardless where we store the App Secret: You only have ONE chance to save it, as soon as you leave this blade, you can't see it anymore.

### This is what you need to do in the 2nd flow in Power Automate

Your trigger is WHEN A NEW ITEM IS CREATED (remember, the PVA flow will end with this action, so basically, the PVA flow kicks off our second flow )

Now we need to initialize the following variables:

![LuiseFreese-LowCodeTeamsProvisioning-2ndflow-initialize-vars](https://user-images.githubusercontent.com/49960482/91986492-09167780-ed2d-11ea-990d-38fed84c7790.png)

- Tenant ID, App ID, App Secret are strings and we get all these IDs out of the app registration of the previous step
- Group ID is a string as well but is empty for now
- I was so tired of typing the Graph URL over and over that I put it into a var as well — this is optional
- We will later need the MailNickname to provision the Team.Mailnickname is the Displayname of the Team WITHOUT spaces. Use the replace expression: replace(DISPLPAYNAME," ","") which just means, replace all spaces with nothing.

### Manager's Approval

We will again create an Adaptive Card for this:

![LuiseFreese-LowCodeTeamsProvisioning-2ndflow-managers-approval](https://user-images.githubusercontent.com/49960482/91986768-6ca0a500-ed2d-11ea-8a13-cc9fe4d9b2d0.png)

Depending on the outcome we let Microsoft Graph create first a group and then update it to a team or we will end the process if the manager doesn't approve. Here is what happens if the Outcome is not Approved:

We update our SharePoint list (status is now rejected) and we post another Adaptive Card to our user to inform him/her and terminate the process.

![LuiseFreese-LowCodeTeamsProvisioning-2ndflow-managers-approvalNO](https://user-images.githubusercontent.com/49960482/91986920-9f4a9d80-ed2d-11ea-9684-d017384e57db.png)

If the Outcome of the Approval is Approved, we need to update our List as well and add an HTTP Call to first create a Group:

![LuiseFreese-LowCodeTeamsProvisioning-2ndflow-managers-approvalYES](https://user-images.githubusercontent.com/49960482/91987008-c1442000-ed2d-11ea-8f2e-8f93234b2f7b.png)

As we do not only want a Microsoft 365 Group but also a Team based on that group, we need the Group ID. To get this ID (remember, we initialized an empty var for that already!), we need the parse JSON action and set our Group ID var to that value:

![LuiseFreese-LowCodeTeamsProvisioning-2ndflowparsejson](https://user-images.githubusercontent.com/49960482/91987214-1122e700-ed2e-11ea-97ce-20fc5cf1b3da.png)

Now it's time to use another two HTTP calls for creating the Team and adding the channel:

![LuiseFreese-LowCodeTeamsProvisioning-2ndflowupdateteam](https://user-images.githubusercontent.com/49960482/91987351-3a437780-ed2e-11ea-8399-d495d33c933c.png)

Please keep in mind to expand the SHOW ADVANCED OPTIONS and enter all authentication information as shown in the Create a group step. Now update your SharePoint list (status is no created) and inform your user with another Adaptive Card in Teams:

### Publish our Bot & add it as an App in Teams

To publish your Bot, just click on PUBLISH in PVA and choose Microsoft Teams as Channel. Copy the APP ID and open App Studio in Teams, where you can create apps. Paste in this App ID and fill in Name, Description, and some links for your privacy statement and terms of use. As valid Domain use token.botframework.com. Download your app as a package and then install it from Teams App Catalogue.

This is our result as a gif:

![provisionbot](https://user-images.githubusercontent.com/49960482/91987925-f43ae380-ed2e-11ea-90c9-562583e96b8e.gif)

**Coming back to the purpose of solutions like this:**

The goal is to enable users and to give them great powers! We now have an easily maintainable solution for IT and a very lean process for the business side of a company to request common asks. We are more efficient as we only need to involve human working time if needed. We don't need to spend lots of time to make users adopt this system as the interface is easy to understand even for users who are not that tech-savvy, plus we have a good chance to narrow the historical gap between business and IT, #BetterTogether story.

If you don't like the chatbot approach, you can also work with a request form in Microsoft Forms or with a PowerApp if you prefer another UI.

---

**Principal author**: [Luise Freese](https://www.linkedin.com/in/luisefreese/)
