

### To make a custom head skin texture variations for the existing vanilla mesh

I assume you have already made a race file for your custom race and
added it to a race group (fe humans, shek, your own) and you have
installed and opened Gimp.

NOTE: the texture files in the **heads** folder are wrong. Edit only the
files in human_male or human_female etc. folders.

#### STEP 1 - Create head variation files for your custom race

When opening your race file, duplicate all head files you wish to
replace with a custom texture. Remove all head files you do not want to
be available for your race.
![](SkinTutorialFCSHeads.png "SkinTutorialFCSHeads.png") Open one of the
variations and copy the texture map path
![](SkinTutorialFCSCopypath.png "SkinTutorialFCSCopypath.png")

Open your computer's file manager and navigate to your Kenshi folder
(usually C:\Program Filesx86\Steam\steamapps\common\Kenshi)

And edit the path by pasting the copied texture map path at the end of
it

so it looks like:

C:\Program
Filesx86\Steam\steamapps\common\Kenshi.\data\character\skins\human_female\human_female_head_variant6_diffuse_HI.dds

Remove the . away from between the Kenshi and \data

Then hit enter it takes a while, but Gimp is opening the file. Remove
the x from the Load mipmaps and hit OK.
![](SkinTutorialNoLoadMipmaps.png "SkinTutorialNoLoadMipmaps.png")

#### STEP 2 - Removing transparency

Now a warning. The image you open has transparency. I am going to show
you how to remove it, BUT USE IT ONLY ON VANILLA TEXTURES or TEXTURES
YOU HAVE THE CREATOR'S PERMISSION TO EDIT. This a copy rights thing. Do
not edit files you haven't got permission to edit.

How to remove transparency from dds files: Open the dds file on Gimp, go
to Layer - Transparency - Threshold Alpha - make it zero

I'M SERIOUS DO THIS ONLY TO LEARN. DO NOT ALTER OTHER PEOPLE'S WORK AND
PASS IT ON AS YOUR OWN.

#### STEP 3 - Edit the file and add transparency, export as .dds

Do your edits and then **add transparency back**. Make sure it has an
active alpha layer (Layer - Transparency). The eye will have 0
transparency, select it and then invert selection. Pick eraser tool,
make it 5000 pixels wide and opacity to 90. Move mouse cursor on the
characters nose and hit enter. Export as .dds and DTX5 compression,
generate mipmaps.

#### STEP 4 - Correct folder path for the file

Move the file you made to a heads folder in your mod folder. If you are
making **alternate faces for vanilla characters** the folder path needs
to be exact: character - skins - human_female
.\mods\yourmodname\character\skins\human_female\filename.dds

If you are making a custom race the path is:
.\mods\yourmodname\character\skins\\**YourRaceName**\filename.dds

#### STEP 5 - Replace each variation texture map path

Replace each variation texture map path with the correct link
referencing where your new texture is. For each variation a different
texture map.

[Category:Modding](Category:Modding "wikilink")
[Category:Skin](Category:Skin "wikilink")
[Category:Race](Category:Race "wikilink") [Category:Custom
skin](Category:Custom_skin "wikilink") [Category:Custom
race](Category:Custom_race "wikilink")