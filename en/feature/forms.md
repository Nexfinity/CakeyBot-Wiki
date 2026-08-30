---
title: Forms
description: Custom forms with Cakey Bot - ban appeals, join applications, conditional questions. Build forms, review responses, automate decisions.
published: 1
date: 2026-08-30T21:10:25.952Z
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

**Submit Channel:** If set, every new submission is posted to this channel as an embed.

**Allow Multiple Submissions:** If disabled (the default), a user can only submit the form once.

**Max Responses:** Closes the form automatically once it has collected this many submissions. Leave blank for unlimited.

**Active / Draft:** A draft form is fully editable but its public link returns nothing to submitters (staff with manage access can still open it in preview). Publishing a form takes it out of draft; toggling it inactive afterward stops new submissions without touching the draft state or deleting anything.

**Expires At:** Optional date/time after which the form stops accepting submissions.

**Required Role:** Restricts submission to members holding a specific role. Not used for join applications, since the submitter isn't a member yet.

**Minimum Account Age:** Rejects submitters whose Discord account is younger than this many days.

**Allow External Users:** Lets someone who isn't a member of the guild submit the form. This is turned on automatically for ban appeals and join applications, since neither type of submitter is a current member.

**Allow Anonymous:** Stores a response without the submitter's Discord identity. The submitter still has to sign in with Discord so the form can check they're allowed to submit, but their user ID, name, and answers aren't linked back to them once stored. Because there's no user to act on, a form using this cannot add/remove roles, unban, or invite anyone when a response is decided.

**Success Message:** Custom text shown after a successful submission. Leave blank for the default message.

**Require CAPTCHA:** Adds a Cloudflare Turnstile challenge to the public page.
> Turnstile needs `Turnstile__SiteKey` and `Turnstile__SecretKey` configured on the website. If they're missing, a form with this enabled will refuse every submission rather than silently skip the check.
{.is-warning}

## Approval & Rejection Actions

**Require Approval:** When enabled, a submission has to be reviewed and decided from the dashboard before any of the actions below happen. When disabled, a submission is recorded with nothing further done to it.

**On Approval / On Rejection:** Choose to add roles to, remove roles from, or leave alone the submitter's roles for each outcome, then pick which roles.

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

# Questions

A form is built from questions, added and reordered in the Form Builder. There are 8 question types:

| Type | Description |
| :--- | :--- |
| Short Text | A single line of free text. |
| Long Text | Multi-line free text. |
| Multiple Choice | Exactly one option chosen from radio buttons. |
| Checkboxes | Any number of options chosen from checkboxes. |
| Dropdown | Exactly one option chosen from a dropdown list. |
| Number | A numeric value, optionally bounded by a minimum and maximum. |
| Short Text (Email) | A single line validated as an email address. |
| Short Text (URL) | A single line validated as an absolute URL. |

## Conditional Visibility

Any question can be hidden unless the submitter meets conditions you set, checked against:
* **A previous answer** (equals, doesn't equal, contains, greater than, or less than a value you set).
* **Discord roles** the submitter holds (any of, all of, or none of a list you choose).
* **Server tenure** - how long they've been a member.
* **Account age** - how old their Discord account is.
* **Boost status** - whether they're boosting the server.
* **Nitro status** - whether they have Discord Nitro.
* **Permissions** - whether they hold specific guild permissions.

Conditions within the same group all have to pass (AND); separate groups are combined so that passing any one group is enough (OR). This lets you build something like "show this question if the user has the Verified role AND has been a member 30+ days, OR if they have the Staff role."

> Every condition about the submitter is checked on the server before the page is sent to them. A question they don't qualify for is never included in what their browser receives - it isn't just hidden with CSS.
{.is-info}

# Submitting a Form

Share a form's public link (`https://cakey.bot/forms/<code>`) anywhere - it works for anyone, including people who aren't signed in yet, so a shared link still shows the form's name and description as a preview. Actually answering and submitting requires signing in with Discord.

The public page shows a progress indicator as questions are answered, and a review step summarizing every answer before the final submit. After submitting, the user lands on a status page showing their response's current state (Pending, Under Review, Approved, or Rejected), which they can return to later from the link they were given or from **My Submissions** (`https://cakey.bot/my-form-submissions`), reachable from the user menu once signed in - this lists everything they've submitted across every server that uses Cakey Bot.

# Reviewing Responses

From the Forms page, open a form's Responses to see everything submitted to it. Each response can be approved or rejected with optional reviewer notes attached.

Deciding a response:
* Runs the role changes configured for that outcome (Approval/Rejection Actions above).
* For a **Ban Appeal**, an approval unbans the user from the guild.
* For a **Join Application**, an approval generates the configured invite and DMs it to the applicant, along with any roles held for them (see Join Application Settings above).
* Sends the submitter a DM telling them the outcome, including the invite if one was generated.

A response can only be decided once - approving or rejecting an already-decided response is refused.

You can also export all of a form's responses to CSV from the Responses page.

# Version History

Every save of a form keeps the previous version, up to the last 20. From a form's Version History page you can see what changed between any two versions (a per-section diff) and restore an older version. Restoring is itself just another save, so restoring can be undone the same way.

Editing and re-saving a form reuses its existing question rows rather than recreating them, so responses already collected stay attached to their original questions. If you edit a question's wording after it's already collected answers, those existing answers keep the wording they were originally shown - each answer stores the question text as it was asked at the time, alongside the submitter's answer, so old responses stay readable even after a question is changed or removed entirely.

# Related Commands

Forms are managed entirely through the web dashboard - there are no slash commands for creating, submitting, or reviewing forms.
