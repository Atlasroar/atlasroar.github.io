---
date: 2024-04-20T14:44
tags:
  - kenshi
  - modding
cssclasses:
  - page-kenshi
  - center-images
---




## Facts

- Shirt/vest layer only take red and black, mesh parts have also green
  and blue available
- Color is applied over the base color the texture has. So to get pure
  color_data colors your texture needs to be light grey. If your
  texture(diffuse) has actual colors the result will be combination of
  the color wash and the base color. (Imagine dyeing a red shirt blue,
  the result would be purple).
- Red (RGB 255,0.0) is for FCS color_data file color 1, Green (RGB
  0,255,0) = color 2
- Blue (RGB 0,0,255) is for metallic parts
- Black is absence of color, white is all colors
- Yellow (RGB 255,255,0) is both green and red
- Teal (RGB 0,255,255) should technically be both color 2 and metallic
- Purple (RGB 255,0,255) should be both color 1 and metallic
- Orange would be some murky mixture of both channels, favoring the
  color 1.

Kenshi can tolerate variable changes in the color's tone, darker,
lighter etc. Having the color at full 255 means it will be washed with
pure color value from the color_data channels. If the color map value is
darker, Kenshi tries to adjust the values of the color_data to fit the
map tone.

## Step-by

1.  Finish the making of the garment, have at least it's UV map layout
    done and locked. Finish the texture layout.
2.  Open the texture in a painting program, that allows you to paint
    with pure colors. All free programs do this. Gimp recommended.
3.  You have two colors and combinations of them in your color palette:
    red and green (and blue).
4.  Draw or otherwise paint pure red on a new layer on the map (the
    original texture remains as background layer) on those spots you
    wish to be colored with the color 1 channel from a color_data file.
    Do the same with green (color 2). Usually either is 'everything
    else', but you can have black on everywhere else (== use the color
    the texture has) and just have the colors 1 and 2 be special
    decorative bits, like edges or emblems.
5.  Keep the size of the color map as small as you can. A single color
    map can be like 50x50 pixels. Of course, if you need small details
    you have to keep the color map larger.
6.  Export as .dds, compression DTX1, mipmaps enabled (Not all paint
    programs have these available, but Gimp does)
7.  Move the .dds in your mod's textures folder and link to it in the
    garment's FCS file.
8.  **Set 'don't colorize' to false on the FCS** file of the garment,
    you need to do this with all pieces (pants, top, boots etc).
9.  If you want the garment to use faction colors, you are done. But if
    you want to make several color variations of the garment, then
    you'll use the pull down menu and add 'color' (color_data) file.
    Just add any, and then replace it with a copy.
10. Set the color 1 and color 2 RGB values. You can eyeball them, or use
    a color picker and see its RGB value in your paint program. However
    you do it, you prob. have to relaunch the game several times to see
    how it looks in game in different lighting settings. (Do not forget
    to add the garment to your test start's character).

## Glossary

|                      |                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Color channel**    | Refers to either the color 1 or color 2 channel mentioned in a color_data file                                                                                                                                                                                                                                                                                                                                |
| **Color_data**       | A file type in the FCS, has two channels: color 1 (red) and color 2 (green), input in RGB values. Usually used in faction colors.                                                                                                                                                                                                                                                                             |
| **Color map**        | A RGB layout of colors. Each color (Red, green,blue) matches the layout of the actual texture (diffuse) layout of the garment. This is used to allow the garment to be colored fe. by the faction colors, or just to make several color variations of the item without the need of a new mesh or a new texture for each color variation. Works on garments only. Buildings and furniture use vertex painting. |
| **Color wash**       | A term originated in yarn dyeing, a semi-translucent color (very watery) that is either poured over or yarn is dipped in it, to generate a new color combination, a mixture of the base color of the yarn and the color wash. Tarnishing, if you will. In Kenshi all color_data colors are washes, even though they can be so dark sometimes the base color does not show much.                               |
| **Shirt/vest layer** | A characters outfit usually consists of mesh pieces (body, legs) and an undershirt. The undershirt is the shirt layer. It uses the character skin layout and is texture only. In FCS there is a separate place for shirt layer texture links. They do not get a material file.                                                                                                                                |

[Category:Modding](Category:Modding "wikilink")