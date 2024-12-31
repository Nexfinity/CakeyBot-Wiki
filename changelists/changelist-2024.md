---
title: Changelist 2024
description: 
published: 1
date: 2024-12-31T22:13:33.618Z
tags: 
editor: markdown
dateCreated: 2024-01-02T23:52:26.127Z
---

# December 31st - New Animal Images
## Added 
* Added new `/giveaways list-entries` command.
* Added "Duck, Alpaca, Fish, Seal, Camel & Wolf" imagesm to Daily Content
* Added "Duck, Alpaca, Fish, Seal, Camel & Wolf" to the `/image` command

# December 29th - Daily Capybaras & Anonymous Warnings
## Added
* Added Capybaras to "Daily Content"
* Added support for anonymous warnings

# December 27th - Misc. Fixes
## Fixed
* You can no longer challange bots to tic-tac-toe
* Fixed an issue where the new achievement color banners would not display correctly. (Teal w/ dark background still currently broken)

# December 22nd - Custom Achievements
## Added
* Added support for custom/manual achievements!
  * Management command: `/achievements custom <grant | revoke> <achievement> [user]`
  * Related auto responder placeholders: 
    * `{achievement-grant:<id>}` - Grants the custom achievement to the user.
    * `{achievement-revoke:<id>}` - Revokes the custom achievement from the user.

**Notes:** 
* You can only grant/revoke CUSTOM achievements. You can NOT grant/revoke progress-based achievements.
* You can not swap progress based achievements into CUSTOM / MANUAL achievements after they have been created. (or vice-versa)

# December 21st - Force to Starboard
## Changed
* Combined "Analyze Image" and "Analyze Message" into the same context menu option

## Added
* Added new "Force to Starboard" context menu option

# December 19th - Daily Content
## Added
* Added new Daily Content alerts! You can now have daily images and facts posted to channels in your server!
* Added dedicated birthday page to dashboard. (Including ability to view and delete birthdays in the server)
* Added new `/setup clear-achievement-data` command.

# December 15th - Achievement Fix
## Fixed
* Fixed an issue where achievements would count thread creations twice.

# December 14th - Channel XP Multipliers
## Added
* Added Channel XP Multiplier support for leveling.

# December 11th - Emote Fix
## Fixed
* Fixed the CB_Check emote not displaying correctly.

# December 10th - Statistic Channels
## Added
* Cakey Bot now has support for statistic channels! You can currently configure up to 7 different statistic channels
* Added optional "Required XP Level" requirement for giveaways!

# November 19th - Custom Rank Banner Editor
## Added
* Added support for using our new fancy image editor on `/rank` leveling cards. (Similar to join/leave banners)

# November 14th - Custom Image Banner Editor
## Added
* We've now added a super fancy new custom image banner editor for our join & leave announcement banners.

# October 21st - XP Bot Import
## Added 
* Added support for importing XP data from XP-Bot.Net. Read more: https://xp-bot.net/blog/b1728227181194p

# October 18th - Code Block Reminders
## Added
* Added code block reminders for plaintext code snippits in chat.

# October 17th - Ban Sync Directions
## Added
* Added the ability to choose ban-sync direction \[and unban direction\]

# October 10th - Verification Customization
## Added
* Added the ability to use custom embeds with verification
* Added the ability to customize the button name/text for verification embeds

# October 9th - Verification V2
## Changed
* Overhauled the verification role system and added 3 new methods for verification!
  * Slash Command (Same as previously)
  * Button Press
  * Captcha Solving
  * Custom Password

# October 5th - Ignore Categories
## Fixed
* Fixed an issue where editing a YouTube social feed would cause an "undefined" error for the URL.
* Fixed an issue with command ratelimit cooldown timers displaying incorrect times.
* Fixed a string newlines issue on the `/temp-voice admin create` command.

## Changed
* Added the ability to select entire categories to be ignored for Leveling, AutoMod, AuditLogs, Starboard, & Achievements.

# October 4th - Placeholder Fixes
## Fixed
* Fixed an issue where the `{user.nickname}` placeholder would show the username instead of the nickname.

## Added
* Added support for global names with the `{user.globalname}` placeholder.

