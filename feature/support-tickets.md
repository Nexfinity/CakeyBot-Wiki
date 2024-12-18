---
title: Support Tickets
description: 
published: 1
date: 2024-12-18T03:02:20.557Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:20:47.352Z
---

# Overview

> Make sure that Cakey Bot has the **`Manage Channels`** permission and that the Cakey Bot's role is _above_ the support staff role.
{.is-warning}

Cakey Bot's support ticket system allows your users to make tickets and get 1 on 1 support from your support team. You can easily manage tickets via Discord's button system and even save transcripts of the ticket history.

![](/tickets1.png)

# Configure Tickets

1. Login to our [web dashboard](https://cakey.bot/dashboard/public/).
2. Go to "Support Tickets" [here](https://cakey.bot/dashboard/public/tickets).
3. Configure your desired settings

**Support Staff Role:** Selecting a support staff role will automatically allow users with the selected role to view/access all support tickets. If you do not select a support staff role only Administrators will have access to tickets.

**Transcript Channel:** Selecting a transcript channel will unlock the ability to save ticket history to the selected channel. Which will allow staff to review old closed/deleted tickets.

**Auto Save Transcripts:** If enabled, it will automatically create transcripts for all closed tickets. A transcript channel will have to be configured/set for this to function. <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>

# Usage/Creating Tickets

Once you have enabled and configured support tickets via the web dashboard your users can start making tickets using the `/ticket create <description>` command. You can also create a embed with a button to create tickets with using the **Ticket Creation Embed** section below.

> **Note:** The issue description is optional and a default reason will be filled in if a user does not provide one.
{.is-info}

You do _not_ need to make/set up a support category, Cakey Bot will automatically generate the correct channels and permissions if Cakey Bot has access to do so.

Once a user has closed a ticket, Cakey Bot will send an embed with three different options:

* **Transcript:** Selecting this will save the contents of the ticket to a text file and uplaods it to your transcript channel.
  * If this option is disabled, you will need to configure your transcript channel on the web dashboard.
* **Open:** This option will re-open the ticket to allow the user to provide more information or to ask more questions.
* **Delete:** This option will delete the ticket and clears the channel history.
  * This option does NOT save a transcript unless auto-save is enabled.

![](/tickets2.png)

# Ticket Management
## Add User
You can add other users to tickets by typing the `/ticket adduser <user>` command. This will allow that user to view the ticket if they were not the one who created it. This command can be ran by anyone who can view and send messages within that ticket.

## Remove User
You can also remove other users from tickets by typing the `/ticket removeuser <user>` command. This will revoke that user's ability to view the ticket if they were added to it by the previous command or had access by other means. This command can be ran by anyone who can view and send messages within that ticket.

## Anonymous Replies
By default, any staff members who have view/send access to tickets can respond to them like they would in other channels. However, sometimes staff memebrs may want to reply to a ticket anonymously without showing their username. In order to this all they have to do is run the `/ticket anonreply <message>` command. this will send a generic anonymous message from Cakey Bot instead of the staff member.
> In order to use the anonymous reply system, the staff member MUST have the Support Team role which can be set on the web dashboard.
{.is-info}

# Advanced Settings
These are advanced settings that you can configure via the web dashboard to further customize your support ticket system!

## Ticket Close Confirmation
Defaults to disabled. When enabled, this will prompt the user to confirm that they want to close the ticket with a Yes/No button message.

## DM User on Ticket Close
Defaults to disabled. When enabled, this will send attempt to send a DM to the user who opened the ticket once it has been closed with basic information about the ticket.
> Note: Sometimes users have DMs blocked or Discord will fail to send the DM. There is nothing Cakey Bot can do about this!
{.is-warning}

## Ping Staff Role on Ticket Creation
Defaults to disabled. When enabled, it will ping the Support Team staff role when a new ticket is created.
> Note: You MUST have a Support Team role configured on the web dashboard or this setting will not do anyhting.
{.is-info}

## Allow Feedback Ratings
This allows users to submit feedback ratings on the support they received inside of a ticket.

How it works:
1. Ticket is closed, transcript is created. (a transcript channel **MUST** be set for this feature to work)
2. The bot will send a DM to the user notifying the user their ticket was closed and ask for feedback.
3. The user can then rate their support between 1 and 5 stars.
4. This feedback will be posted/updated on the transcript message for the ticket in the server for staff to review.

> Note: Ticket transcripts must be enabled for this feature to work properly.
{.is-warning}

## Blacklisted Roles
This allows you to prevent specific roles from creating tickets. This can be useful if you have users who are spamming or abusing the ticket system. This will blacklist users from creating tickets via the `/ticket new` command as well as any ticket embeds.

## Embed Color
This will modify the color for the initial embed that is created inside of newly created tickets.

# Ticket Creation Embed

## Default Embed
You can also create a fancy embed with a button that users can click to automatically open up tickets instead of using the slash commands as well. You can create this embed using the `/setup createticketembed default` command.

> You can set a custom message and a custom color for this default embed on the Web Dashboard! You are also able to use [Basic Placeholders](https://wiki.cakey.bot/en/placeholders) in this custom message.
{.is-info}

## Reason Categories
You can also create category-specific embeds which will prompt users to select a reason from a dropdown menu to pre-fill the ticket with. You can create these category embeds by typing `/setup createticketembed <type>`. You can check out the full list of category types and their pre-filled reasons below:
  * Select menu - User Reporting
    * Report User - Broke Rules
    * Report User - Inappropriate Content
    * Report User - Spamming
    * Report User - Scamming/Phishing
    * Report User - Advertising
    * Report User - Malicious Files
    * Report User - NSFW Content
    * Report User - Account Hacking
    * Report User - Bug Abuse
  * Select menu - Moderation
    * Question About Rules
    * Warning Appeal
    * Mute/Ban Appeal
  * Select menu - Purchase issue
    * Payment issue
    * Refund request
    * Missing item/product
  * Select menu - Technical
    * Bug Report
    * Suggestion
    * Feedback
    * Question
    
# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /setup createticketembed | Create an embed to open tickets with a button. | N/A | None | 
| /ticket adduser | Adds a user to the ticket. | \<user> | None | 
| /ticket anonreply | Replies to a support ticket anonymously. | \<message> | None | 
| /ticket create | Create a new support ticket. | [description] | None | 
| /ticket removeuser | Removes a user from a ticket. | \<user> | None | 