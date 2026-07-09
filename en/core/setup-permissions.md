---
title: Setup Permissions
description: Configure Cakey Bot Discord permissions - Role requirements, command restrictions, permission setup. Complete security guide.
published: 1
date: 2025-11-01T06:19:47.103Z
tags: 
editor: markdown
dateCreated: 2023-05-21T21:30:23.705Z
---

# Overview
By default most of Cakey Bot's commands will be available to most users and will be enabled in every channel. However, some of the more sensitive commands such as moderation commands will be locked/hidden to users who have access to ban, mute or manager other members of the server. In order to hide/disable specific commands you can use Discord's native UI to adjust command permissions. We have included a guide for this below.

# Discord Integration Permissions
In order to configure permissions with Discord's native UI you can follow these steps:
1. Open up "Server Settings"
2. Go to Apps->Integrations
3. Select Cakey Bot
4. Find the command you want to adjust permissions for and click it
5. Set your desired permissions

If you would like a more detailed guide for using Discord's native UI you can check out Discord's own blog post on the feature [here](https://discord.com/blog/slash-commands-permissions-discord-apps-bots).

# Dashboard Access Permissions
Command permissions control who can use Cakey Bot's commands in Discord, but you can separately control who can access the **web dashboard** for your server. By default, only users with `Manage Server` or `Administrator` permission can access the dashboard. However, admins can grant specific Discord users or roles dashboard access without requiring them to have `Manage Server` or `Administrator` themselves.

For more details on how to configure this, see the [Dashboard Access](/en/core/dashboard-access) page.