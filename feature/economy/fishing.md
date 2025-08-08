---
title: Fishing Overview
description: 
published: 1
date: 2025-08-08T04:10:04.982Z
tags: 
editor: markdown
dateCreated: 2025-08-08T04:09:34.397Z
---

## Overview
The `/eco fishing` command lets users try their luck at catching fish and earning money in return. It's a simple yet fun minigame that adds variety to the economy system.

### How It Works
When a user runs `/eco fishing`, the system randomly determines the outcome:
 * Success: The user catches a fish and earns a reward based on that fish's rarity.
 * Failure: The user experiences a humorous or unfortunate fishing event (e.g., the line snaps or they reel in an old boot).

### Fish Rarity Table
There are 10 different types of fish to catch, each with its own rarity and reward range. The rarer the fish, the more valuable it is—but the harder it is to catch!

| Fish Name           | Rarity     | Chance % | Value Range     |
|---------------------|------------|----------|-----------------|
| Common Carp         | Common     | 25%      | 100–250         |
| Rusty Trout         | Common     | 20%      | 150–300         |
| Speckled Bass       | Uncommon   | 15%      | 300–500         |
| Bluegill Perch      | Uncommon   | 10%      | 400–650         |
| Electric Eel        | Rare       | 8%       | 700–1,000       |
| Golden Salmon       | Rare       | 6%       | 1,000–1,500     |
| Vampire Catfish     | Epic       | 4%       | 1,500–2,000     |
| Phantom Ray         | Epic       | 3%       | 2,000–3,000     |
| Crystal Koi         | Legendary  | 2.5%     | 3,000–4,000     |
| Mythic Leviathan    | Mythical   | 1.5%     | 5,000–10,000    |

## Minefield
When you run `/eco minefield`, a 4x4 grid of hidden tiles appears. Some of these tiles hide bombs, while the rest are safe. Your goal is to reveal as many safe tiles as possible to increase your reward — but beware: revealing a bomb ends the game and you lose everything!

Each time you click a tile:
* ✅ A safe tile increases your potential payout.
* 💣 A bomb ends the round with no reward.

You can choose to cash out at any time to lock in your earnings before hitting a bomb.

### Profit Table
| Tiles Revealed | Old Reward (×500) | New Incremental Reward |
| -------------- | ----------------- | ---------------------- |
| 1              | 500               | 500                    |
| 2              | 1,000             | 1,250                  |
| 3              | 1,500             | 2,250                  |
| 4              | 2,000             | 3,500                  |
| 5              | 2,500             | 5,000                  |
| 6              | 3,000             | 6,750                  |
| 7              | 3,500             | 8,750                  |
| 8              | 4,000             | 11,000                 |
| 9              | 4,500             | 13,500                 |
| 10             | 5,000             | 16,250                 |
| 11             | 5,500             | 19,250                 |
| 12             | 6,000             | 22,500                 |

> Note: Perfect games result in a double profit jackpot! ($45,000!)
{.is-info}