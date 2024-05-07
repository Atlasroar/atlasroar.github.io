On individual item pages for [Armour](Armour.md "wikilink"), one can find
stats for each type and quality level of armor items. The stats listed
may appear different than in game. This is because the game displays
some values incorrectly. ([Katanas](Katanas.md "wikilink") showing as
having -39% robot damage as an example)

These stats, however, are determined internally by the following
formulae[^1]: (Important to add that items cannot have more than 90% Cut
resistance or Blunt resistance. Items which would have higher than 90%
(Masterwork [Samurai Helmet](Samurai_Helmet.md "wikilink") as an example)
will stop at 90% Cut resistance.

Cut Resistance = (Level +/- Level Bonus) \* (Class \* Material+ Def
Bonus) + (Material Bonus \* Class)

Blunt Resistance = (Level +/- Level Bonus) \* (Class \* Material+ Def
Bonus) + (Material Bonus \* Class)

Harpoon Resistance = (Level +/- Level Bonus) \*Material\*armors
multiplier

Athletics, combat speed, and stealth all use the same formula to
calculate their bonuses
;$StatEffect = Armors Multiplier * ((ClassMax-ClassMin)*
\left ( \frac{Level \pm Level Bonus}{100} \right ) +ClassMin)* ...$

$... ((Material Max-Material Min)*\left ( \frac{Level \pm Level Bonus}
{100} \right ) +Material Min)$

Headgear does not negatively affect athletics, combat speed, or stealth.
Only legwear and footwear affect athletics.

Shirts have their resistances multiplied by 0.8.

Armors multiplier of Harpoon Resistance is assigned to each armor. (It
is usually 1.0)

The weight of an armour piece is dependent on its coverage amount, the
slot it fills and the type of Material it is made of. The following
values shown in the below table were obtained by modding items to have
coverage values such as 100,000 for certain parts to check their weights
then changing around the material types. Using Metal Plate to compare
against the others you will find that Chainmail weighs 0.9x, Leather
0.25, and Cloth 0.1x. Comparing the Armour/Pants/Boots Slots against
Head and Shirt you will find that Head Slot items weigh 1.5x and Shirt
Slot items weigh 0.5x. The weight set on an armour piece is only used if
an item has no coverage. As for the coverage values chest adds 50% more
to the weight of an item than the other coverage parts. If an item
weight does not exceed 1 kg using these values, as an example a [](Holy_Servant_Rags.md) they will be set to 1 kg.

|                                        | Head        | Chest        | Stomach     | Left Arm    | Right Arm   | Left Leg    | Right Leg   |
|----------------------------------------|-------------|--------------|-------------|-------------|-------------|-------------|-------------|
| \[Metal Plate\] Head Slot              | 0.0625 kg   | 0.09375 kg   | 0.0625 kg   | 0.0625 kg   | 0.0625 kg   | 0.0625 kg   | 0.0625 kg   |
| \[Metal Plate\] Armor/Pants/Boots Slot | 0.05 kg     | 0.075 kg     | 0.05 kg     | 0.05 kg     | 0.05 kg     | 0.05 kg     | 0.05 kg     |
| \[Metal Plate\] Shirt Slot             | 0.025 kg    | 0.0375 kg    | 0.025 kg    | 0.025 kg    | 0.025 kg    | 0.025 kg    | 0.025 kg    |
| \[Chain\] Head Slot                    | 0.05625 kg  | 0.084375 kg  | 0.05625 kg  | 0.05625 kg  | 0.05625 kg  | 0.05625 kg  | 0.05625 kg  |
| \[Chain\] Armor/Pants/Boots Slot       | 0.045 kg    | 0.0675 kg    | 0.045 kg    | 0.045 kg    | 0.045 kg    | 0.045 kg    | 0.045 kg    |
| \[Chain\] Shirt Slot                   | 0.0225 kg   | 0.03375 kg   | 0.0225 kg   | 0.0225 kg   | 0.0225 kg   | 0.0225 kg   | 0.0225 kg   |
| \[Leather\] Head Slot                  | 0.015625 kg | 0.0234375 kg | 0.015625 kg | 0.015625 kg | 0.015625 kg | 0.015625 kg | 0.015625 kg |
| \[Leather\] Armor/Pants/Boots Slot     | 0.0125 kg   | 0.01875 kg   | 0.0125 kg   | 0.0125 kg   | 0.0125 kg   | 0.0125 kg   | 0.0125 kg   |
| \[Leather\] Shirt Slot                 | 0.00625 kg  | 0.009375 kg  | 0.00625 kg  | 0.00625 kg  | 0.00625 kg  | 0.00625 kg  | 0.00625 kg  |
| \[Cloth\] Head Slot                    | 0.00625 kg  | 0.009375 kg  | 0.00625 kg  | 0.00625 kg  | 0.00625 kg  | 0.00625 kg  | 0.00625 kg  |
| \[Cloth\] Armor/Pants/Boots Slot       | 0.005 kg    | 0.0075 kg    | 0.005 kg    | 0.005 kg    | 0.005 kg    | 0.005 kg    | 0.005 kg    |
| \[Cloth\] Shirt Slot                   | 0.0025 kg   | 0.00375 kg   | 0.0025 kg   | 0.0025 kg   | 0.0025 kg   | 0.0025 kg   | 0.0025 kg   |

Weight added per 1% coverage by material and slot

|         |           |        |          |      |            |            |
|---------|-----------|--------|----------|------|------------|------------|
| Quality | Prototype | Shoddy | Standard | High | Specialist | Masterwork |
| Level   | 5         | 20     | 40       | 60   | 80         | 95         |

|                    |                    |       |       |        |       |
|--------------------|--------------------|-------|-------|--------|-------|
| Armour Class       |                    | Cloth | Light | Medium | Heavy |
| Class              | (Cut Resistance)   | 0.4   | 0.8   | 0.9    | 1.0   |
|                    | (Blunt Resistance) | 0.03  | 0.21  | 0.27   | 0.3   |
| Class Stat Effects | (Athletics Min)    | 1     | 1     | 0.85   | 0.8   |
|                    | (Athletics Max)    | 1     | 1     | 1      | 0.95  |
|                    | (Combat Speed Min) | 1     | 1     | 1      | 0.9   |
|                    | (Combat Speed Max) | 1     | 1     | 1      | 1     |
|                    | (Stealth Min)      | 1     | 1     | 0.9    | 0     |
|                    | (Stealth Max)      | 1     | 1     | 0.9    | 0.4   |

|                       |                      |       |         |       |       |
|-----------------------|----------------------|-------|---------|-------|-------|
| Material Type         |                      | Cloth | Leather | Chain | Plate |
| Material              | (Cut Resistance)     | 0.1   | 0.55    | 0.6   | 0.75  |
|                       | (Blunt Resistance)   | 1     | 1.33... | 1     | 2     |
|                       | (Harpoon Resistance) | 0     | 0.35    | 0.6   | 0.9   |
| Material Bonus        | (Cut Resistance)     | 0     | 0       | 5     | 10    |
|                       | (Blunt Resistance)   | 0     | 0       | 0     | 0     |
| Material Stat Effects | (Athletics Min)      | 1     | 1       | 1     | 1     |
|                       | (Athletics Max)      | 1     | 1       | 1     | 1     |
|                       | (Combat Speed Min)   | 1     | 1       | 1     | 1     |
|                       | (Combat Speed Max)   | 1     | 1       | 1     | 1     |
|                       | (Stealth Min)        | 1     | 1       | 0.3   | 0.1   |
|                       | (Stealth Max)        | 1     | 1       | 0.7   | 0.8   |

Each type of armour item is assigned "Level bonus", "Cut Def Bonus" and
"Blunt Def Bonus", (and a parameter for Cut resistance Efficiency) thus
items sharing the same "Class" and "Material Type" may have different
Cut resistance and Blunt resistance.

<references />

[Category:Modding](Category:Modding "wikilink")

[^1]: [Comment on Steam Forums by
    Shidan](https://steamcommunity.com/app/233860/discussions/3/1752394382346346068/)