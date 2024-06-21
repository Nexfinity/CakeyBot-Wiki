---
title: Placeholders
description: 
published: 1
date: 2024-06-21T17:19:35.330Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:00:48.805Z
---

# Overview

> **Quick reminder:** You must include the brackets { } when typing the placeholder so Cakey Bot knows to replace it with the correct values.
{.is-success}

![Example usage of placeholders](/placeholders1.png)

> Don't know how to find role/channel/user IDs? You can use this extremely detailed and easy to follow guide [here](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID) written by Discord.
{.is-info}

# Basic Placeholders

## User

`{@username}` - Mentions a specific user. Replace **"username"** with their username\
`<@userid>` - Mentions a specific user. Replace **"userid"** with their user ID _(More reliable)_\
`{user.id}` - The ID of the user\
`{user.nickname}` - The user’s nickname
`{user.username}` - The user’s username
`{user.avatar}`- The user’s avatar URL\
`{user.mention}` - Mentions the user\
`{user.createdAt}` - The user’s registration date\
`{user.joinedAt}` - The user’s server join date
`{user.ispending}` - Whether the user is pending or not (completed welcome verification)
`{user.timedoutuntil}` - How long the user is timed out until
`{user.isstreaming}` - The user's streaming status

## Channel

`{channel}` - The channel name where the command was used\
`{channel.id}` - Channel ID\
`{channel.name}` - Channel name\
`{channel.mention}` - Channel mention\
`{#channel}` - A channel mention. Replace "**channel"** with the name of the channel\
`<#channelid>` - A channel mention. Replace "**channelid**" with the ID of the channel _(More reliable)_
`{channel.isnsfw}` - Whether the channel is flagged as NSFW or not
`{channel.created}` - The date and time the channel was created
`{channel.position}` - The position of the channel in the channel list
`{channel.topic}` - The topic of the channel
`{channel.threadcount}` - The number of threads under a channel
`{channel.slowmodeinterval}` - The slow mode interval on the channel

## Thread
`{thread.ownername}` - The dusplay name for the thread creator
`{thread.ownermention}` - A user mention for the thread creator
`{thread.isprivate}` - True/False if the thread is private or not
`{thread.members}` - The count for the number of members added to the thread
`{thread.parentchannelname}` - The name of the thread's parent channel
`{thread.parentchannelid}` - The ID of the thread's parent channel
`<#{thread.parentchannelid}>` - A channel mention for the thread's parent channel

## Server

`{server.id}` - Server’s ID\
`{server.name}` - Server’s name\
`{server.icon}` - Server’s icon\
`{server.memberCount}` - Number of members in the server\
`{server.ownerID}` - Owner’s ID\
`{server.createdAt}` - Server’s creation date\
`{server.region}` - Server’s region\
`{server.ownername}` - Owner’s Username\
`{server.splashurl}` - Splash URL (if one is set)\
`{server.bannerurl}` - Banner URL (if one is set)\
`{server.verificationlevel}` - The server's verification/moderation level\
`{server.vanityurl}` - Vanity URL code\
`{server.boostlevel}` - Boosted tier level\
`{server.boostcount}` - The number of boosts the server has\
`{server.vanityurl}` - Vanity URL code\
`{server.afkchannel}` - AFK channel name\
`{server.afktimeout}` - The AFK timeout (in seconds)\
`{server.countallchannels}` - The number of channels in the server\
`{server.counttextchannels}` - The number of **text** channels in the server\
`{server.countvoicechannels}` - The number of **voice** channels in the server\
`{server.countemoji}` - The number of emoji in the server\
`{server.countroles}` - The number of roles in the server
`{server.countstagechannels}` - The number of stage channels in the server
`{server.countevents}` - The number of events in the server
`{server.countcategories}` - The number of category channels in the server
`{server.countstickers}` - The number of stickers in the server
`{server.ruleschannel}` - The current rules channel (community-enabled servers)
`{server.maxuploadlimit}` - The current max upload limit for files (Depends on boost level)

## Role

`{&role}` - Mention a role by name. Replace "**role"** with the role name\
`<@&roleid>` - Mention a role. Replace "**roleid"** with the role ID _(More reliable)_

## Time & Date

`{time}` - Current 24 hour time\
`{time12}` - Current 12 hour time\
`{date}` - Current date\
`{datetime}` - Current date with the 24 hour time\
`{datetime12}` - Current date with the 12 hour time

> Currently, all times & dates are for the United States Eastern timezone. In the future, you will be able to select your timezone per-server.
{.is-warning}

## Mentions

