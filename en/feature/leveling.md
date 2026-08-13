---
title: Leveling
description: Discord leveling system with Cakey Bot - XP rewards, role progression, import from MEE6 or Lurkr. Complete setup with formulas and examples.
published: 1
date: 2026-08-13T08:25:23.962Z
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
* [MEE6](https://mee6.xyz/) - imported automatically, no file needed.
* [Lurkr](https://lurkr.gg/) - requires attaching an exported levels JSON file (see below).

In order to automatically import the leveling data make sure you have `Manage Server` or `Administrator` permissions and then run the `/setup import-levels` command, choosing the bot you're migrating from. Keep in mind it may take a few mintues to run if your server has a lot of users/data to export!

### Importing from Lurkr
Unlike MEE6, Lurkr doesn't have a public leaderboard API Cakey Bot can pull from directly - you'll need to export your server's level data from Lurkr's dashboard first:
1. Open your server's Lurkr dashboard and export the levels leaderboard as a JSON file.
2. Run `/setup import-levels` and select `Lurkr` as the bot.
3. Attach the exported JSON file to the `file` option of the command.

Cakey Bot will read the attached file directly, so nothing is fetched from Lurkr automatically for this import.

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

> While **Leveling Enabled** is not required to be enabled for **Voice Leveling** to work, the `/manage-xp` and `/manage-level` commands will not function while it is disabled.
{.is-info}

| Name                     | Description                                                                                                                             | Default Value | Min Value | Max Value | Premium Feature  |
| :----------------------- | :-------------------------------------------------------------------------------------------------------------------------------------- | :------------ | :-------- | :-------- | :--------------- |
| Leveling Enabled         | Enables or disables message leveling in the server. Note: `/manage-xp` and `/manage-level` commands won't function if this is disabled. | Enabled       |           |           | No               |
| Voice Leveling Enabled   | Enables or disables voice leveling. You can keep this off to only grant XP for messages.                                                | Enabled       |           |           | No               |
| Remove Roles on Demotion | Automatically removes Role Rewards when a user is demoted using `/manage-xp` or `/manage-level`.                                        | Disabled      |           |           | No               |
| Remove Roles on Level Up | Automatically removes Role Rewards when a user levels up, including via commands.                                                       | Disabled      |           |           | No               |
| Wipe User XP on Leave    | Wipes a user’s XP when they leave, are kicked, or banned.                                                                               | Disabled      |           |           | No               |
| Ignore Muted Users       | Toggles whether muted users earn XP in voice channels.                                                                      | Enabled       |           |           | No               |
| Ignore Deafened Users       | Toggles whether deafened users earn XP in voice channels.                                                                      | Enabled       |           |           | No               |
| Ignore Solo Users        | Toggles whether users alone in a voice channel earn XP.                                                                                 | Enabled       |           |           | No               |
| Disable Level Up Mentions        | Toggles whether level up messages will mention users/roles.                                                                                 | Disabled       |           |           | No               |
| Send Messages as Embed   | Sends level up messages as Discord embeds instead of plaintext.                                                                         | Disabled      |           |           | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span> |
| Max Level                | Sets the maximum level a user can reach.                                                                                                | 999           | 1         | 1,000     | No |
| Min XP per Message       | Sets the minimum XP a user can gain per message.                                                                                        | 15            | 1         | 10,000    | No |
| Max XP per Message       | Sets the maximum XP a user can gain per message. Must be greater than Min XP.                                                           | 25            | 1         | 10,000    | No |
| Text Cooldown                 | Sets the cooldown in minutes between text messages that can earn XP.                                                                    | 1             | 1         | 60        | No |
| Min XP per Image              | Sets the minimum BONUS XP a user can gain per message containing an image.                                                              | 0             | 1         | 10,000    | No |
| Max XP per Image              | Sets the maximum BONUS XP a user can gain per message containing an image. Must be greater than Min Image XP.                           | 0             | 1         | 10,000    | No | 
| Image Cooldown                | Sets the cooldown in minutes between image attachments that can earn bonus XP.                                                          | 1             | 1         | 60        | No |
| Min XP per Video              | Sets the minimum BONUS XP a user can gain per message containing a video.                                                               | 0             | 1         | 10,000    | No |
| Max XP per Video              | Sets the maximum BONUS XP a user can gain per message containing a video. Must be greater than Min Video XP.                            | 0             | 1         | 10,000    | No |
| Video Cooldown                | Sets the cooldown in minutes between video attachments that can earn bonus XP.                                                          | 1             | 1         | 60        | No |
| Min Voice XP per Minute       | Sets the minimum XP a user can gain per minute in a voice channel.                                                                      | 5             | 1         | 10,000    | No |
| Max Voice XP per Minute       | Sets the maximum XP a user can gain per minute in a voice channel. Must be greater than Min Voice XP.                                   | 8             | 1         | 10,000    | No |
| Voice Cooldown                | Sets the interval in minutes at which voice XP is awarded.                                                                              | 2             | 1         | 60        | No |
| XP Rate                  | The multiplier that is set for ever user in the server. It can adjust how quickly (or slowly) users level up.                           | 1x            | 0.25x     | 3x        | No               |
| XP Equation               | The XP-to-level curve used to calculate levels. See [What XP equation is used for leveling?](#what-xp-equation-is-used-for-leveling) below for the available options. | Default (MEE6 Style) |           |           | No               |
| Prevent Consecutive Claims        | Prevents the same user from claiming multiple consecutive random XP drops. Users must wait for another user to claim before claiming again. | Disabled      |           |           | No               |
| Randomize Button Placement        | Randomizes the claim button position in random XP drop messages to prevent automated claiming bots.                                     | Disabled      |           |           | No               |

## Announcement Location
* `Disabled`- This disables ALL level up messages. (`/rank` and `/leaderboard` commands will still work.)
* `Current Channel` - This will send the level up message in whatever channel the message that triggered the level up was sent in.
* `Custom Channel` - This will send ALL level up messages to the custom channel you have set.
* `Private Message/DM` - This will send the level up message to the user's DM. _Note: Some users may have DMs blocked/disabled and may not receive the alert._

## Announcement Message
This is the message that is sent when a user levels up. The default message is: `Congratulations {user}! You have advanced to level {level}!`.

You can also use a few placeholders in this message:
* `{user}` - The username mention of the user who leveled up.
* `{level}` - The new level that the user has advanced to.
* `{reward}` - The role that was awared to the user.
  * **NOTE: You should only use the reward placeholder on the "Announcement Message When Role Is Awarded" section.**

### Conditional Level Blocks
You can wrap part of your message in a conditional block so it only appears for specific levels:
* `{#level.N}...{/level.N}` - Only shows the text between the tags if the level the user just reached is **exactly** `N`.
* `{^level.N}...{/level.N}` - The inverse: only shows the text between the tags if the level the user just reached is **NOT** `N`.

For example, this message shows a special line only on level 10:
```
Congratulations {user}! You have advanced to level {level}!{#level.10}You've unlocked double digits!{/level.10}
```

You can stack as many of these blocks as you want, and each one is evaluated independently:
```
{#level.10}You've unlocked double digits!{/level.10}{#level.25}Quarter century club!{/level.25}
```

Blocks can also be nested inside each other, as long as each closing `{/level.N}` matches the most recently opened tag with the same `N` (like nested brackets). This lets you build a "none of the above" fallback message that only shows up when none of the listed levels matched:
```
{^level.10}{^level.25}{^level.50}Keep going, you're doing great!{/level.50}{/level.25}{/level.10}
```

Text outside of any conditional block always shows up as normal, exactly like any other placeholder text.

> Both the Announcement Message and the "Announcement Message When Role Is Awarded" message are capped at **2,000 characters**.
{.is-info}

## Leaderboard Vanity URL <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>
This allows you to set a custom word or pharse to be used to easily access your server's leaderboard instead of the default URL that uses the server's ID.

For example, the default leaderboard URL will look something like this: `https://cakey.bot/leaderboard/id/408424043482447872`. This default URL can be difficult to remember. 
If you set a vanity URL to something like `caketropolis`, you can then access your server's leaderboard via `https://cakey.bot/leaderboard/caketropolis` which is alot easier for users to remember.

> NOTE: If you set a vanity URL, the default URL will also continue to work. (You can use both URLs to access to leaderboards). Also this setting is linked/syncronized across multiple features.
{.is-info}

> Vanity URLs are capped at **20 characters** and cannot start with "id".
{.is-warning}

## Ignored Roles & Channels (NoXP Roles/Channels)
This is a list of channels or roles where XP will NOT be rewarded to users.

## Double XP Days
You can also specify days for Cakey Bot to award double XP on. The double XP will be calculated AFTER the XP rate has been calculated. You can select multiple days to apply double XP on.

![Double XP Options](/image_(9).png)

# Role Rewards
You can set up to 10 different role rewards (Or up to 20 with a premium susbcription). As users level up they will receive these roles once they meet the level requirement. You can also use the "Remove Roles on Level Up" setting to have old role rewards removed when users are assigned a new role. By default, users will keep ALL of their role rewards.

> Note: In order to prevent abuse, Cakey Bot will prevent selecting roles that contain `Administrator`, `Manage Server` or `Manage Roles` permissions. In addition, if these roles gain this permission after being set, the bot will no longer assign them.
{.is-danger}

# Leaderboard Roles
In addition to level-based Role Rewards, you can automatically grant roles to whoever currently holds a Top 10 leaderboard position (ranked by total XP). Unlike Role Rewards, these roles are re-evaluated on a recurring basis (roughly every 15-30 minutes) and follow whoever currently occupies each position - if someone is overtaken and drops out of a position (or out of the top 10 entirely), the bot automatically removes the role from them and grants it to whoever now holds that spot.

You can configure a role for each position independently on the dashboard. Leaving a position set to "None" means no role is granted for that position. **Positions #1-3 are free for every server.** Positions #4-10 are <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span> and appear locked on the dashboard until your server has Premium.

> Note: In order to prevent abuse, Cakey Bot will prevent selecting roles that contain `Administrator`, `Manage Server` or `Manage Roles` permissions. In addition, if these roles gain this permission after being set, the bot will no longer assign them.
{.is-danger}

> If multiple users are tied in XP, they ALL receive the role for the better (lower-numbered) position. For example, if two users are tied for what would be #2 and #3, both receive the role configured for position #2, and the role for position #3 is not granted to anyone that cycle.
{.is-info}

> If your server's Premium subscription lapses, roles previously granted for positions #4-10 are automatically removed. Positions #1-3 keep working regardless of Premium status. Any positions #4-10 you had configured are preserved (not deleted) while Premium is inactive, and pick back up automatically if you resubscribe.
{.is-warning}

# Role & Channel XP Multipliers
You can set up to 5 different multipliers of each type (Or up to 10 with a premium susbcription). Role and Channel multipliers are counted separately. If a user qualifies one (or more) of these multipliers, all of their received XP will be multiplied by the largest multiplier they have. Role and Channel XP multipliers will NOT stack with other multipliers of the same type if a user qualifies for multiple (Role multipliers WILL stack with a Channel multiplier though). They WILL also stack with other multipliers such as  double XP days.

> Note: Role/Channel XP multipliers will get added AFTER other XP multipliers (such as double XP days and global rate).
{.is-info}

> Multiplier values must be between **0.01 and 10.00**.
{.is-info}

# XP Decaying
XP Decay reduces a user's XP over time when they are inactive, ensuring leaderboards reflect active participation. Decay begins after a set period of inactivity and is applied daily at a configurable rate. It stops once users reach a minimum XP level. Multipliers do not affect XP decay, ensuring fairness across all users.

> **Note:** XP decay is **NOT** affected by multipliers.
{.is-info}

## Configuration Settings
| Name          | Description                                                                                                                                         | Default Value |
| :------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------- | :------------ |
| Decay Rate (per day)    | Determines the percentage of XP lost per day once the decay process begins. This is based on the user's current XP and is applied daily.           | 0.10 (10%)    |
| Days Since Activity    | Specifies the minimum number of days of inactivity before XP decay starts.                                                                          | 7 days        |
| Minimum Level | Sets the minimum XP level for decay to occur and defines the lowest level a user can decay to. XP will not drop below this threshold. | 1 |
| Decay Ignore Roles | Users with these roles will not have XP decay applied even if inactive | None |

> Decay Rate can be set between **0.01-1.0** (1%-100%). Days Since Activity can be set between **1-365** days. Minimum Level can be set between **1-1,000**.
{.is-info}


# Random XP Drops
Random XP Drops introduce timed XP bonuses that occur during active event periods or seasons. These drops encourage engagement and reward users for participating during special occasions. When enabled, random XP drop events can occur across configured channels, providing users with additional XP rewards upon claiming. You can also manually spawn XP drops with `/leveling spawn-xp-drop`, even if the random timer system is disabled.

> **Note:** Random XP Drops can only occur when the feature is enabled and a valid output channel is configured.
{.is-info}

## Configuration Settings
| Name                  | Description                                                                                                                                              | Default Value |
| :-------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------ |
| Drops Enabled         | Determines whether Season XP Drops are active. When disabled, no XP drops will occur regardless of other settings.                                      | Off (0)       |
| Output Channel        | The channel where XP drop events are announced. If multiple are selected, the bot will randomly choose one for each drop. | None (0)      |
| Min. XP               | The minimum XP amount that can be awarded during a drop event.                                                                                          | 500           |
| Max. XP               | The maximum XP amount that can be awarded during a drop event.                                                                                          | 2000          |
| Min. Time (Hours)     | The minimum interval between XP drop events, measured in hours.                                                                                         | 2 hours       |
| Max. Time (Hours)     | The maximum interval between XP drop events, measured in hours.                                                                                         | 6 hours       |

> **Note:** If no valid channel is set, drops will not trigger. You need to have drops enabled AND at least one output channel selected.
{.is-warning}

> **Limits:** Min. XP and Max. XP have a hard cap of **1,000,000**. Min. Time (Hours) can be set between **1-23**. Max. Time (Hours) can be set between **2-24** and must be greater than Min. Time.
{.is-info}


**Behavior Overview**
- XP drop events are randomly scheduled between the configured minimum and maximum hours.  
- Each drop awards a random XP amount within the defined XP range.  
- Drops will only occur when both the feature and output channel are set.  
- Claiming a drop resets the drop timer and triggers the next event window.
- The previous drop must be claimed for a new one to spawn.
- The random images used for the drops may change throughout the year to reflect the current season or nearby holiday to help keep things refreshing/new.

> **Tip:** Use shorter time intervals during events to increase engagement and activity.
{.is-success}

# Rank Card Customization

## Banner Images
You can set different image banners for the `/rank` card. [Premium](https://cakey.bot/premium) servers also have access to a wider selection of image banners for their rank cards.

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
From the "Leveling" page on the [dashboard](https://cakey.bot/dashboard), you can choose which XP-to-level equation your server uses under the **XP Equation** setting. Four options are available:

| Equation | Formula (XP needed to advance from level `lvl`, minus `xp` already earned towards it) |
| :--- | :--- |
| Default (MEE6 Style) | `5 * (lvl ^ 2) + (50 * lvl) + 100 - xp` |
| Linear | `2000 - xp` (a flat 2,000 XP per level, regardless of current level) |
| Lurkr Style | `50 * (lvl ^ 2) - (100 * lvl) + 150 - xp` |
| Amari Style | `20 * (lvl ^ 2) - (40 * lvl) + 55 - xp` |

Where:
* `lvl` is your current level
* `xp` is how much XP you already have towards the next level.

**Default (MEE6 Style)** is the same leveling XP equation Cakey Bot has always used, and matches the popular MEE6 bot's curve. It remains the default for all servers.

> Changing this setting takes effect immediately - every user's displayed level is recalculated against the new curve the next time it's checked, since only raw XP is ever stored (not level). This means levels can jump up or down right away for existing users; there is no gradual transition or grandfathering of old levels.
{.is-warning}

You can use our free [XP Calculator](https://cakey.bot/xp-calculator) tool to work out exactly how much XP is needed between two levels under any of the four equations - if you're logged in, it can even load your server's currently configured equation automatically.

## Is there a cooldown or anti-abuse?
Yes, Cakey Bot has a cooldown for messages to help discourage spamming. Only one message per 60 second interval will award XP, even if multiple messages are sent during that time.

## How can I combat malicious users spamming for free XP?
There's several tools you can use:
* `/manage-level` and `/manage-xp` commands allow you to manually adjust a user's XP or level to remove ill-gotten xp or levels
* You can mute or timeout the user to prevent them sending messages.
* Could you configure a no-xp/ignored role on the dashbaord and assign it to them to prevent them from getting any XP while they are unmuted.
  
# Related Commands
Usage Key: `<required>` / `[optional]`
| Command                          | Description                                                              | Usage                                      | Permission             |
| :------------------------------- | :----------------------------------------------------------------------- | :----------------------------------------: | :--------------------: |
| /leaderboard                     | View the top 10 users on the leaderboard.                                | [limit]                                    | None                   |
| /leveling manage-level           | Manage a user's level.                                                   | \<give \| remove \| set> \<user> \<level>  | ManageServer           |
| /leveling manage-xp              | Manage a user's XP.                                                      | \<give \| remove \| set> \<user> \<xp>     | ManageServer           |
| /leveling spawn-xp-drop          | Manually spawn an XP drop in a channel.                                  | [min-xp] [max-xp] [channel]                | ManageServer           |
| /rank                            | Get your rank or another user's rank.                                    | [user]                                     | None                   |
| /setup export-cakey-levels       | Exports your Cakey Bot leveling and XP data.                             | N/A                                        | ManageServer or Administrator |
| /setup import-levels             | Imports your leveling and XP data from other bots. NOTE: EXISTING LEVEL DATA WILL BE OVERWRITTEN! | \<bot> [file]      | ManageServer or Administrator |
| /setup reset-levels              | Reset the leveling for this server. This will RESET ALL user levels & XP!| \<confirm>                                 | ManageServer or Administrator |
| /setup reset-levels-missing      | Reset the levels/xp for users who have left the server.                  | \<confirm>                                 | ManageServer or Administrator |
