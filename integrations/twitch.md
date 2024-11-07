---
title: Twitch Integration
description: 
published: 1
date: 2024-11-07T06:28:30.845Z
tags: 
editor: markdown
dateCreated: 2024-10-24T06:16:41.719Z
---

# Overview
> This feature is currently in BETA testing.
{.is-warning}

# Linking/Unlinking a Twitch Account
> Note: All of the scopes that Cakey Bot requests are read-only. Linking your account to Cakey Bot will not give Cakey Bot edit access to anything. You can also fully unlink your account at any time.
{.is-info}


# Supported Events
Cakey Bot currently supports 6 primary events for regular accounts and 8 primary events for affiliates/partners. Some events may have additional subevents such as `Begin`, `Progress` or `End` that can be toggled separately. 

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

> Note: Internally Twitch handles Timeouts as bans with a duration (think like Temp Bans). In addition to this, their API does NOT provide us a way to determine the difference between an unban and a timeout removal. This means both of these actions will be linked to the same event. This is a limitation on Twitch's end.

## Affiliate/Partner Events
> This events/actions are only available on affiliate/partner accounts. If you become an affiliate/partner after initially linking your Tiwtch account as a non-affiliate, you can use the "Re-Link Twitch Account" button to update your affiliate/partner status in our dashboard to access these settings.
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