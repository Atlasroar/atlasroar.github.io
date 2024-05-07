Edited by Cattrina 29th May 2022

For a guide to building your own city in a saved game please see the
[Guide to Building an Outpost](Guide_to_Building_an_Outpost.md "wikilink").
For guide for making dialogue see [](Dialogue_Structure_Overlook.md). For lootable items
see [Creating a Special Placeable/Lootable Item for Your
Town](Creating_a_Special_Placeable/Lootable_Item_for_Your_Town "wikilink")
and [](Vendor%20Lists.md).

**Getting started**

To find the modding tool "The [](Forgotten_Construction_Set.md)";

First you need to navigate to your Kenshi directory. The default
directory is "C:\Kenshi". However this may be different due to personal
preferences.

If purchased through Steam, you can run the game normally through steam,
and choose whether to run the game, or the editor. For manual launch,
the directory will be within the steam
folder:"C:\\...}\Steam\steamapps\common\Kenshi".

To be able to test the mod in game, you need to open the FCS separately
from within the Kenshi folder, as Steam cannot open both, the game and
FCS at the same time.

## Step 1: Creating the mod file

Inside your Kenshi directory, launch "forgotten construction set.exe".
Once you have the program loaded up, you need to create a new mod. You
do this by clicking the "New Mod" button on the load window and giving
it a name. Your new mod should appear in the lower section of the load
window checked and tagged as active. Leave all the vanilla mods listed
there (above line) as they are. Untag all other mods (below line). Press
done.

## Step 2: Modifying the newly created file

Once you have the newly created mod loaded, click on the text that says,
"Towns" on the left hand side. After you click this, you will see new
text in the box to the right. Right click in this box, and click new
item. The item editor will open. Where it says "Name" under "Base" in
the left box will be the name of the town. Edit the "TOWN" value to what
you want the name of the town to be. After this you can click on the
drop down box on the top right of the window, and you will see various
options. The main ones to note are faction and residents. After you have
edited this to your liking, save the file.

Many also prefer to just duplicate an existing file. This may be easier
for beginners, just be sure you do not leave any old residents with high
priority there (see step 5).

## Step 3: Making the town while ingame

First make sure your mod is the only one loaded in the mods tab of the
Kenshi launcher.

To begin making your town, go to the area where you want to construct
the town and hit SHIFT+F12 to open the editor. First we need to place
the town marker. Click the towns button on editor panel at the top left
of the screen and select your town. Then click on the ground where you
want the center of your town to be to place the marker. You can use the
search box at the bottom of the list to help find your town. Towns not
yet placed in the world show up as red in this list. Towns with a number
next to them indicate that multiple instances of that town have been
placed. Click the towns button again to hide this list.

Once you have placed the marker, you can begin placing the buildings and
walls down on the map. Using this editor is similar to building an
outpost in the game but with more options and placed buildings are fully
constructed when you click confirm. You need to use the buildings button
in the editor panel rather than the normal game build button to get the
extra options. The controls for the editor are as follows:

| Actions                      | Computer Controls                                           |
|------------------------------|-------------------------------------------------------------|
| Navigation                   | WASD, Arrow keys (standard controls for navigating the map) |
| Rotation                     | Mouse Wheel Click drag, or hold Ctrl and move the mouse     |
| Selection                    | Left Mouse click                                            |
| Rotating an Object           | \< and \> keys on keyboard in preview mode                  |
| Changing height of an Object | = and - keys on keyboard                                    |
| Deleting an Object           | Delete key                                                  |

Buildings can also be adjusted after they have been placed. You can
switch between movement and rotation in the transform window that
appears. You can also switch between local and global axis modes. If you
close the transform window the gizmo will disappear, but it will come
back if you select the building again.

You cannot select and adjust existing buildings when the build menu is
active, press the buildings button again to deactivate it after placing
your buildings and hitting confirm.

Press the save button on the editor panel to save your mod. Make sure
that your mod is first selected in the dropdown list next to the save
button.

## Step 4: Interiors and Exteriors

#### Interiors

