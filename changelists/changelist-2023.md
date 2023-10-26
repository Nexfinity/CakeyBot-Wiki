---
title: Changelist 2023
description: 
published: 1
date: 2023-10-26T11:59:53.247Z
tags: 
editor: markdown
dateCreated: 2023-01-02T17:57:13.587Z
---

# October 26th - Giveaways!
## Added
* New `/giveaway` commands!

# October 25th - /lockqueue Removal
## Removed
* Removed `/lockqueue` command

# October 24th - Auto Ban Moderation & Double XP Days
## Added
* Added a new "Auto Ban" settings that can be found on the "Auto Mod" page. It currently includes 4 different toggles to apply to new users who join your Discord server:
  * Invite in Username
  * Unverified Bots
  * New Accounts (<24 Hours Old)
  * No Avatar
* Added new "Disable Self-Starring" option for starboard
* Added the ability to change the `/rank` overlay opacity
* Added the ability to change the `/rank` accent color
* Added the ability to set specific days to award double XP to users for leveling

# October 23rd - Custom Embed Placeholder Support
## Added
* Added support for placeholder variables inside of Custom Embeds used for Auto Responders.

# October 22nd - QOL Improvements
## Added
* Added new "Analyze Message" context menu option for messages
* Added the ability to have starboard ignore specific channels.
* Added a toggle for tickets to ping the user who opened the ticket.

## Removed
* Removed "Base64 Encode" & "Base64 Decode" context menu options for messages
* Removed "Mute" & "Unmute" context menu options for users

# October 18th - Custom Bot Improvements
## Fixed
* Fixed an issue where tickets would not send a DM when closed

## Changed
* Discord Invites in automod will now allow whitelisted URLs/invites

## Added
* Added new Brazillian Portuguese language
* Added support for custom chat bot API key from open AI on custom bots
* Added support for custom chat bot personality on custom bots
* Added support for custom status messages on custom bots

# October 12th - Language File Updates
## Changed
* Updated all of Cakey Bot's language files to the latest translations on Crowdin.

# October 11th - Birthday Fix
## Fixed
* Fixed an issue where `/birthday set` wouldn't let users set a valid year
* Fixed an issue where "Channel Updated" audit log event could spam when there are no changes to listed due to Discord.
* `/filterpreset none` will now properly disable the "Reverb" effects

## Changed
* Re-implemented music track artwork resolution.

# October 9th - Permission Overwrite Audit Log & Trivia Updates
## Changed
* Re-enabled permission overwrite updated list for Channel Modified audit log event (and made the output human-readable instead of raw values)
* `/warn` now shows the warning ID in the success message.
* `/trivia` will now display the user's selected answer.
* Removed all duplicate trivia questions to decrease likelihood of duplicate questions appearing.

## Added
* Re-added the ability to purchase additional AI Chat Bot requests (You no longer need to have an active premium subscription to purchase additional requests)
* Several `/trivia` categories had very few questions so over a thousand new questions have been added. (Up to a total of over 2,600+ now!)
* Added two new categories to `/trivia`. "Art" and "Celebrities"

# October 8th - Trivia Category Selection
## Added
* Allow optional category selection for `/trivia`

# October 5th - Transcript Fixes
## Fixed
* Fixed an issue where ticket transcripts were not being generated.
* Fixed an issue where some image generations would fail to upload after modification.

# October 3rd - Misc. Bug Fixes
## Fixed
* Added validation to the `/emote import` and `/sticker import` commands to verify the file is actually a zip.
* Fixed several other misc. bugs

