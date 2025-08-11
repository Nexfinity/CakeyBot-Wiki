---
title: Economy Overview
description: 
published: 1
date: 2025-08-11T10:03:57.160Z
tags: 
editor: markdown
dateCreated: 2024-03-14T19:35:02.607Z
---

# Overview
The economy system offers a dynamic and customizable experience that fosters engagement and competition among server members. Users can earn currency through commands like `/eco beg`, `/eco work`, and mini-games such as `/eco coinflip`, `/eco high-or-low`, and `/eco guess`, while also competing for the top spot on the leaderboard with `/eco leaderboard`. 

They can spend or trade their wealth using `/eco shop`, `/eco pay`, and `/eco donate`, or take risks with commands like `/eco rob` and `/eco split-or-steal`. The system is highly configurable, allowing server owners to personalize settings such as the currency symbol and its position, number formatting, initial and max balances, the ability to transfer balances, and whether user balances are wiped when they leave the server. 

This combination of commands and customization options makes the economy system a versatile feature that adds excitement and interaction to any community.

## Popular Features
The Economy System offers multiple ways for users to interact with the virtual economy:

* **Currency Management:** Check balances, view leaderboards, and transfer funds
* **Earning Methods:** Work, beg, or rob other users for currency
* **Games & Gambling:** Play games of chance or challenge other users
* **Item Shop:** Purchase items that provide benefits or unlock roles
* **Boosts:** Apply multipliers to increase earnings
* **Customization:** Configure currency symbol, initial balances, and other server-specific settings

# Earn Money
## Solo Betting Games
There's several games that rely entirely on RNG/randomization to determine the outcome. These games tend to have the highest risk-to-reward ratio and are usually more profitable. They can also be played entirely solo so you don't have to wait on other users to play. These games include:
* **/eco coinflip** - Guess the result to win 50% of your bet.
  * There's a 0.02% chance for the coin to land on it's side. If this occurs, the player wins 2x their bety regardless of their guess.
* **/eco guess** - Guess the number (1-10) for a chance to gain 3x the amount.
  * You also get 2x if you are +/- 1 off from the correct answer instead of 3x.

## Player VS Player Games
There's also several games that allow you to directly challenge other users in the server. These tend to be a little less profitable than RNG games but can introduce a new level of competition and fun among the players. These games include:
* **/eco rock-paper-scissors** - Challenge another user to Rock, Paper, Scissors.
* **/eco split-or-steal** - Challenge another user to split or steal.

> The system includes safeguards against collusion in PvP games, such as prize modifiers based on player history in `/eco split-or-steal`.

## Other Earning Commands
Cakey Bot also includes several other ways to earn money that do not include any games, though some of them still include a certain level of RNG that can affect the profits. These commands include:
* **/eco work** - Work for money.
* **/eco rob** - Attempt to rob another user.
* **/eco beg** - Beg for money.

# Customization
In addition to the regular commands, there's a number of customization options that you can configure on our dashboard. These options include:

| Name                         | Description                                                                                                                                                                                                    | Default Value       | Min Value | Max Value | Premium Feature |
| :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------ | :-------- | :-------- | :--------------- |
| Currency Symbol             | Customize the currency symbol (e.g., $, €, ¥, or emojis).                                                                            | $          |           |           | No               |
| Currency Symbol Position    | Define the currency symbol's position before or after the balance (e.g., $100 or 100$).                                                                            | Before          |           |           | No               |
| Initial Balance             | The starting balance for new users. Also used during resets with `/ecoadmin reset-economy`.                                                                                                                        | 100                 | 0         | 1,000,000,000 | No               |
| Max Balance                 | The maximum balance users can hold to prevent inflation.                                                                                                                 | 1,000,000,000              | 0         | 1,000,000,000 | No               |
| Number Separator Character  | Defines how large numbers are formatted (e.g., comma `1,000` or period `1.000`).                                                                                                                               | Comma (`,`)         |           |           | No               |
| Allow Balance Transfers     | Enables or disables users sending money to one another. Disabling this restricts commands like `/pay`, `/rob`, etc.                                                                                           | Enabled             |           |           | No               |
| Wipe User Balance on Leave  | When enabled, wipes a user’s balance when they leave or are kicked/banned. They will only retain the "Initial Balance" if they rejoin.                                                                       | Disabled            |           |           | No               |
| Add Space to Currency Symbol| Adds a space between the currency symbol and the number for better readability (e.g., `$100` → `$ 100`).                                                                                                       | Disabled            |           |           | No               |
| Fishing Weight    | Define if the weight of caught fish should be kg or lbs.                                                                            | lbs          |           |           | No               |

