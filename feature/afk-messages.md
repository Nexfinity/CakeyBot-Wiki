---
title: AFK Messages
description: Discord AFK status with Cakey Bot - Away messages, return notifications, status tracking. Automatic presence system guide.
published: 1
date: 2025-04-30T11:05:08.360Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:17:02.783Z
---

# Overview

AFK messages allow you to automatically display a message to users who ping you. This allows you to explain why you might not be responding or when you'll be back. AFK messages have a 100-character limit to prevent abuse and you are unable to use clickable links/user mentions in the message. Currently, AFK messages default to being permanent and will last until you or a server admin removes it. This behavior can be configured.

> AFK messages will also have a trashcan button added to them. When clicked, it will delete the AFK message in order to keep the channel clean. It will not remove the user from being AFK however.
{.is-info}

# Setting an AFK Message

You are able to set your own AFK message by typing `/afk <message>`. If you ever forget what you have your AFK message set to you can always type `/afk` without any message and it'll show what message you currently have set. (If one is set)

> Your AFK message will not be sent if a BOT mentions you or if you mention yourself.
{.is-warning}

# Removing an AFK Message

> Users who have the **`Manage Server`** permission node can force remove a user's AFK message using the `/unafk <user>` command.
{.is-info}

You are able to remove your own AFK message by typing the `/unafk` command.

Server moderators with **Manage Server** can also remove AFK statuses from the web dashboard and see a list of all currently applied AFK messages.

# Configuration

You can also configure AFK messages further by using our [Web Dashboard](https://cakey.bot/dashboard/public). There are a few options you can change:

| Name                | Description                                                                                                                                                    | Default Value | Min Value | Max Value | Premium Feature |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|-----------|-----------|------------------|
| AFK Module Status   | Toggles whether users can set AFK statuses in your server.                                                                                                     | Enabled       | N/A       | N/A       | No               |
| Max AFK Time        | Determines how long a user's AFK status remains before being removed. Use `-1` for permanent AFK status.                                                       | `-1`          | `1`       | `10080` (1 week)   | No               |
| AFK Prefix          | Automatically applies `[AFK]` to a user's nickname while AFK, and removes it once they return. Bot must have proper nickname permissions.                      | Disabled       | N/A       | N/A       | No               |
| Auto Remove AFK     | Automatically removes AFK status if a user sends a message or joins a voice channel (excluding being moved to AFK voice channels).                             | Enabled       | N/A       | N/A       | No               |

> In order for Cakey Bot to modify other user's nicknames Cakey Bot must have the `Manage Nicknames` permission AND Cakey Bot's highest role must exceed the user's highest role.
{.is-warning}

> **Helpful Tip:** You can also view all AFK users on our web dashboard.
{.is-success}

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /afk | Set an AFK status to display when you are mentioned. | \<reason> | None | 
| /unafk | Removes any AFK message you have set if one is set. (Unset other user's AFK if your admin) | [username] | None / ManageGuild | 