## Changed
* All commands should now properly return _some_ error if something goes wrong. (even if it's only a generic error message) 

# September 24th - New Emote & Sticker Commands
## Fixed
* `/emote create` & `/emote rename` now enforces Discord's 2 character minimum requirement for the name (and regex checks the name for validity)

## Changed
* Updated `/emote create` & `/emote delete` to display the remaining emote slot count after creating or deleting an emote.
* The sticker count for `/serverinfo` will now also show remaining slot count and max slot count for stickers.
* Increased max `/purge` limit to 200 (Previously 100)

## Added
* Added new `/emote create <file> <name>` command.
* Added new `/emote delete <emote>` command.
* Added new `/emote list` command.
* Added new `/emote rename <emote> <newName>` command.
* Added new `/emote download <emote>` command.
* Added new `/emote big <emote>` command.
* Added new `/emote import <zipFile>` command.
* Added new `/emote export` command.
* Added new `/sticker create <file> <name> <description>` command.
* Added new `/sticker delete <emote>` command.
* Added new `/sticker list` command.
* Added new `/sticker rename <emote> <newName>` command.
* Added new `/sticker download <emote>` command.
* Added new `/sticker big <emote>` command.
* Added new `/sticker import <zipFile>` command.
* Added new `/sticker export` command.

## Removed
* Removed the `/banlookup` command.

# September 23rd - Add & Remove Tag Placeholders
## Added
* Added a new placeholder: `{addtag:tag-name-here}` - Adds a tag to the thread if it doesn't exist already.
* Added a new placeholder: `{removetag:tag-name-here}` - Removes a tag from the thread if it exists.

# September 21st - Bug Fixes
## Fixed
* Fixed `/suggestion` command
* Fixed `/imagepoll` command
* Fixed `/poll` command
* Fixed some audit log events failing to log due to missing user avatars
* Fixed some other misc. bugs.

# September 19th - Moderation Improvements & Bug Fixes
## Fixed
* Fixed an issue where `/tictactoe` would respond with The application did not respond
* Fixed an issue where the AI player could override a tile already selected by the human player.

## Changed
* You can now use a custom reason when clicking "Warn User" on a user or message report.
* Removed the 31 day max limit from TempBans and TempMutes.

## Added
* Added the ability to blacklist certain file extensions on your server.
* Added the ability to assign temporary roles to users with `/role temporary`

# September 13th - Warning Bug Fixes
## Fixed
* Fixed an issue where `/warnings` would display garbled/unreadable text for warning reasons
* Fixed an issue where warnings would instantly expire if the server had expiry test to "Never"
* Fixed several other misc. bugs related to new EF core system

# September 3rd - Censor Improvements
## Fixed
* Fixed some issues where strings would not be properly censored as well as fixing several false positives. (Mainly with AI chat bot)

# Aug 25th - Custom Embed Fix
## Fixed
* Fixed an issue with custom embeds including `+` symbols not being rendered properly

# Aug 23rd - Git Preview Label
## Changed
* Add "Delete Preview" label to the Git Preview button

# Aug 20th - Nickname Changed Updated
## Changed
* The "Nickname Changed" audit log event will now show _who_ changed the target user's nickname (if it wasn't the user themselves)

# Aug 19th - User Roles Updated
## Changed
* The "User Roles Modified" audit log event will now show _who_ changed the target user's roles
* The "User Roles Modified" audit log event now also supports listing multiple roles being added/removed at once (such as when bots bulk add/remove roles)

# Aug 14th - Fixed Lyrics
## Fixed
* Fixed `/lyrics` command

# Aug 12th - Server Timezones
## Fixed
* Fixed an issue with `/search lmgtfy` due to expired SSL certificate

## Added
* Added new `Server Timezone` setting on the web dashboard. Currently just affects when birthday announcements are sent on your server but it may also impact other features in the future.

# Aug 9th - Revoking Invites
## Added
* Added the ability to revoke new invite links via a button for audit log entries.

# Aug 5th - Leaderboard Vanity URLs
## Added
* Added the ability to set a custom vanity URL for your leveling/XP leaderboards! For example: https://cakeybot.app/leaderboard/caketropolis

# July 7th - Bug Fixes
## Fixed
* Fixed an issue where `/play` would show unknown error instead of the intended/proper error message
* Fixed an issue where certain auto responder content would have the data decoded/shown incorrectly
* Fixed a TON of random/misc bugs and errors throughout the entire bot

