---
title: Starboard
description: Create Discord starboard with Cakey Bot - Pin popular messages automatically, showcase best content. Community feature guide.
published: 1
date: 2025-11-01T06:20:12.164Z
tags: 
editor: markdown
dateCreated: 2023-06-12T02:59:49.416Z
---

# Overview
The Starboard feature in Cakey Bot is a functionality designed for Discord servers that allows users to highlight and showcase notable or popular messages within a dedicated channel known as the starboard. It provides a way to recognize and preserve memorable messages that receive a certain level of appreciation from the community.

The Starboard feature in Cakey Bot can be a fun and engaging way to recognize and highlight valuable contributions or entertaining messages within a Discord community. By allowing users to easily star messages and providing a dedicated channel to showcase them, it encourages interaction and appreciation among server members.

# How to Setup Starboard
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard) and select your server.
2. From the left sidebar, pick "Starboard".
![starboard_1.png](/starboard/starboard_1.png)
3. After that, click "Enable Starboard" and "Update".
<image src="/starboard/starboard_2.png" width="800px" alt="Enabled Screenshot">

**Done!** Starboard is now enabled in your server. Remember to set a starboard channel for messages to appear when they are stared.

## Settings
### Min. Emote Required
Min. Emote Required means how many reactions the message needs to have until is gets put on the starboard. Defaults to **2** reactions, and the dashboard enforces a minimum of **1**.
Here's how to change it:
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard) and select your server.
2. From the left sidebar, pick "Starboard".
3. After that, under the "Min. Emote Required" section, enter the amount of reactions a message needs to get to show up on the starboard.
<image src="/starboard/starboard_3.png" width="800px" alt="Min. Emote Screenshot">
### Ignored Channels
You can specify channels, categories, and threads to ignore entirely — messages starred in these locations will never be added to the starboard.
Here's how to set it up:
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard) and select your server.
2. From the left sidebar, pick "Starboard".
3. After that, under the "Ignored Channels" section, select the channels, categories, or threads you would like to exclude from the starboard.
### Max Message Age (Days)
You can set a maximum message age, in days. Messages older than this will be skipped and will not be added to the starboard even if they receive enough reactions.
Here's how to set it up:
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard) and select your server.
2. From the left sidebar, pick "Starboard".
3. After that, under the "Max Message Age (Days)" section, enter the maximum age (in days) a message can be before it's no longer eligible for the starboard.
### Enable Self-Star
Controls whether users are allowed to star their own messages.
> If this setting is disabled, Cakey Bot will automatically remove a user's star reaction from their own message rather than simply ignoring it.
{.is-info}

Here's how to set it up:
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard) and select your server.
2. From the left sidebar, pick "Starboard".
3. After that, toggle the "Enable Self-Star" setting on or off depending on whether you want users to be able to star their own messages.
### Starboard Channel
The starboard channel is where the stared messages will show up. Here's a guide on how to set it up:
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard) and select your server.
2. From the left sidebar, pick "Starboard".
3. After that, under the "Starboard Channel" section, select the correct channel that you would like your stared messages to appear.
<image src="/starboard/starboard_4.png" width="800px" alt="Channel Screenshot">
### Custom Star Emote
You can set a custom star emote so that members do not have to react with a `⭐`, but a custom emoji.
Here's how to do that:
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard) and select your server.
2. From the left sidebar, pick "Starboard".
3. After that, under the "Custom Star Emote" section, select the emote you would like people in your server to react with.
<image src="/starboard/starboard_5.png" width="800px" alt="Emote Screenshot">