# September 27th - Misc. improvements
## Fixed
* Fixed an issue where "Thread Updated" audit log events would not display modified tags

## Changed
* Birthday messages now allow mentions/pings
* Server Boosted roles can now be selected as XP role multipliers
* Twitch social feeds will now automatically strip @ symbols to prevent invalid username inputs

# September 12th - New Resources
## Added
* Added two new resources to the website:
  * https://cakey.bot/xp-table.html
  * https://cakey.bot/xp-calculator.html

# September 3rd - User App Context Menus
## Changed
* Added support for Cakey Bot's context menu in user apps/DMs (excluding user/message reporting)

# September 2nd - Temporary Voice Lobbies
## Added
* Added temporary voice lobbies!
  * Create a temporary voice channel lobby with: `/temp-voice admin create-lobby` (You can freely rename the lobby and category channels)
  * Users can then join the voice channel and automatically get their own voice channel they can manage
  * Once all users have left the temporary voice channel, it will self-delete
  * You can disable/remove the feature either by deleting the channels or running the `/temp-voice admin clear-lobby` command.

# August 30th - Server Banners & Bug Fixes
## Fixed
* Misc. bug fixes.

## Changed
* Added some additional permission checks for some moderation commands.

## Added
* Added server banner to the `/serverinfo` command, if the server has one.

# August 29th - Ticket Transcript Fix
## Fixed
* Fixed support ticket transcripts

# August 26th - Bug Fixes
## Fixed
* Fixed an issue where economy high/lo buttons would override ticket creation.
* Fixed an incorrect error message for the `/ecoadmin manage-money` command.

# August 24th - Bulk Kick Role
## Added
* Added new `/role bulkkick <role>` command. Requires ManageServer AND ManageRoles permission to use.

## Changed
* Updated the previous Auto role/Leveling role change to also disable roles that have the Manage Roles permission to prevent role escalation.

# August 23rd - Role Mention Cooldowns & Self Roles
## Added
* Re-added a widely requested feature, self roles! Use the /selfrole command to configure.
* Added new "Role Mention Cooldown" system. This allows you to define cooldowns for mentionable roles to prevent users from spamming mentions.

# August 22nd - New Games & Bug Fixes
## Fixed
* Fixed an issue where Cakey Bot would not automatically generate default Anti-Raid settings when joining a new server.
## Changed
* Added new custom error message pages to web dashboard for when data is missing from the database.
* Relocated the `/debug` command to `/setup debug`

## Added
* Added the ability to bypass ban syncs by using `-nosync` in the ban reason.
* Added the ability to have ticket channels ignored for Channel Created & Deleted audit log events.
* Added new `/random-user` command.
* Added new `/eco high-or-low` economy game command.

# August 15th - Spanish Locale
## Added 
* Added new Spanish locale for web dashboard and the bot. Thanks @Xurtan & @Tonno for your contributions!

# August 8th - Polls and Poleplay
## Fixed
* Fixed several more bugs.

## Changed
* Added the ability to "Re-roll" dice with the click of a button.

## Added
* Added new `{poll:}` placeholder to put Discord polls on auto responders.
* Added new `/rp bonk <user>` command.
* Added new `/role listusers` command.
* Added new `/setup force-check-boosts` command.

# August 7th - Bug Fix Roundup
## Fixed
* Fixed a massive collection of bugs and internal issues. (Too many to really list, majority of which were fairly minor, or specific edge-cases)

# July 16th - AFK Fix
## Fixed
* Server admins can now actually remove AFK messages from other users

# July 4th - Economy Fixes & Birthday Resetting
## Fixed
* Fixed voice transcripts not being properly censored.
* Fixed not being able to purchase economy items.
* Fixed not being able to use some economy commands on yourself.
* Fixed not being able to bulk import some auto responder flag types.
* Fixed integer overflow issue on some economy commands.

## Changed
* Updated `/eco shop` to display a "All items owned" option when everything is owned.
* Removed the additional date formatting when viewing birthdays.
* Enabled some game commands for user apps. (like `/coinflip` & `/dice`)
* Temporarily disabled lucky cube again for re-balancing.

