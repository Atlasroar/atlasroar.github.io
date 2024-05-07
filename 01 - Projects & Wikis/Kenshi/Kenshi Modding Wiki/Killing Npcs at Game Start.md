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



by Cattrina

You know, sometimes you just want to restart the game but want to keep
the world states. Usually one would go about it by importing the old
save with dead characters. But what if that save file was corrupted?
This is one way to create a start where all the uniques you want, become
dead very shortly after game start.

1\) Pick up a town/nest etc. for the player character(s) to spawn in.
Technically this should work also if it is a nest very closeby the
player spawn place.

2\) Make the character-to-be-dead (fe. Seta) a resident of the town.
Make sure there is a house they can spawn in (interior and exterior
layouts match etc). Priority 5

3\) remove Seta's squads, make him wounded, like +10 on head and legs
but -80 or -100 on arms

4\) remove their AI pack, create a new Ai for them to patrol town

5\) You can rename and regear them if you want to hide the fact from the
player you are killing uniques

6\) **give Seta a food item as a death item**

7\) Create a new faction and make all the CTBDs part of that faction.

8\) Create new faction for the muggers and a new squad for that faction,
populate it, gear them up

9\) make them also residents of the town priority 5 and AI patrol town
priority 0 + AI attack enemies priority 2

10\) add them also the AI goal 'Looting corpses and food' and make it's
priority 5

11\) make the new faction hate the First Faction

These muggers will kill the CTBDs by looting their death item after
mugging them unconscious. NOTE: these two squads cannot be housemates.

[Category:Modding](Category:Modding "wikilink") [Category:Modding
Guide](Category:Modding_Guide "wikilink")