This page contains information about modding Kenshi's research topics.
Modding is done through the construction set. Research is one of the
main categories.

## Attributes

Attributes are the Items own stats that do not require references to
other Items (such as weapons or factions). They are found on the left
hand side of an Item's properties window.

### Base

- Name: Pretty straightforward, this is the name which the game and
  construction set display for this Item.
- Object Type: What type of Item this is (RESEARCH). Can not be changed.
- String ID: The String ID is a unique identifier for each item, it must
  never be the same for 2 objects. DO NOT CHANGE IT if already placed in
  the game world (otherwise those references will vanish). If it is
  already referenced by another object (e.g. item in a character
  inventory), that's okay because it will update the ID in those
  references. It is what determines when an item in a .mod file
  modifies/inherits from an item in another file (usually .base).

### Building Improvements

The attributes in this category affects items contained in the "improve
buildings" reference.

- Power Capacity Increase: Increases the power capacity by this amount.
- Power Increase: Increases the power output by this amount.
- Production Mult: Increases the production multiplier by this amount.

### General

- Blueprint Only: If True, the player won't be able to research this
  manually. Instead, they'll have to obtain a blueprint.
- Category: The category of the research in the [](Technology.md). The original categories are as follows:
  - Core
  - Crafting
  - Defense
  - Electrics
  - Farming
  - Industry
  - Smithing
  - Training
- Description: A string containing a description. This will serve as the
  description for the research in the tech menu, or the description of
  the blueprint for this research.
- Is Level Upgrade: If True, completing this research will progress the
  player to the next tech level.
- Level: The tech level that the player must have before researching.
- Money: The cost of the blueprint for this research.
- Time: base value for how many in-game hours it will take to complete
  the research at a [Research Bench](Research_Bench.md "wikilink").

### Repeats

- Repeat Mult: Multiplies the cost for each level of research.
- Repeats: How many times this topic can be researched. When this value
  is greater than 0, val1 of enabled items/buildings will represent how
  many times the research needs to be done before unlocking.

## References

References are properties of an item that are determined by other Items,
such as a characters inventory, a faction's members or a town's
residents. These are not always required and can often be left
blank. They are found on the right hand side of an Item's properties
window.

- Blueprint Item: This research is tied to a specific blueprint. For
  example, the Skeleton-Human Transformation Bible.
- The resources, typically [Artifacts](Artifacts.md "wikilink"), required
  to initiate this research.
- Enable Armour: After this research is complete, this armour will
  become craftable.
- Enable Backpack: After this research is complete, this backpack will
  become craftable.
- Enable Buildings: After this research is complete, this building will
  become available in the construction menu.
- Enable Crossbow: After this research is complete, this crossbow will
  become craftable.
- Enable Item: After this research is complete, this item will become
  craftable.
- Enable Robotics: After this research is complete, this robotic limb
  will become craftable.
- Enable Weapon Model: After this research is complete, your characters
  will be able to create weapons of this model.
- Enable Weapon Type: After this research is complete, this weapon will
  become craftable.
- Improve Buildings: Buildings that are affected by the "Building
  Improvements" attributes.
- Requirements: Research that must be completed before this research
  becomes available.

[Category:Modding](Category:Modding "wikilink")