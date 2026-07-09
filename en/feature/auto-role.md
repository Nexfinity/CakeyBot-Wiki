---
title: Auto Role
description: Automatic Discord role assignment with Cakey Bot - Join roles, timed roles. Member management guide.
published: 1
date: 2025-11-01T06:20:01.773Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:17:36.935Z
---

# Overview

> Make sure that Cakey Bot has the **`Manage Roles`** permission and that the Cakey Bot's role is _above_ the roles it is trying to assign.
{.is-warning}

> Note: In order to prevent abuse, Cakey Bot will prevent selecting roles that contain `Administrator`, `Manage Server` or `Manage Roles` permissions. In addition, if these roles gain this permission after being set, the bot will no longer assign them.
{.is-danger}

Auto Role allows you to make Cakey Bot automatically give one or more roles to a member after they join your server. These roles are granted immediately unless you have the server Verification level set to High or Extreme. In which case, Cakey Bot will automatically grant the roles after 10 minutes have passed.

# Setup

Auto Role will automatically assign the configured role(s) to users when they join your server. You can select multiple roles to be assigned simultaneously. In order to set the Auto Role(s) you will need to set them in the [Web Dashboard](https://cakey.bot/dashboard). You can also remove/disable the Auto Role feature by simply setting the role with "none" in the dropdown menu.

> If your server has the High or Extreme Verification level set, the auto role will be given after 10 minutes in order to prevent bypassing discord verification levels.
{.is-info}