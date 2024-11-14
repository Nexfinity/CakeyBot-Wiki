---
title: Announcements
description: 
published: 1
date: 2024-11-14T21:25:35.626Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:18:12.467Z
---

# Overview

Cakey Bot can automatically post custom messages when users join/leave or are banned. You can have Cakey Bot announce for one or all of these events and set different messages (or image banners) for each event.

# Enable/Disable Announcements

In order to start posting announcements, you will need to designate a text channel as the announcement channel. You can do this by setting it in the [web dashboard](https://cakey.bot/dashboard/public/). In order to disable announcements, simply select "None" instead of a specific channel in the dropdown.

Supported announcement event types:
* User Joined
* User Left
* User Banned
* User Boosted the server

> Cakey Bot will need access to Send/Read messages in the channel you designate for announcements. Cakey Bot may also require **`Use External Emoji`** permission if you include external emojis in the announcement messages.
{.is-warning}

# Send as DM Toggle
You can also toggle an option called "Send as DM". When enabled this setting will attempt to send any configured message, image and embeds via the user's DMs. This setting is separate from the regular channel sending, this means it can can be configured in any of these 3 ways:
* Send message only in server channel
* Send message only in DM
* Send message in DM & in channel

Note: DMs for the user leave event will likely fail 90% of the time due to the user likely no longer sharing any servers with Cakey Bot.

> Due to Discord limitations DMs will sometimes fail to send to users and should not be considered guarenteed to be sent. For example, some user's privacy settings may block randfom DMs from bots, or the user may have the bot blocked.
{.is-warning}

# Message Announcements

You can set/modify messages and the announcement channel via our [web dashboard](https://cakey.bot/dashboard/public/). Just log in, select a server, and head on over to the "Announcements" page. Once here you can select a channel as well as setting the custom message. You can set a message for any one of these events, some of them or all of them. You can also set different channels for each event type.

> In order to have Cakey Bot send the messages, you will have to set a channel for Cakey Bot to post to. You can find more information about this below.
{.is-info}

# Image Banner Announcements

You can also use a fancy banner picture for your join/leave announcements too! In order to set an image banner as your join/leave message just toggle the "Image Banner" setting to enabled. [Premium](https://cakey.bot/premium.php) servers also have access to a wider selection of image banners for their announcements.

Default join/leave banner images:
![](/announcements2.png)

Our fancy image banner editor:
<image src="/image_(25).png" width="800px">

# Custom Embeds

> Using custom embeds on announcements is a [**Premium Only**](https://cakey.bot/premium.php) feature.
{.is-warning}

You can include an optional embed on announcements by following the steps below:

1. Login to the dashboard.
2. Use our [custom embed editor](https://cakey.bot/dashboard/public/embed-editor) to design your embed.
3. Copy your browser URL or click the "**Get Data Link**" button in the dropdown menu and copy the URL from there.
4. Paste the URL you copied in the last step into the **Embed URL** text field.

> Custom embeds will work with all **Basic Placeholders**. You can find the list of supported placeholders [here](https://wiki.cakey.bot/en/placeholders). Custom embeds will **NOT** work with the **Advanced Placeholders**.
{.is-info}

# Placeholders

Announcements will work with all **Basic Placeholders**. You can find the list of supported placeholders [here](https://wiki.cakey.bot/en/placeholders).

> Announcements will **NOT** work with the **Advanced Placeholders**.
{.is-warning}