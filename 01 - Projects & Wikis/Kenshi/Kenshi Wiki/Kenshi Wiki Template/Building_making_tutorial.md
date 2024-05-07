This tutorial gives you an overlook on the process how to create
buildings in a 3D modeling program, such as Blender, and make them work
in Kenshi. This is based on my (Cattrina) personal experiences and
discussions with other modders. It is not a bible. If you find any
issue, mistake or lack, please contact me via Kenshi Official Discord.

### Basics

To test your building in world, first make a save and then load the save
after you have built the house. This ensures all collisions and doors
are calculated correctly.

Making a tower in Kenshi is like building a tall cake. **Each level
exactly the same thickness.** Each slice of cake gets its own interior,
exterior mesh, floor and ceiling meshes. But the compilation needs to
account to exactly same height (or the very least the floor
mesh&collision at correct level). Otherwise the floor toggle on the game
UI might not work correctly. You might get away with odd level/floor
heights, but it is always best to stick to vanilla measures if you do
not have the actual need for different/not uniform floor heights.

Exteriors and Blacks are listed as parts and interiors, stairs and
floors and ceilings as interiors.

TIP **only the ground floor exterior walls need collision.** Floors
above need only black as/with collision (so characters won't walk
through walls and fall out. If you decide to not use blacks on top
floors, then the interior wall file needs to have a separate collision.

You might want to make sure none of the collisions you make overlap. I
mean not a nanometer. They kinda need to be slightly apart. If they
overlap the game may crash. This has happened to me often, but others
say they have no issue with overlap. So I guess it is more of a computer
issue. But you will never know what computers your mod users have. This
is a good thing to remember, if you suddenly start getting feedback from
players that their game crashes. Or, you might never get a single
player, who has overlap issues.

### About ceilings and floors

In real life the bottom of the floor above me is my ceiling. But in
Kenshi ceiling and floor are two different meshes. This is because for
ease of playing the top part of the ceiling needs to be invisible, so
the player can see in. This is achieved by making the ceiling an
one-sided plane. The ceiling has no collision. Other option is to make
the ceiling a part of the interior mesh, but that means walls and the
ceiling would have the same material file (texture).

**TIP**: Best setup is to have your floor lvl a millimeter higher than
vanilla (because tall characters tend to have their feet sunk in the
floor in some vanilla houses) and the collision a millimeter higher than
the floor surface. Floor collision is either a **flat cube** with the
collision shape **box**, or a plane with collision shape mesh, or a
complex mesh with a hole for the stairs with collision shape mesh.
Interior ceilings are called from the same level they belong to.

The COLLISION for a floor goes to the black/black upper in the EXTERIOR
parts. The floor is not rendered when no-one is on the level. So if the
collision is in the floor mesh, you cannot navigate in the level when
only the black is showing. Ground floor collision is part of the base
file.

NOTE: I usually put my floor collision inside the same lvl black as a
separate link. But you will notice many vanilla buildings have the floor
collision in the interior file of the **previous** floor. This did not
work with my brain, it was better for my understanding to have it in the
black of the same floor. But you do you, whatever is better for your
brain. Just use the same method always, so you won't confuse yourself.
The main thing is the next floor's/lvl's collision must be clickable
when that room is still in its black state. If you put the collision in
that level's floor, it is not rendered when black.

### Doors

The door move distance is in the door part itself. If you are making,
let's say a huge building, you need to also adjust the door move
distance.

<s>Doors need also very specific script (xml) to work. So far I have
been unable to make a custom door script, so I just use the vanilla door
collision.</s> Turns out the game automatically assigns all mesh items
the correct script when loading the mod in to the game automatically.
All you need to do, is to list the door in the door section inside the
house file in FCS and have it a proper collision. Kindrad also recommend
making the door collision vastly thicker than the door. This is because
the NPCs often clip through the doors and having the collision thicker
helps with this. I have not tested if this will cause the overlap crash.
I have a new computer now and this has not crashed yet.

### Making a custom collision

Try to make your collision as cube-like as possible. Use the cube
primitive, do not use a sphere, triangle, a plane or any other shape to
make your collision. Start with a cube. Collision should have only the
minimal amount of vertices. Use collision shape 'box' as often as you
can. That is the easiest shape for the engine. Others have also made the
plane to work. So if it works for you, it is good to use. Use collision
shape mesh for openings (like floors and doorways) and stairs. The origo
for stairs is at crosshairs, for floors at the walking level.

To make a collision with an walk-through opening, use collision shape
'mesh'. Windows do not need to be walk-through.

For floors you need **a cube that is flat**, collision shape **box, or a
plane** with collision shape **mesh**. You need to position it on top of
the floor mesh, so it almost touches the floor surface. The origo of the
floor **collision** being slightly on the floor surface. If the origo
resides any lower, the character sinks into the floor. Many use the
plane shape for this reason as a collision. If you try the plane and it
does not work, it may be because of you using the vanilla import/export
plugin[. Use
IO_Continued](https://github.com/Kindrad/Kenshi_IO_Continued) instead.

DO NOTE: the floor **mesh**'s origo needs to be in the foundation level,
at the XYZ crosshair. If not, the alignment and placing of the mesh will
be in the wrong place.

Do not rename a collision file in the file explorer. The name of the
mesh is part of the coll file data and if you change that Kenshi's
engine cannot read it. The result is character sinking though the floor.
(Luckily no crashes this time). If you need to rename it just re-export
it with the correct name.

You might want to make sure none of the collisions you make overlap. I
mean not a nanometer. They need to be slightly apart. If they overlap
the game may crash. See my tutorial video Kenshi Furniture Tutorial:
Custom Collision for step by step how to make collisions
<https://www.youtube.com/watch?v=ng0qJcjKbco>

The COLLISION xml link for a floor goes to the black upper in the
EXTERIOR part of the previous floor. So floor 1 collision goes to
exterior part BLACK UPPER for floor 0. And floor 2 collision goes to
exterior part BLACK for floor 1 etc.

see also Boron's notes about building collisions [](Buildings%20Collision%20&%20Navmesh.md)

### The Mask and Mask Trigger

The Mask is a special mesh and collision script combination, it triggers
the terrain to vanish upon contact with a player character. It also
controls weather, making sure it does not rain or sandblast indoors.
Mask&trigger DO NOT track character entry to the building and the
visibility of the interiors, the Black handles that. Mask need to be 3D,
so **all sides closed, no openings, all vertices connected to their
neighbor.**

**Mask collision size and shape affects the volume where the character
is considered to be inside the building. The mask covers the entire
house,** from 1st floor to roof**,** blacks cover the individual floor
where a character can go**.** **Use as simple geometry as you can.** If
you cannot use a box, use a pentagon etc. For odd shaped houses (imagine
a hour glass shape) you kinda need to make a mask that shaped too, cause
otherwise you'd see no rain on the level where the narrowing is, when
you stand outside and look at the house in rain.

**Mask Collision:**

Step 1

Just create a simple primitive (ie box, pentagon) that encompasses the
interior of your building, especially covering the entrance. You can add
a few loops to better shape it, but keep them at minimum. Sometimes
extra flaps framing the doorway can be used. It is better if you can
make it work without the flaps, but if nothing else works, do the flaps.
I (Cattrina) have had builds where nothing else made the game understand
my character walked indoors, but those were really odd shaped buildings
(a pyramid, leaning tower). ![](Flaps.png "Flaps.png")Step 2

Add collision to it. Export it as xml. You do not need to add a [](Mask_Trigger_Collision_Script.md),
this is needed only if you want other settings than default values. 99%
of builds are fine with default. Adding a Mask Trigger Collision Script
currently requires your mesh shape to be square or rextangular, so using
vanilla values allows you to use more complex shapes.

**Mask Mesh:**

Take a duplicate of the mask object, edit and turn the normals to face
inwards (turn collision off). Export as normal mesh.

The mask is called from level 0

Mask mesh and trigger coll (xml) **do not need to be identical!** I just
offered this option so you do not have to make another mesh item from
scratch, if you do not want to.

The mask and trigger collision bottom needs to be under floor collision.
Otherwise the player cannot place objects on the floor.



### The Black and Black upper

Kenshi uses interesting tactics to reduce engine load: it renders the
furniture inside only if a player character is inside the building.
However if the door is open, the player could see in and see there's no
furniture. This is solved by a room sized black mesh AKA 'darkness'
preventing the player looking in a building. I think this is also part
why there are such small windows on the buildings. The blacks are called
from the previous floor.

These are not just to hide the fact that there are no furniture rendered
when looking from outside in, they also turn automatically into interior
collision. So make sure your blacks are snug to the walls, have a door
opening and a proper collision xml.

Blacks go to the exterior parts. Only level 0 has upper and lower, all
other floors have only one black mesh. Blacks are always rendered, but
turned invisible when someone is in the level. The mask covers the
entire house, from 1st floor to roof**, blacks cover the individual
floor where a character can go.**

NOTE: I usually put my floor collision inside the same floor black as a
separate link. But you will notice many vanilla buildings have the floor
collision in the interior file of the **previous** floor. This did not
work with my brain, it was better for my understanding to have it in the
black of the same floor. But you do you, whatever is better for your
brain. Just use the same method always, so you won't confuse yourself.
The main thing is the next floor's/lvl's collision must be clickable
when that room is still in its black state. If you put the collision in
that level's floor, it is not rendered when black.

**TIP**: Kenshi uses the black part as a collision to detect when the
character leaves or enters the building, or a floor. So it is important
the blacks have a collision file each.


=== What part on which level ===

For me as a Finn it always causes confusion with the floor numbering, as
here in Finland first floor is the one you step into, but it's ground
floor in Kenshi. I have however noticed super odd floor numbering in
vanilla buildings. You might get more confused if you look vanilla
buildings for clues.

The building level is set to every separate sub-part too. So if you make
an interior part with three other parts included in it, all four need to
be called from the same level.

***Rule: everything player sees when char is in that floor is called
from that level. Including blacks that hide previous floor. Exteriors
are called from the next level.***

> **Level 4 = fourth floor (four stairs up) NOTE: Kenshi does not allow
> true floors above lvl 2 if you need more, make two 'floors' per lvl)**
>
> As Exterior parts
>
> - ceiling between floors 4-5
> - exterior walls for floor 3
> - black for floor 3 with floor 4 floor collision xml
>
> As Interior parts
>
> - interior walls for floor 4
> - the floor 4 mesh, no collision
> - stairs & their collision for lvl 4

> **Level 3 = third floor (three stairs up) NOTE: Kenshi does not allow
> true floors above lvl 2 if you need more, make two 'floors' per lvl)**
>
> As Exterior parts
>
> - ceiling between floors 3-4
> - exterior walls for floor 2
> - black for floor 2 with floor 3 floor collision xml
>
> As Interior parts
>
> - interior walls for floor 3
> - the floor 3 mesh, no collision
> - stairs & their collision for lvl 3-4

