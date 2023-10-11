---
title: Setup Custom Bot
description: 
published: 1
date: 2023-10-11T17:22:49.847Z
tags: 
editor: markdown
dateCreated: 2023-05-17T18:39:13.501Z
---

# Overview
Custom Bot is an advanced version of Premium that allows you to completely rebrand Cakey Bot with your own Logos and Username! Custom Bot allows you to have:
* Custom Chat Bot AI API Key
* Custom Bot Profile Picture
* Custom Bot Username
* Custom Bot Bio
* Better Performance

# Purchasing Custom Bot
To purchase a Custom Bot simply follow these instructions:
1. Navigate to our [premium website page](https://cakeybot.app/premium.php)
2. If you haven't done so already, you will need to login to Discord using any of the "Login to Purchase" buttons on the page.
3. Go to the "Custom Bot" section and choose either Monthly or Yearly.
4. Once you have done so, you can then click "Subscribe" and follow the on-screen instructions.

# Setting Up Custom Bot
> Note: All of the steps below assume that you have already purchased a Custom Bot subscription and are currently trying to configure it and set it up.
{.is-info}

## Creating a Custom Bot Token
1. Go to https://discord.com/developers/applications, login with your Discord account and press the "New Application" button.
<image src="https://wiki.cakeybot.app/newapp.png" width="800px">

2. Give a name to your application and press "Create". Don't worry about it too much right now, you can always change the name of your bot at any time!
<image src="https://wiki.cakeybot.app/image_(1).png" width="800px">

3. Select the "Bot" page from the left side navigation.
  
4. Scroll down to the Privileged Gateway Intents section and enable the "Server Members Intent" and "Message Content Intent".
4a. Note: "Presence Intent" is not currently used and does NOT have to be enabled.
<image src="https://wiki.cakeybot.app/intents.png" width="800px">

5. Press the "Reset Token" button to reset your token
<image src="https://wiki.cakeybot.app/image_(5).png" width="800px">
  
6. Press "Yes, do it!" on the modal
<image src="https://wiki.cakeybot.app/image_(2).png" width="800px">
  
7. Enter 2FA code if necessary
<image src="https://wiki.cakeybot.app/image_(3).png" width="800px">

8. Now you should see your token, just like in the screenshot below: 
![token2.png](/token2.png)
  
9. Press the "Copy" button and keep a hold of your token for later use

> This token is super secret and you should never give it to anyone else without knowing why or you risk someone else taking over your bot. If you think your token might have leaked, please press the regenerate button or delete your application.
{.is-warning}
  
> Keep this Discord Developer dashboard open for now. We'll return to invite the bot later.
{.is-info}

Now, you can go back to Cakey Bot's [web dashboard](https://cakeybot.app/dashboard/public/premium) to set up your Custom Bot with this token. To set up the Custom Bot on Cakey Bot's dashboard just follow these steps:

1. Login to the web dashboard

2. Navigate to the "Premium" page

3. Click the "Set Custom Bot Token" under the "Premium Subscriptions" section
![settoken2.png](/settoken2.png)

4. Select the Custom Bot plan you want to set the token on and paste your token
![settoken.png](/settoken.png)

5. Click "Set Token".

> Note: the new bot replaces Cakey Bot. You can keep the default Cakey Bot in your server if you wish, however we reccomend kicking the default bot to prevent spam/duplicate entries for stuff like Audit Logs and Custom Commands/Auto Responders.
{.is-info}

If you have any issues with this, do not hesitate to join our [support server](https://cakeybot.app/discord)!
  
## Assign Servers
Once you have created and setup the custom bot instance, you will need to assign it to the servers you plan to invite it to/configure it on. To assign the bot to a server follow these steps:
1. Navigate to the "Premium" page on the web dashboard if you are not already on the page.
2. Click the "Add Server" button under the "Applied Subscriptions" section
3. Select the custom bot plan and the server you want to assign it to.
4. Click "Add Server" button.
5. Repeat for every server you want to use the custom bot in.

## Inviting Your Custom Bot
1. On the Discord Developer dashboard select your bot application
2. Go to the "OAuth2"->"General" page from the left navigation bar
3. Click the blue "Add Redirect" button. This button may say "Add Another" if a redirect already exists, this is fine. 
<image src="https://wiki.cakeybot.app/redirects.png" width="800px">
> **Note:** If you've used this bot before, it's possible other URLs may already exist. If so, simply replace an existing one with Cakey Bot's website URL or add it as a new one with the "Add Another" button.
{.is-info}
4. In the text field enter `https://cakeybot.app` and hit the "Save" button
5. You can now invite your bot using this URL: 
`https://discord.com/oauth2/authorize?client_id=BOT_ID_HERE&permissions=8&redirect_uri=https://cakeybot.app&response_type=code&scope=bot+applications.commands+identify+guilds`
  a. Replace `BOT_ID_HERE` with your bot applications client ID. (Visibale at the top of the OAuth2 page)
  
## Enabling 2FA For Moderation
If the Custom Bot isn't moderating a server properly, the server may have the Highest security setting enabled. This means that the owner of the Custom Bot will need to have 2FA (2-Factor Authentication) enabled for their Discord account.

The following actions will all fail if that person does not have 2FA (2-Factor Authentication) enabled for their Discord account.
* kick (/kick and automated actions)
* ban (/ban, /tempban and automated actions)
* unban (/unban and automated actions)
* delete message (/purge, automod, AR/CC)
* give role (self roles, verify role, welcome role, mute)
* remove role (self roles, mute)
* channel perms overrides (muted role, support tickets, automated actions)
* webhook creation (modlog, social feeds)
* full permission option (administrator)

In order to fix this issue, you will need to enable 2FA on the Discord account that created the custom bot. ([see this discord tutorial](https://support.discord.com/hc/en-us/articles/219576828-Setting-up-Two-Factor-Authentication))

If this isn't an option, you can also disable the 2FA requirement on the server, however, **we do NOT recommend doing that.**

If you have any issues in getting this sorted, do not hesitate to join our [support server](https://cakeybot.app/discord)!

# Additional Customization
Once you have setup and configured your bot you can setup additional customizations like custom API keys, custom embed colors and more. Simply login to the web dashboard and navigate to the "Custom Bot" page.