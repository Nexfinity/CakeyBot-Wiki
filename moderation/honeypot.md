---
title: Honeypot
description: Automatically punish users who post in a designated trap channel with Cakey Bot's Honeypot feature.
published: 1
date: 2026-06-07T18:25:31.619Z
tags: 
editor: markdown
dateCreated: 2026-06-07T18:14:17.602Z
---

> This feature is currently in **beta**. Behaviour may change without notice.
{.is-warning}

# Overview
The Honeypot feature lets you designate a channel as a trap. Cakey Bot will automatically post a visible warning embed in the channel, alerting users that posting there will result in punishment. Any user who sends a message in the honeypot channel regardless of content is immediately punished with the action you have configured.

This is useful for catching spam bots, self-bots, or phishing accounts who ignore channel warnings. This can act as an early-detection layer on top of your existing moderation setup.

# How It Works
1. You select a channel as the honeypot and choose a punishment type.
2. Cakey Bot sends a warning embed into that channel so users are aware it is a trap.
3. If any user sends a message in the channel, Cakey Bot applies the configured punishment automatically.
4. If a log channel is configured, Cakey Bot posts a record of who was punished and when.

When you change the honeypot channel, the old warning embed is removed and a new one is posted in the newly selected channel. Clearing the channel disables the feature and removes the embed.

# Setup
Navigate to **Dashboard → Honeypot** for your server.

## Honeypot Channel
Select the text channel to designate as the trap. Once saved, Cakey Bot will immediately post a warning message in that channel. Any user who sends a message there will be automatically punished.

Set this to **None** to disable the honeypot entirely. The warning embed will be removed from the previously configured channel.

## Punishment
The action Cakey Bot takes against any user who sends a message in the honeypot channel. Available options:

| Punishment | Description |
|------------|-------------|
| **Timeout** | Temporarily mutes the user in the server. |
| **Kick** | Removes the user from the server. They can rejoin with a valid invite. |
| **Softban** | Bans then immediately unbans the user, deleting their recent messages without permanently barring re-entry. |
| **Ban** | Permanently bans the user from the server. |

The default punishment is **Softban**.

> **Note:** All punishment types will also delete the offending message from the honeypot channel. The softban & ban types will remove the emssage from ALL affected channels.
{.is-info}

## Log Channel
An optional channel where Cakey Bot posts a log entry each time the honeypot is triggered. The log entry will include details about the user who was caught. Leave this unset to disable logging.