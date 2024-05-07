![](ShekWithWarhammer.png "ShekWithWarhammer.png") The purpose of this
tutorial is to explain the process behind adding custom weapons to the
game using the [](Forgotten_Construction_Set.md). The goal is to add a war
hammer to the game, as seen in the image.

## Requirements

Before starting, a mesh is required for the weapon. Since mesh creation
will not be covered in this tutorial, the war hammer mesh can be
[downloaded
here.](https://kenshi-modding-files.s3.amazonaws.com/KenshiCustomWeapon.zip)

When making a mesh from scratch, it is important to remember that the
weapon will be held at the mesh's
origin.![](WeaponsInGameWorld.png "WeaponsInGameWorld.png")

## Adding The Weapon

Open up the Forgotten Construction Set and create a new mod.

In the Game World window, navigate to the Items\>Weapons category. Add a
new
weapon.![](RecommendedWarhammerAttributes.png "RecommendedWarhammerAttributes.png")
Fill out all of the weapon's attributes. A screenshot of recommended
values can be seen on the right, however experimentation is encouraged.
For a detailed explanation as to what each attribute does, see
[Weapons](Weapons_(FCS).md "wikilink").

### Adding a mesh to the weapon

The FCS can only read files that have been placed in the Kenshi folder,
so any files that the mod will reference, such as the weapon's .mesh
file, must be placed in the same folder as the .mod file.

In the "Files" section of the attributes menu, click on the "..." button
next to the "Bare Sword" attribute and navigate to the .mesh file. Do
the same for "Mesh".

Weapons of similar types typically use the same collision files, so for
the "Physics File" attribute, navigate to
"Kenshi/data/items/weapons/phs/chopper01.xml". Without a physics file,
it will be impossible for the player to select the dropped weapon
in-game.

At this point, the weapon should be ready for use, however there is
currently no way for the player to obtain it in normal gameplay.

### Creating a new research

![](WarhammerResearch.png "WarhammerResearch.png") All weapon types have
to be researched before they can be crafted. Navigate to the "Research"
category and create a new research.

The screenshot to the right provides the recommended values for this
tutorial, however experimentation is recommended. For an explanation of
each attribute and reference, see [Research](Research_(FCS).md "wikilink").

The two references here are very important. The first is "Enable Weapon
Type", which makes it possible for the player to craft the selected
weapon when the research is complete. The next is "Requirements", which
defines prerequisite research.

At this point, the mod should be ready for use in-game.

[Category:Modding](Category:Modding "wikilink")