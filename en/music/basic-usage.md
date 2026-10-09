---
title: Basic Usage
description: Play music in Discord with Cakey Bot - Basic commands, queue management, volume control. Music bot beginner's guide.
published: 1
date: 2026-10-08T12:00:00.000Z
tags: music
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

If no song is currently playing when you add one, it will start to play instantly. If a song is currently playing, your song will be added to a queue that will play through automatically.

> If you play a live stream, other songs in the queue will not be played until either the live stream ends or until someone skips the live stream.
{.is-info}

# Requirements

Cakey Bot requires at least **`Connect`** and **`Speak`** permissions to function. You will also need to be in a voice channel to summon Cakey Bot to it. If Cakey Bot is currently being used by users in another channel you will not be able to summon it to your channel. Many commands in Cakey Bot excluding `/disconnect` require a song to be playing in order to be used. If a song is not playing an error message will be displayed. Some commands can not be used while a live stream is playing, to use these commands you will have to wait until the live stream ends or skip the live stream.

# Configuration
| Name               | Description                                                                                                                                                                                                         | Default Value | Min Value | Max Value | Premium Feature |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|-----------|-----------|-----------------|
| Title Blacklist    | A list of words/phrases that are blocked from appearing in song titles. Used to filter inappropriate or abusive content. Limited to 2,000 characters.                                                             | Empty         | —         | —         | No              |
| Default Volume     | Controls the initial playback volume of the bot. Resets to this value when the queue ends or new playback begins.                                                                                                  | 50            | 0         | 100       | No              |
| 24/7 Music         | Keeps the bot in a voice channel continuously, even when not actively playing music.                                                                                                                               | Disabled      | —         | —         | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>             |
| Vote Skipping      | Enables vote-based skipping of currently playing songs.                                                                                                                     | False         | —         | —         | No              |
| Max Song Length    | Restricts the maximum allowed duration of a song in the queue (in minutes).                                                                                                  | -1            | -1        | 1440      | No              |
| Autoplay           | When the queue runs out, adds songs similar to the last one so the music keeps going.                                                                                        | Disabled      | N/A       | N/A       | No              |
| Private Responses  | Music command replies are only shown to the member who used the command.                                                                                                     | Disabled      | N/A       | N/A       | No              |
| Music Log Channel  | A channel where the bot posts a short line for each song played and each change made to the player.                                                                          | None          | N/A       | N/A       | No              |

> A Max Song Length of `-1` means unlimited song length.
{.is-info}

# Autoplay
With autoplay on, Cakey Bot adds a song similar to the last one whenever the queue runs out, so the music keeps going without anyone queueing more. It only does this while somebody is listening, and it avoids songs it has played recently.

Autoplay can be turned on and off from the Music page of the [web dashboard](https://cakey.bot/dashboard), with the Autoplay button on `/nowplaying`, or with the Autoplay button on the [song request channel](/en/music/song-request-channel) message. Songs you queue yourself always play before anything autoplay adds.

# Music Log Channel
When a Music Log Channel is set on the Music page of the [web dashboard](https://cakey.bot/dashboard), Cakey Bot posts a short line there whenever a song starts playing, a song is added to the queue, autoplay picks a song, or a member changes the player, for example by skipping, pausing or changing the volume. Each line names the member or says the song came from autoplay.

The bot sends at most one message per second for each server. Lines that come in during that second are combined into the next message.

# Restarts and Reconnects
Cakey Bot remembers each server's player: the queue, the song that was playing and how far into it, the volume, the loop setting and whether autoplay was on. After a bot restart or a reconnect it rejoins the voice channel and carries on from where it was.

> A player is only brought back if it was playing within the last 30 minutes. One that was stopped with `/disconnect`, finished its queue, or was left alone in its channel is not brought back.
{.is-info}

> The `/volume` command's `volume` parameter accepts a range of **1-200%** and only changes the volume of the current playback session. To update the persistent Default Volume setting above instead, use the command's separate `default-volume` parameter (**0-100**, matching the dashboard's range) — this can be set with or without also changing the live `volume`, and doesn't require a song to be currently playing.
{.is-info}

> The `/play` command's queue is capped at **50 songs** for non-Premium servers. Members with [Cakey Personal](/en/feature/cakey-personal) have no queue limit (up to 5,000 songs) in any server.
{.is-info}

# Multiple Music Bots

Cakey Bot has additional bots that you can invite that are designed specifically for music playback! You can find the invites to these bots on our "Premium" page of the [web dashboard](https://cakey.bot/dashboard). Note that you must have premium enabled on the server in order to invite these additional music bots.

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
| /playlist add   | Adds the current queue's songs to an existing playlist.    | \<name>                          | None                 |
| /playlist list  | List all of your currently saved playlists.                | N/A                              | None                 |
| /playlist rename| Renames the selected playlist.                             | \<name> \<newName>                 | None                 |
| /queue          | Displays the current music queue.                          | N/A                              | None                 |
| /radio          | Plays a live online radio station.                          | \<query>                          | None                 |
| /restart        | Goes to the start of the current song.                     | N/A                              | None                 |
| /resume         | Resumes the current song.                                  | N/A                              | None                 |
| /seek           | Seeks to a specific position or moves forward/backward in the current song.               | \<time>                           | None                 |
| /shuffle        | Shuffles the current song queue randomly.                  | N/A                              | None                 |
| /skip           | Votes to skip the current song.                            | [count]                          | None                 |
| /volume         | Changes the bot's volume. (1-200%)                          | [volume] [default-volume]         | None                 |