`{@username}` - Mentions a specific user. Replace **"username"** with their username\
`<@userid>` - Mentions a specific user. Replace **"userid"** with their user ID _(More reliable)_\
`{user.mention}` - Mentions the user\
`{channel.mention}` - Channel mention\
`{#channel}` - A channel mention. Replace "**channel"** with the name of the channel\
`<#channelid>` - A channel mention. Replace "**channelid**" with the ID of the channel _(More reliable)_\
`{&role}` - Mention a role by name. Replace "**role"** with the role name\
`<@&roleid>` - Mention a role. Replace "**roleid"** with the role ID _(More reliable)_\
`{everyone}` - Mentions `@everyone`\
`{noeveryone}` - Disables `@everyone` (being able to mention everyone) in the command\
`{here}` - Mentions `@here`\
`{nohere}` - Disables `@here` (being able to mention everyone online with `@here`) in the command\
`{nomentions}` - Disables **ALL** mentions in the command **including** `@everyone`, `@here`, role mentions & user mentions.

## Message

`{messagelink}` - Displays a Discord message link/url to the original command/message that triggered the response\
`{quote:#channelid}` - Quote the last message in the provided channel. Replace "**channelid**" with the ID of the channel\
`{reply}` - Sends the response as a Discord "reply" to the message that triggered it.

## Other

`{random:min:max}` - Generates a random number between the min/max. Replace "**min**" and "**max**" with a number between 0 and 999,999,999. **Note:** Your minimum number must be smaller than your maximum number.\
`{delay:0-60}` - Delays the response for up to 60 seconds. Only the first delay placeholder in a response will work. If you exclude the delay placeholder then responses will be sent instantly.

> **Note:** The delay placeholder only accepts a number, **not** a range of numbers. For example, if you wanted to do 35 seconds, you would use `{delay:35}` **not** `{delay:0-35}`.
{.is-info}

# Advanced Placeholders

> _Advanced Placeholders only work on "Auto Responders". They will **not** work on join/leave/ban announcements._
{.is-warning}

## Delete

> **Note:** Delete placeholders will not work while using DM placeholders on a command.
{.is-warning}

`{delete}` - Delete initial message the user sent _after_ the response sent.
`{deleteafter:x}` - Delete the response automatically after `X` amount of seconds. Replace the `x` with a number between 1 and 99.
`{confirmdelete}` - Add a trashcan button to the response that deletes the response when it is clicked. (Similar to AFK messages & Git Previews)

> These require Cakey Bot to have "Manage Message" permissions.
{.is-info}

## Require

`{require:&role}` - Set the required role to use the command. Replace "**role**" with the role ID.\
`{require:#channel}` - Set the required channel that the command can be run in. Replace "**channel**" with the channel ID.\
`{require:@user}` - Set the specific user who can use this command. Replace "**user**" with the user ID.

Examples:

```asciidoc
{require:&237273200055156736}    //Specific role ID

{require:#225182513465786369}    //Specific channel ID

{require:@225182513465786369}    //Specific user ID
```

## Not

`{not:&role}` - Blacklist a specific role from using the command. Replace "**role**" with the role ID.\
`{not:#channel}` - Blacklist the command from being run in a specific channel. Replace "**channe**l" with the channel ID.\
`{not:@user}` - Blacklist a specific user from using the command. Replace "**user**" with the user ID.

Examples:

```asciidoc
{not:&237273200055156736}    //Specific role ID

{not:#225182513465786369}    //Specific channel ID

{not:@225182513465786369}    //Specific user ID
```

## Add Tag/Remove Tag on Forums/Threads
> These placeholders will only trigger for the initial post on a new thread. Existing threads will be unaffected.
{.is-warning}

`{addtag:tag-name-here}` - Adds a tag to the thread if it doesn't exist already.
`{removetag:tag-name-here}` - Removes a tag from the thread if it exists.

## Forum/Thread Posts/Comments

`{closethread}` - Closes/archives the thread to prevent new replies/comments.
`{lockthread}` - Locks the thread so that only moderators can open/unlock it.
`{deletethread}` - Deletes the thread entirely.

> Using the thread placeholders *below* will prevent the message from being triggered inside of ALL non-thread channels.
{.is-warning}

`{originalpostonly}` - Only trigger for the original post in a thread.
`{commentsonly}` - Only trigger for messages that are a comment inside of a thread.

## Respond

`{respond:#channel}` - The channel that the command will send the response to. Replace "**channel**" with the channel ID. _Limited to one channel per command._

## DM

> Cakey Bot can sometimes fail to send a DM if the user has their privacy settings set to block DMs from users in the server. This is NOT a bug and not something Cakey Bot can bypass.
{.is-warning}

`{dm}` - Direct message the bot response to the user who called the command. _**Limited to one DM per command.**_\
`{dm:@user}` **-** Direct message the bot response to the specified user. Replace **"user"** with the user ID. _**Limited to one DM per command.**_

Examples:

```asciidoc
{dm:@225182513465786369}    //Specific user ID
```

> Spamming commands that use this variable will lead to your server being blacklisted from using Auto Responders.
{.is-danger}

## Response Chance

Don't want to have the bot respond every...single...time? Well with the response chance placeholder, you can set a percentage between 0% and 100% for the bot to respond or not respond to the trigger. Also, only the first chance placeholder will be taken into account, any extras will be ignored. You can see some examples below:

```asciidoc
{chance:0}   //0% chance to respond
{chance:35}  //35% chance to respond
{chance:100} //100% chance to respond
```

