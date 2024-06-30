---
title: Song Request Channel
description: 
published: 1
date: 2024-06-30T23:12:05.575Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:08:52.952Z
---

# Overview

> This feature requires slightly more setup to enable. To add this feature to your discord you must have **`Manage Server`** permissions. Also note that Cakey Bot requires the following permissions as well: **`Create Channels`**, **`Add Reactions`**, **`Manage Messages`**
{.is-warning}

# Setup

In order to set up this feature you must have **`Manage Server`** permissions. You can then run the `/setup songrequest` command in any channel that Cakey Bot has access to read/view messages in. If you and Cakey Bot both have the required permissions, a new channel called _`#cakey_songrequests`_ will have been created.&#x20;

In this new channel, you will see a fancy embed with 6 buttons added to it and a block of text with more information above it. Do NOT delete this message. If you do, you will need to delete the channel and run the setup again.

![](/song_request.png)

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