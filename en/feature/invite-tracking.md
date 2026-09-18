---
title: Invite Tracking
description: Discord invite tracking with Cakey Bot - See who invited who, invite leaderboards, fake invite detection, invite labels and scheduled reports.
published: 1
date: 2026-09-18T12:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-09-18T12:00:00.000Z
---

# Overview
Invite tracking records which invite every new member arrived through and credits the member who created it. It powers an invite leaderboard, join and leave statistics, per code labels that can hand out a role, and scheduled reports, and it tells announcements who invited a new member.

> Cakey Bot needs the **`Manage Server`** permission to read the server's invites. Without it, joins cannot be attributed to anybody.
{.is-warning}

# Setup
1. Head over to [Cakey Bot's Dashboard](https://cakey.bot/dashboard) and select your server.
2. From the left sidebar, pick "Invite Tracking".
3. Open the "Invite settings" tab and enable the feature. The bot fetches the server's current invites straight away.

Members who were already in the server when tracking was enabled have no recorded inviter; only joins from then on are attributed.

# How Invites Are Counted
Every member has four counters, and their total is worked out as **Regular - Left - Fake + Bonus**.

* **Regular** ~ Every join credited to the member.
* **Left** ~ Invited members who have since left the server. Whether these are subtracted is a setting.
* **Fake** ~ Joins that do not count, see below.
* **Bonus** ~ Invites granted by hand from the dashboard.

A join is fake when any of these apply:
* The account is younger than the **fake delay** (in days). Set it to 0 to accept every account.
* The member has been in the server before and **rejoins count as fake** is on.
* The member joined through their own invite.
* The inviter is on the invite blacklist. The join is recorded, but nobody is credited.

When an invite is used up on its last use, Discord deletes it before the bot can read the count. The bot still attributes the join when it is the only invite that disappeared at that moment.

# Dashboard Tabs
* **Invite leaderboard** ~ Every inviter with their totals, over all time or the last day, week or month. Members can be hidden from the ranking with the eye button, and the ranking can be downloaded as CSV.
* **Invite analytics** ~ Joins against leaves over time and how members arrived (invite, vanity URL, bot or unknown).
* **Invite labels** ~ Give an invite code a name so joins through it read as a campaign, and optionally hand a role to everyone who arrives through it.
* **Invite blacklist** ~ Members and roles whose invites are never counted.
* **Invite adjustments** ~ Change a member's regular, bonus or fake counts by hand, forgive lost invites for everyone after a mass leave, or reset a single member or the whole server.
* **Invite reports** ~ Post a weekly or monthly summary of the server's joins and leaves to a channel.
* **Invite settings** ~ Enable the feature, the fake delay, rejoins counting as fake, whether leaves are subtracted, and a public leaderboard page at `/leaderboard/your-address`.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /invites view | A member's totals. | [user] | None |
| /invites inviter | Who invited a member, and through which code. | \<user> | None |
| /invites list | Everyone a member has invited. | [user] | None |
| /invites codes | The invite codes a member owns, with their uses and labels. | [user] | None |
| /invites leaderboard | The invite leaderboard. | [range] | None |
| /invites stats | Join and leave statistics for the server. | [range] | None |
| /invites sync | Refreshes the cached invite list. | N/A | ManageServer |