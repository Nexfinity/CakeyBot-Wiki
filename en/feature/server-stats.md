---
title: Server Statistics
description: Discord server activity statistics with Cakey Bot - Message and voice activity per member and channel, charts, busiest hours, activity roles and live counter channels.
published: 1
date: 2026-09-18T12:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-09-18T12:00:00.000Z
---

# Overview
Server statistics records how many messages each member sends in each channel and how long they spend in voice, and turns that into charts, rankings, a busiest hours heatmap, activity based roles and live numbers for counter channels.

Only counts are stored, never message content. Members can opt out of being counted individually everywhere with `/serverstats privacy`; their activity still adds up in the server and channel totals but cannot be traced back to them.

> Free servers can look back up to **7 days**, premium servers up to **30 days**.
{.is-info}

# Setup
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard) and select your server.
2. From the left sidebar, pick "Server Stats".
3. Open the "Tracking settings" tab and enable tracking. Activity is recorded from that moment on.

# Dashboard Tabs
Every tab follows the range picked at the top: the last 24 hours, 7 days or 30 days. The raw counts for the range can be downloaded as CSV.

* **At a glance** ~ Messages sent, hours in voice, active members, member count, joins and leaves, with message and voice charts over time.
* **Message activity** ~ Messages by channel over time, and the busiest channels and members.
* **Voice activity** ~ Voice time by channel over time, and the channels and members with the most voice time.
* **Members and growth** ~ Member count over time with joins and leaves per day.
* **Busiest hours** ~ A heatmap of which hours of which weekdays the server is busiest, in UTC.
* **Activity roles** ~ Roles handed out automatically from activity, see below.
* **Counter channels** ~ The placeholders that put live activity numbers into statistic channel names and the stats message.
* **Tracking settings** ~ Enable tracking, whether bots count, whether muted or deafened voice time and the AFK channel count, excluded channels, roles and members, and resetting one member or the whole server.

# Activity Roles
A rule gives a role to the members whose activity matches it and removes it again when it no longer does. Each rule sets:

* The role to hand out.
* What is counted: message count or voice time.
* How members are picked: everybody past a number, or only the highest placed.
* The number to reach, or how many members to pick.
* How many days of activity to look at.

The rules are worked out every 30 minutes at most; the interval is configurable.

# Counter Channels and the Stats Message
[Statistic channel](/en/feature/statistic-channels) names and the stats message accept activity placeholders alongside the usual server placeholders, so one name can read `Messages this week: 1,204 | Top: Sylveon`. See the [server statistics placeholders](/en/placeholders#server-statistics) for the list; each one takes an optional day window such as `{messages:7d}`.

# Related Commands
Every command takes an optional range of a day, a week or a month. A month is premium only.

Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /serverstats server | How active the server has been. | [range] | None |
| /serverstats me | Your own activity. | [range] | None |
| /serverstats user | A member's activity. | \<user> [range] | None |
| /serverstats channel | A channel's activity. | \<channel> [range] | None |
| /serverstats top | The most active members or channels by messages or voice. | [kind] [range] | None |
| /serverstats chart | A chart of messages, voice or member growth. | [kind] [range] | None |
| /serverstats privacy | Opts you in or out of per member statistics in every server. | N/A | None |