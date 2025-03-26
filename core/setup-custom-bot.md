---
title: Setup Custom Bot
description: 
published: 1
date: 2025-03-26T09:27:56.807Z
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

> Note: It is important that you follow every step in this guide. If you skip or ignore steps or sections the bot will not work as expected or you may not be able to configure it on the web dashboard. Also please read the FAQ at the bottom of the page. It answers many common issues/questions. If you run into issues, please open a ticket on our [support Discord](https://cakey.bot/discord).
{.is-danger}

# Purchasing Custom Bot
To purchase a Custom Bot simply follow these instructions:
1. Navigate to our [premium website page](https://cakey.bot/premium.php)
2. If you haven't done so already, you will need to login to Discord using any of the "Login to Purchase" buttons on the page.
3. Go to the "Custom Bot" section and choose either Monthly or Yearly.
4. Once you have done so, you can then click "Subscribe" and follow the on-screen instructions.

# Setting Up Custom Bot
> Note: All of the steps below assume that you have already purchased a Custom Bot subscription and are currently trying to configure it and set it up.
{.is-info}

> Note: For the easiest setup possible you should try to follow this guide step-by-step in order.
{.is-info}

## Creating a Custom Bot Token
1. Go to https://discord.com/developers/applications, login with your Discord account and press the "New Application" button.
<image src="/newapp.png" width="800px" alt="New application popup">

2. Give a name to your application and press "Create". Don't worry about it too much right now, you can always change the name of your bot at any time!
<image src="/image_(1).png" width="800px" alt="Create application popup">

3. Select the "Bot" page from the left side navigation.
  
4. Scroll down to the Privileged Gateway Intents section and enable the "Server Members Intent" and "Message Content Intent".
  
> Note: "Presence Intent" is not currently used and does NOT have to be enabled. 
{.is-info}
  
<image src="/intents.png" width="800px" alt="Privileged intents">
  
> Notice: It is important that you enable these intents. If you do not, the bot will NOT start.
{.is-danger}

5. Press the "Reset Token" button to reset your token
<image src="/image_(5).png" width="800px" alt="Token reset">
  
6. Press "Yes, do it!" on the modal
<image src="/image_(2).png" width="800px" alt="Confirmation popup">
  
7. Enter 2FA code if necessary
<image src="/image_(3).png" width="800px" alt="2FA popup">

8. Now you should see your token, just like in the screenshot below: 
![token2.png](/token2.png)
  
9. Press the "Copy" button and keep a hold of your token for later use

> This token is super secret and you should never give it to anyone else without knowing why or you risk someone else taking over your bot. If you think your token might have leaked, please press the regenerate button or delete your application.
{.is-warning}
  
> Keep this Discord Developer dashboard open for now. We'll return to invite the bot later.
{.is-info}

Now, you can go back to Cakey Bot's [web dashboard](https://cakey.bot/dashboard/public) to set up your Custom Bot with this token. To set up the Custom Bot on Cakey Bot's dashboard just follow these steps:

1. Login to the web dashboard

2. Navigate to the "Premium" page

3. Click the "Set Custom Bot Token" under the "Premium Subscriptions" section
![settoken2.png](/settoken2.png)

4. Select the Custom Bot plan you want to set the token on and paste your token
![settoken.png](/settoken.png)

5. Click "Set Token".

> Note: Once you set the token, you will see a blue "Invite" button appear on the table. Do NOT click this yet, you will need to follow additional steps in the "Inviting Your Custom Bot" section below before the invite URL will work properly.
{.is-warning}
  
> Note: The new bot replaces Cakey Bot. You can keep the default Cakey Bot in your server if you wish, however we recommend kicking the default bot to prevent spam/duplicate entries for stuff like Audit Logs and Custom Commands/Auto Responders.
{.is-info}

If you have any issues with this, do not hesitate to join our [support server](https://cakey.bot/discord)!
  
## Assign Servers
>  Custom Bots will work/function in any number of servers you invite the bot to, even if it is not assigned to the server in the web dashboard. Assigning a server is only required if you wish to change settings for the bot on a specific server in the web dashboard.
{.is-info}

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
<image src="/redirects.png" width="800px" alt="Redirect configuration">
> **Note:** If you've used this bot before, it's possible other URLs may already exist. If so, simply replace an existing one with Cakey Bot's website URL or add it as a new one with the "Add Another" button.
{.is-warning}
4. In the text field enter `https://cakey.bot/success_invite.html` and hit the "Save" button (**Note:** This link does not match the one in the screenshot.)
5. You may return to the web dashbord and on the "Premium" page there should be a "Invite" button next to your custom bot subscription in the "Premium Subscriptions" list.

> Custom Bots are currently able to be invited to an unlimited number of servers. This may change in the future if users abuse the capability.
{.is-info}
  
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

In order to fix this issue, you will need to enable 2FA on the Discord account that created the custom bot. ([see this tutorial](https://support.discord.com/hc/en-us/articles/219576828-Setting-up-Two-Factor-Authentication))

If this isn't an option, you can also disable the 2FA requirement on the server, however, **we do NOT recommend doing that**.

If you have any issues in getting this sorted, do not hesitate to join our [support server](https://cakey.bot/discord)!

# Additional Customization
Once you have setup and configured your bot you can setup additional customizations like custom API keys, custom embed colors and more. Simply login to the web dashboard and navigate to the "Custom Bot" page.
  
# Custom Emote Replacement
Cakey Bot even allows you to customize and swap out every custom emote we use in the bot. In order to do this simply follow the steps listed below:
1. Naivate to the [Discord dev portal](https://discord.dev) website where you first created your bot.
2. Open/select your custom bot/application from the dashboard
3. Click the "Emote" tab on the left sidebar
4. Find the emote that you want to replace with your own. (Write down or take note of the EXACT name of this emote)
5. Delete the emote
6. Upload your new custom emote image (Use the EXACT name of the one you deleted previously)
7. Restart your custom bot via Cakey Bot's custom bot dashboard
  
<image src="/custom-emotes.png" width="800px" alt="Custom emote management">
  
> Note: Custom bots will syncronize their emotes on every startup. This means any random extra/invalid emotes will be deleted and any missing emotes will be replaced by the default. Be sure you use the EXACT name of the emotes when swapping them out.
{.is-warning}
  
# Frequently Asked Questions
**Q**: Do I need to keep the main Cakey Bot?
   **A**. No, you should kick the main bot once the custom one is added. However, you can use the premium music bots next to your custom bot, although they will not receive custom branding.
  
**Q**: My bot appears to be offline.
   **A**. Please verify you enabled the correct intents when creating the bot on Discord's developer dashboard.
  
**Q**: How many servers can I invite the custom bot to?
   **A**. Currently, unlimited. This may change in the future if users abuse the capability however.
  
**Q**: Will my settings persist from the main Cakey Bot or will I need to set them up again?
   **A**. Yes, The main bot and custom bot will share the same settings for a given server. No additional setup or copying is required.
  
**Q**: Do I need to assign every server in the dashboard that I invite the custom bot to?
   **A**: No, only for servers that you wish the change the web dashboard settings on. the custom bot will function at a basic level in all servers it's invited to.
  
**Q**: How do I change the profile picture, username or bio/about me? 
   **A**: You can adjust these on the Discord Developer Dashboard where you created the custom bot originally.
  
**Q**: How do I setup custom status, emotes and other advanced customization for the custom bot? 
   **A**: Check out the "Additional Customization" & "Custom Emote Replacement" sections above this FAQ for more information.