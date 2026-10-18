---
title: Data Import
description: Move to Cakey Bot from MEE6, Lurkr, Polaris, Arcane, Amari, Tatsu or UnbelievaBoat - Import levels, XP, balances and MEE6 server settings from the dashboard, with undo.
published: 1
date: 2026-10-18T20:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-10-18T20:00:00.000Z
---

# Overview
Data import brings what your server built up on another bot over to Cakey Bot. Levels and XP come over from MEE6, Lurkr, Polaris, Arcane, Amari and Tatsu, balances from UnbelievaBoat, and a MEE6 export carries most of a server's settings. Every import shows a preview before anything is written, and can be undone for 24 hours.

> Only one import runs on a server at a time, and uploaded files are limited to **25 MB**.
{.is-info}

# Setup
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard) and select your server.
2. From the left sidebar, pick "Import".
3. Pick the source, give it what it needs (nothing, a file or a key), and start the import.
4. Check the preview, choose how the data is merged, and apply it.

# Sources
| Source | Brings over | What you need |
|---|---|---|
| MEE6 | XP, levels and level roles | Make the leaderboard public in MEE6's dashboard under Leveling. |
| MEE6 settings | Server settings, see below | The export from MEE6's dashboard, see below. |
| Lurkr | XP and levels | The JSON file from Lurkr's level export. |
| Polaris | XP, plus level roles and your curve with the Everything export | Download your XP from Polaris' website for your server. |
| Arcane | Member levels | Arcane has no export, so open the server's leaderboard on arcane.bot, scroll until every member is loaded, run the export script linked on the page in the browser console and upload the JSON it saves. |
| Amari | XP and levels | An Amari API key, applied for on amaribot.com and sent by DM, usually within a day. |
| Tatsu | XP only | Run `t!apikey create` in any channel and paste the key Tatsu sends you by DM. |
| UnbelievaBoat | Cash and bank balances | An application on UnbelievaBoat's site, authorized on your server from the application's page. |
| Other file | XP, levels or balances | Any JSON or CSV file with a user ID and an XP, level, cash or bank value per member. |

API keys are only used to read the data and are not stored.

# Levels and XP
The preview shows how many members come over and how many already have XP on Cakey Bot. Before applying you choose:

* **Merge mode** ~ Replace what members have, keep whichever is higher, or add on top of what members have.
* **Skip members below level** ~ Members under this level are left out. 0 keeps everyone.
* **Level curve** ~ Each bot works out levels from XP differently. Either the XP is converted to your server's curve so every member keeps their level and progress, or you switch the server to the source's curve and members keep their XP numbers as they were.
* **Import level roles** ~ When the source has level roles, the same roles are set for those levels here, replacing any role already set on them. Roles that no longer exist are skipped.

# Balances
UnbelievaBoat balances come over as cash and bank. The same three merge modes apply, and balances above your server's maximum balance are lowered to it.

# MEE6 Settings
The MEE6 settings import reads an export made on your server's MEE6 dashboard. The export is made by your own browser with the MEE6 login it already has, so nothing is shared with Cakey Bot except the settings file.

> This step needs a desktop browser. Phones and tablets cannot run bookmarks or the console on the MEE6 dashboard.
{.is-warning}

1. On the import page, pick "MEE6 settings". The page gives you an "Export from MEE6" bookmark and the same script to copy.
2. Drag the bookmark onto your bookmarks bar, or right-click it and bookmark the link.
3. Open your server's dashboard on mee6.xyz and click the bookmark, or paste the script into the browser console there (Ctrl+Shift+J, or Cmd+Option+J on a Mac).
4. The settings are sent straight to the import page, which carries on by itself. If that does not happen, the script also downloads the file, and you can upload it on the page.

The link in the bookmark only works for 10 minutes, so take a fresh copy each time you import.

You then pick the sections to bring over:

| Section | What comes over |
|---|---|
| Server | The server's time zone. |
| Welcome and goodbye | Welcome and goodbye messages, the welcome embed and join roles. Cakey Bot sends one welcome message, so when MEE6 had both a channel message and a DM, the channel message is kept. |
| Level settings | XP rate, level up message and where it goes, level roles, no XP roles and channels, and the level curve when no member has XP here yet. |
| Birthdays | Birthday channel, role and message. |
| Custom commands | Each command becomes an auto responder. |
| Reaction roles | Each message becomes a self role panel with its roles as buttons, posted as a new message. |
| Auto-moderation | Word, invite, link, mention and spam filters, the repeated text, caps, emoji, spoiler and zalgo checks, ignored roles and channels, and the warning punishments. |
| Twitch alerts | Followed streamers and the channel they are announced in. |
| Economy | The currency symbol, the shop and XP boosts. |
| Audit log | Which log types are on. MEE6 does not share its log channel, so you pick one per log type afterwards. |
| Embeds | Saved embeds, kept as your embeds on Cakey Bot. |
| Automations | Automations started by a message containing some text become auto responders. |
| Achievements | Trophies become achievements, with the unlock announcement channel and message. |
| Feeds | YouTube, Reddit and RSS subscriptions become social feeds. |
| Timers | Timed messages become auto messages on the closest schedule Cakey Bot offers. |

After the import, each section reports what was brought over and what was left out. Some rules apply to everything:

* Items past your plan's limits are imported switched off, with a note saying how many. Nothing is dropped.
* Names already in use on Cakey Bot, and settings that point at channels or roles that no longer exist, are skipped.
* Before the import, the page warns about roles above the bot's highest role and channels it cannot post in, so you can fix the bot's permissions first.
* Embeds only send on premium servers, so they are saved and used once the server has premium.

# Undo and History
The import history lists the last 25 imports with what each one changed. The latest import of each kind (levels, balances or settings) can be undone for **24 hours**. Undo puts everything the import changed back to how it was, and anything earned or changed since is lost.
