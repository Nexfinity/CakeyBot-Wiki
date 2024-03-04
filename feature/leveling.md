---
title: Leveling
description: 
published: 1
date: 2024-03-04T15:37:34.018Z
tags: 
editor: markdown
dateCreated: 2022-12-23T12:37:54.412Z
---

# Overview
Cakey Bot provides all servers with free role rewards and leaderboards. Configure custom XP rates, ignored/no XP roles/channels, and other configuration features!

> Migrating from MEE6 or another leveling bot? You can automatically import your leveling/xp data with the `/setup import-levels` command!
{.is-info}

# Importing/Exporting Leveling Data
## Importing
Cakey Bot makes it extremely easy to import your data from external/third-party bots! Currently we have support to automatically import data from these bots:
* [MEE6](https://mee6.xyz/)
* [Amari](https://amaribot.com/)

In order to automatically import the leveling data make sure you have `Manage Server` or `Administrator` permissions and then run the `/setup import-levels` command. Keep in mind it may take a few mintues to run if your server has a lot of users/data to export!

> Note that importing data will **WIPE** all existing leveling data for your server. This process can not be reversed so be sure before you run the command.
{.is-warning}

Don't see your prevous leveling/xp bot in the list above? No problem! You can still use the `/manage-levels` and `/manage-xp` commands to manually migrate your user data to Cakey Bot! Unlike some other bots, both of these commands are completely free to use!

## Exporting
We believe in vastly different philosophy than our competitors and as end-users of these kinds of systems ourselves in the past, we understand the pain and frustrations some of the other options give you.
All of which is why we allow you to export/download your leveling data at any time, instantly and completely for free!

In order to export your data, simple run the `/setup export-cakey-levels` command and you'll receive a CSV file with all of your data. Keep in mind it may take a few mintues to run if your server has a lot of users/data to export!

# Leveling Configuration

## Leveling Enabled
This disables or enables message leveling in the server.
> While this is not requied to be enabled for Voice Leveling to work, the `/manage-xp` and `/manage-level` commands will not function while this is disabled.
{.is-info}

## Voice Leveling Enabled
This disables or enables voice leveling in the server. You can keep this disabled while regular leveling is enabled so that users only earn XP for messages if you wish.

## Remove Roles on Demotion
Enabling this feature will have Cakey Bot automatically remove any Role Rewards when a user gets demoted via the `/manage-xp` or `/manage-level` commands.

## Remove Roles on Level Up
Enabling this feature will have Cakey Bot automatically remove any Role Rewards when a user levels up. (Including the `/manage-xp` or `/manage-level` commands.)

## Max Level
> This setting is limited to premium servers.
{.is-warning}

This allows you to set the maximum level that a user a level up to. By default the max level is set to 999.

## Announcement Location
* `Disabled`- This disables ALL level up messages. (`/rank` and `/leaderboard` commands will still work.)
* `Current Channel` - This will send the level up message in whatever channel the message that triggered the level up was sent in.
* `Custom Channel` - This will send ALL level up messages to the custom channel you have set.
* `Private Message/DM` - This will send the level up message to the user's DM. _Note: Some users may have DMs blocked/disabled and may not receive the alert._

## Announcement Message
This is the message that is sent when a user levels up. The default message is: `Congratulations {user}! You have advanced to level {level}!`.

You can also use a few placeholders in this message:
* `{user}` - The username mention of the user who leveled up. (It will not send ping notifications)
* `{level}` - The new level that the user has advanced to.
* `{reward}` - The role that was awared to the user.
  * **NOTE: You should only use the reward placeholder on the "Announcement Message When Role Is Awarded" section.**

## Min/Max XP
> This setting is limited to premium servers.
{.is-warning}

This sets the minimum and maximum XP a user can be given per message. There's a few limits: 
* The Max XP must be larger than the Min XP
* Both must be larger than 0
* Both must be less than 10,000

The default values for this setting are:
* Min XP: 15
* Min XP: 25

## Min/Max Voice XP
> This setting is limited to premium servers.
{.is-warning}

This sets the minimum and maximum XP a user can be given per minute spent inside of a voice channel. There's a few limits: 
* The Max XP must be larger than the Min XP
* Both must be larger than 0
* Both must be less than 10,000

The default values for this setting are:
* Min Voice XP: 5
* Min Voice XP: 8

## Leaderboard Vanity URL
> This setting is limited to premium servers.
{.is-warning}

This allows you to set a custom word or pharse to be used to easily access your server's leaderboard instead of the default URL that uses the server's ID.

For example, the default leaderboard URL will look something like this: `https://cakey.bot/leaderboard/top.php?id=408424043482447872`. This default URL can be difficult to remember. 
If you set a vanity URL to something like `caketropolis`, you can then access your server's leaderboard via `https://cakey.bot/leaderboard/caketropolis` which is alot easier for users to remember.

NOTE: If you set a vanity URL, the default URL will also continue to work. (You can use both URLs to access to leaderboards)

## XP Rate
This is a multiplier that is set for ever user in the server. It can adjust how quickly (or slowly) users level up. You can set these rates:
* 0.25x
* 0.5x
* 0.75x
* 1x
* 1.5x
* 2x
* 2.5x
* 3x

## Ignored Roles & Channels (NoXP Roles/Channels)
This is a list of channels or roles where XP will NOT be rewarded to users.

## Double XP Days
You can also specify days for Cakey Bot to award double XP on. The double XP will be calculated AFTER the XP rate has been calculated. You can select multiple days to apply double XP on.

![image_(9).png](/image_(9).png)

# Role Rewards
You can set up to 10 different role rewards. As users level up they will receive these roles once they meet the level requirement. You can also use the "Remove Roles on Level Up" setting to have old role rewards removed when users are assigned a new role. By default, users will keep ALL of their role rewards.

> Note: Newly added role rewards will only apply to users the next time they level up, they will not retroactively apply to current users who are high enough level.
{.is-info}

# Role XP Multipliers
You can set up to 5 different role multipliers. If a user has one (or more) of these roles, all of their received XP will be multiplied by the largest role multiplier they have. Role XP multipliers will NOT stack with each other if a user has multiple roles. However, they WILL stack wityh existing multipliers like double XP days.

> Note: Role XP multipliers will get added AFTER other XP multipliers (such as double XP days).
{.is-info}

# Rank Card Customization

## Banner Images
You can set different image banners for the `/rank` card. By default you can change the color of the banner from Red (Default color) to any of the colors listed below:
* Blue
* Green
* Orange
* Pink
* Purple
* Light Teal
* Yellow

Currently image banners will be applied to ALL users in the server.  [Premium](https://cakey.bot/premium.php) servers also have access to a wider selection of image banners for their rank cards.
<!-- Premium users are able to set their own separate banner images. However, server owners are able to disable this feature if they wish and force the server-selected banner image. -->

## Accent Colors & Overlay Opacity
You can also change/set the accent color as well as the opacity of the the black overlay between the text and background image to improve readability.

# Rank Card Badges
Users who support Cakey Bot will get badges on their profile, so you'll know they're cool.

[![A demo profile card](/card.png)](/card.png)

## ![two cyan hands shaking](/cb-partner.png) Partner Badge
This badge is given out to [our partners](https://cakey.bot/partners.html), some of the coolest bots across the Discord ecosystem. This by far the rarest badge with only 4 users!
<br />
 
## ![two cyan hands shaking](/cb-translator.png) Translater Badge
This badge is given to people who make Cakey Bot available in other languages.
<br />

## ![the CakeyBot logo](/cb-staff.png) Staff Badge
This badge is given to developers, moderators, writers, and administrators working on Cakey Bot.
<br />

## ![cb-tester.png](/cb-tester.png) Active Tester
This badge is given to users who actively help test new Cakey Bot features and provide feedback in our tester Discord server.
<br />

## ![The highest tier badge](/tier_10_64.png) Premium Badge
Users who purchase the premium version of Cakey Bot get a special badge that evolves as they maintain their membership.
![progression_banner.png](/progression_banner.png)