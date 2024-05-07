This article is a part of the [](Dialogue_Structure_Overlook.md) overlook guide.

# How to make the text inside the dialogue to stand out?

Sometimes when you are creating a long conversation, you might want to
highlight some words to make them stand out.

Here are some options what you can do:

### Creative typing

You can use the entirety of your keyboard. Emphasis can be done putting
symbols around a word, for example: \*text\*, -text- or even @text@. You
can use also capital letters, just remember capitalizing is considered
shouting. /ANYWORD/ is reserved for the text swaps, so do not use /+caps
for emphasis. Just be consistent whatever emphasis method you pick. Do
not mix it up.

*"You -might- think I am odd, but -I- know I am the SANEST OF ALL!"*

### Color

You can just slap a hex color code (fe \#66ff66) in front of a word and
it works. No brackets needed, just the hashtag. Just remember, there are
different UI color schemes available, so it is best to use universally
visible colors (for the not colorblind).

It is also recommended you use word swaps for your colors. It will just
not help you remember which is which, but it also allows the people with
color issues to change them to something they can see properly.

How to use: just type the hex in front the word to be recolored, or,
preferably the color word swap like: *"Wouldn't /BLOODRED/ you like to
see that".*

<s>Yes, you need to put the hex or word swap name **in front of every
word you want to color** as there is no brackets you can put around the
entire sentence. If you know you are gonna need to repeat one specific
sentence in that color, make a separate word swap for it so you only
need to type the hexes once. fe, \#821400 this \#821400 darn \#821400
map and use it in the dialogue *"I can't believe it /THISMAP/ gets every
landmark wrong!"*</s>

Upon more tests it looks like the color tends to want to color
everything after in the same dialogue. You might have to return to
original color by recoloring the text with the hex of the normal text
color. For vanilla it is \#140805, for Dark UI it is \#9c9c9c. This also
means the mod cannot be used with both UIs, you must choose. Altho you
could make the NPC ask in the beginning which UI the player has and then
use 'use always the same answer' in the word swap for the main color.
Cumbersome and immersion breaking, but no need to make two mods.

I tested \</\>, \</#\>, /# and \# as a possible end brackets, but the
ones with \# turned the text green XD. Also tested three spaces and a
empty row, does nothing. Same for unicode control characters fe. ^@.

Colors that work for both vanilla and dark UI:

- Blood red \#821400
- Navy blue \#253c97
- Forest green \#36660e (on the verge of visibility on vanilla)
- Pure white \#FFFFFF
- Rusty red \#873711
- Dark purple \#541484 (on the verge of visibility on Dark UI)

<figure>
<img src="DialogueColors.png" title="DialogueColors.png" />
<figcaption>DialogueColors.png</figcaption>
</figure>

As you can see pure white is the best color option for either UI color
scheme for emphasis.

Avoid black, grey, greyish brown, too dark and too light, as well as too
bright colors. Yellows and greens tend to be hard to read on vanilla and
blues and purples on Dark UI. Pick a medium light tone that is slightly
muted.

### Bold and Italics

Unfortunately there is no bolding or italizing text in vanilla Kenshi.

We have tried

- html \<i\>\</i\>
- ascii code \u0016
- putting words inside asterixes and underscores (\*text\* _ text _)
- lua formatting \<i\>\</\>
- square brackets \[i\]\[/i\]
- swirly brackers {i}{\i}

the last two resulting in error.

There is a rumor, that we would need a lua script to add this function
and re_kenshi to load this script to the game. Which would make it
horribly cumbersome for the end user just to see italics.

[Category:Modding](Category:Modding "wikilink")
[Category:Dialogue](Category:Dialogue "wikilink")