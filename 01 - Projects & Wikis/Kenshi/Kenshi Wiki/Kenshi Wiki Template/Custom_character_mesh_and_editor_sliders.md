Bored having every character ingame looking alike? Tried editing their
face in Blender, only to realize all the editor sliders on the game
start from jaw up have vanished?

This is because all the shape keys for the face are missing. I recommend
this video <https://www.youtube.com/watch?v=ypRhJAfJXAc&t=539s> for
instructions how to add the missing keys. Timestamp: 8:59

### Basic how to

In Object data properties (triangle) under shape keys, click the +. The
first click makes the current setup a base (basis). So the mesh in its
current form becomes what everything else is compared to. Each click
on + gives a new key to add extremes.

1.  click + to add a new key
2.  name the key using the exact case sensitive form Kenshi uses (same
    names as in editor data xml file)
3.  Edit the character mesh to the extreme form for that shape key. Ie.
    if you edited eye height, move the eyes up to the highest you want
    them.
4.  move the shape key value to 1.000 (regardless if this is a low
    extreme or high extreme)
5.  click basis to go back to base
6.  repeat for every slider

And when you export the character, remember to tag shape keys along with
tangents, binormals, animation and skeleton



### Slider names

For the names of the keys look in to the editor data xml file.
Unfortunately you cannot add your own, Kenshi expects these exact ones.
Changing the name="" value does not do anything, the slider names are
hard-coded. However, you can just leave any keys out, if you do not need
them.

Some has two extremes compared to the base, so you need to make two keys
for those

**narrow_cheekbones** **wide_cheekbones**

**big_mouth**

**wide_mouth**

**wide_nose**

**long_nose**

**arch_nose**

**high_nose**

**tiltdown_nose tiltup_nose**

**low_brow** **high_brow**

**tiltup_brow tiltdown_brow**

**shallow_eyes**

**narrow_eyes close_eyes**

**tiltdown_eyes tiltup_eyes**

**high_eyes big_eyes**

**underbite overbite**

[Category:Modding](Category:Modding "wikilink") [Category:Character
mesh](Category:Character_mesh "wikilink")
[Category:Sliders](Category:Sliders "wikilink") [Category:Editor
data](Category:Editor_data "wikilink")