# Anti-Abuse Mechanics
> Note: Details are intentionally limited for this in order to make it more difficult for malicious actors trying to abuse the economy system. Also not all anti-abuse mechanics may be listed.
{.is-info}

To help maintain balance and fairness in the economy, Cakey Bot includes several anti-abuse measures across money transfer actions including (but not limited to) `/rob` and `/pay`. These checks are designed to discourage spammy or predatory behavior and ensure a fun experience for everyone. These limits help prevent users from exploiting alts or friends to quickly boost their balance unfairly.

## All Economy Commands
All economy commands will have some sort of rate-limit for each command. These generic rate limits are always within a **randomized** time period (to help prevent botting/automatic abuse) and may be linked to a specific user or the entire server.

## Rob Command Protections
The `/rob` command also includes several layered checks:
* Robbing Limit – Prevents users from robbing too many people in a random time frame.
* Target Saturation – Protects users from being robbed excessively over a period of time.
* Pair Abuse Prevention – Detects frequent rob attempts between the same two users within a random amount of time.

## Pay Command Protections
The `/pay` command also has some additional checks to curb farming and funneling:
* Sender Limit – Users cannot send payments to others too frequently.
* Receiver Limit – Users cannot receive too many payments within a random period of time.

# Related Commands
Usage Key: `<required>` / `[optional]`

> Individual commands can be toggled on/off separately via the web dashboard.
{.is-info}

| Command                  | Description                                                     | Usage                                      | Permission             |
| :----------------------- | :------------------------------------------------------------- | :------------------------------------------ | :--------------------- |
| /eco balance             | Check your balance or the balance of another user.             | \<user>                                     | None                   |
| /eco beg                 | Beg for money.                                                 | N/A                                         | None                   |
| /eco coinflip            | Guess the result to win 50% of your bet.                       | \<guess> \<amount>                          | None                   |
| /eco guess               | Guess the number (1-10) for a chance to gain 2x-3x the amount. | \<guess> \<amount>                          | None                   |
| /eco high-or-low         | Guess higher or lower to win more money.                       | N/A                                         | None                   |
| /eco iteminfo            | View information about a specific item.                        | \<item>                                     | None                   |
| /eco items               | View all of the items you or someone else owns.                | \<user>                                     | None                   |
| /eco leaderboard         | View the top 10 users on the leaderboard.                      | N/A                                         | None                   |
| /eco pay                 | Pay another user.                                              | \<user> \<amount>                           | None                   |
| /eco donate              | Donate to a randomly selected user.                            | \<amount>                                   | None                   |
| /eco rob                 | Attempt to rob another user.                                   | \<user>                                     | None                   |
| /eco rock-paper-scissors | Challenge another user to Rock, Paper, Scissors.               | \<amount>                                   | None                   |
| /eco shop                | Purchase items from the shop for bonuses.                      | N/A                                         | None                   |
| /eco split-or-steal      | Challenge another user to split or steal.                      | N/A                                         | None                   |
| /eco work                | Work for money.                                                | N/A                                         | None                   |
| /eco fishing fish              | Fish in a specific biome for a chance to catch fish.            | `<biome> <rod> <bait>`      | None       |
| /eco fishing list-biomes       | List all available fishing biomes.                              | N/A                         | None       |
| /eco fishing list-rods         | List all available fishing rods.                                | N/A                         | None       |
| /eco fishing list-bait         | List all available fishing baits.                               | N/A                         | None       |
| /eco fishing inventory         | View your (or selected players) fishing inventory & stats.      | `[user]`                    | None       |
| /eco fishing leaderboard       | View the top 10 users on the fishing leaderboard.               | `<type>`                    | None       |
| /eco minefield           | Play a minefield game for a chance to earn money.              | N/A                                         | None                   |
| /ecoadmin manage-money   | Manage a user's economy balance.                               | \<give \| remove \| set> \<user> \<amount>     | ManageServer or Administrator |
| /ecoadmin reset-economy  | Reset the economy for this server. This will RESET ALL user balances! | \<confirm>                             | ManageServer or Administrator |
