---
title: Fishing
description: 
published: 1
date: 2025-08-14T11:45:36.593Z
tags: 
editor: markdown
dateCreated: 2025-08-08T04:09:34.397Z
---

# Overview
The `/eco fishing` command is your gateway into a fully overhauled fishing system where you can explore diverse biomes, catch fish of varying rarities, discover mythic treasures, and even reel in some unexpected trash loot.

Fishing is no longer just “cast and hope” — your success is influenced by biome difficulty, bait choice, and the rod you use. Every catch adds to your stats, which feed into the server's leaderboards.

Whether you’re chasing rare Mythic Fish, farming money in profitable waters, or just collecting everything the world’s oceans, rivers, and magical lakes have to offer, there’s always another fishing trip waiting.

# How It Works
When you run `/eco fishing fish`, the system follows a multi-step process to determine your results:

* 🎯 Biome Selection
  * You can choose a specific biome to fish in (each has its own difficulty, fish species, and loot pool).

* 🎣 Rod & Bait Effects
  * Your equipped rod impacts your chances of catching more fish.
  * Special bait can boost profits, increase rare fish odds, or even help you catch more trash for certain events.

* ⚖ Catch Determination
  * The game calculates your success based on biome difficulty, rarity chances, and bonuses from gear and bait.
  * Possible results:
    * Fish Catch — Earn money based on rarity and biome.
    * Trash Catch — Old boots, cans, and other oddities (counts toward trash stats).
    * Missed Catch — The fish got away, or something unexpected happened (also increments trash stats).

* 💰 Rewards
  * Fish value is randomized based on its rarity and biome.
  * All catches (fish or trash) are recorded in your fishing stats and contribute to leaderboards.
 
# Leaderboard Command
The `/eco fishing leaderboard <type>` command lets you view the top 10 players in various fishing-related categories.
It’s perfect for seeing who dominates the waters — whether they’re skilled anglers, treasure hunters, or just the most persistent trash collectors.

## Leaderboard Types
| Type                           | Description                                                                             |
| ------------------------------ | --------------------------------------------------------------------------------------- |
| **Total Fish Caught**          | Shows the top 10 players who have caught the highest total number of fish (any rarity). |
| **Total Trash Caught**         | Shows the top 10 players who have caught the most junk items while fishing.             |
| **Total Value of Fish**        | Ranks players by the total market value of all fish they’ve caught.                     |
| **Total Weight of Fish**       | Ranks players by the combined weight of all fish caught.                                |
| **Most Mythic Fish Caught**    | Players who have caught the highest number of *Mythic*-rarity fish.                     |
| **Most Legendary Fish Caught** | Players who have caught the highest number of *Legendary*-rarity fish.                  |
| **Most Epic Fish Caught**      | Players who have caught the highest number of *Epic*-rarity fish.                       |
| **Most Rare Fish Caught**      | Players who have caught the highest number of *Rare*-rarity fish.                       |
| **Most Uncommon Fish Caught**  | Players who have caught the highest number of *Uncommon*-rarity fish.                   |
| **Most Common Fish Caught**    | Players who have caught the highest number of *Common*-rarity fish.                     |

# Inventory & Stats Command
The `/eco fishing inventory [user]` command displays everything you own in the fishing system — including your bait supply, rods, and a full set of fishing statistics.
You can check your own inventory or look at another player’s stats if you have their username.

## Inventory Details
* 🎯 **Baits** - Shows how many of each special bait you currently own, along with your maximum carrying capacity for each type.
* 🎣 **Fishing Rods** - Lists which fishing rods you own.
* **Statistics** - Alongside your inventory, this command also provides detailed fishing stats including:
  * 📊 Catch Stats
    * Total Fish Caught (all rarities combined)
    * Total Trash Caught
    * Total Value of Fish (based on sell prices)
    * Breakdown by rarity:
      * Mythic, Legendary, Epic, Rare, Uncommon, Common

  * 🌎 Biome Stats
    * Total Biomes Fished In
    * Most Fished Biome
    * Least Fished Biome
    * Catch count per biome

  * ⚖ Weight Stats
    * Largest Fish (by weight)
    * Smallest Fish
    * Average Weight of Fish
    * Total Weight of All Fish Caught
    
> 💡 **Tip:** This command is a great way to track your progress toward leaderboard dominance or identify which biomes you should focus on next.
{.is-success}


# Fishing Rod List
| Rod Name          | Cost   | Fail Chance | Description                                            |
| ----------------- | ------ | ----------- | ------------------------------------------------------ |
| **Basic Rod**     | Free   | 30%         | Fishing rod with a 30% chance of failure when casting. |
| **Advanced Rod**  | 25,000 | 20%          | Fishing rod with a 20% chance of failure when casting.  |
| **Master Rod**    | 50,000 | 10%          | Fishing rod with a 10% chance of failure when casting.  |
| **Legendary Rod** | 100,000 | 2%          | Fishing rod with a 2% chance of failure when casting.  |

