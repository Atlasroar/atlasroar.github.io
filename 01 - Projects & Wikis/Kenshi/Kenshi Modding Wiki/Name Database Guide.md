---
date: 2024-04-20T14:44
tags:
  - kenshi
  - modding
cssclasses:
  - page-kenshi
  - center-images
---
[[Kenshi Modding Wiki]]


Courtesy to Shidan

# Basics

- Can not be set as general name database for a race, needs to be set
  separately **per** each **character**.
- You can have several word swaps on the character name slot
- 'Named' to false

Use word swaps, manually setting the name of a character to a word swap
name, fe, /CBTSHEKNAMES/, and set the 'Named' to false so they use the
word swap name. Try to make the word swap names unique, in case other
modders use the same word swap name. I use in mods my initials CBT in
front. Do note, that this is really cumbersome, you cannot really copy a
list of names from somewhere and paste it, you need to insert every name
in its own row one by one.

**The word swap can have any conditions applied, fe. gender, race,
faction.** Which means you can make a one word swap database for all
races, but it would be the same amount of work anyways than making
separate word swaps. It depends which you find easier, to swap all
character names to /CBTUSEMYDATABASE/ and just adjusting the names
inside the word swap into categories, or having different word swaps.

You need to make a new word swap file per every character you want to
use a different name database. All characters using the same database
have the same word swap in the name. Do note, that in that case it is
very possible to have one or more identically named characters appear in
the game (as if this is not already happening in vanilla). To minimize
this, you should have quite a large database. Also you will have a list
of identically named characters in the character list, which makes it
harder to know which character is which. Additionally you cannot use any
of the identical characters in dialogues as interjectors with 'is
character' enum. Well it would make the picking of the character from
the drop down list very hard. Unless you have saved its file number in
an excel sheet that is.

BUT you can make nested lists, fe, you have a horse that is black. You
can make a larger non-color-based TRADITIONALHORSENAMES swap and a
smaller all black-color related names swaplist like 'Blackie', 'Sable'
etc, and have one of the black name options be exactly
/TRADITIONALHORSENAMES/. In that way if none of the black names were
selected, the game engine would just pick one of the larger non-color
names. Naming the horse character /BLACKHORSENAMES/ would then result
either one of the black names or one of the non-color names.

In my horse example I would have to ensure the horse would actually be
black coated to match the name. But that is for another tutorial.

You should also only do this to **new custom characters** you introduce
with your mod. Otherwise it will conflict with a custom name database
someone else might have made for vanilla characters. **All custom name
databases for vanilla characters need to be a standalone mod** an user
can pick and choose from. Do not include vanilla characters custom name
databases as a part of a mod that also adds other things. Give your
subber the option of choice.

# How to generate pseudo-random names

This works best for the droids, as they can have any letter and number
combination. This could be done for the organics too using syllables.
But no-one knows what words that would make. You would have to be very
careful not to create fe, 'mom-suk-er' or worse as an option.

You can have several wordswaps within one name row. See image. Fe. you
could use it to generate /FIRSTNAME/
/LASTNAME/![](DroidNameRandomizer.png "DroidNameRandomizer.png")

Here's one of the wordswap files: ![](INITIAL1.png "INITIAL1.png")

Here's how the example word swap list looks like:

(of course for the actual mod it would be better to have all of these to
be uniquely named fe. CBTINITIAL1) ![](WordSwaps.png "WordSwaps.png")

[Category:Modding](Category:Modding "wikilink") [Category:Custom name
database](Category:Custom_name_database "wikilink")