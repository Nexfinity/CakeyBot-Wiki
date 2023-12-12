---
title: Localization (Multi-Language)
description: 
published: 1
date: 2023-12-12T04:38:47.189Z
tags: 
editor: markdown
dateCreated: 2022-09-01T03:26:55.413Z
---

# Supported Languages

> New translations are constantly being added to the bot. This means some strings/phrases may not be translated yet especially for features that have been added recently.
{.is-info}

Cakey Bot (and our web dashboard) both support over 10 different languages. The language can be changed per-server and will apply for every user in that server. You can change the server's language from our web dashboard. Currently supported languages are listed below:

* English
* Dutch/Nederlands `(Vikthor)`
* German/Deutsch `(Marcel & MST2)`
* Korean/한국어 `(Johnmacro)`
* Greek/ελληνικά `(xxNikosGaming)`
* Swedish/Svenska `(Hampus)`
* Turkish/Türkçe `(Aleph & Oğuzhan)`
* Italian/Italiano `(GiorgioHerbie)`
* Arabic/العربية `(Sipancoolboy)`
* Romanian/Limba română `(Silviu200530)`
* Japanese/日本語 `(hikarun)`
* Ukrainian/Українська `(papip1)`
* Chinese Simplified/中文 `(Lukeee)`
* Portuguese/Português `(Kaiser)`
* Russian/Русский язык `(Misha133)`

We are adding more languages and you can contribute on our Crowdin page [here](https://crowdin.com/project/cakey-bot). Once the majority of a language is completed (>80% translated) on Github/Crowdin it will be added as an officially supported language. Crowdin and Github are frequently synced so you can contribute to whichever you find the easiest.

> If you plan to contribute, please follow the rules and formatting guidelines provided below in the **Formatting, Rules, Requirements** section.
{.is-warning}

# How Do I Translate?

1. Open the project on the Crowdin page [here](https://crowdin.com/project/cakey-bot).
2. Make any translations/edits/updates to your language
3. Wait for the submissions to be reviewed
4. Make any requested edits to your submissions (if requested by proof readers)
5. Wait for the strings to be merged into the production bot and enjoy!

# Formatting, Rules, Requirements

1. Please do not insert unnecessary punctuation into strings, unless it is
   required for that language
2. Any string that contains ` symbols, please leave them in the same position
   and don't remove them. Also do not change them to other symbols like ' or ",
   these are used to highlight certain text or to prevent "@everyone" pings from
   being used/abused. Removing or changing these could break formatting in Cakey
   Bot
3. If you encounter any placeholders like {0}, {1}, etc, keep them in the
   string. These are automatically replaced in the bot with text so
   `Requested by {0}#{1}` when used in the bot will be replaced with like
   `Requested by MrCake#1337`. For the website strings :data, :data2 and :name are 
   also common placeholders.
4. If you need more context/info about how/where a string is used to provide an
   accurate translation, you can create a discussion or issue oin the string or
   you can join our [Discord](https://cakey.bot/discord) and a proof reader will
   provide further info/screenshots.
5. Do not translate commands. Cakey Bot only accepts base commands in English.
   For example if the translation string is `Usage: /userinfo <user>`, you can
   translate the `Usage:` and `<user>` parts, but you must leave the command
   (`/userinfo`) in English.
6. Do not translate brand names (e.g. Discord, YouTube, Reddit) and be sure to keep any
   capitalization on them.
7. If you are unsure how you should format a specific string you can look at
   another language's file or you can open up a discussion. (You can also ask on
   our [Discord](https://cakey.bot/discord))
8. Don't translate emojis or emotes. This will cause them to break and display incorrectly to users.

# FAQ

**1) What if I don't see a section for my language?**

- You can join our [Discord](https://cakey.bot/discord) and create a ticket requesting for it to be added.

**2) What do the different files mean?**

- **strings.resx:** This file contains all translations that are used in Cakey Bot's responses on [Discord](https://discord.gg/Y3VdQAD).
- **web-strings.php:** This file contains all translations that are used on Cakey Bot's [Web Dashboard](https://cakey.bot/dashboard/public).
- **slash-commands.resx:** This file contains all translations that are used in the slash commands for Cakey Bot on [Discord](https://discord.gg/Y3VdQAD).

**3) Do I need permission to contribute?**

- Nope! Anyone can contribute, just be sure to follow our rules and formatting guidelines above.

**4) When do the translations get added to the bot/website?**

- If the language has already been accepted, they will periodically be added to the produciton servers when major changes have been made. Keep an eye on our website and bot news announcement channels on Discord.
- If the language hasn't been accepted yet, it will need to reach >70% of the strings being approved for it to be accepted and added as a language option.
  - Some accepted languages may have less than this due to new strings being added later. In these cases, the languages will _not_ be removed from the bot/website.