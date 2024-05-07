## Overview

Some skills have their experience rate modified by the "strength" of
your opponent. The logic behind this is never explained in-game, leaving
many players in the dark about how it works. This page is an attempt to
explain exactly what it's checking to determine these modifiers.

When an attacker swings their weapon, a check is run against their stats
to determine the multiplier. This check is always run between two
skills, one from each character, though the specific skills changes
depending on the role of the character in the engagement and their
fighting style (more on this later). This exp rate multiplier scales
from x0.1 at 22.5 levels (The value is set for 0% XP at 25 levels over
your opponent's skill however it has a minimal XP % of 10% which is
achieved at 22.5) above the opponent's opposing skill, to x6.0 at 50
levels below the opponent's opposing skill.

As of right now there are eleven known stats that are affected by this
logic.

- [Melee Attack](Melee_Attack.md "wikilink")
- [Melee Defense](Melee_Defense.md "wikilink")
- [Martial Arts](Martial_Arts.md "wikilink")
- [Dodge](Dodge.md "wikilink")
- [Dexterity](Dexterity.md "wikilink")
- [Blunt](Blunt_Weapons.md "wikilink")
- [Hackers](Hackers.md "wikilink")
- [Heavy Weapons](Heavy_Weapons.md "wikilink")
- [Katanas](Katanas.md "wikilink")
- [Polearms](Polearms.md "wikilink")
- [Sabres](Sabres.md "wikilink")

While not technically part of this system, it is important to note that
exp gain will be drastically altered based on if the swing was a hit or
not. When a unit is hit the defense experience is given to that unit
first, and then attack experience is given based on the new defense
value. Getting hit grants 8x the defense experience compared to
blocking. Having your attack blocked grants only half of the attack
experience. (Dodging can also sometimes reduce exp gain to 0, as the
attack needs to make contact with their hitbox to trigger exp gain at
all for either side, and some dodges will cause the character's hitbox
to avoid the attack altogether.)

## Combat Styles

The skills checked depend on whether you are wielding a weapon or not.
These are explained below.

### Weapon

Offensively, this style will use [Melee Attack](Melee_Attack.md "wikilink")
as its offensive stat. It will challenge the opponent's [](Melee_Defense.md) if they have a weapon, or [](Martial_Arts.md) skill if they are unarmed (Note: Only for
the purposes of exp calculation, it will still challenge the
[Dodge](Dodge.md "wikilink") skill to determine if you hit or not, it just
has no bearing on exp rate here).

Defensively, this style will use [](Melee_Defense.md) as its defensive stat. It will
challenge the opponent's [Melee Attack](Melee_Attack.md "wikilink") if they
have a weapon, and their [Martial Arts](Martial_Arts.md "wikilink") skill
if they are unarmed.

### Unarmed

Offensively, this style will use [Martial Arts](Martial_Arts.md "wikilink")
as its offensive skill. It will challenge the opponent's [](Melee_Defense.md) if they have a weapon, or [](Martial_Arts.md) if they are unarmed (Note: Only for the
purposes of exp calculation, it will still challenge the
[Dodge](Dodge.md "wikilink") skill to determine if you hit or not, it just
has no bearing on exp rate here).

Defensively, this style will use [Dodge](Dodge.md "wikilink") as its
defensive skill (Yes, despite the other skills not challenging it to
determine their exp gain, it will challenge them to determine its own
exp gain). It will challenge the opponent's [](Melee_Attack.md) if they have a weapon, and [](Martial_Arts.md) if they are unarmed.

### Animals

Animals are mostly identical to the weapons combat style, with a notable
exception. Animals will use [Melee Attack](Melee_Attack.md "wikilink") as
their offensive stat when being challenged by someone else's defensive
stat, however when determining their own exp gain they will challenge
both their [Melee Attack](Melee_Attack.md "wikilink") and [](Martial_Arts.md) skills against the opponent's defensive
skill, and both skills will gain exp independently of each other (i.e.
one could gain 4x exp rate, and the other 0.5x).

Defensively, they just use [Melee Defense](Melee_Defense.md "wikilink") as
their defensive skill.

## Dexterity

[Dexterity](Dexterity.md "wikilink") is unusual, as it is never actually
used in any of this logic. It is however modified by the results of the
challenges mentioned above. It only gains exp on attacking. And it will
check your offensive skill vs the opponent's Defense or Martial Arts (If
unarmed), and then modify its gain by the result. The experience gained
is then multiplied by the ratio of cut damage to total damage on a
weapon. Cut damage / (Cut damage + Blunt damage) To give an example, (If
all skills are at the same level) if landing an attack when using a
weapon with 0.3 cut damage and 0.1 blunt damage results in 45% of an
attack level then the unit will also gain 33.75% Dexterity experience.
(As 0.3/0.4 is 0.75 and then 0.75 x 45 results in 33.75)

## Weapon Skills

The experience gained is based off your weapon skill level vs your
opponents modified defense/martial arts level. (Modified meaning wearing
armour that reduces/increases their level in the skill) You only gain
40% of this amount if your opponent blocks your attack.

If blocking an attack you will gain a small amount of weapon skill XP
based off your weapon skill level vs your opponents modified
attack/martial arts level.

## Stat Modifiers

There are many sources of modifiers to the skills involved in these
calculations, but none of them affect the exp gain from the Stronger
Opponent Logic; the base, unmodified stats are used solely. The
following modifiers will affect some challenges, which will use the
modified levels of the stats in the calculations rather than the base
levels.

- Armour Modifiers
- Backpack penalties
- Encumbrance penalties (though the penalties are only applied to
  [Martial Arts](Martial_Arts.md "wikilink") and [Dodge](Dodge.md "wikilink"))
- Indoor bonuses/penalties
- Injuries (though the penalties themselves are only applied to
  [Dodge](Dodge.md "wikilink"))
- Weather penalties
- Weapon modifiers (though obviously only weapon users get the modifiers
  themselves)

Then there is one more source of modifiers, and it is treated
differently depending on the skills. Block Mode will be ignored by
[Melee Attack](Melee_Attack.md "wikilink"), [](Melee_Defense.md), [](Martial_Arts.md), and [Dexterity](Dexterity.md "wikilink")
Challenges. The only skill that accounts for the bonus provided by
Blocks Mode is [Dodge](Dodge.md "wikilink"), which will gain less exp with
the mode toggled on, as it increases your effective level.

[Category:Statistics](Category:Statistics "wikilink")