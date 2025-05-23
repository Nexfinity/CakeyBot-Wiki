---
title: Anti-Raid
description: 
published: 1
date: 2025-02-17T07:31:58.771Z
tags: 
editor: markdown
dateCreated: 2023-12-20T10:17:53.684Z
---

# Overview
The Anti-Raid feature serves as a robust defense mechanism against coordinated attacks on community. By implementing a suite of customizable checks against users and message content, it effectively detects and mitigates common Anti-Raid attacks used on Discord, safeguarding your community and maintaining a positive user experience.

With the capability to monitor user joins, message activity, and other suspicious behaviors, our Anti-Raid feature allows you to stop attacks against your server quickly when they occur. Whether it's detecting mass influxes of new users, identifying patterns in message spam, or flagging accounts created en masse, this feature provides granular control to combat raid attempts effectively.

Additionally, the ability to pause invites or timeout offending users enables you to halt disruptive activities quickly and giving your moderators time to review the offending content at a later point.

# User Join Settings
## Mass Joins
This will check if too many users join your server within the specified time period. The settings you can configure include:
* Minimum User Limit - The amount of users to join within the specified time period to trigger.
* Time Limit - The timeframe to check for number of users joining around the same time.
* Pause Invites Duration - This is how long invites will be paused for when the check has been triggered. This can prevent new joins.
* Notification Channel - Raid alerts for this check will be sent to this channel.
* Role Ping - This role will be pinged/mentioned when the check has been triggered. (This requires a notification channel to be set.)

## Same Account Creation Time
This will check if multiple users were created on the same day when they join at the same time. This can be useful to detect when users were bulk created on the same day and used for raiding purposes. The settings you can configure include:
* Minimum User Limit - The amount of users to join within the specified time period to trigger.
* Time Limit - The timeframe to check for number of users joining around the same time.
* Percentage Trigger - The percentage of users who share the same account creation date.
* Pause Invites Duration - This is how long invites will be paused for when the check has been triggered. This can prevent new joins.
* Notification Channel - Raid alerts for this check will be sent to this channel.
* Role Ping - This role will be pinged/mentioned when the check has been triggered. (This requires a notification channel to be set.)

# Message Settings
## Message Spam
This check will trigger when a user spams the specified amount of messages across any number of channels within your server within the given time period. The settings you can configure include:
* Minimum Message Limit - The amount of messages sent within the specified time period to trigger. (This is global across the server, not per-channel)
* Time Limit - The timeframe to check for number of users joining around the same time.
* Timeout User Duration - This is how long the user will be timed out for when the check has been triggered. This can prevent new messages.
* Notification Channel - Raid alerts for this check will be sent to this channel.
* Role Ping - This role will be pinged/mentioned when the check has been triggered. (This requires a notification channel to be set.)
* Ignored Roles & Channels - This is a list of channels or roles where this check will be ignored.

## Other Checks
This will check the content of messages sent by different users to see if they are similar. This can be effective when a raid contains multiple user accounts all sapmming the same message. The settings you can configure include:
* Similarity Limit - This will trigger if two the last X amount of messages contained the exact same content.
* Fuzzy Score Limit - This is a rough calculation of how similar messages are to each other. This can be helpful if the messages spam the same text/content but ping different users each time.
* Mention Spam Limit - This is how many mentions a message need to contain in order to trigger. The mentions do not have to be unique.
* Timeout User Duration - This is how long the user will be timed out for when the check has been triggered. This can prevent new messages.
* Notification Channel - Raid alerts for this check will be sent to this channel.
* Role Ping - This role will be pinged/mentioned when the check has been triggered. (This requires a notification channel to be set.)
* Ignored Roles & Channels - This is a list of channels or roles where this check will be ignored.