---
title: Changelist 2022
description: 
published: 1
date: 2025-02-20T06:47:13.724Z
tags: 
editor: markdown
dateCreated: 2022-10-18T07:50:13.252Z
---

# Dec 27th - Support Ticket Fixes

### Fixed
* Fixed support tickets not pinging the support role correctly
* Fixed tickets using default message on custom ticket embeds not sending the original ticket embed/reason in the channel

# Dec 21st - Different Announcement Channels

### Fixed
* Fixed wiki link buttons on the Announcements, Tags, and FAQ pages of the website to link to the correct pages on the new wiki/docs

### Changed
* Redesigned the announcements page on the dashboard to be easier to understand and use

### Added
* Added the ability to set different channels for each announcement type (user join/leave/ban/boost)
* Added the ability to set multi-line announcement messages
* Added the ability to set the number of days to prune messages for when banning a user

# Dec 14th - Improve Ticket Close Confirmation
### Changed
* Ticket close confirmation will now delete the ephemeral response if user clicks "No" rather than sending an additional message.

# Dec 8th - New Pride Flag Types

### Added
* Added new flag types for `/generateimage pride`: Pride, Transgender, Progress, Non-Binary, Lesbian, Gay Man, Bi-Sexual

# Dec 7th - Auto Responder Moderation Placeholders

### Added
* Added the ability to use moderation punishments inside of auto responders. Supported punishment types:
  * Warn
  * Timeout
  * Kick
  * Ban
  * Temp Ban


# Nov 28th - Color Rewrite

### Fixed
* Fixed wiki URLs on the `/help` command

### Changed
* Rewrote `/color` command and split it into 3 parts. I also added the ability to generate multiple random colors at once.
  * `/color random <amount>` - Generate a random color. (Or up to 10 random colors)
  * `/color hex <hex>` - View the color information for a given hex code.
  * `/color rgb <red> <green> <blue>` - View the color information for a give RGB code.

# Nov 20th - Manage Nicks Command

### Fixed
* Message deleted audit logs will now properly show message content if the message had files attached

### Changed
* Warnings will now show the names of mentioned channels, roles and users
* Merged /dehoist command into new /managenicks dehoist command
* Merged /unnick command into new /managenicks clear command

### Added
* Created new /managenicks <set | clear | dehoist | alphanumeric> <user | role | all> command

# Nov 16th - Tag Improvements

### Fixed
* Fixed an issue where audit logs for deleted messages would force non-image attachments to jpeg file type
* Fixed an issue where you couldn't modify existing tags with the `/tags edit` command.

### Added
* Added new sub-commands to `/tags`!
 * `/tags nuke` - Delete ALL tags in a server.
 * `/tags prune <user>` - Delete ALL tags from a user.
 * `/tags user <user>` - List the tags a user has made.
 * `/tags raw <tag>` - Display tag in raw format.
 * `/tags transfer <tag> <user>` - Transfer one of your tags to someone else.

# Nov 10th - Ticket Fixes

### Fixed
* Fixed line break on `/ticket adduser` and `/ticket removeuser`
* Ticket related commands can now be ran by all users in the ticker instead of just the user who created the ticket (`/anonreply` still requires the user to have the support team role to use)
* Fixed description typo in `/movemsg`

# Oct 29th - Poll Bug Fix & Suggestion Channel

### Fixed
* `/poll` no longer spams empty choices

### Changed
* `/list <roles | channels | emotes | bannedmembers>`. command now uses neatly formatted text files with numbered lines instead of uploading to Pastebin.

### Added
* Added the ability to set a specific suggestion channel for the `/suggestion` command. 
  * By default it will send/post the suggestion in the channel where the command is ran. If you set a specific channel, all suggestions will be posted there regardless of where the command is ran.
  * You can set this on the "Bot Settings" page of the web dashboard.

# Oct 27th - More Ticket Features!

### Fixed
* Tickets no longer generate a transcript if users don't send any messages in the ticket
* Ticket create button now shows the Successfully created your ticket here: #channel success message

### Added
* Added the ability to toggle sending a DM to the user when their ticket is closed
* Added the ability to add a confirmation when closing a ticket
* Added the ability to change the ticket's embed message content
* Added the ability to ping the selected Support Team role when a ticket is created

# Oct 26th - Suggestion Improvements

