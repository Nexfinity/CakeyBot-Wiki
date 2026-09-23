---
title: Forms
description: Custom forms with Cakey Bot - ban appeals, join applications, conditional questions. Build forms, review responses, automate decisions.
published: 1
date: 2026-09-23T12:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-08-30T20:34:56.856Z
---

# Overview

> You will need **`Manage Server`** or **`Administrator`** permission (or Dashboard Access granted to you, see [Dashboard Access](/en/core/dashboard-access)) to build or manage forms.
{.is-warning}

Forms let you collect structured answers from users through a public web page instead of a Discord command or a plain message. A form can be a general questionnaire, a **ban appeal** that unbans the submitter on approval, or a **join application** that generates an invite for them once approved. Every submission can be reviewed from the dashboard, with approve/reject actions that can add or remove roles, unban the user, or send them an invite automatically.

# Creating a Form

1. Login to our [web dashboard](https://cakey.bot/dashboard).
2. Go to "Forms".
3. Click "Create Form" to open the Form Builder.

**Name/Description:** Shown at the top of the form's public page and on its card in the dashboard.

**Form Type:** Determines who can submit and what an approval does.
* **Regular:** An ordinary form submitted by members of the guild.
* **Ban Appeal:** Submitted by users who are currently banned from the guild. Approving it unbans them.
* **Join Application:** Submitted by users who are not yet in the guild. Approving it generates a one-time invite and DMs it to them.

**Submit Channel:** If set, every new submission is posted to this channel, mentioning the submitter by name. A response containing image answers is posted as a gallery rather than an embed, and a response too long for one Discord message has the whole thing attached as a Markdown file alongside the summary.

> The submitter mention identifies who responded but doesn't actually ping them - only the **Notify Role** mention (if set) sends a real notification. Forms using **Allow Anonymous** show "Submitted anonymously" instead, since there's no Discord identity to mention.
{.is-info}

**Notify Role:** If set, this role is pinged when a submission is posted to the Submit Channel.

**Roles Given On Submit:** Roles handed to the submitter for submitting at all, before anyone reviews anything. Useful for a "Pending Review" tag.

**Allow Multiple Submissions:** If disabled (the default), a user can only submit the form once.

**Allow Resubmitting After Rejection:** Lets a rejected user submit again, even when Allow Multiple Submissions is off.

**Allow Editing After Submitting:** Lets submitters change their answers until the response is decided (see [Editing a Submission](#editing-a-submission)). On by default. Turn it off and the Edit my answers link is hidden and edits are refused.

**Max Responses:** Closes the form automatically once it has collected this many submissions. Leave blank for unlimited.

**Active / Draft:** A draft form is fully editable but its public link returns nothing to submitters (staff with manage access can still open it in preview). Publishing a form takes it out of draft; toggling it inactive afterward stops new submissions without touching the draft state or deleting anything.

**Opens At:** Optional date/time before which the form doesn't accept submissions. Pair it with Expires At to run a form for a fixed window.

**Expires At:** Optional date/time after which the form stops accepting submissions.

**Announcement Channel / Role / Message:** When a form has an Opens At time, Cakey can post an announcement the moment it opens, optionally pinging a role. The announcement is only ever posted once per form. The message supports [placeholders](#placeholders).

**Required Role:** Restricts submission to members holding a specific role. Not used for join applications, since the submitter isn't a member yet.

**Minimum Account Age:** Rejects submitters whose Discord account is younger than this many days.

**Allow External Users:** Lets someone who isn't a member of the guild submit the form. This is turned on automatically for ban appeals and join applications, since neither type of submitter is a current member.

**Allow Anonymous:** Stores a response without the submitter's Discord identity. The submitter still has to sign in with Discord so the form can check they're allowed to submit, but their user ID, name, and answers aren't linked back to them once stored. Because there's no user to act on, a form using this cannot add/remove roles, unban, or invite anyone when a response is decided.

**Success Message:** Custom text shown after a successful submission and in the DM confirming it. Leave blank for the default message. Supports [Markdown](#formatting) and [placeholders](#placeholders).

**Require CAPTCHA:** Adds a Cloudflare Turnstile challenge to the public page.
> Turnstile needs `Turnstile__SiteKey` and `Turnstile__SecretKey` configured on the website. If they're missing, a form with this enabled will refuse every submission rather than silently skip the check.
{.is-warning}

## Approval & Rejection Actions

**Require Approval:** When enabled, a submission has to be reviewed and decided before any of the actions below happen. When disabled, a submission is recorded with nothing further done to it.

**Roles Added / Removed On Approval** and **Roles Added / Removed On Rejection:** Four separate lists. Each decision can both add roles and remove roles at the same time, so you can swap a "Pending" role for a "Verified" one in a single action.

**Pending Role:** Given to the submitter while their response is waiting on a decision, and taken away automatically once it's decided either way.

**Reviewer Roles:** Who is allowed to press the accept and deny buttons on the submission message in Discord (see [Reviewing Responses](#reviewing-responses)).
> Leave Reviewer Roles empty and anyone with **`Manage Server`** or **`Administrator`** can decide responses from Discord instead. Set it to restrict that to specific roles.
{.is-info}

## Ban Appeal Settings
*Only shown for the Ban Appeal form type.*

**Appeal Delay:** Requires this many days to pass since the ban (read from the guild's audit log) before the user is allowed to appeal at all.

**Block Reappealing After Rejection:** If enabled, one rejected appeal permanently bars the user from submitting this form again.

**Max Appeal Attempts:** Caps how many times a user can be rejected before they're barred from appealing again. Ignored if reappealing is already blocked after a single rejection.

**Reappeal Cooldown:** Requires this many days to pass after a rejection before the user can appeal again.

A user can only ever have one appeal pending or under review on a form at a time.

## Join Application Settings
*Only shown for the Join Application form type.*

**Invite Uses / Invite Expiry:** How many times, and for how long, the invite generated on approval stays valid.

**Roles Held For Applicant:** Roles from this list are saved for the applicant the moment they're approved, and applied automatically as soon as they actually join through the generated invite - they don't need to still be present at approval time for this to work.

## Placeholders

The Success Message and the Announcement Message can use these placeholders. A hint under both fields in the builder lists the form ones.

`{form.name}` - The name of the form\
`{form.link}` - The link people use to open the form\
`{form.role}` - The form's Required Role\
`{form.submissions}` - How many submissions the form accepts (Max Responses, otherwise unlimited or 1)\
`{form.opensat}` - When the form opens\
`{form.expiresat}` - When the form closes\
`{user.mention}` - Mentions the submitter\
`{user.id}` - The submitter's ID\
`{user.username}` - The submitter's username\
`{user.globalname}` - The submitter's display name\
`{server.name}` - The server's name\
`{server.id}` - The server's ID

The `user` placeholders describe the submitter, so they come out empty in the launch announcement, which isn't about anyone. On the website, where Discord markup would show up raw, a mention, role, or date is written out as a plain name or date instead. Anything else in curly braces is left as written.

See the [Placeholders](/en/placeholders) page for more on how placeholders work.

# Questions

A form is built from questions, added and reordered in the Form Builder. There are 9 question types:

| Type | Description |
| :--- | :--- |
| Short Text | A single line of free text. |
| Long Text | Multi-line free text. |
| Multiple Choice | Exactly one option chosen from radio buttons. |
| Checkboxes | Any number of options chosen from checkboxes. |
| Dropdown | Exactly one option chosen from a dropdown list. |
| Number | A whole number, optionally bounded by a minimum and maximum. |
| Short Text (Email) | A single line validated as an email address. |
| Short Text (URL) | A single line validated as an absolute URL. |
| Image Upload | A picture uploaded by the submitter. |

A question can also carry an **image of its own**, shown above the answer field. That's separate from the Image Upload type: one is a picture you show the submitter, the other is a picture you ask them for.

## Formatting

Question text, answer options for multiple choice and checkbox questions, the form's description, the Success Message and reviewer notes all support a subset of Markdown: headings (`#`, `##`), bold, italics, underline (`__text__`), strikethrough, subtext (`-#`), lists, links, inline code, code blocks and tables. Formatting follows Discord's rules, so text looks the same on the website as in the DMs Cakey sends. Line breaks are kept as written, so you can lay out examples across several lines.

> Anything that isn't plain formatting or a normal `http`/`https` link is stripped before the page is sent. A question cannot be used to inject scripts into the form.
{.is-info}

Discord custom emotes (typed as `<:name:id>`, or pasted as a `cdn.discordapp.com` emoji link) are rendered as pictures wherever they appear - in question text, answer options, and submitted answers on the dashboard's Responses page.

## Pages

Adding a **page break** splits everything after it onto a new page. Submitters answer one page at a time with Back and Next buttons, and a page counter above the progress bar and beside the buttons.

Each page can have its own title and introduction text, and pages can be dragged into a different order in the builder without disturbing the questions inside them.

To put a question on a different page, use **Move to page** on the question. Pick the page, then choose **Move** to take it there or **Copy** to leave the original where it is. The builder then switches to that page.

Page breaks aren't questions. They're left out of the question count on the Forms page, the responses and the CSV export.

Answers are saved as a draft as each page is completed, so closing the tab part way through doesn't lose anything. Reopening the form picks up where the submitter left off.

## Image Upload Questions

Submitters attach a picture (PNG, JPEG, GIF or WebP) up to 8 MB.

Every upload is decoded and re-encoded before it's stored, so only the actual pixels survive. Anything hidden inside the file is discarded rather than being served back out. Uploads are stored on Cakey's own CDN rather than linked from wherever the submitter got them, so an image can't be swapped out after it's been reviewed.

> SVG files are refused. They're XML and can carry scripts, so they're never accepted as an answer.
{.is-warning}

## Quoting Earlier Answers

Turn on **Quote earlier answers in this question** and write `{{Q1}}` in a question's text to show the answer given to question 1, `{{Q2}}` for question 2, and so on. Questions are numbered in order across the whole form, page breaks not included. Until the earlier question is answered, the placeholder shows nothing, and long answers are cut down to 100 characters.

Duplicating or moving questions updates these numbers, so they still point at the same questions.

## Required Only When

A question can be made required only when an earlier answer matches something, using **Required only when** in its settings. Leave it on **Always use the setting above** to just follow the question's normal Required setting.

## Conditional Visibility

Any question can be hidden unless the submitter meets conditions you set, checked against:
* **A previous answer** (equals, doesn't equal, contains, greater than, less than, is answered, or is not answered). For multiple choice, dropdown and checkbox questions you pick the expected answer from that question's options instead of typing it, so renaming an option doesn't silently break the condition. A condition on a question the submitter can't see never passes.
* **Discord roles** the submitter holds (any of, all of, or none of a list you choose).
* **Server tenure** - how long they've been a member.
* **Account age** - how old their Discord account is.
* **Boost status** - whether they're boosting the server.
* **Nitro status** - whether they have Discord Nitro.
* **Permissions** - whether they hold specific guild permissions.

Conditions are grouped into **rule sets**. Each rule set has its own setting for how its conditions combine:
* **All conditions must pass** (AND)
* **Any condition can pass** (OR)

Use **Add rule set** to add another one. The question shows when **any** rule set passes. This lets you build something like "show this question if the user has the Verified role AND has been a member 30+ days, OR if they have the Staff role" with two rule sets.

> Every condition about the submitter is checked on the server before the page is sent to them. A question they don't qualify for is never included in what their browser receives - it isn't just hidden with CSS.
{.is-info}

# Submitting a Form

Share a form's public link (`https://cakey.bot/forms/<code>`) anywhere - it works for anyone, including people who aren't signed in yet, so a shared link still shows the form's name and description as a preview. Actually answering and submitting requires signing in with Discord. The page shows the server's icon, with its banner above it if it has one.

The public page shows a progress indicator as questions are answered, and a review step summarizing every answer before the final submit. After submitting, the user lands on a status page showing their response's current state (Pending, Under Review, Approved, or Rejected, or just Received for a form without Require Approval), which they can return to later from the link they were given or from **My Submissions** (`https://cakey.bot/my-form-submissions`), reachable from the user menu once signed in - this lists everything they've submitted across every server that uses Cakey Bot. When the form lets them submit again (Allow Multiple Submissions, or Allow Resubmitting After Rejection after a rejection), My Submissions shows a **Submit again** link.

Required questions and invalid answers are caught before the review step, across every page rather than only the one being looked at. Each question needing attention is outlined with the reason underneath it, and the page jumps to the first one.

The submitter also gets a DM confirming the submission, with a **View Submission** button linking to their status page.

## Editing a Submission

A submitter can change their answers from their status page for as long as the response hasn't been decided, as long as the form has **Allow Editing After Submitting** on. Once a reviewer approves or rejects it, editing is refused - what the reviewer acted on stays as they read it.

Editing a response:
* Rewrites the message in the Submit Channel so reviewers see the current answers, marked as edited.
* Keeps the previous answers as a revision.
* Sends the submitter a DM confirming the change.

# Reviewing Responses

Responses can be decided from either the dashboard or Discord.

**From the dashboard:** open a form's Responses from the Forms page to see everything submitted to it. Each response can be approved or rejected with optional reviewer notes attached.

**From Discord:** when a form has Require Approval enabled, its submission message in the Submit Channel carries **Accept** and **Deny** buttons. Denying opens a box asking for a reason, which is passed on to the submitter. Who may press them is controlled by Reviewer Roles (see [Approval & Rejection Actions](#approval-rejection-actions)); with none set, anyone holding **`Manage Server`** or **`Administrator`** can. Once decided, whether from Discord or the dashboard, the message is recoloured, records who decided it, has its buttons removed, and gets a ✅ or ❌ reaction so the outcome shows at a glance.

Deciding a response:
* Runs the role changes configured for that outcome (Approval/Rejection Actions above).
* For a **Ban Appeal**, an approval unbans the user from the guild.
* For a **Join Application**, an approval generates the configured invite and DMs it to the applicant, along with any roles held for them (see Join Application Settings above).
* Sends the submitter a DM telling them the outcome, including the invite if one was generated.

A response can only be decided once - approving or rejecting an already-decided response is refused.

You can also export all of a form's responses to CSV from the Responses page, with one column per question.

# Version History

Every save of a form keeps the previous version, up to the last 20. From a form's Version History page you can see what changed between any two versions (a per-section diff) and restore an older version. Restoring is itself just another save, so restoring can be undone the same way.

Editing and re-saving a form reuses its existing question rows rather than recreating them, so responses already collected stay attached to their original questions. If you edit a question's wording after it's already collected answers, those existing answers keep the wording they were originally shown - each answer stores the question text as it was asked at the time, alongside the submitter's answer, so old responses stay readable even after a question is changed or removed entirely.

# Related Commands

Forms are managed entirely through the web dashboard - there are no slash commands for creating, submitting, or reviewing forms.