> **Note:** You must buy the previous rod before you can buy the next rod. For example, in order to buy the "Legendary Rod", you must first purchase the "Advanced Rod" THEN the "Master Rod" before you can purchase the "Legendary Rod".
{.is-info}

# Fishing Bait Types
| Bait Type | Name | Description | Cost | Max Inventory | Effect |
|-----------|------|-------------|------|---------------|--------|
| LegendaryBoost | Kraken's Charm | Greatly increases the chance (**3×**) of catching a legendary fish. **Consumed on legendary catch.** | 50,000 | 10 | `LegendaryChanceMultiplier ×= 3.0`<br>`ConsumeOnLegendary = true` |
| ExtraBaitChance | Wormhole Larvae | Increases chance of finding additional bait while fishing to **15%**. **Consumed on any bait find.** | 30,000 | 10 | `ExtraBaitChance += 0.15` |
| DoubleProfitNextCatch | Golden Minnow | Doubles the profit of the next fish caught. **Consumed on any fish catch.** | 25,000 | 10 | `ProfitMultiplier = 2.0`<br>`ConsumeOnCatch = true` |
| HigherTierChance | Titan Worm | Increases chance (**1.5×**) of catching a higher-tier fish. **Consumed on any fish catch.** | 15,000 | 10 | `HigherTierChanceMultiplier ×= 1.5`<br>`ConsumeOnCatch = true` |
| TrashMagnet | Rusted Can Lure | Increases chance (**+50%**) of catching trash instead of fish. **Consumed on trash catch.** | 5,000 | 10 | `FailChanceMultiplier ×= 1.5` |
| FishMagnet | Pearlscale Grub | Decreases chance (**−50%**) of catching trash, making fish more likely. **Consumed on fish catch.** | 5,000 | 10 | `FailChanceMultiplier ×= 0.5`<br>`ConsumeOnCatch = true` |

# 🎣 Fishing Biomes & Fish Guide

## How to Read the Tables
| Column               | Meaning                                                                      |
| -------------------- | ---------------------------------------------------------------------------- |
| **Fish**             | Name of the species found in this biome.                                     |
| **Rarity**           | How rare the fish is (Common → Mythic).                                      |
| **Value Range**      | The minimum and maximum sell price range for the fish.                       |
| **Catch %**          | Base probability of catching this fish, before biome difficulty adjustments. |
| **Weight (lbs)**     | The minimum and maximum possible weight range of the fish.                   |
| **Biome Difficulty** | Affects all fish in the biome. Higher = harder to catch fish.                |

## 🌿 Verdant Marsh
**Difficulty:** 0.6x
**Cost:** FREE (Unlocked by default)
**Min. Owned Biomes:** 0
| Fish             | Rarity   | Value Range | Catch % | Weight (lbs) |
| ---------------- | -------- | ----------- | ------- | ------------ |
| Glimmerfin Tetra | Common   | 110–230     | 95%     | 0.3–0.7      |
| Mossback Loach   | Common   | 130–260     | 92%     | 0.5–1.0      |
| Speckled Frogeel | Uncommon | 330–520     | 70%     | 1.0–2.0      |
| Swampjaw Gar     | Uncommon | 410–600     | 65%     | 2.0–3.5      |
| Bramble Pike     | Rare     | 800–1,200   | 38%     | 4.0–6.5      |
| Thornscale Eel   | Epic     | 1,700–2,400 | 18%     | 5.5–8.0      |

## ❄ Frostpeak Lake
**Difficulty:** 1.3x
**Cost:** 88,000
**Min. Owned Biomes:** 0
| Fish             | Rarity    | Value Range | Catch % | Weight (lbs) |
| ---------------- | --------- | ----------- | ------- | ------------ |
| Icewhisk Minnow  | Common    | 120–270     | 93%     | 0.4–0.8      |
| Glacier Carp     | Uncommon  | 340–580     | 72%     | 2.5–4.5      |
| Frostscale Perch | Uncommon  | 390–610     | 70%     | 1.5–3.0      |
| Shiverfin        | Rare      | 720–1,400   | 40%     | 5.0–8.0      |
| Snowblade Trout  | Epic      | 1,800–2,700 | 20%     | 7.0–12.0     |
| Cryo Leviathan   | Legendary | 3,400–4,000 | 6%      | 15.0–25.0    |