## Changed
* Re-enabled the auto-completer for the `/play` command

# July 2nd - Leveling Reward Placeholder
## Added
* Added new `{reward}` placeholder to mention the role a user earned by leveling up
* Added new "Announcement Message When Role Is Awarded" setting to set a custom message for leveling when a reward is granted to use the above placeholder in.

# June 30th - Warning Pings & New Audit Log Events
## Changed
* Warning logs will now ping the target user

## Added
* Added new URL shorteners to scan for anti-phishing
* Added 4 new audit log events:
  * Webhook Created
  * Webhook Updated
  * Webhook Deleted
  * Bot Added

# June 29th - Dedicated Punishment Channels
## Changed
* Audit logs for warnings now have a dedicated "Warning Output Channel" setting on the moderation dashboard page. (Previously sent to "User Modified" audit logs)
* Audit logs for timeouts now have a dedicated "Timeout Output Channel" setting on the moderation dashboard page. (Previously sent to "User Modified" audit logs)

# June 28th - New Auto Responder Flags + /editwarn
## Changed
* Updated the formatting for `/warn` to use a user mention and include username + user ID.

## Added
* Added new `/editwarn` command.
* Added 5 new auto responder flags:
  * Contains image attachment 
  * Contains video attachment
  * Contains audio attachment
  * Contains text attachment
  * Contains executable attachment

# June 26th - Warning Auto Punishments + Expiry Improvements
## Changed
* Warnings now use fancy emote buttons to display active/expired warnings rather than using strikethrough formatting.

## Added
* Added Warning Auto Punishments! You can now configure warnings to automatically punish users when they receive a specific number of warnings!

# June 23rd - Warnings V2!
## Added
* Added the ability for warnings to "Expire" and be "Soft Deleted"

# June 21st - New Thread Placeholders
## Changed
* Changed the `/hash <b6encode | b64decode | md5 | sha512>` command to `/base64 <encode | decode>`.
* Added an optional `softban` parameter to the `/ban` command.

## Added
* `{originalpostonly}` - Only trigger for the original post in a thread.
* `{commentsonly}` - Only trigger for messages that are a comment inside of a thread.

## Removed
* Removed the `/softban` command.

# June 15th - Misc. Fixes
## Fixed
* Pushed several misc. fixes

## Removed
* Removed `/meme` command due to technical issues with the API we use.

# June 13th - /movemsg Bi-Directional Support
## Added
* The `/movemsg` command can now move messages in either direction of the starting message. (Just use a positive OR negative number for the `additional-messages` parameter)

# June 12th - Starboard Released!
## Added
* Released starboards!

# June 9th - Tags V2
## Changed
* Upgraded `/tags create` and `/tags edit` to use modals instead of slash command input (You can now create multi-line tag content!)
* `/tags create <tag> <content>` is now just `/tags create`
* `/tags edit <tag> <content>` is now just `/tags edit <tag>`

## Added
* Added new `/tags info` to view the owner of a tag, the number of times its been used and whether it's enabled.
* Added usage stats to tags, you can now see how many times a tag has been used.

