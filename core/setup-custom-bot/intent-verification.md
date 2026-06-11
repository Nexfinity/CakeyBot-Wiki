---
title: Custom Bot Intent Verification
description: A short guide to help you answer the privileged intent verification application for custom bots.
published: 1
date: 2026-06-11T22:19:59.936Z
tags: 
editor: markdown
dateCreated: 2026-06-11T22:04:47.406Z
---

> **Note:** This only affects custom bots that have more than 10,000 unique users across all servers it is in combined. If your bot does not have this many users then you can disreagrd this page.
{.is-warning}

# Overview
> **Note:** Unless Discord changes it at a later date, you will have to keep re-verifying your bot once a year, so please keep a link to this guide for future applications. If you forget the link, you can always reach out to our [support team](https://cakey.bot/support).
{.is-warning}

TBD

# Form Fill-Out Guide
> **Note:** This guide does NOT guarentee your application will be accepted. This guide should be sufficient for Discord to approve it, however, at the end of the day the application is decided on by Discord. If you run into complications or followup questions from Discord, please reach out to our [support team](https://cakey.bot/support).
{.is-danger}

Discord has a fairly straight forward application form which will ask various questions. For select menus, select the option suggested by this guide and for any text input sections you can copy/opaste the text directly from the code-blocks provided in this guide. This guide should be laid out in the same order as Discord's application form.

## Application Details
```
TBD
```

## Do you have a public Privacy Policy telling your users about their data usage?
Select **Yes**

### Where is your Privacy Policy available?
```
In the bot's bio.
```
> **Note:** The privacy policy is required to be listed somewhere publicly, this is a Discord limitation and not something we can get around. Discord typically requires it to be in the bot's bio. If you do not want to link to Cakey's website directly, you could copy/paste our entire privacy policy onto your own website, github gist, or similar text format that Discord accepts and use that instead. Note that using other listings for it may affect verification approval or require changes asked by Discord's support team.
{.is-info}

### Please share a link to your Privacy Policy.
```
https://cakey.bot/privacy
```

## Privileged Gateway Intents
Select/check both of these intents:
* Server Members Intent
* Message Content Intent
> Do **NOT** select the presence intent. Cakey Bot does not require it and it will increase the chance of the application getting denied if you have this selected.
{.is-danger}

## Server Members Intent
### Why do you need the Guild Members intent?
```
TBD
```
### Please provide links to screenshots and/or videos that demonstrate your use case
```
TBD
```
### Are you storing any API Data off-platform (outside of Discord)?
Select **??**

## Message Content Intent
### Can users opt-out of having their message content data tracked?
Select **No**
## Are you storing message content data off-platform (outside of Discord)?
Select **No**
## Will the message content data be used to train machine learning or AI Models?
Select **No**
## Why do you need the Message Content intent?
```
TBD
```
## Please provide links to screenshots and/or videos that demonstrate your use case
```
TBD
```
## Acknowledgement
Select/checkbox this.

> **Note:** While this should be sufficient for most/all applications/bots, Discord support staff may ask additional or followup questions or request certian changes. If they do, pelase reach out to our support team for assistance.
{.is-info}