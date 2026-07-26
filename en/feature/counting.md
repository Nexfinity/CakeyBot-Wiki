---
title: Counting
description: Discord counting game with Cakey Bot - group counting channel, strict or equation mode, streak tracking. Community engagement guide.
published: 1
date: 2026-07-26T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-07-26T00:00:00.000Z
---

# Overview
**Counting Game** lets your members work together to count upward as a group in a dedicated channel. One person posts a number, the next person continues the count, and so on — if someone breaks the count, what happens next depends on how you've configured the feature.

> Counting Game is configured entirely through the [web dashboard](https://cakey.bot/dashboard) — there is no slash command for it.
{.is-info}

# Accessing Counting Game Settings
1. Open the [web dashboard](https://cakey.bot/dashboard) and select your server.
2. Click "Counting Game" in the left sidebar.
3. Configure your settings and press "Save Changes" to apply them.

# Settings

## Channel
The single channel where the counting game is active. Only messages sent in this channel are checked as counts.

## Mode
Controls what counts as a valid next number.

* **Strict** - The next message must be exactly the next number. For example, after `3` is posted, the next message must be `4`.
* **Equation** - The next message can be any valid math expression that evaluates to the next number. For example, after `3` is posted, someone could post `2*2` for `4`.

## Prevent Consecutive Counting
> Enabled by default.
{.is-info}

When enabled, the same person can't post two counts in a row - someone else has to post the next number before that person can count again.

## Reset on Mistake
> Enabled by default.
{.is-info}

Controls what happens when someone posts a wrong count.

* **Enabled** - A wrong count resets the game back to `1`.
* **Disabled** - A wrong count doesn't count, but the game doesn't reset either. The same next number is still expected, and anyone can try again.

## Fail Role
An optional role that Cakey Bot automatically gives to whoever breaks the count.

# How It Works
When a member posts a correct count, Cakey Bot reacts to their message with ✅.

When a member posts an incorrect count, Cakey Bot replies explaining what happened - whether the count reset back to `1` or is continuing from where it left off - and states the server's all-time highest streak.

> The all-time highest streak is tracked permanently for your server and never decreases, even when the current count resets. It's a record of the best your server has ever done!
{.is-success}

# Related Commands
There are no slash commands for this feature - it is configured entirely through the web dashboard.
