---
title: Changelist 2025
description: 
published: 1
date: 2025-08-30T23:20:28.522Z
tags: 
editor: markdown
dateCreated: 2025-01-10T14:55:14.523Z
---

# August 29th - Chat Bot Replies
## Changed
* Chat AI Bot will now use Discord 'replies' when responding. This makes it more clear that the bot is explicitly replying to a specific user. Also makes the conversation feel a bit more 'natural'.

# August 28th - Banner Rendering Fixes
## Fixed
* Fixed some rendering issues relating to center alignment and shape strokes for join/leave & rank card banners.

# August 18th - Modify Image Fixes
## Fixed
* Fixed most of the `/modifyimage` commands excluding the basic re-color ones such as 'red', 'green' ,'blue', etc.

## Changed
* The `/modifyimage` commands no longer force-resize images down to be tiny.
* The `/modifyimage` commands now preserve original quality and aspect ratio.
* Most of the `/modifyimage` commands (the working ones), are now processed in-memory in the bot itself rather than depending on a third-party API. This ensures better performance (faster), quality and availability.

# August 14th - Purchase Fishing Biomes
## Changed
* Improved context color for fishing purchases (i.e. owned/max items are now have different colors)
* Changed "View Fish" for a biome from a button into a link to the wiki instead
* Higher tier biomes must now be purchased/unlocked
  * 2 Biomes are available by default for FREE (atleast one of which includes a legendary fish)
  * Biomes that have higher tier fish are more expensive
  * Some biomes require payment AND a minimum amount of previous biomes to be purchased. (Specific order of biomes does not matter, only amount)

## Added
* Added "Buy X with X command" alerts to fishing auto-completers to inform users they can buy better gear/biomes

# August 12th - Fishing Balancing
## Fixed
* Fixed an issue where the biome difficulty did not previously actually affect catch rates.
* Fixed some issues where fail chance multipliers were not being calculated correctly.
    * This means upgraded rods should make a much more significant difference in catch chances, especially in biomes with greater difficulties.
## Changed
* Adjusted fail rate of fishing rods:
  * Basic Rod: 10% => 30%
  * Advanced Rod: 7% => 20%
  * Master Rod: 4% => 10%
* Made a HUGE overhaul to the biome fish lists, difficulties, and catch chances. You can check the wiki for exact details, however some notable changes include:
  * The names of fish in specific biomes should generally more closely resemble the theme/name of the biome they are in
  * The catch chances for each tier of fish should be more consistent
  * The biome difficulty is now properly calculated/scaled based on the amount of each tier of fish available in the biome (and therefore more consistent)
  * Fish names, profit, weight and rarity level were unaffected during this overhaul.

This means some fish were swapped or moved between different biomes and catch chances were changed for many of the more rare fish.

# August 11th - Fishing QOL & Bug Fixes
## Fixed
* Economy fishing now respects comma/decimal formatting for fish weight
* Fixed a TON of random/misc. bugs

## Added
* Added a toggle between lbs and kg for fish weight

## Removed
* Removed support for XP-Bot.Net leveling importing since the bot no longer exists.
* Removed support for Amaribot leveling importing since they actively block exporting data now.

# August 8th - Fishing V2 Re-Balance
## Changed
* Fishing rods must be purchased in order. (Can no longer jump straight to the legendary rod)
* Increased the price of fishing rods:
  * Advanced Rod: 10k => 25k
  * Master Rod: 20k => 50k
  * Legendary Rod: 30k => 100k
* Adjusted the cost of some baits:
  * Kraken's Charm: 20k => 50k
  * Wormhole Larvae: 20k => 30k
  * Titan Worm: 10k => 15k
  * Golden Minnow: 30k => 25k
  * Rusted Can Lure: 1k => 5k
  * Pearlscale Grub: 2k => 5k

# August 8th - Economy Fishing Overhaul
## Removed
* Removed the `/eco fishing` command to replace it with a new set of sub-commands.

