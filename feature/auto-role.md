---
title: Auto Role
description: 
published: 1
date: 2024-10-10T02:49:16.000Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:17:36.935Z
---

# Overview

> Make sure that Cakey Bot has the **`Manage Roles`** permission and that the Cakey Bot's role is _above_ the role it is trying to assign.
{.is-warning}

> If your server has the High or Extreme Verification level set, the auto role will be given after 10 minutes in order to prevent bypassing discord verification levels.
{.is-info}

> Note: In order to prevent abuse, Cakey Bot will prevent selecting roles that contain Administrator, Manage Server or Manage Role permissions. In addition, if these roles gain this permission after being set, the bot will no longer assign them.
{.is-danger}

Auto Role allows you to make Cakey Bot automatically give a specific role to a member after they join your server. This role is granted immediately unless you have the server Verification level set to extreme. In which case, Cakey Bot will automatically grant the role after 10 minutes have passed.

# Setup

Auto Role will automatically assign the given role to users when they join your server. In order to set the Auto Role you will need to set it in the [Web Dashboard](https://cakey.bot/dashboard/public/). You can also remove/disable the Auto Role feature by simply setting the role with "none" in the dropdown menu.
