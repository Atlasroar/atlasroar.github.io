Ever wondered why your custom race has seams all over or why your
character looks flat in game?

You must have noticed the vanilla characters use grayscale normal maps,
but however you try, turning a normal map into a displacement map just
does not work right.

This is because Kenshi uses this weird GGG+R system instead of RGB+A.
What you need to do is:

1.  ) Create a normal map like you do. Tweak it until you have no seams.
    Never mind it being flat.
2.  ) Open the normal map in a sophisticated image editing software,
    that is able to divide the RGB into different channels and able to
    create an alpha mask using an image.
3.  Copy the Red channel image to a separate image
4.  Copy the Green channel and paste it over the original Red and the
    Blue channel
5.  Combine the image. You have now a grayscale image.
6.  Create a mask, or however your image editing software does it and
    create an alpha channel using the copy of the Red channel you made
    earlier.
7.  Export to .dds or open it in Gimp to export as .dds if your software
    does not convert to .dds.

The red channel being the alpha is important. Kenshi uses the black and
white data on the red/alpha channel as the displacement map.

Black = hollow White = bump

[Category:Modding](Category:Modding "wikilink")