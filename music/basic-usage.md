---
title: Basic Usage
description: Play music in Discord with Cakey Bot - Basic commands, queue management, volume control. Music bot beginner's guide.
published: 1
date: 2025-12-13T03:30:08.626Z
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

# Configuration
| Name               | Description                                                                                                                                                                                                         | Default Value | Min Value | Max Value | Premium Feature |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|-----------|-----------|-----------------|
| Title Blacklist    | A list of words/phrases that are blocked from appearing in song titles. Used to filter inappropriate or abusive content.                                                                                           | Empty         | —         | —         | No              |
| Default Volume     | Controls the initial playback volume of the bot. Resets to this value when the queue ends or new playback begins.                                                                                                  | 50            | 0         | 100       | No              |
| 24/7 Music         | Keeps the bot in a voice channel continuously, even when not actively playing music.                                                                                                                               | Disabled      | —         | —         | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>             |
| Vote Skipping      | Enables vote-based skipping of currently playing songs.                                                                                                                     | False         | —         | —         | No              |
| Max Song Length    | Restricts the maximum allowed duration of a song in the queue (in minutes).                                                                                                  | 10            | 1         | 180       | No              |

# Multiple Music Bots

Cakey Bot has additional bots that you can invite that are designed specifically for music playback! You can find the invites to these bots on our "Premium" page of the [web dashboard](https://cakey.bot/dashboard/public). Note that you must have premium enabled on the server in order to invite these additional music bots.

# Supported Sources

Cakey Bot supports many different sources including Spotify, Bandcamp, Twitch and more!

You can view all of our current and planned music sources on [this page](https://wiki.cakey.bot/en/music/supported-sources).

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command         | Description                                                | Usage                            | Permission           |
| :-------------- | :--------------------------------------------------------- | :--------------------------------| :------------------- |
| /clearqueue     | Clears all tracks from the queue.                          | N/A                              | Server Mod/DJ        |
| /disconnect     | Makes the bot leave your voice channel.                    | N/A                              | None                 |
| /jumpto         | Jumps to a specific song in the queue.                     | \<song id>                        | None                 |
| /loop           | Makes the current song loop until it's toggled off.        | N/A                              | None                 |
| /lyrics         | Displays the lyrics for the song searched if any are available. | \<query>                        | None                 |
| /nowplaying     | Displays the current song being played.                    | N/A                              | None                 |
| /pause          | Pauses the current song.                                  | N/A                              | None                 |
| /play           | Starts playing music with the given query.                 | \<query>                          | None                 |
| /playfile       | Starts playing the uploaded music file.                    | \<query>                          | None                 |
| /playlist       | Creates, deletes or loads a custom music playlist. (Use !play for youtube/spotify playlists) | \<create \| load \| delete> \<name> | None |
| /playlist list  | List all of your currently saved playlists.                | N/A                              | None                 |
| /playlist rename| Renames the selected playlist.                             | \<name> \<newName>                 | None                 |
| /queue          | Displays the current music queue.                          | N/A                              | None                 |
| /restart        | Goes to the start of the current song.                     | N/A                              | None                 |
| /resume         | Resumes the current song.                                  | N/A                              | None                 |
| /seek           | Seeks to a specific position or moves forward/backward in the current song.               | \<time>                           | None                 |
| /shuffle        | Shuffles the current song queue randomly.                  | N/A                              | None                 |
| /skip           | Votes to skip the current song.                            | [count]                          | None                 |
| /volume         | Changes the bot's volume.                                  | \<volume>                         | None                 |
