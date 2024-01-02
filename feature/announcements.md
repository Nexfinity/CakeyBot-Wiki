---
title: Announcements
description: 
published: 1
date: 2024-01-02T10:14:57.473Z
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

# Message Announcements

You can set/modify messages and the announcement channel via our [web dashboard](https://cakey.bot/dashboard/public/). Just log in, select a server, and head on over to the "Announcements" page. Once here you can select a channel as well as setting the custom message. You can set a message for any one of these events, some of them or all of them. You can also set different channels for each event type.

> In order to have Cakey Bot send the messages, you will have to set a channel for Cakey Bot to post to. You can find more information about this below.
{.is-info}

# Image/Banner Announcements

You can also use a fancy banner picture for your join/leave announcements too! In order to set an image banner as your join/leave message just toggle the "Image Banner" setting to enabled. You can also choose a custom banner image to use if you have a [premium subscription](https://cakey.bot/premium.php). Custom banners must be uploaded to [PostImg](https://postimg.cc/) and the PostImg URL can then posted in the "Banner Background Image" field.

Default join/leave banner images:
![](https://cdn.discordapp.com/attachments/690401612254019625/1031874617456996392/unknown.png)

# Embed Announcements

Premium users can also set a custom embed for join/leave announcements too! To set a custom embed you will need to go to our embed editor located [here](https://cakey.bot/dashboard/public/embed-editor). Once you have designed a custom embed, you can copy the URL and paste it into the "Embed URL" field on the announcements page.

# Placeholders

Announcements will work with all **Basic Placeholders**. You can find the list of supported placeholders [here](https://wiki.cakey.bot/en/placeholders).

> Announcements will **NOT** work with the **Advanced Placeholders**.
{.is-warning}