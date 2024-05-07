---
date: 2024-04-21T15:50
tags: 
cssclasses:
  - page-kenshi
  - center-images
---
[[Kenshi Modding Wiki]]
[[The FCS - A Complete Guide]]


https://lost-blog.com/in-game-editor/


Primarily, in-game editor is used to design towns and building interiors. You can access it any time by pressing Shift + F12. By and large, the three buttons you’ll need for mods are town placement, buildings, and items.

![](https://cdn.gilcdn.com/ContentMediaGenericFiles/5242705f4c88608855b586a93a665fdf-Full.webp?Expires=1713746833&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZG4uZ2lsY2RuLmNvbS8qIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzEzNzQ2ODMzfSwiSXBBZGRyZXNzIjp7IkFXUzpTb3VyY2VJcCI6Ijc1LjIyNS4xNzQuMTYxIn19fV19&Signature=Q-7KFhtu9JDtQgIc9zlhx5KVhDq032aB-DWeRThxYkjbmRNH1uy-ha9toZJV0vAVPPXe-NwN6vk5j5p2nL5kZETE-YH2oM-Ky0lOKthr-W%7EFwHeSaq-hKrh%7EDfEomeN-n0V-ozWBai8XLJpL%7EvYVIlza3F7JRhGa4IJJM4PXNKkH0VBUcfEF74W9V6p0oJvT7bAq-ufEYeNBG86UeVygiL6wogCEguKkM%7EJhFJDwBEY8XhGZRhulhA3iQvhnji2jJP1RhpI6h%7ElJECNr2LinFwgmc5d2HUpGZidV2P2loXpKhoBNeIAsSd7StWK7jQcHw6kesmIN%7EiL7q3IrQBaEoA__&Key-Pair-Id=K1FFKFZRWAZSB)

There are lots of functions here and several things to note about the editor:

- Your camera is unrestricted and you can move beyond the normal limits of your squad’s vision range. This reverts when you close the editor again.
- You must select the correct mod file before committing any changes.
- Each town has a visible radius and marker at its centre.
- Changes to leveldata (i.e. placing and removing buildings and designing new interiors) must be saved to a mod file before you close the game.

In game, each town has a marker that determines where the centre is, and a town’s data tries to fill out the buildings within that radius with NPCs. The town radius is determined by two factors:

- The town type. For instance, the radius of a village is smaller than a military outpost.
- The radius modifier. This is only needed if buildings inside a town extend past its radius.

While towns look outside their radius to see if there are any nearby buildings that should be filled, it’s considered best practice to ensure your town radius encompasses all buildings and walls. The walls (and gates) are important for the AI to determine things like where to stand during an assualt and where to wander around without leaving the town.

Buildings

The buildings list gives you access to all placeable buildings, which are built instantly. Note that, while you may modify a buildings transforms (position and orientation), moving a building too far underground can make it revert to its original position when you close and open the game. This generally takes some practice, but the rule of thumb is that a building’s door should be visible, along with part of the ramp that leads into it, like the stairs for a stormhouse.

Buildings with interiors are a little more complicated, but the crux of it is this:

- Town residents are spawned in buildings with interiors
- The residents determine the interior and exterior layouts of a given building
- A building may have 0 residents, such as a destroyed ruin with loot
- A building may have a fake or empty interior, allowing it to spawn units without a “real” interior

When you click on a building, the editor brings up the transform gizmo and extra settings. If it has an interior assigned to it in the FCS, it also displays the layout panel:

![](https://cdn.gilcdn.com/ContentMediaGenericFiles/5e5f0910eb3296af063e96fff0bf36fa-Full.webp?Expires=1713746833&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZG4uZ2lsY2RuLmNvbS8qIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzEzNzQ2ODMzfSwiSXBBZGRyZXNzIjp7IkFXUzpTb3VyY2VJcCI6Ijc1LjIyNS4xNzQuMTYxIn19fV19&Signature=Q-7KFhtu9JDtQgIc9zlhx5KVhDq032aB-DWeRThxYkjbmRNH1uy-ha9toZJV0vAVPPXe-NwN6vk5j5p2nL5kZETE-YH2oM-Ky0lOKthr-W%7EFwHeSaq-hKrh%7EDfEomeN-n0V-ozWBai8XLJpL%7EvYVIlza3F7JRhGa4IJJM4PXNKkH0VBUcfEF74W9V6p0oJvT7bAq-ufEYeNBG86UeVygiL6wogCEguKkM%7EJhFJDwBEY8XhGZRhulhA3iQvhnji2jJP1RhpI6h%7ElJECNr2LinFwgmc5d2HUpGZidV2P2loXpKhoBNeIAsSd7StWK7jQcHw6kesmIN%7EiL7q3IrQBaEoA__&Key-Pair-Id=K1FFKFZRWAZSB)

- Transform settings allow you to switch between orientation/position modes and the local/global axis.
- Interior layouts are only displayed when the interior of a building is displayed, which is determined by the interior mask assigned to the building in the FCS
- Exterior layouts are always displayed, and usually include things like signs and lights
- You have to be in interior edit mode to edit and save layouts. To edit exterior layouts, enable interior edit mode and disable “show interior”
- Layouts cannot be loaded and edited once you save your game (even if you don’t load it) to prevent bugs. In general, it’s best to launch a debug game start and design your layouts from there

Town Placement

Selecting the town placement option brings up a list of all available towns with a search field at the bottom. Any town that doesn’t yet exist in the game world will be displayed in red text. The numerical value in brackets next to each town denotes the number of instances of that town – a Waystation, for instance, is a town that is reused multiple times.

X

To place a new town marker, select a town from the list and click in the game world to place it. Then save your mod file.

To delete a town marker, navigate to the town so that the marker is on-screen. Then, select it from the town list and hit the “delete” key. You can click again instead to move a town marker.

When placing towns, it’s important to avoid placing them directly over a road to prevent AI pathing issues. Doing so tends to lead to clipping directly through geometry (like walls). However, you can place a town on top of a road as long as you add gates at either end where the road is. This will make wandering AI path through your town, following the road it’s place on.

Items

The items list brings up all placeable groups that are created in the FCS. A placeable group is a selection of randomly spawning items with a respawn cooldown. These items are the ones that populate interiors, littered around on shelves and tables.

X

tem placement groups are saved to a building’s interior like other furniture and only load when that interior is also loaded. Moreover, they’re influenced by a faction’s trade culture – which can be used to prevent certain items from spawning for certain factions.

Navmesh Tools

The navmesh is a hidden, two-dimensional mesh that tells characters where they can go and how to get there. It’s how characters navigate when they’re in the loaded area directly around the player.

X

Roads are used to navigate over long distances, often when AI characters are in the unloaded area. Each faction also has a preference setting for using (or ignoring) roads that is determined in the FCS, though when unloaded they’ll default to roads because it’s how the AI pathfinds long distances without getting stuck.

Navmesh tools in the editor allow you to rebuild parts of the navmesh and design new roads.

Don’t touch roads unless you know what you’re doing.

The road network is like a Jenga tower and breaks spontaneously. A lot.

If you’re dead set on making roads, then take it slow, design them in a new mod file (!) in case you need to revert, and restart the game to verify every change has worked before continuing. The “verify road network” function doesn’t always catch issues.

Rebuilding the navmesh is a quick way of checking your collisions are fine and generally only takes a second or two.

However, the segments that are rebuilt are pretty small – roughly the size of the screen at a “normal” view distance. The navmesh tile that is rebuilt is the one the camera is pointing at, i.e. the spot at which your rotation gizmo displays when you rotate the camera (unless you turned it off).

Quick-saving and quick-loading tends to work, too, and in general it’s easier to use that.

Terrain Features

Terrain features are the big rocks and miscellaneous features that are dotted around the game world as background noise. Features can’t be saved to mod files in the FCS.

Terrain Fog

Terrain fog (e.g. the foglands) is used to put static fog-like particle effect generators into the game world.

Fix Stuff

The magic “fix broken stuff” button. Don't Use this.