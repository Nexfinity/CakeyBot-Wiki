---
title: Purging
description: 
published: 1
date: 2022-10-18T10:45:31.788Z
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
> - There are not enough messages that meet the specified filter
> - Some messages may be older than 2 weeks within the specified amount
> - Some messages may be "pinned" within the specified amount
{.is-warning}
