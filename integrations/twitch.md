---
title: Twitch Integration
description: Discord Twitch alerts with Cakey Bot - Stream notifications, live roles, subscriber sync. Streamer integration guide.
published: 1
date: 2024-11-23T21:01:06.899Z
tags: 
editor: markdown
dateCreated: 2024-10-24T06:16:41.719Z
---

# Overview
The Twitch OAuth Integration allows you to link your Twitch account with Cakey Bot, enabling enhanced functionality and event tracking. Once your Twitch account is linked, Cakey Bot can listen to a variety of events related to your Twitch channel, such as user follows, raids, subscriptions, and more. This integration provides you with a seamless experience in managing and interacting with your Twitch events directly inside of Discord.

# Linking/Unlinking a Twitch Account
## Linking 
To access and our Twitch OAuth Integration you will need to link your Twitch account. In order to do so you will need to click the "Link Twitch Account" button on the Twitch OAuth Integration page and "Authorize" Cakey Bot to your Twitch account. If you do not authorize Cakey Bot, you will be unable to use this feature.

> Note: All of the scopes that Cakey Bot requests are read-only. Linking your account to Cakey Bot will _not_ give Cakey Bot edit access to anything. You can also fully unlink your account at any time.
{.is-info}

## Re-Linking
In order to re-link your Twitch account you can simply click the "Re-Link Twitch Account" button and complete the provided OAuth flow. This can be useful if your OAuth token gets revoked or becomes invalid and needs to be updated. In addition, this will update your Affiliate/Partner status if you achieved it after initially linking your account without it.

## Unlinking
If you no longer wish to use this feature, you can click the "Un-Link Twitch Account" button on the integration page. This will wipe your OAuth token from our database immediately AND wipe all of your configuration settings. You will be able to re-link your Twitch account later if you wish, however, you will need to reconfigure all of your settings if you do.

# Supported Events
Cakey Bot currently supports 7 primary events for regular accounts and 8 primary events for affiliates/partners. Some events may have additional subevents such as `Begin`, `Progress` or `End` that can be toggled separately. 

Technically, Cakey Bot can support _most_ of the events listed on [this page](https://dev.twitch.tv/docs/eventsub/eventsub-subscription-types/). If you are interested in additional events being added, feel free to make a #feature-request on our [support discord](https://cakey.bot/discord).

## Regular Events:
* Follows
* Raids
* Moderator Status
  * Added
  * Removed
* User Banned
* User Timedout
* User Unbanned/Timeout Removed
* Warnings
  * Sent
  * Acknowledged

> Note: Internally Twitch handles timeouts as bans with a duration (think like Temp Bans). In addition to this, their API does NOT provide us a way to determine the difference between an unban and a timeout removal. This means both of these actions will be linked to the same event. This is a limitation on Twitch's end.

## Affiliate/Partner Events
> These events/actions are only available on affiliate/partner accounts. If you become an affiliate/partner after initially linking your Twitch account as a non-affiliate, you can use the "Re-Link Twitch Account" button to update your affiliate/partner status in our dashboard to access these settings.
{.is-info}

* Bits/Cheers
* Polls
  * Begin
  * Progress
  * End
* Predictions
  * Begin
  * Progress
  * Lock
  * End
* Rewards/Redemptions
* Subscriptions
  * New
  * Gift
  * End
* Goals
  * Begin
  * Progress
  * End
* Hype Train
  * Begin
  * Progress
  * End
* VIP Status
  * Added
  * Removed