Each building type has a list of interior layouts. You can either make
use of existing layouts or create your own. To load a layout just select
it in the layouts window that appears when a building is selected.
Selecting an interior here does not permanently assign the interior for
that building. See the population section below.

To create a new layout, you need to enter **Interior Edit Mode** which
is a button at the bottom of the layout window. After this you can place
furniture the same as placing buildings. You can also place items in
interior layouts using the items button on the editor panel. Once the
layout is set up as you like it, type a unique name into the box below
the list of interiors and click save. This should add your interior to
the list. You can modify existing layouts by keeping the same name when
you hit save. Exit the editor mode before placing any new interior
layouts (yes you need to exit the editor after each individual room is
done).

After you reload a game you cannot save right away on the old interior
layout name. To circumvent this, save as some other name, delete the old
name and save again with the old name. Remember to delete your temporary
interior layout name.

Don't forget to place nodes around the interior for places for
characters to stand. There are specific nodes for guards and shopkeepers
in the nodes section of the build menu. They are invisible, so you
cannot edit them later, so place them carefully and do not misclick. You
might want to save a backup layout before doing this, in case you need
to put the nodes somewhere else. If all your furniture in the interior
is coming from a mod, it might be possible to edit the leveldata's
interior layout file and delete the node. But if you are using vanilla
assets, it can be very difficult to see which item is the node.

#### Exteriors

The exteriors list in the bottom half works the same way but it is
mainly meant for shop signs, awnings and lights. You can place any other
outdoor furniture tho, but keep them very close to the building. If the
same exterior layout is used on buildings that are right next to each
other, these outdoor furniture can overlap into the neighboring
building. So front is best location for them.

## Step 5: Population

Populating your town is done in the forgotten construction set. The
building interiors are also selected here. This is all done in the town
properties window from step 2.

First set the town faction if you have not already. Select the faction
in the drop down list and click the Add button. The faction contains a
list of resident squads that the game will assign to the buildings in
your town. You can add residents specific to this town by selecting
residents in the drop down list and clicking the add button. You then
select squads to spawn from the list.

The building built in town determines which resident squad to pick by
matching interior and exterior layout names. The resident squad is
selected from the ones listed as residents for the town and secondarily
from the faction, if the town does not have corresponding squads. If
several squads have identical layout names, the game picks a squad
according to priority and then random, if priorities are the same. If no
matches for both layout names exist, the building will be empty.

And of course; if you make one letter misspell on either the squad or
interior layout, the house will be empty. So make sure they are
*exactly* the same, capital sensitive.

If a building has more than one layout option (fe, an interior layout is
shared with it), the game randomly selects one. This means any resident
listed in the town (or faction) file, which has both the chosen interior
and the exterior layout names, can spawn in the building.

If you want to ***decide exactly*** which building **the specific
squad** uses; duplicate a building's file, give it an unique name. Make
sure it does not share interiors and use that building when you build
your town and give it the unique interior and exterior layout names.
This forces the exact squad to spawn.

## Residents

Residents are squads populated with characters. Each squad is either set
to spawn in a house(building) or to be free roaming. The squads set for
houses must have a matching exterior and interior layout (see above) in
order to be able to spawn in that house. A resident squad without
available house will not spawn at all. There can only be one squad
spawned per house, unless housemates are set.

See [Character (FCS)](Character_(FCS).md "wikilink") how to edit individual
characters,

### Housemates

A housemate is a NPC squad, that habits(spawns in) the same house
another squad inhabits. They can belong to another faction (enemies will
fight) and have a separate vendor list inventory. Housemates are added
in the squad level from the drop down menu. The same way slaves or
prisoners would, but housemates do not follow the main squad's leader.
The house (interior and exterior layout) is picked by the main squad's
specifics.

*Todo: Creating factions, squads and characters.*

## Notes

Population only occurs on a new game. To quickly test your town you can
either create a new game start in the construction set to spawn in your
new town, or import a save game with your character in the town's
location.

If you started with a saved game that contained a player built outpost,
some of that information may be saved in the mod file so it is generally
best to start with a fresh new game when creating towns.

[Category:Modding](Category:Modding "wikilink") [Category:Town
making](Category:Town_making "wikilink")