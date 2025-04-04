---
title: Support Tickets
description: 
published: 1
date: 2025-04-04T01:58:54.662Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:20:47.352Z
---

# Overview

> Make sure that Cakey Bot has the **`Manage Channels`** permission and that the Cakey Bot's role is _above_ the support staff role.
{.is-warning}

Cakey Bot's support ticket system allows your users to make tickets and get 1 on 1 support from your support team. You can easily manage tickets via Discord's button system and even save transcripts of the ticket history.

![Ticket Screenshot](/tickets1.png)

# Configure Tickets

1. Login to our [web dashboard](https://cakey.bot/dashboard/public).
2. Go to "Support Tickets".
3. Configure your desired settings

**Support Staff Role:** Selecting a support staff role will automatically allow users with the selected role to view/access all support tickets. If you do not select a support staff role only Administrators will have access to tickets.

**Transcript Channel:** Selecting a transcript channel will unlock the ability to save ticket history to the selected channel. Which will allow staff to review old closed/deleted tickets.

**Auto Save Transcripts:** If enabled, it will automatically create transcripts for all closed tickets. A transcript channel will have to be configured/set for this to function. <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>

# Usage/Creating Tickets

Once you have enabled and configured support tickets via the web dashboard your users can start making tickets once you create an embed using the `/setup createticketembed` command. Running this command will create a fancy embed with a button that users can click to automatically open up tickets. When users click the button it will prompt them to enter a reason for their ticket.

You do _not_ need to make/set up a support category, Cakey Bot will automatically generate the correct channels and permissions if Cakey Bot has access to do so.

> Cakey Bot will NEED acess to manage channels in order to create the required category and ticket channels.
{.is-warning}

Once a user has closed a ticket, Cakey Bot will send an embed with three different options:

* **Transcript:** Selecting this will save the contents of the ticket to a text file and uplaods it to your transcript channel.
  * If this option is disabled, you will need to configure your transcript channel on the web dashboard.
* **Open:** This option will re-open the ticket to allow the user to provide more information or to ask more questions.
* **Delete:** This option will delete the ticket and clears the channel history.
  * This option does NOT save a transcript unless auto-save is enabled.

![Closed Ticket Screenshot](/tickets2.png)

# Ticket Management
## Add User
You can add other users to tickets by typing the `/ticket adduser <user>` command. This will allow that user to view the ticket if they were not the one who created it. This command can be ran by anyone who can view and send messages within that ticket.

## Remove User
You can also remove other users from tickets by typing the `/ticket removeuser <user>` command. This will revoke that user's ability to view the ticket if they were added to it by the previous command or had access by other means. This command can be ran by anyone who can view and send messages within that ticket.

## Anonymous Replies
By default, any staff members who have view/send access to tickets can respond to them like they would in other channels. However, sometimes staff memebrs may want to reply to a ticket anonymously without showing their username. In order to this all they have to do is run the `/ticket anonreply <message>` command. this will send a generic anonymous message from Cakey Bot instead of the staff member.
> In order to use the anonymous reply system, the staff member MUST have the Support Team role which can be set on the web dashboard.
{.is-info}

## Reminders
Staff members can use the `/ticket remind` command to send a DM reminder to the user who opened the ticket. The DM prompts them to respond if the issue is still unresolved and provides a button link to open the ticket.

## Close Requests
The `/ticket request-close` command allows staff members to request the closure of a ticket. Instead of immediately closing the ticket, this command notifies the original user that opened the ticket that the staff have requested the ticket to be closed. The user can then review and approve or deny the request.

# Advanced Settings
These are advanced settings that you can configure via the web dashboard to further customize your support ticket system!

## Ticket Close Confirmation
Defaults to disabled. When enabled, this will prompt the user to confirm that they want to close the ticket with a Yes/No button message.

## DM User on Ticket Close
Defaults to disabled. When enabled, this will send attempt to send a DM to the user who opened the ticket once it has been closed with basic information about the ticket.
> **Note:** Sometimes users have DMs blocked or Discord will fail to send the DM. There is nothing Cakey Bot can do about this!
{.is-warning}

## Ping Staff Role on Ticket Creation
Defaults to disabled. When enabled, it will ping the Support Team staff role when a new ticket is created.
> **Note:** You MUST have a Support Team role configured on the web dashboard or this setting will not do anyhting.
{.is-info}

## Allow Feedback Ratings
This allows users to submit feedback ratings on the support they received inside of a ticket.

How it works:
1. Ticket is closed, transcript is created. (a transcript channel **MUST** be set for this feature to work)
2. The bot will send a DM to the user notifying the user their ticket was closed and ask for feedback.
3. The user can then rate their support between 1 and 5 stars.
4. This feedback will be posted/updated on the transcript message for the ticket in the server for staff to review.

> **Note:** Ticket transcripts must be enabled for this feature to work properly.
{.is-warning}

## Blacklisted Roles
This allows you to prevent specific roles from creating tickets. This can be useful if you have users who are spamming or abusing the ticket system.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /setup createticketembed | Create an embed to open tickets with a button. | N/A | None | 
| /ticket remind | Sends a reminder to the user. | N/A | None | 
| /ticket request-close | Requests to close the ticket. | N/A | None | 
| /ticket adduser | Adds a user to the ticket. | \<user> | None | 
| /ticket anonreply | Replies to a support ticket anonymously. | \<message> | None | 
| /ticket removeuser | Removes a user from a ticket. | \<user> | None | 