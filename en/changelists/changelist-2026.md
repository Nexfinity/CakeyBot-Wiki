---
title: Changelist 2026
description: Cakey Bot update history - New features, bug fixes, improvements for Discord. Complete version changelog and release notes.
published: 1
date: 2026-09-23T12:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-01-13T22:54:52.663Z
---

# September 23rd - Forms Rule Sets & Placeholders
## Fixed
* Fixed denying a form submission from Discord leaving the Accept and Deny buttons on the post.
  * Denied posts are now marked the same way approved ones are, and both get a ✅ or ❌ reaction, including when decided from the dashboard.
* Fixed Markdown in form descriptions, success messages, reviewer notes and answer options showing as literal asterisks on the website.
* Fixed conditional questions sometimes showing or hiding differently in the browser than on submit.
* Fixed quoted answers (`{{Q1}}`) showing the raw placeholder until the question was answered.
* Fixed page breaks being counted as questions, and showing as empty answers in responses and CSV exports.
* Fixed My Submissions showing responses to forms without a review step as awaiting review forever.
* Fixed saving a custom bot token onto the wrong slot breaking the dashboard for every server. The save is now refused with a message pointing at the right slot.

## Changed
* Form conditions are now grouped into rule sets, each set to all or any of its conditions, instead of a flat list with a rule set number. See the [Forms wiki page](/en/feature/forms#conditional-visibility).
* A condition on a multiple choice, dropdown or checkbox question now picks its expected answer from the question's options instead of it being typed.
* Form text now supports underline, `-#` subtext and headings, matching Discord.

## Added
* Added placeholders to a form's success message and launch announcement, including `{form.name}`, `{form.link}` and `{form.expiresat}`. See the [Forms wiki page](/en/feature/forms#placeholders).
* Added an Allow Editing After Submitting setting to forms, on by default.
* Added Move to page on form questions, to move or copy a question onto another page.
* Added a Submit again link to My Submissions when a form accepts another submission.
* Added the server banner to public form pages.

# September 22nd - Achievement Fixes & User Preferences Button
## Fixed
* Fixed automatic achievements staying locked at full progress.
  * An achievement only unlocked when a counter landed exactly on its limit, so one created, edited, or recreated after you had already passed it never unlocked.
  * Every trigger now unlocks anything you have reached or passed, boost and birthday achievements included.
  * Achievements you already earned are filled in quietly the next time you are active, without announcing them again.
  * Lower tiers of a tier group you already hold are filled in as well.
* Fixed creating an achievement on the dashboard sometimes adding it two or three times.
  * The create button now waits while the save is in flight, and an identical achievement is no longer added twice.
* Fixed sending an embed to a webhook failing with "Discord rejected the embed".
  * Webhook sends now go through the same checks as channel sends, so an embed that posts to a channel posts to a webhook too.
* Fixed the send to channel list showing only None on custom bot servers.
  * Loading a dashboard page could log the custom bot out mid request, which also caused random 401 errors on other pages.
  * If Discord genuinely refuses a custom bot token, the dashboard now says so and links to the Custom Bot settings instead of showing empty lists.

## Added
* Added a Manage User Preferences button to level up, streak reminder, streak reset, and XP decay DMs.
  * Opens `cakey.bot/user-customization`, and if you are not signed in you land back on it after logging in.

# September 20th - Cakey Personal
## Changed
* The Manage Subscriptions page now finds and can cancel Cakey Personal subscriptions.

## Added
* Added **Cakey Personal**, a new plan for you rather than for a server. It stacks with Server Premium and Custom Bot and comes as monthly, yearly or a limited lifetime plan.
  * +50% XP and +25% coins, with daily, weekly and monthly rewards doubled.
  * Your own rank card banner, a lime leaderboard highlight with an icon of your choice, and a rank card badge that grows with every month you stay subscribed.
  * Unlimited music queues and playlists, every music filter in any server, and use of the Music Bot in servers without Premium.
  * A monthly AI allowance of 40 chat requests, 10 image generations and 100 voice transcriptions, used after the server's own limit.
  * The Legendary fishing rod for as long as you are subscribed.
  * Server admins can switch off the XP bonus, the coin bonus and personal rank cards, and Custom Bot owners can hide the Personal leaderboard styling.
  * See the [Cakey Personal](/en/feature/cakey-personal) page.
* Added a real **User Customization** page at [cakey.bot/user-customization](https://cakey.bot/user-customization) with notification preferences that apply in every server: level-up DMs, streak reminders, XP decay DMs and achievement pings. Per-server streak and decay DM settings can now be changed there too. See the [User Customization](/en/feature/user-customization) page.
* Added **claim reminders**: `/eco reminders` (or the User Customization page) sends you one DM when your daily, weekly or monthly reward is ready again.
* Added tier colours and the Personal icon to the website leaderboards and the public leaderboard pages.

# September 18th - Invite Tracking & Server Statistics
## Fixed
* Fixed embed pickers on the Announcements page not saving when an embed was chosen on its own.
* Fixed the Achievement add and remove role pickers offering `@everyone`.

## Changed
* The length limit for Custom Stat Channels now applies to the finished name rather than the template, so templates may be up to 200 characters.
  * Member names inside a channel name are shortened to 32 characters so a long name never pushes the rest out.
* Ping role pickers on the Daily Content, Anti-Raid, and Suggestions pages now offer `@everyone`, like the social feed ones already did.
* Bumped AFK message limit from 100 characters to 300 characters.

## Added
* Added a new Invite Tracking feature.
  * Records which invite every new member came through and credits the inviter.
  * Invite leaderboard, join and leave analytics, labels that name a code and can hand out a role, a blacklist, manual adjustments, weekly or monthly reports, and an optional public leaderboard page.
  * Joins from young accounts, rejoins, and self invites can count as fake.
  * Configured from the dashboard, with `/invites view`, `/invites inviter`, `/invites list`, `/invites codes`, `/invites leaderboard`, `/invites stats`, and `/invites sync` in Discord.
* Added invite placeholders for join, leave, and ban announcements, their embeds, and banners: `{inviter.mention}`, `{inviter.invites}`, `{invite.code}`, `{invite.label}`, `{invite.source}`, `{user.joincount}`, `{user.stayduration}`, and more.
* Added a new Server Statistics feature.
  * Records messages per member and channel and time spent in voice, never message content.
  * At a glance numbers, message, voice, and member growth charts, busiest channels and members, a busiest hours heatmap, excluded channels, roles and members, and a CSV export.
  * Activity roles hand a role to everybody past a message or voice threshold, or only to the top members, and take it back when they drop out.
  * Members can opt out of being counted individually with `/serverstats privacy`.
  * Free servers look back 7 days, premium servers 30.
  * `/serverstats server`, `/serverstats me`, `/serverstats user`, `/serverstats channel`, `/serverstats top`, and `/serverstats chart` in Discord, everything else on the dashboard.
* Added activity placeholders for Statistic Channel names and the stats message: `{messages:7d}`, `{voice_hours:7d}`, `{active_members:7d}`, `{top_chatter:7d}`, `{joins:7d}`, `{time:HH:mm}`, and more, each with an optional day window.
* Added custom stat channels, up to 10 per server, named with any mix of server and activity placeholders.
* Added a live preview of the finished stat channel name against Discord's 100 character limit. The part that will not fit is struck out and the placeholder responsible is named.
* Added support for the stats message to carry a saved embed on premium servers, with the placeholders working inside it.
* Added Invite Tracking and Server Stats groups to the dashboard's placeholder picker, with highlighting in the editors.

## Removed
* Removed the `/arc-raiders` command.

# September 16th - In-Dashboard Help & Custom Bot Fixes
## Fixed
* Fixed the navbar dropdowns not opening on the Economy, Feeds, Tags, and Auto Messages pages.
* Fixed the separator and weight unit dropdowns on the Economy page showing two selected entries.
* Fixed the Embed Builder's Send button disappearing when "Send via webhook" is ticked, which made webhook sending impossible.
* Fixed the Required and Excluded Channels pickers for Auto Responder not listing forum channels. See the [Auto Responder wiki page](/en/auto-responder#permissions).
* Fixed `{user.achievement.count}`, `/achievements view`, and `/achievements leaderboard` disagreeing on how many achievements a member has unlocked.
  * All three now count the same thing: achievements actually unlocked that still exist and are enabled.
  * The progress page also no longer mixes up progress between channel- or role-scoped achievements.
* Fixed `/achievements list`, `/eco iteminfo`, `/eco items`, and other embed commands failing with "Unknown error occurred" on some custom bots.
  * Caused by a malformed website URL in the custom bot settings, which the bot applied to every embed link.
  * The dashboard now rejects a URL Discord would not accept, and the bot ignores one that slipped through. See the [Custom Bot wiki page](/en/core/setup-custom-bot#website-url).
* Fixed channel dropdowns coming up empty on the dashboard when the custom bot could not list the server's channels.
  * Falls back to Cakey Bot's own view of the server when it is also a member. See the [Custom Bot wiki page](/en/core/setup-custom-bot#frequently-asked-questions).

## Added
* Added a "How does this work?" button to feature pages on the dashboard, opening the matching wiki article in a side panel (a bottom sheet on mobile) without leaving the page. Covers most feature pages, from Starboard and Leveling to Audit Log and Anti-Raid. Replaces the old "check out our wiki" banners. See the [Web Dashboard wiki page](/en/core/web-dashboard#getting-help-while-you-configure).
* Added rendering for `#`/`##`/`###` headings and `-#` subtext in the Embed Builder's preview, matching what Discord supports in descriptions and field values. See the [Embed Builder wiki page](/en/feature/embed-editor#designing-your-embed).

# September 14th - Higher Economy Balance Cap
## Changed
* Raised the maximum allowed value for the Max Balance setting from 1,000,000,000 to 1,000,000,000,000 (1 trillion). See the [Economy wiki page](/en/feature/economy#customization).

# September 13th - Markdown Editor & New Achievement
## Added
* Added new changelist pop-up modal on the dashboard for the latest changes.
* Added new achievement trigger for economy balance reached.
* Added new manual economy shop item type with a handler role and notification channel.
* Added a new Discord markdown toolbar with an emote button and a fuzzy searchable placeholder picker fed by the wiki descriptions.
* Added the ability to edit text fields directly in the live preview of the embed editor, with markdown and placeholder highlighting while typing.
* Added `/eco daily`, `/eco weekly`, and `/eco monthly` commands.

# September 12th - Embed Builder, Sender Profiles & Leaderboard Periods
## Fixed
* Fixed the Achievements page's channel and role pickers offering nothing but "None" for target channels/roles and ignored roles.
* Fixed a script error on the Achievements page that kept the limit field visible for triggers with no limit and hid the target pickers entirely.
* Fixed achievement trigger names showing a literal `&#x27;` instead of an apostrophe.
* Fixed ticket transcripts and form image uploads silently failing in some deployments, caused by storage credentials not being passed through to the bot's container.
* Fixed channel and role pickers sometimes showing empty right after a shard reconnect; they now fall back to fetching directly from Discord until the cache is ready again.
* Fixed messages sent from the dashboard being able to mention any role rather than only the ones actually written into them.

## Changed
* Replaced the Embed Editor with a new built-in Embed Builder. See the [Embed Builder wiki page](/en/feature/embed-editor) for the full writeup.
* Every modal field on the dashboard now shows a hint underneath it, replacing the separate info tooltips settings pages used before.
* Select menus now open upward when there isn't room below, and stay the width of their trigger inside modals.
* Economy shop item modals now only show the data field relevant to the item type you're editing, with a proper role picker for role-type items.
* Achievements now use the same shared bulk-select bar as other dashboard pages.
* Pinned Leaderboards, Custom Stat Channels, and Counting Milestone Roles now scale with your plan (Free/Premium/Custom Bot) instead of one flat cap for every server - see the Added entries below for the exact numbers.

## Added
* Added Sender Profiles to the Embed Builder - a display name and avatar you can send an embed under, delivered through a webhook the bot keeps in the channel. See the [Embed Builder wiki page](/en/feature/embed-editor#sender-profiles).
* Added weekly and monthly periods to `/leaderboard` and Pinned Leaderboards, alongside the existing all-time view.
* Added Pinned Leaderboards: keep up to 1 (Free), 3 (Premium), or 5 (Custom Bot) leaderboard messages pinned and automatically refreshed in channels of your choice. See the [Leveling wiki page](/en/feature/leveling#pinned-leaderboards).
* Added a server-wide toggle to turn off XP decay DM notifications entirely.
* Added Counting Saves: a purchasable shop item that absorbs one mistake instead of resetting the count, with `/counting saves` to check your balance.
* Added Milestone Roles for the counting game, automatically granted once the count reaches a number you configure - up to 5 (Free), 10 (Premium), or 20 (Custom Bot) per server.
* Added Custom Stat Channels built from placeholders - up to 1 (Free), 3 (Premium), or 5 (Custom Bot) per server - and an optional Stats Message kept updated in a text channel.
* Added two new placeholders: `{server.countbots}` and `{server.counthumans}`.
* Added a Suggestion Ping Role, pinged whenever a new suggestion is posted.
* Added custom emote rendering to Forms - emotes now render as pictures in question text, answer options, and submitted answers.
* Added a submitter mention to the message posted in a form's Submit Channel.

# September 10th - Forms Review & Achievement Scoping
## Fixed
* Fixed large form submissions failing to post to the submit channel at all. A response now spans several embeds, and attaches the whole thing as a file when it would otherwise be cut short.

## Changed
* Filling in a form now checks required and invalid answers before the review step instead of after submitting, outlining every question that needs attention with the reason underneath and jumping to the first one.
* Answers on a form can now be up to 16,000 characters, raised from 4,000.
* The achievements dashboard page was rebuilt around how cramped it was on mobile.

## Added
* Added accept and deny buttons to form submissions posted in Discord, so responses can be decided without opening the dashboard. Denying asks for a reason, which is passed on to the submitter. Reviewer roles control who can press them, falling back to anyone with Manage Server or Administrator when none are set. See the [Forms wiki page](/en/feature/forms).
* Added separate role lists for each decision, so approving or rejecting can both add roles and remove roles at once, replacing the single add-or-remove choice.
* Added a pending role held while a response waits on a decision, roles handed out for submitting at all, and a role pinged when a submission is posted.
* Added pages to forms. A page break splits the questions that follow it onto a new page, pages can be reordered by dragging, and answers are saved as a draft as each page is completed.
* Added Markdown support in question text, covering bold, italics, lists, links, code blocks and tables.
* Added an Image Upload question type. Uploads are re-encoded before being stored, so only the picture itself is kept, and responses carrying images are posted as a gallery with each picture under the question that asked for it.
* Added editing for submissions. A submitter can change their answers until a reviewer decides, the message in the submit channel is rewritten and marked as edited, and the previous answers are kept as a revision.
* Added scheduled opening for forms, with an optional announcement posted when a form opens.
* Added resubmitting after a rejection as a separate setting from allowing multiple submissions.
* Added per channel and per role scoping for achievements, so a trigger can be tracked against one channel or one role instead of server wide. See the [Achievements wiki page](/en/feature/achievements).
* Added achievement tiers, letting achievements be grouped into a ladder such as Chatter I, II and III.
* Added a per achievement unlock message, overriding the server wide one.
* Added ignored roles for achievements, so members holding them don't accumulate progress.
* Added six achievement triggers: obtaining a role, sending gifs, sending stickers, being muted, minutes streamed in voice, and wearing the server tag.
* Added `/achievements showcase`, drawing every badge a member has unlocked as one image.

# September 6th - Multiple Ticket Panels & Thread Tickets
## Fixed
* Ticket ratings are now stored in the database instead of in memory, so a pending rating request is no longer lost when the bot restarts.
* Closing, reopening, claiming, or saving a transcript on a ticket whose panel has been deleted now tells you the panel is gone instead of silently failing. Every ticket command makes the same check.

## Changed
* Tickets now record when they were opened and closed, which the dashboard uses to show median time to close and reply times.

## Added
* Added support for multiple ticket panels, up to 10 per server. Each panel has its own support role, transcript channel, embeds, button label, blacklisted roles, and auto close/remind settings, so you can run separate ticket types side by side.
  * Editing a panel's embed or button now rewrites the panel message already posted in your server, so what members see always matches your settings.
  * Deleting a panel is blocked while it still has open tickets.
* Added thread tickets. A panel can now open tickets as private threads or public threads instead of channels, which keeps them out of your channel list and sidesteps Discord's 50 channel per category limit.
* Added ticket claiming. Staff can claim and unclaim a ticket from the ticket embed or the dashboard, so it's clear who is handling what.
* Added a Ticket Manager page to the dashboard, listing every ticket with its panel, who opened it, who claimed it, status, rating, and last activity.
  * Sort by any column, filter by state or panel, and search by name or ID.
  * Close, reopen, claim, add or remove a user, reply, send a reminder, or delete a ticket without leaving the dashboard.
  * Tracked ticket categories are grouped by panel with a live channel count, so you can see which are close to Discord's 50 channel cap before tickets start failing.

# August 31st - Detailed Audits & Embed Previewer
## Added
* Added detailed dashboard audit logs.
* Added same-page embed previewer support on feature setting pages.

# August 30th - Forms & Bulk Selection
## Changed
* Audit log entries now name what they affected (e.g. the channel or role name) instead of only showing a count.

## Added
* Added a new Forms system for building custom forms with 8 question types and conditional visibility based on answers, roles, boosts, Nitro, server tenure, account age, and permissions. Forms can be a general questionnaire, a ban appeal (approving it unbans the submitter), or a join application (approving it generates and DMs an invite). See the [Forms wiki page](/en/feature/forms) for the full writeup.
* Added a review workflow for form responses: approve/reject with optional reviewer notes, automatic role changes on either outcome, and a DM to the submitter with the decision.
* Added version history for forms, keeping the last 20 saves with a per-section diff and the ability to restore an older version.
* Added a "My Submissions" page so users can see every form they've submitted across all servers using Cakey Bot.
* Added a shared bulk selection bar to 13 dashboard pages, letting you select multiple items and act on them all at once instead of one at a time.
* Added a collapsible mode for the dashboard sidebar.

# August 16th - Counting Command
## Added
* Added new set of `/counting` commands to view various info and stats for the counting channel and punishment role.

# August 15th - Support Ticket Updates
## Changed
* Adjust support tickets to use an internal stored category ID instead of relying on the category name. This allows you to freely rename ticket categories without issue. 

## Added
* Added the ability to change the open ticket button's text.
* Added the ability to rename ticket panels.
* Added toggles for daily content to optionally create a discussion thread.

# August 12th - Starboard Custom Emotes & XP Equations
## Added
* Added support for custom guild emotes on starboard reactions. 
* Added the ability to change _which_ equation Cakey Bot uses to calculate levels for the XP system.

# August 11th - New Achievement Trigger
## Fixed
* Fixed an issue that could cause some achievements to re-trigger an announcement, such as after streak resets.

## Added
* Added a "Reached level X" trigger for achievements so you can customize even more level up rewards. Such as roles & economy money.

# August 7th - Level-Up Message Conditional Placeholders
## Added
* Added conditional placeholder blocks to Level Up Messages, letting you show or hide part of a message based on the level a user just reached.
  * `{#level.N}...{/level.N}` only shows its contents when the level reached is exactly N.
  * `{^level.N}...{/level.N}` shows its contents when the level reached is NOT N.
  * Blocks can be stacked independently for different levels, or nested to build a fallback message that only shows up when none of the listed levels matched.
* Added syntax highlighting to the Level Up Message and Level Up Message (Role Reward) editors on the dashboard, matching the highlighting already used for AutoResponder placeholders.

# August 6th - Suggestion Decisions
## Added
* Added `/suggestion accept`, `/suggestion deny`, `/suggestion duplicate`, and `/suggestion review`, letting staff decide on a suggestion with an optional reason. The suggestion's embed updates to show the outcome (green/red/blue/yellow) and the reason, if one was given. Deciding requires the Administrator or Manage Server permission.
* Added a Suggestions page to the dashboard showing every decision made for your server, with the ability to edit a decision after the fact.
## Changed
* `/suggestion` is now `/suggestion create` - the old `/suggestion` command has been replaced by the subcommand group above.
* A Suggestion Channel must now be configured before members can create suggestions. The setting has moved off Bot Settings onto the new Suggestions page, which is now the only place to configure it.
* The existing Approve/Deny buttons on suggestions now record their decision the same way the new commands do, so they also show up in the dashboard's decision history.

# August 5th - Leveling Position Roles & Self Role Changes
## Fixed
* Fixed fishing bait sometimes being consumed even when it wasn't the bait you had equipped for that cast. Each bait now only gets used up when it was actually selected and its effect applied.

## Changed
* Self roles are now created, edited, and deleted entirely from the dashboard instead of Discord commands. The `/selfrole addrole` and `/selfrole removerole` commands have been removed; `/selfrole use`, `/selfrole unuse`, `/selfrole list`, and `/selfrole embed` still work as before.

## Added
* Added Self Role Groups, letting you make a set of self roles mutually exclusive.
  * Unique groups let a user hold only one role from the group at a time; claiming a different role in the group automatically removes whichever one they held before.
  * Multi-select groups let a user hold up to a configurable number of roles from the group at once, automatically removing their oldest-claimed role once they go over the limit.
  * Groups can optionally require members to already have a specific role, or be a minimum leveling level, before they can claim any role from that group. If a required role is later deleted, claims from that group are blocked with a clear message until an admin sets a new one or removes the requirement.
* Added full management for self roles and self role groups to the dashboard.
* Added the ability to assign unique roles to users in the top 10 leveling positions.

# August 4th - Auto Responder Permission QOL
## Added
* Added the ability to configure required and ignored roles, users and channels for Auto Responders directly in the UI with select menus instead of manually typed placeholders and IDs.

# August 3rd - Birthday Timezones
## Added
* Added the ability for users to set per-user timezones for their birthday announcement overridding the guild timezone.

# August 1st - Lurkr Importing
## Fixed
* Implemented a TON of misc. bug & performance fixes.

## Added
* Added support to import Lurkr levels with the `/setup import-levels` command.
* :CB_Added: Added a "Remove Once Posted" toggle for Custom Content on the Daily Content feature.

# July 31st - New Counting Settings
## Fixed
* Fixed an issue where Discord's new native GIFs (klippy), were being incorrectly deleted within GIF-only category channels.

## Added
* Added the ability to have the Counting Channel fail role be applied temporarily instead of permanent.
* Added the ability to set ignored roles for Counting channel. (Will not contribute or reset the count)
* Added a button to force reset the current count.
* Added the ability to set a custom message/embed for the counting failure message.

# July 27th - Media Category Channel
## Added
* Added new category channel type for combined media content.

# July 26th - Counting Channel
## Added
* Added new counting channel feature.
* Added new `/birthday list` command.
* Birthday related commands now display the year, if the user provided one.
* Auto Mod audit logs now have localized footer timestamps & user ID information similar to other audit logs.
* Added new forum auto unarchive feature.
* Added custom message support for social feed announcements.
* Added temp-ban support for auto ban triggers in auto mod.

# July 19th - Direct Embed Sending
## Fixed
* Fixed an issue preventing users from enabling anti-raid settings.

## Added
* Added the ability to directly send custom embeds to channels/webhooks instead of requiring the user of auto responder triggers using the new embed editor experience.
* Added "Auto Delete Tickets On Close" support ticket option.

# July 18th - Embed Editor Saving/Loading Support
## Added
* Added the ability to save/load your custom embeds directly in the editor! You can read more about this feature here: https://wiki.cakey.bot/en/feature/embed-editor
  * Additionally, you can now select which embed to use from a dropdown menu instead of dealing with long convoluted copy/paste data strings/urls.

# July 17th - Auto Responder Placeholder Syntax Highlighting
## Added
* Added placeholder syntax highlighting for Auto Responders. 

# July 12th - Perceptual Hashing Checks
## Added
* Added perceptual hashing checks for phishing images.
* Added the ability to adjust the aggresive-ness of the perceptual hashing check for anti-phishing.
  * Lower values (e.g. 0.05) require near-exact matches, reducing false positives. Higher values (e.g. 0.30) are more lenient and may flag visually similar images.

# July 8th - Giveaway & Voice Fixes
## Fixed 
* Fixed `/giveaway reroll` & `/giveaway list-entries` commands not displaying any giveaways in the selector. Note, this will only fix giveaways going forward, not any previous giveaways.
* Fixed an issue where temp voice lobbies were not deleted if the last user to leave was a bot.
* Fixed an issue where "Ignore Muted/Deafened User" options were ignored upon leaving the voice chat.
* Fixed an issue where "Ignored Roles" were not always ignored during voice XP calculations.
* Fixed an issue where anti-raid fuzzy score limit flags default value (and other valid values) as NaN.
* Fixed not being able to select forum channels as "Ignored Channels" across the dashboard.
* Fixed channels not being ordered correctly. (Same as their order in Discord)

## Added
* Added an optional parameter to the `/giveaway reroll` command to allow re-rolling only a specific user on the giveaway instead of all winners for multi-winner giveaways.

# June 28th - Additional Bug Fixes
## Fixed
* Fixed an issue where some servers would receive multiple Daily Contents per day.
* Fixed an issue where birthdays would not be announced in some servers.
* Fixed an issue where birthdays would be sent multiple times (on incorrect days)
* Fixed an issue where channel categories were not displaying on some select menus in the web dashboard.
* Fixed an issue where streak and economy leaderboards would show "Unknown" users when leveling was disabled.

# June 19th - Mega Bug Fix Update
## Fixed
* Fixed an issue where paginated commands (such as ping, warnings, etc) would fail when Discord failed to parse the custom emotes.
* Deployed a massive bot-wide set of bug fixes across many features that were caught by our internal sentry system.
* Deployed a fix for birthdays not announcing.

# June 15th - Honey Pot Channel
## Added
* Released new Honey Pot auto mod feature!

# June 6th - Feature Requests
## Fixed
* Fixed a bug where new tickets couldn't be opened by a user if their previous one was manually deleted by an admin.

## Changed
* Added optional parameter to bulk add/remove role commands to apply them as persistent roles.
* Added optional parameter to xp and eco leaderboards to change the number of users returned. Between 3 and 15 users.
* Changed random XP drop default values for min/max XP. (Dropped 500-2,000 to 100-500)

## Added
* Added the ability to set custom cooldowns for leveling xp earning per-category.

# May 31st - Starboard QOL
## Added
* Added the ability to exclude messages from starboard updates if older than X amount of days.

# April 28th - Manual Drop Command
## Added
* Added new `/leveling spawn-xp-drop` command to manually spawn XP drops.
* Added new optional parameter to the `/tag` command to ping a specific user.

# April 11th - Bug Fixes & QOL Features
## Fixed
* Fixed an issue where join/leave announcements would default to "AV" icon for users who didn't have a profile picture set.
* Fixed an issue where some embed URLs would fail to parse.
* Fixed an issue where editing achievements would throw errors or let you change the type.
* Fixed an issue where the progress was displayed incorrect for custom/manual achievement types.
* Fixed an issue where auto messages and auto responders would incorrectly display an embed being set on them when it wasn't.
* Fixed an issue where you couldn't cancel active subscriptions
* Fixed an issue where all subscriptions were listed as "Premium" even if they were not.
* Fixed the "Update Payment Method" button on the "Manage Subscriptions" page.
* Fixed an issue where the custom bot page would incorrectly prompt you to setup a custom bot you didn't have yet.

## Changed
* Migrated to GPT-Image-1.5 instead of DALL-E due to DALL-E being deprecated on May 12th.
* The "Manage Subscriptions" page now displays old/cancelled subscriptions.
* The custom bot setup wizard now includes a button to invite the bot on the final page.

## Added
* Added a check to the Twitch OAuth settings page that checks when your granted OAuth scopes mismatch from Cakey's currently required ones and prompts you to re-link.
* Added a search, sort and filter system to the Server Discovery system on the website.
* Added additional info/properties for servers (such as displaying server's banner & icons for enabled features on the main page)
* Added the ability to remove scheduled cancellations on the "Manage Subscriptions" page.
* Added server owner name/profile picture to server discovery pages.

# April 7th - Server Discovery
## Added
* Due to popular request, Cakey Bot has now created a "Server Discovery" system for servers that use Cakey Bot! You can view servers here: <https://cakey.bot/discovery>
  * Note: No servers are visible due to none being accepted _yet_.
  * Applications are open and will be processed over the next few days, can apply within the dashboard here once you select a server to manage: <https://cakey.bot/dashboard/discovery>
  * Servers MUST utilize cakey bot and keep Cakey Bot in the server.
  * Server Discovery will display things like server name, icon, invite join link, popular features utilized in cakey bot, links to leaderboards, and more!
  * Ranking is purely randomized (and cached for 6h), searching/filtering coming soon.
  * This is a very early release and we will continue to iterate and improve it based on user feedback.

# April 6th - New Achievement Reward Options
## Added
* Added new reward options for achievements:
  * Remove Leveling XP
  * Add/Remove Economy Money 

# April 5th - Leveling QOL Features
## Changed
* Increased mention cooldown limits.
* Split the Ignore Muted toggle for voice leveling XP into two options (Ignored Muted & Ignore Deafened)

## Added
* Added the ability to have XP decay immunity roles that you can give to users.
* Added additional context to the AI chat bot. (i.e. who the bot is chatting with)
* Added the `/setup reset-all-streaks` command to reset ALL user streaks in the server. (For fairness sake, you can NOT reset specific user's streaks.)
* Added the option to give bonus XP for image and video files on messages.
* Added a toggle for level up messages to ping users.
* Added a toggle for support ticket logs to ping users.
* Added Ignored Channels for Audio Transcripts.
* Added Ignored Channels for Auto Quoter.
* Added Ignored Channels for Git Code Previewer.

# April 4th - Random XP Drop Anti-Abuse
## Added
* Added ignored roles setting for streaks.
* Added some anti-abuse/anti-bot features to Random XP Drops including:
  * Toggle to prevent the same person from claiming a drop back to back
  * Toggle to add randomized button placements

# April 2nd - Random XP Drop Multi-Channel Support
## Added
* Added the ability to select multiple channels for the random XP drops. (Bot will randomly select one channel from the list every time a drop is sent. This helps decrease/discourage auto-clickers/botting)

# March 28th - Gist Support & Random XP Drops
## Added
* Added gist support to the git previewer.
* Added new 'Nord' theme for the website.
* Added the "Specific Role Count" stat channel type.
* Released new "Random XP Drop" system for leveling. (Previously known as the Holiday XP Drop system)

# March 21st - Streaks Leaderboard
## Added
* Added new streaks leaderboard to website.

# March 19th - Website Improvements
## Added
* Added new dedicated page for listing and managing your premium/custom bot subscriptions on the dashboard. You can view/cancel subscriptions or update your payment method easier now. (Lifetime purchases should also be listed too)
* Added new fishing leaderboard to the leaderboard pages. (buttons soon to be added into the bot for quick linking too)

# March 6th - RSS Improvements
## Changed
* Reworked RSS feed processing, now allowing feeds to fail few times before getting disabled to account for network errors or temporary outages.

# February 9th - Audit Log Improvements
## Added
* Added the type of channel created that was created to the channel created audit log event.
* Added unique properties for voice and forum channel types to the channel modified audit log event.

# January 13th - Misc Bug Fixes
## Fixed
* Fixed a TON of random/misc bugs and issues that have appeared over past 3 months or so.