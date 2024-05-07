---
date: 2024-04-20T14:44
tags:
  - kenshi
  - modding
cssclasses:
  - page-kenshi
  - center-images
---



## How to make a new race

### Mesh and character body

1.  Import a vanilla character model with its skeleton into Blender (if
    they are in the same folder, the skeleton will come automatically
    when you select the mesh)
2.  Edit the mesh until you like its appearance.
    - If you are making a giant: Select both skeleton and the mesh and
      go to edit mode, scale them up
    - If you are making a non-standard race and need a tail etc. make
      your add-ons to the skeleton
3.  If you are not making a giant, or have a tail etc., skip this step.
    If you are making a non-standard race: Re-record every animation in
    the skeleton to match the new scale (this is the tedious part)
4.  Do steps 1-3 to both genders
5.  Export the mesh with the skeleton and paste them inside your mod to
    character/meshes/female_skeleton and male_skeleton folders
    respectively
6.  Open FCS and make a new race file, set its mesh to be the new
    mesh(es) you just made for both genders
7.  (Skip this step if you are making a standard race) Make a new
    animations file and add the new skeleton to that. Add that new
    animation file to the new race
8.  Make a new custom start and have a character spawn as this new race.
    Test everything works. If they do, you can stop here.
9.  For minutiae details: Edit the appearance in the start character
    editor until you are happy how the character looks like. You might
    have to adjust the editor_limits file for this race and redo this
    step a few times to get the minutiae to your liking. Fe. if you want
    special skin colors, you need to adjust the editor_limits file. Use
    notepad++ or Visual studio to edit the file.
10. Export the character body (unique name so you know which it is)
11. Navigate to your ..\Kenshi\data\character\bodies\export folder and
    move the body file you just made inside your mod's character\bodies
    folder. (If you do not have one, make one)
12. Open FCS and create a new character file. Add this new bod to the
    character. Add the new race to it. Add a stats file to your
    character. You need to adjust its strength and moving speed up a lot
    to meet the expectations of a large creature.
13. Make a new custom start or just edit the start you already made.
    Make the start have this new character.

### Skin texture

If you edited a vanilla mesh, you probably can use a vanilla skin
texture as a base. Skins can be found in the
..\Steam\steamapps\common\Kenshi\data\character\skins\human_female or
human_male (or shek) folder. The head files are in 'hu'. The head files
in human_female or human_male folders are not used at all.

1.  Open Gimp and double-click a vanilla skin texture file to open.
    Untag 'load mipmaps'
2.  Go to channels on the right side panel (next to layers) and untag
    alpha. Take a screeshot of this. DO NOT COPY SOMEONE ELSE'S TEXTURES
    AND LOAD THEM TO STEAM AS YOUR OWN!!! THIS IS ILLEGAL IN MANY
    COUNTRIES. Only vanilla files can be used like this. You may look
    what others have made, but you may not copy.
3.  Paste that to your preferred image editor as a new image. Crop it to
    be perfectly square.
4.  Do the same to the head texture.
5.  Make your changes
6.  Open them back in Gimp and export as .dds with DXT5 compression. Max
    image size 1024x1024px, recommended as 800x800. Even tho Photoshop
    and many other program can do .dds. very often they are too fancy
    for Kenshi. Kenshi does not support partial transparency and fancier
    programs very often automatically add a soft edge to your images.
    Resulting in a texture you cannot use in Kenshi.
7.  Paste the textures in their correct folders inside your mod folder
    and link to them in the race file in FCS.

[Category:WIP](Category:WIP "wikilink")
[Category:Modding](Category:Modding "wikilink")