# June 5th - Voice Leveling
## Added
* Added Voice XP/Leveling! Your users can now earn XP voice being in voice channels in addition to sending messages. You can enable this feature on the dashboard (It's separate from regular leveling)
  * Premium users can set custom min/max XP for voice leveling. Default is randomized between 5 & 8 XP per minute.

# June 4th - Improved /movemsg
## Added
* Added the ability to move multiple messages at once with `/movemsg`. (Up to 10 at a time)

# June 3rd - Minor Fixes
## Fixed
* Fixed an issue where custom Join/Leave banners would display the default image due to Imgur issues.

## Added
* Added the ability for users to actually set a custom reason when opening support tickets via the default embed.

# June 2nd - Report Improvements
## Fixed
* "Warn User" and "Timeout User" now work properly on User/Message Reports

## Changed
* Moderator actions using the report buttons will now be logged/added directly to the report embed itself.

# May 29th - Voice Message Transcripts
## Added
* Cakey Bot can now transcribe voice messages! You can have it react to voice messages with a 🗒️, whenever a user clicks the notepad Cakey Bot will transcribe the message. If you have a premium server you can make Cakey Bot transcribe all messages.
* Cakey Bot can now moderate voice messages! Just flip the switch in the blacklist words section of the auto moderation dashboard.
* You can now have Auto Mod detect & delete Discord's new Markdown Header formatting on user's messages.

# May 27th - New Placehodlers, Accents & User Reporting!
## Changed
* Auto Mod timeout punishment will now include the 'source' in Discord's audit log reason
* Upgraded the `/radio` command to support over 8,000 radio stations! (Previously was limited to 6)

## Added
* Several new palceholders for auto responder and custom commands:
  * `{addrole:<id>}`
  * `{removerole:<id>}`
  * `{xp-add:<amount>}`
  * `{xp-remove:<amount>}`
* Implemented user reporting! You can now set a "Report Channel" on the moderation page of the dashboard and let user's send you reports via Discord's right-click context menu under "Apps->Report User/Message"
* Added two new "accents" for the Chat Bot AI. They are Valley Girl & Baby Talk.

# May 25th - New Placeholders
## Added
* Added two new AR/CC placeholders: `{createthread}` & `{pinmessage}`.

# May 21st - Git Previewer Fixes
## Fixed
* Fixed an issue that caused github file previews greater than 11 lines long to not embed.
* Fixed an issue that caused github file previews with a file extension longer than 4 characters to not embed.

# May 19th - Announcement System Rewrite & /perms Commands
## Fixed
* A bug that caused the Spotify autocompleter to fail when a song title exceeded 100 characters has been fixed.

## Changed
* We have rewrote our entire announcement system for Cakey Bot! You can checkout more on our wiki page [here](/feature/announcements).

## Added
* The new `/perms` command lets you manage permissions for Cakey Bot commands on the public bot, it does not function on White Label Bots. You can learn more about it in the [Command Perms](/moderation/command-perms) documentation page.

# May 16th - Chat Bot AI Accents
## Added
* Added the ability to change/set different accents for the Chat Bot AI! You can choose between these accents:
  * Default English
  * Australian accent
  * British Accent
  * Pirate Speak
  * L33T Speak
  * UWU Speak
  * Southern US accent
  * Slang language - using colloquial expressions and idioms, suitable for informal conversations among peers.
  * Abbreviated language - using shortened forms of words, such as "u" for "you" or "lol" for "laugh out loud."
  * Emoticon language - using emoticons or emojis to convey emotions or reactions.
  * Witty language - using puns, wordplay, or humorous expressions to entertain and engage users.
  * Binary Code


# May 15th - FREE Chat Bot AI
## Fixed
* The Chat Bot AI will also now send an error message when trying to use it in a server where it has not been enabled rather than silently failing.

## Changed
* In preparation for White Label bots, we have migrated @Cakey Bot over to a dockerized container system. We've fixed most of the issues we ran into but there could still be a few issues/bugs. Please report any bugs or issues that you notice over the next week so we can get them fixed!

## Added
* In addition this this, we also released the Chat Bot AI to ALL servers! Non-premium servers will now get a FREE 20 requests/month while premium servers will retain the current 500 requests/month. You can check out how to enable this feature on our wiki here: [https://wiki.cakeybot.app/en/feature/ai-chat-bot](https://wiki.cakeybot.app/en/feature/ai-chat-bot)

# May 9th - Leveling/QOL Role Rewards
## Fixed
* The `{level}` and `{user}` placeholders now work on the /manage-level & /manage-xp commands
* The `/manage-level` & `/manage-xp` commands now enforce the "Max Level" setting

## Changed
* Updated `/about` to include Cakey Bot's Twitter and Reddit profiles

## Added
* Added new "Role Rewards" for leveling/xp! You can now reward users with up to 10 roles as they level up!
* Added new "Max Level" setting for leveling/xp (Defaults to 999)
* Added new "Remove Role on Level Up" setting for leveling/xp which removes old role rewards when leveling up
* You can now set different colored background images for `/rank` profiles! This setting is currently guild-wide.

# May 7th - Thread Placeholders
## Added
* Added several new "Thread" placeholders for custom commands/auto responders:
  * `{thread.ownername}` - The dusplay name for the thread creator
  * `{thread.ownermention}` - A user mention for the thread creator
  * `{thread.isprivate}` - True/False if the thread is private or not
  * `{thread.members}` - The count for the number of members added to the thread
  * `{thread.parentchannelname}` - The name of the thread's parent channel
  * `{thread.parentchannelid}` - The ID of the thread's parent channel
  * `<#{thread.parentchannelid}>` - A channel mention for the thread's parent channel

# May 3rd - Auto Responder Regex Flag
## Added
* You can now use regexes in Auto Responders! This should give you more control and freedom when trying to match Auto Responder triggers compared to the Wildcard Contains flag.

# May 1st - Auto Mod Invite Fixes
## Fixed
* The invite filter has been entirely rebuilt, reducing false positives and catching some workarounds.

## Added
* Active members of our testing server now have a green bug badge on their `/rank` cards to thank them for helping evaluate @Cakey Bot

# April 30 - Minor Fixes
## Fixed
* The music autocompleter no longer fails when no input is provided.
* The music autocompleter no longer sometimes provides suggestions when a link is sent.
* The music autocompleter now properly returns erors to discord 
* The `/color` commands description no longer refers to purge commands

## Changed
* The `InviteCreated` and `UserJoined` audit log types now use discord timestamps, so the date/time auto adjusts to your region.

# April 23 - Music QOL Improvements
## Fixed
* The `/lyrics` command now works in some situations, a more complete fix is on the way.

## Added
* `/play` Now supports autocomplete! Just start typing and Cakey Bot will suggest songs you might want to play (for instance typing `/play query:Cryptid (m` will suggest `Cryptid (Mothman)`)

# April 21st - Evolving Premium Badges
## Changed
* The Premium badge on the `/rank` XP card will now progressively change over time the longer you have premium. This is similar to how Discord's boost badges work.

# April 19th - Code Preview Sources
## Added
* Added code preview for Gitlab and Codeberg, previously Github only.

# April 17th - Lyrics Fixes
## Fixed
* `/lyrics` no longer censors songs containing the words gay and lesbian and now censors songs containing some transphobic slurs 
* `/lyrics` now paginates songs that are too long to send in one embed; never again will you wonder the words to Dave's latest 7 minute 'masterpiece'

## Added
* Added custom colors for voice channel `join/leave/swap`.

# April 13th - New Placeholders
## Fixed
* `/query` now works on Java servers that block querying

## Changed
* `/query` now shows a green/red embed color depending on the server's status
* Increased `{choice}` placeholder item limit (10=>20)

## Added
* Added a new optional "compact" argument for the `/query` command
* Added several new placeholders for servers, users and channels on custom commands/auto responders:
**Servers:**
=> `{server.countstagechannels}`
=> `{server.countevents}`
=> `{server.countcategories}`
=> `{server.countstickers}`
=> `{server.ruleschannel}`
=> `{server.maxuploadlimit}`
**Channels:**
=> `{channel.isnsfw}`
=> `{channel.created}`
=> `{channel.position}`
=> `{channel.topic}`
=> `{channel.threadcount}`
=> `{channel.slowmodeinterval}`
**Users:**
=> `{user.ispending}`
=> `{user.timedoutuntil}`
=> `{user.isstreaming}`

# April 12th - Query Fixes
## Fixed
* The `/query` command is once again working!

## Changed
* The `/query` command no longer requires you specify a server protocol, it will auto detect the type.

# Aptril 4th - .NET 6 Upgrade
## Fixed
* `JSON` and `ANSI` file previews from github should now embed correctly 
* `/hash SHA256` no longer takes an insufferably long time to calculate

## Changed
* Cakey is now built on the Dotnet 6 framework, instead of Net Core App 3.1, this systemic change lets the bot run faster, adds new tools that will make development easier, and makes sure the bot will receive critical security updates in the coming years.

# Mar 31st - Premium Outage Fix
## Fixed
* Fixed an issue that caused a poorly timed Paypal api outage to expire valid premium subscriptions, all 6 affected users had the situation resolved for it by our staff.

# Mar 28th - QOL Improvements
## Changed
* When using `/warn` the success message will now include a "View Warnings" button to easily view a user's previous warn history with a single click!

## Added
* The GitHub previewer will now include a delete button on the code preview to keep the chat channel clean

# Mar 7th - Color Improvements
## Changed
* Slightly modified the layout/format for the `/color` command + added a "Name" property for the color

## Added
* `/color` now has a visual list of gradient/similar colors on an image banner

# Mar 1st - Rank Profile Badges
## Added
* Added rank profile badges for:
  * Cakey Bot Partners
  * Cakey Bot Translators
  * Cakey Bot Staff
  * Premium Users

# Feb 18th - Music Improvements
## Fixed
* Fixed an issue where all `/sortqueue` commands would just clear the entire queue.
## Changed
* Made some improvements to Spotify Playlist enqueuing.
## Removed
* Temporarily removed support for Apple Music URLs due to complications with parsing them.

# Feb 11th - /play Improvements
## Changed
* I've re-written the song loading system for `/play` and the search results should be a bit more accurate.

# Jan 31st - Birthday Auto Role
## Added
* You can now set an auto role for birthday users with the `/birthday role <role>` command that will temporarily assign the specified role to birthday users for 24h!

# Jan 26th - Custom Join/Leave Banner Fixes
## Fixed
* Fixed an issue where custom join/leave banners would display as the default banner regardless of the URL set.
* Custom join/leave banners should now automatically resize to the correct size.

# Jan 25th - Update Birthday Channel
## Added
* Added new `/birthday channel <channel>` to set/update the birthday channel.

# Jan 24th - Leveling Announcement Fix
## Fixed
* Leveling announcements should now be working again if you were using the default message.

# Jan 12th - Move Message Fix
## Fixed
* `/movemsg` now works with uploaded files/images

# Jan 9th - Birthday Announcements
## Added
* Added the ability for users to set their birthday and have them announced in the server! (Requested by @➳f0r4g3m0n#1583 )
* New commands: 
* `/birthday next <limit>` - View any upcoming birthdays.
  * `/birthday remove [user]` - Remove your birthday. (Or another user's birthday)
  * `/birthday set <date>` - Sets or updates your birthday.
  * `/birthday view <user>` - View a user's birthday. (If they have one set)

## Removed
* Removed `/convert` command

# Jan 7th - Suggestion QOL
* Updated `/suggestion` to use modals!

# Jan 3rd - DM Placeholder Change

## Changed
* Auto responders/custom commands that send a DM using the `{dm}` placeholder will now have a disabled button attached to them that reads `Sent from server: X` to inform users what server triggered the DM.
* Updated and improved several internal methods and fonts to support a wider array of usernames. (This change affects usernames that are displayed on join/leave banners, rank cards and XP leaderboards.)

# Jan 2nd - Leveling & XP Release!

## Added
* You can now grant your users XP while they chat and level them up!

* Features:
  * Set announcement location (current channel, DMs, custom channel, disabled)
  * Ability to set XP rate (0.25x up to 3x)
  * Ability to set NoXP/Ignored roles & channels
  * Ability to set a custom announcement message
  * Ability to set Min/Max XP per message (Premium only)
  * Ability to auto-remove roles when demoting a user

* Commands:
  * `/leaderboard` - View the top 10 users on the leaderboard & get a button to open the leaderboard for your current server
  * `/rank` - View your current level card
  * `/manage-xp` Ability to set, add or remove XP to/from a user.
  * `/manage-level` Ability to set, add or remove levels to/from a user.