---
title: Auto Responder
description: 
published: 1
date: 2025-04-30T10:33:30.908Z
tags: 
editor: markdown
dateCreated: 2022-10-18T07:56:56.699Z
---

# Overview

This feature allows you to set up custom triggers on Discord that Cakey Bot can automatically respond to. For example, you can make Cakey Bot respond to messages such as `wot` with a link to a funny gif. You can also set some flags to determine what types of messages Cakey Bot will respond to.

![image.png](/dash/autoresp/image.png)

# Setup

> You will need **`Manage Server`** or **`Administrator`** permission to manage servers and auto responders.
{.is-warning}

1. Login to the web dashboard on the [main website here](https://cakey.bot/dashboard/public).
2. Click on the server you want to edit auto responders on.
3. Go to the "Auto Responder" page.
4. You can then create, delete, and edit any responses on this page. You can get an overview of any flags that are available below.&#x20;

# Flags

> Note: Only a single auto responder will ever trigger on a given message, even if the message meets the requirements of multiple auto responders. This selection is prioritized by the lowest ID of any matching responders.
{.is-info}

| Flag Type                   | Description                                                                                                                        | File Extensions                                                                                                                                                     |
| :--------------------------| :---------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Exact Match                | Default behavior, looks for exact match strings                                                                                    | –                                                                                                                                                                   |
| Contains                   | Will search the entire message to see if it contains this string/trigger                                                           | –                                                                                                                                                                   |
| Starts With                | Will check to see if the message begins with this string/trigger                                                                   | –                                                                                                                                                                   |
| Ends With                  | Will check to see if the message ends with this string/trigger                                                                     | –                                                                                                                                                                   |
| Contains Files             | Will check to see if the message contains any files/attachments (i.e. documents, images, videos)                                   | –                                                                                                                                                                   |
| From Webhook               | Will check to see if the message was sent by a webhook                                                                             | –                                                                                                                                                                   |
| Contains user mention      | Will check to see if the message contains a user mention                                                                           | –                                                                                                                                                                   |
| Contains channel mention   | Will check to see if the message contains a channel mention                                                                        | –                                                                                                                                                                   |
| Contains role mention      | Will check to see if the message contains a role mention                                                                           | –                                                                                                                                                                   |
| Wildcard Contains          | Searches message with wildcard support: `*` (any chars), `?` (single char), use `\?` for literal question marks                    | –                                                                                                                                                                   |
| Regex Match                | A more powerful version of wildcard, allows full regular expressions                                                               | –                                                                                                                                                                   |
| Contains image attachment  | Checks if attachments include image formats                                                                                        | .jpg, .jpeg, .png, .gif, .bmp, .tiff, .ico, .svg, .webp, .heic, .heif, .jfif, .exif, .raw, .psd, .ai, .eps                                                          |
| Contains video attachment  | Checks if attachments include video formats                                                                                        | .mp4, .avi, .mkv, .mov, .wmv, .flv, .webm, .m4v, .mpeg, .mpg, .3gp, .rm, .swf, .vob, .ts                                                                            |
| Contains audio attachment  | Checks if attachments include audio formats                                                                                        | .mp3, .wav, .flac, .aac, .m4a, .wma, .ogg, .alac, .aiff, .opus, .mid, .midi, .amr, .ape                                                                             |
| Contains text attachment   | Checks if attachments include document/text formats                                                                                | .txt, .csv, .json, .xml, .html, .htm, .md, .log, .rtf, .doc, .docx, .pdf                                                                                            |
| Contains executable attachment | Checks if attachments include executable formats                                                                              | .exe, .msi, .bat, .sh, .app, .jar, .com, .cmd, .vb, .vbs, .ps1                                                                                                       |


> **Note:** When using the "Contains Files", "From Webhook", and "Contains X mention", the "Command" field is still required. However, it is not used to actually trigger the auto response. It's purely a cosmetic property.&#x20;
{.is-warning}

# Limitations/Restrictions

* You can't have duplicate tags with the same name
* Auto Responders are also limited to Discord's message character limit
* Messages sent by bots or webhooks will be ignored

# Placeholders/Variables

Auto Responder will work with BOTH **Basic Placeholders** & **Advanced Placeholders**. Placeholders can be included in the response section and can modify the behavior/output of the response. You can find the list of supported placeholders [here](https://wiki.cakey.bot/en/placeholders).

# Using Emoji/Emotes in Responses

Emoji/Emotes CAN be used in auto responders. However, it requires slightly more work due to how discord parses emotes. Normally in Discord, you could just type `:lel:` or `:smile:` to get an emote, however in Cakey Bot, neither of these will work. In order to get valid emojis you have to send the emojis in discord but place a backward slash in front of it to get the emote's full ID. Like so: `\:lel:` or `\:smile:` which will produce these results: `<:lel:408424717217693717>` or for Unicode emoji: `😄` . Once you have the full emoji id or the raw Unicode output, you can paste these into Cakey Bot's web dashboard and they should work as long as Cakey Bot is in a server that has that custom emote in it.

> It is worth noting that Cakey Bot can use emojis in between servers (similar to nitro users). So if you have an emoji in Server #1, you can use that emoji in a response for Server #2 if Cakey bot is in both of those servers.
{.is-info}

# Using Images in Responses

To use images in responses, you can simply just type the image URL/link like you would in a normal message. If you have the file on your local machine/PC but no URL/link, you can upload it to an image hosting website (such as [Imgur](https://imgur.com/upload)) and paste the URL they provide into the response. Cakey Bot should automatically embed the image in Discord's client if it's a valid URL/image.

# Custom Embeds <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>
You can include an optional embed on responses by following the steps below:

1. Follow the instructions at the top of this page to sign in to the dashboard.
2. Use our custom embed editor to design your embed on the dashboard.
3. Copy your browser URL or click the "**Get Data Link**" button in the dropdown menu and copy the URL from there.
4. Create an auto responder like you normally would and paste the URL you copied in the last step into the **Embed URL** text field.

> Custom embeds will work with all **Basic Placeholders**. You can find the list of supported placeholders [here](https://wiki.cakey.bot/en/placeholders). Custom embeds will **NOT** work with the **Advanced Placeholders**.
{.is-info}

# Bulk Import/Export

> You must apply via support tickets to get access to Bulk Import. Anyone can use Bulk Export without applying. This is to decrease potential abuse.
{.is-info}

## Limitations/Guidelines

* File **MUST** be in CSV format.
* File **MUST** be formatted with all of the required columns.
* Additional/extra columns will be ignored.
* Any fields that have too many characters will be trimmed. Column limits:
  * **Command:** 200 characters
  * **Response:** 2,000 characters
* Any fields that exceed the character will NOT work after importing.
* Bulk importing can **NOT** be canceled or reversed once started.
* Any broken commands will have to be individually deleted or fixed _after_ the import is finished.
* There is a limit of **500 commands** per bulk import.

## What do the columns/fields and their values mean?

The template CSV file and bulk exported CSVs will have a few different columns with various restrictions. These are explained below:

* Status
  * This determines whether or not the command/response is "enabled" or "disabled"
  * Acceptable values:
    * 0 - Disabled
    * 1 - Enabled
* Command
  * This is the command/trigger phrase for a response.
  * It must be less than 200 characters.
* Flags
  * These are only used for Auto Responders, they map directly to the Auto Responder [flags](#flags).
  * Acceptable values:

    | Value | Flag Name                   |
| :---- | :-------------------------- |
| 1     | Exact Match                 |
| 2     | Contains                    |
| 3     | Starts With                |
| 4     | Ends With                  |
| 5     | Contains Files             |
| 6     | From Webhook               |
| 7     | Contains user mention      |
| 8     | Contains channel mention   |
| 9     | Contains role mention      |
| 10    | Wildcard Contains          |
| 11    | Regex Match                |
| 12    | Contains image attachment  |
| 13    | Contains video attachment  |
| 14    | Contains audio attachment  |
| 15    | Contains text attachment   |
| 16    | Contains executable attachment |

* Response
  * This is the response phrase for a trigger/command.
  * It must be less than 2,000 characters.
* Embed
  * This is an optional field for responses that use a Cakey Bot [custom embed](#custom-embeds). Embeds can only be used by Premium Servers regardless if a value is set here or not.
  * The URL must start with `https://cakey.bot/dashboard/publicembed-editor?data=`