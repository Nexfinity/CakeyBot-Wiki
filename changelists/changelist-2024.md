---
title: Changelist 2024
description: 
published: 1
date: 2024-03-04T15:38:00.558Z
tags: 
editor: markdown
dateCreated: 2024-01-02T23:52:26.127Z
---

# March 4th - Role XP Multipliers
## Added
* Added the ability to create up to 5 role multipliers for leveling XP. 

# March 2nd - Locale Updates
## Fixed
* Fixed several misc. bugs.

## Changed
* Russian, Portuguese Brazilian, and German translations updated for bot and website.

# February 29th - 1v1 Economy Gambling
## Fixed
* Fixed the `/tempban` and `/role temporary` commands.

## Added
* Added new `/eco rock-paper-scissors <amount>` command -	Challenge another user to Rock, Paper, Scissors.
* Added new `/eco split-or-steal`	command - Challenge another user to split or steal.

# February 28th - Economy Gambling
## Added
* Added new `/eco guess` command - Guess the number (1-10) for a chance to double your money.
* Added new `/eco coinflip` command - Guess the result to win 50% more money.

# February 27th - Economy Balancing
## Fixed
* Fixed an issue where message deleted audit log events were not firing correctly
* Fixed an issue where rate limit time messages would display an incorrect timer when running multiple rate limited commands back to back.

## Changed
* Dropped cooldown on the `/eco work` command. (30Min => 15Min)
* Adjusted `/eco rob` to cap based on a percentage of target user's balance instead of hard coded numbers. (Allows dynamic scaling for larger balances)
* Modified profit values for the `/eco work` and `/eco beg` commands.

# February 24th - Bug Fix + Free /eqpreset
## Changed
* Updated `/playlist create` so it now includes the currently playing song in addition to any items in the queue itself.
* The `/eqpreset` command is now available to non-premium servers.

# February 22nd - Anti-Raid Released
## Added
* Released new Anti-Raid feature!

# February 21st - Multiple Category Channels
## Changed
* Updated Auto Mod's Category Channels to allow multiple channel selections instead of just one.

## Added
* Added sever more new `/rank` card background banner images for premium servers.

# February 20th - Premium Join/Leave Banners
## Added
* Added two new join and leave background images for premium servers.

# February 19th - Premium /rank Image Banners
## Fixed
* Fixed an issue with the `/selfrole embed` command.
## Added
* Added several new `/rank` card background banner images for premium servers.

# February 18th - Misc. Bug Fixes
## Fixed
* Fixed an issue where Twitch social feeds were not updating correctly.
* Fixed an issue where `/birthday next` didn't sort birthdays correctly due to the year they were set to.

# February 15th - Multiple Auto Roles
## Changed
* Updated "Bulk Update" settings for audit log so each setting applies separately instead of bulk applying all of them.

## Added
* Added the ability to select multiple auto roles.

# February 13th - Bulk Role Management
## Changed
* Invalid Twitch feeds are not automatically removed.
* Auto Quoter is now enabled by default for new servers.

## Added
* Added new `/role bulkadd <role> <roleToAdd>` command.
* Added new `/role bulkremove <role> <roleToRemove>` command.

# February 12th - Reaction Placeholder
## Added
* Added new `{reactoriginal:}` placeholder. This allows auto responders to add reactions to the original message.

# February 6th - QOL
## Added
* Added support for importing XP/level data from Amari Bot using `/setup import` (Already supports importing from MEE6)
* Added the ability for users to leave giveaways by clicking the button again.

# January 29th - Premium Adjustments & Reminder QOL
## Changed
* Changed `/reminder <time> <message>` to `/reminder create <time> <message>`
* Removed premium requirements for `{dm}` & `{reaction}` placeholders
* Updated boost announcements to no longer be premium locked
* Auto responders are now limited to 250 responders for free servers. (Still unlimited for premium)
* `/imagine` command limits adjusted. (5 for free servers, 100 for premium servers)

## Added
* Added new `/reminder list` command
* Added new `/reminder delete <reminder>` command

## Removed
* Removed `/perms` command

# January 28th - Job Scheduler Fix
## Fixed
* Fixed an issue that caused `/reminder`, `/tempban` and birthdays to not correctly trigger after a bot restart.

# January 27th - Auto Quoter QOL
## Changed
* Auto Quoter feature will now allow quoting messages across channels within the same server

# January 26th - Music Improvements & Fixes
## Fixed
* Fixed international Spotify playlist URLs not loading all songs in the playlist
* Fixed the "Est. Time Until Play" time calculation to be more accurate
* Fixed an issue where /play song name auto completer would fail without a valid error message sometimes
* Fixed an issue where some song names or authors would be stripped/removed incorrectly if they contained non-Latin characters
* Fixed an issue where `/tag <tag>` would sometimes fail

## Changed
* Spotify playlists will now instantly queue all songs in the playlist (Instead of taking up to several minutes with extremely large playlists with hundreds of songs in them)
* Made some internal adjustments to caching for music to improve performance when loading/searching for songs

# January 20th - Command Changes
## Fixed
* Fixed an issue where "Total Channels" on the `/stats` command was incorrect

## Changed
* Grouped `/query` command into `/minecraft query` command
* Grouped `/mcskin` command into `/minecraft skin` command

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