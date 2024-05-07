## Cutting Damage

**Cutting damage** is an inflicted damage type. When a character is hit
with a weapon dealing cutting damage, it causes the character to bleed.
Characters can die when the damaged area of their body falls below a
certain point, or if they run out of blood. Therefore, it is important
to bandage cuts with [First Aid Kits](Medical_Items.md "wikilink") or if a
robot, [Skeleton Repair Kits](Skeleton_Repair_Kit.md "wikilink").

## Stun Damage

**Stun damage** is an inflicted damage type. When a character is hit
with a weapon dealing blunt damage, it decreases the condition bar of
that targeted area without causing bleeding. This damage does not need
to be bandaged with First Aid Kits and will heal on it's own.

## Wear and Tear Damage

[Robot Limbs](Robot_Limbs.md "wikilink") and
[Skeleton](Skeleton.md "wikilink") characters experience **Wear and Tear
damage** after being hurt, meaning that their total health is lowered
for the affected body part and it will not fully heal. A character's
wear damage can be tracked by hovering over the condition bar of the
affected body part. However, the player will not be notified for amounts
of wear damage under 5 points. Wear and Tear damage is fixed only
through [Skeleton Repair Beds](Skeleton_Repair_Bed.md "wikilink"). Wear
damage is equal to 4% of damage taken. The damage is applied when hit,
and is not extra damage added on. So a 100 damage hit will reduce your
max health of the body part by 4. Wound degeneration or peeler machines
will not add wear damage.

## Damage Calculations

The damage that you take is cut damage/stun damage modified by your
armor and toughness. See [Resistances](Resistances.md "wikilink") for
additional information. Cut resistance and Blunt resistance are from
worn armour.

**Raw Cut Damage (1 - Cut resistance) (1 - Damage resistance) = Cut
Damage**

The resulting cut damage is this used again for the next armour piece.
The raw cut damage that already was resisted by armour cannot be reduced
further. (So if an armour piece had 80% Cut resist the next armour piece
would only be able to resist the remaining 20% of the cut damage)

Armor also has a Cut Resistance efficiency. This is the amount of cut
damage that is converted into stun damage.

**Raw Cut Damage \* Cut resistance \* (1 - Cut resistance efficiency) =
Additional Stun Damage**

The additional stun damage is not reduced further by armour.

**Raw Blunt Damage (1 - Blunt resistance) (1 - Damage resistance) =
Blunt Damage**

The values shown when hit in game (Provided floaters are enabled) is cut
damage + stun damage.

## Hitmult

- When struck in combat a value called hitmult will increase by 1, up to
  a maximum value of 5 per bodypart. If the current hitmult for a
  bodypart is over 4 and hit it will not increase. Hitmult decays by 1
  over 27.5 in game minutes. If KOed the hitmult of the hit bodypart
  will go to 2 and will not increase until healed above 0 health
  (Assuming this is to prevent repeated KOs in the same part over and
  over again). What hitmult does is as it might sound, multiplies the
  chance to be hit in a part of your body. Using Hive Solder Drone as an
  example if you are struck in your chest (140) then the new chance you
  will be hit in the chest becomes 280. So the % chance to be hit in
  your chest goes from 25% to 40%. If hit again it becomes 50% and so
  on. This is why it sometimes may seem as if enemies are focusing on
  hitting a single part of your body, as they literately are.

## **Hit Chances By Race**

The % Hit Chances are prior to being hit and Hitmult being applied.
Animal health shown is at age 1.1. Animal front limbs are labeled as
Arms in the below charts. Unique boss animals are not listed. Please
note that many % Hit chances shown do not always show the exact percent,
most are cut off a few decimals in. If a % Hit Chance shows a value like
2.08333...% this means that the 3s are repeating. The races are split
into groups (For organization reasons and...) of up to 3 to hopefully
prevent issues on smaller screens.

### **<u>Playable humanoid races</u>**

