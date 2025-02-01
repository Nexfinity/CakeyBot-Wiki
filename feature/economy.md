---
title: Economy
description: 
published: 1
date: 2025-02-01T04:27:15.724Z
tags: 
editor: markdown
dateCreated: 2024-03-14T19:35:02.607Z
---

# Overview
The economy system offers a dynamic and customizable experience that fosters engagement and competition among server members. Users can earn currency through commands like `/eco beg`, `/eco work`, and mini-games such as `/eco coinflip`, `/eco high-or-low`, and `/eco guess`, while also competing for the top spot on the leaderboard with `/eco leaderboard`. 

They can spend or trade their wealth using `/eco shop`, `/eco pay`, and `/eco donate`, or take risks with commands like `/eco rob` and `/eco split-or-steal`. The system is highly configurable, allowing server owners to personalize settings such as the currency symbol and its position, number formatting, initial and max balances, the ability to transfer balances, and whether user balances are wiped when they leave the server. 

This combination of commands and customization options makes the economy system a versatile feature that adds excitement and interaction to any community.

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

# Customization
In addition to the regular commands, there's a number of customization options that you can configure on our dashboard. These options include:
## Currency Symbol & Position
Customize the currency symbol displayed in your server's economy commands. Choose a symbol (e.g., $, €, ¥, or even custom emojis) and define its position—either before ($100) or after (100$) the balance amount.

## Initial & Max Balance
Set the starting balance for new users and the maximum balance users can hold. The initial balance ensures every member has a fair start in the economy, while the maximum balance helps maintain balance and prevent inflation. Both values are fully adjustable to suit your server's economy goals.

> **Note:** If you use the `/ecoadmin reset-economy` command, all users will be reset to the current "Initial Balance" setting, not 0.
{.is-info}

## Number Separator Character
Control how large numbers are formatted by specifying a separator character (e.g., commas 1,000 or periods 1.000). This improves readability for balances in regions with different number formatting standards.

## Allow Balance Transfers
Enable or disable the ability for users to transfer money to one another. This setting can help regulate the economy by preventing abuse or fostering collaboration through shared wealth. Enabling this feature will disable commands and features that allow users to transfer money directly to each other such as `/rob`, `/pay`, and `/eco rock-paper-scissors`. *(This is not a fully inclusive list)*

## Wipe User Balance on Leave
Decide whether user balances should be wiped when they leave the server (or when kicked/banned). Enable this option to ensure the economy remains balanced by preventing users from returning with excessive wealth, or disable it to allow users to retain their progress if they rejoin later.

> **Note:** If users re-join the server later, their original balance will NOT be returned if this setting was enabled. They will retain the "Initial Balance".
{.is-info}

## Add Space to Currency Symbol
Enable this setting to add a space between the currency symbol and the balance amount, improving clarity and readability. For example, `$100` becomes `$ 100` or `100$` becomes `100 $`. This option works seamlessly with both currency symbol positions, whether the symbol is placed on the left or the right of the amount.

# Item Shop
The item shop allows server owners to create a customizable list of purchasable items for their members. These items can include role unlocks, which grant users specific roles upon purchase, and leveling XP to help them progress faster in the server's leveling system. Each item can have its own unique cost, making it easy to design a diverse economy tailored to your server's needs.

> Economy boosts marked as "purchasable" will also display in this shop list.
{.is-info}

## Usage
There's several commands that are used to view, buy and sell items in Cakey Bot. You can see all of the commands below:
* **/eco shop** - Purchase items from the shop for bonuses. 
* **/eco iteminfo** - View information about a specific item.
* **/eco items** - View all of the items you or someone else owns.

## Item Types
This is the list of support item types that you can configure for users to purchase:
* Leveling XP
* Role Unlocks
* Temporary Role Unlocks
* Economy Boosts (Created on separate "Boosts" page.)

## Configuration
* Cost
  * The cost for the user to purchase the item. Note: This only applies if `IsPurchasable` is enabled for the item.
* Type
  * The type of item for the user to unlock/buy.
* Data
  * The `Data` field is the amount of XP to give the user OR the ID of the role to grant. Depending on the "Type" selected.
* Secondary Data
  * The `Secondary Data` field is only used when "Temporary Role" type is selected. It is the _**number of hours**_ for the bot to grant the role to the user.
  
> **Note:** The _type_ of data placed into the `Data` and `Secondary Data` fields will change depending on the `Type` selected. Keep this in mind when creating and modifying items.
{.is-warning}

# Boosts
Boosts allow server owners to create multipliers that users can activate to enhance their earnings in the server's economy. Boosts can stack, meaning users can apply multiple boosts at once for greater rewards. These multipliers only apply to certain commands, such as games, and do not affect direct money modifications like `/pay` or `/donate`. In multiplayer scenarios, boosts are applied to the winnings received by the boosted player, but losses incurred by other players remain unaffected.

## Configuration
* Duration
  * This is how long the boost is active for once purchased. The time is based in hours.
* Multiplier
  * This is how much the boost affects earnings. Keep in mind that boosts can stack with other boosts.
* Cost
  * The cost for the user to purchase the boost. Note: This only applies if `IsPurchasable` is enabled for the boost.
* IsPurchasable
  * When this is enabled, it allows the boost to be purchased in the `/eco shop`. Otherwise users are unable to aquire the boost.

## Notes Regarding Functionality:
* Multiple boosts can be stacked/applied at once.
* Multipliers will only be applied to users who have active boosts (in regards to multi-player games).
* Commands that directly modify money such as `/pay`, `/donate` and `/ecoadmin manage-money` will **NOT** have boosts applied at all.
* When games take money from one player and give it to another, only the amount given to the winner will have boosts applied. The money _taken_ will **NOT** have a multiplier.
  * For example, assume player A has a 2x boost. If player A robs player B successfully, and the resulting amount is `$100`, then player A will receive `$200` (due to the boost), however, player B will only lose `$100` their loss will **NOT** be multiplied/boosted.
  * When this occurs, the success message will display/show the boosted amount, however, it will still only take the non-boosted amount from the loser.

> **Fun Fact:** Multiple boosts will automatically stack, allowing users to purchase multiple boosts and gain even more money!
{.is-success}

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
| /eco donate              | Donate to a randomly selected user.                            | \<amount>                                   | None                   |
| /eco rob                 | Attempt to rob another user.                                   | \<user>                                    | None                   |
| /eco rock-paper-scissors | Challenge another user to Rock, Paper, Scissors.               | \<amount>                                  | None                   |
| /eco shop                | Purchase items from the shop for bonuses.                      | N/A                                       | None                   |
| /eco split-or-steal      | Challenge another user to split or steal.                      | N/A                                       | None                   |
| /eco work                | Work for money.                                                | N/A                                       | None                   |
| /ecoadmin manage-money   | Manage a user's economy balance.                               | \<give \| remove \| set> \<user> \<amount>     | ManageServer or Administrator |
| /ecoadmin reset-economy  | Reset the economy for this server. This will RESET ALL user balances! | \<confirm>                             | ManageServer or Administrator |