## Added
* Added `/eco fishing fish <biome> <rod> <bait>` command!
  * You can now acquire over **100 different unique fish** from **12 different biomes**!
  * You can also purchase **unique baits** and **upgrade your fishing rod** for better chances or additional loot/money!
  * Fish now have a rarity between: `Uncommon`, `Common`, `Rare`, `Epic`, `Legendary`, `Mythic`. With higher rarities being harder to find/catch.
  * Fish now have a **randomized weight** when caught.
  * All trash and fish caught will now be stored and you can view your stats using the `/eco fishing inventory` command!
* Added `/eco fishing list-biomes`
  * View all **13 biomes** as well as unique properties/info about them.
  * Different biomes will have different fish and different chances.
  * Some biomes may also have easier or harder difficult for catching fish at all
* Added `/eco fishing list-rods`
  * Lists available rods to purchase. Higher tier rods have a higher chance to catch fish instead of trash.
* Added `/eco fishing list-bait`
  * Lists available bait to purchase. Different baits have unique properties!
* Added `/eco fishing inventory [user]`
  * You can view all of your owned items in your inventory.
  * You can also view **epic stats** about your fishing history, such as how many types of fish caught & the largest fish caught.
  * you can also optional view another user's inventory and stats.
* Added `/eco fishing leaderboard <type>`
  * You can view 10 different types of leaderboard stats including:
    * Total Fish Caught
    * Total Trash Caught
    * Total Value of Fish
    * Total Weight of Fish
    * Most Mythic Fish Caught
    * Most Legendary Fish Caught
    * Most Epic Fish Caught
    * Most Rare Fish Caught
    * Most Uncommon Fish Caught
    * Most Common Fish Caught

# August 3rd - Clan Tag Audit Fixes
## Fixed
* Fixed clan tag change audit logging.

# August 1st - AI Version Bumps
## Changed
* Updated the AI chat models.
  * Free upgraded from `gpt-3.5-turbo` to `gpt-4o`.
  * Premium upgraded from `gpt-4o` to `gpt-4.1`.
  * Custom bots now default to `gpt-4.1`, can still be changed if using custom API key.

# July 25th - Roleplay Update
## Fixed
* Fixed broken `/rp` commands.

## Changed
* Changed `/rp cuddles` to `/rp bite` (no cuddles gifs on new API)

## Added
* Added `/rp dance` command.
* Added `/rp holdhands` command.
* Added `/rp highfive` command.
* Added `/rp grabcheeks` command.
* Added `/rp lick` command.
* Added `/rp poke` command.
* Added `/rp stare` command.
* Added `/rp wave` command.

# July 24th - Add'l Giveaway Fixes
## Fixed
* Fixed an issue where `/giveaway` output channel was not used correctly.
* Fixed an issue where `/giveaway` considered image urls required instead of optional.

# July 17th - Giveaway Image Fix
## Fixed
* Fixed image banners not displaying on giveaways.

## Added
* Add additional info regarding streak status to `/streaks view`.

# July 13th - Giveaway Overhaul
## Changed
* Overhauled entire giveaway process to include a fancy new giveaway builder.

## Added
* Added support for image banners on giveaways.
* Add clan tag support to the User Modified audit log event.

# June 27th - Staff/Server Notes
## Added
* Staff/server notes are now also available. By default anyone with Administrator or Manage Server will be able to view/manage server notes. You can also optionally set a "Staff Role" on the dashboard to allow non-admins to also view/manage them.

# June 25th - Economy Boost Fixes & Notes
## Fixed
* Fixed a visual error where `/eco minefield` cashout and `/eco fishing` would give boosted money amounts but only display non-boosted amounts in the success messages.
* Fixed an issue where all boosts acted as if they were only a 1x (non-boosted) amount.

## Added
* Added `/notes` command! You can now create personal and public notes in servers. Staff/server notes coming soon.

## Removed
* Removed `/math` command.

# June 21st - Eco Buff & Role Monitoring
## Changed
* Changed the permission required to grant/revoke custom achievements from `Manage Server` to `Manage Events`.
* `/eco minefield` now has better payout options. Profit scales dynamically the more correct tiles you guess and 100% perfect games result in a double profit jackpot!
* Increase max economy shop item count from `10` to `15`.
* The `/eco shop` command is now paginated, meaning we can display all items regardless of length/amount.

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