---
title: Birthdays
description: Discord birthday bot features - Track birthdays, send wishes, birthday roles with Cakey Bot. Community celebration guide.
published: 1
date: 2026-07-26T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2023-01-09T01:24:46.396Z
---

# Overview
You can configure Cakey bot to announce birthdays for your users. All birthdays are retricted to the server you set them in. this means you must manually set your birthday in every server that you would like it announced in. Before you can use any birthday commands, a server admin must enable the feature by selecting a birthday announcement channel.

# Usage
## Birthday announcement channel
The birthday announcement channel is where all of the birthday announcements will be sent in your server. You MUST set a birthday channel before any of the birthday commands can be used. If you do not set an announcement channel then birthdays will not be announced. The birthday channel can be set on the **Bot Settings** page of the [web dashboard](https://cakey.bot/dashboard) or by using the `/birthday channel <channel>` command.
> Note: Due to a Discord limitation you can't disable the birthday announcement channel by using the `/birthday channel` command. You will have to set it to "**None**" in the [web dashboard](https://cakey.bot/dashboard).
{.is-info}

## Setting your birthday
You can set your own birthday by running the `/birthday set <month> <day> [year]` command. `month` is selected from a dropdown and `day` must be between 1 and 31. You can also change or update your birthday by running this command again with the updated date.

The command replies ephemerally with a confirmation, for example:
> Successfully set @user's birthday to: `Jan 5th`
{.is-success}

> Server moderators can manually set/update another member's birthday by passing the optional `user` parameter.
{.is-info}

> The `year` parameter is completely optional — leave it out if you don't want to share it. If provided, it must be between **1900 and 2100**. Year is only ever shown back to you if you actually supplied one, for example `Jan 5th, 1995`.
{.is-info}

## View a user's birthday
You can view a single user's birthday with the `/birthday view <user>` command. This is not ephemeral, so everyone in the channel can see the response.

The response is formatted as, for example:
> @user's birthday is Jan 5th

with the year appended (e.g. `Jan 5th, 1995`) only if that user provided one when setting their birthday.

> If the user hasn't set a birthday, Cakey Bot will reply ephemerally letting you know.
{.is-info}

## View upcoming birthdays
You can view upcoming birthdays with the `/birthday next [limit]` command. This is not ephemeral. By default it will show the next 5 birthdays, soonest first, though you can specify a limit between 1 and 10. Once the calendar rolls over into next year, birthdays will wrap around and continue to be shown in order.

Only members still in your server are included. Each entry is formatted the same way as `/birthday view`, e.g. "@user's birthday is Jan 5th" (with the year appended only if provided).

## List all birthdays
You can view every saved birthday in your server with the `/birthday list` command. Birthdays are grouped and paginated by month — each page covers one month, and months with no birthdays are skipped entirely. Within a page, birthdays are ordered by day and formatted as, for example:
> **5th** - @user

Only members still in your server are included, and each page's footer shows "Page X of Y".

You can navigate between pages using the bot's standard pagination buttons (◀️ ⏮️ ⏭️ ▶️ to move between pages, 🛑 to stop). The menu stays active for 5 minutes of inactivity.

> If nobody in your server has a birthday saved, Cakey Bot will reply ephemerally letting you know.
{.is-info}

## Remove your own birthday or another user's birthday
You can remove your birthday by running the `/birthday remove` command. 
In addition to this you can remove another user's birthday by running `/birthday remove <user>`, however you must have **Manage Server** permission to remove the birthday of another user.

> **Helpful Tip:** You can also view and delete birthdays on the dashboard!
{.is-success}

# Birthday Role
You can also have Cakey Bot assign a temporary birthday role to users on the day of their birthday! This role will be added to the user when the announcement for their birthday is sent, and it'll be removed when the birthdays for the next day are checked. In order to set a birthday role you can either use the `/birthday role <role>` command or you can configure it on the birthday page of the [web dashboard](https://cakey.bot/dashboard).

A birthday role is NOT required for birthday announcements to be made. Announcements will be sent regardless if a role is set or not.

> Note: Due to a Discord limitation you can't disable the birthday auto role by using the `/birthday role` command. You will have to set it to "**None**" in the [web dashboard](https://cakey.bot/dashboard).
{.is-info}

> Note: In order to prevent abuse, Cakey Bot will prevent selecting roles that contain `Administrator`, `Manage Server` or `Manage Roles` permissions. In addition, if these roles gain this permission after being set, the bot will no longer assign them.
{.is-danger}

# Custom Birthday Message
By default, Cakey Bot announces birthdays with a generic message. You can customize this on the "Custom Birthday Messages" field of the birthday page of the [web dashboard](https://cakey.bot/dashboard).

You can enter multiple messages separated by a semicolon (`;`) — a random message from the list will be chosen each time a birthday is announced.

You can also use a few placeholders in your message(s):
* `{user.mention}` - Mentions the user whose birthday it is.
* `{user.username}` / `{user.nickname}` / `{user.globalname}` - The user's username, nickname, or global display name.
* `{server.name}` - Your server's name.

> The custom birthday message is capped at **5,000 characters**.
{.is-info}

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command                           | Description                                                          | Usage                                | Permission                |
| :-------------------------------- | :------------------------------------------------------------------- | :---------------------------------: | :-----------------------: |
| /birthday channel                 | Sets or updates the birthday announcement channel.                  | \<channel>                           | ManageServer or Administrator |
| /birthday list                    | View every saved birthday in the server, grouped by month.          | N/A                                   | None                      |
| /birthday next                    | View any upcoming birthdays.                                        | [limit]                              | None                      |
| /birthday remove                  | Remove your birthday. (Or another user's birthday)                  | [user]                               | None (Manage Server required to remove another user's birthday) |
| /birthday role                    | Sets or updates the birthday auto role.                             | \<role>                              | ManageServer or Administrator |
| /birthday set                     | Sets or updates your birthday. (Or, if a moderator, another user's) | \<month> \<day> [year] [user]        | None (Manage Server required to set another user's birthday) |
| /birthday view                    | View a user's birthday. (If they have one set)                      | \<user>                              | None                      |
| /setup clear-all-birthdays        | Remove ALL birthdays for the server.                                | \<confirm>                           | ManageServer or Administrator |
| /setup clear-missing-birthdays    | Remove birthdays for users who have left the server.                | \<confirm>                           | ManageServer or Administrator |