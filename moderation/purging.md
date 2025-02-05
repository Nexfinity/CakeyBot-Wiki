---
title: Purging
description: 
published: 1
date: 2025-02-05T00:40:26.647Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:11:39.725Z
---

# Basic Purging
You can purge any amount of messages (up to 100) by typing `/purge any <amount>`. This will delete the specified number of messages as long as they are not older than 2 weeks and are not pinned.

# Advanced Purge Filters
If you only want to purge specific messages that meet certain conditions you can use an advanced purge filter by typing `/purge <type> <amount>`. You can view a list of advanced filters below:

* Links (Any well-formatted URL/Link)
* Invites (Discord invite links)
* Images (Any messages that have an image/file attached)
* Mentions (Any messages that contain at least 1 user mention)
* Embeds (Any messages that contain an embed)
* Self (Any messages that were sent by Cakey Bot)
* Bots (Any messages that were sent by a bot)
* Components (Any messages that have buttons or selection dropdowns)
* User (Any messages that were sent by the specified user)
  * **Special Format:** `/purge user <user id>`
* Until (Deletes every message between the command and the specified message ID)
  * **Special Format:** `/purge until <message id>`
* Between (Deletes every message between the specified message IDs)
  * **Special Format:** `/purge between <message id> <message id>`

> Sometimes Cakey Bot will purge fewer messages than the number you specify. This could be due to a few reasons:
> \* There are not enough messages that meet the specified filter
> \* Some messages may be older than 2 weeks within the specified amount
> \* Some messages may be "pinned" within the specified amount
{.is-info}

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command            | Description                                                                | Usage                           | Permission     |
| :----------------- | :------------------------------------------------------------------------- | :----------------------------: | :-------------: |
| /purge any         | Delete a number of messages in the channel.                               | \<amount> [reactions-only]                        | Administrator |
| /purge between     | Delete every message between the two given message IDs. (Includes the two given) | \<first-message-id> \<second-message-id> [reactions-only] | Administrator |
| /purge bots        | Delete messages sent by any bots in the channel.                          | \<amount> [reactions-only]                        | Administrator |
| /purge components  | Delete messages that contain components. (buttons/selects).               | \<amount> [reactions-only]                        | Administrator |
| /purge embeds      | Delete messages containing rich embeds in the channel.                    | \<amount> [reactions-only]                        | Administrator |
| /purge images      | Delete a number of images in the channel.                                 | \<amount> [reactions-only]                        | Administrator |
| /purge invites     | Delete server invites posted in the channel.                              | \<amount> [reactions-only]                        | Administrator |
| /purge links       | Delete a number of links posted in the channel.                           | \<amount> [reactions-only]                        | Administrator |
| /purge mentions    | Delete messages with mentions in the channel.                             | \<amount> [reactions-only]                        | Administrator |
| /purge self        | Delete messages sent by Cakey Bot in the channel.                         | \<amount> [reactions-only]                        | Administrator |
| /purge until       | Delete every message after the given message ID.                          | \<message-id> [reactions-only]                    | Administrator |
| /purge user        | Delete messages sent by given user.                                       | \<user> \<amount> [reactions-only]                | Administrator |