### Changed
* `/suggestion` now automatically opens a discussion thread.
* `/suggestion` is now limited to 1000 characters for the description and 100 for the title.
* Improved overall format/style of the suggestion embed

# Oct 24th - HTML Support Ticket Transcripts

### Added
* Support Tickets now use a fancy web-based transcript system
* Added the ability to anonymously respond to support tickets with `/ticket anonreply <message>`

# Oct 22nd - Support Ticket Categories

### Changed
* Support Ticket and `/purge` message transcripts will now list any attachments/files that were attached to a message

### Added
* Added the ability to create different "category" embeds for Support Tickets using the `/setup createticketembed <type>` command. You can view a list of categories and their options below:
  * Select menu - User Reporting
    * Report User - Broke Rules
    * Report User - Inappropriate Content
    * Report User - Spamming
    * Report User - Scamming/Phishing
    * Report User - Advertising
    * Report User - Malicious Files
    * Report User - NSFW Content
    * Report User - Account Hacking
    * Report User - Bug Abuse
  * Select menu - Moderation
    * Question About Rules
    * Warning Appeal
    * Mute/Ban Appeal
  * Select menu - Purchase issue
    * Payment issue
    * Refund request
    * Missing item/product
  * Select menu - Technical
    * Bug Report
    * Suggestion
    * Feedback
    * Question

# Oct 21st - Manage Users In Tickets

### Added
* Added the ability to add/remove users to/from support tickets with the `/ticket adduser <user>` & `/ticket removeuser <user>` commands.

# Oct 20th - Move Message Fix

### Fixed
* Fixed an issue where `/movemessage` would fail to respond on tenor gifs

# Oct 18th - Spotify Fix

### Fixed
* Fixed an issue where some Spotify playlist tracks would error and cause the entire playlist to not load

# Oct 16th - Deezer Music Support

### Added
* Added support for Deezer in music

# Oct 14th - Chat Bot AI Limit

### Changed
* Chat Bot AI is now limited to 500 requests per month per server. 
  * 1 request = 1 message
  * This is reset on the first of every month
  * You can view your current usage and limits on the "Bot Settings" page of the web dashboard
  * You can purchase higher limits on the premium page by modifying your existing subscriptions. 
    * Starts at $1 per 500 additional requests

# Oct 13th - Music Bug Fix

