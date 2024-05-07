## How to add interior walls and doors to your building

By Cattrina May 15h 2023

You can add interior walls and doors to vanilla buildings or to a
building you made yourself. But if you want vanilla, I suggest you make
a duplicate of the vanilla building, cause none of the vanilla prefab
interior layouts will work with your new walls and doors.

ALSO NOTE: NPCs caught inside rooms like this will: a) vanish when the
region is unloaded b) do not count as prisoners c) try to follow their
leader constantly d) will run with unfathomable speed the second you
have both the interior and the exterior door open at the same time.

Sometimes when an old save is loaded on a running game the door
collisions vanish. I think this is an inbuilt mechanic to allow NPCs to
get trapped inside buildings (when not in a cage). The collision can be
refreshed by opening and closing the door, or loading the save twice in
a row.

### What needs to be done:

-

<!-- -->

- One mesh for all the walls per floor. Yes they need to be one mesh
  object. The origo of it at the crosshairs (making the walls offset
  from the center).
- One collision for the walls with doorways (no planes, all faces must
  be solid). Export as mesh collision shape.
- One mesh for each door.
- One collision for each door, collision shape box.
- Each mesh piece origo at the crosshairs.
- Each collision piece origo in line with the wall (not crosshairs).

<figure>
<img src="InteriorWallsAndDoorsCollision.png"
title="InteriorWallsAndDoorsCollision.png" />
<figcaption>InteriorWallsAndDoorsCollision.png</figcaption>
</figure>

<figure>
<img src="Wall_Collison_shape.png" title="Wall_Collison_shape.png" />
<figcaption>Wall_Collison_shape.png</figcaption>
</figure>

**Make sure none of the collisions of the house touch**. You can make
the door collision slightly smaller than the doorway. Same goes with the
interior walls, they need to NOT overlap with base collision.

This is experimental building technique and we do not know if this
messes up with AI pathfinding. So try to not make these for NPC town, or
if you do, I do not take any responsibility if you break something XD.

### FCS setup

When you have done all your mesh and collision pieces, copy them to the
buildings folder inside your mod and add them in FCS to the building's
file. Do not forget to remove the 'shares interiors with' -references.
You do not need a script for the doors. Door building parts go under
doors and the interior walls go under interior.

<figure>
<img src="InteriorWallsAndDoors_FCS.png"
title="InteriorWallsAndDoors_FCS.png" />
<figcaption>InteriorWallsAndDoors_FCS.png</figcaption>
</figure>

### Door opening values

<figure>
<img src="DoorMove.png" title="DoorMove.png" />
<figcaption>DoorMove.png</figcaption>
</figure>

[Category:WIP](Category:WIP "wikilink") [Category:Building
Meshes](Category:Building_Meshes "wikilink")
[Category:Modding](Category:Modding "wikilink")