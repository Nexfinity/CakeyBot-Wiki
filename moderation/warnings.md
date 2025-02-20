---
title: Warnings
description: 
published: 1
date: 2025-02-19T21:13:32.647Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:13:25.136Z
---

# Overview
Warnings will record the date the warning was received, the reason as well as the moderator who made the warning. Warnings will also automatically post to your [Audit Log](https://wiki.cakey.bot/en/moderation/audit-log) if you have one set up for Cakey Bot. This makes it useful to record previous moderation history for a user and allows you to impost stronger moderation punishments for repeat offenders.

# Usage
## Warn Users
You can warn users with a given reason using the `/warn <user> <reason>` . It will place a warning on their account which you can then view later. By default warnings will also send the user a DM. There is also an optional "isSilent" parameter which will suppress the DM sent to the user for the warning.

> Warnings will also be sent to Cakey bot's audit log as a special event if you have one configured for moderation logs.
{.is-info}

## Anonymous Warnings
The `/warn` command also includes an optional "isAnonymous" parameter. If this is set to true, the user will not see the moderator's name who warned them. 

This will be applied on:
* The DM the user receives (if warning is not silent)
* The audit log entry (Some servers display this publicly)
* The `/warnings` comamnd when ran by a non-moderator

This will NOT be applied on:
* The `/warnings` command when ran by a moderator
* When the "View Warnings" button is pressed on the `/warn` confirmation message
* The website dashboard audit logs
* When a warning is triggered/created via automod or button press

> **Note:** Other moderators will still be able to see the moderwator who gave the warning.
{.is-info}

## View Warnings
There are a few ways to view warnings for users. The most popular method is to view them with slash commands however you can also access them from the web dashboard. This list will include the warning ID, the moderator who gave the warning as well as the time and reason for the warning.
> **TIP!** You can also view warnings using the button that pops up after you warned someone. {.is-success}

### With Commands
You can view a user's warnings with the `/warnings <user>` command. This will show every warning the user has been given in that server and the status of it (if it is active or expired). If there's too many results, the embed will be paginated with buttons under the embed.

### With Dashboard
You can also view warnings on our web dashboard. Once you log in and select a server, you can select the "Warnings" page on the left sidebar.

## Remove Warnings
Cakey Bot provides a few ways to remove and clear warnings from users.

### Single Warning
You can clear a specific warning from a user with the `/unwarn <id>` command. You can get the warning ID from the `/warnings <user>` command or from the [web dashboard](https://cakey.bot/dashboard/public).

### Clear All Warnings
You can clear every warning from a user with the `/clearwarnings <user>` command.
> This command can NOT be undone! Once you've cleared every warning you will have to manually re-add any warnings you want the user to have.
{.is-warning}

# Warning Auto Punishments
> **Note:** Warning auto punishments will only apply to ACTIVE warnings. Expired and soft-deleted warnings are excluded from the count. {.is-info}

## Overview
The "Warning Auto Punishments" feature in Cakey Bot automatically enforces consequences for rule violations by tracking user warnings and triggering pre-defined punishments, such as mutes, kicks, or bans. It helps maintain a healthy community environment, reduces the burden on moderators, and ensures consistency and fairness in disciplinary actions.

## Configuration
You can configure the Warning Auto Punishments feature from the [web dashboard](https://cakey.bot/dashboard/public/), on the "Warnings" page.
Here's how to add your first auto-punishment:
1. Click "Add Punishment".
2. Select the punishment and the required warnings to get that punishment.
3. Click "Update"

**DONE!** You've added your first auto-punishment. You can now repeat this process for additional punishments (up to 10 punishments).

# Auto Moderation Punishment
If you have any Auto Mod events enabled you can set the punishment to automatically warn users when the violate the rules as well. Any warnings given by Auto Mod will be listed next to regular warnings and will be able to removed using the same methods.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /clearwarnings | Removes all warnings from the specified user. | \<user> | MuteMembers or Administrator | 
| /unwarn | Unwarns the specified user. | \<id> [isSilent] | MuteMembers or Administrator | 
| /warn | Warns the specified user. | \<user> \<reason> [isSilent] [isAnonymous] | MuteMembers or Administrator | 
| /warnings | List all warnings for the specified user. | \<user> | MuteMembers or Administrator | 