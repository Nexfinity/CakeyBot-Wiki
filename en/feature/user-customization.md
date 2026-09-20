---
title: User Customization
description: Control how Cakey Bot notifies you across every server - level-up DMs, streak and decay reminders, achievement pings and claim reminders - plus your Cakey Personal settings.
published: 1
date: 2026-09-20T12:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-09-20T12:00:00.000Z
---

# Overview
The [User Customization](https://cakey.bot/user-customization) page is where **you**, not a server admin, decide how Cakey Bot contacts you. It is free for everyone. Sign in with Discord and open the page from your profile menu.

Changes on the page are saved as soon as you flip a switch.

# Notification Preferences (All Servers)
These switches apply in every server you share with Cakey Bot, including servers you join later.

| Setting | What it does |
| :------ | :----------- |
| **Level-up DMs** | Stops level-up messages that a server sends *by DM*. Level-up messages posted in a channel are public and are not affected. Nothing is sent instead. |
| **Streak reminder DMs** | Stops the DM sent shortly before your [streak](/en/feature/streaks) would run out. |
| **XP decay DMs** | Stops the DM sent when you lose XP to [XP decay](/en/feature/leveling). |
| **Ping me for achievement unlocks** | The [achievement](/en/feature/achievements) announcement is still posted in the server, just without notifying you. |
| **Claim reminders** | Master switch for [claim reminders](#claim-reminders). Turning it off stops all of them without deleting your per-server choices. |

> A server can still turn a notification off for everyone, and you can opt out of a single server (below), but nothing here can switch on something a server has disabled.
{.is-info}

# Server-Specific Preferences
Pick a server from the list to override the settings above for that server only:
* **Streak reminder DMs in this server**
* **Take part in streaks in this server**
* **XP decay DMs in this server**
* **Claim reminders** (daily, weekly and monthly separately)

> The page never creates streak or XP records for you. If you have not been active in a server yet, the streak and decay switches are shown as unavailable and your all-servers setting applies until you have some activity there.
{.is-info}

> If your DMs are closed, Cakey Bot cannot reach you and switches reminders off for you automatically.
{.is-warning}

# Claim Reminders
Get one DM when your daily, weekly or monthly economy reward is ready to claim again.

* They are **opt-in** and set per server: on the page above, or in Discord with `/eco reminders`.
* `/eco reminders` on its own shows your current settings. Add `daily`, `weekly` or `monthly` set to `True` or `False` to change them.
* You get **one reminder per reward** each time it becomes available, and one DM lists everything that is ready. There is at most one reminder DM every 10 minutes.
* Switching a reminder on while the reward is already available does not send a DM straight away. Reminders start after your next claim.
* You are only reminded for rewards you have claimed before, and not for very old ones (for example after the bot was offline).
* The DM has a **Turn off for this server** button.
* Servers can disable the daily, weekly or monthly reward. No reminder is sent for a reward the server has turned off.

# Cakey Personal Settings
If you have [Cakey Personal](/en/feature/cakey-personal), the page also shows:
* **Your plan** - billing period and when it renews or ends.
* **Your rank card** - a full banner editor for the rank card that replaces the server's card for you, with a button to go back to the server's card.
* **Leaderboard appearance** - lime highlight on or off, icon on or off, an icon from a set of eight (leaf, star, crown, bolt, gem, heart, flame, sparkles), whether your Personal status is shown on public leaderboard pages, and whether the Personal tier badge is shown on your rank card.
* **Your AI allowance** - how much of your monthly AI chat, image and voice allowance you have used, and when it resets.

If you do not have Personal, the page shows a short summary of it and a link to the [Cakey Personal page](https://cakey.bot/personal).
