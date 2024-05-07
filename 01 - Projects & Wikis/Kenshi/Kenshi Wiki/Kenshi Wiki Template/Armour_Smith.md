<figure>
<img src="Operation.jpg" title="Operation.jpg" />
<figcaption>Operation.jpg</figcaption>
</figure>

Added in the 0.50 update, **Armour Smithing** affects the crafting speed
and quality of the [Armour](Armour.md "wikilink") you craft. Armour
Smithing is composed of two components: producing crafting materials and
crafting the armour itself.

The quality of [Homemade](Homemade.md "wikilink") armour depends on the
skill of the smith (with a small random factor). Unlike in [](Weapon_Smith_(Skill).md), no research is required to
unlock higher armour grades.

The ability to smith armour is negatively affected by darkness therefore
lighting fixtures should be present throughout the whole crafting
process in order to prevent quality deterioration. The skill also
deteriorates if the character has body parts which aren't at full health
(lower skill below \<80-85%). The best way to start learn the skills
from a low level is by making raw materials such as [](Armour_Plating.md),
[Chainmail](Chainmail_Sheets.md "wikilink"),
or [Leather](Leather.md "wikilink") until at least level 40 is reached.
From that point on, the skill can be trained by making
[Bandanas](Bandana.md "wikilink"), which should provide a decent profit at
standard quality.

## Materials

Materials needed for crafting can be made with [](Fabric_Looms.md) (hemp or cotton), a [](Leather_Tanning_Bench.md), a [](Chainmail_Sheet_Fabrication_Bench.md), and a [](Plate_Beating_Station.md). Alternatively,
characters can buy or steal these materials from shops.

The material cost to craft an item is based off the coverage % of the
piece of gear. The formula is (Head + Stomach + Left Arm + Right Arm +
Left Leg + Right Leg)0.01 + (Chest)0.015. For instance Samurai Armour
which has 100 chest coverage (100x0.015=1.5 Materials) and 85 left arm,
right arm, and stomach coverage ((85+85+85)0.01=2.55 Materials) requires
4.05 materials. Heart protector has 50 chest coverage (50x0.015=0.75
Materials) which equals 0.75 Materials. The fabrics cost of items which
do not use Fabrics as their main material is 20% of the materials cost.
So, for heart protector again 0.75 x 0.2 = 0.15. So, the fabrics
required are 0.15 per Heart Protector. If an item has no coverage then
the materials are whatever they are set to.

## Crafting times

### Armour formula

$\text{hours} = \frac{1.3 \times \text{materials} \times \text{slot} \times \text{type}}{\text{Armoursmithing speed}}$

- **Materials** is the main materials used in the recipe. (So, Armour
  Plating for Samurai Armour, Fabrics for Bandanas etc...)
- **Slot** is the armour slot the armor piece is for.

| Slot                             | Multiplier |
|----------------------------------|------------|
| [Head](Headgear.md "wikilink")      | 0.6x       |
| [Armour](Body_Armour.md "wikilink") | 1x         |
| [Shirt](Shirts.md "wikilink")       | 3x         |
| [Pants](Legwear.md "wikilink")      | 0.45x      |
| [Boots](Footwear.md "wikilink")     | 0.5x       |

- **Type** is the main material used when crafting the item.

| Type                                            | Multiplier |
|-------------------------------------------------|------------|
| [Fabrics](Fabrics.md "wikilink")                   | 1x         |
| [Leather](Leather.md "wikilink")                   | 1x         |
| [Chainmail Sheets](Chainmail_Sheets.md "wikilink") | 2x         |
| [Armour Plating](Armour_Plating.md "wikilink")     | 1x         |

- **Armoursmithing speed** is based off your Armoursmithing level. You
  can see it in game by opening up your stats page and mousing over
  Armoursmithing.
  - The Formula for Armoursmithing speed is
    $\text{Armoursmithing speed} = 0.5 + 0.009 \times \text{Armoursmithing level}$

### Clothing formula

If an item has no coverage ([Clothing](Clothing.md "wikilink")) then the
crafting time is:

$\text{hours} = \frac{1.5 \times \text{materials}}{\text{Armoursmithing speed}}$

## Crafting Benches

Crafting armour is done using the [](Leather_Armour_Crafting_Bench.md), [](Chain_Armour_Crafting_Bench.md) and [](Heavy_Armour_Smithy.md). Clothing items are made on the
[Clothing Bench](Clothing_Bench.md "wikilink"). Each of those will require
a separate tech researched through [Science](Science.md "wikilink").

