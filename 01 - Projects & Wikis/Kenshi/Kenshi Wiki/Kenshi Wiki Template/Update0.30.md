**Version 0.30**

__TOC__

I had a new interview a short while back, and only just found it, so
here’s the link if you are interested in the inspiration and underlying
concepts of the game:
[Leviathyn.com](http://leviathyn.com/games-2/previews/2012/09/15/an-interview-with-greenlit-kenshis-creator-chris-hunt/)
I’ve been rather quiet the last month or so, I was keeping my head down
so I could concentrate on restructuring some of the physics code. All
done now, and the next update is now ready via the auto-updater. You
will notice a couple of town layouts might have changed, notably the
starting town. You also might notice that some bandits have reward
bounties shown in their info. That’s something coming in the next update
0.31. Here are the changes:

## 0.30.0 “Re-Population”

Lots of huge internal changes, but it won’t seem like much has changed
gameplay wise

### FEATURES

- Massive code restructure. Put entire physics system on the background
  thread, slight performance increase and world load times are now just
  a couple seconds.
- Flophouses added to some towns, you have to pay to use the beds.
- Made a town auto-population function so it will be easy to add new
  guilds and shops etc

### BUGFIXES

- Fixed the new ghost towns bug (will need a restart/import to fix it if
  you have this bug)
- Fixed the level editor crash
- Enemy prisoners are now considered non-enemies, so passing squads
  won’t attack them.
- Crash dumps give me a bit more information now, not that you really
  care.
- Lots of fixes

## 0.30.1

A big bunch of bugfixing

### FEATURES

- More options for importing your squad to a new game. You can import
  your buildings too, or use it to just reset all your characters
  positions if someone gets stuck on a roof or something.

### BUGFIXES

- Fixed lots of combat spazzing behavior, especially in 2 vs 1 fights,
  tweeks to the combat AI too
- Fixed crash on loading game
- Fixed the mental shopkeepers
- Fixed crash when you pick someone up
- Fixed the ghost town bug even more. Now its like, 200% fixed.
- Other crash fixes
- I’m getting closer to fixing the Black terrain bug that some people
  are getting but this will take some time, as I am entirely dependant
  on help from people on the bug forums.

### NEXT UPDATE

Bounty hunting! Certain NPCs will have bounties, if you take one down
you will have to carry them to a police station to claim your reward. Be
careful, you will only get 50% if they’re dead.

## 0.30.2

Hunting the crashes, lots of crashes fixed. 0.30.1 was a pretty bad
release stability wise, I will continue fixing bugs at super sonic
speed. There are still plenty of bugs around, but I wanted to get this
update out quickly.

- Outposts also act as flophouses now
- Sorted out the town populations, lack of traders etc.
- Can no longer carry people if your left arm is buggered. In future you
  will be able to carry on right side instead.

## 0.30.3

- Tweeked some combat variables, gangs that outnumber you will hit you
  more, carrying your buddies is a little lighter on encumbrance
- Fixed bug with characters sometimes teleporting short distances
- Fixed a crash and a lot of bugs importing with buildings
- Fixed 2 random crashes
- Fixed lots of bugs with building, and sleeping
- Fixed bug when dismantling.
- Other bugs fixed too, I forgot what though.

## 0.30.6

- Properly found the actual source of the freezing bug now, I was just
  treating the symptom before.
- Fixed drag selection with the shift key pressed

## Trivia

Version 0.30 was initially released on 24th October 2012 in a standalone
launcher - it can be considered a precursor to the current
'experimental' branch versioning.

[Category:Updates](Category:Updates "wikilink")