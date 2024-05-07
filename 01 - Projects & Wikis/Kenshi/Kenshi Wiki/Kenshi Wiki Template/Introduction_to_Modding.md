The point of this tutorial is to explain the functions and terminology
of the [](Forgotten_Construction_Set.md) (FCS).

Warning, do not use experimental version of FCS when making mods, the
users who have stable version cannot use the mods.

If you already did that, here's how to get rid of the errors: [](Fix_for_FCS_error_after_Opting_Out_from_Experimental.md)

Official documentation on using the FCS can be found
[here](Using_the_FCS.md "wikilink").

## The Start Screen

![](LoadMods.png "LoadMods.png") When the FCS is first launched, a
window will open showing the loaded files, with the game's core files on
top, and any mods in the mod folder at the bottom.

Next to each file is a checkbox, which signifies which mods will be
loaded into the editor. The mod labeled "\*ACTIVE\*" is the .mod file
that any changes will be saved to.

Mods in the lower section can be re-ordered using the up and down
buttons to the right. Mods on the bottom will overwrite any changes in
the mods above them.

To create a new mod, click the "Create new mod file" button to the
right, and a prompt will appear asking for a name. Once a name is
entered, the mod will appear in the list, and a mod folder will be
generated in Kenshi/mods.

The "DONE" button will close the start screen and open the "Game World"
window.

## Game World

![](WeaponsInGameWorld.png "WeaponsInGameWorld.png") The Game World
allows the user to navigate through the objects contained in the mod
files loaded during startup. The pane on the left contains a list of
categories which contain the individual items. The right panel shows all
of the objects contained in the selected category. Right-clicking these
objects will open a context menu, from which objects can be created,
edited, or deleted. Double-clicking an object will open its edit menu.

## The Edit Menu

All objects consist of attributes, shown on the left, and references,
shown on the right. The edit menu allows the user to modify these.
Selecting any reference or attribute will display a description of what
it does at the bottom of the window.

It is possible to open multiple objects at once.
![](EditMenu.png "EditMenu.png")

### Attributes

Attributes are values that aren't dependent on other objects. Attributes
cannot be added or removed, but can be left blank in some cases. Most
attributes vary between objects, except for the attributes under "Base",
which are contained in every object. There are three attributes under
"Base":

- Name: The name of the object. Doesn't have to be unique, but
  duplicates are not recommended.
- Object Type: The type of object, i.e. the category. Cannot be changed.
- String ID: An automatically-generated unique ID for each object,
  cannot be duplicated. If this value is changed, any instances of this
  object in saved games will become invalid.

### References

Unlike attributes, references are values that depend on other objects.
References can be added and removed. To add a reference, select a
reference to add in the drop-down menu, then click "Add". When a new
reference is added, a prompt will open asking for an appropriate object
to be selected. References can also have additional values, which can
affect how they behave. Information on what these values do can
typically be seen at the bottom of the window.

## The Toolbar

The toolbar is a collection of tools at the top of the screen. What
follows is a description of each tool, from left to right.

- Open: Opens the start screen seen after startup.
- Save: Saves current changes to the active mod file.
- Steam Workshop: Opens a prompt to upload the active mod to the Steam
  Workshop.
- Global Game Settings: Opens an edit menu for the game's base
  attributes.
- Artifacts: Opens an edit menu for the
  [Artifacts](Artifacts.md "wikilink") system.
- Cleanup: Removes obsolete data.
- Changes: Opens the Change List.
- Assets: Opens the Assets list.
- Merge Mod: Merges changes from another mod into the active mod.
- Export Mods File: Obsolete, as mods are already saved to a .mod file.
- Translations: Only available in translation mode.
- Translation Fix: Only available in translation mode.
- Open Any: Opens a mod from any file.

## Other Menus

<figure>
<img src="OtherMenus.png" title="OtherMenus.png" />
<figcaption>OtherMenus.png</figcaption>
</figure>

### Changes Menu

The changes menu displays changes made under the active mod. This
includes changes to existing objects, shown in blue, and new objects,
shown in green.

### Assets Menu

The assets menu displays a list of all external file paths referenced by
object attributes, such as meshes, textures, and collision files.

[Category:Modding](Category:Modding "wikilink")