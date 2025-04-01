---
title: Changelist 2025
description: 
published: 1
date: 2025-04-01T16:53:44.714Z
tags: 
editor: markdown
dateCreated: 2025-01-10T14:55:14.523Z
---

# April 1st - Bug Fixes
## Fixed
* Fixed a visual bug on anti-raid alerts for message spam.
* Fixed an issue where XP decay would remove roles but not add the next eligible role.
* Fixed several misc. bugs.

# March 29th - Color Fix
## Fixed
* Fixed `/color random` rgb and hex code not matching correctly.

# March 22nd - Streak DM Reminder Fix
## Fixed
* Fixed an issue where streak DM reminders would not send a pre-emptive reminder 12 hours prior to the streak expiring.

# March 20th - Leaderboard Overhaul
## Changed
* Overhauled the `/leaderboard` & `/eco leaderboard` commands. Changes include:
  * Leaderboard slots are now dynamically generated. (Meaning you won't have extra empty slots displaying if you have less than 10 users)
  * Font type & size is now consistent between the # text and the usernames
  * Fix a spacing issue where names would get increasing offset the loser to #10 the slots got
  * Custom Bot and Premium users now have a custom background gradient! (+Cakey Bot staff)
  * Fixed a bug where leaderboards would fail to generate if avatar failed to load
* Updated consistency on website/dashboard for premium & custom bot colors to match the bot. (Gold for custom bots & pink for premium)

# March 19th - Auto Message Days & Streak Adjustments
## Changed
* Streaks now send reminder DMs by default.

## Added
* Added the ability to define a specific day for auto messages to send on.
* Added a "Ignore Solo Users" setting for voice leveling.
* Added an optional "required role" property for giveaways.

# March 16th - Bug Fixes
## Fixed
* Fixed XP being awarded to users in AFK channels.
* Fixed the `{require:#}` placeholder not working on forums/threads when `{originalpostonly}` was missing.
* Fixed auto message not parsing/sending Embeds at all.
* Fixed an issue where toggling other leveling settings would also affect the "Ignore Muted Users" setting toggle as well.

# March 6th - Minecraft QOL
## Changed
* `/minecraft query` will now display an error if port AND type are both null. You must specify atleast one.

# February 27th - Leveling XP Fix
## Fixed
* Fixed a long-standing bug where muted/defaened users were not properly ignored when calculating leveling XP.

# February 25th - Random Daily Image
## Added
* Added new "Random Image" for Daily Content

# February 23rd - Streak Role Rewards & Self Role Requirements
## Added
* Added role rewards for Streaks.
* Added a toggle to ignore muted users in VC for leveling XP
* Added the ability to set optional requirements for self roles, including:
  * Minimum XP level
  * Minimum Streak
  * Having an existing role

# February 18th - Leveling Command Merge
## Fixed
* Fixed an issue where streak reminders would be duplicated during bot restarts.

## Changed
* Merged `/manage-xp` & `/manage-level` commands into a single `/leveling` command.

# February 17th - Streaks Improvements
## Added
* Added the ability to view multiple pages on the `/streaks top` command instead of just the first top 10.
* Added DM reminders for soon to expire streaks as well as when the streak finally expires.
* Added new `/streaks toggle-reminder-opt-out` command to opt out of DM updates.
* Added new "SendDmReminders" setting on the dashboard. Defaults to disabled.
* Added new "DisableNicknameChange" setting on the dashboard. Defaults to disabled.
* Added the ability to set ignored channels & roles for anti-raid.
* Added the ability to toggle achievements enabled status.

# February 16th - Forwarded Message Voice Transcription
## Changed
* Bumped `{react:}` placeholder limit to 5. Previously 3.

## Added
* Added voice message transcription support for forwarded messages

# February 14th - Leveling Category Support
## Changed
* Added the ability to set categories on leveling channel multipliers

## Added
* Updated birthday role handler to be more reliable

# February 7th - Streak Fixes
## Fixed
* Fixed an issue where /streaks top could show duplicate entries for the same user.
* Fixed an issue where users who left might not have their streak data wiped correctly.

# February 4th - Reaction Purging
## Added
* Added the ability to bulk purge reactions using `/purge` commands via an optional `[reactions-only]` parameter.

# February 1st - Tempory Role Item Shop
## Added
* Added the ability to add "Temporary Role" unlocks into the economy shop.
* Added some anti-abuse checks to Streaks to prevent people artificially modifying their streak.
* Added the ability to have some channels ignored for Streaks.
* Added the ability to "Clone" existing achievements.

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