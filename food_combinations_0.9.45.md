# He is Coming — food combinations / Cauldron recipes

This is the active 0.9.45-era Cauldron grid decoded from the installed Unity assets. Combine any two **different** ingredients below; order does not matter. There are 12 ingredients and 66 unique pairs.

## Combination matrix

Each intersecting cell is the resulting item. The full base stats and effect for every result follow the matrix.

| Ingredient | Redwood Roast | Spiny Chestnut | Cherry Bomb | Stone Steak | Vampiric Wine | Silverscale Fish | Clearspring Watermelon | Poisonous Mushroom | Sour Lemon | Grilling Skewer | Honeycomb | Seasonal Pumpkin |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **Redwood Roast** | — | Roasted Chestnut | Explosive Roast | Rock Roast | Blood Sausage | Shark Roast | Boiled Ham | Moldy Meat | Lemon Roast | Ham Bat | Honey Ham | Roasted Pumpkin |
| **Spiny Chestnut** | Roasted Chestnut | — | Trail Mix | Petrified Chestnut | Spiked Wine | Spiny Fish | Melon Seeds | Poisonous Durian | Spiny Kiwifruit | Blackbriar Bow | Candied Nuts | Prickly Pumpkin |
| **Cherry Bomb** | Explosive Roast | Trail Mix | — | Cherry Steak | Cherry Cocktail | Explosive Fish | Melon Bomb | Twin Mushroom | Combustible Lemon | Cherrytree Branch | Sugar Bomb | Explosive Pumpkin |
| **Stone Steak** | Rock Roast | Petrified Chestnut | Cherry Steak | — | Bloody Steak | Marbled Stonefish | Mineral Water | Marble Mushroom | Limestone Fruit | Rocksalt Sword | Rock Candy | Petrified Pumpkin |
| **Vampiric Wine** | Blood Sausage | Spiked Wine | Cherry Cocktail | Bloody Steak | — | Crimson Fish | Melon Sangria | Mushroom Soup | Blood Orange | Broken Winebottle | Honey Mead | Bloodwine Gourd |
| **Silverscale Fish** | Shark Roast | Spiny Fish | Explosive Fish | Marbled Stonefish | Crimson Fish | — | Silverscale Melon | Poisonous Pufferfish | Lemon Shark | Silverscale Swordfish | Honey Caviar | Buoyant Pumpkin |
| **Clearspring Watermelon** | Boiled Ham | Melon Seeds | Melon Bomb | Mineral Water | Melon Sangria | Silverscale Melon | — | Bitter Melon | Melon Lemonade | Melonvine Whip | Honeydew Melon | Swan Gourd |
| **Poisonous Mushroom** | Moldy Meat | Poisonous Durian | Twin Mushroom | Marble Mushroom | Mushroom Soup | Poisonous Pufferfish | Bitter Melon | — | Poisonous Lemon | Deathcap Bow | Honey-glazed Shroom | Poisonous Pumpkin |
| **Sour Lemon** | Lemon Roast | Spiny Kiwifruit | Combustible Lemon | Limestone Fruit | Blood Orange | Lemon Shark | Melon Lemonade | Poisonous Lemon | — | Lemontree Branch | Lemon Syrup | Pickled Pumpkin |
| **Grilling Skewer** | Ham Bat | Blackbriar Bow | Cherrytree Branch | Rocksalt Sword | Broken Winebottle | Silverscale Swordfish | Melonvine Whip | Deathcap Bow | Lemontree Branch | — | Bee Stinger | Pumpkin Lance |
| **Honeycomb** | Honey Ham | Candied Nuts | Sugar Bomb | Rock Candy | Honey Mead | Honey Caviar | Honeydew Melon | Honey-glazed Shroom | Lemon Syrup | Bee Stinger | — | Pumpkin Pie |
| **Seasonal Pumpkin** | Roasted Pumpkin | Prickly Pumpkin | Explosive Pumpkin | Petrified Pumpkin | Bloodwine Gourd | Buoyant Pumpkin | Swan Gourd | Poisonous Pumpkin | Pickled Pumpkin | Pumpkin Lance | Pumpkin Pie | — |

