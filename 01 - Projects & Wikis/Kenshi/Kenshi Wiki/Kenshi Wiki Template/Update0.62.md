**Version 0.62**

__TOC__

Here we go, my main focus for this update has been to fix the worst
problems rather than adding new stuff. The biggest fix was a big memory
leak, which should fix, or at least reduce the dreaded “Super crash”
that people were getting after long play sessions. In the background Sam
is working on the pathfinder overhaul that should fix all the
movement/pathing related bugs, so hold off with any movement based bug
reports until then. He should have that ready in about a month. Regular
updates can still happen before then though. As usual an import to a new
game world is recommended but not required.

## 0.62.0

- Your base will get randomly assaulted by dust bandits, starving
  bandits, and sometimes cannibals.
- Sometimes the hungry bandits will try to rob you and take all your
  resources. Lock up your storage boxes in a safe building!
- Added the Splinting feature back in. Splint kits now work, but can
  only be used on arms and legs. It’s automatically done during first
  aid if the medic has a splint kit.
- Added auto-save to the options
- Shopkeepers and their bodyguards won’t keep running out to save the
  town, all town guards won’t stray too far from a town when chasing
  down enemies
- Shortened some of the level 1 research, all research 25% faster,
  building speed 2x slower
- Added a new farming village, planning to do more with it later

### BUGFIXES

- I fixed a pretty significant memory leak, so hopefully that fixes or
  at least improves the “super crash”s
- dust bandit raids now go home after defeating you
- added in female backpack models and a few other clothing tweaks
- Fixed a ton of bugs in the faction assault system
- Fixed a bug that gave all hungry bandits a +5 to combat skills
- Fixed the “Failed to load compositor” crash that some systems were
  getting. (untested)
- Fixed the multiplying/vanishing shopkeepers when big changes made to
  the population options (import required to restore
  shopkeepers)(untested)
- Put error logging and “save failed” warning message to try and catch
  the cause of corrupt savegames
- Fixed KO time increasing when loading game
- Many crashes fixed from player crash dumps

## 0.62.1

- Fixes crashes
- Makes the bandit attacks less frequent

[Category:Updates](Category:Updates "wikilink")