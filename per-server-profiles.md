---
title: Per-Server Profiles
description: Give Cakey Bot a custom nickname, avatar, and banner in a single Discord server without affecting any other server.
published: 1
date: 2026-07-14T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-07-14T00:00:00.000Z
---

# Overview
**Per-Server Profiles** let you customize how Cakey Bot appears in a single server — its nickname, avatar, and banner — without changing how it looks in any other server. This is great for servers that want the bot to match their branding or theme without needing to run a fully separate Custom Bot.

> Per-Server Profiles is a [Custom Bot](/en/core/setup-custom-bot) feature. See the full feature comparison [here](https://cakey.bot/premium).
{.is-info}

# Accessing Per-Server Profiles
1. Open the [web dashboard](https://cakey.bot/dashboard) and select your server.
2. Click "Server Profile" in the left sidebar.
3. Make your changes and press "Save Changes" to apply them.

Changes apply immediately and only affect the bot's appearance in that server.

# What Can Be Customized

## Nickname
Override the bot's display name in this server. Nicknames can be up to 32 characters. Leave the field empty (or check "Clear nickname") to use the bot's default name.

## Avatar
Upload a custom avatar shown only in this server. Accepted formats are PNG, JPEG, GIF, and WebP, with a maximum file size of 256 KB. Use "Remove current avatar" to revert to the bot's default avatar.

## Banner
Upload a custom banner shown on the bot's profile in this server. Accepted formats are PNG, JPEG, and WebP, with a maximum file size of 512 KB. Use "Remove current banner" to revert to the bot's default banner.

# Notes
* Per-Server Profiles require `Manage Server` or `Administrator` permission (or granted [Dashboard Access](/en/core/dashboard-access)) to configure.
* Settings are stored per-server, so the same bot can look different across every server it's in.
* Clearing a field (nickname, avatar, or banner) reverts only that field to the bot's default — the other customized fields are unaffected.

# Related Commands
There are no slash commands for this feature — it is configured entirely through the web dashboard.
