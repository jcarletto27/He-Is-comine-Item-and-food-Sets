# He is Coming — active itemsets in the installed build

This catalog covers the current playable itemsets represented by the installed Patch 16 / 0.9.45-era data. There are **31 unique active itemsets**:

- 13 Woodland sets
- 16 Swampland rows, one of which is the shared **Highborn** set
- 3 Kingmaker-only cross-region sets

So the area lists contain 32 rows in total, but only 31 unique definitions because `set_24` (Highborn) appears in both Woodland and Swampland.

## How the data was identified

- `He is coming_Data/resources.assets` contains English localization keys such as `set_38_name` / `set_38_desc`, the set display names, component hints, and descriptions.
- `He is coming_Data/sharedassets0.assets` contains the serialized set objects. These expose the internal set ID, name, effect text, base-stat fields, and component references.
- `He is coming_Data/il2cpp_data/Metadata/global-metadata.dat` confirms the item/set systems and the gameplay terminology used by the IL2CPP build (`GetMatchingSets`, `GetSetPool`, `GetAllWorkingSetCopies`, and `ITEMSET`). Its `EffectBase` field order (`maxHealth`, `attack`, `armor`, `speed`) was used to decode stat-only set bonuses correctly.
- The official wiki's current area lists were used to distinguish playable sets from removed definitions and other objects that also use a `set_*` ID (notably weapon modifications and unreleased content).

## Woodland

| ID | Itemset | Required items | Function |
|---:|---|---|---|
| `set_38` | Bloodmoon Strike | Bloodmoon Dagger **or** Liferoot Dagger + Swiftstrike Gauntlet | **Wounded:** On your next turn, restore health equal to the damage dealt by your strikes. |
| `set_13` | Briar Greaves | Assault Greaves + Jagged Edge | Whenever you lose armor, gain 1 thorn. |
| `set_9` | Brittlebark Blessing | Brittlebark Buckler + Brittlebark Armor | Brittlebark items' printed effects are disabled; their base stats remain. This primarily removes their drawbacks. |
| `set_23` | Elderwood Mask | Elderwood Staff + Elderwood Necklace | **Battle Start:** Double base attack, base armor, and base speed. |
| `set_3` | Hero's Return | Sword of the Hero **or** Spear of the Hero + Shield of the Hero + Boots of the Hero | Adds **2 attack, 2 armor, and 2 speed** as base stats. |
| `set_24` | Highborn | Any 3 Ring-tagged items | Ring items trigger 1 additional time (normally twice total). |
| `set_123` | Ironbark Crest | Ore Heart + Oak Heart | Every Wood item also counts as Stone, and every Stone item also counts as Wood. |
| `set_16` | Ironbark Shield | Stone Steak + Pinecone Breastplate | **Battle Start:** If health is full, gain 1 armor at each **Turn Start** for the rest of that battle. |
| `set_1` | Lifeblood Transfusion | Lifeblood Armor + Iron Transfusion | Restore 10 health after every battle. |
| `set_11` | Raw Hide | Leather Glove + Leather Vest + Leather Boots | Gain 1 attack every other turn. |
| `set_14` | Redwood Crown | Redwood Rod + Redwood Helmet + Redwood Cloak | **Wounded:** Restore health to full. |
| `set_37` | Saffron Talon | Featherweight Blade + Saffron Feather | **On Hit:** Gain 1 speed. |
| `set_25` | Steelplated Thorns | Spearshield Lance + Bramble Buckler | **Turn Start:** If you have fewer than 10 thorns, double your thorns. |

## Swampland

