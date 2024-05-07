There are two methods to teleport in Kenshi using furniture: 1)
camera-teleporting and 2) furniture-teleporting

Both having the same problem: one cannot teleport to unrendered/inactive
regions or rooms

**Camera-teleporting** is when you have one PC at the chair, that has
use range 99999. You focus the camera to the guy next to the chair,
select another character and sit on the chair. This works perfectly, but
its usage is counterintuitive as the natural way to use a teleport is
like using a lift: you go in the lift, press a button and then get
transported to another floor. Camera-teleporting would be: your friend
goes to floor 2. You then press the button your friend looks at and
voilá you manifest next to your friend.

**Furniture-teleporting** is when you sit on a chair, which origo is far
away. It also has use range 99999 but the benefits with this is you do
not need to have a PC at the exact origo position, as long as the PC is
in the same region as the chair's origo is.

Upside, you can make access to secret places inaccessible with other
means.

Downside of this is a bit hassle setting up the teleporter. Also one
cannot discover teleports by walking to them, if you do not happen to
already have a PC on the same region. This method suits best for small
distance teleporting.

#### This is just a collection of notes from my testing furniture-teleporting.

You can make a chair that has an origo tens of thousands of meters away
from the mesh, making effectively the teleporting character move at the
origo upon sitting the chair. The problem with this is the fact that
**an object is rendered by the region where the origo is.** Which means,
if the player did not already have a character at the region where the
origo is, the chair would be non-existent.

So far this teleporting seems to function only the direction of positive
axis. I tried moving the chair mesh to negative z (so one could tp up)
but negative positions do not work for the collision. Which would mean
only tping down with natural orientation. Of course one can set it up
rotating it upside down with ingame editor and repositioning it.
Naturally that is way too cumbersome for players to build them, but if
you are making Goa'uld ring teleporters in your mother ship as a part of
leveldata that would work fine.

The characaters would not register that as a path, so the NPCs would
just be stuck on first floor. Not really possible to spawn them on upper
floors.

EDIT: after testing it looks like the characters favor the stairs, if
any, to sit on a chair on another floor (a ring teleporter's origo would
be in another floor).

[Category:Modding](Category:Modding "wikilink")