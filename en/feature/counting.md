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

### Fail Role Duration
An optional amount of time (in minutes) the fail role stays assigned before Cakey Bot automatically removes it again.

* Leave this empty or set it to `0` to make the fail role assignment **permanent** - it will not be removed automatically.
* Otherwise, Cakey Bot removes the role after the configured number of minutes elapses, up to a maximum of `43200` minutes (30 days).

## Ignored Roles
An optional list of roles (you can select more than one) that fully exclude members from the counting game. A member is ignored if they hold **any** of the configured roles.

Members with an Ignored Role:
* Cannot contribute a valid count - even if they post the correct next number, it will not be accepted.
* Cannot break/reset the count by posting invalid text.
* Have any message they send in the counting channel **silently deleted** instead. There's no reply, reaction, or streak reset - the message is simply removed as if it never happened.

This is useful for excluding moderators, bots, or other accounts that regularly post in the counting channel from affecting the game.

## Custom Failure Message & Embed
By default, Cakey Bot replies with a built-in failure message when someone breaks the count. You can override this with your own text and/or embed instead.

* **Custom Failure Message** - Plain text sent instead of the default failure message. Supports the same [placeholders](https://wiki.cakey.bot/en/placeholders) used elsewhere on the dashboard (e.g. `{user.mention}`, `{server.name}`).
* **Custom Failure Embed** - A saved embed (built with the dashboard's embed editor) sent instead of the default failure message.
  > Custom Failure Embed is a **premium** feature. Non-premium servers can still set a custom plain-text message, but the embed picker is disabled.
  {.is-warning}

If both are left empty, Cakey Bot falls back to its default failure message. If a Custom Failure Embed was previously set but your server's premium subscription has since ended, Cakey Bot falls back to the Custom Failure Message (or the default message if that's empty too) until premium is restored.

## Reset Current Count
A "Reset Count" button on the dashboard immediately resets the current count back to `0` - the same reset that happens when someone breaks the count - without needing anyone to actually post an invalid message in Discord.

> This only resets the current count and current counter. The all-time highest streak is never affected.
{.is-info}

# How It Works
When a member posts a correct count, Cakey Bot reacts to their message with ✅.

When a member posts an incorrect count, Cakey Bot replies explaining what happened - whether the count reset back to `1` or is continuing from where it left off - and states the server's all-time highest streak.

> The all-time highest streak is tracked permanently for your server and never decreases, even when the current count resets. It's a record of the best your server has ever done!
{.is-success}

# Related Commands
There are no slash commands for this feature - it is configured entirely through the web dashboard.
