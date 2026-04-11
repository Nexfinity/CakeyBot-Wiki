---
title: Setup Custom Bot
description: Create custom Discord bot with Cakey Bot - White-label, custom branding, private bot hosting. Premium customization setup guide.
published: 1
date: 2026-04-11T13:24:41.050Z
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
1. Navigate to our [premium website page](https://cakey.bot/premium)
2. If you haven't done so already, you will need to login to Discord using any of the "Login to Purchase" buttons on the page.
3. Go to the "Custom Bot" section and choose either Monthly or Yearly.
4. Once you have done so, you can then click "Subscribe" and follow the on-screen instructions.

# Setting Up Your Custom Bot
Once you have purchased the custom bot, you can follow these instructions:
1) Navigate to the [custom bot](https://cakey.bot/dashboard/CustomBot) page of the web dashboard.
2) You should be prompted via modal popup to start the setup process using our step-by-step setup wizard. 
* If you get the wizard, follow the on screen instructions to complete the setup process.
* If you do NOT see the wizard, simply click the "Set Up New Bot" button to force open the setup wizard modal. (You can also optionally select the new bot in the dropdown menu and it'll prompt you for setup as well)
3) Once you have everything setup, you can move on the inviting your custom bot with the instructions below.
> **Note:** Do not skip any of the steps/instructions in the wizard. Failure to follow the steps may result in the bot not being setup/started correctly. If you have questions or issues join our [support server](https://cakey.bot/discord).
{.is-danger}

# Inviting Your Custom Bot
1. Navigate to the [premium page](https://cakey.bot/dashboard/premium) on the web dashboard.
2. There should be a "Invite" button next to your custom bot subscription in the "Premium Subscriptions" list.

> Custom Bots are currently able to be invited to an unlimited number of servers. This may change in the future if users abuse the capability.
{.is-info}
  
> **Note:** While you can keep the main Cakey Bot & your Custom Bot in the same server. It is advised to kick the main Cakey Bot to prevent duplicate data (such as double audit logs, or users gaining extra leveling xp from both bots.)
{.is-warning}
  
# Enabling 2FA For Moderation
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
**Q:** Do I need to keep the main Cakey Bot?
  **A:** No, you should kick the main bot once the custom one is added. However, you can use the premium music bots next to your custom bot, although they will not receive custom branding.
  
**Q:** My bot appears to be offline.
 **A:** Please verify you enabled the correct intents when creating the bot on Discord's developer dashboard.
  
**Q:** How many servers can I invite the custom bot to?
 **A:** Currently, unlimited. This may change in the future if users abuse the capability however.
  
**Q:** Will my settings persist from the main Cakey Bot or will I need to set them up again?
 **A:** Yes, The main bot and custom bot will share the same settings for a given server. No additional setup or copying is required.

**Q:** How do I change the profile picture, username or bio/about me? 
 **A:** You can adjust these on the Discord Developer Dashboard where you created the custom bot originally.
  
**Q:** How do I setup custom status, emotes and other advanced customization for the custom bot? 
 **A:** Check out the "Additional Customization" & "Custom Emote Replacement" sections above this FAQ for more information.
  
**Q:** I'm getting the "Private application cannot have a default authorization link" error.
 **A:** Go to the "Installation" section on the Discord developer dashboard and set your "Install Link" to "None". You can also optionally just make the bot public, however, making the bot public is not reccomended as anyone can invite the custom bot to their server and potentially abuse it.