## Added
* Added `/setup clear-all-birthdays` & `/setup clear-missing-birthdays` commands.
* Added thread owner info to "Thread Created" & "Thread Deleted" audit log entries

# July 2nd - More Bug Fixes
## Fixed
* Fixed `/eco shop` command not working once every item has been bought.
* Fixed interactive audit log buttons show both an error and success message
* Fixed `/role add` command sometimes failing hierarchy checks or not returning any message.

## Changed
* Disabled the ability to interact with bots using economy commands.
* Decreased "Lucky Cube" RNG improvement from 33% to 7%

# June 30th - Misc. Fixes & Changes
## Fixed
* Fixed not being able to buy multiple items from the `/eco shop`
* Fixed an issue where voice minute related achievements would not announce if the time didn't match the achievement _exactly_.

## Changed
* Removed year display for `/birthday next`

## Added
* Added new 0.02% chance for coinflips to result in the coin landing on the side. (Causes a 3x win multiplier for economy coinflips, regardless of user's original guess)
* Added the `/setup songrequest-disable` command to unset the song request channel. It won't delete the physical channel though.
* Added `/rp cry` & `/rp pout` commands.

# June 24th - QOL Updates
## Fixed
* Fixed some incorrect text formatting on the `/birthday set` command.

## Added
* Added a 5% chance to get "super work" on the `/eco work` command for up to double the pay.
* Added multiple poll types including "Simple", "Advanced" and "Discord".

# June 23rd - Interactive Audit Logs
## Added
* Added interactive audit logs! Several audit log events will now include various action buttons to revert or modify certain audit log events. Some of these events include:
  * User join
  * User banned/unbanned
  * Invite created
  * Channel, role & webhook created
  
Note: These buttons will still enforce required permissions and role hierarchy on the mods attempting to use them.

# June 21st - Economy Items & More!
## Changed
* The `/poll` command now requires atleast 2 options. (Reduces number of clicks)
* Updated the `{choose:}` placeholder for auto responders. You can now have up to 20 different lists and an unlimited number of items per list.

## Added
* Added several new economy placeholders: (Suggested by @sash.gg )
  * `{user.balance}` - Displays the user's current economy balance as a raw number. (No commas)
  * `{user.balance-formatted}` - Displays the user's current economy balance with a formatted number. (With commas)
  * `{economy-add:<amount>}` - Adds economy money to the user.
  * `{economy-remove:<amount>}` - Removes economy money from the user.
* Added economy item shop! You can purchase items to affect your odds:
  * **Nice Suit** - Improves begging odds by 50%
  * **Ninja Costume** - Improves chance of robbery success by 25%
  * **Lucky Cube** - Improves chance to win RNG-based games by 33%
  * **Guard Dog** - Decreases the likelihood of a successful robbery against you by 50%
  * **Bus Ticket** - Decreases the chance of someone being able to rob you by 25%
* Add several cooldown placeholders for auto responders:
  * `{cooldown-server:<seconds>}` - Adds a cooldown for the entire server for the specified amount of seconds.
  * `{cooldown-channel:<seconds>}` - Adds a cooldown per-channel for the specified amount of seconds.
  * `{cooldown-user:<seconds>}` - Adds a cooldown per-user for the specified amount of seconds.

# June 17th - Math Placeholder
## Added
* Added new `{math:X}` placeholder for auto responders.

# June 11th - AI Chat Bot Improvements
## Fixed
* Fixed birthdays not being announced correctly.

## Added
* Added `GPT-4`, `GPT-4o` and `GPT4-Turbo` options for the AI chat bot _(Limited to custom bots)_
* Increased "max token" usage for AI chat bot from 200 to 1k _(Limited to custom bots)_

# June 8th - Social Feed Threads
## Changed
* You can now assign optional thread IDs for social feeds
* The social feed page will now preserve the last selected tab when editing/adding feeds on the dashboard now
* The auto mod page will now preserve the last selected tab when modifying settings now

# June 1st - Birthday QOL
## Fixed
* The success message on the `/birthday set` command now correctly displays when setting another user's birthday.

## Changed
* Added the ability to set a custom birthday announcement message. (Includes basic placeholder support)
* The `/birthday set` command no longer requires a year. (Defaults to Cakey's creation year if not supplied)

# May 28th - Birthday QOL
## Changed
* Updated `/birthday set` command so that moderators can force set/update other user's birthdays in a server.

# May 21st - High Leveling Limits
## Changed
* Leveling role reward limit has now been increased to a maximum of 20 for premium servers
* Leveling role XP modifier limit has now been increased to a maximum of 10 for premium servers

# May 18th - Add/Remove Roles on Achievements
## Changed
* Updated Auto Responder placeholder priority so message deletion is calculated before thread placeholders (Prevents a niche issue with message deletion when closing a thread via placeholders)
* Economy command rate limits are now per-user+per-server instead of explicitly per user. (This means a user's cooldown is separate for each server instead of being globally linked to the user)

## Added
* Added the ability to grant and remove roles when users unlock achievements

# May 2nd - Reset Levels & Thread Management
## Added
* Added new `/setup reset-levels` command to reset ALL XP/leveling data for a server.
* Added several new thread-specific placeholders: `{closethread}`, `{lockthread}`, & `{deletethread}`

# May 1st - Leaderboard Fixes
## Fixed
* Fixed an issue where the leveling leaderboard on the website would display incorrect progress bars
* Fixed an issue where the leveling leaderboard on the website would fail to display certain users if their level/XP was too low.

# April 28th - Achievements Ignored Channels
## Added
* Added the ability to have specific channels ignored for Achievements. 

# April 27th - Support Rating Fix
## Fixed
* Fixed support ticket ratings not sending correctly.

# April 23rd - Misc. Fixes
## Fixed
* Fixed the Image & GIF only category channels deleting valid posts
* Fixed loading non-Spotify playlists in music (Soundcloud and such)
* Fixed a slightly issue causing birthday announcements to be heavily offset (Might still be off a bit but should be better than before)

# April 22nd - Spy.Pet Detection Improvements
## Fixed
* Created a bypass and re-enabled the "Has Server Been Tracked?" field for the `/setup spypet` command.

## Added
* Added a "Bulk Ban Known Accounts" button to the `/setup spypet` command. (This allows you to bulk ban all of their known accounts, even if they haven't joined yet)

# April 21st - Spy.Pet Detection
## Added
Not sure how many of you follow the news, however, recently a new site called SpyPet was released which actively tracks thousands of servers, hundreds of millions of users and billions of messages across Discord. This is a HUGE invasion of privacy and we think users should not only be aware that this is happening but also provide tools to help defend against it. That's why we have released a new command (`/setup spypet`) which will scan your server and inform you if any of SpyPet's known tracking accounts that are in your server. Which you can then ban or quarantine as you see fit. 

Currently this command will provide 3 things:
1) A list of confirmed SpyPet accounts in your server via ID blacklisting checks
2) A list of highly likely but not 100% confirmed probably accounts by matching their avatar hashes (SpyPet uses a random collection of the same avatars for their accounts, making it easy to track)
3) A true/false showing if you server is or has been tracked by SpyPet currently or previously (even if none of their accounts are still in your server.)

For more info about SpyPet and how it works, you can check out No Text To Speech's video [here](https://www.youtube.com/watch?v=ktxbXlF6UQE)

Also a shout out to @hampus. and @Sylveondeko for providing data and tools to help us provide this feature.

# April 20th - Playlist Fix
## Fixed
* Fixed an issue where creating/adding to Cakey playlists would result in invalid tracks which would prevent loading the playlists later.

# April 18th - Minor Bug Fix
## Fixed
* Fixed an issue where report user/message buttons would become desynced when using claim/mark as finished

# April 14th - More Economy Balancing
## Changed
* Economy RNG now uses Cryptographically secure random number generation
* Decreased `/eco coinflip` cooldown (60s => 20s)
* Decreased `/eco rob` cooldown (200s => 120s)
* Increased the minimum values for regular and super successful robberies

# April 12th - Economy Balancing
## Fixed
* Fixed success message on `/eco coinflip` displaying the wrong value

## Changed
* Increased the `/eco guess` reward from 2x to 5x
* `/eco guess` will now give 2x if you are +/- 1 from the result
* Increased the `/eco coinflip` reward from 30% to 50%
* Added a small chance to lose money on `/eco beg` to deter auto botting
* Added 15s cooldown to `/eco guess`
* Implemented randomized cooldowns for RNG economy games to discourage botting.

# April 11th - Economy Shop & items
## Added
* Added new `/eco donate <user>`
* Added new `/eco shop` command
* Added new `/eco items` command
* Added new `/eco iteminfo <item>` command
* Added new `/eco buy-item <item>` command
* Added new `/eco sell-item <item>` command

# April 7th - Misc. Fixes
## Fixed
* Fixed an issue where the new leveling changes would spam role awarded messages even if the user already had the role assigned. (Reported by @jixenator )

## Changed
* Updated the `{deleteafter:X}` placeholder to allow number values between 1 and 99 instead of just 1 and 9.
* Made several improvements to the music core.

# April 6th - Leveling Improvements
## Fixed
* Fixed leveling roles not being properly removed when leveling up or being demoted
* Fixed XP adjustments not assigning the highest eligible role available instead of only exact level matches

## Changed
* `/rank` and `/leaderboard` usernames are now title cased 
* Level up announcements will no longer actually mention all users within the role.

# April 2nd - Report Improvements
## Added
* Added the ability for users to claim message/user reports
* Added the ability to mark a message/user report as finished

# March 31st - More Bug Fixes
## Fixed
* Fixed an issue where `/lyrics` would fail when taking too long to load sometimes
* Fixed an issue where `/playlist` related commands would fail if the user had more than 25 playlists saved
* Fixed an issue where the additional music bots could be used in non-premium servers
* Fixed an issue where slash commands would sometimes fail for user-installed versions of Cakey Bot
* Fixed an issue where Join Raid detection would sometimes fail to detect properly

# March 30th - Tons of fixes and improvements
## Fixed
* Fixed Deezer as a supported music source.
* Fixed the increase of "Unknown errors" with music recently.
* Fixed an issue where users could use the "Report User" feature to timeout Cakey Bot.
* Fixed an issue where generic RSS feeds would try to ping `@delete-role` when no role was actually set.
* Fixed an issue where social feeds would not always send reliably for custom bots.
* Fixed several other misc. bugs.

## Changed
* Improved music quality slightly and improved search results.
* The `/play` song name auto completer now displays the author as well to help users find the correct track and artist.
* Updated all language locales for Cakey Bot and the web dashboard.

## Added
* Added image parsing support for markdown-based generic RSS feeds.

# March 24th - Channel Selector Icons
## Changed
* Channel selectors on the web dashboard (like ignored channels or such) will now show different icons for Voice, Stage and Announcement channels instead of the regular text # so you can tell the different between channels with the same name.

# March 20th - Cakey Bot Everywhere!
## Added
* You can now install Cakey Bot as a user app! 

# March 19th - New Banners
## Added
* Added some new join and leave background images.

# March 15th - Voice Channel Selection
## Fixed
* Fixed a bug where the `/suggestion` command would fail to create a thread if a suggestion channel was not set.

## Changed
* Added the ability to select voice & stage channels for stuff on the web dashboard (ignored channels, announcement output, category channels, etc) since voice channels have text support now.

# March 14th - Released Sticky Messages!
## Added
* Added the ability to create sticky messages!
  * Commands: 
    * `/stickymessage create <message> [channel] [embedUrl] [delay] [minMessages]`
    * `/stickymessage list`
    * `/stickymessage delete <stickyMessageId>`
  * Default values: 20s delay & 8 minimum messages
  * Premium servers can customize the delay and minimum messages.
  * Max number of sticky messages depends on server tier: 
    * Free: 3 Sticky Messages
    * Premium: 10 Sticky Messages
    * Custom Bots: 15 Sticky Messages

# March 6th - Fix Duplicate Twitch Announcements
## Changed
* Twitch social feed streams should no longer send duplicate announcements if the bot restarts or if we push an update. 

# March 4th - Role XP Multipliers
## Added
* Added the ability to create up to 5 role multipliers for leveling XP. 
* Added the ability for custom bot servers to use custom avatar/usernames on social feed embeds.

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