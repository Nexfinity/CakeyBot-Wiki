---
title: Changelist 2025
description: 
published: 1
date: 2025-06-21T06:36:59.960Z
tags: 
editor: markdown
dateCreated: 2025-01-10T14:55:14.523Z
---

# June 21st - Eco Buff & Role Monitoring
## Changed
* Changed the permission required to grant/revoke custom achievements from `Manage Server` to `Manage Events`.
* `/eco minefield` now has better payout options. Profit scales dynamically the more correct tiles you guess and 100% perfect games result in a double profit jackpot!

## Added
* Added the ability to 'Clone' Auto Messages on the dashboard.
* Added the ability to audit log when _specific_ roles are added to/removed from users.

# June 19th - Dashboard Security
## Fixed
* Fixed an issue where the sidebar info for the selected server did not updating correctly when swapping servers with the dropdown menu in the nav instead of the dashboard page.
* Fixed an issue where the sidebar would incorrectly show the server icon & name when a user tried to access a server they didn't have access to.

## Changed
* The web dashboard now requires users to have "Manage Server" or "Administrator" permissions on one of their roles that does NOT include the `@everyone` role. 
* The owner of the server will now always have access to manage the server regardless of their roles. (Previously they did, but the new role check could have potentially blocked them if they didn't have an admin role lol)

## Added
* Added new fancy portal graphic to the premium and custom bot error pages. (When users try to access the feature when they don't have premium/custom bot)

# June 14th - Audit QOL
## Added
* Added "Jump To" link for message deleted audit logs.

## Changed
* Voice channel join/leave audit logs now use mentions instead of plaintext usernames.
* Display "Time in Channel" on join/leave voice audit logs.

# May 21st - Temporary Role Placeholder
## Added
* Added `{addtemprole:}` placeholder.

# May 20th - Rendering Fix
## Fixed
* Fixed an issue with `/rank` cards where corners were not properly rounded on the progress bar and the rectangle shapes.

# May 8th - Economy & Self Role CV2 Overhaul
## Fixed
* The `/selfrole add` command now has proper validation for maximum added roles
* Fixed an issue where high-low games could be played by other users.
* Fixed `/animequote` not returning any results
* Fixed a visual bug on `/eco high-or-low` where it would always show 5 on the first stage but would select a random number behind the scenes. (The first stage is no longer randomized)

## Changed
* Reformatted the `/eco shop` command to look nicer and be easier to navigate.
* The ability to allow multiple purchases for `/eco shop` items and boosts can now be configured per-item instead of globally forced.
* Upgraded the self role limit from **125** to **250**. (Maximum number of roles a server can have)
* The `/selfrole list` command is now paginated to support this.
* The `/selfrole embed` command now makes use of Discord's new CV2 component system to allow up to 10 select menus in the same embed message.
* The `/eco minefield` bomb message now displays the tile number based on a 1-index instead of 0-index.

# May 6th - QOL Updates
## Fixed
* Deployed a patch that should fix birthdays announcing 1 day late for some time zones.
* Fixed a bug where a user couldn't have multiple temporary roles in the same server.

## Changed
* Added alert to dashboard to refresh server list. (Plus displays permissions required to configure servers)
* Streak reset warning now has a different title from the actual reset message to make them less confusing. (The embed colors are also different)
* XP & temporary roles can now be purchased multiple times in economy shop.

## Added
* Added new DM notice when XP decay gets applied to user. (Can be opted out similar to streak DM alerts)

# May 2nd - High/Low Multi-Stage
## Changed
* `/eco high-or-low` is now a multi-stage game, where you can keep guessing for higher potential rewards!
* You can now set different thresholds for auto kick/ban for new account creation.

# May 1st - Auto Kick
## Fixed
* Fixed an issue where `/eco minefield` would generate a new message when cashing out instead of updating the original one.

## Added
* Added new "Auto Kick" system (based on the Auto Ban system)

# April 29th - Fishing & Minefield Minigames
## Added
* Added new `/eco fishing` minigame!
* Added new `/eco minefield` minigame!

# April 27th - Economy Improvements
## Fixed
* Fixed an issue where `/eco leaderboard` would not display custom current formats/prefixes.

## Changed
* Economy `/eco work` now has unique/random messages for both success and failures.
* Economy `/eco work` now has a special 'scaling' bonus to pay pay when triggering the "super pay".

# April 25th - Leaderboard Fixes & Economy Anti-Abuse
## Fixed
* Fixed rendering issues on `/eco leaderboard` so it now properly matches `/leaderboard`'s style
* Fixed an issue where both leaderboards could display blank gaps if the bot was unable to load data for some users (i.e. they share no server with the bot anymore)
* Fixed an issue where `/leaderboard` showed the wrong position number for users not in the top ten.

## Changed
* `/eco leaderboard` will now display the user's current rank data if they are not within the Top 10. (Similar to `/leaderboard`)
* Modified `/donate` economy command to target users with less balance than the user running the command. 

## added
* Added economy transaction log. Mainly for internal tracking and anti-abuse measures, may become visible on dashboard per-server later.
* Added additional anti-abuse mechanics for the `/pay` & `/rob` commands.

# April 24th - Misc Changes
## Changed
* Added pagination to the `/ping` command.
* Music now uses a Lavalink cluster instead of a single node. (Should solve the problem with getting "no results" for Spotify)

## Removed
* Temporarily disabled birthday announcements while we debug and fix some timing issues.

# April 18th - Bulk Voice Management
## Added
* Added new `/bulk-voice` commands.
* Added new role ping parameter for `/giveaway` command for giveaway creation notifications.

# April 16th - Command Toggles
## Added
* Added the ability to toggle/disable individual roleplay commands.
* Added the ability to toggle/disable individual economy commands.

# April 9th - QOL & Fixes
## Fixed
* Fixed an issue where streak opt-in/opt-out buttons wouldn't apply for the correct server.

## Changed
* Streak opt-out will now remove streak data from the user's nickname.
* `/achievements list` & `/achievements view` are now both paginated for servers with a lot of achievements.

# April 5th - New Announcement Banners
## Added
* We have added 4 new premium join/leave banners! (with day & night variants)
  * Gaming
  * Lofi/Chill
  * Floral
  * Coffee Shop
  
Shout out to @CX for his awesome work on these banners!

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