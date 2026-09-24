---
title: Self Roles
description: Discord self-assignable roles with Cakey Bot - Reaction roles, role menus, color selection. Member customization guide.
published: 1
date: 2025-11-01T06:20:08.470Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:20:14.430Z
---

# Overview

> Make sure that Cakey Bot has the **`Manage Roles`** permission and that the Cakey Bot's role is _above_ the roles it is trying to assign.
{.is-warning}

Self Roles allows users to add/remove roles to/from themselves from a list of roles that have been created/set by the server admins.

> Note: In order to prevent abuse, Cakey Bot will prevent selecting roles that contain `Administrator`, `Manage Server` or `Manage Roles` permissions. In addition, if these roles gain this permission after being set, the bot will no longer assign them.
{.is-danger}

> A server can have a maximum of **250** self roles.
{.is-warning}

# Managing Self Roles (Dashboard)

Self roles are created, edited, and deleted entirely from the [dashboard](https://cakey.bot/dashboard)'s Self Roles page. Click **Add Self Role** to create one, choosing:

* The role to make self-assignable.
* An optional description shown to users.
* Optional [role requirements](#role-requirements) (Required Level, Required Streak, Required Role).
* An optional [role group](#role-groups) to make the role mutually exclusive with other roles in the same group.

Each self role can also be edited or deleted from the same page.

Once you've added some roles to the self role list, you (and your users) can add/remove them from yourselves using the `/selfrole use <role>` and `/selfrole unuse <role>` commands.

> If you want to use our advanced self-assign method (selection dropdowns) you will need to create a self-role embed using the `/selfrole embed` command. This will generate an embed where users can assign themselves roles using select-menu dropdowns. For a panel you can design and edit from the dashboard, see [Role Panels](#role-panels).
{.is-info}

# Role Panels

A role panel is a message Cakey Bot posts in a channel where members pick roles with a click, no commands needed. Panels are managed under **Role Panels** on the Self Roles dashboard page.

Each panel has:

* A **name**, only shown on the dashboard.
* A **picker style**: a **select menu** (one dropdown; what a member has selected is what they hold) or **buttons** (one per role; pressing it adds or removes that role).
* An **embed title and text** shown above the picker. With Premium, a saved embed from the Embed Builder can take their place, with the text field then posted as the message above it.
* **Roles**: up to 25 roles. Each can have its own label and emoji (a unicode emoji, or a custom emote as `<:name:id>`), and with buttons, a button colour. A role that is not a self role yet is added to your self role list when the panel is saved, so its requirements and group can be set there afterwards.

The dashboard shows a live preview of the panel while you edit it. Click the paper plane on a panel to post it into a channel. Editing a posted panel updates the message in Discord on its own; deleting a panel removes the message too.

Panels respect every self role rule: role requirements, group limits and prerequisites, and the Administrator / Manage Server / Manage Roles restriction.

> Free servers can keep **1** panel, Premium servers **3**, and Custom Bots **10**. One panel is enough for most servers, since it offers up to 25 roles.
{.is-info}

> With Premium, a panel can use a saved embed from the Embed Builder instead of the plain title and text, for full control over the look.
{.is-success}

# Role Requirements
You can also set optional role requirements. This means users will need to meet or exceed these requirements in order to assign the role to themselves. The currently supported requirements are:
* Required Level
* Required Streak
* Required Role

# Role Groups

Role Groups let you make a set of self roles mutually exclusive, so users can only hold a limited number of roles from that group at once. Groups are managed from the same dashboard page as self roles, under **Role Groups**.

There are two group types:

* **Unique** - a user can only hold **one** role from the group at a time. Claiming a different role in the group automatically removes whichever role from that group they held before.
* **Multi-select** - a user can hold up to a configurable maximum (2-25) roles from the group. Claiming one more role than the limit allows automatically removes the user's **oldest-claimed** role in that group first, then grants the new one.

Both the `/selfrole use`/`/selfrole unuse` commands and the self-role embed's selection dropdowns respect group limits. `/selfrole list` shows each role's group name and type (and, for Multi-select groups, the max role count) so users know the constraints before picking.

> Deleting a role group does **not** delete the roles that belonged to it. They simply become ungrouped and stop being mutually exclusive - nothing is removed from users who already hold them.
{.is-info}

## Group Prerequisites

Independently of a group's type (Unique or Multi-select), you can set a **Prerequisite** that a member must satisfy before claiming *any* role from that group. This is optional and configured per-group on the dashboard, alongside the group's type.

Currently supported prerequisite types:
* **Must have a role** - the member must already hold a specific role.
* **Minimum level** - the member must be at least a given [leveling](/en/feature/leveling) level (based on the same XP/level data used everywhere else in Cakey Bot).

More prerequisite types (e.g. account age, server boost status) may be added in the future.

If a member doesn't meet a group's prerequisite, claiming a role from that group (via `/selfrole use` or the self-role embed) is rejected with a message explaining what's missing (e.g. "Requires Level 10+" or naming the required role). `/selfrole list` also shows each group's prerequisite (if any) so members know what's needed before trying.

> A prerequisite only gates claiming *new* roles from the group - it doesn't retroactively remove roles from members who already hold them if a prerequisite is added or changed later.
{.is-info}

> If a **Must have a role** prerequisite's configured role is later deleted from the server, the group fails closed: claiming *any* role from that group is blocked for everyone, with a message telling members the group is misconfigured and needs an admin to fix it. This stays in effect until an admin sets a new required role or removes the prerequisite entirely - it will not silently start letting claims through again on its own.
{.is-warning}

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /selfrole embed | This command creates a self-role embed message. | N/A | ManageRoles | 
| /selfrole list | This command lists self roles users can assign to themselves, including each role's group. | N/A | None | 
| /selfrole unuse | This command allows users to unassign themselves roles. | \<role> | None | 
| /selfrole use | This command allows users to assign themselves roles. | \<role> | None | 
