---
title: Embed Builder
description: Design and save custom Discord embeds with Cakey Bot - Build rich embeds visually with sender profiles and reuse them across Auto Responder, Auto Messages, Announcements, and Verification.
published: 1
date: 2026-07-19T00:04:50.164Z
tags: 
editor: markdown
dateCreated: 2026-07-19T00:03:28.448Z
---

# Overview

The Embed Builder is a visual, Discord-style tool on the web dashboard for building rich embeds. Its live preview renders Markdown, resolves channel and role mentions to their real names and colors, shows custom emotes and timestamps, fills in your server's placeholders, and lays the message out with a sender's avatar and name exactly as Discord would - so what you see while building is what members actually see.

Once you've designed an embed, you save it to your server, and it becomes available to pick from a **Custom Embed** dropdown on other pages - [Auto Responder](/en/auto-responder#custom-embeds), [Auto Messages](/en/feature/auto-messages#custom-embeds), [Announcements](/en/feature/announcements#custom-embeds), and [Verification](/en/feature/verification-role#set-a-custom-verification-embed). Those pages preview a saved embed through this same renderer, so a preview elsewhere can never disagree with how it looked in the builder.

# Accessing the Embed Builder

1. Login to the [web dashboard](https://cakey.bot/dashboard).
2. Click on the server you want to create an embed for.
3. Go to the "Embed Builder" page in the sidebar.

# Designing Your Embed

Use the builder to set your embed's title, description, color, author, footer, fields, thumbnail, and image, and preview exactly how it will look in Discord as you go. You can add multiple embeds to a single message, and a plain text message body alongside them.

* **Emote picker** - a picker button next to the message content, embed description, and each field's name/value lets you insert a server custom emote or a standard emoji at your cursor.
* **Placeholder support** - the preview fills in your server's [placeholders](https://wiki.cakey.bot/en/placeholders) so you can see the real values while designing.
* **Raw JSON** - the "Export" button reveals the embed's underlying JSON, which you can edit directly and re-apply, if you'd rather write it by hand for a specific field.
* Leaving the page with unsaved changes prompts you to confirm first, so you don't lose your work by navigating away by accident.

> Discord's own limits apply and are enforced as you type: 2,000 characters for the message content, up to 10 embeds per message, 256 characters for a title, 4,096 for a description, up to 25 fields, 256 characters per field name, 1,024 per field value, 2,048 for the footer, 256 for the author name, and 6,000 characters total across everything in the message.
{.is-info}

# Sender Profiles

A Sender Profile is a display name and avatar you can send an embed under, instead of it appearing to come from Cakey Bot itself. Messages sent through a profile are delivered via a webhook the bot keeps in the destination channel, so they show up under the profile's own name and picture.

## Creating a Sender Profile

1. Open the Embed Builder and click **Manage** next to the sender profile picker.
2. Set a **Name** (up to 80 characters; names containing "discord" or "clyde" aren't allowed) and an **Avatar** URL (up to 512 characters).
3. Optionally set a **Webhook URL** of your own (up to 512 characters, must be a genuine Discord webhook URL).

> A server can have up to **25** sender profiles.
{.is-info}

## How Sending With a Profile Works

* **No webhook URL set on the profile:** when you send to a channel, Cakey Bot automatically creates (or reuses) a webhook it keeps in that channel and posts through it under the profile's name and avatar. You don't need to create anything yourself, but **the bot needs the Manage Webhooks permission** in the destination channel for this to work.
* **Webhook URL set on the profile:** that URL becomes the destination directly, and the channel picker is hidden - your message goes wherever that webhook points, which doesn't have to be a channel the bot can even see.

> Deleting a sender profile does not delete the webhook it sent through - the bot shares one webhook per channel across every profile that uses it, so other profiles sending to that same channel are unaffected.
{.is-info}

# Saving Your Embed

Once you're happy with your embed, use the Saved Embeds panel:

* **Save** - Saves your current embed, overwriting the one you have loaded, or creating a new saved embed if you started from scratch.
* **Load** - Switches to a different saved embed and loads it into the builder.
* **Rename** - Renames the currently loaded saved embed.
* **Delete** - Deletes the currently loaded saved embed.

> Any admin with dashboard access can see and select every saved embed on the server, not just their own - but only the person who created a saved embed can **Rename**, **Delete**, or overwrite it with **Save**. Everyone else can still pick it from the dropdown or save their own changes as a new saved embed.
{.is-warning}

> Servers are limited to **100 saved embeds** total, and each person is separately limited to **100 saved embeds** per server. A single save can contain at most **10 embeds**. Exact duplicate saves (identical embed content) are blocked.
{.is-info}

# Sending Your Embed Directly

If you just want to post the embed right now rather than attaching it to a saved embed elsewhere, click **Send Embed** in the Saved Embeds panel. This sends whatever is currently in the builder - you don't need to save it first.

A window will open letting you choose how to send it:

* **Channel** - Pick a channel from the dropdown and optionally a Sender Profile to send it as. Without a profile selected, it posts as Cakey Bot itself, and the bot needs **View Channel**, **Send Messages**, and **Embed Links** permissions in that channel - if it's missing any of them, you'll be told which one.
* **Webhook URL** - Toggle "Send to a webhook URL instead" to post the embed through a Discord webhook rather than the bot. Paste in the webhook's URL and the embed is sent as that webhook, without needing the bot to have any permissions in the destination channel.

> Sending an embed posts it immediately - there's no preview step after you hit Send. Double check the embed and destination first.
{.is-warning}

# Using a Saved Embed Elsewhere

Once an embed is saved, it appears in the **Custom Embed** dropdown on any page that supports custom embeds:

* [Auto Responder](/en/auto-responder#custom-embeds)
* [Auto Messages](/en/feature/auto-messages#custom-embeds)
* [Announcements](/en/feature/announcements#custom-embeds)
* [Verification](/en/feature/verification-role#set-a-custom-verification-embed) _(Custom Bot servers only)_

Just select it from the dropdown - no more copying and pasting a URL.

> Custom embeds will work with all **Basic Placeholders**. You can find the list of supported placeholders [here](https://wiki.cakey.bot/en/placeholders). Custom embeds will **NOT** work with the **Advanced Placeholders**.
{.is-info}
