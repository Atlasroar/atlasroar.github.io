This page contains information about [modding](Modifications.md "wikilink")
Kenshi's characters. Modding is done through the [](Forgotten_Construction_Set.md) (FCS).

## Attributes

Attributes are the Items own stats that do not require references to
other Items (such as weapons or factions). These are mostly strings,
integers and mesh/body files. They are found on the left-hand side of an
Item's properties window.

### Base

- Name: Pretty straightforward, this is the name which the game and
  construction set display for this Item.
- Object Type: What type of Item this is (CHARACTER). Cannot be changed.
- String ID: The String ID is a unique identifier for each item, it must
  never be the same for 2 objects. DO NOT CHANGE IT if already placed in
  the game world (otherwise those references will vanish). If it is
  already referenced by another object (e.g., item in a character
  inventory), that's okay because it will update the ID in those
  references. It is what determines when an item in a .mod file
  modifies/inherits from an item in another file (usually .base).

(Rule of thumb: you will probably never need to change String ID, unless
you've done something very, VERY wrong)

### Bounty

- Assigns Bounties: If true, this character will assign bounties to
  characters they see committing crimes.
- Bounty Amount: Size of bounty (if any).
- Bounty Amount Fuzz: Bounty amount will randomly vary by this amount.
- Bounty Chance: Chance of this character having a bounty (between 0 and
  100).

### General

- Body: The body shape of this character (.body file). Leave blank for
  random body.
- Dumb: This character is incapable of using dialogue, except in cases
  the dialog specifically calls for the character.
- Faction Importance: Multiplier for the effect on faction relations any
  actions relating to this character. Set low for peasants, high for
  nobles or diplomats (nobles like Tengu have it set to 100).
  Essentially this expresses how important this character is to its
  faction.
- Mesh: Supposed to change the character's mesh, does not seem to do
  anything. Use body instead.

### Levels

- Armour Grade: Sets the grade of armour worn by this character.
- Armour Upgrade Chance: Percent chance that a piece of armour worn by
  the character will be one weapon grade higher.
- Combat Stats: Base level for combat-related skills.
  - Strength, Toughness, Dexterity, Weapon Skills, (0.5x) Assassination,
    Athletics, Swimming, Melee Attack, Melee Defense, (0.1x) Martial
    Arts, (0.1x) Dodge, Turrets, Precision Shooting, Field Medic.
- Ranged Stats: Base level for ranged combat skills.
  - Perception, Turrets, Crossbows, Precision Shooting.
- Stats Randomize: Randomizes stats by this amount. (The randomization
  occurs before racial bonuses)
- Stealth Stats: Base level for stealth-related skills. (Overwrites
  stats that are given from Combat stats)
  - Dexterity, Stealth, Lockpicking, Thievery, Assassination, Field
    Medic.
- Strength: Base level for this character's strength. (Overwrites
  Strength given from Combat stats)
- Unarmed Stats: Base level for hand-to-hand skills. (Overwrites stats
  effected given from Combat stats)
  - Dexterity, Martial Arts, Dodge.

### Money

- Money Item Max: Maximum number of [Cats](Cats.md "wikilink") the
  character may have in their inventory (the physical money they have).
- Money Item Min: Minimum number of cats the character may have in their
  inventory (the physical money they have).
- Money Item Prob: Likelihood of this character having cats in their
  inventory, 0-1.
- Money Max: Maximum amount of money that this character will spawn with
  (i.e., for buying at a [Shop Counter](Shop_Counter.md "wikilink")). Works
  like "wages" works, except that it isn't broken like "wages" is. Will
  not be visible in inventory.
- Money Min: Minimum amount of money that this character will spawn with
  (i.e., for buying at a [Shop Counter](Shop_Counter.md "wikilink")). Works
  like "wages" works, except that it isn't broken like "wages" is. Will
  not be visible in inventory.
- Wages: This amount of money is added to the character's balance every
  day, ideally to make sure civilians can keep shopping. Wages are
  broken, meaning that NPCs will run out of money (except if "money max"
  and "money min" have been set to non-0).

### Tags

- Is Trader: If true, this character is a trader. Must have either a
  large backpack or a shop, and a vendor item list. If this is set to
  true the character will obtain cats based off their stock value. (If
  set to false they can still be traded with but will have no money,
  examples are Holy Nation and Traders Guild Caravans)
- NPC Class: The NPC's classification, used so different NPCs can
  recognize each other. Once the NPC is a playable character (due to
  having been recruited), the NPC class it has doesn't do nor changes
  anything.

### Type

- Female Chance: Percent chance that this character will spawn as a
  female.
- Named: If true, this character has a name randomly chosen from the
  name list. Otherwise, the "Name" attribute will be used.
- Shaved: Whether or not this character's head is shaved like a slave's.
  For Sheks, this will result in their horns being removed.
- Slave: Sets current slave state, such as none, obedient, or escaped.
- Unique: This character will only ever spawn once.
- Wears Uniform: This character's clothing counts as a faction uniform.
  Particularly, if set true for a player character, its clothing will be
  set as part of the player faction.

## References

