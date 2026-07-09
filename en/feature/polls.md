---
title: Polls
description: Create Discord polls with Cakey Bot - simple yes/no polls, advanced multi-option polls with reactions, and native Discord polls with timers and multi-select support.
published: 1
date: 2026-07-09T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-07-09T00:00:00.000Z
---

# Overview

Cakey Bot offers three poll types to suit different use cases — a quick yes/no poll, a fully custom multi-option poll using emoji reactions, and a native Discord poll with a built-in timer. Any server member can create a poll without needing special permissions.

> Cakey Bot requires the **`Add Reactions`**, **`Send Messages`**, and **`Embed Links`** permissions in the channel where the poll is posted.
{.is-warning}

# Poll Types

## Simple Poll
`/poll simple <question>`

Posts a quick yes/no poll as an embed. Cakey Bot adds three reactions automatically: 👍 (yes), 👎 (no), and 🤷 (unsure). Members vote by clicking a reaction.

- **Question limit:** 300 characters

## Advanced Poll
`/poll advanced <question> <response1> <response2> [response3–10]`

Posts a custom multi-option poll as an embed. You provide the question and between 2 and 10 answer options. Cakey Bot adds a regional indicator emoji (🇦, 🇧, 🇨 ...) for each option, which members click to vote.

- **Question limit:** 300 characters
- **Options:** 2 minimum, 10 maximum
- **Option length:** 55 characters each

## Discord Poll
`/poll discord <hours> <question> <response1> <response2> [response3–10] [multiselect]`

Posts a poll using Discord's native poll system. The poll runs for a set duration and shows live vote counts. Once the timer expires, voting closes automatically and Discord displays the final results.

- **Duration:** 1–168 hours (up to 7 days)
- **Question limit:** 300 characters
- **Options:** 2 minimum, 10 maximum
- **Option length:** 55 characters each
- **Multi-select:** Optional — when enabled, members can vote for more than one option

> Discord native polls cannot be ended early or modified after posting. Use `/poll advanced` if you need more control.
{.is-info}

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /poll simple | Posts a yes/no/unsure reaction poll. | \<question> | None |
| /poll advanced | Posts a custom multi-option reaction poll. | \<question> \<response1> \<response2> [response3-10] | None |
| /poll discord | Posts a native Discord timed poll. | \<hours> \<question> \<response1> \<response2> [response3-10] [multiselect] | None |
