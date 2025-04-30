---
title: Sticky Messages
description: 
published: 1
date: 2025-04-30T11:11:22.562Z
tags: 
editor: markdown
dateCreated: 2024-03-12T18:44:40.360Z
---

# Overview
Sticky messages are a feature that ensures important information remains visible at the bottom of a channel, regardless of new messages being sent. When enabled, the bot will automatically re-post the designated sticky message whenever new messages are added to the chat, maintaining its visibility. This is particularly useful for announcements, server rules, or critical updates that need constant attention. Users can set or update the sticky message content through simple bot commands, making it easy to keep the community informed and organized.

# Usage
## Creating Sticky Messages
To create a sticky message, use the `/stickymessage create <message-text> [channel] [embed-url] [delay] [min-messages]` command. You can view a description of the parameters below:

| Parameter       | Description                                                                                      | Default Value | Min Value | Max Value | Premium Feature |
|-----------------|--------------------------------------------------------------------------------------------------|---------------|-----------|-----------|------------------|
| `message-text`  | The text content of the sticky message.                                                          | -           | -       | -       | No               |
| `channel`       | The channel where the sticky message will be posted. If not provided, uses the current channel.  | Current       | -       | -       | No               |
| `embed-url`     | An optional embed URL to attach to the sticky message.                                           | None          | -       | -       | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>               |
| `delay`         | The time delay in seconds between re-posting the sticky message.                                 | 20          | 5       | 60      | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>               |
| `min-messages`  | The minimum number of messages required before re-posting the sticky message.                    | 8           | 3       | 100     | <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>               |

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