| Hiver     | [Hive Soldier Drone](Hive_Soldier_Drone.md "wikilink") |            |              |
|-----------|-----------------------------------------------------|------------|--------------|
|           | Limb Health                                         | Hit Chance | % Hit Chance |
| Head      | 200                                                 | 80         | 14.2857%     |
| Chest     | 100                                                 | 140        | 25%          |
| Stomach   | 100                                                 | 60         | 10.7142%     |
| Left Arm  | 100                                                 | 80         | 14.2857%     |
| Right Arm | 100                                                 | 40         | 7.1428%      |
| Left Leg  | 100                                                 | 80         | 14.2857%     |
| Right Leg | 100                                                 | 80         | 14.2857%     |

| Human     | [Greenlander](Greenlander.md "wikilink") |            |
|-----------|---------------------------------------|------------|
|           | Limb Health                           | Hit Chance |
| Head      | 100                                   | 80         |
| Chest     | 100                                   | 140        |
| Stomach   | 100                                   | 140        |
| Left Arm  | 100                                   | 80         |
| Right Arm | 100                                   | 40         |
| Left Leg  | 100                                   | 80         |
| Right Leg | 100                                   | 80         |

| Skeleton  | [Skeleton](Skeleton_(Race).md "wikilink") |            |              |
|-----------|----------------------------------------|------------|--------------|
|           | Limb Health                            | Hit Chance | % Hit Chance |
| Head      | 200                                    | 80         | 13.33%       |
| Chest     | 200                                    | 140        | 23.33%       |
| Stomach   | 200                                    | 80         | 13.33%       |
| Left Arm  | 200                                    | 80         | 13.33%       |
| Right Arm | 200                                    | 60         | 10%          |
| Left Leg  | 200                                    | 80         | 13.33%       |
| Right Leg | 200                                    | 80         | 13.33%       |

| Shek      | [Shek](Shek.md "wikilink") |
|-----------|-------------------------|
|           | Limb Health             |
| Head      | 125                     |
| Chest     | 125                     |
| Stomach   | 125                     |
| Left Arm  | 125                     |
| Right Arm | 125                     |
| Left Leg  | 125                     |
| Right Leg | 125                     |

| Southern Hive | [Hive Soldier Drone South Hive](Southern_Hive_Soldier_Drone.md "wikilink") |            |              |
|---------------|-------------------------------------------------------------------------|------------|--------------|
|               | Limb Health                                                             | Hit Chance | % Hit Chance |
| Head          | 200                                                                     | 80         | 14.2857%     |
| Chest         | 100                                                                     | 140        | 25%          |
| Stomach       | 100                                                                     | 60         | 10.7142%     |
| Left Arm      | 100                                                                     | 80         | 14.2857%     |
| Right Arm     | 100                                                                     | 40         | 7.1428%      |
| Left Leg      | 100                                                                     | 80         | 14.2857%     |
| Right Leg     | 100                                                                     | 80         | 14.2857%     |

### **<u>Playable Animal Races</u>**

|           | [Goat](Goat.md "wikilink") |            |              |
|-----------|-------------------------|------------|--------------|
|           | Limb Health             | Hit Chance | % Hit Chance |
| Head      | 159.75                  | 100        | 16.6666...%  |
| Chest     | 159.75                  | 100        | 16.6666...%  |
| Stomach   | 106.5                   | 100        | 16.6666...%  |
| Right Arm | 106.5                   | 100        | 16.6666...%  |
| Left Arm  | 106.5                   | 100        | 16.6666...%  |
| Right Leg | 106.5                   | 50         | 8.3333...%   |
| Left Leg  | 106.5                   | 50         | 8.3333...%   |

|           | [Pack](Pack_Bull.md "wikilink")/[Wild Bulls](Wild_Bull.md "wikilink") |            |              |
|-----------|-----------------------------------------------------------------|------------|--------------|
|           | Limb Health                                                     | Hit Chance | % Hit Chance |
| Head      | 211                                                             | 100        | 18.5185...%  |
| Chest     | 211                                                             | 100        | 18.5185...%  |
| Stomach   | 211                                                             | 100        | 18.5185...%  |
| Right Arm | 105.5                                                           | 100        | 18.5185...%  |
| Left Arm  | 105.5                                                           | 100        | 18.5185...%  |
| Right Leg | 105.5                                                           | 20         | 3.7037...%   |
| Left Leg  | 105.5                                                           | 20         | 3.7037...%   |

