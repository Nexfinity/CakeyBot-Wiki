---
title: Changelist 2025
description: 
published: 1
date: 2025-02-01T17:04:21.853Z
tags: 
editor: markdown
dateCreated: 2025-01-10T14:55:14.523Z
---

# February 1st - Tempory Role Item Shop
## Added
* Added the ability to add "Temporary Role" unlocks into the economy shop.
* Added some anti-abuse checks to Streaks to prevent people artificially modifying their streak.
* Added the ability to have some channels ignored for Streaks.

# January 31st - Streak Achievements
## Added
* Added the ability to create achievements that unlock when a user acquires a certain streak.

# January 30th - Streaks!
## Removed
* Removed `/emotetext` command.

## Added
* Added new "Streaks" feature. Encourage users to be active in your server by rewarding them for consecutive days of activity. Users can even compete on the leaderboard to see who has the longest streak!

# January 28th - Suggestion Improvements
## Changed
* The `/suggestion` command will now swap votes if the user has already voted for the opposite option, instead of erroring.
* The "Approve" & "Deny" buttons for `/suggestion` have been moved to the same row as the upvote/downvote buttons to save vertical space.

## Added
* Added the ability to forward approved/denied suggestions to a specific output channel.
* Added new `/ticket remind` command. This will send a DM reminder to this user.
* Added new `/ticket request-close` command. This will send a close request in the ticket for the user.

# January 25th - Emote Stats
## Added
* Added new `/emote stats` & `/emote top` commands.

# January 24th - Auto Messages
## Added
* Added new recurring "Auto Message" system!
* Added new `/setup toggle-autopublish` command to quickly and easily toggle the auto-publish status of the current channel.

# January 23rd - Support Ticket Customization
## Changed
* Introduced a +50% bonus to the user who steals in `/eco split-or-steal` to help discourage collusion/abuse.
* `/eco split-or-steal` will now introduce a prize modifier based on the player's previous choice history.

## Added
* Added the ability to customize _both_ the embed used to open support tickets AND the initial embed sent inside of newly created tickets.

# January 22nd - XP Decay & Ticket Re-Work Prep
## Changed
* Adjusted `/rob` cooldown to match `/work`.
* Pre-existing embeds using this category system will still function, however, they will act as a default embed and won't specify the additional drop-down menus anymore.

## Removed
* Removed the `/ticket create` command. (You now have to create a ticket embed for users to open tickets using `/setup createticketembed`)
* Removed the "category" options from the `/setup createticketembed` command. Instead it will ask for a panel number to generate an embed for (Currently just 1)

## Added
* Added XP decay system, can configure:
  * Days since last activity before decay starts
  * Percentage to decay per day
  * Minimum level before user is eligible to start decaying (and where decay stops)
* Added optional "Description" field for giveaways.
* Added the ability to send the Level Up messages inside of a basic embed.

# January 21st - Economy Boosts
## Fixed
* Fixed an issue where economy items were displayed globally for the `/eco iteminfo` command.

## Added
* Added economy boosts! You can create custom boosts on the dashboard and allow users to purchase them via `/eco itemshop`.

# January 20th - Economy Shop Re-Release
## Added
* Added the ability for server owners to create a list of items that can be purchased in the economy shop. These items allow users to unlock specific roles or gain leveling XP.
* Added a toggle to put a space between the currency prefix and the value.

# January 19th - Economy Customization
## Added
* Added a ton of new economy customization! Including:
  * Custom currency symbol (plus position)
  * Initial & max balances
  * Separator character customization
  * Ability to wipe user balances on user leave
  * Ability to disable commands related to money transferring between users (i.e. /rob, /pay, etc)
* Added ability to wipe user XP data on user leave for leveling

# January 18th - Economy Changes
## Removed
* The `/eco sell` command has been removed
* Removed all economy shop items

# January 17th - Randomized Birthday Messages
## Added
* Added the ability to set randomized/multiple birthday messages. (Semicolon `;` separated list)

# January 15th - Dashboard Improvements
## Added
* Added new alerts to the top of all of the dashboard pages to help direct users to the related wiki articles.
* Implemented a ton of internal caching for data. (This should make page loading a bit faster/more responsive)

# January 13th - Daily Content Pings
## Changed
* Updated tickets to auto-pin the initial message

## Added
* Added the ability to ping a role for Daily Content

# January 12th - Misc. Fixes
## Fixed
* Fixed an issue where custom bot social feeds wouldn't respect the "Use Default Data" setting.
* Fixed an issue where custom daily content wouldn't handle "mixed" content types correctly.
* Fixed an issue where long descriptions would not be displayed on achievements correctly.
* Misc. internal bug fixes.

## Changed
* Achievement descriptions are now limited to 140 characters. (Previously 500)

## Added
* Added an ending message with user mentions for when giveaways end.
* Added "Links Only" category to Auto Mod

# January 10th - Custom Daily Content
## Added
* Added new "Custom Data" support for Daily Content (Limited to custom bots)

# January 7th - Bug Fixes
## Fixed
* Removed some incorrect images from the "Panda" & "Capybara" daily image collections.
* Fixed support for selecting category, forums and media channels as ignored channels for Starboard, Audit Logs, and Auto Mod. (Selecting these will ignore threads created in these channels)

# January 5th - Suggestion Overhaul
## Changed
* Visual overhaul for `/suggestion` command.
  * Reactions replaced with upvote/downvote buttons
  * Added ability for server owners to approve/deny suggestions
  * Added a button to create a discussion thread

# January 1st - Server Boost Count
## Added
* Added "Server Boost Count" to statistic channels.