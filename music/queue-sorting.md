---
title: Queue Sorting
description: 
published: 1
date: 2025-04-30T10:50:40.643Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:07:47.675Z
---

# Overview

Cakey Bot has several sorting methods to help you keep your queue clean and organized. You can also bulk remove songs from the queue using these filters too!

# Queue Sorting
These options allow you to re-sort songs that are currently in the queue. It will not affect the currently playong song.

| Subcommand | Description                                                                 | Command Example                                     | Requires Arguments |
|------------|-----------------------------------------------------------------------------|----------------------------------------------------|--------------------|
| `title`    | Sorts the queue by song titles (A–Z or Z–A).                                | `/sortqueue title asc`                             | Yes (`asc/desc`)   |
| `author`   | Sorts the queue by the song author (A–Z or Z–A).                            | `/sortqueue author desc`                           | Yes (`asc/desc`)   |
| `length`   | Sorts the queue by song duration (shortest to longest or vice versa).       | `/sortqueue length asc`                            | Yes (`asc/desc`)   |
| `reverse`  | Reverses the entire queue order.                                            | `/sortqueue reverse`                               | No                 |
| `swap`     | Swaps the positions of two songs in the queue by their track IDs.           | `/sortqueue swap 2 5`                              | Yes (2 track IDs)  |

# Queue Cleanup
These options allow you to remove a few songs or bulk remove a ton of songs from the queue using a few different filters. This can help remove spam and keep the queue clean overall.

| Subcommand   | Description                                                                                                          | Command Example                       | Requires Arguments         |
|--------------|----------------------------------------------------------------------------------------------------------------------|----------------------------------------|----------------------------|
| `first`      | Removes the very first song in the queue.                                                                            | `/remove first`                        | No                         |
| `last`       | Removes the last song in the queue.                                                                                  | `/remove last`                         | No                         |
| `single`     | Removes a specific song from the queue by its track ID.                                                              | `/remove single 4`                     | Yes (1 track ID)           |
| `range`      | Removes a range of songs from the queue using their numeric track IDs.                                               | `/remove range 2 6`                    | Yes (2 track IDs)          |
| `duplicates` | Removes duplicate or repeat songs from the queue.                                                                    | `/remove duplicates`                   | No                         |
| `userleft`   | Removes all songs added by users who are no longer in the voice channel with the bot.                               | `/remove userleft`                     | No                         |
| `user`       | Removes all songs added by a specific user.                                                                          | `/remove user @Username`               | Yes (user mention or ID)   |
| `keyword`    | Removes all songs where the title contains a specific keyword (e.g., to filter inappropriate content).               | `/remove keyword loud`                 | Yes (keyword string)       |

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