|           | [Crabs](Crab.md "wikilink") |
|-----------|--------------------------|
|           | Limb Health              |
| Head      | 218                      |
| Chest     | 218                      |
| Stomach   | 218                      |
| Right Arm | 218                      |
| Left Arm  | 218                      |
| Right Leg | 218                      |
| Left Leg  | 218                      |

### **<u>Unplayable Humanoid Races</u>**

| Skeleton  | [Skeleton Log-Head MKII](Skeleton_Log-Head_MKII.md "wikilink") |            |              |
|-----------|-------------------------------------------------------------|------------|--------------|
|           | Limb Health                                                 | Hit Chance | % Hit Chance |
| Head      | 200                                                         | 80         | 12.12%       |
| Chest     | 150                                                         | 140        | 21.21%       |
| Stomach   | 150                                                         | 140        | 21.21%       |
| Left Arm  | 150                                                         | 80         | 12.12%       |
| Right Arm | 150                                                         | 60         | 9.09%        |
| Left Leg  | 150                                                         | 80         | 12.12%       |
| Right Leg | 150                                                         | 80         | 12.12%       |

| Skeletons               | [Skeleton MKII Screamer](Skeleton_MKII_Screamer.md "wikilink") |            |
|-------------------------|-------------------------------------------------------------|------------|
| (Not in Skeleton Group) | Limb Health                                                 | Hit Chance |
| Head                    | 150                                                         | 80         |
| Chest                   | 150                                                         | 140        |
| Stomach                 | 150                                                         | 140        |
| Left Arm                | 150                                                         | 80         |
| Right Arm               | 150                                                         | 60         |
| Left Leg                | 150                                                         | 80         |
| Right Leg               | 150                                                         | 80         |

| Fishmen   | [Fishman](Fishman.md "wikilink") |            |
|-----------|-------------------------------|------------|
|           | Limb Health                   | Hit Chance |
| Head      | 150                           | 100        |
| Chest     | 150                           | 100        |
| Stomach   | 150                           | 100        |
| Left Arm  | 150                           | 80         |
| Right Arm | 150                           | 80         |
| Left Leg  | 200                           | 10         |
| Right Leg | 200                           | 10         |

| Cannibals | [Cannibal Skav](Cannibal_Skav.md "wikilink") |            |
|-----------|-------------------------------------------|------------|
|           | Limb Health                               | Hit Chance |
| Head      | 100                                       | 80         |
| Chest     | 80                                        | 140        |
| Stomach   | 80                                        | 140        |
| Left Arm  | 80                                        | 80         |
| Right Arm | 80                                        | 40         |
| Left Leg  | 80                                        | 80         |
| Right Leg | 80                                        | 80         |

| Deadhive  | [Deadhive Soldier](Deadhive_Soldier.md "wikilink") |            |              |
|-----------|-------------------------------------------------|------------|--------------|
|           | Limb Health                                     | Hit Chance | % Hit Chance |
| Head      | 100                                             | 80         | 14.2857%     |
| Chest     | 100                                             | 140        | 25%          |
| Stomach   | 100                                             | 60         | 10.7142%     |
| Left Arm  | 100                                             | 80         | 14.2857%     |
| Right Arm | 100                                             | 40         | 7.1428%      |
| Left Leg  | 100                                             | 80         | 14.2857%     |
| Right Leg | 100                                             | 80         | 14.2857%     |

| Hive      | [Hive Queen](Hive_Queen.md "wikilink") |
|-----------|-------------------------------------|
|           | Limb Health                         |
| Head      | 75                                  |
| Chest     | 75                                  |
| Stomach   | 75                                  |
| Left Arm  | 75                                  |
| Right Arm | 75                                  |
| Left Leg  | 75                                  |
| Right Leg | 75                                  |

