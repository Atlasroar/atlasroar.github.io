---
date: 2024-04-20T14:44
tags:
  - kenshi
  - modding
cssclasses:
  - page-kenshi
  - center-images
---


Boron speaks of mesh colliders, he means the mesh collision shape with
rigid body.

### Tips by Boron

I'm going to assume you're using Blender and the images will reference
it.

Colliders can be tricky to make for buildings with interiors. You can
get away with a simple box collider for, furniture, walls, and squarey
platforms. For everything else you'll want to use mesh colliders.

### Box Colliders

Bounding box colliders can be added to objects (use boxes) in the
physics panel. Set the rigid body type to passive and select "box" as
the collision shape. ![](Bounding_Box.png "Bounding_Box.png")

### Mesh Colliders

Mesh colliders are complicated collision shapes and work well for
buildings and complex meshes. It's generally better to use mesh
colliders with well-aligned vertices than to just mash a bunch of boxes
together.

The navmesh is essentially a 2D plane, so make your mesh colliders as
planes and do your best to snap vertices together. This is particularly
important for buildings with interiors and multiple floors (below).

To make a mesh collider, set the collision shape to "mesh" in the
physics properties panel.

### Exporting Colliders

Navigate to File \> Export \> Kenshi Collision (.xml) to export your
collision shape.

Use the Kenshi Mesh and Collision Viewer to look at it if you want to
check it out.

### Doors

Use a box collider for doors and make the box a fair bit thicker than
the door. It won't entirely negate clipping issues, but giving it a
decent width should help to mitigate the issue.

### Buildings

Buildings need one collider per floor, one per set of stairs, and at
least one collider for the walls. In general, you should make clean
colliders with as little geometry as possible to get the best results.
Cutting corners will only cause issues later on - topology is important
here.

To make your collision shape, start by making a 2D plane as contiguous
geometry. For best results, make your stairs as simple quad "ramps" with
4 vertices. Once you're done, separate each floor and stair collider
into separate objects and export them. You shouldn't run into any issues
as long as the vertices of your stairs are snapped to the vertices of
each floor, like this: ![](Plane_Collider.png "Plane_Collider.png")

To calculate the navmesh properly, Kenshi needs interior triggers and
masks. The trigger is an xml file to detect when a player is inside a
building, and the mask is a mesh with the normals pointing inwards that
hides any terrain that might clip inside the building.

In my experience, interior triggers should be made from primitives (i.e.
box colliders) that conform to the interior of your building.

Stairs and upper floors often won't work at all without a trigger so
make one before testing your collision out.

Wall collision should be separate from your walkable floor collision and
assigned to a higher floor than the collision itself (e.g. floor 1 for a
floor 0 interior). Otherwise, you'll click on the wall when you're
trying to click on the floor (see the [](Building_making_tutorial.md)).

You probably don't need to bother with wall colliders for upper floors.

### Masks

Interior masks are meshes combined with trigger xml files

To make them, make a shape that conforms to the interior walls of your
mesh. Then flip the normals so that they're pointing inwards (activate
backface culling to check). Masks don't need to be too complicated but
they do need to conform well enough to hide terrain that might be
clipping into your buildings.

### Troubleshooting

If your colliders aren't working, try saving and reloading your game.
Kenshi often won't update the navmesh until you do. If you're making
edits and still running into problems, locate your collision files and
delete the .bin files with the same names. These files are what Kenshi
generates from your xml files and can be stubborn, so just yeet them
after edits and restart the game.

You can regenerate individual navmesh tiles in-game from the editor by
clicking "regenerate sector" in the Navmesh panel. This is useful if you
either don't want to save and load after placing a building or if you've
got existing buildings that you've updated the files for. Each navmesh
tile is roughly screen-sized, so make sure you center your camera on
your building so that the rotation gizmo is placed on it when you rotate
your view. Regenerating a tile only takes a second or two so you can
move around a bit and mash the regenerate button to update the navmesh.

### Complex Collisions

It's possible to do any of the following:

- Path directly into upper floors
- Path through buildings to get to other buildings
- Have split navmesh islands, so that you have to go up a floor to reach
  another spot on the same floor
- Have multiple separate stairs on one floor

Pathing directly into upper floors is tricky and you **must** snap your
collider vertices together else it either won't work or you'll have
crash-prone meshes. The two ways of doing it are:

1.  Add a "ramp" into the building that is actually multiple sets of
    stairs
2.  Snap a separate building/collider directly to the place you want to
    path into by choosing the "snaps to" option in a building and
    aligning the meshes and colliders in Blender before exporting.

[Here's a
link](https://www.reddit.com/r/Kenshi/comments/upmm4q/modular_fortresses_for_lita_done/)
to an older Reddit post with some of the complex navmesh stuff.

[Category:Wip](Category:Wip "wikilink")
[Category:Modding](Category:Modding "wikilink")