> **Level 2 = second floor (two stairs up) NOTE: last actual lvl
> possible**
>
> As Exterior parts
>
> - ceiling between floors 2-3
> - exterior walls for floor 1
> - black for lvl 1 with lvl 2 floor collision xml
>
> As Interior parts
>
> - interior walls for floor 2 (no need for collision)
> - the floor 2 mesh, no collision
> - stairs & their collision for lvl 2-3

> **Level 1 = first floor (one stairs up)**
>
> As Exterior parts
>
> - ceiling between floors 1-2
> - exterior walls for ground floor + collision (This prevents people
>   from falling through the wall)
> - black upper for lvl 0 with lvl 1 floor collision xml
>
> As Interior parts
>
> - interior walls for floor 1 (no need for collision)
> - the floor 1 mesh, no collision
> - stairs & their collision for lvl 1-2

<figure>
<img src="ExteriorToLVLAbove.png" title="ExteriorToLVLAbove.png" />
<figcaption>ExteriorToLVLAbove.png</figcaption>
</figure>

> L**evel 0 = base, ground level**
>
> As Exterior parts
>
> - the foundation mesh & collision (base) this collision acts as the
>   ground floor walking surface
> - **no** exterior walls!
> - black lower for floor 0 (This is for the doorway to show black + it
>   acts as the walking in trigger collision, no user made collision,
>   Kenshi's engine handles this)
>
> As Interior MASK
>
> - MASK - a collision with special script to trigger when characters
>   walk in, hides terrain, does not trigger room arrival
>
> As Interior parts
>
> - interior walls for ground floor
> - stairs & their collision for lvl 0-1
>
> As Door
>
> - front door - a collision with special script to open door
> - the floor 0 mesh, no collision



### Troubleshooting

#### Why doesn't my game load?

Make sure you have all the collisions (xml) in the same exact case
sensitive form you have on your file. Sometimes when I do some re-edits
and save the collision again I accidentally save it with slightly wrong
name. That will result your game trying to pull the collision but
cannot, bc the collision does not exist. That will result to an endless
loading upon the game start.

The other reason might be Kenshi does not like the collision to be
linked in that building part. Try moving the collision to the root file.

FIX: you need to find what collision link is misspelled. And/or make
sure the actual xml file is in the correct folder.

Third reason; your interior or exterior collisions touch in the game
space.

FIX: make sure interior and exterior collisions do not touch in Blender
(then they won't touch in the game either).

#### Why does my walls look like they exploded ( a graphics malfunction)

You have one or more mesh faces occupying the same graphical space.
Usually the interior and exterior being exactly identical, only the
other its normals flipped. Where in more modern graphic engines this
causes only texture flickering, in Kenshi it causes havoc.

FIX: To avoid this make the interior mesh smaller by x and y axis. Z
needs to be the same unless you want gaps between your stories.


#### Why does the game crash?

![](CollisionOverlap.png "CollisionOverlap.png") Many things can cause
this, one being: You have two or more collisions overlapping. Usually
your wall collision overlapping with the floor collision.

FIX: Make sure when you create your building, that you keep all pieces
separate.

Crashes are notoriously hard to figure out, as same issue may work
today, but won't load properly the next. Good luck.



#### Why does my character sink through the floor, or walk through walls?

- No collision link on the correct black mesh or base mesh file in FCS
  FIX: add the link
- The collision's origo is not high enough. FIX: when making the
  collision, move and resize it in object mode and make sure yellow dot
  is on floor mesh surface level. ***Floor mesh origo at xyz crosshairs,
  floor coll origo at walking surface.***
- The collision is wrongly shaped, too small, misaligned or it has a
  hole (missing normals) on its surface FIX: make sure the collision
  size, shape and position matches the floor and it does not have any
  unwanted holes.
- Collision xml filename has been changed via windows file explorer
  (double-right-clicked and rename chosen). FIX: re-export with correct
  name.
- The collision you exported is a two-dimensional item and you used
  IO_Continued or vanilla xml exporter. FIX: make your collision mesh 3
  dimensional. Yes ALL edges need to meet another edge.



#### Why my character cannot enter the building I made?

- There is a collision in the way TIP: it can be also the
  ground/foliage!
  - 1\) Make sure you made **both** the base and the wall collision as
    collision shape 'mesh' with an opening for a door
  - 2\) Is the doorway opening large enough?
  - 3\) Is there a correct collision link in the correct story level?
  - 4\) Are both your blacks the correct size?
  - 5\) Are mask mesh and trigger xml identical in size, shape and
    location?
  - 6\) Is the doorway too high for the character? FIX: lower the
    building or add a ramp or stairs.
- The pathfinding cannot find the doorway
  - 1\) Is a door closed? Is there something blocking the way? FIX:
    remove obstacle and/or rebuild navmesh (shift+F11)
  - 2\) Is there a properly navigable path? If you used a ramp, does the
    ramp have collision and is it set to 'walkable'? Is the collision of
    the ramp aligned correctly (origo on surface)?
  - 3\) Is there a gap between floor collision and ramp/stairs
    collision?

#### Why my building has gaps between levels?

- Your story walls are too short. Maybe you resized them and forgot the
  edges need to align with lower and above floors.
- Is an entire floor wall missing? Make sure you have a correct mesh
  called from correct level and that it has the normals correct way out.


==== Why is there a invisible thing around my building that makes the
ground vanish? ==== That's the base collision. It's purpose is to get
rid of the foliage and ground mesh from overlapping the floor.

Either your base collision is too large or its center is not aligned
with the base's center. A collision's origo does not have to be at
crosshairs. Just make sure the collision covers the base exactly on all
dimensions.

FIX: resize or move the collision mesh in Blender to fit the base.

[Category:Modding](Category:Modding "wikilink")
[Category:Buildings](Category:Buildings "wikilink")
[Category:WIP](Category:WIP "wikilink")