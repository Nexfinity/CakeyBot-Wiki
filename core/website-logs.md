---
title: Dashboard Audit Logs
description: 
published: 1
date: 2025-04-04T01:58:34.634Z
tags: 
editor: markdown
dateCreated: 2022-10-18T07:55:26.492Z
---

# Overview
Cakey Bot provides several logs accessible on the website. These include changes to bot settings via the dashboard, moderation actions taken by moderators or Auto Mod, and lists of persistent roles or temporary actions applied to users.

# How to locate your Website Logs
1. Head over to the [Web Dashboard](https://cakey.bot/dashboard/public) and select your server.
2. Select the type of logs you want to look  at from the sidebar. (Logs, Warnings, Persistent Roles, or Temporary Actions)
3. If you selected Logs, you can also narrow it down by selecting one of the Dashboard, Moderation or Auto Mod tabs.
4. Scrolling down the page will reveal the options to switch pages as well as the number of results shown in the page.

# Dashboard Logs
These logs are added whenever anyone with Administrator or Manage Server permissions has used your Dashboard to change a Bot setting. This will include the time of the change, the Administrator's Discord tag, and what change they made.
![Dasboard Log Screenshot](/logs1.png)

# Moderation Logs
These logs are added whenever one of your Server Moderators successfully use a moderation command on a user which creates a mod log. This will include the time of the moderation, which action was performed, the Discord tag of the user which was moderated, and the Discord tag of the moderator.
![Mod Log Screenshot](/logs2.png)

# Auto Mod Logs
These logs are added whenever a user triggers automod in your server. This will include the time of the Auto Mod violation, the Discord tag of the user which triggered the Auto Mod, and which filter they triggered.
![Auto Mod Log Screenshot](/logs3.png)

# Warnings
These logs are added whenever a user is warned by a moderator. This will include the time of the warning, the Discord tag of the user which was warned, the Discord tag of the moderator, and the reason for the warning.

To clear warnings from users in your server, you can use the `/clearwarnings` command.
![Warning Log Screenshot](/logs4.png)

# Persistent Roles/Mutes
This page contains a list of all of the persistent roles applied to users. Including any persistent mutes. These are roles that will automatically be re-applied to users if they leave and rejoin your server. You can also delete these roles from specific users with the delete button.
![Persistent Role Log Screenshot](/logs5.png)

# Temporary Roles/Actions
This page lists all temporary roles and actions applied to users, including temporary bans and mutes. These roles are set to automatically expire and will be removed from users at a designated time in the future.
![Temporary Role Log Screenshot](/logs6.png)