## 🔥 Emberdeep Caverns
**Difficulty:** 1.4x
**Cost:** 94,000
**Min. Owned Biomes:** 0
| Fish                | Rarity    | Value Range | Catch % | Weight (lbs) |
| ------------------- | --------- | ----------- | ------- | ------------ |
| Ember Guppy         | Common    | 100–210     | 91%     | 0.3–0.7      |
| Sootscale Fishlet   | Common    | 150–280     | 88%     | 0.4–0.9      |
| Magma Ray           | Uncommon  | 360–630     | 73%     | 3.0–5.0      |
| Cinderspine Snapper | Rare      | 900–1,400   | 37%     | 5.0–7.0      |
| Flamegill Serpent   | Epic      | 2,000–2,900 | 20%     | 6.0–9.0      |
| Ashdrake            | Legendary | 3,300–3,900 | 5%      | 10.0–18.0    |

## 🪸 Coral Archipelago
**Difficulty:** 2.0x
**Cost:** 188,000
**Min. Owned Biomes:** 3
| Fish                  | Rarity   | Value Range | Catch % | Weight (lbs) |
| --------------------- | -------- | ----------- | ------- | ------------ |
| Dazzlefin             | Common   | 120–250     | 94%     | 0.3–0.8      |
| Reefbloom Tang        | Common   | 140–270     | 91%     | 0.5–1.2      |
| Starstriped Clownfish | Uncommon | 400–630     | 70%     | 1.2–2.5      |
| Coralback Flounder    | Uncommon | 390–610     | 68%     | 1.8–3.0      |
| Sunscale Surgeon      | Rare     | 1,000–1,500 | 38%     | 3.5–5.5      |
| Prismtail Marlin      | Epic     | 2,100–2,900 | 18%     | 10.0–16.0    |
| Tidewyrm              | Mythic   | 6,200–9,800 | 2%      | 20.0–35.0    |

## 🌌 Twilight Forest Streams
**Difficulty:** 0.7x
**Cost:** FREE (Unlocked by default)
**Min. Owned Biomes:** 0
| Fish                    | Rarity    | Value Range | Catch % | Weight (lbs) |
| ----------------------- | --------- | ----------- | ------- | ------------ |
| Shadow Minnow           | Common    | 100–230     | 87%     | 0.2–0.5      |
| Glowtail Darter         | Common    | 160–280     | 71%     | 0.3–0.7      |
| Duskfin Trout           | Uncommon  | 300–520     | 60%     | 1.0–2.0      |
| Barkscale Bass          | Uncommon  | 410–650     | 58%     | 2.5–4.0      |
| Hollow Pike             | Rare      | 800–1,300   | 36%     | 4.5–7.0      |
| Sylvan Eel              | Epic      | 1,800–2,800 | 18%     | 6.0–9.0      |
| Spiritfish of the Grove | Legendary | 3,400–4,000 | 5%      | 9.0–14.0     |

## 🏜 Sunscorch Dunes
**Difficulty:** 1.1x
**Cost:** 70,000
**Min. Owned Biomes:** 0
| Fish            | Rarity    | Value Range | Catch % | Weight (lbs) |
| --------------- | --------- | ----------- | ------- | ------------ |
| Mirage Minnow   | Common    | 110–250     | 84%     | 0.2–0.6      |
| Sandstream Carp | Common    | 150–270     | 69%     | 0.5–1.0      |
| Dune Stinger    | Uncommon  | 370–610     | 65%     | 2.0–3.5      |
| Dustfin Catfish | Rare      | 900–1,300   | 35%     | 4.5–7.0      |
| Blisterjaw      | Epic      | 1,600–2,500 | 20%     | 6.0–10.0     |
| Djinnscale      | Legendary | 3,200–3,950 | 6%      | 10.0–18.0    |

## 🌊 Abyssal Trench
**Difficulty:** 3.0x
**Cost:** 327,000
**Min. Owned Biomes:** 5
| Fish             | Rarity   | Value Range | Catch % | Weight (lbs) |
| ---------------- | -------- | ----------- | ------- | ------------ |
| Gloomfang        | Uncommon | 380–600     | 75%     | 2.5–4.0      |
| Abyssangler      | Uncommon | 400–650     | 70%     | 3.0–5.0      |
| Lantern Maw      | Rare     | 850–1,450   | 40%     | 4.0–7.0      |
| Voidscale        | Rare     | 750–1,200   | 38%     | 3.5–6.0      |
| Abyssborn Eel    | Epic     | 1,700–2,700 | 20%     | 7.0–12.0     |
| Leviathan Wraith | Mythic   | 6,000–9,500 | 2%      | 25.0–40.0    |

## 💎 Crystal Caverns
**Difficulty:** 1.2x
**Cost:** 83,000
**Min. Owned Biomes:** 0
| Fish          | Rarity    | Value Range | Catch % | Weight (lbs) |
| ------------- | --------- | ----------- | ------- | ------------ |
| Gleamfish     | Common    | 140–260     | 88%     | 0.5–1.0      |
| Crystalfin    | Uncommon  | 330–580     | 70%     | 1.5–3.0      |
| Gemscale Pike | Uncommon  | 350–600     | 65%     | 2.0–4.0      |
| Echofish      | Rare      | 1,000–1,400 | 38%     | 4.0–6.5      |
| Quartzjaw     | Epic      | 1,800–2,700 | 20%     | 6.0–10.0     |
| Opal Serpent  | Legendary | 3,400–4,000 | 5%      | 10.0–15.0    |

