---
title: Temp Voice Lobbies
description: 
published: 1
date: 2024-09-13T05:10:44.356Z
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

# Configuring