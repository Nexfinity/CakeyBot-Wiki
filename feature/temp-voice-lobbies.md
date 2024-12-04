---
title: Temp Voice Lobbies
description: 
published: 1
date: 2024-12-04T03:34:40.314Z
tags: 
editor: markdown
dateCreated: 2024-09-03T02:47:56.721Z
---

# Overview
The Temporary Voice Lobby feature provides server owners with a dynamic and flexible voice channel system that automatically creates and manages voice channels for users. This feature is perfect for servers that want to offer personalized voice experiences without cluttering the server with too many static channels.

## Key Features
* **Lobby Channel:** Server owners can create a designated "Lobby" voice channel. This acts as a hub for users who want to generate their own temporary voice channels.

* **Automatic Channel Creation:** When a user joins the lobby, the bot will automatically create a new voice channel for that user. This new channel is exclusive to the user and is used as their personal space.

* **User Channel Management:** The user who joined the lobby will have management permissions over their temporary voice channel. This allows them to:
  * Rename the channel
  * Adjust permissions (who can join or speak)
  * Set user limits for the channel
  * Disconnect unwanted users
  * Toggle the privacy of the channel
  * Delete the channel
 
* **Automatic Deletion:** Once all users have left the temporary voice channel, it will be automatically deleted by the bot, keeping the server clean and organized without any manual intervention.

# Setup
> You will need **`Manage Server`** or **`Administrator`** permission to set up this feature.
{.is-warning}

Admins can easily set up and manage the Temporary Voice Lobby feature using a set of simple commands. Follow these instructions to configure and control the lobby and temporary voice channels.

## Creating the Lobby
To create the Lobby voice channel and its associated category, use the following command: `/temp-voice admin create-lobby`.

This will create a Lobby channel and a new category to house the temporary voice channels. 
> Both the Lobby and Category channels can be freely renamed after creation without affecting functionality.

## Removing the Lobby
If you want to disable the temporary voice feature and remove all related channels, you can use: `/temp-voice admin clear-lobby`.

This will delete the Lobby channel, the category, and any existing temporary voice channels that were created by the bot.

## Managing temporary voice channels
If needed, admins can forcefully delete any user's temporary voice channel without waiting for it to auto-delete by running: `/temp-voice admin force-delete <channel>`.

This command gives admins control over manual removal of temporary channels.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| / | TBD | N/A | None | 