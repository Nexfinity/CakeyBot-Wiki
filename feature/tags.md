---
title: Tags
description: 
published: 1
date: 2025-04-30T11:14:00.159Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:21:24.448Z
---

# Overview

This feature allows you to set up a variety of "tags" that users can list and use to output pre-determined strings of text. This is useful for creating public FAQ responses without making a bunch of [Auto Responders](https://wiki.cakey.bot/en/auto-responder). Also, you can configure tags to be modified by different permission levels, unlike Custom Commands which can only be modified by server admins. The different permission tiers are listed below:

| Manage Own       | Manage All      | Description                                                                 |
|------------------|------------------|-----------------------------------------------------------------------------|
| Admins           | Admins           | Only administrators can manage tags. _(Default behavior)_                   |
| Mods             | Admins           | Moderators can manage their own tags; admins can manage all tags.           |
| Mods             | Mods             | Moderators can manage every tag, regardless of ownership.                   |
| Users            | Admins           | Users can manage their own tags; admins can manage all tags.                |
| Users            | Mods             | Users can manage their own tags; moderators can manage all tags.            |
| Users            | Users            | Any user can manage all tags, regardless of who created them.               |

> **Note:** These permissions only affect creating, deleting, and modifying tags. ALL users will be able to USE every tag regardless of who created the tag.
{.is-info}

# Create/Manage Tags (Web Dashboard)

1. Login to our [web dashboard](https://cakey.bot/dashboard/public).
2. Go to "Tags".
3. Click the "Add New Tag" button
4. Fill in the required information. All tags will require a name and a response.
5. Click "Create"

Once you have created tags, you can also modify them here.

# Create/Manage Tags (Bot/In-Discord)

You can manage and list tags using the following commands:

* To list all commands simply type `/tags` or `/tags list`.
* To create a tag type `/tags create`.
* To modify a tag type `/tags edit <tag>`.
* To delete a tag just type `/tags delete <tag>`.

To use a tag simply type `/tag <name>`.

# Limitations/Restrictions

* You can't have duplicate tags with the same name
* Tags are also limited to Discord's message character limit
* @User, @Role and @Everyone/@Here mentions are completely disabled in tags

# Using Emoji/Emotes in Tags

Emoji/Emotes CAN be used in Tags. However, it requires slightly more work due to how discord parses emotes. Normally in Discord, you could just type `:lel:` or `:smile:` to get an emote, however in Cakey Bot, neither of these will work. In order to get valid emojis you have to send the emojis in discord but place a backward slash in front of it to get the emote's full ID. Like so: `\:lel:` or `\:smile:` which will produce these results: `<:lel:408424717217693717>` or for Unicode emoji: `😄` . Once you have the full emoji id or the raw Unicode output, you can paste these into Cakey Bot's web dashboard and they should work as long as Cakey Bot is in a server that has that custom emote in it.

> It is worth noting that Cakey Bot can use emojis in between servers (similar to nitro users). So if you have an emoji in Server #1, you can use that emoji in a custom command in Server #2 if Cakey bot is in both of those servers.
{.is-info}

# Using Images in Tags

To use images in responses, you can simply just type the image URL/link like you would in a normal message. If you have the file on your local machine/PC but no URL/link, you can upload it to an image hosting website (such as [Imgur](https://imgur.com/upload)) and paste the URL they provide into the response. Cakey Bot should automatically embed the image in Discord's client if it's a valid URL/image.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command           | Description                                   | Usage           | Permission                |
| :---------------- | :------------------------------------------- | :-------------: | :-----------------------: |
| /tag              | Display the content for a tag.               | \<name>         | None                      |
| /tags create      | Create a new server tag.                     | N/A             | None                      |
| /tags delete      | Delete a server tag.                         | \<tag>          | None                      |
| /tags edit        | Modify a server tag.                         | \<tag>          | None                      |
| /tags info        | View info for a specific tag.                | \<tag>          | None                      |
| /tags list        | List server tags.                            | N/A             | None                      |
| /tags nuke        | Delete ALL tags in a server.                 | N/A             | ManageServer or Adminstrator |
| /tags prune       | Delete ALL tags from a user.                 | \<user>         | ManageServer or Adminstrator |
| /tags raw         | Display tag in raw format.                   | \<tag>          | None                      |
| /tags transfer    | Transfer one of your tags to someone else.   | \<tag> \<user>  | None                      |
| /tags user        | List the tags a user has made.               | \<user>         | None                      |