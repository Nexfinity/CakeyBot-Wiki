---
title: Reminders
description: 
published: 1
date: 2024-12-04T03:36:45.149Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:19:42.217Z
---

# Overview

Cakey Bot allows you to set reminders for yourself easily using the `/reminder` command. When you use this command, Cakey Bot will send you a Direct Message on the date and time that you use in the command along with whatever message you set.

# Usage

> If you block Cakey Bot or do not share any servers with Cakey Bot at the time that your reminder is sent, you will not receive it. Cakey Bot has to have access to message you directly to deliver the reminder as reminders are sent using Direct Messaging.
{.is-warning}

To create a reminder all you need to do is run the `/reminder <time> <text>` command. You will need to set an amount of time from this moment for Cakey Bot to remind you as well as a small block of text. Text is limited to 200 characters and there is no limit for the timeframe. Cakey Bot accepts most human-readable time frames, for example: `1d5h30s` or `3w5d`.

You can also view all of your current reminders with the `/reminder list` command.

You also have the ability to delete any of your existing reminders by using the `/reminder delete <remidnerId>` command.

![Reminder Example](/reminder_1.png)

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /reminder create | Creates a personal reminder for the time given. | \<time> \<text> | None | 
| /reminder delete | Deletes the selected reminder. | \<reminderId> | None | 
| /reminder list | List all of your current reminders. | N/A | None | 