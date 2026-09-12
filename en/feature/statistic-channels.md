---
title: Statistic Channels
description: Discord statistics display with Cakey Bot - Member count, server stats, semi-live counters. Server metrics visualization guide.
published: 1
date: 2025-11-01T06:20:13.375Z
tags: 
editor: markdown
dateCreated: 2024-12-06T05:52:28.431Z
---

# Overview
The statistic channels feature allows you to track many things relating to your server, from online members, channel count, role count, and more.

Statistic channels are locked voice channels on the side of your server that display the information in the channel name.

> Statistic channels will refresh/update once every ~20 minutes.
{.is-info}

# Setup
1. Login to our [web dashboard](https://cakey.bot/dashboard).
2. Go to "Statistic Channels".
3. Toggle/enable any statistic channels you want. (Wait up to 20 minutes for them to generate)
4. (Optional) Set custom text/name for the channels. Using `{count}` as the placeholder for the stat value/number. This custom text is limited to 75 characters.

> **Helpful Tip:** You can freely reposition the stats category and channels! Also, you can freely rename/customize the category name!
{.is-success}

# Removing/Deleting Stat Channels
In order to remove or delete a stat channel you will first need to disable/toggle the specific stat channel in the dashboard. Once you have done that, you can freely delete the channel in your server just like a normal channel.

> **Note:** If you delete the stat channel _without_ disabling it in the dashboard, it will continue to re-generate/create the channel every time the stats update.
{.is-info}

# Supported Stats
* Total Members ~ The total number of members in the server (bots & humans combined)
* Total Bots ~ Tracks how many bots are in the server
* Total Humans ~ Tracks how many Humans are in the server
<hr>

* Total Channels ~ The total number of all channel types in the server
* Text Channels ~ The total number of text channels in the server
* Voice Channels ~ The total number of voice channels made in the server
<hr>

* Total Roles ~ The total number of roles made in the server
<hr>

* Total Server Boosts ~ The total number of boosts in the server
<hr>

* Specific Role Count ~ The total number of users who have the specified role

> **Note:** You must select a role before you can enable the "Specific Role Count" stat channel.
{.is-warning}

# Custom Stat Channels
In addition to the fixed stats above, you can build your own voice channels named however you like, combining any mix of stats into a single name using [placeholders](https://wiki.cakey.bot/en/placeholders) - for example `Text: {server.counttextchannels} | VC: {server.countvoicechannels}`.

1. Login to our [web dashboard](https://cakey.bot/dashboard).
2. Go to "Statistic Channels" and find the **Custom Stat Channels** section.
3. Type a channel name using placeholders and save it.

Cakey Bot creates the channel under your stats category and keeps it updated every ~20 minutes, the same as the fixed stat channels above.

> You can have up to **10** custom stat channels per server. Each name is capped at **100 characters**, matching Discord's own channel name limit.
{.is-info}

# Stats Message
Instead of a voice channel, you can have Cakey Bot keep a single message updated in a regular text channel with whatever stats you want written into it.

1. Login to our [web dashboard](https://cakey.bot/dashboard).
2. Go to "Statistic Channels" and find the **Stats Message** section.
3. Choose a channel and write your message using [placeholders](https://wiki.cakey.bot/en/placeholders), then save.

The message is edited in place roughly every 20 minutes with the latest numbers.

> The stats message can be up to **2,000 characters** - much longer than a channel name allows, since it isn't limited by Discord's channel naming rules.
{.is-info}

> Changing the message's channel starts a fresh message in the new channel. The old message left behind in the previous channel isn't deleted automatically.
{.is-warning}

# New Placeholders
These placeholders are available for use in Custom Stat Channel names and the Stats Message:
* `{server.countbots}` - Number of bots in the server.
* `{server.counthumans}` - Number of human members in the server.
* `{server.countmembers}` - Total member count (bots and humans combined).
* `{server.countonline}` - Number of members currently online, idle, or do-not-disturb (excludes offline/invisible).
* `{server.countboosts}` - Number of server boosts.