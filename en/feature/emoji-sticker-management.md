---
title: Emoji & Sticker Management
description: Manage Discord server emojis and stickers with Cakey Bot - create, delete, rename, lock, export, import, and view stats via slash commands.
published: 1
date: 2026-07-09T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-07-09T00:00:00.000Z
---

# Overview

> Make sure that Cakey Bot has the **`Manage Emojis and Stickers`** permission.
{.is-warning}

Cakey Bot lets you manage your server's custom emojis and stickers directly from Discord using the `/emote` and `/sticker` commands. You can create, delete, rename, and lock emotes, view usage statistics, and bulk export/import your entire emoji or sticker collection as a zip file.

> All `/emote` and `/sticker` commands require the **`ManageEmojisAndStickers`** permission, since it's set as the default required permission for both command groups.
{.is-info}

# Emote Commands

## Create
The `/emote create <file> <name>` command creates a new custom emote from an uploaded image.
* `name` must be **2-30 characters** and can only contain letters, numbers, and underscores.
* The image must be **PNG, JPEG, JPG, or GIF** and no larger than **256 KB**.
* The server must have a free emote slot available.

## Delete
The `/emote delete <emote>` command deletes the specified emote from the server.

## List
The `/emote list` command sends a text file listing every emote in the server, including their ID, name, and URL.

## Rename
The `/emote rename <emote> <newName>` command renames the specified emote. The new name must be at least 2 characters.

## Lock
The `/emote lock <emote> [roleIds]` command restricts an emote so that only members with the specified roles can use it.
* `roleIds` is a semicolon-separated list of role IDs (e.g. `123456789012345678;234567890123456789`).
* Omitting `roleIds` removes the restriction, allowing everyone to use the emote again.

## Big
The `/emote big <emote>` command displays a large version of the specified emote along with its name and ID.

## Download
The `/emote download <emote>` command provides direct download links for the emote in multiple image formats (PNG/JPG/WEBP, plus GIF for animated emotes) and sizes (16px up to 2048px).

## Export
The `/emote export` command downloads every emote in the server and packages them into a single zip file.

## Import
The `/emote import <zipFile>` command imports emotes from an uploaded zip file. Images are added until the server's free emote slots are used up; invalid file types, oversized files, and nested zips are skipped automatically.

## Stats
The `/emote stats` command shows overall emote usage statistics tracked by the bot: total uses, unique emotes used, average uses per emote, and the top emote overall, top Unicode emote, and top custom emote.

## Top
The `/emote top` command shows the top 10 most-used emotes tracked by the bot in the server.

# Sticker Commands

## Create
The `/sticker create <file> <name> <description>` command creates a new sticker from an uploaded image.
* `name` must be **2-30 characters**.
* `description` is required and must be at least 2 characters.
* The image must be **PNG, APNG, or GIF** and no larger than **256 KB**.
* The server must have a free sticker slot available.

## Delete
The `/sticker delete <sticker>` command deletes the specified sticker from the server.

## List
The `/sticker list` command sends a text file listing every sticker in the server, including their ID, name, and URL.

## Rename
The `/sticker rename <sticker> <newName>` command renames the specified sticker. The new name must be at least 2 characters.

## Big
The `/sticker big <sticker>` command displays a large version of the specified sticker along with its name and ID.

## Download
The `/sticker download <sticker>` command provides direct download links for the sticker in multiple image formats (PNG/JPG/WEBP) and sizes (16px up to 2048px).

## Export
The `/sticker export` command downloads every sticker in the server and packages them into a single zip file.

## Import
The `/sticker import <zipFile>` command imports stickers from an uploaded zip file. Images are added until the server's free sticker slots are used up; invalid file types, oversized files, and nested zips are skipped automatically.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /emote create | Creates a new emote from an uploaded image. | \<file> \<name> | ManageEmojisAndStickers |
| /emote delete | Deletes the specified emote. | \<emote> | ManageEmojisAndStickers |
| /emote list | Lists all emotes in the server as a text file. | N/A | ManageEmojisAndStickers |
| /emote rename | Renames the specified emote. | \<emote> \<newName> | ManageEmojisAndStickers |
| /emote lock | Restricts an emote to specific roles (or unlocks it). | \<emote> [roleIds] | ManageEmojisAndStickers |
| /emote big | Displays a large version of the specified emote. | \<emote> | ManageEmojisAndStickers |
| /emote download | Provides download links for the specified emote. | \<emote> | ManageEmojisAndStickers |
| /emote export | Downloads all server emotes as a zip file. | N/A | ManageEmojisAndStickers |
| /emote import | Imports emotes from an uploaded zip file. | \<zipFile> | ManageEmojisAndStickers |
| /emote stats | Shows emote usage statistics for the server. | N/A | ManageEmojisAndStickers |
| /emote top | Shows the top 10 most used emotes in the server. | N/A | ManageEmojisAndStickers |
| /sticker create | Creates a new sticker from an uploaded image. | \<file> \<name> \<description> | ManageEmojisAndStickers |
| /sticker delete | Deletes the specified sticker. | \<sticker> | ManageEmojisAndStickers |
| /sticker list | Lists all stickers in the server as a text file. | N/A | ManageEmojisAndStickers |
| /sticker rename | Renames the specified sticker. | \<sticker> \<newName> | ManageEmojisAndStickers |
| /sticker big | Displays a large version of the specified sticker. | \<sticker> | ManageEmojisAndStickers |
| /sticker download | Provides download links for the specified sticker. | \<sticker> | ManageEmojisAndStickers |
| /sticker export | Downloads all server stickers as a zip file. | N/A | ManageEmojisAndStickers |
| /sticker import | Imports stickers from an uploaded zip file. | \<zipFile> | ManageEmojisAndStickers |
