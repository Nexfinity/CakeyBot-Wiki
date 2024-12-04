---
title: Muting
description: 
published: 1
date: 2024-12-04T03:34:57.677Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:14:40.491Z
---

# Muting

When you run the `/mute <user>` command, Cakey Bot will assign a mute role to that user preventing them from chatting/speaking in voice channels. Now, You might be asking "What role does Cakey Bot use for this?". This depends on a few factors:

1. If you have set a mute role in the web dashboard, Cakey Bot will use that role.
2. If you have not manually set a mute role, Cakey Bot will scan for any role with the name "Muted", if it finds one it will use that role.
3. If Cakey Bot does not find a "Muted" role, it will generate a brand new role with appropriate permissions

> Note: In order for Cakey Bot to mute a user several things must happen. Cakey Bot must have **`Manage Roles`** permission and Cakey Bot's highest role must be higher than the Mute role and the muted user's highest role.
{.is-info}

# Temporary Mutes/Timeouts

You can also mute people temporarily. It works exactly like normal muting above and requires the same setup/permissions but it will automatically remove the mute after the specified time. You can temporarily mute someone by using the `/timeout <user> <time> <opt:reason> <opt:isSilent>`command.

> Note: This command was previously known as `/tempmute`, it has now been replaced in favor of `/timeout` as it uses native Discord systems to mute the user which is more effective and reliable.
{.is-info}

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| / | TBD | N/A | None | 