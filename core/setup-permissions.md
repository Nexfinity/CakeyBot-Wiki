---
title: Setup Permissions
description: 
published: 1
date: 2023-05-23T03:30:46.940Z
tags: 
editor: markdown
dateCreated: 2023-05-21T21:30:23.705Z
---

# Overview
By default most of Cakey Bot's commands will be available to most users and will be enabled in every channel. However, some of the more sensitive commands such as moderation commands will be locked/hidden to users who have access to ban, mute or manager other members of the server. In order to hide/disable specific commands you can either use Discord native UI to adjust command permissions or you can use our custom `/perms` commands. We have included guides for both methods below.

# Discord Integration Permissions
In order to configure permissions with Discord's native UI you can follow these steps:
1. Open up "Server Settings"
2. Go to Apps->Integrations
3. Select Cakey Bot
4. Find the command you want to adjust permissions for and click it
5. Set your desired permissions

If you would like a more detailed guide for using Discord's native UI you can check out Discord's own blog post on the feature [here](https://discord.com/blog/slash-commands-permissions-discord-apps-bots).

# /perms Command
> The `/perms` command is just a different method of setting commands. Behind the scenes it uses the same native Discord permission system and any changes will be the same/synced between the two methods.
{.is}

Cakey Bot's `/perms commands` slash command lets you manage who can run commands and where they can run the commands. It plugs into Discord's command permissions API so users who can't run commands won't see them. If you would like to directly edit the commands in Discord, instead of using Cakey Bot's tools, you can use the "Discord Integration Permissions" method listed above. 

## Authorization 
After you run a `/perms commands *` command for the first time, you'll be prompted to authorize Cakey Bot, simply click the "Authorize" button on the error message then click "Authorize" in the menu that pops-up and re-run the command.
![an error message reading "Failed to Get Command Permissions: CakeyBot needs your permission to edit some server data, like command permissions. To authorize it please click the button below." A button marked 'Authorize' is below it.](/perms-failed-message.png)

## Viewing Permissions { #view-perms-link }

To view permissions you need to run `/perms commands <type> command-id:<command>`, where type is the kind of permission you want view, and command is selected from the list of options given to you. For instance if you ran `/perms commands channel command-id: play` you would get a responce like this:
![perms-empty.png](/perms-empty.png)
(note: you need to type the word "play" in this example to ensure your selecting a command, and not the word play)

## Adding Permissions
To add permissions you need to open the permission menu, as explained in the [Viewing Permissions](#view-perms-link) section, then click the 'Add <Channels/Roles/Users>' button, select allow/deny, and apply the permissions. For instance if a recent bout of music-spam in `#bug-report` makes you want to block `/play` there you just need to:
1. Open the Permissions Menu (see [Viewing Permissions](#view-perms-link))
1. Select 'Add Channels`
1. Click 'Deny' so that you stop command use, instead of allowing it
1. And select the channel(s) you want to modify (up to 25 at a time!)
![perms-selecting.png](/perms-selecting.png)
After clicking out of the menu your changes will be applied. Because of a Discord issue, changing permissions can take up to 30s, so make sure you select everything you need.

## Removing Permissions
To remove permissions you need to open the permission menu, as explained in the [Viewing Permissions](#view-perms-link) section, then click the 'Remove <Channels/Roles/Users>' button. To remove the permission added you just added you need to 
1. Open the Permissions Menu (see [Viewing Permissions](#view-perms-link))
1. Select 'Remove Channels`
1. Select `bug-report` from the menu that appears
![perms-remove-selecting.png](/perms-remove-selecting.png)
After clicking out of the menu your changes will be applied. Because of a Discord issue, changing permissions can take up to 30s, so make sure you select everything you need.