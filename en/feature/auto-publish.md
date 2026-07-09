---
title: Auto Publish
description: Automatically publish messages in Discord announcement channels with Cakey Bot. Set up auto-crossposting to push updates to all servers following your channel.
published: 1
date: 2026-07-09T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-07-09T00:00:00.000Z
---

# Overview

Cakey Bot can automatically publish (crosspost) messages in Discord Announcement channels. When enabled, any new message posted in a configured announcement channel is immediately published, pushing it out to all servers that follow that channel — without anyone needing to manually click the Publish button each time.

> Auto Publish only works in **Announcement (News) channels**. It has no effect on standard text channels.
{.is-warning}

> Cakey Bot requires the **`Manage Messages`** permission in the announcement channel to publish messages.
{.is-info}

# Setup

Auto Publish channels can be configured in two ways:

## Via the Web Dashboard
1. Log in to the [web dashboard](https://cakey.bot/dashboard).
2. Go to **Auto Publish**.
3. Select an announcement channel from the dropdown and click **Add**.

To remove a channel, click the delete button next to it in the list.

## Via Slash Command
Run `/setup toggle-autopublish` inside the announcement channel you want to enable or disable. Running the command again in the same channel will toggle it off.

> `/setup toggle-autopublish` requires the **Manage Server** permission.
{.is-info}

# Behaviour & Limits

- Every new message posted in an enabled announcement channel is automatically published.
- **Polls and forwarded messages are skipped** — Discord does not support crossposting these message types.
- Discord enforces a rate limit on how often messages in a single channel can be published. If the rate limit is hit, Cakey Bot will automatically pause publishing for that channel until the limit expires, then resume publishing new messages normally.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /setup toggle-autopublish | Enables or disables auto publish in the current announcement channel. | N/A | Manage Server |
