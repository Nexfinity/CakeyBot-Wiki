---
title: Queue Sorting
description: 
published: 1
date: 2024-12-04T06:25:36.656Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:07:47.675Z
---

# Overview

Cakey Bot has several sorting methods to help you keep your queue clean and organized. You can also bulk remove songs from the queue using these filters too!

# Queue Sorting
These options allow you to re-sort songs that are currently in the queue. It will not affect the currently playong song.

## Title
This will sort all of the songs in the queue based on their title. You can sort by ASC or DESC using the `/sortqueue title <asc/desc>` command.

## Author
This will sort all of the songs in the queue based on their author. You can sort by ASC or DESC using the `/sortqueue author <asc/desc>` command.

## Length
This will sort all of the songs in the queue based on their total length/duration. You can sort by ASC or DESC using the `/sortqueue length <asc/desc>` command.

## Reverse
This will reverse the order of every song in the queue. You can reverse the queue by using the `/sortqueue reverse` command.

## Swap
This will allow you to swap the position of two different songs in the queue. You can do this by running the `/sortqueue swap <firstTrackId> <secondTrackId>` command.
>  You must use the numeric ID of the songs in the queue for this command.
{.is-info}

# Queue Cleanup
These options allow you to remove a few songs or bulk remove a ton of songs from the queue using a few different filters. This can help remove spam and keep the queue clean overall.

## First
This will remove the very first song in the queue. You can remove the first song by using the `/remove first` command.

## Last
This will remove the last song in the queue. You can remove the last song by using the `/remove last` command.

## Single
This will remove a specific song from the queue. You can remove the song by using the `/remove single <trackId>` command.

## Range
This will remove a a range of tracks from the queue. You can remove the range of songs by using the `/remove range <firstTrackId> <secondTrackId>` command.
>  You must use the numeric ID of the songs in the queue for this command.
{.is-info}

## Duplicates
This will remove any duplicate or repeat songs from the queue. You can remove the duplicates by using the `/remove duplicates` command.

## User Left
This will remove any songs that were added to the queue by any suers who are no longer in the voice channel with the bot. You can remove these songs by using the `/remove userleft` command.

## User
This will remove any songs that were added to the queue by a specific user. You can remove these songs by using the `/remove user <user>` command.

## Keyword
This will remove any songs where the title of the song contains the provided keyword. This can be useful to remove inappropriate or "ear rape" type songs. You can remove these songs by using the `/remove keyword <keyword>` command.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command                | Description                                                     | Usage                                   | Permission           |
| :--------------------- | :------------------------------------------------------------- | :------------------------------------- | :------------------- |
| /sortqueue author       | Sorts the queue based on the author.                           | <asc/desc>                              | Server Mod/DJ        |
| /sortqueue length       | Sorts the queue based on the length.                           | <asc/desc>                              | Server Mod/DJ        |
| /sortqueue reverse      | Sorts the queue in reverse of current order.                   | N/A                                     | Server Mod/DJ        |
| /sortqueue swap         | Swaps two different tracks in the queue.                       | \<firstIndex> \<secondIndex>              | Server Mod/DJ        |
| /sortqueue title        | Sorts the queue based on the title.                            | \<asc/desc>                              | Server Mod/DJ        |
| /remove dupes           | Removes any duplicate songs from the queue.                    | N/A                                     | None                 |
| /remove duplicates      | Removes any duplicate songs from the queue.                    | N/A                                     | None                 |
| /remove first           | Remove the first song from the queue.                          | N/A                                     | Server Mod/DJ        |
| /remove keyword         | Removes songs from the queue if their title contains the specified keyword. | \<keyword>                              | Server Mod/DJ        |
| /remove last            | Remove the last song from the queue.                           | N/A                                     | Server Mod/DJ        |
| /remove range           | Removes the range of songs from the queue.                     | \<song id> \<song id>                     | Server Mod/DJ        |
| /remove single          | Removes the given song from the queue.                         | \<song id>                               | Server Mod/DJ        |
| /remove user            | Removes songs from the queue that were added by the specified user. | \<user>                                 | Server Mod/DJ        |
| /remove userleft        | Removes songs from the queue if users are no longer in the voice channel. | N/A                                     | None                 |