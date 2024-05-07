

#### Blender

- Only 4 weighted bone assignments per vertex. If you have more, ogre
  will eliminate the lowest weighted one. Means: only four bones can
  affect a vertex (sliver of skin). Fe. I have a tattoo on the back of
  my hand. Moving the fingers can make the tattoo dance. Moving the
  thumb will not.
- All vertices must be assigned to at least one bone - assign vertices
  that do not need to move to the Bip01.
- Each bone must have a keyframe at the beginning and at the end of the
  animation strip.
- Use unique animation strip names. I mean it. Have fe. your own
  nominator. I, myself, have CBT at the beginning of my strip names. In
  that way if I make a chair that uses **my** basic sit 'CBTbasicSit' I
  know the game will call **MY** basic sit and not any of the dozen
  basic sits other modders have made. The more furniture makers there
  are, the more likely it is that two or more of you will use the same
  generic name for the animation. You spent hours making the animation,
  you should make sure your subber will see your hard work :)
- Do not edit or replace the main animation skeletons unless you are
  making an animation overhaul. 90% of other mods in the workshop rely
  on the vanilla basic animations. If you need to replace one animation
  in the vanilla skeleton, just make a new skeleton with just that one
  animation **with the literal same strip name** the vanilla skeleton
  does and add that to all races you want to alter. It would be good if
  the replacement you make would work in its vanilla purpose ie. no
  point replacing vanilla animation if you do not want it to be called
  whenever the vanilla one was. Also of any other mod is loaded after
  your mod in the game, the vanilla skeletons are replaced back. This is
  why it is recommended to just have your own animation file and just
  add that to every race. At least the mod loading order does not affect
  your mod.



#### FCS

- An animation file must be assigned to each sub-race you want to be
  able to use it. Common ones like sits and sleeps on furniture should
  go to all playable races. This also means a patch is required for each
  additional race in the workshop (if you want them to be able to use
  your anim).
- Having the animations in the vanilla file patch formation is strongly
  suggested. If a computer quip is to happen and Kenshi forgets what it
  was playing it will look the animation from the male_skeleton or
  female_skeleton folders. If the animation is not there, it can crash.
- Yes, female and male skeletons are similar enough for some static
  poses to work for both. But if any movement is involved, make a
  separate skeleton for both.

See also the video: [Making a Kenshi Animation, a Blender and FCS
Tutorial](https://www.youtube.com/watch?v=U0XpZUQV6CQ)

[Category:Animation](Category:Animation "wikilink")
[Category:Modding](Category:Modding "wikilink")