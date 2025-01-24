---
title: Statistic Channels
description: 
published: 1
date: 2025-01-01T19:15:35.011Z
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
1. Login to our [web dashboard](https://cakey.bot/dashboard/).
2. Go to "Statistic Channels" [here](https://cakey.bot/dashboard/public/statistic-channels).
3. Toggle/enable any statistic channels you want. (Wait up to 20 minutes for them to generate)
4. (Optional) Set custom text/name for the channels. Using `{count}` as the placeholder for the stat value/number.

> **Helpful Tip:** You can freely reposition the stats category and channels! Also, you can freely rename/customize the category name!
{.is-success}

# Removing/Deleting Stat Channels
In order to remove or delete a stat channel you will first need to disable/toggle the specific stat channel in the dashboard. Once you have done that, you can freely delete the channel in your server just like a normal channel.

> **Note:** If you delete the stat channel _without_ disabling it in the dashboard, it will continue to re-generate/create the channel every time the stats update.
{.is-info}

# Supported Stats
* Total Members ~ The total number of members in the server
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