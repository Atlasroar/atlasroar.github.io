*This page is work in progress, I report here whenever I have new info -
Cattrina*

Kenshi uses semi-custom scripting language called Particle Universe. The
ending .pu.

The cool part of .pu is you can just edit it with any text editor, like
notepad, and then after finishing you can just rename it as .pu and it
works.

There is, however, a visual particle editor available here: [External
forum with download
link](https://forums.ogre3d.org/viewtopic.php?t=81206)

It comes with several script examples



### Setup for particle effects

In your mod's folder create a new folder called particles (lowercase).
Inside particles folder create three folders called textures, materials
and scripts (all lowercase).

In the **textures** folder goes the texture you want each particle to
have. Fe. if you want to have autumn leaves falling there goes the
picture of the leaf in png format.

In the **scripts** folder goes the .pu file.

In the **materials** folder you set up the marriage of the script and
texture. Save as .txt and when done change the .txt ending to .material.

`material falling_leaves// exact material name, called in the .pu file`

`{`

`   technique`

`   {`

`       pass`

`       {`

`           vertex_program_ref Basic_Coloured_Texture_VP {}`

`           fragment_program_ref Basic_Texture_FP {}`

`           lighting off //full bright off `

`           scene_blend alpha_blend //allows transparency`

`           depth_write off //double side material!!`

`           cull_hardware none`

`           texture_unit autumnleaf.png //the image file in textures folder`

`           {`

`               texture_alias autumnleaf.png`

`               texture autumnleaf.png`

`               tex_address_mode clamp`

`           }`

`       }`

`   }`

`}`

[Category:Modding](Category:Modding "wikilink")