<table>
<caption>Buildings and Technology</caption>
<thead>
<tr class="header">
<th><p>Building</p></th>
<th><p>Research related to</p></th>
<th colspan="2"><p>Input</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="3"><p><a href="Clothing_Bench" title="wikilink">Clothing
Bench</a></p></td>
<td><p><a href="Clothing_Manufacture_(Tech)" title="wikilink">Clothing
Manufacture</a></p></td>
<td rowspan="3"><figure>
<img src="Fabrics.png" title="centre" />
<figcaption>centre</figcaption>
</figure></td>
<td rowspan="3"><p><a href="Fabrics"
title="wikilink">Fabrics</a></p></td>
</tr>
<tr class="even">
<td><p><a href="Hats_and_Headgear_(Tech)" title="wikilink">Hats and
Headgear</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="Simple_Clothing_Types_(Tech)" title="wikilink">Simple
Clothing Types</a></p></td>
</tr>
<tr class="even">
<td rowspan="2"><p><a href="Leather_Armour_Crafting_Bench"
title="wikilink">Leather Armour Crafting Bench</a></p></td>
<td rowspan="2"><p><a href="Leather_Armour_Crafting_(Tech)"
title="wikilink">Leather Armour Crafting</a></p></td>
<td><figure>
<img src="Fabrics.png" title="centre" />
<figcaption>centre</figcaption>
</figure></td>
<td><p><a href="Fabrics" title="wikilink">Fabrics</a></p></td>
</tr>
<tr class="odd">
<td><figure>
<img src="Leather.png" title="centre" />
<figcaption>centre</figcaption>
</figure></td>
<td><p><a href="Leather" title="wikilink">Leather</a></p></td>
</tr>
<tr class="even">
<td rowspan="2"><p><a href="Heavy_Armour_Smithy" title="wikilink">Heavy
Armour Smithy</a></p></td>
<td rowspan="2"><p><a href="Plate_Armour_Crafting_(Tech)"
title="wikilink">Plate Armour Crafting</a></p></td>
<td><figure>
<img src="Fabrics.png" title="centre" />
<figcaption>centre</figcaption>
</figure></td>
<td><p><a href="Fabrics" title="wikilink">Fabrics</a></p></td>
</tr>
<tr class="odd">
<td><figure>
<img src="Armour_Plating.png" title="centre" />
<figcaption>centre</figcaption>
</figure></td>
<td><p><a href="Armour_Plating" title="wikilink">Armour
Plating</a></p></td>
</tr>
<tr class="even">
<td rowspan="2"><p><a href="Chain_Armour_Crafting_Bench"
title="wikilink">Chain Armour Crafting Bench</a></p></td>
<td rowspan="2"><p><a href="Chain_Armour_Crafting_(Tech)"
title="wikilink">Chain Armour Crafting</a></p></td>
<td><figure>
<img src="Fabrics.png" title="centre" />
<figcaption>centre</figcaption>
</figure></td>
<td><p><a href="Fabrics" title="wikilink">Fabrics</a></p></td>
</tr>
<tr class="odd">
<td><figure>
<img src="Chainmail_Sheets.png" title="centre" />
<figcaption>centre</figcaption>
</figure></td>
<td><p><a href="Chainmail_Sheet" title="wikilink">Chainmail
Sheet</a></p></td>
</tr>
</tbody>
</table>

Buildings and Technology

## Blueprinted Armour

Shops in cities sell blueprints that allow factions to learn how to make
specific clothing. Many can also be found at the [](The_Great_Library.md).

### Clothing Bench

- [Bandana](Bandana.md "wikilink")
- [Samurai Clothpants](Samurai_Clothpants.md "wikilink")
- [Straw Hat](Straw_Hat.md "wikilink")

### Leather Armour Bench

- [Assassins Rags](Assassins_Rags.md "wikilink")
- [Leather Shirt](Leather_Shirt.md "wikilink")
- [Leather Turtleneck](Leather_Turtleneck.md "wikilink")
- [Leather Vest](Leather_Vest.md "wikilink")
- [Longcoat](Longcoat.md "wikilink")
- [Ninja Rags](Ninja_Rags.md "wikilink")
- [Rattan Hat](Rattan_Hat.md "wikilink")
- [Sleeveless Longcoat](Sleeveless_Longcoat.md "wikilink")
- [Tagelmust](Tagelmust.md "wikilink")
- [Tricorn Hat](Tricorn_Hat.md "wikilink")
- [Turban](Turban.md "wikilink")

### Heavy Armour Smithy

- [Mercenary Plate](Mercenary_Plate.md "wikilink")
- [Tin Can](Tin_Can.md "wikilink")
- [Heart Protector](Heart_Protector.md "wikilink") (Already learned when
  unlocking Plate Armour Crafting so this blueprint is useless)
- [Masked Helmet](Masked_Helmet.md "wikilink")
- [Visored Helmet](Visored_Helmet.md "wikilink")
- [Side Angle Hachigane](Side_Angle_Hachigane.md "wikilink")
- [Hachigane](Hachigane.md "wikilink")
- [Iron Hat](Iron_Hat.md "wikilink")
- [Plated Longboots](Plated_Longboots.md "wikilink")

### Chain Armour Crafting Bench

