---
title: Item/Boost Shop
description: 
published: 1
date: 2025-08-08T04:13:34.650Z
tags: 
editor: markdown
dateCreated: 2025-08-08T04:12:25.252Z
---

# Item/Boost Shop
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
* **Leveling XP:** Grants a specified amount of XP in the Leveling System.
* **Role Unlocks:** Grants permanent access to specified Discord roles.
* **Temporary Role Unlocks:** Grants time-limited access to roles. (specified in hours)
* **Economy Boosts:** Enhances earning rates for specified periods. (Created on separate "Boosts" page.)

## Configuration
* **Cost:** The cost for the user to purchase the item. Note: This only applies if `IsPurchasable` is enabled for the item.
* **Type:** The type of item for the user to unlock/buy.
* **Data:** The `Data` field is the amount of XP to give the user OR the ID of the role to grant. Depending on the "Type" selected.
* **Secondary Data:** The `Secondary Data` field is only used when "Temporary Role" type is selected. It is the _**number of hours**_ for the bot to grant the role to the user.
  
> **Note:** The _type_ of data placed into the `Data` and `Secondary Data` fields will change depending on the `Type` selected. Keep this in mind when creating and modifying items.
{.is-warning}

# Boosts
Boosts allow server owners to create multipliers that users can activate to enhance their earnings in the server's economy. Boosts can stack, meaning users can apply multiple boosts at once for greater rewards. These multipliers only apply to certain commands, such as games, and do not affect direct money modifications like `/pay` or `/donate`. In multiplayer scenarios, boosts are applied to the winnings received by the boosted player, but losses incurred by other players remain unaffected.

## Configuration
* **Duration:** This is how long the boost is active for once purchased. The time is based in hours.
* **Multiplier:** This is how much the boost affects earnings. Keep in mind that boosts can stack with other boosts.
* **Cost:** The cost for the user to purchase the boost. Note: This only applies if `IsPurchasable` is enabled for the boost.
* **IsPurchasable:** When this is enabled, it allows the boost to be purchased in the `/eco shop`. Otherwise users are unable to aquire the boost.

## Notes Regarding Functionality:
* Multiple boosts can be stacked/applied at once.
* Multipliers will only be applied to users who have active boosts (in regards to multi-player games).
* Commands that directly modify money such as `/pay`, `/donate` and `/ecoadmin manage-money` will **NOT** have boosts applied at all.
* When games take money from one player and give it to another, only the amount given to the winner will have boosts applied. The money _taken_ will **NOT** have a multiplier.
  * For example, assume player A has a 2x boost. If player A robs player B successfully, and the resulting amount is `$100`, then player A will receive `$200` (due to the boost), however, player B will only lose `$100` their loss will **NOT** be multiplied/boosted.
  * When this occurs, the success message will display/show the boosted amount, however, it will still only take the non-boosted amount from the loser.

> **Fun Fact:** Multiple boosts will automatically stack, allowing users to purchase multiple boosts and gain even more money!
{.is-success}