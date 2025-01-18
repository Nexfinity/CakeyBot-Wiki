---
title: Economy
description: 
published: 1
date: 2025-01-18T16:20:27.413Z
tags: 
editor: markdown
dateCreated: 2024-03-14T19:35:02.607Z
---

# Overview
> This feature is still currently in "BETA" and may change considerably before release.
{.is-warning}
## Basic Commands
* **/eco balance** - Check your balance or the balance of another user.
* **/eco leaderboard** - View the top 10 users on the leaderboard.
* **/eco pay** - Pay another user.

# Earn Money
## RNG Games
There's several games that rely entirely on RNG/randomization to determine the outcome. These games tend to have the highest risk-to-reward ratio and are usually more pfoitable. they can also be played entirely solo so you don't have to wait on other users to play. These games include:
* **/eco coinflip** - Guess the result to win 50% of your bet.
  * There's a 0.02% chance for the coin to land on it's side. If this occurs, the player wins 2x their bety regardless of their guess.
* **/eco guess** - Guess the number (1-10) for a chance to gain 2x-3x the amount.
  * You also get 2x if you are +/- 1 off from the correct answer instead of 3x.

## Player VS Player Games
There's also several games that allow you to directly challange other users in the server. These tend to be a little less profitable than RNG games but can introduce a new level of competition and fun among the players. These games include:
* **/eco rock-paper-scissors** - Challenge another user to Rock, Paper, Scissors.
* **/eco split-or-steal** - Challenge another user to split or steal.

## Other
Cakey Bot also includes several other ways to earn money that do not include any games, though some of them still include a certain level of RNG that can affect the profits. These commands include:
* **/eco work** - Work for money.
* **/eco rob** - Attempt to rob another user.
* **/eco beg** - Beg for money.

# Item Shop
Items can be purchased from the item shop in order to gain an advantage or improve your odds in various economy games/activites. Currently all items are persistent and are not consumable. Items will also incur a daily cost which will remove the item if you run out of money to pay for them.
## Usage
There's several commands that are used to view, buy and sell items in Cakey Bot. You can see all of the commands below:
* **/eco shop** - Purchase items from the shop for bonuses. 
* **/eco iteminfo** - View information about a specific item.
* **/eco items** - View all of the items you or someone else owns.

## Available Items
TBD

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command                  | Description                                                     | Usage                                      | Permission             |
| :----------------------- | :------------------------------------------------------------- | :---------------------------------------- | :--------------------- |
| /eco balance             | Check your balance or the balance of another user.             | \<user>                                    | None                   |
| /eco beg                 | Beg for money.                                                 | N/A                                       | None                   |
| /eco coinflip            | Guess the result to win 50% of your bet.                       | \<guess> \<amount>                          | None                   |
| /eco guess               | Guess the number (1-10) for a chance to gain 2x-3x the amount. | \<guess> \<amount>                          | None                   |
| /eco high-or-low         | Guess higher or lower to win 50% of your bet.                  | \<amount>                                  | None                   |
| /eco iteminfo            | View information about a specific item.                        | \<item>                                    | None                   |
| /eco items               | View all of the items you or someone else owns.                | \<user>                                    | None                   |
| /eco leaderboard         | View the top 10 users on the leaderboard.                      | N/A                                       | None                   |
| /eco pay                 | Pay another user.                                              | \<user> \<amount>                           | None                   |
| /eco rob                 | Attempt to rob another user.                                   | \<user>                                    | None                   |
| /eco rock-paper-scissors | Challenge another user to Rock, Paper, Scissors.               | \<amount>                                  | None                   |
| /eco shop                | Purchase items from the shop for bonuses.                      | N/A                                       | None                   |
| /eco split-or-steal      | Challenge another user to split or steal.                      | N/A                                       | None                   |
| /eco work                | Work for money.                                                | N/A                                       | None                   |
| /ecoadmin manage-money   | Manage a user's economy balance.                               | \<give \| remove \| set> \<user> \<amount>     | ManageServer or Administrator |
| /ecoadmin reset-economy  | Reset the economy for this server. This will RESET ALL user balances! | \<confirm>                             | ManageServer or Administrator |
