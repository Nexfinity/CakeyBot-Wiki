---
title: Achievements
description: Discord achievement system with Cakey Bot - Custom badges, milestone rewards, progress tracking. Gamification setup guide.
published: 1
date: 2026-04-06T20:45:57.985Z
tags: 
editor: markdown
dateCreated: 2023-12-18T10:08:47.560Z
---

# Overview
The Achievement System within our Discord bot empowers server owners to create diverse and engaging milestones for users to unlock based on their activities and contributions within the community. These achievements serve as markers of accomplishment, encouraging participation and interaction across the server.

# How it Works
* **Achievement Creation:** Server owners can create and customize various achievements with specific requirements tailored to diverse user engagements. These achievements encompass a wide range of activities and events within the server.

* **User Engagement Tracking:** The bot continuously tracks user activities and progress towards achieving the set criteria for each milestone. Progression is monitored for various actions like time spent in voice channels, message count, boosting the server, participation in events, reactions added, thread creation and involvement, and birthday settings.

* **Unlock Alerts:** Once a user fulfills the prerequisites for unlocking an achievement, a visually appealing image alert is automatically generated and sent to a specified channel, showcasing the user's accomplishment and encouraging further engagement within the server.

# Create/Manage Achievements
## Create Achievements
To create an achievement login to our [web dashboard](https://cakey.bot/dashboard) then follow these steps:
1. Open the "Achievements" page
2. Click the blue "Create New Acheivement" button
3. Make any desired configurations on the pop-up modal
4. Click "Create Achievement" button

> You can create up to **10 achievements** per server. [Premium](https://cakey.bot/premium) servers have no limit on the number of achievements.
{.is-info}

The achievement fields have the following limits:

| Field | Limit |
| :--- | :--- |
| Name | 300 characters |
| Description | 140 characters |
| Icon Name | 20 characters |
| Progression Target (limit) | 1,000,000 |
| XP Add / XP Remove Reward | 0 - 1,000,000 |
| Eco Money Add / Eco Money Remove Reward | 0 - 1,000,000 |

## Clone Achievements
Need a new achievement that's similar to one you already have? Instead of starting from scratch you can clone an existing achievement:
1. Open the "Achievements" page
2. Find the achievement you want to clone
3. Click the clone button on the achievement
4. This will open the create achievement modal pre-filled with the cloned achievement's settings - make any desired changes and click "Create Achievement"

## Edit Achievements
To modify an achievement follow these steps:
1. Open the "Achievements" page
2. Find the achievement you want to modify
3. Click the blue pen button on the achievement
4. Make any desired changes on the pop-up modal & click save

## Enable/Disable Achievements
Achievements can be temporarily disabled without deleting them. While disabled, users will not be able to unlock or progress towards the achievement. To toggle an achievement:
1. Open the "Achievements" page
2. Find the achievement you want to enable/disable
3. Click the enable/disable toggle on the achievement

## Delete Achievements
To delete an achievement follow these steps:
1. Open the "Achievements" page
2. Find the achievement you want to delete
3. Click the red trash can button on the achievement
4. Confirm the deletion in the pop-up modal

# Customization Options
## Background Banners
Currently there is a "Dark Mode" background (shown top) and a "Light Mode" background (shown bottom).
<image src="/achievement-backgrounds.png" width="600px" alt="Banners">

## Badge Shapes & Colors
There are several different badge combinations that you can select for your achievement unlock banners.
You can chose between 5 shapes including:
* Hexagon
* Pentagon
* Circle
* Diamond
* Square

<image src="/achievement-badges.png" width="600px" alt="Badges">

You can also chose between 9 different colors:
* Red
* Brown
* Blue
* Purple
* Grey
* Green
* Pink
* Teal
* Yellow
  
<image src="/colors.jpg" width="600px" alt="Colors">

## Icons
We currently support the full set of Font Awesome Pro icons that you can select for your banners (currently limited to solid style). You can select any RGB color to be applied to the icon as well.

# Rewards
When a user unlocks an achievement, Cakey Bot can automatically reward them with any combination of the following:
* **XP Add / XP Remove** - Adds or removes leveling XP from the user.
* **Eco Money Add / Eco Money Remove** - Adds or removes economy money from the user.
* **Add Roles** - Grants the selected Discord role(s) to the user.
* **Remove Roles** - Removes the selected Discord role(s) from the user.

## Ignored Channels
You can select specific channels to be excluded from counting towards achievement progress. For example, if you exclude a channel from message-count tracking, messages sent in that channel won't count towards a "Send X messages" achievement.

# Types of Achievements
## Progression-Based Achievements
Currently Cakey Bot supports several progression-based events for awarding achievements. These events include:
* X minutes spent in voice channels.
* Send X messages.
* Boosted the server.
* Joined X giveaways.
* Add X reactions.
* Create X threads.
* Joined X threads.
* Set their birthday.
* Acquire an X day streak.
* CUSTOM / MANUAL

> **Note:** Announcements for unlocks are only sent when a user's stats are equal to the required limit. If an achievement is created after the user exceeds the limit the announcement will not be sent. Though it will still be displayed as unlocked for the user when checked via commands.
{.is-info}
  
> **Note:** You can not swap progress based achievements into CUSTOM / MANUAL achievements _after_ they have been created. (or vice-versa)
{.is-warning}

> The progression target (e.g. the "X" in "Send X messages") is capped at **1,000,000**.
{.is-info}
  
# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /achievements info | View information about a specific achievement. | \<achievement> | None | 
| /achievements list | View a list of all achievements for this server. | N/A | None | 
| /achievements view | View the selected users progress towards achievements. | [user] | None | 
| /achievements custom | Grant or revoke a custom achievement. | \<grant \| revoke> \<achievement> [user] | Manage Events |
| /setup force-check-boosts | Force check user boosts for achievements. | N/A | ManageServer or Administrator | 
| /setup clear-achievement-data | Remove ALL achievement data for the server. | N/A | ManageServer or Administrator | 