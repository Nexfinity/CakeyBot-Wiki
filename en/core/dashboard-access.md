---
title: Dashboard Access
description: Grant specific Discord users or roles access to the Cakey Bot web dashboard without requiring Manage Server or Administrator permission.
published: 1
date: 2026-07-09T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-07-09T00:00:00.000Z
---

# Overview
By default, only users with `Manage Server` or `Administrator` permission can access the web dashboard for a server. **Dashboard Access** lets a user who already has `Manage Server` or `Administrator` grant specific Discord **users** or **roles** access to the dashboard for that server, without the grantee needing `Manage Server` or `Administrator` themselves.

This is useful if you want to give someone (such as a moderator or a support-role holder) the ability to manage Cakey Bot's dashboard settings without giving them broader Discord server permissions.

> Dashboard Access only grants access to the **web dashboard**. It does not change what Discord slash commands a user can run — that is controlled separately by Discord's native permission system. See [Setup Permissions](/en/core/setup-permissions) for more info.
{.is-info}

# Granting Dashboard Access
1. Navigate to the [web dashboard](https://cakey.bot/dashboard) and select your server.
2. Go to the "Bot Settings" page.
3. Find the "Dashboard Access" section.
4. Add the Discord user (by Discord ID) or role you would like to grant access to.
5. Save your changes.

Once granted, the specified user(s) or role members will be able to log in and manage the dashboard for that server, even if they do not have `Manage Server` or `Administrator` permission.

# Removing Dashboard Access
You can remove a previously granted user or role from the "Dashboard Access" section on the Bot Settings page at any time. Removing access immediately prevents that user/role from managing the dashboard for the server, unless they separately hold `Manage Server` or `Administrator` permission.

# Related Commands
There are no slash commands for this feature — it is configured entirely through the web dashboard.
