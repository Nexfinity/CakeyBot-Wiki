---
title: Forum Auto-Unarchive
description: Keep Discord forum threads from archiving with Cakey Bot - instant unarchiving for up to 2 forum channels per server.
published: 1
date: 2026-07-26T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-07-26T00:00:00.000Z
---

# Overview
Forum Auto-Unarchive keeps threads in specific forum channels from ever staying archived. The moment Discord archives a thread in a monitored forum channel, Cakey Bot immediately un-archives it again, so the thread stays active and visible indefinitely.

This is useful for forum posts that should act more like permanent pinned topics (FAQs, rules threads, ongoing megathreads, etc.) rather than posts that naturally go quiet and archive after a period of inactivity.

> Cakey Bot needs the **`Manage Threads`** permission in the forum channel for this to work.
{.is-warning}

# Setup
1. Login to our [web dashboard](https://cakey.bot/dashboard).
2. Go to the "Forum Unarchive" page.
3. Add the forum (or media) channel(s) you want to keep permanently unarchived.
4. That's it — no further action needed. The bot handles unarchiving automatically from this point on.

> You can monitor a maximum of **2 forum channels** per server with this feature.
{.is-info}

> Only Forum and Media channel types can be selected.
{.is-info}

# How It Works
When a thread inside a monitored forum channel archives (whether from Discord's normal inactivity timer or from someone archiving it manually), Cakey Bot detects the change and immediately un-archives it, also extending the thread's auto-archive duration to the maximum (1 week) to reduce how often it needs to step in.

> This does not prevent someone from **locking** a thread, only from it staying **archived**. Locked + unarchived threads will stay visible but won't accept new messages.
{.is-info}

# Removing a Monitored Channel
To stop a forum channel from being auto-unarchived, simply remove it from the list on the "Forum Unarchive" dashboard page. Existing threads in that channel will no longer be forced to stay unarchived going forward.
