---
title: Daily Content
description: Daily automated Discord content with Cakey Bot - Facts, jokes, quotes, custom posts. Engagement automation setup guide.
published: 1
date: 2025-11-01T06:20:03.045Z
tags: 
editor: markdown
dateCreated: 2024-12-18T02:24:11.247Z
---

# Overview
Cakey Bot's Daily Content feature allows servers to automatically receive fun and engaging daily updates at noon in their server. With a variety of images and facts to choose from, this feature adds a touch of entertainment and curiosity to your server. Whether it’s adorable animal pictures or fascinating facts, you can customize the type of content delivered to suit your community’s interests.

> **Fun Fact:** You can change Cakey Bot's timezone on the dashboard so the content always announces at noon in your timezone!
{.is-success}

# Setup
1. Login into the [web dashboard](https://cakey.bot/dashboard).
2. Select the server you want to configure.
3. From the left menu, select the "Daily Content" page.
4. Enable the daily content you want to see and select an output channel.

> Note: You MUST also select a channel, if you do not, then no daily content will be sent.
{.is-warning}

Each content category has its own individual output channel and optional role-ping setting, so you can send different categories to different channels and ping a different role for each one.

> The number of categories you can have enabled at once is tiered: **1** enabled category for non-premium servers, **3** for premium servers, and unlimited for whitelabel servers.
{.is-info}

# Daily Image Types
* Random Image
  * Will select a random image from any of the categories below. This is its own separately configurable category with its own output channel and role-ping setting, not just an aggregation of the categories below it.
* Cat
* Dog
* Fox
* Bird
* Panda
* Pikachu
* Red Panda
* Capybara
* Duck
* Alpaca
* Fish
* Seal
* Camel
* Wolf

# Daily Fact Types
* General
  * Random general knowledge fact (not animal-specific)
* Dog
* Cat
* Panda
* Fox
* Bird
* Koala
* Capybara

# Custom Content
> You MUST have an active custom bot subscription to use this type.
{.is-warning}

This daily content type allows you to specify a custom list of text or images for the bot to send. The list is separated by semicolons (`;`) and is limited to 65,000 characters. You can also set a Custom Title, which is limited to 255 characters.