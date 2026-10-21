---
title: Song Request Channel
description: Discord song request channel with Cakey Bot - Dedicated music commands channel, queue management. Music bot channel setup guide.
published: 1
date: 2026-10-21T12:00:00.000Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:08:52.952Z
---

# Overview

> This feature requires slightly more setup to enable. To add this feature to your discord you must have **`Manage Server`** permissions. Also note that Cakey Bot requires the following permissions as well: **`Create Channels`**, **`Manage Messages`**
{.is-warning}

# Setup

In order to set up this feature you must have **`Manage Server`** permissions. You can then run the `/setup songrequest` command in any channel that Cakey Bot has access to read/view messages in. If you and Cakey Bot both have the required permissions, a new channel called _`#cakey_songrequests`_ will have been created.&#x20;

In this new channel, you will see a fancy embed with 5 buttons added to it and a block of text with more information above it. Do NOT delete this message. If you do, you will need to delete the channel and run the setup again.

![Song Request Embed](/song_request.png)

> You can freely rename and move the song request channel into other categories after it's created without any issues as Cakey Bot uses the channel ID to update the messages.
{.is-success}

# Removal
You can also use the `/setup songrequest-disable` command to disable the song request channel. This will NOT delete the channel OR the embed. This will simply prevent the bot from listening for song requests in the channel. To re-enable the feature you will need to run the `/setup songrequest` command again. 

> Note: Running the setup command again after disabling the channel will create a NEW channel. It will not re-enable the old channel.
{.is-info}
 
# Usage

The song request channel is very simple to use. In order to use it, you (or whoever is attempting to use it) must be in a voice channel that Cakey Bot can view/join. Once you are in a voice channel, you can either post a song name or a URL/Link to a valid music source and Cakey Bot will automatically search for and add the song to the queue. When it has done so, it will also update the embed picture/content. As you add/remove items to/from the queue, the queue message under the embed will also update.

> You don't have to use the _`#cakey_songrequests`_ channel in order to make use of the embed system! As long as you have the embed/song request channel setup, it will always update with the current song/queue info regardless if you use the channel or if you use regular commands.
{.is-info}

# Additional Music Bots
<span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>

Each of the [additional music bots](/en/music/basic-usage#multiple-music-bots) (Cakey Bot 2 to Cakey Bot 6) can have its own song request channel. Set them up on the dashboard's **Music** page under **Music Bot Request Channels** by picking a channel for each bot that is in your server. The bot posts its player message in that channel within a minute of saving.

The additional music bots can't read messages, so typing a song in their channel does nothing. Members add songs with the **Add Song** button on the player message instead, which asks for a song name or link. It's best to stop members from sending messages in these channels.

Removing a bot's channel on the dashboard stops it using that channel, but leaves the channel and the player message where they are.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /setup songrequest | Creates and configures the song request channel. | N/A | ManageServer or Administrator | 
| /setup songrequest-disable | Disables the song request channel. (If one is set) | N/A | ManageServer or Administrator | 