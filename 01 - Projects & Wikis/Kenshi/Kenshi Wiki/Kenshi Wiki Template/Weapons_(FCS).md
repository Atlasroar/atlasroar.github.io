<figure>
<img src="Katana04.png" title="Katana04.png" />
<figcaption>Katana04.png</figcaption>
</figure>

This page contains information about [modding](Modifications.md "wikilink")
Kenshi's weapons. Modding is done through the [](Construction_Set.md). Weapons are a sub-category under
Items.

Weapons are made up of two objects: A Weapon and a Model. A Manufacturer
connects the two.

## Weapons

This is the weapon type. It includes the base stats and mesh files of
the weapon.

### Base

- Name: Pretty straightforward, this is the name which the game and
  construction set display for this Item.
- Object Type: What type of Item this is (WEAPON). Can not be changed.
- String ID: The String ID is a unique identifier for each item, it must
  never be the same for 2 objects. DO NOT CHANGE IT if already placed in
  the game world (otherwise those references will vanish). If it is
  already referenced by another object (eq item in a character
  inventory), that's ok because it will update the ID in those
  references. It is what determines when an item in a .mod file
  modifies/inherits from an item in another file (usually .base).

(rule of thumb: you will probably never need to change String ID unless
you've done something very, VERY wrong)

### Craft

- material cost: Amount of materials needed to craft.

### Damage

These attributes modify the damage inflicted by the weapon. All
attributes will affect a weapon's damage, but some attributes are more
important to some weapon types than others.

- animal damage mult: Damage multiplier of damage against animals.
  Unaffected by quality.
- armor penetration: Value (Percent) subtracted from the enemy armor
  before damage calculation. Negative values increase the effective
  armor of the target up to a max of 90%.
- bleed mult: The amount of bleeding this weapon causes. It's directly
  related to cut damage. The higher the cut damage, the more bleed
  damage is dealt via this multiplier.
- blunt damage multiplier: Weapon weight, multiplied by stats, used by
  heavy weapons to calculate weapon damage.
  - The weight of the weapon is actually the blunt dmg of the weapon x
    (20x"weight mult") or the "weight kg" of the weapon. Whichever is
    greater.
- cut damage multiplier: Multiplied by attack skill, used by sword-like
  weapons to calculate weapon damage.
- human damage mult: Multiplier of damage against humans. Unaffected by
  quality.
- minimum cut damage multiplier: Provides minimum damage cap, only handy
  for modding beginners.
- pierce damage multiplier: Bonus Harpoon damage. Not affected by weapon
  quality, only stats.
  - This adds a LOT of harpoon damage to a weapon. Commonly used for
    animal weapons in base game. MASSIVELY impacts the cut damage done
    by an animal. To give an example of the impact this has on damage...
    - A bull with 100 all stats, age 1.0, only set to use an Old
      Refitted Blade quality weapon and has a backpack on so its
      Dexterity is not increased for being naked.
      - Pierce mult set to 0 = 35.464 cut + 20.8 blunt damage vs 50
        Toughness target.
      - Pierce mult set to 1 = 201.464 cut + 20.8 blunt damage vs 50
        Toughness target.
- robot damage mult: Multiplier of damage against robots. Unaffected by
  quality.

### Files

Item models/meshes.

- bare sword: Sword mesh only, no sheath. (mesh)
- icon: Inventory icon image. (png)
- mesh: Item mesh, sheathed if a weapon. (mesh)
- physics file: Collision data for dropped items. (xml)
- sheath: Sheath mesh only, no sword. (mesh)

### General

- description: Description of the item that is displayed in tooltips
  etc.
- length: The length of the weapon, the maximum reach.

### Inventory

- auto icon image \[true-false\]: Actually does nothing for weapons.
- inventory footprint height: height of the item (in tiles) in your
  inventory.
- inventory footprint width: width of the item (in tiles) in your
  inventory.
- slot: Allows for items to go into certain inventory slots.
  (ATTACH_WEAPON for weapons)
- value: Base monetary value of the item. The final value is affected by
  quality.
- weight kg: Minimum weight of the weapon, can be overwritten by blunt
  damage multiplier if it is higher (Blunt dmgx20x"weight ).

### Inventory icon

These values determine how the icon is generated.

- icon offset H: horizontal alignment.
- icon offset V: vertical alignment.
- icon zoom: image scale, lower=bigger.

## Mod

- attack mod: Bonus/penalty to melee attack skill.
- defense mod: Bonus/penalty to melee defense skill.
- indoors mod: Modifier to attack + defense if indoors.
- weight mult: Multiplier for weight. Used to make weapons lighter
  without affecting the blunt damage. (Although the description
  continues by saying it should usually be kept at 1.0, MANY weapons
  have under 1.0 (All Polearms, many Sabres, 2 Blunt Weapons...))

## Models

This contains the weapon texture and modifiers for the stats. The model
can also adjust the weapon size.

## Manufacturers

Manufacturers contain a list of weapons and a list of models. All
permutations of the listed weapons and models are possible weapons in
the game. They also contain various stat modifiers that affect the final
weapon. The first value of each row in the "weapon models" list is
called "model value" and it's used in the weapon stat generation,
ranging from 1 to 100. In the unmodded game, it starts at 5 on "Rusted
junk" and increases at intervals of 5 for each new model until it
reaches 50 "Catun No. 3" at which it will skip 45 as "MK 1" is 50. It
will then skip 65 as "Edge type 1" is 70. The trend continues until
"Edge type 3" at 80. Meitou is 100.

As a reference, here is a table with all of the stat modifiers of each
manufacturer on the base game.

| Manufacturer | Blunt damage mod | Cut damage mod | Min Cut damage | Weight mod | Price mod |
|--------------|------------------|----------------|----------------|------------|-----------|
| Unkown       | 1                | 1              | 1              | 1          | 0.3       |
| Ancient      | 1                | 0.9            | 1              | 0.7        | 0.8       |
| Catun        | 1.2              | 1              | 1              | 1.2        | 1.2       |
| Skeletons    | 1                | 1              | 1              | 1          | 1.2       |
| Edgewalkers  | 1                | 1.1            | 1              | 1          | 1.4       |
| Cross        | 1                | 1.1            | 1              | 1          | 2         |
| Homemade     | 1                | 1              | 1              | 1          | 1         |

## Price multipliers

There are additional hidden quality multipliers when calculating for
weapon base price. These values are reversed engineered and double
checked against the default "sword price" and "loot multiplier". Do note
that some of these values may be off due to rounding issues.

| Quality            | Level | Multiplier |
|--------------------|-------|------------|
| Rusted Junk        | 5     | 18.85      |
| Rusted Blade       | 10    | 20.65      |
| Mid-Grade Salvage  | 15    | 23.3       |
| Old Refitted Blade | 20    | 27.05      |
| Refitted Blade     | 25    | 32.275     |
| Catun 1            | 30    | 39.35      |
| Catun 2            | 35    | 48.55      |
| Catun 3            | 40    | 59.95      |
| Mk 1               | 50    | 87.5       |
| Mk 2               | 55    | 101.8      |
| Mk 3               | 60    | 115.025    |
| Edge 1             | 70    | 135.625    |
| Edge 2             | 75    | 142.7      |
| Edge 3             | 80    | 147.9375   |
| Meitou             | 100   | 157.392    |

## Stat generation formulas

To get an idea of how powerful or weak, or how expensive a given weapon
is, here are some of the formulas used to generate the stats as seen
in-game. The damage multipliers are taken from the damage section of the
given weapon, the "weight kg" from the inventory section, and both the
"model value" and "manufacturer factor" from the Manufacturer
definitions.

- **Blunt Damage**: blunt damage multiplier \* model value / 50 \*
  manufacture factor
- **Cut Damage**: cut damage multiplier \* (0.3 + 0.017 \* model value)
- **Weight**: Maxim (weight kg; 20 \* Blunt Damage \* weight mult \*
  manufacture factor)
- **Price:** FCS Value \* Quality \* Manufacturer \* FCS Global Sword
  Price Mult \* FCS Loot Price Mult Gear (or FCS Loop Price Mult Player
  Weapon)

In order to use a weapon without a combat speed penalty you require a
strength level equal to 40 times the blunt damage of a weapon or just
the weight of the weapon, whichever is the greater value. The x2 weight
rule of thumb spread around does not work for many weapons such as all
Katanas, Polearms, as well as many Blunt weapons and Sabres.

[Category:Modding](Category:Modding "wikilink")