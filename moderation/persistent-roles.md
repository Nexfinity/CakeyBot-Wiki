---
title: Persistent Roles
description: 
published: 1
date: 2024-12-04T03:34:52.209Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:12:19.317Z
---

# Overview

> Make sure that Cakey Bot has the **`Manage Roles`** permission and that the Cakey Bot's role is _above_ the roles it is trying to assign.
{.is-warning}

# Persistent Role Command

Persistent Roles will auto-assign the given roles to a user when they rejoin your server. This can be excellent on VIP, Staff or Mute roles.

To add/remove a persistent role from a user you can use the `/role persistent <user> <role>` command.

After you have added some persistent roles to a user, they will be automatically applied to the user when they rejoin your server.

> You can also view and remove persistent roles from our [web dashboard](https://cakey.bot/dashboard/public). However, you can not currently add persistent roles via the [web dashboard](https://cakey.bot/dashboard/public).
{.is-info}

# Persistent Mutes

A common use case for persistent roles is to automatically re-apply a mute role when a user leaves/joins the server to try and get rid of the mute or bypass it. If you use Cakey bot's mute command \(`/mute <user> <reason>`\), they will NOT have the mute role added as a persistent role. You will have to run the persistent role command separately OR you can enable "Persistent Mutes" on the moderation section of the [web dashboard](https://cakey.bot/dashboard/public) to have mutes added as persistent roles automatically.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| / | TBD | N/A | None | 