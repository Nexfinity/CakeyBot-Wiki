---
title: Endpoints
description: 
published: 1
date: 2023-11-12T16:23:52.440Z
tags: 
editor: markdown
dateCreated: 2023-05-19T05:44:43.759Z
---

# API Endpoints
> We currently have no public endpoints. If you would be interested in playing with our API once we open up testing you can show your interest in our [support Discord](https://cakey.bot/discord).
{.is-warning}

API Base URL:
```
https://cakey.bot/dashboard/public/api
```

# Default Response
Unless otherwise stated, all endpoints will return this standard success code if they succeed:
```
{
	"code": "200"
}
```

# Leveling/XP
## Get Top 10 Users:
**Type:** GET
```py
/leaderboard/top
```

**Example Response:**
```
{
	"code": "200",
	"users": [
		{
			"user_id": "173439637388263425",
			"xp": "5435",
			"avatar": "280ed6b3055cec471deb963d2e90fce1"
		},
		{
			"user_id": "786375627892064257",
			"xp": "5",
			"avatar": "280ed6b3055cec471deb963d2e90fce1"
		}
	]
}
```

## Get User XP:
**Type:** GET
```py
/xp/get/{userid}
```

**Example Response:**
```
{
	"code": "200",
	"xp": "5345"
}
```

## Set User XP:
**Type:** POST
```py
/xp/set/{userid}/{amount}
```

## Add User XP:
**Type:** POST
```py
/xp/add/{userid}/{amount}
```

## Remove User XP:
**Type:** POST
```py
/xp/remove/{userid}/{amount}
```

## Get User Level:
**Type:** GET
```py
/level/get/{userid}
```

**Example Response:**
```
{
	"code": "200",
	"level": "6"
}
```

## Set User Level:
**Type:** POST
```py
/level/set/{userid}/{amount}
```

## Add User Level:
**Type:** POST
```py
/level/add/{userid}/{amount}
```

## Remove User Level:
**Type:** POST
```py
/level/remove/{userid}/{amount}
```

# Moderation

## View All Warnings:
**Type:** GET
```py
/moderation/warn/view/all/{userid}
```

**Example Response:**
```
{
	"code": "200",
	"warnings": [
		{
			"id": "134",
			"username": "CottageDwellingCat1",
			"moderator": "MrCakeslayer#1337",
			"reason": "some text",
			"timestamp": "2018-09-04 11:29:30"
		},
		{
			"id": "1965",
			"username": "CottageDwellingCat1",
			"moderator": "MrCakeslayer#1337",
			"reason": "spamming",
			"timestamp": "2018-10-04 12:39:50"
		}
	]
}
```

## View Single Warnings:
**Type:** GET
```py
/moderation/warn/view/single/{userid}/{warn_id}
```

**Example Response:**
```
{
	"code": "200",
	"username": "CottageDwellingCat1",
	"moderator": "MrCakeslayer#1337",
	"reason": "some text",
	"timestamp": "2018-09-04 11:29:30"
}
```

## Warn User:
**Type:** POST
```py
/moderation/warn/add/{userid}/{reason}
```

## Unwarn User:
**Type:** POST
```py
/moderation/warn/remove/{warn_id}
```
