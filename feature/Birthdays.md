---
title: Birthdays
description: 
published: 1
date: 2023-02-01T03:37:03.938Z
tags: 
editor: markdown
dateCreated: 2023-01-09T01:24:46.396Z
---

# Overview
You can configure Cakey bot to announce birthdays for your users. All birthdays are retricted to the server you set them in. this means you must manually set your birthday in every server that you would like it announced in. Before you can use any birthday commands, a server admin must enable the feature by selecting a birthday announcement channel.

# Usage
## Birthday announcement channel
The birthday announcement channel is where all of the birthday announcements will be sent in your server. You MUST set a birthday channel before any of the birthday commands can be used. If you do not set an announcement channel then birthdays will not be announced. The birthday channel can be set on the **Bot Settings** page of the [web dashboard](https://cakeybot.app/dashboard/public) or by using the `/birthday channel <channel>` command.
> Note: Due to a Discord limitation you can't disable the birthday announcement channel by using the `/birthday channel` command. You will have to set it to "**None**" in the [web dashboard](https://cakeybot.app/dashboard/public).
{.is-info}

## Setting your birthday
You can set your own birthday by running the `/birthday set <date>` command. You can also change or update your birthday by running this command again and using the updated date.
> The date MUST be formatted like `MM/DD/YYYY`. Time is not required and announcements will be sent to servers at 12:01 AM EST.
{.is-info}

## View upcoming birthdays
You can view upcoming birthdays with the `/birthday next` command. By default it will show the next 3 birthdays though you can specify a limit between 1 and 10.

## Remove your own birthday or another user's birthday
You can remove your birthday by running the `/birthday remove` command. 
In addition to this you can remove another user's birthday by running `/birthday remove <user>`, however you must have **Manage Server** permission to remove the birthday of another user.

# Birthday Role
You can also have Cakey Bot assign a temporary birthday role to users on the day of their birthday! This role will be added to the user when the announcement for their birthday is sent, and it'll be remvoed when the birthdays for the next day are checked. In order to set a birthday role you can either use the `/birthday role <role>` command or you can configure it on the birthday page of the [web dashboard](https://cakeybot.app/dashboard/public).

A birthday role is NOT required for birthday announcements to be made. Announcements will be sent regardless if a role is set or not.

> Note: Due to a Discord limitation you can't disable the birthday auto role by using the `/birthday role` command. You will have to set it to "**None**" in the [web dashboard](https://cakeybot.app/dashboard/public).
{.is-info}