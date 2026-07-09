---
title: Giveaways
description: Discord giveaways with Cakey Bot - Host giveaways with role/level requirements, entry buttons, rerolls and automatic winner picking. Setup guide.
published: 1
date: 2026-07-09T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-07-09T00:00:00.000Z
---

# Overview

> You will need the **`Manage Events`** permission to create, end, reroll or view the entries of a giveaway.
{.is-warning}

Cakey Bot's giveaway system lets you host giveaways directly from Discord using the `/giveaway` command. Members enter by clicking a button on the giveaway message, and Cakey Bot will automatically pick and announce the winners once the giveaway ends. You can also optionally require a specific role or leveling rank to enter, end giveaways early, and reroll winners at any time after a giveaway has ended.

# Creating a Giveaway

To start a new giveaway, run `/giveaway create <winners> <prize> <outputChannel> [file]`.

* **winners** - The number of winners to pick. Must be between `1` and `99`.
* **prize** - The prize being given away. Limited to `300` characters.
* **outputChannel** - The text (or announcement/news) channel the giveaway will be posted in.
* **file** *(optional)* - An image to attach to the giveaway.

Running this command does not post the giveaway right away. Instead, Cakey Bot opens an interactive giveaway builder only you can see, showing the following fields with a "Modify" button next to each one:

* **Prize**
* **Description**
* **Winners**
* **Duration** - defaults to `1d` (1 day). Accepts human-readable durations such as `1d5h30s` or `3w5d`.
* **Image**
* **Ping Role** - a role to mention in the announcement when the giveaway is posted.
* **Required XP Level** - defaults to `0` (no requirement).
* **Required Role** - defaults to `N/A` (no requirement).

Once you're happy with the settings, click **Create Giveaway** to post it to the selected channel, or **Cancel Giveaway** to discard it. Only the person who ran the command can modify or finalize that giveaway's builder.

> The Ping Role is only used to mention the role in the announcement message and is not saved for later - it cannot be changed once the giveaway has been posted.
{.is-info}

# Entering a Giveaway

Members can enter any active giveaway by clicking the 🎉 button on the giveaway message. Clicking it again removes their entry, allowing them to leave a giveaway they've already entered.

If a giveaway has a **Required Role** and/or **Required XP Level** set, members must meet those requirements before they're allowed to enter:

* **Required Role** - the member must have the specified role.
* **Required XP Level** - the member's level (based on your server's [leveling](/en/feature/leveling) system) must be equal to or higher than the required level. This is only enforced if leveling is enabled on your server.

> There is no invite requirement, message-count requirement, or blacklist role support for giveaways - only an optional required role and/or required level.
{.is-info}

# Managing Giveaways

## Listing Active Giveaways
Use `/giveaway list` to view every currently active giveaway in the server, including a link to the giveaway message, host, prize, and when it ends.

## Viewing Entries
Use `/giveaway list-entries <giveaway>` to get a text file listing every user currently entered into a giveaway (active or ended).

## Ending a Giveaway Early
Use `/giveaway end <giveaway>` to end a giveaway immediately instead of waiting for its duration to run out. This picks winners right away and locks the giveaway the same way it would naturally ending.

## Rerolling Winners
Use `/giveaway reroll <giveaway> [count] [winner]` on an ended giveaway to pick new winner(s):

* Leave both **count** and **winner** empty to reroll the same number of winners as the original giveaway.
* Set **count** (`1`-`30`) to reroll a specific number of winners instead.
* Set **winner** to replace one specific winner with a newly picked entrant instead of rerolling everyone.

> Once a giveaway has been posted, its prize, duration, or winner count can no longer be edited directly - only `/giveaway end` and `/giveaway reroll` can act on a live/ended giveaway.
{.is-info}

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /giveaway create | Creates a new giveaway using an interactive builder. | \<winners> \<prize> \<outputChannel> [file] | ManageEvents |
| /giveaway end | Ends a giveaway early and picks winners immediately. | \<giveaway> | ManageEvents |
| /giveaway list | Lists all currently active giveaways. | N/A | ManageEvents |
| /giveaway list-entries | Lists all users entered into a giveaway. | \<giveaway> | ManageEvents |
| /giveaway reroll | Rerolls the winner(s) of an ended giveaway. | \<giveaway> [count] [winner] | ManageEvents |