### <u>**Unplayable Animal Races**</u>

|           | [Beak Thing](Beak_Thing.md "wikilink") |            |              |
|-----------|-------------------------------------|------------|--------------|
|           | Limb Health                         | Hit Chance | % Hit Chance |
| Head      | 267.5                               | 50         | 11.1111...%  |
| Chest     | 428                                 | 100        | 22.2222...%  |
| Stomach   | 428                                 | 100        | 22.2222...%  |
| Right Arm | 428                                 | 50         | 11.1111...%  |
| Left Arm  | 428                                 | 50         | 11.1111...%  |
| Right Leg | 428                                 | 50         | 11.1111...%  |
| Left Leg  | 428                                 | 50         | 11.1111...%  |

| Robotic Spiders | [Iron Spider](Iron_Spider.md "wikilink") |            |              |
|-----------------|---------------------------------------|------------|--------------|
|                 | Limb Health                           | Hit Chance | % Hit Chance |
| Head            | 200                                   | 150        | 21.4285%     |
| Chest           | 200                                   | 150        | 21.4285%     |
| Stomach         | 200                                   | 100        | 14.2857%     |
| Right Arm       | 200                                   | 100        | 14.2857%     |
| Left Arm        | 200                                   | 100        | 14.2857%     |
| Right Leg       | 200                                   | 50         | 7.1428%      |
| Left Leg        | 200                                   | 50         | 7.1428%      |

| Spiders   | [Blood Spider](Blood_Spider.md "wikilink") |            |
|-----------|-----------------------------------------|------------|
|           | Limb Health                             | Hit Chance |
| Head      | 31.5                                    | 100        |
| Chest     | 31.5                                    | 100        |
| Stomach   | 31.5                                    | 100        |
| Right Arm | 31.5                                    | 100        |
| Left Arm  | 31.5                                    | 100        |
| Right Leg | 31.5                                    | 100        |
| Left Leg  | 31.5                                    | 100        |

| Gorillos  | [Gorillo](Gorillo.md "wikilink") |            |
|-----------|-------------------------------|------------|
|           | Limb Health                   | Hit Chance |
| Head      | 273                           | 100        |
| Chest     | 364                           | 100        |
| Stomach   | 364                           | 100        |
| Right Arm | 364                           | 100        |
| Left Arm  | 364                           | 100        |
| Right Leg | 182                           | 100        |
| Left Leg  | 182                           | 100        |

| Raptors   | [River Raptor](River_Raptor.md "wikilink") |            |
|-----------|-----------------------------------------|------------|
|           | Limb Health                             | Hit Chance |
| Head      | 106                                     | 150        |
| Chest     | 106                                     | 150        |
| Stomach   | 106                                     | 100        |
| Right Arm | 106                                     | 100        |
| Left Arm  | 106                                     | 100        |
| Right Leg | 106                                     | 50         |
| Left Leg  | 106                                     | 50         |

| Colossals | [Cleanser Unit](Cleanser_Unit.md "wikilink") |            |
|-----------|-------------------------------------------|------------|
|           | Limb Health                               | Hit Chance |
| Head      | 2000                                      | 100        |
| Chest     | 2000                                      | 100        |
| Stomach   | 2500                                      | 100        |
| Right Arm | 1500                                      | 100        |
| Left Arm  | 1500                                      | 100        |
| Right Leg | 1500                                      | 50         |
| Left Leg  | 1500                                      | 50         |

|           | [Boneyard Wolf](Boneyard_Wolf.md "wikilink") |            |
|-----------|-------------------------------------------|------------|
|           | Limb Health                               | Hit Chance |
| Head      | 323                                       | 150        |
| Chest     | 323                                       | 150        |
| Stomach   | 323                                       | 100        |
| Right Arm | 323                                       | 100        |
| Left Arm  | 323                                       | 100        |
| Right Leg | 323                                       | 50         |
| Left Leg  | 323                                       | 50         |

__NOTOC__

[Category:Guides](Category:Guides "wikilink")
[Category:Combat](Category:Combat "wikilink")