References are properties of an item that are determined by other Items,
such as a character's inventory, a faction's members or a town's
residents. These are not always required and can often be left
blank. They are found on the right-hand side of an Item's properties
window.

- AI Goals: Set of goals that will always apply to this character if
  NPC. For player characters, this doesn't do anything.
- Animation Files: Overrides the default animation files with other
  specified files.
- Announcement Dialogue:
- [Backpack](Backpacks.md "wikilink"): What kind of backpack this character
  spawns with.
- [Blueprints](Blueprints.md "wikilink"): Blueprints found in this
  character's inventory.
- Bounty Factions: If this character has a bounty specified, these
  factions that will arrest it. If one is not specified, the character's
  bounty will default to a United Cities bounty.
- [Clothing](Clothing.md "wikilink"): What equipment this character spawns
  with. Negative quantity will count as a chance for nothing in that
  item's slot. Chance is relative, and per slot.
- [Crossbows](Crossbows.md "wikilink"): The crossbows that this character
  starts with. Crossbows are a flat % chance of spawn, independent of
  melee weapon chances. If character is selected to spawn with crossbow,
  it will attempt to move the back weapon of the character (if they had
  one) to the hip slot. If the hip slot is too small for the weapon or
  is already full, the back weapon will simply be removed and replaced
  by the crossbow.
- Death Items: Items spawned in the character's inventory on death, such
  as trophies. If removed from a living character's inventory, they will
  be instantly killed.
- Death Triggers: If the player kills the character, triggers an assault
  on the player's outpost.
- Dialogue: Adds to the dialogue package for when the player talks to
  this character.
- Dialogue Package: Which dialogue package this character uses.
- Dialogue Package Player: Dialogue this character uses when
  player-controlled.
- [Faction](Factions.md "wikilink"): What faction the character belongs to.
  This value is usually useless, as the squad will override it.
- Imprisonment Triggers: Triggers a raid on the player's outpost when
  the player imprisons this character.
- Inventory: What items the character spawns with. If the character
  spawns without enough space in his inventory (due to having too many
  or too big items), but has a backpack with enough space, then the
  surplus items will spawn in the backpack. Items will spawn with random
  charge values (Like food, first aid kits, repair kits...) unless they
  are set to spawn with 2 of that item. (In which case both will be at
  full charges)
- [Personality](Personality.md "wikilink"): What Personality the character
  has. Personality determines dialogue. A character can only have one
  active personality tag. If multiple are assigned to a character, a
  random one will be picked from them, with the probability of being
  picked given by whether it pertains to the "always", "common", "rare"
  or "never" tags. The "warm/kind", "cold/cruel", "normal" and "end"
  personalities are not naturally used in the game.
- [Race](Races.md "wikilink"): What race this character is of.
- [Robot Limbs](Robot_Limbs.md "wikilink"): Specifies robotic limbs that
  this character spawns with. The first value is for quality level,
  vanilla values (Shoddy, Standard, etc.) are 5, 20, 40, 60, 80, 95;
  though it should accept alternate levels too. A negative quality level
  will make that entry count as a chance to keep their normal limb.
- Schedule: Actions that this character does at specific times during
  the day.
- Shopping: Types of items that this character will buy at a [](Shop_Counter.md). This runs on item type, not
  specific items. So, if a character has [Bread](Bread.md "wikilink") on
  their list, they can buy all food items, etc.
- Starting Health: Character's health (%) on spawn. This is cut damage
  and is bandaged already. A value less than -100% the max health for
  their race on limbs means amputation.
- [Stats](Statistics.md "wikilink"): Base stat package the character spawns
  with. Can be slightly randomized with the "stats randomise" attribute.
- Unique Replacement Spawn: If this character is a unique character who
  has died or was already spawned, the game will try to spawn another
  character instead.
- Vendors: What kind of vendor this character is. Package determines
  shopkeeper's inventory. Only works on characters if they have a
  backpack on, otherwise set the vendor list on the squad.
- Weapon Level: When this character spawns, it's weapons will be of this
  level (manufacturer). The value is the relative chance between the
  manufacturers.
- [Weapons](Weapons.md "wikilink"): Weapons this character spawns with. If
  the total chance from all the weapons combined equals less than 100,
  there is a chance to spawn with no weapon in that slot. If it equals
  more than 100, it will only count down from the top of the list in the
  FCS till it hits 100. Then any chance that makes it go over 100 is
  ignored. (e.g., five weapons all with a 30 chance, the top three in
  the list would each have a 30% chance to be selected, the fourth one
  would only have a 10% chance to be selected, and the fifth would have
  no chance.) 0 Chance is treated the same as a 100 chance if it is the
  only weapon present. And a 0 or negative quantity causes that weapon
  to be completely ignored in spawning if there are multiple weapons.
  - Val 0 = How many weapons spawn on the character. (2 max for back and
    1 max for hip)
  - Val 1 = Slot the weapon spawns in. 0=hip 1=back
  - Val 2 = Absolute chance of spawning.
    - The game allows for 2 items to spawn on a characters back and 1 on
      their hip.

[ru:Characters (FCS)](ru:Characters_(FCS) "wikilink")

[Category:Modding](Category:Modding "wikilink")