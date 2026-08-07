---
title: Suggestions
description: Discord suggestion system with Cakey Bot - vote on suggestions, and accept/deny/duplicate/review decisions with reasons. Setup guide.
published: 1
date: 2026-08-07T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-08-07T00:00:00.000Z
---

# Overview

Suggestions let your members propose ideas and vote on them with a simple upvote/downvote embed. Staff can then accept, deny, mark as a duplicate, or put a suggestion under review - each decision updates the suggestion's embed with a colored status and an optional reason, and is recorded so it shows up in the dashboard's decision history.

> A Suggestion Channel must be configured before members can create suggestions - see [Configuring Suggestions](#configuring-suggestions) below.
{.is-warning}

# Configuring Suggestions

1. Login to our [web dashboard](https://cakey.bot/dashboard).
2. Go to the "Suggestions" page and set the **Suggestion Channel** where new suggestions will be posted. This is required - `/suggestion create` won't work until it's set.
3. On that same page, optionally set the **Suggestion Approved Channel** / **Suggestion Denied Channel** to forward a copy of accepted/denied suggestions there as well.

# Creating a Suggestion

Once a Suggestion Channel is configured, any member can run `/suggestion create` to open a form asking for a title and description. Submitting it posts an embed - always in the configured Suggestion Channel, regardless of which channel the command was run in - with upvote/downvote buttons, an **Approve**/**Deny** button pair, and a **Create Discussion Thread** button.

> If no Suggestion Channel is configured yet, `/suggestion create` shows an error explaining that an admin needs to set one up first, with a link to this article.
{.is-info}

# Voting

Members vote using the 👍/👎 buttons on a suggestion embed. Voting the opposite direction swaps your vote; clicking the same button again removes it. Vote counts are shown directly on the buttons.

# Deciding on a Suggestion

Members with the **Administrator** or **Manage Server** permission can decide on a suggestion two ways:

* **Buttons** - Click **Approve** or **Deny** directly on the suggestion embed. This updates the embed's color and footer immediately, but doesn't support attaching a reason.
* **Slash commands** - `/suggestion accept`, `/suggestion deny`, `/suggestion duplicate`, or `/suggestion review`, each taking the suggestion's message link or ID and an optional reason. These support all four outcomes (including Duplicate and Under Review, which have no button equivalent) and let you explain the decision.

Whichever path is used, the suggestion's embed color updates to match the outcome:

| Status | Color |
| :--- | :--- |
| Accepted | Green |
| Denied | Red |
| Duplicate | Blue |
| Under Review | Yellow |

If a reason was given, it's added to the embed as a **Reason** field. Deciding on a suggestion again (with either method) replaces its previous decision.

> The suggestion's message ID doubles as autocomplete for the slash commands - typing part of a suggestion's title will suggest matching recent suggestions.
{.is-info}

# Dashboard Decision History

The dashboard's **Suggestions** page lists every decision made for your server - status, moderator, reason, and when it was decided - and lets you edit a decision after the fact. Editing from the dashboard saves the change and updates the live embed in Discord to match.

# Limitations/Restrictions

* Decisions are keyed to the suggestion's Discord message - if a suggestion's message is manually deleted in Discord, its vote and decision records are automatically cleaned up and it disappears from the dashboard history.
* The Suggestion Channel setting itself can still be cleared after suggestions already exist. If that happens, the bot loses track of which channel those older suggestions live in - this limits autocomplete, requires a full message link (not a bare ID) for the slash commands, and prevents the dashboard from syncing edits back to Discord, for suggestions created while a different (or no) channel was configured.
* Only the most recent decision for a suggestion is kept - deciding again overwrites the previous outcome rather than keeping a history of every change.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :---------- | :------------------------------------------------------------------------ | :---: | :--------: |
| /suggestion create | Posts a suggestion for members to vote on. | N/A | None |
| /suggestion accept | Accepts a suggestion, updates its embed, and records the decision. | `<suggestion> [reason]` | ManageServer or Administrator |
| /suggestion deny | Denies a suggestion, updates its embed, and records the decision. | `<suggestion> [reason]` | ManageServer or Administrator |
| /suggestion duplicate | Marks a suggestion as a duplicate, updates its embed, and records the decision. | `<suggestion> [reason]` | ManageServer or Administrator |
| /suggestion review | Marks a suggestion as under review, updates its embed, and records the decision. | `<suggestion> [reason]` | ManageServer or Administrator |
