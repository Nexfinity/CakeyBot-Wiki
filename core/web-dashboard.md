---
title: Web Dashboard
description: Configure Cakey Bot via web dashboard - Easy Discord bot setup without commands. Visual configuration interface guide.
published: 1
date: 2025-04-30T09:06:17.629Z
tags: 
editor: markdown
dateCreated: 2022-09-01T02:36:22.985Z
---

# Overview

Cakey Bot is a highly customizable utility and moderation bot. You can configure many features and settings in Cakey Bot using our web dashboard. You can access our web dashboard by visiting [this link](https://cakey.bot/dashboard/public) or by clicking "Manage Servers" in the navigation bar of our website.

Once you have selected a server to manage, you will be taken to that server's home page. This page will show you general server stats and some basic bot settings like the default music volume, language, and command prefix. After you are on this page, you can either modify these settings or navigate to other modules to configure.

![image.png](/dash/image.png)

# Login
> You will need **`Manage Server`** or **`Administrator`** permission to manage servers.
{.is-warning}

To access the Web Dashboard, server administrators must:

1) Visit [this link](https://cakey.bot/dashboard/public) or click "Manage Servers" on the main Cakey Bot website
2) Authenticate with their Discord account
3) Select a server from the list of servers they have permission to manage
4) If Cakey Bot is not in the selected server, they will be prompted to invite the bot first

# Server Homepage
After selecting a server, administrators are taken to that server's homepage. This page displays:

* Server statistics (member count, channel count, etc.)
* Core bot settings (prefix, default music volume, language)
* Quick access to all available configuration modules

This serves as the central hub from which administrators can navigate to other sections of the dashboard.

# Manage/Customize

Once you have selected a server to manage, you will be taken to that server's homepage. The homepage will display basic statistics and general core settings for that server.

Once you have selected the server you want to modify you can change various features and core settings for it.

# Viewing Server Activity & Logs

The dashboard provides several read-only panels that display important information about your server:

## Moderation Logs
The logs panel shows a complete history of moderation actions taken in your server, including:

* Warnings issued
* Timeouts applied
* Bans and kicks
* Message deletions
* Other moderation activities

This provides administrators with a comprehensive audit trail of all moderation actions.

## User Warnings
This panel displays all current warnings that have been issued to users in your server, including:

* The user who received the warning
* The moderator who issued the warning
* The reason for the warning
* The date and time the warning was issued

## Temporary Actions
This panel displays temporary data/actions such as temporary roles and temporary bans.

# Best Practices
When using the Web Dashboard, consider these recommended practices:

1) **Regular Review:** Periodically review your configuration settings to ensure they still align with your server's needs.

2) **Permission Management:** Only give `Manage Server` or `Administrator` permissions to trusted individuals, as they will gain full access to the dashboard.

3) **Feature Integration:** When enabling new features, consider how they will interact with existing ones. For example, economy rewards might affect the leveling system.

4) **Testing Changes:** After making significant changes, test the functionality in your server to ensure it behaves as expected.

5) **Backup Settings:** Before making major configuration changes, consider documenting your current settings as a backup. The dashboard does not have any built-in rollback or backup systems.