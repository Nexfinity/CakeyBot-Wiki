---
title: Embed Editor
description: Design and save custom Discord embeds with Cakey Bot - Build rich embeds visually and reuse them across Auto Responder, Auto Messages, Announcements, and Verification.
published: 1
date: 2026-07-19T00:04:50.164Z
tags: 
editor: markdown
dateCreated: 2026-07-19T00:03:28.448Z
---

# Overview

The Embed Editor is a visual, Discord-style tool on the web dashboard for building rich embeds. Once you've designed an embed, you save it to your server, and it becomes available to pick from a **Custom Embed** dropdown on other pages — [Auto Responder](/en/auto-responder#custom-embeds), [Auto Messages](/en/feature/auto-messages#custom-embeds), [Announcements](/en/feature/announcements#custom-embeds), and [Verification](/en/feature/verification-role#set-a-custom-verification-embed).

> This replaces the old workflow of copying a generated URL and pasting it into an "Embed URL" text field. Embeds are now saved to your server and picked from a dropdown instead.
{.is-info}

# Accessing the Embed Editor

1. Login to the [web dashboard](https://cakey.bot/dashboard).
2. Click on the server you want to create an embed for.
3. Go to the "Embed Editor" page in the sidebar.

# Designing Your Embed

Use the editor to set your embed's title, description, color, author, footer, fields, thumbnail, and image, and preview exactly how it will look in Discord as you go. You can also add multiple embeds to a single message, and switch to a raw JSON editor if you'd rather write the embed JSON directly.

# Saving Your Embed

Once you're happy with your embed, use the **Saved Embeds** panel at the top of the editor:

* **Save** — Overwrites the currently selected saved embed with your changes.
* **Save As New** — Saves your current embed as a brand new entry, without touching whichever one you had selected.
* **Rename** — Renames the currently selected saved embed.
* **Delete** — Deletes the currently selected saved embed.

Use the dropdown at any time to switch to a different saved embed and load it back into the editor.

> Any admin with dashboard access can see and select every saved embed on the server, not just their own — but only the person who created a saved embed can **Rename**, **Delete**, or overwrite it with **Save**. Everyone else can still pick it from the dropdown or clone it with **Save As New**, which creates a new saved embed owned by them.
{.is-warning}

> Servers are limited to **100 saved embeds** total, and each person is separately limited to **100 saved embeds** per server. A single save can contain at most **10 embeds**. Exact duplicate saves (identical embed content) are blocked.
{.is-info}

# Sending Your Embed Directly

If you just want to post the embed right now rather than attaching it to a saved embed elsewhere, click **Send Embed** in the Saved Embeds panel. This sends whatever is currently in the editor — you don't need to save it first.

A window will open letting you choose how to send it:

* **Channel** — Pick a channel from the dropdown and the bot will post the embed there. The bot needs **View Channel**, **Send Messages**, and **Embed Links** permissions in that channel — if it's missing any of them, you'll be told which one.
* **Webhook URL** — Toggle "Send to a webhook URL instead" to post the embed through a Discord webhook rather than the bot. Paste in the webhook's URL and the embed is sent as that webhook, without needing the bot to have any permissions in the destination channel.

> Sending an embed posts it immediately — there's no preview step after you hit Send. Double check the embed and destination first.
{.is-warning}

# Using a Saved Embed Elsewhere

Once an embed is saved, it appears in the **Custom Embed** dropdown on any page that supports custom embeds:

* [Auto Responder](/en/auto-responder#custom-embeds)
* [Auto Messages](/en/feature/auto-messages#custom-embeds)
* [Announcements](/en/feature/announcements#custom-embeds)
* [Verification](/en/feature/verification-role#set-a-custom-verification-embed) _(Custom Bot servers only)_

Just select it from the dropdown — no more copying and pasting a URL.

> Custom embeds will work with all **Basic Placeholders**. You can find the list of supported placeholders [here](https://wiki.cakey.bot/en/placeholders). Custom embeds will **NOT** work with the **Advanced Placeholders**.
{.is-info}
