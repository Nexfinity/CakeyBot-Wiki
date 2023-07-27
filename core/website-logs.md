---
title: Dashboard Audit Logs
description: 
published: 1
date: 2022-12-22T00:53:32.823Z
tags: 
editor: markdown
dateCreated: 2022-10-18T07:55:26.492Z
---

# Overview
Cakey Bot has a few different logs which can be found on the website. This includes changes to the Bot settings via the Dashboard, Moderation actions performed by Moderators or Auto Mod and lists of persistent roles or temporary actions applied to users.

# How to locate your Website Logs
1. Head over to the [Web Dashboard](https://cakeybot.app/dashboard/public) and select your server.
2. Select the type of logs you want to look  at from the sidebar. ([Logs](https://cakeybot.app/dashboard/public/mod-logs), [Warnings](https://cakeybot.app/dashboard/public/warnings), [Persistent Roles](https://cakeybot.app/dashboard/public/persistent-roles) or [Temporary Actions](https://cakeybot.app/dashboard/public/temporary-actions))
3. If you selected Logs, you can also narrow it down by selecting one of the Dashboard, Moderation or Auto Mod tabs.
4. Scrolling down the page will reveal the options to switch pages as well as the number of results shown in the page.

# Dashboard Logs
These logs are added whenever anyone with Administrator or Manage Server permissions has used your Dashboard to change a Bot setting. This will include the time of the change, the Administrator's Discord tag, and what change they made.
![](https://cdn.discordapp.com/attachments/690401612254019625/1031873552502235187/unknown.png)

# Moderation Logs
These logs are added whenever one of your Server Moderators successfully use a moderation command on a user which creates a mod log. This will include the time of the moderation, which action was performed, the Discord tag of the user which was moderated, and the Discord tag of the moderator.
![](https://cdn.discordapp.com/attachments/690401612254019625/1031873552997158912/unknown.png)

# Auto Mod Logs
These logs are added whenever a user triggers automod in your server. This will include the time of the automod violation, the Discord tag of the user which triggered automod, and which filter they triggered.
![](https://cdn.discordapp.com/attachments/690401612254019625/1031873553362059284/unknown.png)

# Warnings
These logs are added whenever a user is warned by a moderator. This will include the time of the warning, the Discord tag of the user which was warned, the Discord tag of the moderator, and the reason for the warning.

To clear warnings from users in your server, you can use the `/clearwarnings` command
![](https://cdn.discordapp.com/attachments/690401612254019625/1031873553802465311/unknown.png)

# Persistent Roles/Mutes
This page contains a list of all of the persistent roles applied to users. Including any persistent mutes. These are roles that will automatically be re-applied to users if they leave and rejoin your server. You can also delete these roles from specific users with the delete button.
![](https://cdn.discordapp.com/attachments/690401612254019625/1031873554188349491/unknown.png)

# Temporary Roles/Actions
This page contains a list of all of the temporary roles and/or actions applied to users. This will include temporayr bans/mutes. These are roles that will automatically be expire and be removed from users some time in the future.
![](https://cdn.discordapp.com/attachments/690401612254019625/1031873554591010847/unknown.png)