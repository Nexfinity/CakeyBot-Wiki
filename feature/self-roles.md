---
title: Self Roles
description: 
published: 1
date: 2024-09-12T11:08:37.674Z
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