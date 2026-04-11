---
title: Changelist 2026
description: Cakey Bot update history - New features, bug fixes, improvements for Discord. Complete version changelog and release notes.
published: 1
date: 2026-04-11T18:24:01.317Z
tags: 
editor: markdown
dateCreated: 2026-01-13T22:54:52.663Z
---

# April 11th - Bug Fixes & QOL Features
## Fixed
* Fixed an issue where join/leave announcements would default to "AV" icon for users who didn't have a profile picture set.
* Fixed an issue where some embed URLs would fail to parse.
* Fixed an issue where editing achievements would throw errors or let you change the type.
* Fixed an issue where the progress was displayed incorrect for custom/manual achievement types.
* Fixed an issue where auto messages and auto responders would incorrectly display an embed being set on them when it wasn't.
* Fixed an issue where you couldn't cancel active subscriptions
* Fixed an issue where all subscriptions were listed as "Premium" even if they were not.
* Fixed the "Update Payment Method" button on the "Manage Subscriptions" page.
* Fixed an issue where the custom bot page would incorrectly prompt you to setup a custom bot you didn't have yet.

## Changed
* Migrated to GPT-Image-1.5 instead of DALL-E due to DALL-E being deprecated on May 12th.
* The "Manage Subscriptions" page now displays old/cancelled subscriptions.
* The custom bot setup wizard now includes a button to invite the bot on the final page.

## Added
* Added a check to the Twitch OAuth settings page that checks when your granted OAuth scopes mismatch from Cakey's currently required ones and prompts you to re-link.
* Added a search, sort and filter system to the Server Discovery system on the website.
* Added additional info/properties for servers (such as displaying server's banner & icons for enabled features on the main page)
* Added the ability to remove scheduled cancellations on the "Manage Subscriptions" page.
* Added server owner name/profile picture to server discovery pages.

# April 7th - Server Discovery
## Added
* Due to popular request, Cakey Bot has now created a "Server Discovery" system for servers that use Cakey Bot! You can view servers here: <https://cakey.bot/discovery>
  * Note: No servers are visible due to none being accepted _yet_.
  * Applications are open and will be processed over the next few days, can apply within the dashboard here once you select a server to manage: <https://cakey.bot/dashboard/discovery>
  * Servers MUST utilize cakey bot and keep Cakey Bot in the server.
  * Server Discovery will display things like server name, icon, invite join link, popular features utilized in cakey bot, links to leaderboards, and more!
  * Ranking is purely randomized (and cached for 6h), searching/filtering coming soon.
  * This is a very early release and we will continue to iterate and improve it based on user feedback.

# April 6th - New Achievement Reward Options
## Added
* Added new reward options for achievements:
  * Remove Leveling XP
  * Add/Remove Economy Money 

# April 5th - Leveling QOL Features
## Changed
* Increased mention cooldown limits.
* Split the Ignore Muted toggle for voice leveling XP into two options (Ignored Muted & Ignore Deafened)

## Added
* Added the ability to have XP decay immunity roles that you can give to users.
* Added additional context to the AI chat bot. (i.e. who the bot is chatting with)
* Added the `/setup reset-all-streaks` command to reset ALL user streaks in the server. (For fairness sake, you can NOT reset specific user's streaks.)
* Added the option to give bonus XP for image and video files on messages.
* Added a toggle for level up messages to ping users.
* Added a toggle for support ticket logs to ping users.
* Added Ignored Channels for Audio Transcripts.
* Added Ignored Channels for Auto Quoter.
* Added Ignored Channels for Git Code Previewer.

# April 4th - Random XP Drop Anti-Abuse
## Added
* Added ignored roles setting for streaks.
* Added some anti-abuse/anti-bot features to Random XP Drops including:
  * Toggle to prevent the same person from claiming a drop back to back
  * Toggle to add randomized button placements

# April 2nd - Random XP Drop Multi-Channel Support
## Added
* Added the ability to select multiple channels for the random XP drops. (Bot will randomly select one channel from the list every time a drop is sent. This helps decrease/discourage auto-clickers/botting)

# March 28th - Gist Support & Random XP Drops
## Added
* Added gist support to the git previewer.
* Added new 'Nord' theme for the website.
* Added the "Specific Role Count" stat channel type.
* Released new "Random XP Drop" system for leveling. (Previously known as the Holiday XP Drop system)

# March 21st - Streaks Leaderboard
## Added
* Added new streaks leaderboard to website.

# March 19th - Website Improvements
## Added
* Added new dedicated page for listing and managing your premium/custom bot subscriptions on the dashboard. You can view/cancel subscriptions or update your payment method easier now. (Lifetime purchases should also be listed too)
* Added new fishing leaderboard to the leaderboard pages. (buttons soon to be added into the bot for quick linking too)

# March 6th - RSS Improvements
## Changed
* Reworked RSS feed processing, now allowing feeds to fail few times before getting disabled to account for network errors or temporary outages.

# February 9th - Audit Log Improvements
## Added
* Added the type of channel created that was created to the channel created audit log event.
* Added unique properties for voice and forum channel types to the channel modified audit log event.

# January 13th - Misc Bug Fixes
## Fixed
* Fixed a TON of random/misc bugs and issues that have appeared over past 3 months or so.