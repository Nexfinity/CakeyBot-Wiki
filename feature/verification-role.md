---
title: Verification Role
description: 
published: 1
date: 2024-10-09T23:14:14.381Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:21:54.369Z
---

# Overview

> Make sure that Cakey Bot has **`Manage Roles`** permission.
> 
> Also, ensure that Cakey Bot's role is _above_ the verification role you want Cakey bot to give users.
{.is-warning}

# Tutorial Video
<div style="left: 0; width: 100%; height: 0; max-width: 560px; max-height: 315px; position: relative; padding-bottom: 315px;"><iframe src="https://www.youtube.com/embed/y_DgmqeXQnY?rel=0" style="top: 0; left: 0; width: 100%; height: 100%; max-width: 560px; max-height: 315px; position: absolute; border: 0;" allowfullscreen scrolling="no" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture;"></iframe></div>

# Verification Command

You can force users to run the `/verify` command in order to be granted a role that you have selected. This is a great way to make sure users read any rules or important info you have before they are able to chat in your server. Users will only need to type the`/verify` command in order to get the role.&#x20;

# Configuring Verification

In order to set the role that you want users to get, you will need to type `/setup verifyrole <role>`. You can also disable or remove the role by typing `/setup verifyrole 0`. If you want to change the role later, you can just run the initial setup command and type the new role and it will update the currently saved role.

> **Helpful Tip:** You can also set the verification role in the [web dashboard](https://cakey.bot/dashboard/public)!
{.is-success}