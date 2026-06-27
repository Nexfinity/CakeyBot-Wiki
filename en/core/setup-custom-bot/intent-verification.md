---
title: Custom Bot Intent Verification
description: A short guide to help you answer the privileged intent verification application for custom bots.
published: 1
date: 2026-06-27T12:52:13.792Z
tags: 
editor: markdown
dateCreated: 2026-06-11T22:04:47.406Z
---

> **Note:** This only affects custom bots that have more than 10,000 unique users across all servers it is in combined. If your bot does not have this many users then you can disregard this page.
{.is-warning}

# Overview
> **Note:** Unless Discord changes it at a later date, you will have to keep re-verifying your bot once a year, so please keep a link to this guide for future applications. If you forget the link, you can always reach out to our [support team](https://cakey.bot/support).
{.is-info}

TBD

# Form Fill-Out Guide
> **Note:** This guide does NOT guarentee your application will be accepted. This guide should be sufficient for Discord to approve it, however, at the end of the day the application is decided on by Discord. If you run into complications or followup questions from Discord, please reach out to our [support team](https://cakey.bot/support).
{.is-danger}

Discord has a fairly straight forward application form which will ask various questions. For select menus, select the option suggested by this guide and for any text input sections you can copy/paste the text directly from the code-blocks provided in this guide. This guide should be laid out in the same order as Discord's application form.

## Application Details
```
This application is a custom bot variant of Cakey Bot (https://cakey.bot). The bot's main/primary features include:
AFK Messages - Allow users to set an AFK message so other users know when someone is AFK and when they'll be back.
Audit Log - Advanced log for all actions performed on your Discord server and users.
Announcements - Customizable join/leave/ban/kick messages.
Auto Moderation - Advanced and fully configurable via our web dashboard.
Auto Quoter - Automatically quote Discord messages in when a URL is posted in a channel.
Auto Responder/Custom Commands - Have Cakey Bot respond to custom text triggers or commands using powerful placeholder variables.
Games - Cool games to make your server fun and entertain your players.
Giveaways - Host giveaways and reward your users with fancy prizes!
Leveling/XP - Level up your users and grant roles for their efforts!
Moderation - Contains powerful moderation tools to keep your server in check and running smoothly.
Music - Play music from popular web sources, Direct URL/Web File and Spotify in your server.
Reminders - Useful to way to remember a list of stuff to do directly in Discord.
Roleplay - A variety of commands that are great for roleplay servers.
Role Management - Easy to use commands to update and manage the roles in your server.
Social Feeds - Monitor events and social feeds for popular services like Twitch, Reddit and more!
Starboard - Star messages to save them to your starboard. Promote funny messages and encourage user activity/discussions.
Support Tickets - Provide easy 1on1 support between your users and staff team using private ticket channels! You can even save transcripts of closed tickets.
Tags - Create tags that anyone in your server can use or even allow users to create their own tags.
Text & Image Manipulation - Various commands to modify and manipulate text strings & images.
Verification Role - Useful feature to help prevent raids and bot attacks on your Discord.
```

## Do you have a public Privacy Policy telling your users about their data usage?
Select **Yes**

### Where is your Privacy Policy available?
```
In the bot's bio & the `/help` command.
```
> **Note:** The privacy policy is required to be listed somewhere publicly, this is a Discord limitation and not something we can get around. Discord typically requires it to be in the bot's bio. If you do not want to link to Cakey's website directly, you could copy/paste our entire privacy policy onto your own website, [Github gist](https://gist.github.com/), or similar text format that Discord accepts and use that instead. Note that using other listings for it may affect verification approval or require changes asked by Discord's support team.
{.is-info}

### Please share a link to your Privacy Policy.
```
https://cakey.bot/privacy
```

## Privileged Gateway Intents
Select/check both of these intents:
* Server Members Intent
* Message Content Intent
> Do **NOT** select the presence intent. Cakey Bot does not require it and it will increase the chance of the application getting denied if you have this selected.
{.is-danger}

## Server Members Intent
### Why do you need the Guild Members intent?
```
Join/Leave Announcements - Sending custom embeds/image banners for user join/leave notifications
Audit Logs/Moderation - Audit logging for potential malicious users (i.e. malicious links/invites in profile data), abusive nickname moniotoring.
User leaderboards for xp/leveling/economy/fishing/streaks - Displaying user info (such as username/nickname & profile pictures) on image-based leaderboard rankings for various features
Achievements - Allows granting achievements for certain triggers that require user profile information.
```
### Please provide links to screenshots and/or videos that demonstrate your use case
```
https://cdn.cakey.bot/Intent%20Verification/announcements.jpg
https://cdn.cakey.bot/Intent%20Verification/auditlogs.png
https://cdn.cakey.bot/Intent%20Verification/automod.jpg
https://cdn.cakey.bot/Intent%20Verification/leveling.png
```
### Are you storing any API Data off-platform (outside of Discord)?
Select **Yes**

### Are you storing API Data for 30 days or less?
Select **No**

### How do users contact you to request deletion of their activity data?
```
They can contact the Cakey Bot support team and request deletion. They can also send an email to support@cakey.bot if they prefer an off-platform method. Links to our support Discord can be found on the main website (https://cakey.bot) or via the `/help` command.
```

### Are you encrypting the data that you store at rest, as is required by our developer policy?
Select **Yes**

## Message Content Intent
### Can users opt-out of having their message content data tracked?
Select **No**
### Are you storing message content data off-platform (outside of Discord)?
Select **No**
### Will the message content data be used to train machine learning or AI Models?
Select **No**
### Why do you need the Message Content intent?
```
Auto Quoter/Git Preview - Allows users to paste a message link or github/gitlab url and Cakey Bot will embed a preveiw in the chat. (Has anti abuse limitations for message quoter to prevent sharing in external servers)
Auto Moderation/Anti-Raid - Cakey Bot monitors chats and messages for content that violations a server's word blacklist, malicious links, files or other relaterd spam or malicious content.
Honeypot/Anti-Phishing - Allows Cakey Bot to monitor for phishing content to delete it (i.e. MrBeast scam images)
Auto Responder/Custom Commands - Let's server setup custom responses/triggers based on message content
AI Chat Bot (opt-in) - Allows users to opt-in to use Cakey Bot's AI Chat Bot feature. Allow scope to a specific channel and perserves a temporary 2 message history that gets purged automatically.
Category Content Restrictions - Auto Mod feature that monitors message/file content in specific channels to enforce specific rule-sets (such as GIF-only channels or Spotify only links)
Emoji Stats - Cakey Bot reads messages for emojis and saves an incrementing count of emoji usage. (Does not store message/userids, only emoji+count)
Leveling/XP - Cakey bot monitors messages to allow users to earn XP for different types. Message content is required to give varying amounts of XP based on message type and for anti-abuse/spam purposes.
Role Mention cooldowns - Cakey bot can monitor messages that ping specific roles and disable role mentions for specified cooldown amount to prevent spam abuse.
Starboard - Ability for users to react and pin message content to a dedicated channel.
```
### Please provide links to screenshots and/or videos that demonstrate your use case
```
https://cdn.cakey.bot/Intent%20Verification/auditlogs.png
https://cdn.cakey.bot/Intent%20Verification/auditlog-message.jpg
https://cdn.cakey.bot/Intent%20Verification/auotquoter.png
https://cdn.cakey.bot/Intent%20Verification/auto-responder.jpg
https://cdn.cakey.bot/Intent%20Verification/automod.jpg
https://cdn.cakey.bot/Intent%20Verification/git-preview.png
https://cdn.cakey.bot/Intent%20Verification/honeypot.jpg
https://cdn.cakey.bot/Intent%20Verification/leveling.png
https://cdn.cakey.bot/Intent%20Verification/starboard.png
```
## Acknowledgement
Select/check this.

> **Note:** While this should be sufficient for most/all applications/bots, Discord support staff may ask additional or followup questions or request certian changes. If they do, pelase reach out to our support team for assistance.
{.is-info}