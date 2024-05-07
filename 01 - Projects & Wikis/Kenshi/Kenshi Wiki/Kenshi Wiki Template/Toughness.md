Toughness was introduced in version 0.61.0 of Kenshi and appears to
replace a [stat](Statistics.md "wikilink") that was previously known as
"Warrior Spirit" (though it was never actually implemented). Toughness
determines a character's [Damage](03%20-%20Projects%20&%20Wikis/Kenshi/Kenshi%20Wiki/Kenshi%20Wiki%20Template/Damage.md "wikilink") Resistance, wound
degeneration and KO point (Knock Out Point).

## **Values**

- Damage Resistance: Starting value for a character at 0 Toughness is
  -65% and at level 100 is 65%. This means that each level of Toughness
  will increase your damage resistance by 1.3%. Until a character
  reaches level 50 they will take increased damage.
- KO point: The greater the Toughness this number will grow in negative
  value. Current range is -10 to -85 (-85 is a character at maxed
  Toughness).
- Wound Degeneration: This starts out at 1.7x at 0 Toughness and goes
  down to 0.03x at level 100. This is the speed at which cut damage over
  20 on a bodypart "\<" worsens. Certain NPCs (King, Esata, Eyegore to
  name a few) can spawn with over 102 Toughness leading to a negative
  Wound Degeneration, meaning that their injuries will actually heal on
  their own without the need for bandages.

## Formulas for values

- Damage Resistance (%) = -65 + (Toughness)1.3
- KO point = -10 - (Toughness)0.75
- Wound Degeneration Speed = 1.7 - (Toughness)0.0167

## **Improving Toughness**

The following methods are ways of improving a character's Toughness
(quoted directly from In-game):

- Getting hurt, getting beaten up, losing battles
- Get up and fight when you should be playing dead
- Bonuses if you are fighting critically wounded
- Making certain (often foolish) dialogue choices
  - "*It means starting fight with drunks, bandits, or any other usually
    hostile factions through dialog"*
- Once your health drops below your KO point \[Specific to your
  character\] your health becomes critical and you won't be able to get
  back up again. You will need healing and go into a coma.

Toughness combat exp scales based on the amount of damage received
relative to your toughness level, using the skill diff modifiers in the
FCS. Damage that is resisted via armour or toughness itself IS still
counted for this purpose, even though the damage might be nullified.

- At 25 damage or lower than your toughness level, you will receive x0.1
  the amount of exp.
- At 10 damage over your toughness level, you will receive x2 exp. This
  scales up to x6 exp at 50 damage over your toughness level.

[Category:Statistics](Category:Statistics "wikilink")