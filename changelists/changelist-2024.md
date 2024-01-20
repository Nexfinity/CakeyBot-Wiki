---
title: Changelist 2024
description: 
published: 1
date: 2024-01-20T05:32:43.716Z
tags: 
editor: markdown
dateCreated: 2024-01-02T23:52:26.127Z
---

# January 19th - Minecraft Command Category
## Fixed
* Fixed an issue where "Total Channels" on the `/stats` command was incorrect

## Changed
* Grouped `/query` command into `/minecraft query` command
* Grouped `/mcskin` command into `/minecraft skin` command

# January 16th - Achievement Commands
## Added
* Added the accompanying commands for Cakey's achievement system: 
  * `/achievements info <achievement>` - View information about a specific achievement
  * `/achievements list` - View a list of all achievements for this server.
  * `/achievements view [user]` - View the selected users progress towards achievements.

# January 10th - $N Fix & Join DMs
## Fixed
* Fixed an issue where $N was applied to the message response, not the initial message

## Added
* Added the ability to send join & leave announcements as a DM to the user.

# January 5th - Ban Sync
## Added
* Added ban sync. Now you can create pools of guilds; a ban in a server will be replicated to all servers it has a common pool with. 

# January 4th - Generic RSS Feeds & Music Fixes
## Fixed
* Auto-disconnect for music players has been fixed when the voice channel is empty.

## Added
* Added support for generic RSS feeds. Currently we support:
  * Atom feeds
  * RSS 2.0 feeds
* Music players will now be automatically paused and resumed depending on whether users are in the voice channel.

# January 3rd - Achievements
## Added
* Added a new major feature called Achievements!

# January 2nd - Auto Publish
## Added
* Added Auto Publisher for announcement channels