## Result properties

Stat order was decoded using the IL2CPP `EffectBase` layout: max health, attack, armor, speed.

| Result | Ingredient 1 | Ingredient 2 | Base stats | Effect |
|---|---|---|---|---|
| **Bee Stinger** | Grilling Skewer | Honeycomb | +3 attack | First Turn: Give the enemy 4 poison, 3 acid and 2 stun on hit |
| **Bitter Melon** | Clearspring Watermelon | Poisonous Mushroom | +2 attack | Turn Start: Spend 1 of another random status effect to gain 1 poison |
| **Blackbriar Bow** | Spiny Chestnut | Grilling Skewer | +3 attack | Can't strike. Turn Start: Gain thorns equal to your attack |
| **Blood Orange** | Vampiric Wine | Sour Lemon | +3 speed | Battle Start: Gain 1 acid. Wounded: Restore 4 health for each acid you have |
| **Blood Sausage** | Redwood Roast | Vampiric Wine | +5 max health | Wounded: Restore 1 health 5 times |
| **Bloodwine Gourd** | Vampiric Wine | Seasonal Pumpkin | — | Wounded: Steal 50% of the enemy's current health |
| **Bloody Steak** | Stone Steak | Vampiric Wine | — | Wounded: Restore 10 health and gain 10 armor |
| **Boiled Ham** | Redwood Roast | Clearspring Watermelon | +5 max health | Battle Start, Exposed & Wounded: Decrease a random status effect by 2 |
| **Broken Winebottle** | Vampiric Wine | Grilling Skewer | +2 attack | Wounded: Restore 4 health and gain 4 additional strikes |
| **Buoyant Pumpkin** | Silverscale Fish | Seasonal Pumpkin | — | Exposed: Steal 2 attack from the enemy and give them 2 riptide |
| **Candied Nuts** | Spiny Chestnut | Honeycomb | — | Your thorns deal double damage |
| **Cherry Cocktail** | Cherry Bomb | Vampiric Wine | — | Battle Start & Wounded: Deal 3 damage and restore 3 health |
| **Cherry Steak** | Cherry Bomb | Stone Steak | — | Battle Start: If your health is full, deal 1 damage 5 times. Otherwise gain 10 armor instead |
| **Cherrytree Branch** | Cherry Bomb | Grilling Skewer | 0 attack | Can't strike. Turn Start: Deal 1 damage 1 time. Increase the number of times this triggers by 1 each turn |
| **Combustible Lemon** | Cherry Bomb | Sour Lemon | +3 speed | Battle Start: Gain 1 acid. At the start of your third turn, deal damage equal to your acid |
| **Crimson Fish** | Vampiric Wine | Silverscale Fish | — | Wounded: Give the enemy 2 riptide. Whenever riptide triggers, restore 3 health |
| **Deathcap Bow** | Poisonous Mushroom | Grilling Skewer | +5 attack | Battle Start: Gain 3 poison. Turn Start: If you have poison, gain 1 additional strike |
| **Explosive Fish** | Cherry Bomb | Silverscale Fish | — | Battle Start: Give the enemy 1 riptide. Whenever riptide triggers, deal 1 damage |
| **Explosive Pumpkin** | Cherry Bomb | Seasonal Pumpkin | — | Battle Start: Deal 1 damage 2 times and steal that much attack |
| **Explosive Roast** | Redwood Roast | Cherry Bomb | +5 max health | Battle Start: Deal 1 damage 3 times |
| **Ham Bat** | Redwood Roast | Grilling Skewer | +5 max health, +4 attack | Battle Start: Gain 2 additional strikes |
| **Honey Caviar** | Silverscale Fish | Honeycomb | — | Exposed: Give the enemy 10 riptide |
| **Honey Ham** | Redwood Roast | Honeycomb | — | Double your max health |
| **Honey Mead** | Vampiric Wine | Honeycomb | — | Wounded: Restore health to full and restore 1 health at Turn Start for the rest of the battle |
| **Honey-glazed Shroom** | Poisonous Mushroom | Honeycomb | +4 attack | Turn Start: Give the enemy 2 poison |
| **Honeydew Melon** | Clearspring Watermelon | Honeycomb | — | Battle Start: Give all your status effects to the enemy |
| **Lemon Roast** | Redwood Roast | Sour Lemon | +5 max health, +5 speed | Battle Start: Gain 2 acid |
| **Lemon Shark** | Silverscale Fish | Sour Lemon | +3 speed | Battle Start: Gain 1 acid. Exposed: Give the enemy riptide equal to your acid |
| **Lemon Syrup** | Sour Lemon | Honeycomb | +3 speed | Battle Start: Double your speed |
| **Lemontree Branch** | Sour Lemon | Grilling Skewer | +2 attack, +3 speed | On Hit: Spend 2 speed and gain 1 additional strike on your next turn |
| **Limestone Fruit** | Stone Steak | Sour Lemon | +3 speed | Battle Start: Gain 1 acid and 8 armor. If your health is full, gain 2 acid and 16 armor instead |
| **Marble Mushroom** | Stone Steak | Poisonous Mushroom | +4 attack | Turn Start: Gain 2 poison and 3 armor |
| **Marbled Stonefish** | Stone Steak | Silverscale Fish | — | Exposed: Give the enemy 2 riptide and gain 3 armor for each riptide the enemy has |
| **Melon Bomb** | Cherry Bomb | Clearspring Watermelon | — | Battle Start: Deal 1 damage 2 times. Whenever you deal 1 damage, decrease a random status effect by 1 |
| **Melon Lemonade** | Clearspring Watermelon | Sour Lemon | +3 speed | Battle Start, Exposed & Wounded: Remove all your acid |
| **Melon Sangria** | Vampiric Wine | Clearspring Watermelon | — | Battle Start: Decrease a random status effect by 1. Whenever a status effect is decreased, restore 1 health |
| **Melon Seeds** | Spiny Chestnut | Clearspring Watermelon | — | Battle Start, Exposed & Wounded: Decrease a random status effect by 1 and gain 3 thorns |
| **Melonvine Whip** | Clearspring Watermelon | Grilling Skewer | +2 attack | Battle Start: Gain 1 additional strike. On Hit: Decrease a random status effect by 1 |
| **Mineral Water** | Stone Steak | Clearspring Watermelon | — | Battle Start: Decrease all your status effects by 1 and gain 5 armor for each removed status effect |
| **Moldy Meat** | Redwood Roast | Poisonous Mushroom | -5 max health, +5 attack | — |
| **Mushroom Soup** | Vampiric Wine | Poisonous Mushroom | +2 attack | Turn Start: Gain 2 poison and restore 5 health |
| **Petrified Chestnut** | Spiny Chestnut | Stone Steak | — | Battle Start: If your health is full, gain 10 thorns and 10 armor |
| **Petrified Pumpkin** | Stone Steak | Seasonal Pumpkin | — | Battle Start: If your health is full, steal all of the enemy's armor |
| **Pickled Pumpkin** | Sour Lemon | Seasonal Pumpkin | +3 speed | Battle Start: Steal 2 attack from the enemy and gain 2 acid |
| **Poisonous Durian** | Spiny Chestnut | Poisonous Mushroom | +2 attack | Battle Start: Gain 2 poison. Whenever you take damage from poison, gain 3 thorns |
| **Poisonous Lemon** | Poisonous Mushroom | Sour Lemon | +3 attack, +4 speed | Battle Start: Gain 1 acid and 5 poison |
| **Poisonous Pufferfish** | Silverscale Fish | Poisonous Mushroom | +2 attack | Battle Start: Gain 3 poison, then give the enemy riptide equal to your poison |
| **Poisonous Pumpkin** | Poisonous Mushroom | Seasonal Pumpkin | +2 attack | Battle Start: Gain 3 poison. Whenever you take damage from poison, steal 1 attack from the enemy |
| **Prickly Pumpkin** | Spiny Chestnut | Seasonal Pumpkin | — | Battle Start: Gain 5 thorns. Whenever the enemy loses armor to thorns, gain that much armor |
| **Pumpkin Lance** | Grilling Skewer | Seasonal Pumpkin | +3 attack | Every 3 strikes, steal 1 attack from the enemy |
| **Pumpkin Pie** | Honeycomb | Seasonal Pumpkin | — | Battle Start: Steal all attack from the enemy |
| **Roasted Chestnut** | Redwood Roast | Spiny Chestnut | +5 max health | Battle Start: Gain 5 thorns |
| **Roasted Pumpkin** | Redwood Roast | Seasonal Pumpkin | +5 max health | Battle Start: Steal 2 attack from the enemy |
| **Rock Candy** | Stone Steak | Honeycomb | — | Battle Start: Gain 20 armor. If your health is full, gain 50 armor instead |
| **Rock Roast** | Redwood Roast | Stone Steak | +5 max health, +5 armor | — |
| **Rocksalt Sword** | Stone Steak | Grilling Skewer | +3 attack | On Hit: If your health is full, gain 3 armor |
| **Shark Roast** | Redwood Roast | Silverscale Fish | +5 max health | Exposed: Give the enemy 2 riptide |
| **Silverscale Melon** | Silverscale Fish | Clearspring Watermelon | — | Battle Start, Exposed & Wounded: Decrease a random status effect by 1, if you do, give the enemy 2 riptide |
| **Silverscale Swordfish** | Silverscale Fish | Grilling Skewer | +3 attack | Battle Start: Gain 1 additional strike. First Turn: Give the enemy 1 riptide on hit |
| **Spiked Wine** | Spiny Chestnut | Vampiric Wine | — | Wounded: Restore 5 health and gain 5 thorns |
| **Spiny Fish** | Spiny Chestnut | Silverscale Fish | — | Battle Start: Give the enemy 1 riptide. Whenever riptide triggers, gain 3 thorns |
| **Spiny Kiwifruit** | Spiny Chestnut | Sour Lemon | +3 speed | Battle Start: Gain 2 acid and gain thorns equal to acid |
| **Sugar Bomb** | Cherry Bomb | Honeycomb | — | Turn Start: Deal 1 damage 3 times |
| **Swan Gourd** | Clearspring Watermelon | Seasonal Pumpkin | — | Battle Start, Exposed & Wounded: Decrease a random status effect by 1 and steal 1 attack from the enemy |
| **Trail Mix** | Spiny Chestnut | Cherry Bomb | — | Battle Start: Deal 1 damage 3 times and gain 1 thorn 3 times |
| **Twin Mushroom** | Cherry Bomb | Poisonous Mushroom | +2 attack | Battle Start: Deal 1 damage 2 times. Whenever a bomb deals non-strike damage, give the enemy 1 poison |

## Data notes

- Base stats and effect text above come from each result's serialized `EffectBase` record in `He is coming_Data/sharedassets0.assets`.
- Recipe pairing was checked against the current working Cauldron grid. Serialized removed/unreleased recipes are not included.
- All 66 unordered pairs are present exactly once. The symmetric matrix repeats them on both sides of the diagonal for lookup convenience.
- Current reference: https://wiki.hoodedhorse.com/He_is_Coming/Cauldron
- Current grid: https://wiki.hoodedhorse.com/He_is_Coming/Cauldron/CombinationsOverview
