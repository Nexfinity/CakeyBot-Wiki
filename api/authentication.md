---
title: Authentication
description: 
published: 1
date: 2023-05-20T00:33:58.116Z
tags: 
editor: markdown
dateCreated: 2023-05-19T05:43:11.629Z
---

# Overview
Cakey Bot exposes a select few API endpoints to help you automate some of Cakey Bot's features and extend them into your own websites and bots. Note this API may change over time and endpoints may be added, changed or removed. If you would like to stay up-to-date on all of our changes regarding the API you should join our [support Discord](https://cakeybot.app/discord).

# Authentication
Access to the API requires a valid API token, which can be generated from the "Bot Settings" page.

The token must be passed in the Authorization header, as a Bearer token, for ALL requests made to the Cakey Bot API:

```
Authorization: Bearer eyJhbGc...aXczt18H6437W
```

# Rate Limits
There is a global rate limit of 60 requests per 1 minute across all endpoints. However, some endpoints maybe have a stricter rate limit. In these cases, the stricter rate limit will be noted on the specific end points.

# Error Handling
## Receiving Errors
By default Cakey Bot's website (including API) will return HTML-style error messages. If you would like to receive these as JSON-style messages for the API you should include a JSON accept header on your request like so:

```
Accept: application/json
```

If you accept errors as JSON they will be formatted with a "code" value as well as an "error" value like so:
```
{
	code: "403",
	error: "You don't have access to this endpoint."
}
```

## Error Types
Cakey Bot will return these types of errors:
| Code      | Description |
| ----------- | ----------- |
| 400 | Bad request/invalid input. |
| 401 | Missing API token. |
| 401 | API token invalid. |
| 403 | You don't have access to this endpoint. |
| 404 | API endpoint not found. |
| 405 | Method not allowed for this route. |
| 418 | I'm a teapot. |
| 429 | Too many requests. Please try again later. |
| 500 | Internal server error. |

> Note: The "418: I'm a teapot" error is fairly uncommon. In Cakey Bot's API we use this as a generic "Hey you aren't supposed to be here yet" error message for upcoming/unreleased endpoints.
{.is-secondary}
