---
title: Verification Role
description: 
published: 1
date: 2025-03-26T08:30:23.251Z
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

# Overview
Cakey Bot offers a versatile user verification system that allows server administrators to select from four different verification methods. These options provide flexibility based on the server's needs and ensure that new members are properly verified before gaining access to the server's full features. This is a great way to make sure users read any rules or important info you have before they are able to chat in your server. Once a user successfully completes the verification process, they are automatically assigned the pre-selected verify role. Below is an overview of the available verification methods:

> Note: ALL of the methods below (except Slash Command) REQUIRE the verification embed. (See setup section below)
{.is-warning}

## Slash Command
1) The user simply types the `/verify` command and they receive the role.

## Button Click
1) The user simply presses the "Verify" button at the bottom of the verification embed and they receive the role.

## Captcha
1) The user presses the "Verify" button at the bottom of the verification embed. 
2) Once they do, they will receive a captcha image along with a new "Verify" button. 
3) The user then clicks this button and enters the captcha letters into the popup. 
4) If they type the correct letters, they receive the role.

## Custom Password
1) The user presses the "Verify" button at the bottom of the verification embed. 
2) Once they do, they will receive a popup asking for the server's custom password.
3) If they type the correct password, they receive the role.

> Note: You will have to set the password on the web dashboard. If no password is set, ALL attempts will fail.
{.is-warning}

# Setting Up Verification

## Set the Verification Role ~(Required~ ~for~ ~ALL~ ~methods)~
In order to set the role that you want users to get, you will need to type `/setup verifyrole <role>`. You can also disable or remove the role by typing `/setup verifyrole 0`. If you want to change the role later, you can just run the initial setup command and type the new role and it will update the currently saved role.

> **Helpful Tip:** You can also set the verification role in the [web dashboard](https://cakey.bot/dashboard/public)!
{.is-success}

> Note: In order to prevent abuse, Cakey Bot will prevent selecting roles that contain `Administrator`, `Manage Server` or `Manage Roles` permissions. In addition, if these roles gain this permission after being set, the bot will no longer assign them.
{.is-danger}

## Create the Verification Embed ~(Required~ ~for~ ~some~ ~methods)~
Most of the verification methods require the verification embed in order to function. The only method that does NOT require the embed is the Slash Command method. However, the verification method does support slash command verification.

In order to create the verification embed, simply run the `/setup createverifyembed <channel>`. The command will ask what channel you want the embed to be sent to.

> Note: You will need to set the desired verification type BEFORE you create the embed. If you change the verification type later, you will need to delete the embed and generate a new one.
{.is-info}

## Set a Custom Embed Message
In order to set a custom embed message, simply login to the [web dashboard](https://cakey.bot/dashboard/public) and navigate to the "Verification Role" page. Once there, you should see a text box labeled "Verification Message". You can set any message you want up to 2k characters.

> Note: Setting a custom embed message is NOT requied. If no message is set, Cakey bot will generate a default message.
{.is-info}

> **Helpful Tip:** You can also use _some_ [basic placeholders](/placeholders) in the custom message!
{.is-success}

## Set a Custom Password
In order to set a custom password, simply login to the [web dashboard](https://cakey.bot/dashboard/public) and navigate to the "Verification Role" page. Once there, you should see a text box labeled "Custom Password". You can set any password you want up to 255 characters. Passwords are not currently case sensitive.

> Note: A custom password will only be required with the "Custom Password" method. Also, if no password is set, ALL attempts will fail.
{.is-info}

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command | Description | Usage | Permission |
| :--- | :--- | :---: | :---: |
| /verify | The command that users run to verify themselves. | N/A | None | 
| /setup verifyrole | Set a role that users can assign to themselves when typing the command. | \<role> | ManageServer or Administrator | 
| /setup createverifyembed | Generate an embed with verification instructions. | N/A | None | 