### Fixed
* Pushed another update to prevent queuing 30s "sample" songs (The previous patch I made for this apparently didn't apply to all sources)

# Oct 12th - Timeout & Ticket Bug Fixes

### Fixed
* Fixed "The application did not respond" error on `/ticket create`

### Changed
* Users can no longer see closed tickets
* Set max reason length to 500 for moderation commands. (This already existed, it just applies it directly in the Discord UI now)
* `/timeout` is now properly localized
* `/timeout` now uses Discord's timestamps
* Timeouts now show in Cakey Bot's audit log
* `/ticket create` now uses ephemeral response on success to decrease spam

### Added
* Added Spotify URLs to Auto Mod's Categroy-Specific Channels

# Oct 8th - Slash Command Migration Alert Removal

### Removed
* Removed "Slash Command Migration" warning. Please make sure your users are aware that text commands will no longer work with Cakey Bot and they will need to use Slash Commands.


# Oct 7th - Bulk Import & Export

### Added

* Added the ability to bulk import/export custom command and auto responder data.

# Oct 5th - Snipe Removal

### Removed

* Removed Sponsor Block feature (Since youtube is no longer supported)
* Removed `/snipe`, while I haven't received any warnings for it yet it seems that Discord does not like bot's that include it, so removing out of precaution

# Sept 30th - Music Changes

### Fixed

* Fixed issue where Cakey Bot would enqueue 30s 'sample' songs

### Changed

* Song URLs now no longer link to the original music source and instead redirect to Cakey Bot's main website
* `/nowplaying` no longer shows the current source provider

### Removed

* Removed support for YouTube in music (Now defaults to sound cloud)
* Removed the `/grab` command
* Removed YouTube sources from `/radio`

# Sept 16th - Category Specific Channels

### Added

* Added new Category Specific Channels!
  * YouTube URLs Only
  * Reddit URLs Only
  * Twitter URLs Only
  * GitHub URLs Only
  * Videos Only
  * Images Only
  * GIFs Only
  * Files Only
  * Emotes & Stickers Only
  * Counting Only

# Sept 22th - Music Title Blacklist

### Fixed

* `/play` command errors now use a proper error embed rather than plain text

### Changed

* Updated Auto Mod URL whitelist to be case-insensitive
* Updated Auto Mod URL blacklist to be case-insensitive
* Updated Auto Mod word blacklist to be case-insensitive
* Song request channel will now auto fast forward to timestamp if included in YouTube URL (Similar to `/play` command)

### Added

* Added new Music title blacklist

# Sept 19th - Audit & music Improvements

### Changed

* Increased Spotify album track limit from 20 to infinite on `/play` command. (For premium servers)
* Increased Spotify playlist track limit from 100 to infinite on `/play` command. (For premium servers)

### Added

* Added sponsor block support to music (For premium servers)
* Added emoji changed to Role Modified audit log event.
* Added icon changed to Role Modified audit log event.
* Added channel overwrite changes to Channel Modified audit log event.

### Removed

* Removed `/weather` command.

# Spet 18th - Channel Mix Filter

### Added

* Added new `/filterpreset vibrate`
* Added new `/filter channelmix <LeftToLeft> <LeftToRight> <RightToLeft> <RightToRight>`

# Sept 16th - Verify Command Bug Fix + New Filter Presets

### Fixed

* Fixed an issue where `/verify` would fail to respond to the command even on success
* Fixed `/filter timescale` success message showing incorrect variable names

### Added

* Added new filters to the `/filterpreset` command
  * Chipmunk
  * Darth Vader
  * Slow Mo
  * Speed

# Sept 15th - Feed Embed Colors & New EQ Presets

### Fixed

* Fixed not being able to set band #0 on equalizer
* Fixed equalizer success messages showing `#Zero`, `#One` for bands instead of `#0`, `#1`
* Fixed "Est. time until play" showing the incorrect time when adding tracks to the queue
* Fixed an issue where the `/filterpreset` command could be used by non-premium servers
* Fixed an issue where the `/eqpreset` command could be used by non-premium servers

### Changed

* Descriptions for filters will now show the default value
* `/equalizer` now shows default values if no bands have been set instead of an error message

### Added

* Added the ability to set custom embed colors on all social feeds!
* Added new presets to the `/eqpreset` command
  * Electronic
  * Soft
  * Pop
  * Ear Rape

# Sept 14th - AFK V2 + Premium Chat Bot

### Changed

* Command prefix setting has been moved from `Bot Settings/Core` to the `Custom Commands` page since it only affects custom commands now.

### Added

* Added a toggle to prefix user's nicknames with `[AFK]` when they are AFK
* Added a toggle to remove a user's AFK message/status when they send a message or join a VC
* Added a new AI chat bot system `[Premium-Only Feature]`

# Sept 12th - Improve Music Sources

### Fixed

* Fixed a typo in the `/purge` command
* Re-added BassBoost preset to `/filterpreset`

### Added

* Added music queue looping!
* Added support for Spotify albums
* Added support for YouTube Music playlists
* Added additional music artwork fallback images

# Sept 11th - Play File Support for Music

### Fixed

* Pushed a fix where `/purge` wouldn't show a success message if audit log wasn't configured

### Changed

* Merged `/gif <query>` into the `/search gif <query>` command to make room for the new `/playfile` command.

### Added

* Added new `/playfile <file>` command so you can listen to tracks you have downloaded on your PC/phone!

# Sept 9th - Premium Music Updates

### Fixed

* Fixed Premium Music Bots not working

### Changed

* Synced missing features to the music bots:
  * Duration included in "added to queue" message
  * Added the new `/sortqueue` commands
  * Added the player action history on `/nowplaying` command
  * Added the player control buttons on `/nowplaying` command

# Sept 6th - Tags V2

### Changed

* `/tags create <tag>` now checks if a tag exists before creating it.

### Added

*   Tag creation and management uses a new tiered permission system!

    * Manage Own: Admins - Manage All: Admins
    * Manage Own: Mods - Manage All: Admins
    * Manage Own: Mods - Manage All: Mods
    * Manage Own: Users - Manage All: Admins
    * Manage Own: Users - Manage All: Mods
    * Manage Own: Users - Manage All: Users

    The permissions default to `Manage Own: Admins - Manage All: Admins` so that only admins can create/manage tags by default meaning you'll have to manually enable tag creation for users if you want to use tags in your server.

# Sept 6th - Music Player Action History

### Changed

* Moved `/dehoist` command to `/dehoist all`

### Added

* Added new "Player History" to the `/nowplaying` command!
  * This will show the last 5 events applied to the current music player and who made the actions.
* Added new `/dehoist single <user>` sub-command
* Added new `/dehoist role <role>` sub-command

# Sept 4th - Shipping QOL

### Changed

* `/weather` command now has a country flag icon for the country
* `/ship` now has a compatibility percentage calculated
* `/ship` no longer allows you to ship yourself with yourself

# Aug 28th - Now Playing Controls

### Added

* Added button controls to `/nowplaying`!
  * Rewind (-10s) => Play/pause
  * Fast forward (+10s)
  * Volume down (-10)
  * Toggle mute
  * Volume up (+10)
  * Loop song
  * Stop & clear queue
  * Skip song

# Aug 25th - New Audit Events

### Added

* Added new "User Kicked" audit log event
* "User Banned" and "User Kicked" audit log events will now show which moderator kicked/banned the user as well as the reason.
  * This requires Cakey Bot to have access to Discord's Audit Logs otherwise it'll just show that the user was banned/kicked without additional info

# Aug 24th - Song Request Channel V2

### Fixed

* Fixed song only playing for X amount of seconds before randomly disconnecting
* Fixed queue embed not showing the currently queued songs correctly/not updating
* Fixed messages sent by Cakey Bot in the song request channel not being deleted properly (including join related messages)
* Fixed songs not auto-skipping to the next one in the queue on song end if enqueued via song request channel
* Fixed a bug that allowed users to control the song request channel via reactions/buttons if they were not in the same voice channel with the bot

### Changed

* Upgraded song request channels to buttons (instead of reactions)
  * When clicking an existing reaction or clearing all reactions on the music embed, it'll auto migrate
  * When using the `/setup songrequest` command, it'll create using the new buttons

# Aug 23th - YouTube Social Feed

### Added

* Added new YouTube social feed notifications for new video uploads!
  * Note: Due to limitations with how infrequently YouTube's RSS feed updates, it can take UP TO 30 minutes after the video upload for Cakey Bot to "notice" the video and send the alert in Discord.

# Aug 19th - Audit Log Improvements

### Changed

* Bulk Message deletions will now save a transcript of the bulk deleted messages
* Deleted messages that contain an image now use a more reliable method for storing the image in the log
* Updated `/purge between` so that the message ID order does not matter anymore.

# Aug 11th - Auto Mod Bug Fix

### Fixed

* Auto Mod now actually triggers on the minimum value rather than Minimum + 1

# Aug 10th - Max Volume Increase

### Changed

* Increased max `/volume` for music (100 => 200)

# Aug 5th - QOL Improvements

### Changed

* The `/tag <tag>` command now makes use of Discord auto-complete system
* The `/tags edit <tag>` & `/tags delete <tag>` commands now make use of Discord auto-complete system
* Moved `/ticket createembed` command to `/setup createticketembed` (Added docs for this as well)
* Changed `/ticket createticket <opt:desc>` command to `/ticket new <opt:desc>`

# Aug 4th - Roleplay QOL

### Fixed

* Fixed an issue where `/queue` & `/warnings` would say "failed to respond" but actually sent a response

### Changed

* `/rp` commands will now mention the user rather than showing a plain username

# July 29th - Bug Fixes + New Command

### Fixed

* Reasons for non-silent moderation commands will now show as expected.
* Fixed some false positives with the new phone number auto mod check.
* Fixed an issue where warning audit logs would be missing the hashtag between usernames/discriminators.
* Fixed an issue where some slash commands would be shown only to the original user and not to the entire chat
* Slash commands/interactions will now properly display in your selected language like old text commands did (if you have a non-english language set on the web dashboard for your server)

### Changed

* Merged `/verify setup` & `/musicsetup` into a single `/setup <verifyrole | songrequest>` command.

### Added

* Added new `/movemsg <messageId> <newChannel>` command.

### Removed

* Removed `/pokedex` command.

# July 28th - Phone Number Auto Mod

### Added

* Added new 'phone number' check to auto mod

# July 27th - Slash Command QOL Updates

### Fixed

* `/purge` commands will no longer show a "failed to respond" error message
* `/purge` result messages now properly send to the log channel instead sending in the channel where the command was ran

### Changed

* Updated `/playlist list` & `/playlist delete` so they can be used while music is not playing.
* User playlists are now global and not linked to a specific server.
* `/unwarn` will now send a DM to the user notifying them of the removal.
* Modified the parameters of `/unwarn <user> <id>` to `/unwarn <id> <opt:isSilent>`
* All moderator commands that can provide a reason now include a `isSilent` parameter instead of using the old "-s"/"-silent" method in the reason itself.
* YouTube songs will now jump to the specified time if the URL contains a `?t=453` timestamp.

### Added

* Added a new `/remove keyword <keyword>` sub-command to remove all tracks in the queue whose title contains the specified keyword.
* Added a new `/remove user <user>` sub-command to remove all tracks in the queue that were added by the specified user.
* Added new `/sortqueue <title | author | length> <asc/desc>` command to re-sort the queue.
* Added new `/sortqueue reverse` command to re-sort the queue in reverse.
* Added new `/sortqueue swap <firstIndex> <secondIndex>` command to swap two tracks around in the queue.
* Updated `/playlist list` & `/playlist delete` so they can be used while music is not playing.
* Added new `/playlist rename <name> <newName>` sub-command to rename user playlists.

### Removed

* Removed `{prefix}` placeholder for auto responder/custom commands.
* Removed `/rp poke` sub-command due to API being removed.

# July 26th - Music Updates + Bug Fixes

### Fixed

* Fixed an issue where Cakey Bot would not work in Discord servers that had a newer 19-digit length server ID
* Misc. Bug Fixes

### Changed

* `/pause` now works as a toggle and will resume if the song is currently paused. (Instead of having to type `/resume`)

### Added

* The anti-phishing module in the auto moderation now includes several popular IP-grabbing URLs in the blacklist.
* Added an optional `shuffleQueue` parameter to the `/play` command to shuffle the queue after queueing a new song/playlist.
* Added an optional `count` parameter to `/skip` to skip more than one song at a time.
* Added an optional `playTop` parameter to `/play` to insert a song at the start/top of the queue instead of the end.
* Added new `/remove first` sub-command to remove the first track in the queue.
* Added new `/remove last` sub-command to remove the last track in the queue.
* Added a new `/lockqueue` command that will prevent the queue from being modified by non-DJs/moderators. (This will disabling skipping, removing, jumping to, and shuffling but will still allow users to add new songs.)

# July 21st - Query & Slash Command Fixes

### Fixed

* Fixed `/query` showing incorrect information for PE/Bedrock servers
* Fixed wildcard contains flag for auto responder not working properly with literal `?` triggers.
* Fixed an issue where `/play` would return an incorrect error response

### Removed

* Removed the `/join` command. Cakey Bot will auto-join when running the `/play` command.

# July 3rd - Command Removal

### Removed

* Removed `!togglemention` command
* Removed `!togglehoist` command
* Removed `!rolecolor` command
* Removed `!bing` command
* Removed `!covid` command
* Removed `!video` command
* Removed `!staff` command
* Removed `!vote` command
* Removed `!xkcd` command
* Removed `!fakebots` command
* Removed `!premium` command
* Removed `!inviteinfo` command
* Removed `!quote` command

# June 30th - 8D audio

### Fixed

* Fixed default values for some audio filters
* Fixed audio filters not properly disabling

### Added

* Added new `!8d` audio filter for music `[Premium command]`
* Added new `!reverb` audio filter for music `[Premium command]`

# June 28th - More music sources and Echo filter

### Added

* Added support for `.mkv` files for Direct URL source
* Added new `Echo` music filter. Usage: `!filter echo <delay> <decay>`
* Added a ton of new support music sources:
  * Apple music
  * OC Remix
  * Get Yarn
  * Clyp It
  * Reddit
  * Mix Cloud
  * TikTok _**(Experimental, works on most videos)**_

# June 2nd - Text-In-Voice + Music Filters

### Changed

* Fined tuned all music filters to sound a bit better

### Added

* Cakey Bot now supports Text-In-Voice channels
* Added new "bandpass" filter

# June 1st - Massive Music Rewrite - Part 1

### Fixed

* Fixed inactivity disconnect after 30 seconds
* Fixed `!join` saying it lacks permissions when it joins anyways
* Fixed `!move` just disconnecting Cakey Bot
* Fixed `!nowplaying` now highlighting the song title link incorrectly
* Fixed missing emoji on the FinishedPlaying/NowPlaying message
* Fixed `!lyrics` not working
* Fixed being able to go into negatives with `!rewind`

### Changed

* Moved TrackEnd code into player & fix now playing messages when a track ends (much more reliable)
* Slightly increased `!lyrics` cooldown to prevent abuse
* Decreased audio buffer size (Filters/volume changes take effect faster)

### Added

* Added support for voice text channels (sometimes fails due to DNet bug will be fully functional in a few days)
* Added ability for DJs/Admins to force move cakey while playing music

# May 30th - Auto Role Fix

### Fixed

* Fixed an issue where Cakey Bot would spam auto roles when modifying a user's roles

# May 28th - Anime Fixes

### Fixed

* Fixed `!anime` command
* Fixed `!manga` command

### Changed

* Prefixes are now case-insensitive

# May 25th - FMBot Bot Scrobbling

### Added

* FMBot's Bot Scrobbling feature now works with Cakey Bot's music. ([https://fmbot.xyz/](https://fmbot.xyz/))

# May 21st - More Support Tickets

### Changed

* Ability to open up-to \~500 support tickets (Discord max channel limit) \[Previously was limited to \~150]

# May 20th - Misc Bug Fixes

### Added

* Added more URLs to phishing URL

### Fixed

* Debug inspect will now send the output as a file if the content is longer than 2k characters (Reported by @CelticTrinculo )
* Fixed hierarchy related error messages (Reported by @CelticTrinculo )

# May 17th - Confirm Delete Fix

### Fixed

* Fixed `{confirmdelete}` placeholder

# May 16th - Support Fixes

### Fixed

* Re-wrote the entire Support Ticket category creation process so it should be much more reliable (Discord caching messed with it a bit)

### Changed

* Swapped Cakey's default auth link to in-app
* Added in-app auth to all Cakey music bots

### Removed

* Removed `!steam` command
* Removed `!moviedb` command
* Removed `!timezone` command
* Removed `!fortune` command
* Removed `!modmenu` command
* Removed `!imdb` command
* Removed `!trailer` command

# May 9th - Timestamp QOL

### Changed

* Updated all visible timestamps to use Discord's localized timestamp system
  * `!warnings`, `!userinfo`, `!serverinfo`, `!inviteinfo`

# May 2nd - Banner Fixes

### Fixed

* Join/leave banners have been restored and are now functional again.

# April 17th - Bug Fixes

### Fixed

* Fixed transcripts not showing any messages for embeds or file attachments on support tickets
* Fixed auto mod invite false positives with channel/message links
* Fixed Cakey Bot's DM/group chat detection

### Changed

* Improved layout/formatting for `!serverinfo` and `!userinfo` commands (Also removed deprecated fields)
* Audit message deleted will now directly attach any deleted images to the audit log message for persistent storage instead of relying on third parties (Imgur)

# April 14th - Responder Bug Fixes

### Fixed

* Fixed webhook detection for auto responder

# April 12th - Higher Ticket Limits

### Changed

* Increased number of open tickets a server can have (50 => 150)
  * This limit was due to category channels only being able to have up to 50 channels each, Cakey Bot will now create "Support Tickets 2" and "Support Tickets 3" as needed.
  * If this becomes insufficient, I'll increase the limit again for larger servers.

# April 9th - Custom Embeds

### Added

* You can now attach a custom embed to your auto responders and custom commands!
* Note: For the time being custom embeds will be limited to Premium servers only.

# April 5th - Song Thumbnails

### Fixed

* Cakey Bot now supports Stage channels again
* Re-added thumbnail preview support for `!nowplaying` commands
* Song request channel image should now update to resolved track image again

# March 26th - Query Bug Fix

### Fixed

* Fixed `!query` for MCPE/bedrock servers

# March 22nd - Timeout Improvements

### Changed

* Update `!timeout` command max duration to 28 days

# March 14th - Reply Placeholder

### Added

* Added new `{reply}` placeholder for custom commands/auto responder to "reply" to the message that triggered it.

# March 13th - Radio Streams

### Added

* Added new `!radio` command to easily queue up live radio streams without finding the direct URL. (If you have suggestions for more, post them in 「🌟」feature-requests )
  * Note: You can still use direct URLs for live radio if you wish

# March 11th - Music Fixes + Spotify Playlists

### Fixed

* Fixed single-song Spotify URLs not loading
* Fixed `!nowplaying` showing the incorrect source (Will be applied on next restart)

### Changed

* Disabled the ability to use playlist URLs in `!search` command (Since it's designed to only load a single song anyways)
* Patched an exploit where `!playlist` command allowed users to bypass premium restrictions on music
* Moderation commands now include use-specified reason in the audit log entry

### Added

* Added "stayed for" property to audit user left event
* Added support for Spotify playlist URL loading
* Added reason support for `!timeout` command

# March 6th - Social Feed Features

### Added

* Added new `!timeout <user> <time>` command.
* Modified social feed limits (read up in 「📣」website-updates )
* Added the ability to have social feeds ping a specific role
* Ability to set custom embed color for social feeds coming soon

# March 5th - Reddit Fixes

### Fixed

* Multiple fixes for Reddit social feed

### Changed

* No longer require channel ID for any social feed

### Added

* Added support for "Link Posts" on Reddit feeds
  * Images for "Link Posts" will properly be embeded inside of Discord as a preview

# March 2nd - Auto Responder Fixes

### Fixed

* Auto Responder webhook trigger should now be functional again
* Fixed an issue where Twitch/Reddit feeds would not send at all

### Changed

* Custom Commands/Auto responder `{not:}` & `{require:}` placeholders are now checked before all other placeholders. (This means `{delete}` no longer triggers if you have a `{not:}` placeholder)

# Feb 25th - Auto Mod Punishments

### Added

* Added new auto mod punishment type: `Delete & Timeout User (1h)`
* Punishment type now shows on the auto mod log entry

# Feb 21st - More Trivia Questions!

### Added

* Added 500 new trivia questions!

# Feb 20th - Auto Mod Fixes

### Fixed

* Mass capitalization, Duplicate character and duplicate word checks should now work properly with "min character" and "min percent" properties
* Discord invite link check should now properly detect Discord invites again (the anti-phishing module broke this by accident)

# Feb 15th - Image Manipulation/Banner Fixes

### Fixed

* Fixed join/leave image banners not working
* Fixed `!query` banners not working
* Fixed `!pride` command not working

### Added

* Added support for canary URLs to auto quoter

# Feb 14th - Misc. Bug Fixes

### Fixed

* `!trivia` now properly disables answer buttons after being clicked
* All Image Manipulation commands support messages with multiple attachments/images
  * Currently it only applies to the first image/attachment
* Fixed a ton of misc. errors and bugs

### Changed

* Uploaded completed Arabic translations

# Feb 3rd - Fixed Webhooks/Social Feeds

### Fixed

* Twitch and Reddit social feeds should now send as expected again

# Feb 2nd - Phishing Improvement

### Changed

* Cakey Bot will now ignore URLs on the phishing check if the URL is added to the dashboard whitelist (if you have false positive triggers)

# Jan 26th - Fixed Error Messages

### Fixed

* Fixed error messages not displaying (ratelimits, missing permissions, module disabled, multiple matches, etc)
* Fixed typereader not working with plain user IDs on commands

# Jan 25th - Error Message Bug Fixes

### Fixed

* Fixed multiple bugs with `!warnings` if the user has left the server or doesn't share _any_ servers with Cakey Bot.
* Fixed error messages not showing on invalid server/guild users

### Added

* Fully pushed caching for server settings on Cakey Bot. This means some changes on the web dashboard may take up to 5 minutes to apply in your server.
  * Some settings (like auto responder, custom commands, tags and auto moderation) will all still update live/instantly.

# Jan 9th - Silent Moderation QOL

### Changed

* "-s" and "-silent" will be stripped from the reason
* "\[SILENT]" will be prefixed before the reason so that you know the action was done silently (without sending a DM to the user)

Remember, if you run the command in a public channel, some users may still see that you took the action, silent just prevents Cakey from sending a notice DM to the infracted user.