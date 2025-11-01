---
title: Setup Permissions
description: Configure Cakey Bot Discord permissions - Role requirements, command restrictions, permission setup. Complete security guide.
published: 1
date: 2024-11-02T06:04:36.508Z
tags: 
editor: markdown
dateCreated: 2023-05-21T21:30:23.705Z
---

# Overview
By default most of Cakey Bot's commands will be available to most users and will be enabled in every channel. However, some of the more sensitive commands such as moderation commands will be locked/hidden to users who have access to ban, mute or manager other members of the server. In order to hide/disable specific commands you can either use Discord native UI to adjust command permissions or you can use our custom `/perms` commands. We have included guides for both methods below.

# Discord Integration Permissions
In order to configure permissions with Discord's native UI you can follow these steps:
1. Open up "Server Settings"
2. Go to Apps->Integrations
3. Select Cakey Bot
4. Find the command you want to adjust permissions for and click it
5. Set your desired permissions

If you would like a more detailed guide for using Discord's native UI you can check out Discord's own blog post on the feature [here](https://discord.com/blog/slash-commands-permissions-discord-apps-bots).