## 🌩 Stormbreaker Coast
**Difficulty:** 2.5x
**Cost:** 269,000
**Min. Owned Biomes:** 4
| Fish                 | Rarity   | Value Range  | Catch % | Weight (lbs) |
| -------------------- | -------- | ------------ | ------- | ------------ |
| Tempest Darter       | Common   | 110–240      | 97%     | 0.4–0.9      |
| Thunderfin           | Uncommon | 360–600      | 73%     | 2.0–4.0      |
| Rainscale Mackerel   | Uncommon | 400–650      | 70%     | 2.5–4.5      |
| Bolt Pike            | Rare     | 800–1,300    | 38%     | 4.5–7.5      |
| Stormspine Barracuda | Epic     | 2,000–2,900  | 18%     | 8.0–13.0     |
| Skyshatter Leviathan | Mythic   | 6,500–10,000 | 2%      | 30.0–50.0    |

## ☠ Cursed Bog
**Difficulty:** 2.2x
**Cost:** 223,000
**Min. Owned Biomes:** 4
| Fish       | Rarity   | Value Range | Catch % | Weight (lbs) |
| ---------- | -------- | ----------- | ------- | ------------ |
| Bogskipper | Common   | 120–240     | 90%     | 0.3–0.8      |
| Witchfin   | Uncommon | 360–630     | 70%     | 2.0–3.5      |
| Leechgill  | Uncommon | 400–650     | 65%     | 2.5–4.0      |
| Bonejaw    | Rare     | 900–1,400   | 38%     | 4.5–7.5      |
| Soulcarp   | Epic     | 1,800–2,800 | 20%     | 6.5–10.0     |
| Wraithfin  | Mythic   | 5,800–9,200 | 2%      | 22.0–35.0    |

## 🏔 Crystalglass Highlands
**Difficulty:** 1.3x
**Cost:** 91,000
**Min. Owned Biomes:** 0
| Fish                 | Rarity    | Value Range | Catch % | Weight (lbs) |
| -------------------- | --------- | ----------- | ------- | ------------ |
| Silverstream Koi     | Common    | 150–270     | 89%     | 0.4–1.0      |
| Mistfin              | Uncommon  | 360–580     | 73%     | 2.0–3.5      |
| Highland Shimmerfish | Uncommon  | 420–650     | 68%     | 3.0–5.0      |
| Echo Trout           | Rare      | 850–1,400   | 38%     | 4.0–6.5      |
| Glassscale           | Epic      | 1,900–2,900 | 20%     | 7.0–11.0     |
| Celestine Ray        | Legendary | 3,400–4,000 | 5%      | 12.0–18.0    |

## ✨ Faelight Glade
**Difficulty:** 1.1x
**Cost:** 77,000
**Min. Owned Biomes:** 3
| Fish          | Rarity    | Value Range | Catch % | Weight (lbs) |
| ------------- | --------- | ----------- | ------- | ------------ |
| Petalfin      | Common    | 120–260     | 86%     | 0.3–0.7      |
| Sparkletail   | Uncommon  | 340–580     | 73%     | 1.8–3.2      |
| Faegill       | Uncommon  | 370–600     | 70%     | 2.0–3.8      |
| Gleamfin Wisp | Rare      | 900–1,350   | 36%     | 4.0–6.0      |
| Sylphfish     | Epic      | 2,000–2,800 | 20%     | 7.0–10.0     |
| Arcana Eel    | Legendary | 3,400–4,000 | 6%      | 11.0–16.0    |

# Related Commands  
Usage Key: `<required>` / `[optional]`  

> Fishing commands can be toggled on/off via the web dashboard.  
{.is-info}  

| Command                       | Description                                                     | Usage                      | Permission |
| :---------------------------- | :-------------------------------------------------------------- | :------------------------- | :--------- |
| /eco fishing fish              | Fish in a specific biome for a chance to catch fish.            | `<biome> <rod> <bait>`      | None       |
| /eco fishing list-biomes       | List all available fishing biomes.                              | N/A                         | None       |
| /eco fishing list-rods         | List all available fishing rods.                                | N/A                         | None       |
| /eco fishing list-bait         | List all available fishing baits.                               | N/A                         | None       |
| /eco fishing inventory         | View your (or selected players) fishing inventory & stats.      | `[user]`                    | None       |
| /eco fishing leaderboard       | View the top 10 users on the fishing leaderboard.               | `<type>`                    | None       |