| ID | Itemset | Required items | Function |
|---:|---|---|---|
| `set_86` | Agaric Armor | Fungal Rapier + Mushroom Buckler | **Turn Start:** Gain 1 poison; your poison is capped at 1. |
| `set_6` | Basilisk's Gaze | Basilisk Fang + Basilisk Scale | **Battle Start:** Give the enemy 2 stun. |
| `set_60` | Bloodstone Pendant | Bloodlord's Axe **or** Bloodlord's Whip + Bloodstone Ring | Whenever one healing instance restores at least 5 health, gain 2 attack. |
| `set_45` | Champion's Greaves | Champion's Blade + Champion's Armor | Adds **6 speed** as a base stat. |
| `set_42` | Deadly Toxin | Nerve Poison + Viper Extract | The first time the enemy gains poison, give it 5 acid. |
| `set_122` | Golden Jigsaw | Liferoot Banjo + Small Kazoo | Adds **20 max health** as a base stat. |
| `set_24` | Highborn | Any 3 Ring-tagged items | Ring items trigger 1 additional time (normally twice total). This is the same shared definition as Woodland Highborn. |
| `set_31` | Holy Crucifix | Holy Tome + Holy Shield | Negates negative base stats. |
| `set_41` | Ironstone Crest | Forge Hammer + Forge Gauntlet | **Turn Start:** Steal 2 armor from the enemy. |
| `set_53` | Ironstone Fang | Crimson Fang + Venomous Fang | **First Turn:** Gain 3 armor on hit. |
| `set_57` | Liquid Metal | Rusty Sword + Rusted Plate | **Battle Start:** Give the enemy 20 armor. This is primarily setup for effects that exploit or remove enemy armor. |
| `set_34` | Marble Anvil | Marble Sword + Serpent Lyre | Trigger **Exposed** at Battle Start instead of waiting to lose all armor. |
| `set_46` | Marshlight Aria | Marshlight Lantern + Riverflow Violin | **Exposed:** Trigger Symphony 3 times. |
| `set_48` | Seafood Hotpot | Silverscale Fish + Clearspring Watermelon + Sour Lemon | **Battle Start:** Gain 2 armor for each point of speed. |
| `set_44` | Twilight Crest | Sunlight Crest + Moonlight Crest | All Crest-tagged items trigger twice. |
| `set_47` | Weaver Medallion | Weaver Armor + Weaver Shield | Adds **5 max health** as a base stat. |

## Kingmaker-only cross-region sets

These combine one Woodland-side component with one Swampland-side component, so the matching bundles must be selected in Kingmaker.

| ID | Itemset | Required items | Function |
|---:|---|---|---|
| `set_51` | Iron Chain | Chainmail Sword + Chainmail Armor | **Exposed & Wounded:** Gain 3 attack on each of those triggers. |
| `set_49` | Ironstone Arrowhead | Ironstone Spear + Ironstone Sandals | **On Hit:** Gain 1 armor. |
| `set_125` | Woodcutter's Regret | Woodcutter's Axe + Woodcutter's Boots | Applies **-5 base max health**. The component items reward empty equipment slots, so the set's penalty is part of its tradeoff. |

## Serialized but no longer active

These definitions are still visible in the installed assets, but they are not in the current working itemset lists and should not be counted as playable sets.

| ID | Old set | Components | Last serialized function/status |
|---:|---|---|---|
| `set_40` | Crystal Mirror | Marble Mirror + Sinful Mirror | Disabled; formerly copied status effects you gained to the enemy. |
| `set_36` | Vampire Cloak | Sanguine Morphosis + Vampiric Stasis | Removed; formerly doubled healing for the turn when stunned. |
| `set_27` | Ironstone Ore | Ironstone Bracelet + Petrified Statue | Removed; gained armor equal to negative speed. |
| `set_55` | Sanguine Gemstone | Sanguine Scepter + Ruby Gemstone | Removed in bugfix 0.9.45; restored 1 health on hit when attack was exactly 1. |
| `set_101` | Ironstone Gem | Removed gemstone pairing | Removed in Patch 16; serialized effect says attack is always equal to speed. |

## Notes on misleading remnants

- A raw search finds many more `set_*` objects than the 31 above. Some are weapon modifications (for example Frozen Spork), removed content, developer placeholders (`set_991` through `set_999`), or unreleased area content.
- The English localization hint for `set_125` still says **Woodcutter's Glove**, but the current playable relation is **Woodcutter's Boots**. The newer item and current itemset list agree on Boots; the hint is stale.
- Older online guides are out of date for several sets. In particular, the installed data has Deadly Toxin at 5 acid, Marshlight Aria at 3 Symphony triggers, Twilight Crest doubling Crest triggers, and the Patch 16 sets listed above.

## Current reference pages

- https://wiki.hoodedhorse.com/He_is_Coming/Woodland_itemsets
- https://wiki.hoodedhorse.com/He_is_Coming/Swampland_itemsets
- https://wiki.hoodedhorse.com/He_is_Coming/Kingmaker_itemsets
- https://wiki.hoodedhorse.com/He_is_Coming/Patches
