---
title: Staff Notes
description: Discord staff notes system with Cakey Bot - Personal notes, public bulletins, staff-only notes. Note-taking setup guide.
published: 1
date: 2026-07-09T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2025-02-20T22:00:42.440Z
---

# Overview

> Make sure that Cakey Bot has the **`View Channel`**, **`Send Messages`**, and **`Embed Links`** permissions in the channel you run `/notes list` from.
{.is-warning}

Staff Notes gives your server a lightweight, in-Discord note board. Members can jot down notes for themselves, post notes that are visible to everyone, or (if they're staff) post notes that only your staff team can see. All notes are managed entirely through buttons and modals without leaving Discord.

Some examples of how servers use Staff Notes:
- **Personal** notes for reminders, to-do items, or anything you want to keep track of for yourself
- **Public** notes for announcements, pinned information, or community bulletins visible to all members
- **Server** (staff-only) notes for tracking moderation context, member warnings, internal staff reminders, or anything your team needs to keep private from regular members

# Configure Staff Notes

1. Login to our [web dashboard](https://cakey.bot/dashboard).
2. Go to "Bot Settings".
3. Under **Notes Staff Role**, select the role that should be treated as staff for the Staff Notes feature.

> If you don't set a Notes Staff Role, only members with the **Administrator** or **Manage Server** permission will be treated as staff. Staff status controls who can view/create **Server** category notes and who can edit or delete other members' **Public** notes.
{.is-info}

# Note Categories

Every note belongs to one of three categories:

* 👤 **Personal** — Only visible to the member who created it. Not even staff can see another member's Personal notes.
* 🌍 **Public** — Visible to every member who runs `/notes list`. Any member can create a Public note, but only the note's creator or a staff member can edit/delete it.
* 🛠️ **Server** — Only visible to staff (members with the configured Notes Staff Role, or the Administrator/Manage Server permission). Only staff can create, view, edit, or delete Server notes.

> The category tab for **Server** notes is disabled for non-staff members, since they don't have any notes to view in that category.
{.is-info}

# How to Use

Running `/notes list` opens a paginated menu that is only visible to you (ephemeral), showing 5 notes per page. From here you can create, view, edit, and delete notes without needing any additional commands.

## Viewing Notes

At the top of the menu are three category buttons (Personal / Public / Server), each showing how many notes exist in that category. Click a category to switch to it. Notes are listed with the timestamp they were created and their content.

## Creating a Note

While viewing a category, click the **Create a new note** 📝 button. This opens a text box where you can type your note (up to 300 characters). Submitting it adds the note to whichever category tab you had open.

## Editing/Deleting a Note

Click the ✏️ button next to a note to open its management view. From here you can:

* **Edit content** 📝 — Opens a text box pre-filled with the note's current content so you can update it.
* **Delete note** 🗑️ — Permanently deletes the note. There is no confirmation prompt.
* **Change category** — Use the dropdown menu to move the note into a different category. The Server option only appears if you're staff, and the Personal option only appears if the note belongs to you.
* **Go back** 🚪 — Returns to the notes list.

> You can only edit/delete a note if you created it, or if it's a Public or Server note and you're staff. This means non-staff members can never modify a Public note that someone else made, and can't touch Server notes at all.
{.is-info}

The notes menu stays active for 30 minutes of inactivity, after which its buttons will be disabled.

# Permissions

Any member can run `/notes list` and create Personal or Public notes. No special Discord permission is required to use the command itself. Staff-only actions (viewing/creating Server notes, and editing/deleting other members' Public notes) require the configured Notes Staff Role, or the Administrator/Manage Server permission — see [Configure Staff Notes](#configure-staff-notes) above.

# Limitations/Restrictions

* Note content is limited to 300 characters.
* There is no way to see who created a note or when it was last modified from the notes menu itself.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command     | Description                                                              | Usage | Permission |
| :---------- | :------------------------------------------------------------------------ | :---: | :--------: |
| /notes list | Opens the notes menu to view, create, edit, and delete notes. | N/A   | None       |
