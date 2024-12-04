---
title: Basic Usage
description: 
published: 1
date: 2024-12-04T03:35:38.903Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:01:58.307Z
---

# Basic Usage

> In order to use music Cakey Bot will need **`Connect`** and **`Speak`** permissions for any voice channels you want to listen to music in.
{.is-warning}

# Overview

Cakey Bot can play music from multiple sources which you can view a full list of [here](https://wiki.cakey.bot/en/music/supported-sources). In order to listen to music you will need to follow the steps below.

1. Join a voice channel that Cakey bot has access to join/speak in
2. Type `/play <song>` (The `/play` command will auto-summon Cakey Bot)
   1. You can also use the `/move` command if no one else is using the bot
3. If you typed !join or !move in step two you will now need to type !play \<song> in order to start playing a song

If no song is currently playing when you add one, it will start to play instantly. If a song is currently playing, your song will be added to a queue that will play through automatically.

> If you play a live stream, other songs in the queue will not be played until either the live stream ends or until someone skips the live stream.
{.is-info}

# Requirements

Cakey Bot requires at least **`Connect`** and **`Speak`** permissions to function. You will also need to be in a voice channel to summon Cakey Bot to it. If Cakey Bot is currently being used by users in another channel you will not be able to summon it to your channel. Many commands in Cakey Bot excluding `/dc` require a song to be playing in order to be used. If a song is not playing an error message will be displayed. Some commands can not be used while a live stream is playing, to use these commands you will have to wait until the live stream ends or skip the live stream.

# Title Blacklist

Cakey Bot also supports blacklisting specific words and phrases from song titles. This can be useful to discourage or prevent users from enqueueing abusing music (such as ear rape or inappropriate content). You can configure this list on the [web dashboard](https://cakey.bot/dashboard/public) on the Music page.

# Default Volume

By default, Cakey Bot's volume will be set to 50 when playing music. You can change the volume using the `/volume <amount>` command but the volume will revert to 50 if the queue runs out of songs or the next time you use Cakey Bot. You can however change the default volume on our [web dashboard](https://cakey.bot/dashboard/public/) from 50 to any number between 0 and 100.

# Multiple Music Bots

Cakey Bot has additional bots that you can invite that are designed specifically for music playback! You can find the invites to these bots on our premium page [here](https://cakey.bot/dashboard/public/premium). Note that you must have premium enabled on the server in order to invite these additional music bots.

# 24/7 Music <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>
Cakey Bot has the ability to play music 24/7 and never leave a voice channel (except during bot restarts). You can enable this feature by toggling the "24/7 music" switch on the [Web Dashboard](https://cakey.bot/dashboard/public) on the Music page.

# Supported Sources

Cakey Bot supports many different sources including Spotify, Bandcamp, Twitch and more!

You can view all of our current and planned music sources on [this page](https://wiki.cakey.bot/en/music/supported-sources).

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| / | TBD | N/A | None | 