_(Note: You don't need `{chance:100}` to make the bot respond all the time, simply excluding **any** chance placeholder will act as 100%)_

## Link/URL Buttons

`{linkbutton:(text)[url]}` - Adds a link button to the message. Replace "text" with what you want the button to say and replace "url" with the link/url you want the button to open in the browser. _There is a limit of 25 buttons per message/response and a max of 80 characters for the button text._

Examples:

```asciidoc
{linkbutton:(Cakey Bot)[https://cakey.bot]}
{linkbutton:(Open Link)[https://google.com]}
{linkbutton:(Some Random Text)[https://youtube.com]}
```

## Message Management
`{createthread}` - Creates a thread using the triggering message
`{pinmessage}` - Pins the triggering message
> Note: Discord has a limit of 50 pins per-channel. 
{.is-info}

## User Management
> Note: Cakey Bot must have access to manage roles & Cakey Bot's highest role must be above the role you are trying to grant/remove from the user. Cakey Bot's role must also be higher than the user's highest role.
{.is-info}

`{addrole:<id>}` - Adds a role to the user.
`{removerole:<id>}` - Removes the role from the user.

## Leveling/XP
`{xp-add:<amount>}` - Adds XP to the user.
`{xp-remove:<amount>}` - Removes XP from the user.

## Economy
`{user.balance}` - Displays the user's current economy balance as a raw number. (No commas)
`{user.balance-formatted}` - Displays the user's current economy balance with a formatted number. (With commas)
`{economy-add:<amount>}` - Adds economy money to the user.
`{economy-remove:<amount>}` - Removes economy money from the user.

## Moderation
> Note that moderation placeholders will only work on Auto Responders and can NOT be used for Announcements.
{.is-info}

- The maximum time for any temporary moderation action used in an Auto Responder is 27 days. Invalid times will be ignored or capped to 27 days.
- The time for temporary moderation actions must be formatted in a `5d6h2m7s` format. (You can include just the times you need, for example you could just do `1d`)
- Any provided reason will be trimmed to 500 characters regardless of original length.
- You can include multiple punishment types on the same response, however, only the _first_ punishment of _each_ type will be applied.
  - For example, if you include two warnings and a timeout on a response, the first warning and the timeout will be applied but the second warning will be ignored.
```asciidoc
{warn:reason}
{timeout:reason:time}
{kick:reason}
{ban:reason}
{tempban:reason:time}
```

## Reactions

> **Note:** This placeholder will not work on messages that use `{confirmdelete}` or `{dm}`. Also, Cakey Bot can ONLY use Emoji from any server that Cakey Bot is in. (Similar to nitro users)
{.is-warning}

You can also add reactions to responses (up to 3). To add a reaction simply include a reaction placeholder anywhere in the response string. You will need to get Discord's unique ID for the reaction you plan to use. You can do this by typing the emoji in Discord and placing a backslash in front of it. Some placeholder examples are shown here:

```asciidoc
{react:<a:200IQ:730769872698736692>} //Animated/Gif Emote
{react:<:r6s:847490914749382719>}    //Custom Server Emote
{react:😄}                           //Normal Unicode Emote
```

You can also have reactions apply to the original message that triggered the auto responder by using the `{reactoriginal}` placeholders:
```asciidoc
{reactoriginal:<a:200IQ:730769872698736692>} //Animated/Gif Emote
{reactoriginal:<:r6s:847490914749382719>}    //Custom Server Emote
{reactoriginal:😄}                           //Normal Unicode Emote
```

## Choose & Choice

The `{choose:}` and `{choice}` variables let you pick random items from a list or lists.\
To set up a list, use `{choose:item1;item2;item3}`. You can have up to 10 lists, using `{choose1:}`, `{choose2:}`, and so on. You can have up to 20 items per list.

`{choice}` - Get a random value from your list.\
`{choice3}` - Get a random value from list 3.

Examples:

```asciidoc
{choose:pie;cake;icecream;}
{user.Username} likes {choice}

{choose1:apples;oranges;pears}
{choose2:dogs;cats;horses}
My favorite fruit is {choice1} and my favorite animal is {choice2}!
```

## Math Expressions
The `{math:X}` placeholder allows you to parse math expressions! 

Example:
```asciidoc
What is 5-2? It is: {math:5-2}!
```

## Arguments/$N Variable
`$N` - Returns a command argument.

**Examples:**

```
Input: !slap Joe a big fish
Response: You slapped $1 with $2 $3+
Result: You slapped Joe with a big fish
```

$1 represents the first argument (Joe) in the command call.\
$2 represents the second argument (a), and so on.\
$3+ represents all the arguments after the first one in the command call (big fish) since Joe is the first argument.

> **Remember:** Do **not** include this variable in the initial command/trigger. Place $1 $2 and so on **only** in the _response_ field.&#x20;
{.is-info}

![The diagram above is a visual representation of how argument variables work in auto responders.](/placeholders2.png)