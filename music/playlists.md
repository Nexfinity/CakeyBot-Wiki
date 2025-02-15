---
title: Music Playlists
description: 
published: 1
date: 2024-12-04T06:06:35.892Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:02:54.523Z
---

# Overview

> Playlists must have 50 songs or less to be added to the queue and can not exceed the max queue size of 50 songs. ([Premium](https://cakey.bot/premium.php) users are excluded from this limit)
{.is-warning}

# Load Playlists

Cakey Bot can automatically load entire playlists of songs from Soundcloud, Spotify, and Bandcamp. When you use a playlist URL instead of a song name, every song in the playlist will be added to the queue.

# Create/Load Custom Cakey Bot Playlists

Cakey Bot also has its own built-in playlist system.

## Creating a Custom Playlist

If you already have songs added to the queue you can save them with the `/playlist create <name>` command and it'll create a new playlist for you. You can also use the `/playlist add <name>` command to add more songs to an existing playlist.

## Loading a Custom Playlist

If you want to load them back into the queue at a later date you can simply run `/playlist load <name>`.&#x20;

## Deleting a Custom Playlist

You are also able to delete playlists with the `/playlist delete <name>` command.&#x20;

## Listing All Custom Playlists

If you want to see a list of all of your playlists and the number of songs in each playlist you can run the `/playlist list` command.

> A remarkable feature of using Cakey Bot's custom playlist system is that you don't have to navigate to external websites to use it AND your playlist can contain songs from multiple different sources (YouTube, Twitch, Spotify, Bandcamp, etc).
{.is-success}

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /playlist | Creates, deletes or loads a custom music playlist. (Use !play for youtube/spotify playlists) | \<create \| load \| delete> \<name> | None | 
| /playlist list | List all of your currently saved playlists. | N/A | None | 
| /playlist rename | Renames the selected playlist. | \<name> \<newName> | None | 