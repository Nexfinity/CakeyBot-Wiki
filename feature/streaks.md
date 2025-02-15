---
title: Streaks
description: 
published: 1
date: 2025-02-01T17:05:48.850Z
tags: 
editor: markdown
dateCreated: 2025-01-28T23:45:44.838Z
---

# Overview

> Make sure that Cakey Bot has the **`Manage Nicknames`** permission and that the Cakey Bot's role is _above_ any users that it is trying to modify the nicknames of.
{.is-warning}

Encourage users to be active in your server by rewarding them for consecutive days of activity. Users can even compete on the leaderboard to see who has the longest streak!

# How It Works
Each time a user sends a message, their streak updates if at least 24 hours have passed since their last message. If more than 48 hours pass without a message, the streak resets. 

The bot will also automatically update the user's nickname to display their current streak alongside a customizable streak icon, ensuring real-time tracking of active participation.

> **Fun fact:** You can also create Achievements that unlock when users reach a certain number of days on their streak!
{.is-success}

# Setup
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard/public/) and select your server.
2. From the left sidebar, pick "Streaks".
3. After that check "Enable Feature".

**Done!** Streaks are now enabled in your server.

> **Note:** Due to a discord limitation, Cakey Bot will **never** be able to modify the nickname of the server owner, regardless of the role positions.
{.is-info}

## Custom Streak Icon
You can set a custom streak icon that will be used instead of `🔥`.

Here's how to do that:
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard/public/) and select your server.
2. From the left sidebar, pick "Streaks".
3. After that, under the "CStreak Icon" section, select the emote you would like to be used for the streak icon.

> You can even set custom streak emotes for 100 day streaks and 1 year streaks!
{.is-success}

## Ignored Channels
This is a list of channels that will be ignored when looking for messages to update a user's streak.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /streaks top | Shows the top streaks for the server. | N/A | None | 
| /streaks view | Shows your current streak. (Or the selected user's) | [user] | None | 
| /streaks toggle-opt-out | Allows you to opt out of streaks for your account. | N/A | None | 