---
title: Auto Moderation
description: Discord auto moderation bot - Spam filters, raid protection, content blocking with Cakey Bot. Complete security setup guide.
published: 1
date: 2025-11-01T06:20:30.792Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:10:13.844Z
---

# Overview

Auto Moderation allows Cakey Bot to automatically detect rule breakers and punish them automatically even while your moderators are offline or busy! Auto Moderation can detect anything from spam, inappropriate content, and even zalgo text.

# Setup

> You will need **`Manage Server`** or **`Administrator`** permission to manage servers and setup Auto Moderation.
{.is-warning}

> You can also grant specific users or roles dashboard access without requiring Manage Server or Administrator. See [Dashboard Access](/en/core/dashboard-access) for details.
{.is-info}

1. Login to the web dashboard on the [main website here](https://cakey.bot/dashboard).
2. Click on the server you want to edit custom commands on.
3. Go to the "Auto Moderation" page.
4. You can then customization how Auto Moderation works in your server. Including which checks/rules are applied and their thresholds.

# Features

* Blacklist file extensions
  * Can also be inverted into a **whitelist mode**, only allowing the listed extensions instead of blocking them.
* Capitalization check
* Duplicated text
* Duplicated words
* Word Blacklist
  * Can also optionally check blacklisted words in **voice channel transcripts**, not just text messages.
* Discord invite URLs
  * Includes an option to whitelist/ignore invites from **partnered** and **verified** Discord servers.
* Any URL/Link (+Whitelist specific URLs)
* Mass mentions
* Mass emoji
* Has Spoilers
* Self bot detection
* Auto-Dehoist nicknames
* Scam Link Detection
* Stickers detection
* Zalgo detection
* Phishing URL Detection
  * **NOTE:** This feature is only to help block malicious URLs while allowing "safe" URLs. While we constantly try to improve its accuracy, it will NOT block every unsafe URL. You will still need to manually review some URLs.
  * **Note:** We now include a blacklisted image hash database. This will actively try to block known phishing related images that bypass traditional text moderation bots/tools.
  * **Note:** The image similarity threshold (0.01–1.0) is configurable on the dashboard. Lower values require near-exact matches (fewer false positives); higher values are more lenient and may catch more image variants.
* Markdown Headers
* Phone Number Detection
  * Fully configurable check to detect and act on messages containing phone numbers.

# Ignored Roles/Channels

Most Auto Moderation checks can be configured to skip specific roles and channels, letting you exempt trusted roles or non-monitored channels from moderation checks entirely.

# Excluding Admins/Mods/Bots

Cakey Bot lets you toggle whether Admins, Mods, and/or Bots should be excluded from Auto Moderation checks entirely, so trusted roles/accounts aren't accidentally punished.

# Punishment Types

1. Delete Message
2. Delete Message & Warn User
3. Warn User
4. Delete Message & Kick User
5. Delete Message & Kick + Warn User
6. Ban User (Delete 24h)
7. Delete Message & Timeout User

# Category Specific Channels

Cakey Bot allows you to define category channels. This means Cakey Bot will automatically delete messages that do not fit the category you set on the channel. For example, if you set a channel to only allow GitHub URLs, Cakey Bot will delete every message that isn't a GitHub URL posted in that channel.

You can view a list of category channels you can configure below:

* YouTube URLs Only
* Spotify URLs Only
* Reddit URLs Only
* Twitter URLs Only
* GitHub URLs Only
* Videos Only
* Images Only
* GIFs Only
* Files Only
* Emotes & Stickers Only
* Counting Only
* Links Only

# Auto Kick/Ban
Cakey Bot also allows you to automatically kick or ban users when they join your server if certain conditions are met. This can help you automatically combat specific types of bot attacks if all of the attacking users meet the criteria. 

> Keep in mind these options are not intended to always be enabled as they can impact real users, however, they can be useful to combat certain types of bot/raid attacks. Especially if used in addition to regular auto moderation settings.
{.is-info}

You can automatically kick or ban users when they join if they meet any of the criteria below:
* Numeric Only Usernames
  * This will automatically kick ban users whose entire username is nothing but numbers (for example: `534534534534`) as this is a commonly used naming scheme for some raids.
* Invite in Username
* Unverified Bots
* New Accounts (1 Hour Old by default)
* No Avatar

You can even set a threshold for how old the user's account must be before the 'New Accounts' detection gets triggered.