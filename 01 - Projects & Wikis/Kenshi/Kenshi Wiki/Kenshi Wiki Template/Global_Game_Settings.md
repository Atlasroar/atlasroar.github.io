The point of this guide is to explain what editing the Global game
settings (GLOBAL CONSTANTS) does in FCS. This page was created with
Kenshi v1.0.55 and FCS v2.0.

### WIP

## Block success

- base block chance - Chance to block vs opponent when defenders defense
  = attack(or martial arts)
- block chance increase per 10levels - If defence is 10 levels over
  opponents attack the chance to block successfully goes up by this
  much. The Maximum chance is 95%
- block chance reduction per 10levels - If defence is 10 levels under
  opponents attack the chance to block successfully goes down by this
  much. The Minimum chance is 5%.

## Combat balance

- attack chance factor - How often unit will attack over another if
  their attack skill is higher. 1 + ("attack chance factor") (attack
  levels higher than opponent) = chance of attacking.
- max num attack slots - The description is a bit misleading. Multiple
  enemies can and will attack you at once even with 1 set due to a ton
  of different factors. The higher the Attack slots the more it rewards
  giant groups.

## Combat damage

- blunt damage 1 -
- blunt damage 99 -
- blunt permanent organ damage - Causes blunt damage to do part flesh
  "organ" damage (what cut normally does). If the value is 0 then it
  does stun damage like normal. If it is 1 then it deals flesh "organ"
  damage.
- bow damage 1 - This value is multiplied by the "Pierce damage min 0"
  and "Pierce damage min 1" of a Crossbow to determine the minimum
  damage of a Crossbow.
- bow damage 99 - This value is multiplied by the "Pierce damage max 0"
  and "Pierce damage max 1" of a Crossbow to determine the maximum
  damage of a Crossbow.
- cut damage 1 - "cut damage 1" x "damage multiplier" = Minimum cut
  damage for cut majority weapons. For cut damage weapons you also take
  ("cut damage 99" - "cut damage 1") x "global damage mult" to determine
  the scaling cut damage gained for each 1.0 cut damage a cut majority
  weapon has. Half of this value is given for every 100 Dex, half is
  given for every 100 Weapon skill)
- cut damage 99 -
- damage resistance max - Damage Reduction at 100 Toughness. 1 = 100%. 0
  = 0%, -1 = -100% and so on. Does not scale past level 100 Toughness.
  If this is set over 1 then a target will heal from damage taken when
  they reach that level.
- damage resistance min - Damage Reduction at 0 Toughness. 1 = 100%, 0 =
  0%, -1 = -100% and so on. Does not scale below level 0 Toughness.
- immediate blood loss - (Cut dmg done)(Weapon Blood Loss)(Racial
  Bleedrate of target hit)("immediate blood loss") = How much blood/oil
  a character will lose instantly upon taking damage.
- pierce damage multiplier - Multiplier for the scaling pierce damage
  (Harpoon damage) on weapons. It is also multiplied by the global
  "damage multiplier". In base game this is on every animal weapon
  except Gorillos. This makes up a TON of animal damage and is why
  animals have insanely high damage when trained. However, it is hard
  countered by armour.
- stumble damage max - When hit you will always be staggered, however
  stumble is the long animation which plays if you receive too much
  damage. The description is misleading. It is actually "stumble damage
  max" x "damage multiplier". By default, this value is set to 80 which
  means that at 100 Toughness the result is 52.
- unarmed damage mult - Another description which lies. It states it
  affects all damage calculations for this damage type however it only
  affects the damage gain from Toughness for Martial Arts.

## Faction

- max faction size - Maximum characters the player can have in their
  faction.
- max squad size - Max amount of characters a player can drag into a
  squad.
- max squads - Max squads the player can have at a given time.

## GAME SPEEDS

- build speed - The higher this value, the faster you can build.
- prison time - The higher this value, the longer the jail sentence.
- production speed - The higher this value, the faster crafting will be.
- research level increase rate - The higher this value, the longer
  higher level technologies will take.
- research rate - The lower this value, the faster research speed will
  be.

## General

- min dismantle materials percent - Amount of materials that are dropped
  when mismantling a structure. When dismantling an item with 1 material
  it will give that 1 material back, if the amount is not exact, it may
  give the amount rounded up or down.
- minimum lockpick chance - Minimum % chance to attempt to unlock a
  container. (5% by default

## Global balance

- damage multiplier - Multiplier for many formulas including scaling
  piercing/cut/blunt damage, minimum cut/blunt damage, stumble damage
  max. Does not affect the damage of Crossbows or Martial Arts.

## Hunger

- bed hunger rate - Multiplier for the speed at which hunger drains when
  sleeping.
- encumbrance hunger rate - Multiplier for hunger rate when fully (100%)
  encumbered. (1 = 2x hunger speed)
- fed recovery rate mult - Multiplier for the speed your hunger fills
  after eating food.
- food quality mult - The "charges" value on a food item multiplied by
  this value = Nut total on the item.
- starvation time - Time it takes for lose 100 Hunger, the higher this
  value, the slower hunger will drain.

## Medic

- heal rate mult -
- medic speed mult -
- medkit drain 1 -
- medkit drain 99 -
- resting heal rate mult - Multiplier for blood regeneration when
  sleeping. (Does NOT affect bodypart heal rate)
- robot wear rate - If this value is over 0 then combat damage taken on
  robotic health will decrease the maximum health of that bodypart. A
  value of 1 (default) means a health decrease of 4% of the damage
  taken.
- XP rate medic 1 - How fast you level field medic and robotics at level
  0.
- XP rate medic 99 - How fast you level field medic and robotics at
  level 100.

## Medical

## Prices

## Weather

## Weight

## XP