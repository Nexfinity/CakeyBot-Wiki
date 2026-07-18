---
title: Auto Messages
description: Schedule Discord messages with Cakey Bot - Timed announcements, recurring posts, auto content. Automated messaging setup guide.
published: 1
date: 2026-07-18T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2025-01-24T04:16:57.525Z
---

# Overview
The auto message feature allows server owners to schedule recurring messages that are automatically sent to a specified channel at a designated time. Messages can be scheduled to send every day, or on a specific day of the week. These messages can be simple text or enhanced with a custom Discord embed, making them versatile for announcements, reminders, or community engagement. The feature includes options to enable or disable messages, ensuring flexibility based on the server's needs. Messages are sent reliably at the set time, helping server owners maintain consistent communication with their members.

> Message content is limited to 2,000 characters. The number of auto messages you can create is tiered: **1** for non-premium servers, **3** for premium servers, and **10** for whitelabel servers.
{.is-info}

# Setup

> You will need **`Manage Server`** or **`Administrator`** permission to manage servers and auto messages.
{.is-warning}

> You can also grant specific users or roles dashboard access without requiring Manage Server or Administrator. See [Dashboard Access](/en/core/dashboard-access) for details.
{.is-info}

1. Login to the web dashboard on the [main website here](https://cakey.bot/dashboard).
2. Click on the server you want to edit auto messages on.
3. Go to the "Auto Messages" page.
4. You can then create, delete, and edit any messages on this page.

> Auto Messages will send every day at the specified time by default, or you can configure a specific day of the week for the message to send instead. The time will be absed on the "Timezone" that you configure for your server on the "Bot Settings" page.
{.is-info}

# Custom Embeds <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>
You can include an optional embed on responses by following the steps below:

1. Follow the instructions at the top of this page to sign in to the dashboard.
2. Open the [Embed Editor](/en/feature/embed-editor) and design your embed.
3. Click **Save** (or **Save As New**) and give it a name.
4. Create an auto message like you normally would, then select your saved embed from the **Custom Embed** dropdown.

> Custom embeds will work with all **Basic Placeholders**. You can find the list of supported placeholders [here](https://wiki.cakey.bot/en/placeholders). Custom embeds will **NOT** work with the **Advanced Placeholders**.
{.is-info}
