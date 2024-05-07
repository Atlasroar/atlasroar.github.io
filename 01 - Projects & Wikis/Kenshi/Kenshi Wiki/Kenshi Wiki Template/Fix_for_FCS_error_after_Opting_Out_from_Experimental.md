Because of the version differences between experimental branch and
stable branch of Kenshi an end user (subber) is not able to use mods
made in the experimental version of FCS if they are using the stable
version. The error for them occurs as odd 'dependency' which is usually
named after the mod creator's username. The mod does not load in game at
all.

When opting out from the experimental branch the mod maker (modder) gets
an error, not being able to use FCS at all. This is because the modder
has one or more mods in their Kenshi/mods folder they have opened and
saved while the experimental version was ongoing.

#### Here's the fix

Move all mods you might have saved on the experimental to another
folder. Test if FCS works, then move each back one by one and test FCS,
if you get an error, you need to revert that mod in Steam workshop to an
earlier version, sub to it yourself and replace the files in your mod on
your computer. You need to do that to each mod you saved when on
experimental.

If you created a new mod while in experimental or you made significant
changes since previous update, you have two options; either leave it as
is and put a disclaimer on the mod that it is for the experimental, or
remake the FCS files. You can use the mesh skeleton and dds files, just
copy or move them to the new mod you make to the old one's image.
Unfortunately one cannot merge two different version FCS files.

I recommend going back to experimental and taking screenshots of all
your files and subfiles, for your subber's sake it would be nice if you
recreated the files using original file string ID

Here's how: look what the original string ID is for each file and type
it down, then go make an identical file in the new mod and replace the
new string ID with the old one's string ID. This way any subber already
using your mod may keep their already built items from your mod.

[Category:FCS](Category:FCS "wikilink")
[Category:Error](Category:Error "wikilink") [Category:Forgotten
construction set](Category:Forgotten_construction_set "wikilink")