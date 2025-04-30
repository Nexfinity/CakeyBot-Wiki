---
title: Leveling
description: 
published: 1
date: 2025-04-30T10:07:55.732Z
tags: 
editor: markdown
dateCreated: 2022-12-23T12:37:54.412Z
---

# Overview
The Leveling & XP System in Cakey Bot provides a comprehensive user progression framework that rewards user activity in Discord servers. Cakey Bot provides all servers with free role rewards and leaderboards. Configure custom XP rates, ignored/no XP roles/channels, and other configuration features! This technical documentation covers the mechanics of XP earning, level calculation, role rewards, and system configuration

> Migrating from MEE6 or another leveling bot? You can automatically import your leveling/xp data with the `/setup import-levels` command!
{.is-info}

# Importing/Exporting Leveling Data
## Importing
Cakey Bot makes it extremely easy to import your data from external/third-party bots! Currently we have support to automatically import data from these bots:
* [MEE6](https://mee6.xyz/)
* [Amari](https://amaribot.com/)
* [XP-Bot.Net](https://xp-bot.net/) - **Note:** This source requires a file upload, read more: https://xp-bot.net/blog/b1728227181194p

In order to automatically import the leveling data make sure you have `Manage Server` or `Administrator` permissions and then run the `/setup import-levels` command. Keep in mind it may take a few mintues to run if your server has a lot of users/data to export!

> Note that importing data will **WIPE** all existing leveling data for your server. This process can not be reversed so be sure before you run the command.
{.is-danger}

Don't see your prevous leveling/xp bot in the list above? No problem! You can still use the `/manage-levels` and `/manage-xp` commands to manually migrate your user data to Cakey Bot! Unlike some other bots, both of these commands are completely free to use!

## Exporting
We believe in vastly different philosophy than our competitors and as end-users of these kinds of systems ourselves in the past, we understand the pain and frustrations some of the other options give you.

All of which is why we allow you to export/download your leveling data at any time, instantly and completely for free!

In order to export your data, simple run the `/setup export-cakey-levels` command and you'll receive a CSV file with all of your data. Keep in mind it may take a few mintues to run if your server has a lot of users/data to export!

# XP Earning Mechanics
The system provides two primary methods for users to earn XP:

* **Message XP:** Users earn between 15-25 XP (default) for each message sent in the server
* **Voice XP:** Users earn between 5-8 XP (default) per minute spent in voice channels

Key technical constraints:
* A 60-second cooldown between message XP awards prevents spam
* Muted/deafened users can be excluded from voice XP (configurable)
* XP rates can be modified server-wide or through multipliers
* Channels and roles can be excluded from XP earning

When a user earns enough XP to exceed their current level's threshold, a level-up event is triggered, which can:

* Award role rewards if configured
* Send level-up announcements via configured channels
* Remove previous role rewards if configured
* Update the user's rank on the leaderboard

# Leveling Configuration

> While **Leveling Enabled** is not requied to be enabled for **Voice Leveling** to work, the `/manage-xp` and `/manage-level` commands will not function while it is disabled.
{.is-info}

| Name                     | Description                                                                                                                             | Default Value | Min Value | Max Value | Premium Feature  |
| :----------------------- | :-------------------------------------------------------------------------------------------------------------------------------------- | :------------ | :-------- | :-------- | :--------------- |
| Leveling Enabled         | Enables or disables message leveling in the server. Note: `/manage-xp` and `/manage-level` commands won't function if this is disabled. | Enabled       |           |           | No               |
| Voice Leveling Enabled   | Enables or disables voice leveling. You can keep this off to only grant XP for messages.                                                | Enabled       |           |           | No               |
| Remove Roles on Demotion | Automatically removes Role Rewards when a user is demoted using `/manage-xp` or `/manage-level`.                                        | Disabled      |           |           | No               |
| Remove Roles on Level Up | Automatically removes Role Rewards when a user levels up, including via commands.                                                       | Disabled      |           |           | No               |
| Wipe User XP on Leave    | Wipes a user’s XP when they leave, are kicked, or banned.                                                                               | Disabled      |           |           | No               |
| Ignore Muted Users       | Toggles whether muted or deafened users earn XP in voice channels.                                                                      | Enabled       |           |           | No               |
| Ignore Solo Users        | Toggles whether users alone in a voice channel earn XP.                                                                                 | Enabled       |           |           | No               |
| Send Messages as Embed   | Sends level up messages as Discord embeds instead of plaintext.                                                                         | Disabled      |           |           | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span> |
| Max Level                | Sets the maximum level a user can reach.                                                                                                | 999           | 1         | 1,000     | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span> |
| Min XP per Message       | Sets the minimum XP a user can gain per message.                                                                                        | 15            | 1         | 1,000     | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span> |
| Max XP per Message       | Sets the maximum XP a user can gain per message. Must be greater than Min XP.                                                           | 25            | 1         | 1,000     | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span> |
| Min Voice XP per Minute  | Sets the minimum XP a user can gain per minute in a voice channel.                                                                      | 5             | 1         | 1,000     | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span> |
| Max Voice XP per Minute  | Sets the maximum XP a user can gain per minute in a voice channel. Must be greater than Min Voice XP.                                   | 8             | 1         | 1,000     | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span> |
| XP Rate                  | The multiplier that is set for ever user in the server. It can adjust how quickly (or slowly) users level up.                           | 1x            | 0.25x     | 3x        | No               |

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

## Leaderboard Vanity URL <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>
This allows you to set a custom word or pharse to be used to easily access your server's leaderboard instead of the default URL that uses the server's ID.

For example, the default leaderboard URL will look something like this: `https://cakey.bot/leaderboard/top.php?id=408424043482447872`. This default URL can be difficult to remember. 
If you set a vanity URL to something like `caketropolis`, you can then access your server's leaderboard via `https://cakey.bot/leaderboard/caketropolis` which is alot easier for users to remember.

> NOTE: If you set a vanity URL, the default URL will also continue to work. (You can use both URLs to access to leaderboards)
{.is-info}

## Ignored Roles & Channels (NoXP Roles/Channels)
This is a list of channels or roles where XP will NOT be rewarded to users.

## Double XP Days
You can also specify days for Cakey Bot to award double XP on. The double XP will be calculated AFTER the XP rate has been calculated. You can select multiple days to apply double XP on.

![Double XP Options](/image_(9).png)

# Role Rewards
You can set up to 10 different role rewards (Or up to 20 with a premium susbcription). As users level up they will receive these roles once they meet the level requirement. You can also use the "Remove Roles on Level Up" setting to have old role rewards removed when users are assigned a new role. By default, users will keep ALL of their role rewards.

> Note: In order to prevent abuse, Cakey Bot will prevent selecting roles that contain `Administrator`, `Manage Server` or `Manage Roles` permissions. In addition, if these roles gain this permission after being set, the bot will no longer assign them.
{.is-danger}

# Role & Channel XP Multipliers
You can set up to 5 different multipliers of each type (Or up to 10 with a premium susbcription). Role and Channel multipliers are counted separately. If a user qualifies one (or more) of these multipliers, all of their received XP will be multiplied by the largest multiplier they have. Role and Channel XP multipliers will NOT stack with other multipliers of the same type if a user qualifies for multiple (Role multipliers WILL stack with a Channel multiplier though). They WILL also stack with other multipliers such as  double XP days.

> Note: Role/Channel XP multipliers will get added AFTER other XP multipliers (such as double XP days and global rate).
{.is-info}

# XP Decaying
XP Decay reduces a user's XP over time when they are inactive, ensuring leaderboards reflect active participation. Decay begins after a set period of inactivity and is applied daily at a configurable rate. It stops once users reach a minimum XP level. Multipliers do not affect XP decay, ensuring fairness across all users.

> **Note:** XP decay is **NOT** affected by multipliers.
{.is-info}

## Configuration Settings
| Name          | Description                                                                                                                                         | Default Value |
| :------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------- | :------------ |
| Decay Rate    | Determines the percentage of XP lost per day once the decay process begins. This is based on the user's current XP and is applied daily.           | 0.10 (10%)    |
| Decay Days    | Specifies the minimum number of days of inactivity before XP decay starts.                                                                          | 7 days        |
| Decay Minimum | Sets the minimum XP level for decay to occur and defines the lowest level a user can decay to. XP will not drop below this threshold. | 1 |

# Rank Card Customization

## Banner Images
You can set different image banners for the `/rank` card. [Premium](https://cakey.bot/premium.php) servers also have access to a wider selection of image banners for their rank cards.

Our fancy image banner editor:
<image src="/leveling-editor.jpg" width="800px" alt="Banner Editor">
  
> The recommended image size is `Width: 930` x `Height: 280` for custom image banners.
{.is-info}

# Rank Card Badges
Users who support Cakey Bot will get badges on their profile, so you'll know they're cool.

[![A demo profile card](/card.png)](/card.png)

| Badge      | Name      | Description                      |
| :--------- | :--------- | :------------------------------ |
| ![partner badge](/cb-partner.png) | Partner | This badge is given out to our partners, some of the coolest bots across the Discord ecosystem. This by far the rarest badge with only 2 users! |
| ![translator badge](/cb-translator.png) | Translater | This badge is given to people who make Cakey Bot available in other languages. |
| ![the CakeyBot logo](/cb-staff.png) | Cakey Bot Staff | This badge is given to developers, moderators, writers, and administrators working on Cakey Bot. |
| ![active tester badge](/cb-tester.png) | Active Tester | This badge is given to users who actively help test new Cakey Bot features and provide feedback in our tester Discord server. |
| ![graphic designer badge](/cb-graphic-designer.png) | Graphic Designer | This badge is awarded to talented individuals who contribute to Cakey Bot’s visual identity by designing emotes, icons, banners, or other graphical assets. Their creativity helps enhance the bot’s appearance and branding across Discord. |
| ![custom bot icon](/cb-custom-bot.png) | Custom Bot Owner | This special badge is granted to users who purchase a Custom Bot version of Cakey Bot. <3 |
| ![The highest tier badge](/tier_10_64.png) | Premium User | Users who purchase the premium version of Cakey Bot get a special badge that evolves as they maintain their membership. |

## Premium User Badge Progression
![progression banner](/progression_banner.png)

# Frequently Asked Questions
## What XP equation is used for leveling?
Cakey Bot uses the same leveling XP equation as the popular MEE6 bot. You can use the following formula to calculate how much XP you need to level up:
`5 * (lvl ^ 2) + (50 * lvl) + 100 - xp`, where
* `lvl` is your current level
* `xp` is how much XP you already have towards the next level.

## Is there a cooldown or anti-abuse?
Yes, Cakey Bot has a cooldown for messages to help discourage spamming. Only one message per 60 second interval will award XP, even if multiple messages are sent during that time.

## How can I combat malicious users spamming for free XP?
There's several tools you can use:
* `/manage-level` and `/manage-xp` commands allow you to manually adjust a user's XP or level to remove ill-gotten xp or levels
* You can mute or timeout the user to prevent them sending messages.
* Could you configure a no-xp/ignored role on the dashbaord and assign it to them to prevent them from getting any XP while they are unmuted.
  
# Related Commands
Usage Key: `<required>` / `[optional]`
| Command                          | Description                                                              | Usage                                   | Permission                |
| :------------------------------- | :----------------------------------------------------------------------- | :------------------------------------: | :-----------------------: |
| /leaderboard                     | View the top 10 users on the leaderboard.                                | N/A                                    | None                      |
| /leveling manage-level           | Manage a user's level.                                                   | \<give \| remove \| set> \<user> \<level>  | ManageServer             |
| /leveling manage-xp              | Manage a user's XP.                                                      | \<give \| remove \| set> \<user> \<xp>    | ManageServer             |
| /rank                            | Get your rank or another user's rank.                                    | [user]                                 | None                      |
| /setup export-cakey-levels       | Exports your Cakey Bot leveling and XP data.                             | N/A                                    | ManageServer or Administrator |
| /setup import-levels             | Imports your leveling and XP data from other bots. NOTE: EXISTING LEVEL DATA WILL BE OVERWRITTEN! | N/A | ManageServer or Administrator |
| /setup reset-levels              | Reset the leveling for this server. This will RESET ALL user levels & XP!| \<confirm>                              | ManageServer or Administrator |
| /setup reset-levels-missing      | Reset the levels/xp for users who have left the server.                  | \<confirm>                              | ManageServer or Administrator |
