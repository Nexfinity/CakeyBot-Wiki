---
title: Self Roles
description: 
published: 1
date: 2025-02-23T21:50:16.750Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:20:14.430Z
---

# Overview

> Make sure that Cakey Bot has the **`Manage Roles`** permission and that the Cakey Bot's role is _above_ the roles it is trying to assign.
{.is-warning}

# Self Role Command

Self Roles allows users to add/remove roles to/from themselves from a list of roles that have been created/set by the server admins.

To add/remove a role from this list you can use the `/selfrole addrole <role>` and `/selfrole removerole <role>` commands.

To list all roles that can be self-assigned you can use the `/selfrole list` command.

After you have added some roles to the self role list you (and your users) can add/remove the roles from yourself using the `/selfrole use <role>` and `/selfrole unuse <role>` commands.

> If you want to use any of our advanced self-assign methods (like buttons or selection dropdowns) you will need to create a self-role embed using the `/selfrole embed` command. This will generate an embed using the assignment method you set on our web dashboard.
{.is-info}

# Role Requirements
You can also set optional role requirements. This means users will need to meet or exceed these requirements in order to assign the role to themselves. The currently supported requirements are:
* Required Level
* Required Streak
* Required Role

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /selfrole addrole | This command allows admins to add self roles for users to assign themselves roles. | \<role> [description] [requiredLevel] [requiredStreak] [requiredRole] | ManageRoles | 
| /selfrole embed | This command creates a self-role embed message. | N/A | ManageRoles | 
| /selfrole list | This command allows admins to list self roles users can assign to themselves. | N/A | None | 
| /selfrole removerole | This command allows admins to remove self roles for users to assign themselves roles. | \<role> | ManageRoles | 
| /selfrole unuse | This command allows users to unassign themselves roles. | \<role> | None | 
| /selfrole use | This command allows users to assign themselves roles. | \<role> | None | 