- [Armoured Hood](Armoured_Hood.md "wikilink")
- [Bucket Zukin](Bucket_Zukin.md "wikilink")
- [Chain Shirt](Chain_Shirt.md "wikilink")
- [Chainmail](Chainmail.md "wikilink")
- [Karuta Zukin](Karuta_Zukin.md "wikilink")
- [Kusari Zukin](Kusari_Zukin.md "wikilink")

### Special

- [Human Skin Suit](Human_Skin_Suit.md "wikilink")

## Armour Grades

| Quality    | Level Range |
|------------|-------------|
| Prototype  | 0           |
| Shoddy     | 20          |
| Standard   | 40          |
| High       | 60          |
| Specialist | 80          |
| Masterwork | None[^1]    |

Armour Grades by Level

### Critical Success Chance

Upon crafting a piece of armour there is a chance that the armour
crafted will be one quality grade higher than normal. This 'critical
success chance' is dependent on how much higher the crafter's skill is
compared to the armour quality he is crafting. The chance of a critical
success can be viewed by selecting the corresponding station for the
piece of armour, selecting "Queue...", and rolling the cursor over the
piece of armour currently being crafted. Critical Success chance
increases by 1% for every 50% of a level you gain. Example at 90
Armoursmithing you would have a 20% chance to craft Masterwork quality
armour.

### Name of Smith

The game makes note of the name of the Smith that created the armour (as
well as weapon), for example "This item was made by Player of Nameless
(faction)". This feature can be used to make little "player notes" in
the game by temporarily changing character names (via the Plastic
Surgeon) and player faction renaming. For example, "Uniform of Smiths"
Cloth Shirt can be produced and placed in a general container where a
player could place a typical uniform of his or her faction's smiths.
This can be done by renaming a character to "Uniform" and the players
faction to "Smiths" and have that character make the item.

Another use of this technique is to keep track of specific characters'
boxes. For example, a simple Iron Stick crafted by Red of Nameless
faction placed in a container can remind the player that all items in
the container belong to Red.

NB smith's name does not change on the already created armour once the
name has been changed (back). Name of Smith is erased once an item has
been sold to a vendor and the trading window is closed.

### Branded Clothing Items

High quality clothes made by the player can be identified from lower
quality items made by the player or the NPCs. While they give no stats
bonus depending on their quality, the player-crafted high quality items
are marked by a slight change in the worded description of these items.
Such items are described as a "high quality armour", followed by a
generic description that cites the creator's name ("This high quality
dyed shirt was made by Red of Nameless"). Only the smiths that are able
to regularly craft "Specialist" level gear make items with this special
description. Other clothing items simply note the creator's name. The
same naming convention applies to Armours of "Specialist" quality or
above.

<references />

## Most profitable Armour to craft for each bench

This chart is made using Specialist quality armour values and 1x
material values. If a town has a mark up (or down) it may cause an
armour piece to be more or even not profitable at all. If you are a
beginner and want to know what to make at the very start just begin with
Bandanas. This is more for users wanting to make the most out of their
high level Armoursmith.

| Armour Name                                                                                       | Time to Craft (1x speed) | Material \#          | Fabrics \#   | ~Cost per craft | Selling Price | Profit per | ~Profit/hr  |
|---------------------------------------------------------------------------------------------------|--------------------------|----------------------|--------------|-----------------|---------------|------------|-------------|
| (Heavy Armour Smithy) [Heart Protector](Heart_Protector.md "wikilink")                               | 0.975 hours              | 0.75 Armour Plating  | 0.15 Fabrics | c.387.45        | c.4,352       | c3,664.55  | c.4,066.2   |
| (Clothing Bench) [Bandanas](Bandana.md "wikilink")                                                   | 0.312 hrs                | 0.4 Fabrics          | Extra N/A    | c.25.2          | c.692         | c.666.8    | c.2,137.179 |
| (Leather Armour Crafting Bench) [Rattan Hat](Rattan_Hat.md "wikilink")                               | 0.546hrs                 | 0.7 Leather          | 0.14 Fabrics | c.118.02        | c.867         | c.748.98   | c.1,371.758 |
| (Chain Armour Crafting Bench) [Blackened Chain Hive Shirt](Blackened_Chain_Hive_Shirt.md "wikilink") | 19.5hrs                  | 2.5 Chainmail Sheets | 0.5 Fabrics  | c.6,349         | c.10,674      | c.4,325    | c.221.7948  |

Specialist Armour Cost to make and Profits/time (Note this does not
include your Armoursmithing speed. You can multiply that yourself to get
your cats/hr.

In other words, if you have Armour Plating, make Heart Protectors, if
you do not have instead of tons of Fabrics make Bandanas, if you are
running low on Fabrics then make Rattan Hats. Blackened Chain Hive Shirt
is horrid profit and is suggested to never actually make. It is the
"Best" profit of its bench however which is why it was included here.

[Category:Statistics](Category:Statistics "wikilink")

[^1]: Technically, it is possible to consistently craft Masterwork grade
    armour after reaching a certain level (130). However, this is only
    possible through reaching a critical success chance of 100%. The
    predicted result displayed cannot surpass Specialist.