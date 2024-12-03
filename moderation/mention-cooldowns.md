---
title: Mention Cooldowns
description: 
published: 1
date: 2024-09-13T05:13:40.959Z
tags: 
editor: markdown
dateCreated: 2024-08-23T21:59:57.952Z
---

# Overview
The Role Mention Cooldown feature allows users to manage the frequency at which specific roles (up to 5) can be mentioned in Discord channels. This is useful for preventing role spam or controlling how often certain roles receive notifications.

This feature is ideal for managing high-traffic channels where certain roles may be over-mentioned, ensuring that these roles only receive pings when necessary. It prevents unnecessary spam and ensures that role notifications remain meaningful.

## Key Features
* **Customizable Cooldown Duration:** Users can set a cooldown for role mentions between 1 minute and 1440 minutes (24 hours). This ensures flexibility in how frequently roles can be mentioned.
* **Up to 5 Roles:** You can add up to 5 roles to be managed by the mention cooldown system, giving control over which roles are protected from excessive pings.
* **Automatic Cooldown Reset:** When a role is mentioned in a chat channel, it automatically becomes unmentionable for the duration of the cooldown. Once the cooldown expires, the role will be automatically restored to a mentionable state.
* **Automated Role Management:** No manual intervention is required to make roles mentionable again—everything is handled automatically, allowing for a hands-off experience once the cooldown is set.

# Setup
1. Login into the [web dashboard](https://cakey.bot/dashboard/public).
2. Select the server you want to configure.
2. From the left menu, select the "Mention Cooldowns" page.

## Add a Role

1. Click the green "Add Role" button to add a new role to the cooldown list.
2. A dropdown menu will appear where you can select the role you'd like to apply a cooldown to.
3. Enter the desired cooldown duration in minutes (from 1 to 1440).
4. Once you've configured the role and cooldown, click the "Update" button to save your changes.

> Note: For this to work, the role will need to initially be set where users can mention it, otherwise they won't be able to mention it to trigger the cooldown.
{.is-info}

## Remove a Role
If you wish to remove a role from the cooldown list you can follow these steps:
1. Locate the role in the list.
2. Click the red "x" button next to the role to remove it.
3. After making changes, click the blue "Update" button to save your configuration.