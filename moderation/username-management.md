---
title: Username Management
description: 
published: 1
date: 2023-11-12T16:37:31.382Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:12:51.806Z
---

# Username Management
You can bulk (or even singlularlly) managed user nicknames in your server with the `/managenicks` command. There's tons of pre-defined filters as well as simple tools to just clear a nickname or set it to something specific. All filters can be applied to a singular user, all users with a specific role or to all users in the server.

## Set
This command will set the specified user or user's nickname to the exact string that you specify in the command.

## Clear
This command will clear the specified user or user's nickname to their base username. This can be useful if you accidentally set everyones nickname to something incorrectly.

## Alpha-Numeric
This command will strip all non-alphanumeric characters from the specified user or user's nickname. This can be useful if you have users who are using fancy unicode characters in their name that can be difficult to read. 
> Note: If the user has no alpha-numeric characters in their name at all, their nickname will be set to "AlphaNum Name Please".
{.is-info}

## Dehoist
> See **Username Dehoisting** section below for more info on this specific filter.

# Username Dehoisting

Username dehoisting gives you the ability to manually or automatically dehoist users who use special characters in their usernames/nicknames to show at the top of the user list.

## Manually Dehoist

You can manually dehoist users by typing the `/managenicks dehoist` command in Discord. There are a few different types of dehoisting you can do:

* All
  * This will dehoist every user in the server. Note that this command may take several minutes to complete, especially in a large server.
* User \<user>
  * This will just dehoist that specific user.
* Role \<role>
  * This will dehoist all users who have the specified role. Note that this command may take several minutes to complete, especially in a large server.

## Automatically Dehoist

You can setup automatic dehoisting by logging into our [web dashboard](https://cakey.bot/dashboard/public) and going to the "Auto Mod" page. Once on the page, simply enable the "Auto Dehoist" feature and Cakey Bot will start automatically dehoisting users.

> Note: Auto Dehoist will only apply to new users in the server or suers who change their nickname AFTER the feature has been enabled. For existing users you will need to manually dehoist them. After existing users have been dehoisted, auto dehoist will take affect for new nickname changes.
{.is-info}