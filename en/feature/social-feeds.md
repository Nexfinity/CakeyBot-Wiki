---
title: Social Feeds
description: Social media feeds with Cakey Bot - Twitch, YouTube, Reddit, RSS integration. Automated content sharing setup guide.
published: 1
date: 2026-07-26T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:18:44.517Z
---

# Overview

Cakey Bot has the ability to send live updates and notifications to specific channels using web hooks. While Cakey Bot only supports a few official sources, you can suggest less-common feeds for us to look into adding though! You can set up these feeds via the "Social Feeds" page on the [web dashboard](https://cakey.bot/dashboard).

> **Note:** Non-premium servers are limited to **1 enabled feed** for each of Twitch, YouTube, and RSS. Reddit feeds require a [premium subscription](https://cakey.bot/premium) entirely (see below). Upgrading to premium removes these caps.
{.is-info}

> **Note:** This page covers Twitch live-stream notifications only. For full Twitch event integration including subscriber/follower/donation events, see the [Twitch Integration](/en/integrations/twitch) page.
{.is-info}

# Setup/Add Feeds

1. Login to our [web dashboard](https://cakey.bot/dashboard).
2. Go to "Social Feeds".
3. Click the tab for the feed you want to add (i.e. Reddit, Twitch, etc)
4. Click the "Add New Feed" button
5. Fill in the required information. All feeds will require a channel ID and a web hook URL for that channel in order to post messages there. You can read how to create a web hook URL [here](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks).
   1. You can optionally set a custom embed color and a role to ping for new notifications.
   2. You can also optionally set a Discord Thread ID, which will make notifications post into that specific thread instead of the channel itself.
6. Click "Create"

> **Note:** It can take _up to_ 5 minutes for modifications/additions to sync with the bot. After that, most feeds will search for new content/events every 10 seconds to 1 minute depending on the feed type and rate limits.
{.is-info}

# Custom Messages
Every feed type (Twitch, YouTube, Reddit, and RSS) supports an optional **Custom Message**, configurable per-feed on the [web dashboard](https://cakey.bot/dashboard). When set, this text is sent as the actual message content alongside the notification embed — not baked into the embed itself — so it's the right place to put an `@everyone` or role mention if you want one included in the message text itself (in addition to, or instead of, the feed's normal role ping setting).

> If a feed has both a role ping **and** a Custom Message configured, the role ping is sent first, immediately followed by your custom message text.
{.is-info}

Custom Messages support placeholder tokens that get replaced with real values from the notification. Supported tokens differ per feed type:

| Feed Type | Supported Tokens |
| :--- | :--- |
| Twitch | `{link}`, `{streamer}`, `{title}`, `{game}` |
| YouTube | `{link}`, `{channel}` |
| Reddit | `{link}`, `{subreddit}`, `{title}` |
| RSS | `{link}`, `{title}` |

Example (Twitch): `@everyone {streamer} just went live playing {game}! {link}`

> Custom Messages are limited to 2,000 characters, matching Discord's own message length limit.
{.is-info}

# Previews
# Tabs {.tabset}
## Twitch
![Twitch Screenshot](/twitch.png)

## YouTube
> **Notice:** Due to how slowly YouTube's video RSS feeds update, upload notifications can be delayed _UP TO_ 30 minutes after the actual upload time. &#x20;
{.is-warning}

![YouTube Screenshot](/youtube2.png)

## Reddit
> Reddit feeds currently require a [premium subscription](https://cakey.bot/premium) to use due to rate limit concerns.
{.is-warning}

![Reddit Screenshot](/reddit.png)

## Generic RSS 
> **Notice:** Currently Atom & RSS 2.0 feeds are supported. Other feeds might work but are NOT guaranteed.
{.is-info}

![RSS Screenshot](/image_(11).png)

# How to Create & Aquire Webhook URLs
Webhook URLs are created within Discord. Cakey Bot will send data to these URLs which in turn will post the social feed emssages in the given channel. To create and aquire a webhook URL simply follow these steps: 
1. Open the settings for the channel you want to create a webhook for. (Click the gear icon)
2. Click the "Integrations" tab.
3. In the webhooks section, click the "Create Webhook" button.
4. Click the webhook you just created and click the "Copy Webhook URL".
5. Paste this URL on Cakey Bot's dashboard when creating your social feed when you are asked for a "Webhook URL".

You can read more about webhooks on [Discord's help article](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks).