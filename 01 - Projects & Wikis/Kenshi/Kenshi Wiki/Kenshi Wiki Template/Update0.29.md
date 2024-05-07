**Version 0.29** added encumbrance mechanics to Kenshi.

__TOC__

There’s a new update for those who haven’t noticed yet.  0.29 adds
encumbrance to the game, so if you notice all your characters can only
walk slowly now, then you need to lighten their inventories. I think in
the next update I will raise the lower limit for carry weight, I don’t
want the player to spend all their time crawling slowly along and
getting bored. Here are the changes:

## 0.29.0

- Encumbrance has an effect now. Your inventory and gear will weigh you
  down, making you move slower. How much you can carry depends on your
  strength.
- Strength is also increased by walking about with a heavy inventory. 
  The heavier it is, the faster the increase.
- Your encumbrance is shown in the inventory window.
- The stats panel in the corner shows you if you are gaining strength or
  athletics XP based on your encumbrance.
- Better look closely at your inventory now to see what you can still
  carry.  If you are one of those sneaky people with a shopkeepers
  backpack, you might want to get rid of it now.
- Athletics skill is now functional.  Running at full speed without any
  encumbrance will improve it faster.

#### FIXES

- Inventory item icons now have transparency
- Fixed the bug where 100’s of caravan traders could swarm around an
  area.  If you have this you will need to import to a new game to get
  rid of them.  Or kill them all.
- Fixed another dialog system bug where you could hire Wingwang for
  free.
- Fixed bug where you couldn’t lock your doors
- Fixed the bug where you sometimes couldn’t loot bodies

## 0.29.5

- Re-tuned encumbrance stuff a little. Its a bit easier to carry more
  weight now, especially at lower levels. More adjustable numbers in the
  construction set.
- Storage boxes can stack up to 10x more items.
- Heavy weapons are slightly lighter in the inventory
- Un-bandaged bodypart damage slowly worsens once it gets below 40 (not
  affected by stun damage)
- Characters always use the weapon on their back first, the weapon
  sheathed on their hip is 2nd choice.
- Backpacks half the weight of whatever is inside them, but also deduct
  a little from your combat stats-\>
- Tweek: Bleeding rate down 33%, bleeding clot rate up 50%. This brings
  more focus back to bodypart damage over plain boring bloodloss.
- Medkits drain twice as fast when used by a novice medic.
- You can build cages, and stick prisoners in there. Not much else to do
  yet, its still unfinished.

#### BUGFIXES

- Fixed crash when closing map window
- Made a fail-safe in the rare event that there is a certain crash while
  saving, so it will finish up before crashing and avoid corrupting your
  savegame.
- Fixed encumbrance affecting combat speeds
- Fixed bug with the pathfinder when demolishing structures
- Medkits now vanish from your inventory when used up.
- Improved the medic AI behaviour bugs when in battle
- Backpack contents affects total weight even if not equipped.

## 0.29.6

- Made the GUI more clear about when your stats are being affected by
  your equipment.
- Fixed a few more bugs
- Importing squad only imports players faction relations.
- Did some magic that will help with some slowdowns
- Possibly improved the problem that causes hundreds of wandering
  traders to collect in an area

#### SAVE CORRUPTION

- Rearranged the savegame code so that it saves your squad 1st, so if it
  crashes you can still import your squad.
- Your previous savegame is backed up to a folder called "bak". Rename
  the folder to replace "quicksave" if you want to restore the old save.

## 0.29.7

- Made weapon speeds less drastically affected by inventory encumbrance

#### BUGFIXES

- Traders don't visit your base and get in the way all the time
- Can heal someone or pick them up while they are in bed
- Fixed the bug where characters unlock the door before using a cage or
  bed, but only on newly built stuff
- NPCs in bed or in a cage will load and save correctly
- Made the startup config window show less useless options so its easier
  to notice the screen resolution setting

[Category:Updates](Category:Updates "wikilink")