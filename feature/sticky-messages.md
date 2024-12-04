---
title: Sticky Messages
description: 
published: 1
date: 2024-12-04T03:39:31.016Z
tags: 
editor: markdown
dateCreated: 2024-03-12T18:44:40.360Z
---

# Overview
Sticky messages are a feature that ensures important information remains visible at the bottom of a channel, regardless of new messages being sent. When enabled, the bot will automatically re-post the designated sticky message whenever new messages are added to the chat, maintaining its visibility. This is particularly useful for announcements, server rules, or critical updates that need constant attention. Users can set or update the sticky message content through simple bot commands, making it easy to keep the community informed and organized.

# Usage
## Creating Sticky Messages
To create a sticky message, use the `/stickymessage create <message-text> [channel] [embed-url] [delay] [min-messages]` command. You can view a description of the parameters below:
* `message-text`: The text of the message to be stickied.
* `channel`: The channel to sticky the message in (or current if none is provided).
* `embed-url`: The embed URL for the message. <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>
* `delay`: The delay between reposting the sticky message in seconds.
  * Default: 20 seconds
  * 5-60 seconds <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>
* `min-messages`: The minimum amount of messages between sticky messages.
  * Default: 8
  * 3-100 messages <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>

Example: `/stickymessage create "Welcome to the channel! Please read the rules." #general 30 10`

## Listing Sticky Messages
To list all current sticky messages, use the `/stickymessage list` command.
This command will display all sticky messages currently set in the server along with their respective IDs.

## Deleting Sticky Messages
To delete a sticky message, use the `/stickymessage delete <id>` command with the message ID. Where ID is the unique identifier of the sticky message to be deleted.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /stickymessage create | Create a new sticky message. | \<message> [channel] [embedUrl] [delay] [minMessages] | ManageServer or Administrator | 
| /stickymessage delete | Delete the specified sticky message. | \<stickyMessageId> | ManageServer or Administrator | 
| /stickymessage list | Get a list of all sticky messages in the server. | N/A | ManageServer or Administrator | 