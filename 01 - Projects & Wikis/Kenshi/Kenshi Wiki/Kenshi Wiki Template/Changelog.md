The **changelog** shows what changes were implemented with each version
of [Kenshi](Kenshi.md "wikilink"). You can find the changelog in the Kenshi
main directory. This list is everything included in that file to date.


After updating the Changelog with the newest development documentation,
please update the current version numbers \[ here\] and \[ here\]. All
this data and more can be found at Kenshi's [update page on
Steam.](https://store.steampowered.com/news/app/233860?updates=true)

## NOTES:

- Certain nVidia driver versions (possibly mixed with certain windows 10
  updates) are causing crashes. I'm not currently sure what the solution
  is, but try installing a few different driver versions.
- Nvidia's GeForce driver 397.31 and 397.64 have been reported to cause
  kenshi crashes.
- If you experience random crashing, you are probably running out of
  video memory.  Turn down "Texture quality" in the game options

<!-- -->

- No more 32-bit support, it's impossible, the game's gotten too big to
  fit within the 3GB memory limitation.  You can still access the older
  32-bit version through Steam's \[kenshi-\>properties-\>betas\] tab.
- Initial loading time is sometimes pretty long on non-SSDs.  The
  terrain will take ages to load in and things will look weird/white for
  a while but once loaded everything should be fine.
- You won't see all new map content unless you import your savegame
  after an update

## 1.0

### 1.0.59 (Experimental)

- Fixed a bug that messed up dialogue events for a few NPCs
- Minor bugfixes for FCS

### 1.0.58 (Experimental - FCS 2.11)

- Fixed a bug that caused items to use old names

### 1.0.57

- Small updates to Japanese translation in main branch plus experimental
  release of FCS v2.1.

### 1.0.55

- Hotfixes
- Update to Japanese translation

### 1.0.55 (Experimental)

- Hotfix for mods not loading header info

### 1.0.54 (Experimental)

- Hotfix for the popup message box showing no text

### 1.0.53 (Experimental)

- Generate distant towns is now an option, disabled by default.
- Hopefully fixed the crash from 1.0.52
- Bed recovery rate multiplier now displayed in tooltip
- Font loading deferred to when splash screen is displayed (to prevent
  long initial black screen for heavy languages)

### 1.0.52 (Experimental)

- Towns can now be seen from miles away instead of popping into view at
  close range
- Disguise quality is now affected by your UNMODIFIED stealth skill.
  Before your disguise would be negatively affected by things like the
  armour you were wearing, but this was the disguise itself so wasn't
  quite as intended

### 1.0.51

- Fixed deleting saves from new save location
- Fixed bar squads not spawning in Heng due to multiple towns in one
  zone
- Fixed issue with initial player health if race was changed during
  character creation

### 1.0.50

- Fix for Stun damage recovery rate being 10x too slow
- A crash fix for missing meshes in some weird rare situation

### 1.0.49

- Fix for importing that was broken in last update

### 1.0.48

- Due to recent windows updates causing even more save issues when the
  game is installed in the C:/Program Files/ folder, Saves can now
  optionally be stored in the user directory instead of the install
  path.  It can be set in the options.
- Fixed FCS 'xp rate athletics' constant doing nothing
- Added Stun Recovery Rate and Robot First Aid Speed constants to FCS

### 1.0.47c

- Fixed missing japanese translation files

### 1.0.47b

- Korean translation update only, no change to exe

### 1.0.46

- Fixed a random dialog crash
- Added some directX dlls to hopefully help some people with install
  issues
- Fixed crash dropping things in character portrait panels
- Moved save complete message to after the back thread is finished
  copying files
- Fixed 2 crashes that could happen from missing mod data
- Fixed animal trading window not closing if confirm button is canceled

### 1.0.45c (Experimental)

- Updated Korean Translation (There was a file mix-up before)

### 1.0.45b Posted On February 28, 2020 (Experimental)

- Added Korean Translation

### 1.0.45 Posted On January 22, 2020 (Experimental)

- Fixed dialogue interrupts not working on announcments another NPC
  interjected. Could affect certain player base raids.
- Fixed crash dismantling cages with an unconscious occupant
- If you kidnapped the pack beast of a wandering trader, the beasts
  inventory would still get re-stocked.
- Fixed possible crash when dismantling a turret that is being used
  (which should be impossible)

FCS/MODDING

- Fixed crash if modded charcter mesh has uvs outside 0-1 range (other
  than head)
- Fixed an issue with CHARACTER "stealth stats" property
- Fixed crash if character model failed to load due to missing skeleton
  file

### 1.0.44

- Hotfixed the recent character editor infinite loading fix breaking new
  games
- Added 'character limit reached' message when buying animals
- Fixed building town allocation when placing town markers
- Added error number to CRASHDUMP FAILED log message (description was
  garbled)
- A fix for animals walking into buildings

### 1.0.43

- Fixed character editor crashing if character model fails to load from
  a mod
- Fixed interior layout editor mod tracking (level editor)
- Fixed crash with the restricted food tooltip for some mods
- Fixed restricted food tooltip potentially missing some races
- Fixed a few minor dialog bugs

TRANSLATION

- Chinese updated

### 1.0.42

- Hotfix for a crash with the backpack stealing thing from yesterday.
- Cleaned up list of races that can eat restricted food in item tooltip

### 1.0.41

- Removed the "Disable civilians in towns" option as it was causing some
  issues with things like Waystations being unpopulated, and no longer
  made a noticeable performance gain.  Thanks to Shidan for spotting
  that one.
- Fixed use cursor appearing on player built tables
- Fixed stealing backpacks from animals not counting as stealing
- Backpack contents marked as stolen when you steal a backpack

FIXES

- Fixed a crash with the new fix for the previous new fix for the
  previous ragdoll crash
- Fixed translations, fonts and audio when kenshi install path contains
  non-ascii characters
- Fixed texture loading error handling- with invalid textures (eg from
  file corruption or a broken mod) you now just get black, instead of a
  crash

### 1.0.40

- Quick fix for the newly introduced bug that caused the zone loading to
  get stuck

### 1.0.39

- Fixed a crash with the new fix for the previous ragdoll crash
- Fixed bodyguard betrayal triggering more than once per betrayal,
  leading to oversize relation penalties. Penalty should be 20 to
  reputation.
- Fixed boots appearing on robot legs if boots have a colour map
- A bunch of small stability fixes to the FCS

### 1.0.38

These 2 insidious random crashes were fixed with the help of the player
Kapaer. He is a total genius who managed to track down the crashes on
his own system and make a mod that hacked the game and fixed them.
Thanks to this and the info he provided we were able to use the memory
addresses to track down the problems at the source. Kapaer's name has
been added to the game in his honor.

- Fixed a random crash that would happen if someone caught someone else
  committing the crime of assault against \*nothing\* (no victim)
- Fixed a random crash when picking up characters, or something related
  to that. Would only happen with certain people's PCs, so was hard to
  catch. There is a small chance that this could fix the passable walls
  bug too.

OTHER FIXES

- Clamped a value to hopefully avoid the cursed money item bug, where
  you would pick up a coin and get minus a billion cats
- Mostly fixed the issue with characters patrolling into private
  buildings
- Fixed interior visibility in build mode
- Fixed interior not loading correctly if you complete a building while
  inside it
- Fixed item labels being cut off at certain resolutions

### 1.0.37

- Slaves are now only fed up to 100 if not in a cage, instead of 115
- Pet animals now heal 2x speed when KO, as they have no other means of
  healing and spend too much of their lives in comas
- Holy farm storage is no longer full of ration packs
- The GUI tooltip now also shows your bounty even if you are a slave

FIXES

- Fixed AI bug where a guard captures someone out of the boundaries of
  the town, and keeps picking them up and putting them down again
- SLAVE state is no longer reset when you are arrested by police. Slaver
  caravans should come by and collect slaves, but mods could prevent
  this, meaning that a slave could get arrested and trapped in a police
  station forever. Now its possible to wait-out a sentence.
- Fixed AI stalling when crafting items when different input items are
  needed.
- Fixed inventory item limit being ignored when AI moves large item
  stacks.
- Reduced characters running through the air or underground when zones
  are loading in the background

### 1.0.36

- Fixes for a few building interior visibility bugs
- A fix for NPCs sometimes dying if you knocked them out and then left
  the area, now it takes their health into account.
- Fixed bounty dialog not triggering if you hand in Eyegor
- A crash fix

### 1.0.35

- Stopped NPCs thinking animals are weak because they don't have weapons
- Fixed a crash if loading an invalid item in a character inventory (eg
  from a missing mod)
- Fixed particle effects of buildings on roofs
- Fixed crash if character dies while rearranging squads
- Fixed missing temples in Holy Nation towns
- Fixed DC_IS_NEARLY_KO being unhandled (it is a duplicate of
  DC_NEARLY_KO)
- Fixed some dialog not triggering as DC_IS_ENEMY always returned true
- Some minor fixes to the navigation mesh

TRANSLATION

- Chinese and german updated

### 1.0.34

- Fixed game freeze when changing font size in certain languages
- Fixed chinese character names and tips display, changed to clearer
  font

### 1.0.33

- Fixed dismantle button missing from turret info datapanel if
  upgradeable
- Fixed crash in Escape Cannibal Cage tutorial

TRANSLATION

- Chinese update, new font

### 1.0.32

- Fixed clothing being chosen for characters before race limiter is set
  up
- Fixed boots spawning on characters with no legs
- Fixed boot slot not being disabled for characters spawned with no legs
- Fixed crash when making savegame names ending in ...
- Fixed getting stealth xp when in a cage
- Random crash fix

TRANSLATION

- French and chinese update

### 1.0.31

- Chinese language option added
- Fixed problem with the FCS def files if system decimal separator is a
  comma
- Kral's chosen and Band of Bones no longer go to the Border Zone

### 1.0.30

- Fixed robot limbs spawned on characters not behaving as robot limbs
- Fixed removing an arm of carried characters causing them to be dropped
- Fixed crash in the FCS when creating new items

### 1.0.29

- Fixed a random crash
- Fix for some situations where a carried person would never get put
  down if they died
- Passive characters wont fire turrets unless attacked
- Fixed dropping items onto portraits when view is scrolled

### 1.0.28

- Japanese translation rollback to v1.0.22, last known best version. 
  There is currently a mix-up with the japanese translation that we are
  working to fix, but we're not doing well because we don't understand
  japanese.

### 1.0.27

- Japanese language update

### 1.0.26

- Fixed crash if combat is cleared in an EV_I_DEFEATED_SQUAD dialogue
  event
- Fixed characters having incorrect voice after changing race/gender in
  the character editor
- Fixed kidnap order on wild animals
- Added a new save logging system to help debug any save/load related
  problems
- Finally fixed the blood spider attack range

FCS

- Existing translations can be exported as gamedata.po
- Fixed exporting multi-line translated strings when exporting
  gamedata.po
- Added 'no longer used' description for deprecated values

### 1.0.25

- Fixed crash if missing save folder
- Fixed limb stumps causing crash when changing race in character editor
- Fixed a few minor town guards that didn't respond to attacks

### 1.0.24

- A rare crashfix
- Fixed crash added in last update, if character has no clothing
- Fixed possible towns having null faction
- Removed unplaceable towns from town list in ingame editor

### 1.0.23

- Fixed toggling block,hold,passive,jobs buttons not always working as
  expected
- Fixed stealth KO animation restarting without moving if you try to KO
  someone else
- Added "toggle HOLD" keybind
- Characters spawning with robot limbs can be optional
- Fixed all limbs being missing for characters spawned with at least one
  robot limb

TRANSLATIONS

- Japanese translation complete

### 1.0.22

- Changes to save file system to attempt to reduce saving errors caused
  by windows file locks
- Fixed NPC's hitting many times at once if you get in a cage during
  their attack, causing instant death
- Fixed player orders to bash gate
- Fixed override towns not updating public state, which could result in
  aggressive town AI after a faction takeover
- Fixed items in buildings being unowned if you import the game inside a
  building
- Fixed crash if modded skeleton files are missing
- Fixed a crash in character editor

FCS

- Added a check all/active/none button to mod selection
- Characters can be spawned with robot limbs
- Fixed a crash exporting translations

TRANSLATIONS

- updated gamedata.pot
- Japanese update

### 1.0.21

- Tweaked missing item mesh fallback again
- Fixed backpack contents not being imported for backpacks in containers
- Fixed overriding newland/land/textures path in mods
- Error message when game fails to detect a mouse
- Fixed mod crash if character model is missing
- Added error message for missing character model so you know why you
  are being attacked by something invisible

### 1.0.20

- Fix for some cases where a base raid wouldn't leave
- Fix for some cases where the carrying/bed/cage states could get mixed
  up resulting in the wrong context menu commands showing on a character
- Fixed crash loading a physical item with non-existant mesh file
- Fixed crash when loading character in bed where the target is not a
  bed

### 1.0.19

- `Fixed dismantle button not showing on empty containers`
- `Fixed odd behaviour when switching to overlapped armour meshes`
- `Fixed crash in peeler machine when characters don't have 7 body parts`

`TRANSLATIONS`

- `Portuguese tweaked to fit GUI, translated tips`
- Russian update

### 1.0.18

- `Fixed navmesh issues in spider factory and Bastion`
- `Fixed treasure not spawning in spider factory`

### 1.0.17

- Pick lock task now displays 0% if below minimum lockpick threshold
- Stopped import recalculating player town on buildings that don't
  create towns
- 2 crash fixes

### 1.0.16

- Fixed crash when recruiting someone if leader is following unloaded
  character
- Town override states updated on import - Fixes towns in map screen
- Tweak for previous fix in .15

### 1.0.15

- Fixed characters using low lod terrain height when jumping across the
  map (could use characters to appear in weird places, like private
  buildings if they were in squin)
- Fixed characters moving super fast after colliding with sloped navmesh
  edge (could cause who knows what kinda issues)
- Crossbow XP only increases if target is in range (exploit fix)

### 1.0.14

- Japanese translation updated (proof reading 70% complete)

### 1.0.13

- Small AI performance optimisation, prevents cases where your framerate
  could get destroyed if you were running a huge base with 100's of
  machines.
- Fixed crash if character name uses missing wordswap
- Also only show one error message per missing wordswap
- Fixed game not exiting after failing to save
- Back thread save icon not stuck on when failing to save
- Fixed platoons not saving if faction name contains \*

TRANSLATION

- French and Russian updated

### 1.0.12

- Fixed getting neverending assaults from the Holy Nation if you killed
  all of their leaders
- Fixed another crash related to animation modding
- Fix for an Black Dragon assault that could never end in some
  situations

### 1.0.11

- Added death items to the Skin Bandits to make them less frustrating
- Fixed skin bandits just dropping captives at the town entrance
- Fixed crash when adding combat animations in a mod
- Fixed a rare case where characters could get stuck on the edge of an
  obstacle
- French spelling fix

### 1.0.10

- Font scaling should be improved, increasing font size should no longer
  over-increase the line spacing
- The font scaling slider in the options should no longer crash probably
- Fixed animals sometimes replying to human speech
- Fixed the bridge in Rebirth (again)
- Doors use name of parent building in context menu
- AI fix for inacessible walled off towns with an internal gate

TRANSLATIONS

- Small updates for Spanish, German, Portugese

### 1.0.9 

- Lots of AI fixes for police, so they shouldn't now forget to heal or
  release any prisoners 
- Fixed animation modding crash 

<!-- -->

- Fixed gamedata modIndex value for modded animation load order

TRANSLATIONS 

- Japanese update

### 1.0.8 

- A fix that should solve the problem of buildings and walls sometimes
  getting assigned to the wrong town, which led to bugs like characters
  not getting food or not building things. 
- Nests can no longer spawn in inaccessible locations 
- More NPC AI fallback for bad nest locations 

<!-- -->

- The point at which your health causes you to go into a coma, based on
  toughness, is now moddable in the FCS: \["max toughness ko point"\] 

TRANSLATIONS 

- German update

### 1.0.7 

- Fixed the City Hero gang waiting for you by the wrong gate in Heng. 
- If you defend yourself from the City Heroes or similar bandits you
  should no longer get attacked by the guards 
- Fixed carpets disappearing from your buildings on re-load 
- 2 crash fixes, one caused by re-ordering the research list

### 1.0.6 

- Truncated research data panel lines if name is too long 
- AI fallback for bad nest locations 
- Fixed game crashing if install path has non-ascii characters 

TRANSLATIONS

- Changed the launcher saying spanish was incomplete, because it's not,
  it's finished 
- Spanish tweaks for some stat names being too long to fit on their GUI
  lines

### 1.0.5 

- Combat spark effects added 
- "Entered new biome" notification sound 
- Fixed a crash that could be caused by a bad mod

### 1.0.4

- Combat spark effects added
- "Entered new biome" notification sound
- Fixed being able to reorder research to skip prequisites
- Fixed multi-line datapanel text overlapping
- AI fix where a crippled character with un-healable legs would still
  keep trying to heal them
- Fixed some bugs with corpse disposal AI 
- Slaves can no longer claim bounties on other slaves in a slave camp
- Fixed an AI bug in Okran's Shield where prisoners were all getting
  piled up by a bed
- Fixed a crash that could be caused by a bad mod

TRANSLATIONS

- Japanese, french, german, portugese, spanish updated

### 1.0.3

- A small number of people are getting an unexplained random crash, this
  is an experiment to see if something we did fixes it
- A bug sometimes gives player buildings the wrong town, not sure how
  but sypmtoms of this will be the AI not getting food or items or
  building things.  With this update you should be able to fix any
  broken towns by importing.

### 1.0.2

- Fixed again that pesky bridge in Rebirth
- A fix for the AI constantly alternating between self preservation and
  another task
- Announcement dialogs shouldn't get repeated, but if they do it won't
  keep snapping the camera to the location anymore, only once per raid
- A fix for characters in crowds sometimes getting pushed through walls
- Buildings town reassigned when new player outpost created (for
  walls).  If you built your town walls before anything else they would
  be assigned the wrong town and the AI builders would ignore them.

TRANSLATIONS

- Spanish tweaks
- French update

### 1.0.1

- French updated (99%)

### 1.0.0

- 390 updates later
- 1611 occurences of the word "fix"
- Number of years passed unknown
- Thankyou to all the supporters, forum moderators and bug reporters for
  all your hard work

TRANSLATIONS:

- Russian updated (100%, thanks Vlad!)
- French updated

## 0.99

### 0.99.99

- Fixed slavers stealing your prisoners
- NPCs have more money for buying from shop counters, especially
  caravans and anyone in the slave trade
- (Steam) No longer clears previous installed mod list file if steam
  failed to connect
- A navmesh freeze fix

TRANSLATIONS

- All languages have had updates except russian, because we can't find
  our translator

### 0.99.31

- Fixed the missing audio problem from last update
- More fog princes in the Fog Islands, to make sure people get eaten

### 0.99.30

- Stack now has a functioning police station
- Flotsam has a bakery
- Fixed characters getting fed an invisible meal when getting in a cage
  if tagged as escaping
- Fixed slaves picking their own shackles not counting as a crime
  because they were considered part of the enslaving faction
- Changed the over-aggressive skeletons in HN territory
- Fixed a crash

### 0.99.29

- Fixed newly built walls collision being passable so you couldn't walk
  on top until the game was re-loaded
- Gate guards in Mongrel should stay closer to the gate and not go off
  getting lost fighting in the foglands so much.
- Walls made 2.5 times tougher again, they should now be approx 25% as
  tough as their equivalent gates
- \[Dismantle\] button now asks if you are sure, except for walls
  because you might want to delete a lot of them some day
- Fixed the Machinists faction selling Hemp in UC towns
- a rare crash fix
- Fixed the collision
- Some other technical mumbo-jumbo

TRANSLATIONS

- Spanish update (99% complete)

### 0.99.28

- Fix for many of the ally aid campaigns not triggering
- Fixed prison sentence times not saving, so all prisoners got pardoned
  on reload

### 0.99.27

- Fix for Rebirth town size being too low, confusing the guards AI
- Fixed the bridge in Rebirth
- An AI fix where newly recruited characters were missing the "protect
  allies" job
- Prevent passing squads from stopping to relax in hostile towns if they
  pass by
- Fixed anti-slaver allied dialogue
- Possible fix for characters sometimes slowing to a walk when nearing
  their destination
- More nice loading screens

### 0.99.26

- AI shopping should now work, traders should buy stuff from your shop
  counters, NPCs will visit your town if it is set to public
- Fix for characters being magically freed from cages after healing
- Walls now twice as tough against smashing
- Rare fix for AI getting stuck when pathing back home to a locked up
  base
- Stopped captured NPCs disappearing on load when their town is
  destroyed
- Prisoners who escape from cages will now bash their way out of locked
  doors instead of getting confused

TRANSLATIONS

- Japanese rolled back due to errors, will update again soon

### 0.99.25

- Fix for raid campaigns repeating their announcement dialog instead of
  leaving/attacking
- Floating damage numbers now include the cut-stun efficiency damage
  factor

TRANSLATION

- Searching for text in FCS translation mode selects the line when
  dialog is opened
- Japanese updated

### 0.99.24

- Artifact items quantity assigned to locations is directly proportional
  to town value rather than random (rewards more consistent) (optional:
  requires import to see changes)
- AI fix for cases when a base had only one gate and the AI wouldn't go
  through
- When other factions take over a Holy Nation town they break all the
  emperor statues
- Fixed the city hero gangs not harassing players
- Fixed EV_I_SEE_ALLY
- Fixed indoor combat stat penalty
- The non-violent food raids go home rather than hang around your food
  barrels for 4 hours
- Fixed the Mongrel building in Black Scratch
- Fixed loading screen when window resized
- AI fix for guards that dont put the criminals in cages and just hold
  them while in shopkeeper mode
- Untestable fix for "give up chase" dialog event triggering when people
  are just fighting and not even chasing
- Road editor handles locked roads

### 0.99.23

- Terrain and navmesh updated, probably nothing noticeable, move along

### 0.99.22

- Escaping from an evil faction cage, like cannibals, no longer tags you
  as an escaped prisoner
- Fixed using strength or tools to break out of prisoner poles
- Fixed tooltips not showing for the "committing crime" and "escaped
  prisoner" panels
- Fixed name truncation on character portraits for multi-byte characters
- Update to the roads to fix NPCs getting stuck with long-range travel

### 0.99.21

- Fix for a suspected crash

### 0.99.20

- You can now use tools or brute strength to unlock any lock, door, cage
  or container.  Good for treasure hunters, not so good for thieves. 
  Now non-thief characters won't feel forced to learn lockpicking
- Tools are more heavy and expensive than before
- Tools are single use, they break after opening the lock
- Using tools is really slow
- Brute strength only really works with very very strong characters on
  weak locks (strength needed = 3 x lock hardness)
- travel shops now sell tools
- Severed limbs are now properly bloody
- Fixed hive interiors not showing
- Fixed bandits not looting food from containers
- An AI fix for certain gate/wall configurations
- A fix for AI attacking freed slaves that should be no longer hostile
  after freeing
- Fixed the corrupted item icons on ATI cards
- Slightly more fishmen
- Slaver cages have better locks, ancient safes have slightly easier
  ones
- Fix for campaign data that got some values mixed up, resulting in
  traders being "war leader" for example
- Fixed the blurry item icons
- Tweaked GUI line spacing to try to fix main stats panel on some
  resolutions
- Fixed put-in-bed order overriding dismantle order if carrying someone
- Added sfx to NPCs buying stuff

### 0.99.19

- Added in some missing armour/clothing crafts
- Tweaked some bounty character's wanted factions
- A general AI fix that might have seen them running off to far away
  buildings
- Another fix for AI campaigns where they go home without raiding your
  base first
- Fix to prevent gaining stealth xp from the person you are carrying
- Prevented slavers from beating up obedient player slaves when another
  player in the same squad was getting beaten
- Fixed a crash when you kidnap a unique NPC and return to their town or
  something i dunno but i fixed it

### 0.99.18

- Fixes for the Slave escape AI
- Fixed the western path to Worlds end
- Fixed slavers taking player's prisoners
- Fixed stealth KO on prisoners setting them free
- Fixed stealth KO on prisoners providing massive easy XP harvesting
- Fixed broken navmesh in Tower of abuse, infested lab and far east tech
  lab
- Fixed a rare random crash in the engine code
- Fix for Hive hut doorways sometimes getting blocked

### 0.99.17

- Regenerated entire navmesh, should solve some of the passable
  obstacles that were being encountered
- A crashfix

### 0.99.16

- Fixed up the slaver AI for the reaver HQ, also passing reaver patrols
  can gather up more slaves from the cages
- Slaves no longer protect allies if in obedient slave mode
- Slaves now get totally balded, because it looks more slavey
- When an ex-slave finally reaches not-slave status, his hair grows back
- Fixed imprisoned characters being set as slaves if they were once a
  slave before, when they shouldn't be, eg in police cages
- Fixed not being able to loot bodies while crawling
- Fixed bar NPCs not healing themselves when wounded
- Character stats window updates progress when open

### 0.99.15

- Fixed missing import faction relations option
- Added something to help prevent your bodyguard NPCs from attacking
  your allies if they are enemies
- Tweaked the Forage AI to hopefully prevent butchering certain friendly
  animals like caravan mules
- Fixed people repeatedly beating up slaves after they've been
  recaptured, especially the Reavers
- Fixed slaver AI getting confused when they found an unconsious person
  wearing shackles who wasn't a slave
- Attack animation no longer cuts out the moment the victim is knocked
  out
- There was an issue where a character trying to get up would get stuck
  on the floor (with his animation resetting) each time he was hit. Now
  they will ignore the hits while getting up, but each one has a 10%
  chance of causing a short knockout
- Town shek now react to player HN ally with 'Thug hunter' rather than
  attack
- Fixed Reavers sending out Slave Traders to raid player base
- Fixed gui not updating when obedient slave job added

### 0.99.14

Improved some aggro/law based stuff:

- Neutral "Military" NPCs no longer have legal immunity unless they are
  from a town resident faction
- The act of enslaving now counts as a crime, but only when it's in the
  town of a faction that is anti-slavery. This means you can attack the
  slaver in self defence (at the right moment) without getting yourself
  in trouble. Town guards will stay out of it.
- Slavers now have their own NPC type classification. Law enforcers will
  stay out of any conflicts involving slavers, instead of helping them
  (unless they are allies of course, like the United Cities). This
  doesn't mean you can just attack them unprovoked though.
- Town guards will only attack slavers caught in the act if they are
  anti-slavery and the victim is an ally, otherwise they will not bother
  with it.
- Slaver caravans won't take slaves from cages in towns that aren't
  slavery friendly
- Removed Holy Nation patrol from Nothern Coast to stop them wiping out
  the fishing village
- Anti-slavery factions will fight to free their allies from slavers if
  they see them get captured
- Fixed some AI bugs where law enforcers wouldn't deliver their catches
  to cages and would get stuck in other tasks
- Fixed a crash with NPC AI looting
- GUI buttons no longer pressed on mouseup after drag-selecting
- Added import Relations option to import game

### 0.99.13

- Mouse buttons are now reconfigurable
- More fixes to stop Shark town destroying itself
- Fixed trade caravans going to some bandit hideouts and starting a
  fight
- Fixed town reaction changes sometimes missing part of the town when
  the town covered multiple zones, so would keep some old residents
- Kidnapping slaves now counts as "slave freeing" rather than kidnapping
- Fixed inaccessible roof of the metal wall-house

### 0.99.12

- Bandit squads used to "occupy" your town in spirit, even if they
  failed the assault, causing bugs and nuisances. Now they won't occupy
  the town if they are defeated first.
- Fixed a bug with unique characters that join the player getting
  incorrect world states, which could trigger the wrong dialogs and war
  campaigns.
- NPCs can no longer enslave, loot or butcher anyone while they
  themselves are playing dead
- NPCs on turrets will now also shoot anything attacking their fellow
  residents, sometimes they wouldn't help if they were different
  factions
- Fixed another random "not eating in town" bug
- Shrieking bandit relations can now deteriorate, so they don't stay
  neutral forever
- Lockpicking a slaves shackles now correctly counts as the crime of
  "slave freeing" rather than burglary
- Removed player hauling job from general storage
- Fixed carried characters disappearing when character edtor opened
- Fixed beard colour on character model for some hairstyle combinations
- Finished the ragdoll for the land bats
- Fixed crash moving characters to squads that were saved empty
- Items on buildings drop to the ground when the building is dismantled

### 0.99.11

- To help town guards from getting gradually worn down and killed off,
  leading to town depopulation, gate guard squads can now regenerate
  over time (as the town would have assigned new guards).  Doesn't yet
  work if you are permanently resident in the town.
- Fixed a bunch of crashes

### 0.99.10

- Added a new option to the AI panel for turrets to shoot at neutral
  targets, like bandits and wildlife. May cause extra aggro and corpses.
- Fixed the slave AI in the holy mines
- Gate guards are a bit stronger
- Some of the more mild mannered factions should no longer bash your
  gates down just to casually get past
- Increased number of simultaneous attack slots for some of the larger
  creatures
- Added "training" category to the building options
- Made final boss a bit harder
- Added separate factions to Shark bar fights to avoid town civil war
  outbreaks
- Fixed being unable to talk to Grey
- Added dialogue to Bo

### 0.99.9

- Hive princes can no longer eat foul meat, because they are too good
  for it. Also they now have 80 HP
- Fixed characters randomly not eating
- If you buy a normally-hostile type of slave or prisoner such as a
  bandit, he will no longer be attacked the moment he leaves his cage
- Fixed the "grouped" movement speed orders affecting characters when
  they weren't part of the group, eg when someone goes off to operate a
  machine
- Also fixed a crash
- Fixed attributes in character stats window displaying incorrectly for
  animals

FCS

- Fixed search function not working properly in translation mode

### 0.99.8

- Fixed hivers being able to wear human shirts
- Fixed unique NPCs getting lost forever when disappearing in the
  wilds.  Now they will turn up back home when they escape captivity
  etc. (import required to replace any missing unique NPCs)
- Another bug fix that should stop NPC squads sometimes getting doubled
- Fixed thief fence not refreshing money
- Fixed NPCs getting stuck carrying characters

### 0.99.7

- Fixed some bars not being used by AI
- Fixed a bug that would have randomly prevented dialog from triggering
  with repeat limits
- Fixed some campaign chains getting broken due to duplicate triggers
  being disallowed
- Fixed some campaigns not triggering if player base is nearby to a
  ruined town of that faction
- Fixed a crash

### 0.99.6

- If you named your faction "Spiders", your characters would randomly
  turn into spiders
- Burning damage no longer affects robot limbs
- Holy Citizen start now has a holy flame book and better relations. 
  Also you can now buy "the holy flame" from traders in the holy nation
- Added "harpoon limit" to the graphics options
- Tweaked ancient science book distribution so it doesn't go mostly to
  the ashlands (needs import)
- Fixed flickering buildings bug
- Tweaked AI for inquisitors and nobles to stop them patrolling and
  getting lost
- Fixed town allocation when starting your outpost by building walls
- Fixed construction scaffold shadows for some building material modes
- Fallback RTWSM shader if tessellation unsupported
- Fixed __DEAD_SQUAD__ sometimes appearing on load

TRANSLATION

- French, German, Russian, Portugese added some missing wordswaps

### 0.99.5

- Update to the RTWSM shadow system, improves a lot of the shadow
  glitches
- Improved characters staying together in speed matching movement mode-
  the leading characters will slow down to let the stragglers catch up
- Fixed a crash when trying to load corrupt save
- A few pathfinder/movment fixes
- Stopped having no shoes affecting 'looks like a slave' if you can't
  wear shoes
- Fixed Tinfist not talking
- Fixed unique prisoners not spawning (requires import)
- Fixed an NPC duplication bug
- Fixed slavers continually picking up and dropping targets that are
  'staying low'
- Fixed Anti-slaver ally bodyguard bug 
- Fixed King Gurgler's head value
- Fixed endless dialogue with Crab Queen
- Added Mourn barman dialogue
- Fixed Shek pacifier not increasing relations after being paid
- Fixed Esata leading a war campaign against player ally base
- Changed bounty relations gained from Holy Nation inquisitor. You can
  now still increase relations slightly even when accepting payment.
- Changed enemy faction relation penalties for certain alliances. This
  means you shouldn't get armies marching to your base simply for
  allying with a faction. Unless you've murdered their friends.
- Balances to Holy Nation assault repetitions
- Added Holy Flame to holy bar shop inventories
- Additions to Boss Simion's dialogue. He now recognizes carried nobles
- Adjusted Luquin's stats to avoid recruiting issues
- Added armour trader to ally skin bandits (find them in the HQ)
- Added dialogue for Yamdu, Tengu and Koin
- Fixed Noble Ohta going missing after world state change
- Changes to UC world states
- Added extra ally UC campaigns
- Added ally UC bodyguards
- Savant can now give you a certain unnecessary machine blueprint
- The Hub now sells crossbow bolts

TRANSLATION

- Japanese version fix for tooltips not displaying line breaks
- Changed to a more readable font

### 0.99.4

- Added L/R mouse button swap option, for left-handed mousers
- Fixed a bug with sound detection not working properly with th the
  stealth stat, so extremely high stat would make them hear you
- Headgear can now have stealth bonuses, but not penalties
- Fixed player towns sometimes becoming undiscovered on import
- Fixed crash if mounted building doesn't exist
- Fixed a crash in build mode

### 0.99.3

- Fix for NPCs (usually slaves and recruits) going missing when you
  leave and return to a town.  Import recommended to restore missing
  NPCs
- Engineer job doesn't automatically repair destroyed buildings
- Japanese translation update
- Portugese translation update

### 0.99.2

- Added leather and chain shirts for the Hivers
- Rugs are no longer available for the player to build, now they are an
  item you can buy from traders and drop on the floor to place them.
- Added a new hat

#### FIXES

- Fixed random camera jumps when tracking a character
- Fixed some town NPCs getting deleted from the world if they were
  knocked out or imprisoned, basically the "murder detector" was too
  sensitive.
- Fixed dead animals appearing in trader list
- Fixed NUM+ keybind not saving
- Few other small fixes and a crash fix

### 0.99.1

- Added a few missing armour crafts
- fixed 2 inaccessible towns (import game if not fixed)
- fixed staff weapon reach

### 0.99

- The new map section is finally open! I won't detail its content to
  avoid spoilers but basically this area is less civilised and more
  dangerous, designed for end-game exhibitions.

#### FIXES

- -An AI fix that should stop characters running off for no reason
  sometimes

## 0.98

### 0.98.62

- Stopped characters with robot legs screaming that their feet are
  burning
- Fixed some animation bugs when characters are getting up
- Fixed some camera glitches
- Made the Dodge stat visible for melee characters
- Fixed some small AI bugs
- Fixed underground building check making walls and gates near cliffs
  float

### 0.98.61

- Big optimisation for the particle system, should run smoother in zones
  with heavy particles like the deserts
- Default setting for limb loss option set to "rare"
- If a leg goes below -100 health (and isn't amputated) then the
  character is crippled and has to crawl
- Wordswaps updated for french, german, portugese
- Fixed the bug where a group order to attack a target wouldn't register
  for some of the characters

### 0.98.60

- hotfix for characters unresponsive to movement bug

### 0.98.59

- No more wall termites, now if you seal up your base with no gates the
  AI will smash the walls down
- A fix for the animation modding system

#### TRANSLATION

- Fixed the french translation not working at all
- Updated french, spanish and japanese languages

### 0.98.58

- Fixed armour dodge stat not applying if it was a bonus
- Mounted buildings use town of the building they are mounted to
- Allow dismantling of mounted buildings on player owned buildings in
  npc towns
- Fixed being able to build inside NPC town radius if player town is
  nearby
- Fixed picking up characters again
- Fixed dead character animation not updating straight away when picked
  up, causing rigamortis

<!-- -->

- Random crash fix

### 0.98.57

- A fix for picking up characters
- Fix for a character editor crash for the southern hive

### 0.98.56

- Reduced the armour athletics penalties
- Minor improvements for AI campaigns, should improve them all arriving
  at the destination at the same time more often
- Stopped imprisoned NPCs being set as the leader of a campaign
- Overlapping player towns now get merged, to reduce AI confusion
- Fixed being able to build inside NPC town radius if player town is
  nearby
- Town population building allocation now consistent each game
- Fixed context menu crash if no player characters
- Medic job no longer ignored when carrying a hostile npc
- Fixed a saving bug

### 0.98.55

- Changed again the tooltip display of the "cut to stun" to again try
  and make it easier to understand: with the previous update it wasn't
  clear if the stun was added or subtracted from the cut resistance.  It
  now shows the total cut resistance like it did before the previous
  update, and also shows an "efficiency" percentage.  eg. 80% cut resist
  efficiency will leave a 20% stun damage.  
- Samurai armour dexterity penalty removed but overall damage penalty
  increased to compensate, so blunt weapons don't get an advantage over
  swords for samurais
- Samurai helmet now protects from dust storms
- Assassins rags dexterity bonus reduced by 0.1
- Added more stat penalties to the police helmet and reduced blunt
  resist slightly
- A few more subtle stat tweaks, generally increased the gap slightly
  between the heavy, medium and light armours.
- Fixed a typo in the gui code that was showing the wrong melee defence
  bonus in the armour tooltip (it showed the attack bonus instead)
- Spread a few more armour items and blueprints around some of the
  shops.  You can now find blueprints for a faction-neutral version of
  Holy Chest Plate and the Armoured Hood
- Added a Blackened chain tagelmust
- "Self Preservation" AI should now react to charging enemies once they
  get close 
- Fixed horizon fog blending with clouds
- Fixed a mistake in Plated Jacket giving it 90% cut resist

### 0.98.54

GEAR REBALANCE PART 3

- The idea now is that the light/medium armour guys should be able to do
  more harm and do well 1 on 1, and the heavy guys should handle being
  outnumbered better and overall last longer
- This is a big shake-up for armour. It's un-tested, so I would
  appreciate feedback, point out any items that you think are
  over-powered or worthless. 
- -Heavy armour has penalties to dexterity and attack skills.  The idea
  is that it limits you to being a tank, your attack has been sacrificed
  a little for defence.
- -Medium armours are designed to be for generalists.  Less protection
  than heavy but only mild skill penalties and so more tactical options.
- -Light and specialist armours are designed to be un-restrictive or
  even offer bonuses, suitable for rangers or glass-cannon melee ninjas
  and duelists
- -Armour can penalise dexterity and damage dealing
- -Changed the display of the armour stun damage stats in the armour
  tooltips to try and make it clearer to understand: it now shows 1 line
  for the final derived cut resistance, and a 2nd line for the incoming
  cut damage that gets converted into stun damage.  Adding these 2
  numbers together will get the total "cut resistance" number that it
  used to display before.
- -Increased shirt armour cut resist by 10%
- -Reduced plate armour stealth penalty so its still severe but not so
  total
- -The hiver shirts will be delayed because our artist went on holiday,
  and employment law says I have to let him.

FIXES

- -Some small tweaks to improve character movement bugs
- -Fixed haul job stealing items from bars if player town radius
  overlaps
- -Fixed player caravan and military formation spot issues
- -Formation refreshed when value in AI panel changed
- -Fixed bright yellow or white clouds at dusk
- -Fixed AI confusion with almost full inventories when picking items
  off the ground

### 0.98.53

- -Fixed furniture disappearing from purchased buildings on import
- -Added keybinds to select next/previous character
- -Fixed game not starting if there are non-ascii characters in
  installed path

2ND GEAR REBALANCE

- Released prematurely because I needed to get the above bug-fixes out.
  I will continue tweaking and experimenting with the armour balances. 
  Please leave feedback in the form of angry rants.
- -Toughness-based damage resistance amplified, so 20% more damage at 0
  toughness and 20% less damage at max toughness
- -All shirt armour damage resistances reduced by 40%
- -Global damage decreased 10% to counterbalance the above 2 changes 
- -All weapons had their armour penetration bonuses/penalties amplified
  by 50%
- -Heavy armour coverage reductions from the last rebalance have been
  reverted
- -Chain and plate damage resistance increased by 0.05, leather lowered
  by the same amount, also further reduced based on weight class
- -Increased damage and armour piercing of the Heavy Polearm by 10%
- -katana class damage penalty vs robots reduced from 50% to 40%
- -Cleavers get a 10% penalty vs animals
- -Stealth penalties removed from helmets
- -Not yet added, but the plan is to add some hiver-specific armour
  shirts

### 0.98.52

- -New animation mod system, allows modders to make animations that
  don't clash with existing animations or updates or other mods.  Can
  also make unique animations that are used for specific races or
  characters.
- -Fixed not being able to escape from your own cages
- -Bleeding is now saved and loaded properly
- -An improvement to the AI bug where they would give up a chase
  immediately

### 0.98.51

- Fixed an issue where npc faction ownership of player buildings could
  get mixed up on import
- Fixed some npc squads not loading correctly
- Fixed a few pathfinding failure cases, sometimes causing characters to
  stop mid-journey, or ignore a certain "unreachable" building

### 0.98.50

- Minifix for a crash when loading town/outposts that had no faction
  assigned
- Fixed the delay when loading a carried character

### 0.98.49

- Reduced the number of fog princes in the fog islands
- Added some undertakers to Mongrel, to help clear up all the bodies
- Fixed character editor starting race limits
- Fixed unique characters being duplicated if recruited and you import
  in their starting town
- Fixed a couple of crashes
- Wrote a few more Beep events

### 0.98.48

- Added more world reaction content
- Fixed cannibal/fogmen not kidnapping people if far from town
- Player owned buildings in towns no longer get erased when a town gets
  destroyed due to world reaction events
- Slightly increased the global number of science artifacts to
  compensate for them spreading out to the new un-released zone
- Added race limits to certain game starts (eg holy nation start has to
  be a human), added a few more basic game start-off options
- Fixed NPCs using the players cages for prisoner storage/collection
  again.
- Fixed world apocalypse if you made it to 6:04am on day 3495 
- Fixed looting dead pack animals from caravans not counting as theft
- Fixed slavers duplicating slave rags when equipping new slaves,
  resulting in piles of slave clothes everywhere
- Slavers don't get so carried away attacking bad slaves that have
  already been re-captured
- Fixed some foliage rocks sometimes having incorrect dust colour
- Fixed negative medic stats never increasing
- Fixed dialog crowd trigger bug that messed up the Esata event
- Fixed player towns becoming undiscovered when loaded after imports
- Fixed a couple small crashes

### 0.98.47

- Fixed mounted buildings (turrtets and lights) having incorrect town on
  import
- Fixed HOLD button not disabling hold mode
- Fixed an AI glitch with the auto-sit if the target chair was un-built
  and clashed with ditch resources
- Fixed dead bodies disappearing when being carried
- Fixed a crash

### 0.98.46

- "Passive" button added back in, to keep certain characters out of
  trouble
- Fixed slavers attacking you for kidnapping their slave a split second
  after buying the slave off you
- Fixed enemies sometimes rescuing their leader and putting him in your
  bed because it's nearest and they don't think you're enemies anymore,
  and then repeatedly picking him back up again once he's in bed because
  he looks like he needs rescuing again.
- Fixed bar beds being unusable
- You know when a machine crafting an item would be at 99% progress just
  as it ran out of materials? That shouldn't happen anymore.
- We fixed Crash X, but such creatures are crafty and cannot be trusted,
  so we have yet to celebrate by painting ourselves in its blood.

### 0.98.45

- Finished adding robot limb crafting.  It's expensive though, you'll
  need a lot of AI cores for anything above Economy Limbs
- Though Crash X's plague continues, more in depth we have gone with the
  debug data, hunting, ever hunting, each day closer to our prey.
- Fixed a blank building interior bug
- Fixed a possible squad disappearance bug

### 0.98.44

- Mini patch to add some more debug data, for it seems the random crash
  still plagues us after all.  I shall call it: Crash X

### 0.98.43

- Hotfix for a new, different crash

### 0.98.42

- Finally finished distributing all the Cross grade weapons in the
  world.  Most of it's in the new map area, but a couple have been moved
  around in the current zone.
- Fixed that random crash that has been plaguing us for ages
- Fixed old squads suddenly appearing from nowhere or duplicating on
  imports

### 0.98.41

- Added a new option to control town assault frequency. Not the events,
  but the bandits passing by who try to conquer your town.  Realised the
  old option wasn't working properly.
- It can also be disabled completely.  It defaults to \[Normal\].  For
  reference, the raid frequency before now was the one named \[High\],
  so the default should now be a little calmer.  \[Bombardment\] has no
  limits whatsoever, so anything could happen.
- Improved some of the audio ambience for the buildings
- Fixed a saving bug

#### WEAPON REBALANCE

All this rebalancing has not been heavily tested yet, so I appreciate
feedback.

- Katana types now have a penalty to armour penetration, to compensate
  for their superior speed and lightness
- Katanas have a 10% damage bonus vs humans, but a 50% penalty against
  robots
- Hacker types have a bonus to armour penetration, because that's what
  they're all about.
- Polearms do more damage

#### ARMOUR REBALANCE

The idea was to mix things up a little so instead of some armours being
better or worse it's now more balanced, the stronger ones have more
weaknesses, and the weaker ones have more strengths.

- Heavy armours now have slightly reduced coverage.  No heavy plate
  armour can have 100% coverage on a bodypart, to reflect the gaps in
  the plates.
- Heavy and plate armour now pretty much makes stealth skills
  impossible, and give a penalty to crossbow skills due to being more
  cumbersome
- Chainmail now slows your combat speed slightly, and is a little worse
  for stealth, the blackened mail is no longer ridiculously better than
  the others
- Medium and light armours now have less cut-converted-into-stun damage
  penalty, especially the coats and leather shirts
- Plated Rags are now better for stealth
- Lots of other stat tweaks and changes that you will have to find on
  your own.

### 0.98.40

- Hotfix for the autosave loop issue

### 0.98.39

- New savegame system, saving should now be much faster, especially on
  non-SSD type drives.
- Slaver cage warden now puts dead slaves in the disposal instead of
  just carrying them around forever
- Slavers notice if you try stealing slaves by carrying them away
- Stopped slavers stealing from player cages
- Fixed a case where robot limbs didn't get healed if you didn't have a
  medkit
- Fixed a case where you would be paralysed if someone released you from
  a prisoner pole
- Stopped being able to place buildings that create towns in ruins
- Added some internal data tracking stuff to help hunt down one
  particular random crash we are getting

### 0.98.38

- Oh man, the town override world reaction stuff wasn't in that last
  update either, cus I forgot I had it disabled in release mode. It's in
  the game for sure now though, for sure.

<!-- -->

- Town overrides and roaming squads for world states. Added the Holy
  Nation, United Cities and Traders Guild. This means that the world now
  reacts to your actions i.e. if you take down certain leaders or
  capture powerful bounties. You can talk to allied faction leaders for
  hints on how to destroy enemy factions (so far that's Moll/ Esata/
  Simion) 

<!-- -->

- Arrange buttons added to more containers
- AI fix when a player outpost is too close to a town

### 0.98.37

- My mistake, the town override and world reaction stuff wasn't included
  in the last update, it's in there now.
- AI Campaign leader should now wait for the rest of his forces to catch
  up before attacking the target town

FIXES

- Fix for cannibals not healing random prisoners because they were
  planning to eat them but not for a long time.
- Fix for campaign AI when the target town vanishes
- Fixed the missing animation when running in stealth mode while
  carrying someone
- Fixed items thinking they were indoors if dropped on a building's ramp
- Dialogue crowd trigger doesn't affect people already saying something
  (endless loop fix)
- Fixed a bug with UTF-8 squad names
- Fixed player town handle and coverage data not being saved, which
  should fix a bunch of small bugs, including one of the "walking
  through walls" issues
- A couple of stability fixes

### 0.98.36

- Town overrides and roaming squads for world states. Added the Holy
  Nation, United Cities and Traders Guild. This means that the world now
  reacts to your actions i.e. if you take down certain leaders or
  capture powerful bounties. You can talk to allied faction leaders for
  hints on how to destroy enemy factions (so far that's Moll/ Esata/
  Simion)
- Blood splat size is now based on damage
- You can now pickup allied npcs to help injured slaves escape
- Added different blueprint item colors for different types of item
- Selected player characters can have different map marker colour
- Some fixes to popup menu on carried characters
- Map item crash fix
- A bunch of character movement fixes
- Fixed unselectable spotlights mounted on Gate III
- Fixed campaigns never leaving on victory
- Fixed unlock sound continually triggering
- Fixed crash dragging last research item when research completes

### 0.98.35

- The extra stun damage % in armour also now applies to pierce damage. 
  Means that heavy armour guys still get a little stun damage from
  crossbows
- fixed non bandits and cannibals not detecting prison escapes
- Stopped blood drips under water
- Fix for engineer job conflicts with resource ditching
- Fixed a few more bugs that could break AI campaigns
- Engineer job now ignores jobs that are outside of closed gates
- Increased stat-penalty light levels tolerance, so it doesn't have to
  be so bright
- Fixed illegal goods fencing tooltip
- Added extra checks to prevent animals spawning in nests on top of
  player
- Fixed some characters not floating in water when unconcious
- Fixed police not healing prisoners
- Fixed prison sentence time tooltip
- Fixed character position when exiting cages

### 0.98.34

- More fixes to the campaign AI, fixed premature retreats and
  cancellations when changing target
- Fixed that bug where you would randomly see corrupted geometry flash
  up on the screen
- Cannibals should now heal their captives if carrying them on a long
  journey
- Fixed Luquin
- Fixed Rebirth guards not catching escaping slaves
- Fixed a crash with a certain map item
- Fixed some escaped slave NPCs still getting tagged as escaped
  prisoners

### 0.98.33

- Re-Jiggered the map item system. Maps are now more useful, they will
  always unlock different locations to the ones you already know. There
  are now better maps in the shops that can specifially show you where
  to potentially find Ancient Science books or Engineering Research or
  whatever you are looking for.
- It's now possible to lose your pursuers properly.  Before, when you
  were caught stealing or sneaking they would track you artificially
  wherever you ran.  Now they will only be able to remember where they
  saw you last, plus a bit of extra projection (he went thataway), then
  they lose the trail.
- Changed the auto eject intruders AI to a normal job assigned from the
  context menu.
- Fixed auto eject job from forcing walk mode.
- Added an auto eject job for throwing out of buildings, if you have a
  building in another factions town.
- AI no longer shoots at crawling characters with turrets.  This way
  when bandits take over your base and pile your guys outside the gate
  you can crawl away without getting shot by the turrets.
- Changed medical state for robots from "Unconscious" to "Rebooting".
- Some AI improvements to the occupy town behaviors.  Bandits often
  thought they had occupied a town prematurely.
- If your town has been occupied by bandits it no longer deters hostile
  campaign events.  It still deters non-hostile ones, like traders and
  taxmen, so you don't get in trouble when the bandits don't pay your
  taxes.
- Crawling characters will now get up (if they can) when they are under
  attack.
- Medical tooltips now show the point at which you will die, useful when
  you have a worn-out robot character and don't know what his HP is.
- Rain collector no longer works in acid rain.
- Research and crafting queues are now re-orderable with drag and drop.

#### FIXES

- Fixed the hydroponic farms just giving 1 item per plant, instead of 2
  or 3.
- Stopped being able to snap buildings to structures you don't own.
- Another medic/robotics AI fix.
- Slightly improved turret snap node selection.
- Fixed bodyguard squad map markers becoming the wrong colour when
  platoon unloaded.
- Additional logging in game launcher for debug purposes.

### 0.98.32

- Added a pause button to incomplete buildings so that you can put them
  on hold and your engineers will build other stuff instead
- Player characters can now automatically throw KO intruders out of the
  base (check AI options)
- Fixed campaigns going to empty bases, and they could get confused if
  you had 2 bases in the same active area and one was empty.  They can
  now redirect too.
- Fixed AI bug relating to distance with the turret jobs
- Turret gunners should feed themselves properly now
- Stopped characters with the "rescue" job from rescuing dead allies and
  putting them in beds
- Fixed the Yabuta bandits existing in the desert before you have freed
  Yabuta (requires import)
- Fixed a medic AI bug (usually with slavers)
- "Ditching resources" task now includes raw meat
- Fixed a thievery XP exploit

### 0.98.31

- You can now select a carried character and use the context menu to
  "Put down" on the portrait, instead of having to hunt down which of
  your characters was carrying them
- Fixed bug with armour crafting material costs being too low
- Made the pack bull less slow
- Your stealing chance will now be tested against the nearest victim on
  the same floor, which will fix some situations where you got a
  too-easy steal chance because an npc was directly above you
- Fixed the carry animation when running at high speeds
- Tweaked model for the short cleaver 
- Fixed attack selection distance bugs for scaled up animals like the
  megaraptor
- Boots are now dropped when both legs are lost
- Boots are now refreshed when attaching robot limb if wearing one boot
- Splint kits now disappear when used up
- 2 crash fixes
- Fencing an item now also factors in if the victim was from the same
  town, not just the same faction

### 0.98.30

- Re-added Toppers (weapon and blueprint) to the game, though they are
  rare
- Added toughness as a bonus stat for Hivers, to compensate for low HP
  and reflect their spindly downtrodden insecty natures.
- Sped up crop harvest speeds a bit
- UC farm shops now sell a more global selection of crops
- Reduced encumbrance and injury dodge penalties so martial artists
  don't become sitting ducks
- Fixed the base translation gamedata.pot being in french
- Fixed slavers unable to tag you as an obedient slave when in stealth
  mode
- Fixed slavers and police destroying your items when trying to store
  them
- A fix with the NPC AI getting confused when healing you when you have
  a robot limb
- NPC captors can now heal robots
- Importing a game no longer resets the "Day"
- Fixed martial arts skill in the main GUI displaying the base stat
  instead of the derived
- Fixed Seto not joining you when you give the bugmaster to the shek
- Fixed player HOLD AI so that when you give a specific attack order
  they move forward to reach the target
- Fixed farmer skill calculation on crop yield display
- Fixed some more termite issues
- Fixed some wall AI bugs
- Fixed a bug/exploit where you could get stealth XP in your own
  buildings
- Fixed another AI running off miles away to attack someone bug
- Fixed thievery checks being skipped if wearing full backpack
- Fixed characters playing dead skipping thief dialog event
- Missing directx dependencies error caught with more relevant message
- Russian language updated

### 0.98.29

- Crossbow crafting playtested and fine tuned
- Moved crossbow parts and spring stell crafting to the arrow bench
- Fixed more the AI for crossbow crafting
- Fixed the predicted quality GUI for crossbow crafting
- Fixed crossbow crafting using wrong ingredients and wrong rates
- Added some acid resistance to the chain hoods
- Fixed mouseover in character stats panel
- Fixed characters teleporting to different floors when exiting beds and
  cages
- Player cage default action is no longer PICK_LOCK

### 0.98.28

- Tuned some of the stat penalties, ranged stats should get less severe
  penalties for injuries and hunger, friendly fire should be less of a
  problem
- Added a crossbow storage locker
- Fixed an AI bug with engineers collecting resources from the ground
- Fixed the "forage animals" AI job
- Fixed the AI bug with the crossbow parts storage box
- Rebalanced ore mines (drill was slower than the manual rocks)
- Fixed characters dropping their carried allies/prisoners to go and
  have a sit down
- Characters in offscreen update mode stop and switch modes at screen
  edges (fixes suddenly appearing onscreen, which looks like
  teleporting/spawning)
- Fixed patrolling characters going into some buildings when they
  shouldn't
- A few rare pathing fixes
- A rare crash fix
- Spanish translation updated (65% complete)

### 0.98.27 Posted On May 15, 2018

- Crossbow damage increased by around 20%
- Crossbows now affected by the global combat damage multiplier
- Crossbow global damage multipliers added to FCS
- When you select a character who is being carried by another player
  character, you will give orders to the carrier instead
- Shop guards don't track your position when they can't see or hear you,
  they go by your last known position
- Fixed a freeze when you press CONFIRM in the character editor that
  increases in size based on how long you spent on your character, if
  blood was enabled
- Severed limbs on the ground disappear after 24 hours
- Fixed ally campaigns, where allied factions came to support you
  against a common enemy campaign but left too soon
- Fixed the import with "NPC states" causing previously encountered
  living NPCs to be missing (requires re-import to fix)

### 0.98.26

- Added a target distance influence to the "protect allies" AI
- Police no longer take your weapons when you are arrested (unless they
  were stolen)
- Police only confiscate stolen items if they are recently stolen, and
  not stolen from a bandit
- Fixed another AI problem where escaped slaves and prisoners could be
  "magically" spotted by police
- Fixed hostile campaigns not looting food
- Fixed AI stealing building materials from towns
- Fixed player AI not auto-using beds
- Fixed player idle AI all trying to sit in the same chair
- Fixed player characters trying to sleep in NPC beds
- Fixed characters attacking police when released from prison if in HOLD
  mode
- Fixed items disappearing from animal inventory if right clicked when
  your inventory is full
- Fixed characters not attacking when ordered
- Fixed another termites bug
- Character sleeping position not affected by character height
- Fixed shackles display bug on single robot legs
- Fixed crossbow range, dodge, and hunger rate tooltips
- Stopped animals patrolling towns from going indoors
- German translation updated

### 0.98.25 Posted On May 8, 2018

- Hunger rate now varies with activity:
- Running around while encumbered or fighting with very heavy weapons
  will make you get hungry faster
- Working at mines will make you get hungry faster
- Sitting around will make you use less enery and get hungry slower
- Added options sliders to adjust frequency and size of base attacks and
  AI campaigns
- Toughness XP gain rate reduced by a third, setting added in FCS
- You now get some toughness XP when you lose a limb
- Fixed dead people screaming
- Fixed a bug where an NPC you did a crime to could magically see you
  afterwards even if you hid
- Fixed animals not eating foul meat from animal feeder
- Fixed NPCs getting stuck confiscating weapons if nothing to take
- Fixed slavers re-capturing slaves after you buy them
- Stopped mouse buttons 4 and 5 acting as left mouse button
- Fixed AI getting food from storage in NPC towns
- Fixed a crash

### 0.98.24

- Cost to buy buildings in towns has doubled
- Characters with damaged robot limbs won't keep trying to sleep it off
- Enabled stealing from prisoners, no thievery XP gains
- Fixed an AI bug preventing the Medic job from automatically healing
  NPC allies (eg hired mercs, fellow escapees)
- Import now has the option to import the unique NPC states, eg if
  you've killed phoenix, he will still be dead when you import your game
- Fixed characters getting Toughness XP when getting picked up
- Fixed Toughness damage resistance not being applied to armour's "cut
  to stun" damage
- Toughness damage resistance is now also applied to pierce damage
- Disabled putting items in dead animals
- Fixed raid announcement dialogs repeating
- Additional power requirement added to building upgrade tooltip
- A rare crashfix and some minor AI fixes

### 0.98.23 Posted On May 1, 2018

- Added various Hive world state reactions throughout the map if
  anything happens to the Hive queens
- You can now use the beds in ruins and bandit hideouts
- Characters with 1 robot leg now just wear 1 shoe
- Weapon "indoors" penalties no longer take effect inside massive
  buildings like the labs
- Fixed the NPC civil wars that kept breaking out, usually from the
  shinobi thieves

### 0.98.22

- Rebalanced AI vision ranges.  If the NPC is in the light and you are
  standing in darkness, he can't see you.  If he's in the darkness and
  you're in the light, you can be seen a mile away.  If you are both in
  the darkness you can be seen, but only if you are kind of close.
- Also AI can now hear you easier when you are not in stealth mode, if
  you are running around behind them.
- Fixed some campaigns not working or moving towards the destination
- Fixed rotating objects becoming unstable after an extremely long time
- Nest debris cleared when nest destroyed
- Fixed loading character shaved tag from save if set in gamedata
- Carried characters get dropped if left robotic arm is removed

### 0.98.21

- Fixed characters being carried at weird angles
- Tweaked the AI senses, you should be able to fight large outpost
  towers 1 floor at a time, more or less, instead of being mobbed by the
  whole tower
- NPCs outside of their building are no longer 100% blind to thievery,
  they can factor in range, with a penalty.  Unless the door is closed.
- clamped faction relations to +/-100
- another unjust wall termites fix
- Fixed building interiors randomly appearing in mid-air away from the
  town
- Fixed upstairs flickering when the camera is tracking a character on
  stairs
- fixed a bug that prevented certain campaigns triggering

### 0.98.20

- Fixed population multipliers affecting squads they shouldn't
- Fixed some bounties having no weapons
- 1 new male & 1 new female face
- Fixed the Purple Sands

### 0.98.19

- Fixed characters not getting food from the food store
- Looting shop counters now requires ALT-click
- Fixed town guards not attacking certain hostile factions
- Fixed the low blood of the mega-crab
- Fixed crossbow users unable to target neutrals
- Fixed a random crash

### 0.98.18

- Japanese language added
- Fixed prisoners not following/joining you when you free them.  Mainly
  affects Tengu's Vault.  (Needs import)
- Fixed the navmesh problems where towers couldn't be entered and whole
  zones were getting inaccessible
- Stopped town invaders doing your research for you
- Thinned out some of the heavy clustering of resource rocks that
  allowed extremely industrious mining and riches
- Stopped AI conflicts between the animal feeder and the food storage

### 0.98.17

- Blood trails fade out with bleed rate
- Prevented some loopholes where you could buy powerful NPCs from
  slavery and recruit them
- Fixed slavers not putting their slave loot in storage
- Fixed some items getting under the floor when dismantling
- Fixed crossbows sometimes not loading right and then not being able to
  shoot
- Fixed campaigns arriving and saying nothing
- Possible fix for shops running low on goods and money for some players
- Fixed a bug that could make a squad disappear
- Fixed characters sometimes walking through town walls when offscreen
- Fixed UC citizens reporting you for kidnapping when you try to turn in
  a faction enemy like the Phoenix, also fixed some of the bounty values
- Fixed Freedom Seekers start missing vegetable farms tech
- A fix for unjust wall termites (could still happen other ways, send us
  a savegame if it does)
- Fixed legless characters standing in cages

### 0.98.16

- Fixed depopulated towns when importing a game where you owned a
  building there
- Fixed the broken iron and copper prospecting & drill placement
- Fixed a random crash
- Fixed the crash on import
- Fixed characters incapable of speaking being able to talk to NPCs

### 0.98.15

- Added extra attack slots to large creatures so they can be hit by more
  attackers at once
- Fix for some AI bugs and the crafting window showing nothing

### 0.98.14

- German language now mostly finished except for wordswaps

#### FIXES

- Fixed the infinite loading bug
- Some small performance optimisations
- Fixed wounds not degenerating
- Fixed the characters still finishing their current order first when
  being given a new order
- Fix for the Mighty Canhead not attacking on arrival
- Fixed the icons coloring wrong
- Fixed a bug where wall placement would say "too close to a town"
- Fixed a few crashes that could happen from broken mods

### 0.98.13

- Fix for a game freeze and slowdown of swamp zone loading times

### 0.98.12

- Attack can now be shift-clicked to make a permanent-job, which
  basically puts the character into an "attack enemies on sight" mode 
- You now suffer bloodloss while an amputated limb goes un-bandaged
- Wall termites- A check to see if you've sealed up your town with walls
  and no gates, it will destroy some of your walls (to prevent a lot of
  bugs that would happen, and because it's cheating)
- Health is clamped so it cant go lower than 3x -max health
- NPCs relying on dialog events to attack you are now more alert because
  they can be triggered by sound
- Fixed the tent materials to be double-sided
- Fixes for characters stopping when moving long distances
- Fixed a bug with the robot limb HP when re-equipping
- Fixed a game freeze when picking up NPCs sometimes
- Stopped _DEAD_SQUAD__ appearing on import game
- Gear inventory icons are now colorised
- Removed an erroneous raid that made the anti slavers attack you just
  for being an ally of UC or HN factions

### 0.98.11

- Lowered the lock lvl of ancient safes to compensate for the lockpick
  limits.  Regular safes are still the same though
- Fixed a bug where butchery items could cause deaths
- Fixed player characters AI accidentally stealing items from towns
- Fixed a critical slowdown bug that could occur at random situations
- A few more fixes for AI medics in HOLD mode
- Fixed crazy stealth multiplier on the Armoured face plates
- Fixed not being able to dismantle camps built inside ruins
- Fixed some gui scaling issues when the window changes size
- Attempt to fix utf-8 save file names
- Advanced options panel shows previously saved values when importing

### 0.98.10 Posted On Feb 28, 2018

- You can no longer attempt to pick locks that are beyond your skill
  level (if it's less than 5% success chance)
- Added cheaper robot repair kits.  It's false economy though, you don't
  get as much for your money
- Robot limbs now store their HP and damages.  They wont give you a
  damaged leg when you first equip one, or do confusing stuff when
  un-equipping.
- HOLD position mode now limits the range of the medic jobs
- Possible fix for characters in HOLD mode getting all the aggro from
  enemies, and the aggro confusing medics.  Hard to test though, so not
  sure what will happen this time.
- Some other AI control tweaks, like not going back into your
  bandit-occupied town to get food
- Weapons "indoors penalty" no longer factors in the weapons bonuses
  when indoors (basically its a bit harsher now)

#### FIXES

- Fixed empty food items staying in inventory because there was still a
  crumb left behind
- Another AI tweak to stop characters running off to fight far away
  targets
- Fixed animals not getting butchered properly
- Skeleton bed now heals everything
- Fixed campaign AI so that they go home if your town is occupied by
  bandits
- Fixed bandit town occupation so it doesn't count bandits as occupiers
  when they are out of the town
- Fixed some cases of disappearing bandit corpses
- Fixed some campaign triggers getting missed

### 0.98.9

- Added a rain collector building
- Pet dogs prioritise combat actions over playing with severed limbs
  once they reach about 30-40% of fully grown
- Characters will now pickup items they need from the floor eg to find
  building materials or to fill a storage box
- If you build a furnace and set someone to work at it they will pick up
  all the severed limbs lying around and dispose of them
- Bodyguard orders are now always counted as a permanent job
- Stopped the fogmen swarming Mongrel to eat its prisoners
- Fixed right-click order to designate target when shooting from a
  turret
- Items dropped when dismantling buildings don't get put in invalid
  places
- Fixed used up items not dissapearing from backpacks
- Stopped buyback of stolen goods triggering fencing check if allied
  with the faction you stole it from
- Fixed portraits for characters with crouched idle stance
- Fixed robot characters being hungry when using rock bottom start

### 0.98.8

- Added some improvements to prevent campaigns blaming you when they are
  defeated by a 3rd party on the way to your base
- Made some adjustments to prevent passing bandit squads from constantly
  assaulting your town, though it still should happen often, it
  shouldn't be so relentless now.  Need your feedback for further
  adjustments.
- Archers won't shoot at people playing dead
- Fixed animals not aging to 100%
- Fixed animals eating a limb and getting so much nutrition they don't
  need to eat for months
- Fixed adult dogs not fetching severed limbs
- Characters can no longer eat more than 50nu of food in one go

### 0.98.7

- Characters now get covered in blood
- Animals stats are now reduced to 25% when you buy one.  This is
  because animals grew into high stats by default, so they were
  overpowered because those high stats weren't earned through combat,
  just time.  Now they have to be trained up like everybody else.  This
  doesn't apply to strength and dex, so they still get big and strong
  naturally without training, just the skills need to be trained.
- Adult player dogs no longer play with limbs, though they still collect
  limbs and carry them around a bit, they eat them quickly and don't run
  off. Adult wild dogs still run off with limbs.
- it now takes about 20 seconds for a bandit to butcher your pet dog, so
  you have a chance to stop him
- Characters won't sit around idle if they are selected
- Being in HOLD mode while sneaking no longer ruins your sneaking
- Fixed "use turret" orders not working when too far away
- Changed the ranged combat target selection function to be more
  flexible, let me know if things improve or not with target selection
- Fixed a miscalculation in the strength XP gain rate for encumbered
  martial arts combat.  It was like 10x too high, now it's the same
  rates as using a heavy weapon.
- Fixed the FCS character random weapon selection
- Possible missing wordswap fix
- AI improvements for town guards roaming too far from town
- Possible AI fix to help stop Shark getting wiped out by spiders

### 0.98.6

- Fixed bodyguard-type NPCs having x-ray vision and running off
  attacking every enemy in the area
- Fixed public beds being free to use
- Fixed the ammobox being really tiny
- Stopped characters under "hold position" mode running to open doors in
  combat

### 0.98.5

- Added Thievery Training box and a tier 3 lockpick training box.  You
  need awkward materials to build them though.
- Potential fix for the clothing display bug on AMD cards
- Fix for shop keepers going missing
- Fixed crash picking up corpses
- Fixed a bug with town gates not getting opened
- Fixed holy nation slavers constantly re-dressing slaves
- NPCs are less aggressive about healing KO'ed neutrals, they won't bash
  down your gates to heal your enemies for example
- Fixed crash in crafting list window

### 0.98.4

- Should fix issue some were having with AI not doing production jobs
- Fixed robot limb health clamping to 100 when loading a game
- fixed being unable to dismantle camping stuff when built indoors
- Fixed another AI bug with the sitting when idle going into other
  peoples buildings and triggering out of home town
- Fixed GUI having excess line spaces at larger text sizes
- Possible fix for a crash when selecting Garru
- Fixed crash when finishing crossbow crafting
- Stopped pet dogs from eating corpses (they just eat limbs now)
- Removed accidental mods

### 0.98.3

- Fixed the Ammobox that I threw together too fast
- Fixed an AI bug with the sitting when idle
- Prevented idle sitting when in hold position mode
- Fixed robot limb health clamping to 100 when loading a game
- Fixed the slavers "gathering slaves for shipping" AI
- Portugese translation complete

### 0.98.2

- Tweaked crossbow crafting costs

<!-- -->

- Added storages for crossbow parts and ammo

#### FIXES

- Fixed the blank inventory icons
- Fixed the UC guards killing all the Thieves and Tech Hunter shop
  owners, resulting in empty shops
- Fixed the armor & clothing craft benches not working
- Fixed a crash on startup for AMD cards (possibly... we don't have any
  AMD cards to try it on)
- Fixed some mods crashing the game
- Fixed a bug causing everyone in bandit squads to have crossbows,
  instead of a small percentage
- Fixed construction set translation mode skipping character names

### 0.98.1

- Fixed the tent blueprints not unlocking
- You now get a small amount of dexterity XP from reloading
- Fixed some of the bad automatic inventory icons
- Fixed AI bug when trying to fight with a broken right arm

### 0.98.0 Posted On Feb 27, 2018

- It's the best update ever. It adds and tweaks a lot of things that
  together change the game experience a bit. It's a good time to try
  starting a new game if you were thinking about it.

#### BIG FEATURES

##### BLOOMIN' ROBOT LIMBS!

- when a limb goes below -100 damage, that limb gets amputated
- lost legs means you have to crawl on the floor
- Legs damaged past your KO point also makes you crawl on the floor,
  until they are bandaged.
- robot limbs can be added or removed at a Skeleton Bed
- robot limbs will affect your stats in various ways
- If you are crawling around on the floor you can still fight really
  badly as long as you have at least 1 arm.
- Your amputated limb goes flying through the air.  Dogs will run off
  with it.
- If your pet dog finds a limb he'll get all defensive and keep running
  away with it until he finally eats it.  Only happens with young dogs,
  so don't worry he will grow out of it eventually.
- Limb loss can be reduced or disabled in the options

##### FLIPPIN' CROSSBOWS!

- Crossbow shops dotted around the world
- You need ammo too
- Crossbows and ammo can be crafted in your base

##### BLOOD!

- Blooooood!
- Blood gets sprayed on the ground
- People get covered in blood
- Blood pools grow around people who are bleeding out
- Crawling and bleeding people leave a bloody slug trail behind them. So
  fun.
- 18 new beards and 17 new hairs added to the game.  Credit goes to
  Arkhiel for generously donating them.
- New hand-painted inventory item icons.  Credit goes to Diogo Santos
  for making them.
- Some roaming bandit squads will assault your base and attempt to
  capture it.  If they win they will throw you out and live there
  themselves, use your stuff, eat all your food.  You will have to
  remove them by force to get your base back.
- HOLD button replaces the PASSIVE button.  This puts characters into
  "hold position" mode.  Stops your characters running off to fight, but
  now they still fight anything that comes in range. You can use this to
  position melee guys tactically, to protect your bow units for example,
  or guard a doorway.  Also still serves its original purpose of keeping
  your weak workers away from combat.

#### FEATURES

- When playing dead, you can switch to stealth mode and crawl around on
  the ground giving your buddies first aid or trying to escape without
  getting noticed
- The travel shops now sell tent blueprints.  These can protect you from
  acid rain when you are camping.
- Slavers and Traders guilds have near 0 relations multiplier, so
  fighting them causes less relations loss but they assign bounties to
  you instead
- Swearing filter is now removed from the game, but is still available
  in the options
- Hivers now have proper face morphs for the character editor, they can
  have more variety now, go and give all your hivers plastic surgery cus
  they're funny
- When placing buildings, ramps can automatically change to the correct
  building for the snap target
- Bandits now loot more food and take meat from downed animals, meaning
  they will eat your dog.
- Idle characters now sit around on chairs in your home base.  Looks
  nice, and is a handy way to keep track of who's idle.
- Using training equipment can now be set as a perma-job
- Confirmation message added for when selling stolen items, to prevent
  accidents
- New keybinds added for stuff in the "orders" panel
- "Perception" stat added, affects accuracy with shooting in general
- "Precision shooting" stat added, affects friendly fire chance
- "Lockpicking" stat added, separated now from the "Thievery" stat,
  which now just covers stealing.  This means that all your characters
  don't end up inadvertently becoming specialised thieves as a result of
  escaping cages.
- Thievery stat XP rate is doubled to compensate for the stat division. 
  Lockpicking rate is the same.
- "Crossbow smithing" stat added for crafting bows and ammo

#### TWEAKS

- A new AI sensory system change means that your squad now has to rely
  on line of sight, which should hopefully stop them running off over
  the hills to fight enemies
- The Fog Islands have better natural resources, so it's now a nice
  place to build.  It's lovely, you should move there.
- Damaged robot limbs don't degenerate
- You now get a combat XP bonus when a character fights outnumbered
- Disguises don't count as disguises unless they reach over 40%
- Skimmers are less edible
- The "strong" new recruits are now weaker, because thats the spirit of
  the game.
- Chance of death default increased 20%.  You guys aren't dying enough.
- You can now camp indoors in old buildings and ruins
- Overall toughness XP rate reduced by 28%
- Campfire is now automatic cooking
- Animals age 2x slower
- Robots and robotic limb damage is now healed instantly, but wear
  damage rate has been doubled, and first aid speed is 0.33x slower

#### ECONOMIC BALANCE

- Weapons and armour are now almost quarter of the price. I think they
  were so expensive I never bought anything, just looted and stole,
  missing out on the joys of shopping.
- Beefed up Armour King's security, because you guys shouldn't steal
  from him, the best armourer in the world, you should experience the
  joys of shopping.
- Gear loot sell price penalty reduced a little to compensate for the
  cheaper prices
- As a result of all the above, crafting gear is not so insanely
  profitable and riches are generally harder to come by
- Animal skin is worth 8x more money, and makes 4x more leather.  Hemp
  worth 2x more. 
- The prices of food have gone up 10% (because of Brexit)
- Shops close 2hrs later
- Stopped nearby towns having vastly different trade markups, trade
  profit margins are more distance based
- Improved the shops available in the great desert area
- Armour blueprints 50% more expensive
- Chainmail sheets are less profitable
- Beak Thing nests have more eggs, raiding them should be a profitable
  adventure

#### FIXES

- Fixed some bugs with the road based pathfinding
- Turns out all elder animals were running in the opposite direction of
  their pathfinders.  They were walking backwards cus they're old.
- Fixed path not changing when clicking on distant terrain more than
  once
- Fixed prisoners reacting violently when you bust them out of their
  cages and calling you "intruder"
- Fixed a bug with weapon stats within a manufacturing group all being
  the same
- Characters can use medkits from their backpack
- Fixed negative vendor money due to faction prosperity
- Disabled ordering animals to pick up items
- Slavers don't magically know when a slave has removed their shackles
  when they are in a cage
- Follow task leaves animals outside
- visiting taxmen etc getting attacked by bandits won't trigger a base
  assault
- Fixed AI for the Splint job
- Fixed AI continually stopping and starting crafting jobs
- Fixed some bugs with the AI getting stuck with certain complex
  combinations of perma-jobs
- Unconcious check for flashing portraits
- Fixed some bugs with the dialog system picking the wrong target race
  or changing dialog targets to the wrong person
- Fixed screen labels never disappearing
- Fixed potentially infinite wolves
- Fixed building limited item stack limits being wrong for some items
- Fixed retreating campaign squads constantly activating when defeated
- Fixed not being able to build in the corner of a sloping stationhouse
- Stopped AI trying to put items in unbuilt buildings
- An improvement to the spawning distribution of squads when multiple
  separate map areas are active
- Fixed some disappearing prisoners
- Fixed walls getting incorrect gatecode if next to a building.
- A few audio bugs have been fixed
- Fixed issues with prisoners going missing when the map is unloaded
- Fixed a stealth XP exploit
- Finally made a proper ragdoll for the Skimmers. I hate making
  ragdolls.
- You can no longer build furniture inside incomplete buildings
- Fixed slavemasters only gathering 1 slave for work
- A few tweaks to the navmesh system
- Lots of small bugs, tweaks and crashes fixed
- Lots of new bugs and crashes added to replace the ones that we fixed

#### FCS

- Fixed a bug with the word count in translation mode not including
  translations of deleted source lines
- Enabled creating new wordswaps in translation mode
- Fixed crash in certain older windows versions

## 0.97

### 0.97.6 Posted On Oct 18, 2017

- Degeneration rate of red damage that is above the 0 mark is halved
- More fixes for slavery AI
- Updated medical panel GUI to cover the new wound degeneration
- fixed a stealing exploit

### 0.97.5

- Bunch of fixes for slavery AI
- AI panel options kept on import game
- Fixed crash building walls
- No corpse flies or smell on dead robots

### 0.97.4

- Increased chance of death re-balance (I'm trying to make people die
  more):
  - Bleeding speed reduced by 33%, but blood clots 50% slower (extra
    bloodloss, but more time to treat it, but more dangerous when left
    untreated)
  - blood regenerates 33% faster (so recovery times are the same)
  - untreated (red) damage degenerates even when the body part is above
    0 health, but at half the speed
  - injuries overall degenerate 1.5x faster, but the rate is based on
    the amount of red damage
  - KO time slightly reduced
- Small content teaks and additions to the new map area:
  - Added a thing to Darkfinger
  - Added a different thing to Sinkuun
  - Added something awesome to the Deadlands
- Skimmers much stronger, but move in smaller groups.  Made the ambushes
  work properly
- Inventory shift right-click now transfers entire item stack
- Tweaks to some armour values
- Fixed the animal feeder having a tiny capacity
- Fixed slave traders busting down your door to steal your slaves
- Fixed a bunch of pathfinder bugs that were making characters stop
  mid-journey
- Stopped animal limbs from going ragdoll, cus it looked stupid

### 0.97.3

- Increased HP of soldier/worker hiver heads, both to reflect their bony
  appearance and to compensate for inability to wear helmets
- Restricted a few more headgear items for hive workers
- Put more in place to stop taxman visits if you leave your base
- Stopped characters getting resources and food to eat from shop
  counters
- Fixed ragdolls not colliding with foliage rocks
- Fixed a bug where the overhead attack sometimes went undetected and
  got through a characters defences
- Fixed gate-code bug when wall ramps are loaded
- Fixed crafting building crash when recipe has fewer items
- Flies sound actually stops at a distance (still needs attenuation)
- Fixed dead npcs not being saved

### 0.97.2

- A bunch of level fixes like repositioning buildings, fixing blockages
  etc
- Added some Iron and Copper resources to a few of the new map zones
- added bull backpacks back to the holy farms
- Reduced faction penalties in Narko's Trap
- Megabeasts made stronger
- Slave towns no longer hostile on sight
- Tengu's Vault now hostile on sight
- A few more small bug fixes

### 0.97.1

- Fix for engineer job not fetching building materials
- Mainly just crashfixes

### 0.97.0

- Freakin' new map section released!
- Skeletons now accumulate small amounts of wear and tear damage as they
  get repaired over and over.  This wear damage can be repaired at a
  Skeleton Repair Bed.
- Destroyed buildings now cost 50% more to buy
- Fixed artifacts disappearing from shops (like the ancient science
  books)
- Stopped items disappearing from crafting buildings when recipe changes
- Improved lag with ragdolls going to sleep (when many ragdolls)
- Fixed crash dismantling buildings
- Bunch of small fixes and tweaks

## 0.96

### 0.96.27

- Slightly reduced upper tier heavy armour resistance, to make the top
  tiers less overpowered
- Regenerated world navmesh to speed up zone loading times
- Improved navmesh splicing (whatever that means)
- Changed physics xml and bin files to use Ogre resource manager (fixes
  steam mods)

### 0.96.26

- another hotfix for the slowdown problem

### 0.96.25

- hotfix for the engineering job not fetching building materials

### 0.96.24

- (Fix) Dogs and goats can now eat food off the ground
- Dogs can now eat straight out of the food storage.  While working on
  this my dog ran around my base and ate my entire stockpile of food,
  metal plates and buildings materials.  Fixed that too.
- Added a special animal feeding barrel.
- Fixed not being able to go on roofs
- Fixed a potential heavy lag bug

### 0.96.23

- Hotfix for a crash
- Updated translation base data

### 0.96.22

- Animals will eat food dropped on the ground
- Animals will eat food out of the storages at your home base, if "feed
  animals" is enabled in the AI options
- Pretty sure that the goats were eating themselves
- Some small fixes

### 0.96.21

- Artifact distribution has been tweaked, there should be less of a
  shortage of AI cores and science books
- Tweaked dust settle amounts
- Stopped mounted buildings in towns from creating player outposts
  inside the NPC town
- Fixed character name tags appearing in character editor
- Stability fixes

### 0.96.20

- Added font size option slider
- Fixed a bug where NPCs could sometimes get moved through walls when
  running off-screen. This was the bug many people thought was enemies
  spawning in their bases. Should now be fixed.
- Fix for spazzy animal animation bugs, especially for leviathans
- Few fixes for windmill audio
- Fixed corpse flies audio positioning
- Fixed expand stats button appearing when gui is hidden
- Fixed paladins not having their gear set as uniforms

### 0.96.19

- Hotfix for the farm growth rate bug caused by an optimisation in
  0.96.18
- Fixed the Rebirth slave delivery AI

### 0.96.18

- fixed the random lag problem from 0.96.17
- tweaked the medic AI so it shouldn't run off too far
- Fixed crash when approaching a certain village
- Bit of memory clean up for stray homeless squads
- Altered the player AI to choose nicer beds to sleep in
- stopped medkits increasing charges when skill is \> 100
- unique NPCs that escape captivity can now travel all the way back home
  to resume their lives
- Fixed foliage showing inside the ancient lab
- Fixed escape menu fade out not being full screen
- Fixed expand stats button becoming stuck on screen
- Fixed a crash on exit for turrets

### 0.96.17

- Cannibals weren't eating people because they would rather sit down and
  relax.  Fixed that now, prepare for horror.
- Corpse flies sound integrated
- Wind generator sound intensity based on rotation speed
- Fixed again the hive trader not leaving after finishing his
  announcement
- Fixed characters sometimes moving while still getting up off the floor
- Fixed slope calculation for building placement
- Fixed a road following bug
- Sound emitter fixes
- Fixed preview building usage nodes becoming invalid if you change
  floor
- Fixed select all button sometimes switching squads
- Fixed portraits and squad tabs never flashing
- Fixed dead characters not updating if no living characters are left

### 0.96.16

- Fixed a crash in the campaign system
- Possible fix for that flickering AI medic bug
- Small improvement to building/navmesh complications
- Fixed being eaten by spiders not updating appearance of dead bodies
  (sucking them dry)
- Bodies don't disappear so fast when being eaten by spiders 
- Squad panel drop target hidden to make reordering squads easier
- Fix for AI trying to heal animals with large navmesh footprint

### 0.96.15

- Fixed excessive numbers of free wanderers joining your base
  (hopefully, it should be super rare, let me know if not)
- Stopped hive traders visiting too frequently
- Other fixes related to AI campaign frequency
- Fixed physics attachments being duplicated
- Fixed a bed usage bug

### 0.96.14

- Fixed the hive traders not leaving, and getting hostile
- Fixed the faction arrival message spam
- Stopped characters going to bed for rest if they are carrying someone
- Stopped wandering traders going to no-go zones (eg hiver caravan in
  holy nation)
- Mounted turrets and lights repositioned when parent building is
  upgraded
- Splinting now splints over blunt damage as well
- Splinting can also apply to non-limbs, to help counter work quality
  penalties when crafting etc.
- Fixed 'Put in bed' missing fron right click menu
- Biome title text does not appear when in town, so it doesn't keep
  triggering if you build on a biome border
- Orders, Crafting, Research and Squad lists maintain scroll offset when
  modified
- Character names can now contain wordswaps
- You now get back slightly more materials when you dismantle buildings,
  and the number has been added to the FCS global settings
- Fixed a situation where slavers or police could re-arrest you after
  releasing you from prison because they remember you're a criminal
- Fixed a bug in the campaign target selector that might have been
  bypassing the distance limits
- If a non-aggressive AI campaign (like the tax man) is defeated on the
  way to your base and you weren't involved then it won't trigger an
  aggressive response

### 0.96.13

- Added some race-specific foods. Hivers can eat raw and foul meat.
- Police no longer set imprisoned slaves free if they don't have a
  bounty
- Fixed up the slave shipment chain- slaver caravans gather up slaves
  and deliver to work camps.  "Freelance" hunters deliver them to the
  nearest slave shop.
- Tweaked some of the fertility altitudes for some biomes like Vain
- Reduced range of UC tax man
- Added missing inventory icon for martial artist bindings
- Fixed some damaged gamedata that caused a bunch of tiny bugs
- Fixed water depth bug for characters in ragdoll mode
- Fixed some prisoners not spawning in cages
- Fixed characters being invisible when spawned sitting
- Fixed direct orders to use beds

### 0.96.12

- Some of the katana attacks now have reduced max-hits per attack,
  meaning they are less effective against groups. (Mainly the downward
  combo, but I also increased the power a little, this makes katanas
  more of a duelists weapon.)
- Fixed bug where conversations cut out after an interjection
- Hive traders will sometimes visit your base
- Doubled cost of animals
- Shek slaves get their horns cut off
- Lowered the price mark-up on illegal goods in the SW empire towns, the
  idea is that you only get the huge markups when you travel far east to
  the new empire regions
- Fixed navmesh not always updating when building walls
- GUI updated if window size changes
- AI options load/save fix

### 0.96.11

- Fixed the stupidly big move marker
- Fixed the broken hydroponic farms from last update
- Fixed occasional non-aggressive robot spiders
- Fixed creating too many face morphs
- Fixed animal inventory window for different sized inventories
- Fixed interior edit mode floor visibility
- Disabled deleting parent building in interior edit mode

### 0.96.10

- Iron spiders have more iron plates and electrical components, to make
  them worth harvesting
- Tweaked farm fertility calculations
- Fixed missing face options in character editor
- Fixed some logic bugs in the dialog system
- Fixed battery drain amount
- Fixed stealing stuff without holding alt
- Fixed wall previews being red when valid
- Fixed outsideFurniture property when confirming multiple buildings at
  once
- Fixed indoor particles (again)
- Building sound emitters can stop if nobody is working

CONSTRUCTION SET

- Fixed crash loading translation with missing original line variant
- Fixed translation line disappearing if translated to empty
- Changed translation ORIGINAL_MODIFIED state colour to orange (easier
  to see)

### 0.96.9

- Added AI control options panel
- NPCs now have random faces
- Fixed floor number of dropped items
- Fixed mouse traces for items on upper floors
- Fixed visibility for items with no collision (Fancy Rug)

### 0.96.8

- Added some missing components for the Robotics Storage
- Improved the auto-sleeping AI bugs, not sure if it's perfect yet.
   Planning to add an AI control panel later on to enable/disable things
- Added missing combat skill effect to backpack tooltips
- Fixed inquisitors randomly attacking you when innocent
- Fixed a shadow artifact

### 0.96.7

- Halved the "water avoidance" factor in the pathfinding for player
  characters, let's see how it works out.
- Fixed unlock shackles action not working
- Kidnapping failure should now result in the victim getting up and
  attacking you properly
- Fixed a bug that could cause a possible persistent slowdown after a
  raid
- Fixed a possible crash if a player-given order is impossible in the
  first frame
- Fixed unbuilt lights contributing to light level
- Fixed empty faction list when importing
- Fixed a turret-related crash
- stopped potential infinite sound loop when loading a game mid-loop

### 0.96.6

BALANCES

- Sped up some production buildings
- Added automatic fabric looms tech to lvl 4
- Removed bread from Food Store
- If you upgrade a building that produces its own construction material
  (eg farms, iron refinery) then it will absorb its own inventory
  contents towards the upgrade cost

FIXES

- Fixed a dialogue bug that skipped relations and money checks
- Fixed a duplication bug in the grass system
- Fixed a rare NPC population duplication bug
- Possible fix for a turret upgrade related crash

### 0.96.5

- Characters automatically go to bed if they are wounded and have
  nothing else to do
- Characters automatically ditch any spare resource items in containers
  if they have nothing else to do or are stuck with their current job,
  this should free up some of the jams
- Player characters no longer automatically heal or help allies from
  other factions

FIXES

- Fixed some items not spawning in nests
- Fixed some loot items not spawning in nests
- Jobs mode now saves and loads properly
- You no longer get XP for stealing from prisoners
- Turret/light attachment nodes more visible
- Reduced max sloping value of all buildings
- The game now only autosaves once if you leave the game paused for ages
- Fixed AI tolerance for accessing a turret built with the wrong floor
  ID
- Fixed characters incorrectly falling over on load due to injury
- Fixed a possible startup crash
- Fixed null pointer crash with faction discovery
- Fixed some characters appearing on the floors above

### 0.96.4

- Hotfix!  .3 had a crash
- Added 2 new cannibal raid types

### 0.96.3

- Animal backpacks now have way more space, making them useful for
  setting up bases
- Beak things now have meat
- Made cannibals slightly weaker again, added more Beakthings to the
  Cannibal Plains
- Reduced the penalty for tresspassing
- Crime "Assault" doesn't override other crimes any more, so its easier
  to see what you did
- \[Jobs\] button also no longer skips follow and bodyguard jobs

FIXES

- EDITOR: Fixed crash opening translations
- Unbuilt (ie still passable) walls no longer make characters bounce
  over the top, and can be clicked through to select characters etc
- Fixed map items pointing to the wrong towns after import
- Fixed crash on dismantling buildings
- Fixed building audio "cavernous" setting not working right
- Fixed cannibals not properly capturing people if they were drawn out
  of their home town
- Fixed "He's in the water" bug when loading a game with ragdolled
  characters
- Fixed deadcat bar having no inventory
- Fixed the Empire taxman assault triggering when it wasn't supposed to
- Flipped the default setting for "Invert mouse Y", because people start
  the game without checking through the options first and then freak out
  because the camera is the wrong way around
- Fixed map item inventory sounds

### 0.96.2b

- Fixed the Automated Ore Mines research unlocking all 3 levels at once

### 0.96.2

- Construction shops now have blueprints for most of the decorative
  furniture like tables and carpets
- You can now build a lot closer to ruins
- Placing buildings now has an adjustable slope-matching setting, so you
  can make more upright buildings
- The disable jobs button now doesn't disable medical type jobs

FIXES

- Fixed a bug that was preventing victims from screaming when they were
  being eaten alive.
- Fixed furniture sometimes not being buildable above floor 0
- Fixed some talking animals
- Possible fix for escaping fog men tagging you as a criminal

### 0.96.1

- Fixed the "show markers" option not being saved properly
- Made the new hideous green markers a little more subtle.  Our artist
  is on holiday, he will fix them up nice when he gets back.

### 0.96.0

- Added character mouse movement and camera rotation markers (designed
  to help beginners, disable them in the options if you don't need them)
- Halved the athletics penalty of samurai armour
- The bread oven is now automated, but cooks at half the speed
- AI must get up before applying first aid
- Fixed arm ragdoll with damage from blocked punches
- Paried punch sound no longer metalic with sparks
- Added loading progress bar
- Fixed a potential rare AI bug with certain gates built on slopes

## 0.95

### 0.95.44

OPTIMISATION

- Huge terrain system optimisation, frame rate should be better when
  looking at the horizon now, and also more detailed. Unfortunately
  won't do much good for those with slow systems who already have the
  view distance and terrain detail way down.
- Secondary lod threshold for distant terrain
- Initial loading state continues until everything is loaded
- Changed slow startup load sequence to happen behind splashscreen logos
- Some general small optimisations to the code

FEATURES

- Replaced "chase" button with a "jobs" enable button, so you can stop
  your characters trying to run back to base to do their jobs when they
  are away from home
- Dropping an character who isn't an ally now knocks them out, to help
  with capturing slippery bounties
- Characters now prioritise eating higher-grade food first
- Mouse traces ignore collision of destroyed building walls
- Added some of the system messages to the dialogue log window

FIXES

- Added borderless option to ingame options
- Shop signs no longer clickable, causing characters to pathfind
  upstairs instead of to the ground floor
- Fixed crosbow strings flickering
- Fixed the non-aggressive armory spiders
- Fixed some missing cannibal village squads, and possible cannibal
  raids not activating
- Fixed a crash when loading games in the GOG release
- Fixed random flat foliage
- Rewritten interior building placement building collision checks
- Fixed corpse flies sometimes not appearing
- Fixed the random missing apostrophes
- Fixed placing buildings on top of foliage rocks with collision
- Fixed material when dismantling non instanced buildings
- Fixed buildings with offsets in build icons

### 0.95.43

- lights no longer consume power during the day
- made cannibals slightly stronger
- Reduced instances of town guards overzealously attacking you for
  tresspassing in private buildings
- Fixed town radius not expanding correctly (causes all sorts of weird
  problems)
- Fixed selling and buyback prices for stolen items
- You can now use medkits from your backpack
- Fixed item group placement orientations
- Right click menu on doors is only instant when locked
- Fixed duplicated node removal
- Fixed reversed animations not starting (specifically put down
  character)
- Fixed some patrols never starting
- Added 'I dont have a splint kit' character message
- Fixed characters colliding with who they are carrying (caused jitter
  on pickup)
- Added level editor save warning when player towns exist
- Fixed duplicated town nests when loading
- Fixed nests being diferent when loaded from ingame menu
- Fixed occupied nest cages being duplicated when loaded
- Fixed speed groups not being created for characters loaded in group
  speed mode
- Fixed harpoons being drawn before thier material is set up
- Added loading progress bar
- Fixed paying for beds again when loading
- Fullscreen mode re-enabled

### 0.95.42

- Fixed a bug that could potentially make a savegame crash on load

### 0.95.41

- Fixed bounty clearing immediately when you get put in jail, resulting
  in no GUI info
- Fixed Shek guards attacking you on sight because they remember
  something bad you did ages ago
- Turret accuracies tweaked to require more skill
- Turret max reload speed now more skill dependent because it no longer
  uses "accuracy perfect skill" to adjust
- Added missing acid protection to all the Plate Jackets
- Samurai body armour chest coverage changed from 90-\>100%
- Fixed random crash on loading mid-game

### 0.95.40

- Fix for anyone with fullscreen mode set in their cfg getting broken
  screen resolution
- gorillos are a bit stronger
- Fixed a case where animals could freeze in combat against someone in
  defensive mode
- Fixed the inability to path inside the metal warehouse building

### 0.95.39

- Temporarily disabled true fullscreen mode 'cus it's broken and I don't
  want new players getting confused

### 0.95.38

- Borderless window option added to the launcher. True fullscreen mode
  re-enabled.
- Fixed monitor selection sometimes not working
- Sped up the speed of sawing through shackles (and fixed a crash)
- River raptors in Okrans Pride mainly only spawn from nests now
- Fixed the goat ragdoll
- Removed a debug cheat game-start that was left in by accident

### 0.95.37

- Fixed the acidentally recruitable ninjas everywhere.  If you got any
  then you should free them back into the wild.
- Fixed the Y-house roof
- NPCs should now react properly when you free them from a prison
- Fixed the missing Megaraptor
- Fixed prisoners being immediately freed by law enforcers
- Added Shek guards to collect bounties from

### 0.95.36

- Can loot backpacks on the ground
- Acid damage changed to stun damage to prevent constant AI healing
  attempts
- Can only put empty backpacks inside other backpacks
- Fixed un-enterable armory in Mongrel
- Fixed placing characters in unbuilt beds and cages
- Fixed Task_UnlockDoor doing nothing for cages
- Fixed characters building nearby stuff without geting out of bed
- Fixed infinite nest population bug
- Player characters only get food from player owned containers
- Fixed dropped items appearing on the floor above in buildings with low
  ceilings

### 0.95.35

- "Imposter!" incidents should be a little less sensitive now
- Occupied cages in nests are saved
- Fixed incorrect build cost on cactus farms
- Implemented sound when dropping items
- Fixed nest random seed
- Fixed town nests not spawning
- Fixed bug replacing locked prisoner shackles with other footwear

### 0.95.34

- Fixed crash when using MEDIC button
- Fixed unequippable backpacks
- Stopped the "Help! I'm stuck" message (was supposed to be debug only,
  and animals were saying it)

### 0.95.33

- Sandstorms now affect attack stats, especially turret skills
- Gave a boost to the light value when calculating the stat penalty for
  working in darkness

FIXES

- Fixed acid rain not affecting characters
- Fixed races with different max health (hivers) suffering injury
  penalties to stealth
- Fixed holy mine slaves attacking you when you fight their masters
- AI doesn't try to flee if it is trapped within a locked building or
  closed walls.  They will resort to fighting instead, which will be
  good news if you are one of those weirdos that make slave battle
  arenas.
- Fixed possible gui threading crash with picking up items with alt held
- Fixed player town radius calculation (caused some AI bugs)
- Big animals don't go indoors
- Audio tweaks

### 0.95.32

- Fixed importing .po files from google translator toolkit to the
  construction set
- Remove town marker when all buildings dismantled
- Fixed reset tutorials crash
- Fixed crash in stolen goods tutorial

### 0.95.31

- More stability fixes
- Fixed faction relations not getting positive effects when joining eg
  Shinobi Thieves
- Fixed initial light state for lights on roofs
- Possible workaround for failing to detect video resolutions

### 0.95.30

- A few minor stability fixes
- Few fixes for nests like not re-loading buildings.
- Added option to delete savegames
- characters now fetch food when in owned buildings in other towns

### 0.95.29

- Fixed a bug with the trading range
- Fixed GUI display of the dodge skill calculations

### 0.95.28

- Added some missing AI cores to certain labs
- Fixed Ashlander Stormgoggles for the female mesh
- Fixed a thievery exploit that involved using a second character hidden
  far away out of sight
- Fixed crash moving characters between squads in grouped movement mode
- Fixed Tagelmust price being absurdly high
- A fix for upgrading farms
- Fixed importing games with purchased buildings
- Stopped town patroling squads from trespassing
- Added logging to detect incomplete gamedata from mod conflicts
- Corpse furnace job ignores targets that cannot be carried
- Fixed crash when calculating research time with broken gamedata
- Fixed crash when NPCs try to use player beds

### 0.95.27

- Player town now gets classified based on it's size and significance,
  which is reflected by the towns map icon and will later affect AI
  actions
- Slightly improved the weapons and armour for sale in Mongrel, added 2
  new recruits there
- Created the foundation systems of world state queries, which will be
  explained later in a blog post

FIXES

- Fixed a crash in one of the southern waystations
- Fixed weird case of buildings at outposts/ruins being assigned to
  nests and not populating the interiors
- Though I couldn't confirm it, I had reports of Stealth skill acting
  weak when it goes above 100, so I clamped the internal calculations to
  100 just to be sure
- Fixed the AI bar squads again

### 0.95.26

- Stopped acid burning your feet when indoors
- Stopped the empty context menus from popping up
- Fixed shop window showing when looting a character thats getting up
- Fixed Hub bar not reacting to thievery
- Fixed failed right-click looting when stealing equipped items
- Forced context menu on clicking cages and doors
- Hats automatically hidden in character editor face/hair tabs
- Fixed visual bug when multiple animals were trying to eat the same
  target

### 0.95.25

- Fixed cannibals never eating their captives, now they will eat one
  periodically, even if the cages aren't all full
- Fixed some missing squads + interiors in cannibal villages
- New map town icons
- Added SFX for picking up and dropping things
- Fixed the weird spark particle effect in combat
- Fixed apostrophes in text randomly appearing as big spaces
- Fixed right click combat sometimes not working
- Fixed crash creating navmesh for unloaded zone
- Fixed crash when dismantling
- Fixed dialogue system "give item" function
- Fixed characters not moving if loaded in group movement mode
- Fixed speedOverride causing npcs to run everywhere
- Overhauled the buy-back function when trading, fixes a few bugs
- Character appearance randomised on new game
- Enabled walking on top of furniture
- Improvements to the tutorials

### 0.95.24 (again, un-numbered)

- I accidentally included a test quicksave in the last patch which
  overwites the "quicksave" slot, this removes it to prevent any further
  save losses

### 0.95.24

- Hotfix for farm harvesting failing constantly
- Fixed calculations for harvest success chance
- added missing veg farns M and S

### 0.95.23

- Hotfix for the bugged character editor popup window that was
  preventing new games

### 0.95.22

FEATURES

- Farms now divided up into different sizes, so there is now more need
  to re-invest your crops to upgrade farm sizes before you can reap full
  outputs, starting a farm is harder
- Small tweaks to farming balance, Greenfruit now more productive,
  hydroponic farms balanced.
- Added a downgrade button to buildings, so now you can bail-out if you
  change your mind because you don't have enough materials
- Added smooth filtering to the RTW shadows

FIXES

- Characters don't eat your greenfruit unless they are starving (\<60)
- Fixed a few subtle import related bugs, including unrecognised
  research benches
- Fixed rare case of characters sometimes getting frozen and
  unresponsive in a combat pose
- Tweak for animal portraits 
- Character editor opens when buying animals (to change names)
- Fixed crash dismantling buildings indoors
- Fixed indoors state flag on items dropped by dismantling stuff

### 0.95.21

- Added a limit to certain attack types hitting multiple targets.
   Spiders and raptors can now only hit a single target at a time. Dogs
  and goats can hit 1 or 2 depending on the attack.  This is moddable
  for everything.
- Increased light level for calculating stat penalty when working in
  darkness
- Farming research costs changed (2 crops & 2 books)
- Characters now share backpack food even when at their home base
- Farm plant condition no longer degenerates after the farm has fully
  grown
- Fixed some little problems with movement orders on walls and gates

### 0.95.20

- Fixed a rare bug where player furniture could vanish from a savegame.
   If this happened to you, press Ctrl+shift+F11 and you should get them
  back.
- Fixed a door/gate opening AI bug introduced in the last update
- Fixed crash when deleting/upgrading buildings
- Fixed inability to interact with ore resources
- Some small fixes for mouse selection of objects
- Fixed sleeping NPCs shouting "stop theif" but staying in bed and going
  back to sleep

### 0.95.19

- Building exteriors are now hidden individually, instead of per zone
- Corpse flies added
- Optimisation for the foliage system

<!-- -->

- Skeletons no longer get a healing bonus from being in a bed

FIXES

- Fixed a bug causing the healing rate to be crazy high when in bed
- You can no longer steal from allied factions
- A few long-range pathfinding fixes
- Fixed a few exploits for thievery and stealth XP
- Added PC-camera maximum distance for selection box
- Fixed exploit dismantling un-built buildings giving free materials
- Fixed trading inventory closing when changing character
- Added acid burn particle effect, fixed bodyDecayTimer
- Repeat crafting option saved
- Character movement speed option saved
- Improved rain particle delay when camera is moved
- Stopped turret and light nodes being deleted when buying a building
- Fixed flickering bug when eating corpses

### 0.95.18

- more stability fixes and small performance improvement
- Fixed global fog blending between biomes
- Reset global weather values (clouds, wetness, dust) when jumping long
  distances

### 0.95.17

- couple of stability fixes

### 0.95.16

FIXES

- Fixed a major crash

<!-- -->

- Actually added some money items to loot to some of the shops and
  buildings

### 0.95.15

- Added an info panel in the FACTIONS screen that shows any contracts
  with NPCs you have, like for mercenary bodyguards
- Added repeat option to the crafting queue
- Added sleeping bags.  You need to buy some of these, they can be used
  to create camp beds and are re-usable.
- Camp beds now have half the healing rate bonus of normal beds.
   Healing rate now displayed in the GUI
- Wandering squads should now go shopping and relax at the bar for a
  while when they arrive in a new town, they also prefer to wait until
  morning to head out again.
- Number of materials returned when dismantling something now clamped to
  at least 1, so camp beds are now re-usable
- Added a move speed option to match the speed of your slowest character
- Characters now suffer a skill penalty when working in the darkness,
  now you actually need lights in your base
- Stolen items can now stack if they are stolen from the same source
- Sometimes abandoned buildings and ruins can have locked doors
- Added tooltip in new game advanced options window and options windows,
  to explain some of the settings.
- Added a physical item for money

FIXES

- Fixed a bug where your buildings could get tagged with the wrong town,
  causing the AI to refuse to work/eat/use things
- Fixed some situations where towns clash, eg if a player builds a huge
  town, or builds too close to other towns/nests and building ownership
  can come into conflict
- Fixed map stacking
- Fixed repeated knock-out animation loops when attempting to stealth-KO
  someone
- Fixed building swaps for buildings in other faction's town.
- Fixed crash dismantling building with mounted buildings. Also added
  some behavior.
- Fixed dialogue log missing lines sometimes
- Fixed an exploit where you could learn blueprints without buying them

### 0.95.14

- Added a storage box for robotics parts
- Fixed a crash in the construction set when opening dialogue objects
- Doubled the "use" range of lights, in the hope it helps with lights
  sometimes being too far for engineers to reach
- Tweaked food-finder AI to use closest food container
- Removed the "no terrain cutting" from the options.  It was a debug
  option from a long time ago, and no longer needed.

### 0.95.13

- Added lots of new books and writings to the world
- Bit more audio work, unarmed combat sounds added
- Added sound emitters to buildings, foliage and map features, also
  building interior ambient sound variants
- Garru now has attacks

NOTE: footsteps are temporarily inaudible in this version, will be fixed
next update

FIXES

- Fixed certain nests not spawning residents
- Fixed criminals getting released from cages early
- Probable fix for NPCs vanishing some time after being captured
- Fixed a bug that stopped some of the biome entry conversations from
  triggering
- Fixed carried dead characters being left behind when their old squad
  unloads
- Fixed path following case causing character to stick on walls
- Thief fences won't freak out if you try to sell them drugs
- Rounded health display text a bit so it wont stop at 99
- Fixed build menu icon crash

### 0.95.12

- Fixed the stealth mode marker arrows not disappearing

### 0.95.11

- Martial arts damage amount reduced, so that it doesn't skyrocket so
  early (It was getting powerful too quickly).  Also sliiightly higher
  damage at low levels.
- You can no longer bail out & recruit prisoners that hate you, or ones
  that are super strong.
- Scorchlander strength changed to 0.9x, accounting for their slightly
  smaller build
- Added more information to the farm placement tooltip to reduce
  confusion

### 0.95.10

- Fixed the stupid crash on saving/loading
- Fixed up the fogmen AI, some weren't bringing victims back to the
  nests, and they weren't always doing the worship thing
- Increased the amount of fog men, there's also a rare fog man swarm
- Animals can now bash down your gates, no more raptors hanging around
  outside
- Fixed the missing "tied to a pole" animation
- Fixed an important missing dialog option for the construction trader
- Fixed the rain not affecting farm water amount
- Reduced the "too close to town" build limit
- Fixed a bug with the AI sometimes not acknowledging mines as a
  resource source

### 0.95.9

- Fix for doors being un-clickable if you jump back and forth between
  zones
- A fix for NPCs being unable to hurt you when you are disguised as an
  ally
- Fixed duplicated clothing appearing on hive characters
- Emissive disabled when there's no power to the light
- Added the missing bar to Last Stand
- Stopped battery charge changing when paused
- Fixed a bug when loading a carried character and they drop in a random
  world position
- Stopped random doors appearing when unloading
- Farm fertility display popup fixed for fertility effect multiplier
- A few crash fixes

CONSTRUCTION SET

- Automatically fills out duplicated translation lines (eg if there are
  30 different lines that say "ok" then you only need to translate it
  once instead of 30 times)
- Added translation stats to the construction set
- added back the dialog export function for translations to use poedit
- Fixed custom column sorting for filenames

### 0.95.8

- Characters can no longer attack with their broken arms, they have to
  resort to kicks or whatever they can do
- Likewise if your sword arm is broken you can't block, so you'll have
  to resort to dodging
- Defensive combat mode now applies the +20 bonus to dodging if you are
  unarmed
- Tweaked weapon animation selection, mainly to fix the mismatching
  polearms stance, but also to add variety for specific weapons to use
  unique stances
- Reduced xp rate for toughness
- Small bugfix for difficulty of clicking on characters while paused
- a certain fix for AI/pathfinding with walls
- Fixed a problem with npcs sometimes teleporting back on screen after
  walking off
- Fixed the clouds
- Fixed a certain import crash

### 0.95.7

- The construction set now has a "translation mode" for using to
  translate the dialogue
- Dismantling buildings now gives back some of the materials
- Characters now feel the weather. 
- Duststorms strongly affect visibility and hearing range, and prevent
  tracking by smell
- Rain affects visibility and hearing range a small amount
- Certain clothing can protect you from the elements.  Goggles are good
  in dust storms.

Some fine-tuning for stealthy raids:

- NPC hear range is halved when you are indoors and they are not (or
  vise-versa).  Range is halved again if the door is closed
- alarm range is halved, and gets halved again if you are indoors, and
  then halved again if the buildings door is closed
- stealth knockouts take into account your visibility more, and you
  can't knockout someone if they are in combat unless they are totally
  unaware of you
- Tweaked the follow AI for escaping slaves/prisoners so if you make a
  run for it they will keep up rather than stay behind trying to fight
  everyone
- guards standing outside of a building will no longer keep the door
  open
- Fixed a bug with some slaves not reacting when you free them
- shopkeepers won't talk to you if you are an enemy
- Armour can now have skill bonuses for unarmed, dodge, and fist damage.
- Backpacks now negatively impact dodging
- Added more slaves to the slave towns
- Low-level slaves are a bit more likely to join you, others like
  captured bandits now a little less likely.
- Encumbrance and other penalties have a slightly lower effect on move
  speed

FIXES

- Fixed the trade window when you talk to a sleeping trader
- Fixed non-player faction relations all being 0 on import

### 0.95.6

- Added narcotics production to the tech tree
- Fixed the incorrect damage resistence number in the damage floating
  text when in simple mode
- Fixed stealth arrow markers not turning off
- Stopped player from re-claiming bounties by releasing prisoners
- Fixed bonus attack/defence stats display in the main GUI 
- Fixed a few crashes

### 0.95.5

- Added some feedback arrows to stealth mode
- Added options setting for displaying the floating damage numbers
- Increased amount of food sold in bars

FIXES

- Fixed a particular AI hauling bug

### 0.95.4

- Added dodging to the combat system.  You dodge when unarmed, and it
  can also be used to break out of stun-lock states
- Characters now have rear-direction block animations
- Tweaked the camera limit so you can look upwards a little more
- A messagebox now tells you what item caused you to get arrested for
  smuggling
- Made block animation blending look a little nicer
- Added sound effect for barefoot characters
- Added the plastic surgeon to empire towns
- Added a few more combat stance animations for different weapons

FIXES

- Fixed bounties getting deducted instead of awarded
- Fixed a bug with populating towns (mongrel was a victim)
- Fixed AI cores not getting spawned (needs import)
- Fixed NPCs coming into your base to work at your farms
- Fix for charater direction jittering when moving very slowly
- Fixed some visual bugs in the wetness system
- Fixed crash upgrading turrets in while use
- More tweaks for crowded combat movement
- Fixed the bar squads duplicating when loading a game or returning to
  an area

### 0.95.3

- Added a block for "thrust" direction, so you can now block unarmed and
  animal attacks
- Tweaked the formula for character muscle visibility.  Its no longer
  affected by strength (which now only affects bulk) or toughness.  The
  idea is to make characters end up looking a bit different to each
  other based on their skills (as opposed to everyone just ending up big
  and muscular)

<!-- -->

- the new formula is: max(dexterity, martialArts) \* 3.f + (athletics +
  swimming) - (cooking + science);

FIXES

- Fixed a bug that was messing up the combat movement and making
  everybody bunch up too close
- Fixed block animations not playing.  How did nobody notice that?
- Fixed some flickery animations and some animation bugs

### 0.95.1

- Fixed the fog islands zone
- Fixed some problems with importing
- Fixed random black inventory icons
- Fixed characters in character editor showing on top of each other at
  start.
- Fixed a few crashes
- Fixed the duplicated NPCs

### 0.95.0

- Unlocked more of the map with a new major faction.

FIXES

- Characters don't randomly get wet when created
- Small fixes for stuff like light emissive materials, a road-following
  bug, weird grass shinyness during rain

## 0.94

### 0.94.7

- hotfix for the crash when arriving in certain areas

### 0.94.6

- Possible fix for the performance slowdown some people have reported
  since v94.3
- slaves are now valued by skills
- Fixed turrets to save how many harpoons they have loaded
- Fixed interior not shown when inside a building and paused

### 0.94.5

- Some small AI tweaks, including a max range to AI weapon looting
- Fix for invisible harpoons

### 0.94.4

- A crashfix related to firing turrets

### 0.94.3

- Temporary fix for a random crash in the terrain engine
- Broken turrets fix (couldn't reload)
- Some memory optimisations
- Other small things

### 0.94.2

- Hotfix for the crashing, sorry i didn't notice sooner

### 0.94.1

- Fixed vanishing furniture on import game
- Fixed the main GUI displaying the wrong values for attack and defence
  skills
- Removed a few things from the Stenn Desert to speed up performance
- Fixed bar characters not spawning
- Fixed some destroyed buildings not appearing in towns
- Fixed randomly black buildings
- Fixed a few crashes and visual bugs

### 0.94.0

Note: The new map area isn't 100% finished, wait a few more updates if
you want to explore it at it's best. As a result I've made a last minute
descision to not release the very bottom part of the map until next
update.

FEATURES

- Active map area has (almost) doubled! New content and factions!
- You should notice a general performance improvement. The towns are
  still the slowest spots to be in, but they should have improved,
  especially the Holy Nation cities.
- Smuggling is now a career option. Buy narcotics or illegal goods and
  sell them wherever they are illegal to make huge profits. (You'll have
  to find where to buy/sell them yourself)
- It now gets wet when it rains. But, get this, it stays dry indoors.

SPECIAL SUPRISE FEATURE

- Unarmed combat added. It's designed to be a lot more challenging than
  learning a weapon. Probably will need further balancing, hasn't been
  fully tested in long-term gameplay.

NOTABLE FIXES

- Overhaul of the the animation blending system, combat animations
  should blend more smoothly now

<!-- -->

- Fixed up the combat movement/flocking system
- Also fixed most of the jittering in the movement system (not perfect
  yet)
- Fixed the holy nation bounty collection
- Fixed a common situation where NPCs wouldn't help defend their
  teammates if they weren't looking
- Slightly reduced the cut damage of the Falling Sun
- Combat XP rate is now also multiplied if you change the global combat
  damage option

## 0.93

### 0.93.28

- Fixed weapon smith critical successes not working
- Fixed inaccurate gui info in the weapon smith
- Armour smithing capped at "specialist" grade (unless you get a
  critical success)
- Added missing armoured rags to the crafting bench
- Fixed "get out of my house" dialog events when you were in a cage
- Fixed "intruder" events when you just get released from prison, also
  added a notification

### 0.93.27

- The AI now knows when it is in a chase, and should give up properly
  when they lose sight of you
- Removed the empty weapon smithing techs, they were left in by mistake,
  it's supposed to cap at mkIII
- Fixed the incorrect rum recipie
- Fixed closed doors being passable by animals
- Police shouldn't lock you up in private buildings anymore, so you
  don't get arrested again for tresspassing when you are released
- Food ingredients are now shown in the item tooltip and crafting window
- Some small fixes for characters getting stuck in certain situations

### 0.93.26

- Fixed the gate guard dialogs triggering repeatedly
- Fixed the buggy Flotsam guard approach dialogs
- Stopped civil wars breaking out in Bad Teeth all the time
- Weapon prices doubled to match up with the armour prices
- Fixed missing edgewalkers description
- Added more treasure 'n stuff
- Using equipment/ dummies in npc owned buildings is now illegal. You
  need to join the thieves guild if you want to use training equipment.

### 0.93.25

- Some small tweaks to Scorchlanders
- Added low-tiers to higher level weapon benches, just so its less
  confusing when you don't have any high level options available to
  craft there
- Fixed a bug with food getting super high nutrition levels, and then
  characters wouldn't eat it because it was too good and they would
  rather starve to death.
- Fixed flotsam safehouse
- tiny additional map content update.  Added some simple tips to the
  mechanical shop keepers dialog.

### 0.93.24

- Performance boost! I measured an average 5-10 fps increase.  This is
  not the main Ogre 2.0 performance update, that comes later.
- Tons of new weapons!  The number has doubled.  More interesting blunt
  and hacking weapons, polearms added, blunt skill unlocked, old ones
  overhauled visually.  Rare and unusual weapons to find.
- Weapon types have more characteristics and stats have been rebalanced.
   Weapons can have advantages or penalies when used indoors, and bonus
  damage against certain opponents or animals.
- Characters will automatically switch to their side-arm weapon when
  indoors, if it has less of an indoors penalty than their main weapon.

SMITHING OVERHAUL

- Crafted weapon quality is limited by character skill
- Crafted armour quality is entirely dictated by character skill (no
  need for further research)
- Crafting has a critical success chance, if character is skillful there
  is a chance the final item will be one grade higher.
- material costs and craft time vary by weapon type
- Crafted gear is now "imprinted" with the name of the smith
- Scattered appropriate weapon blueprints around the world

SMALL STUFF

- Labouring skill XP rate increased 50%
- Inventory interface subtly tuned to be a little nicer to use

### 0.93.23

ECONOMIC BALANCING

Over the last few years the economy of Kenshi has seen some inflation so
I've re-balanced it a little

- Recruits cost a lot more to hire, it's not so easy to rapidly get a
  bigger squad early on.
- Cost of books is doubled
- Bounty amounts for crimes are roughly doubled
- You can no longer sell armour that is part of another factions uniform
- Cooking food speed is x3, but ingredient cost is x8.  Now the focus is
  less on waiting around for cooking, and more on running farms and
  protecting your crops until harvest time.
- Properly added the research and crafting for the 3 main alcoholic
  drinks.  These are the new cash crop as food was made less profitable
  in the last update.
- Chainmail is 50% heavier

AI ANNOYANCE FIXES

- Tracked down the bug where your character would keep stopping when you
  are trying to run away from attackers
- Stopped chars going crazy constantly cursing and chasin' off varmints
  and ignoring your orders
- Stopped chars going off to get food in the middle of a fight
- turrets no longer aim too high for small or young animals
- some rare cases led to characters running away instead of fighting

FIXES

- Fixed a crash on save when you had a bounty with a minor faction

### 0.93.22

FOOD OVERHAUL:

- This is the result of some extensive testing, to further balance the
  hunger system in the way originally intended
- hunger time is doubled again.  It takes almost twice as long to get
  hungry.
- food nutritional quality is halved, but also food cost is halved too.
   Remember the yellow and red states are supposed to be starvation,
  your ribs are showing, you shouldn't be able to fully recover from
  malnutrition with just 1 meal.
- So, technically speaking, those 2 above result in the same amount of
  eating and costs, its just stretched over a slower timeframe now.
- Food is no longer a trade good, so you only get 50% of its value when
  you sell it.  Bread won't make you rich anymore.  This will double-up
  as a plot point with the Trader's Guild later on.  The cash crop will
  be drugs and alcohol.

FEATURES:

- Added a simple thieves/assassins guild
- You can now stealth-knockout sleeping NPCs
- Bounties are now assigned by factions. Committing a crime in the Holy
  Nation won't make you a criminal in the Empire or Shek Kingdom.
- Tuned the "spawn" distributions.  Should reduce the situations where
  you defeated a bandit or animal squad and then more and more kept
  coming to fill the population vacuum.
- Also implemented a mild co-existence system, so small time villages
  don't get instantly wiped out by their dangerous evironment eg the
  BeakThing-Hiver wars
- When your character gets sucked dry by a vampiric creature and dies,
  it leaves behind all his gear and clothes, just sitting there empty
  where once was your beloved character.
- You can no longer sell a fence back their own items that you stole
  from them
- Athletics XP rate reduced by 25%

### 0.93.21

MORE THIEVERY REBALANCE:

- Stealth sound overhaul.  When sneaking, targets will sometimes hear
  you.  The chance depends on distance and skill.  A zero-skill
  character will be lucky if he can sneak around a shop without being
  detected.  This gives more XP to compensate.
- Stealing chances rebalanced
- Town guards will investigate buildings that have their doors left open
  at night.  They can recognise intruders.
- You can no longer steal from your hired bodyguards if they get knocked
  out, they will now see it as a betrayal.  IF they see it happen, that
  is.

FIXES:

- Dogs shouldn't go to sleep right next to your body after knocking you
  out anymore
- Fixed hired bodyguards not healing your guys
- Fixed an AI bug with crafting bench hauling

### 0.93.20

- The last update nerfed the stolen goods sell values too strongly
  (15%), they've been increased to 50%.  I wanted to fix this before the
  weekend, because it ruined thievery.

### 0.93.19

- Fixed characters not getting up off the ground

### 0.93.18

THIEVERY REBALANCE:

- Kidnapping is now a crime, you can't just pick up sleeping shopkeepers
  and run off with them.  Well, you can, but now there are consequences.
- Fixed some AI bugs where NPCs don't go to bed.  Stopped bar guards
  taking paying customers out of bed and dumping them outside.
- blueprints and maps no nonger count as trade goods and so their
  re-sale value has the loot penalty
- all stolen items also count as "loot", so you can no longer sell
  stolen goods for full price
- fences now buy stuff at 50% instead of 25%, to make up for the loot
  penalty a bit
- you shouldn't get attacked at shop closing time anymore

FIXES:

- Fixed infinite lockpicking sound again
- put a minimum cap on bar patrons, so there's less chance of getting
  empty bars
- shouldn't be able to put animals in cages any more (because they don't
  fit)
- Some smaller AI and crash fixes

### 0.93.17

- Fixed another random crash that was introduced in the last update that
  addressed a random crash introduced in the update previous to that one
- Stealth knock-outs now have a skill-based success chance.  Tougher
  NPCs will be harder to knock out.  Percentage chance is displayed.
- Fixed the robotics skill, healing was using medic skill instead
- Fixed hydroponic farms crop yield
- Armour king now has a slightly lighter weapon, so he's way more
  deadly.
- A few more maps added to the travel shops
- Fixed a display error in the weapon stats

### 0.93.16

- Fix for a frequent crash introduced in the last update
- Looting law changes.  You don't get tagged as a looter until you
  actually take an item from someone, and it doesn't count as a crime if
  the item was stolen from you to begin with, or if the victim is a
  bandit, criminal or slave.  
- NPCs can also now get tagged as looters, same laws apply.
- Fixed possible issue with mod's data folders

### 0.93.15

- There was a mistake with the foldername instructions in
  /mods/readme.txt, it's now been corrected.
- Audio volumes have been re-balanced, footstep sounds don't dominate
  everything anymore.
- Fixed another talking animals bug
- Theoretical fix for hitting KO characters in combat
- Disabled dust bandit raid campaigns temporarily, until i have time to
  test and fix them up properly
- Fixed the AI bug where the shopkeeper would lock the door before
  telling you to leave, instead of after, and then consider you an
  intruder
- Fixed crash when picking up certain animals, and when sometimes using
  the furnace

### 0.93.14

INTERESTING FEATURES

- Added 2 Shek towns and a new zone in the SW of the active map area
- Stolen items can now stack if you put them in machines or storage
  boxes
- Heat haze effect
- a 2nd fix for talking animals because the bulls kept swearing when
  they joined you
- Solved the bug preventing walking on roofs
- Fixed more animal ragdolls

UNINTERESTING FEATURES

- Default Wanderer now starts with a loincloth so you're more like the
  other good-for-nothings.  Trousers make you feel like you're better
  than everyone else.
- Fixed interior reloading when following a character upstairs
- Limit max attack slots to prevent crash
- Unclamped GUI scaling for higher resolutions.
- Stopped ground effect particles appearing indoors
- Few AI bugs and crashes
- Fixed patrolling characters stopping
- Fixed ragdoll characters always facing the same way on load

### 0.93.13

- If your prison sentence expires and nobody comes to release you, you
  can escape without being branded a criminal for escaping
- Fixed enemy recognition for the GUI (eg when to show red mouse
  cursor + context menu options)
- Fixed some of the animal ragdolls, added the missing gorillo
- Fixed attack range for some animals
- Increased physical strength bulk multiplier by 50%
- Moll now has dialogue
- A few more crash fixes

### 0.93.12

- Fixed Splint kits.  They now work properly, and will save your life
  some day.  Its now a separate job to medic.
- Added a gameplay difficulty option for hunger time, higher settings
  means it takes longer to get hungry
- You can now buy and repair ruined buildings that you find
- A few crash fixes
- Fixed being unable to pickup map items

### 0.93.11

- Fixed building construction progress and research sometimes not
  progressing
- included missing translation .pot files
- bed rental can have different costs
- Fixed beds getting stuck as occupied if you get out too fast
- adjusted character appearance calculation.  Bulk (eg arm size) comes
  from strength or smithing skills.  Muscle definition comes from a
  combination of strength, toughness, athletics, swimming, and
  dexterity, and is reduced by the cooking + science skills
- Fixed trader's inventory stack duplication bug
- Added loaded translations from mods

### 0.93.10

- Fixed another of the new AI hauling bugs and a crash
- Fixed the high-level rare artifacts not being created when you import
  a game
- Fixed some cases of internal town wars kicking off
- Fixed invisible characters when loading
- Translation fixes
- Translation enabled in release
- Other small AI fixes

### 0.93.9

- crashfix

### 0.93.8

- When you pass the starvation threshold you now pass out randomly and
  periodically, instead of forever.  Gives you one last chance to find
  some food and survive.
- Reduced hunger recovery rate by half.  Means you recover from
  starvation slower, but also means that a full belly lasts longer

FIXES

- Fixed the newly introduced hauling AI bugs
- A few small audio bugs
- Fixed construction set translation exporter

### 0.93.7

- hotfix for debug lines showing on birds
- Fixed fertility value bug
- Non-swimming races don't ragdoll float in water

### 0.93.6

- Many many content additions, tweaks and small adjustments to things.
  Current map area content can now be considered mostly complete.
- Characters get wet
- Added a dialogue log window
- Ragdolls now float in water
- You can now pickup and carry animals
- Buildings now cast full shadow & reflections even if you are indoors
- Added the functionality to allow game translations
- Soft particles (no more harsh ground-intersection lines)
- resource storages are no longer infinite, they store between 25-100
  items.  This is an experiment, let me know if it causes problems
- When hauling, characters now only grab as many resource items as there
  is available storage space for

FIXES

- Fixed vanishing slaves (they were all escaping when their masters got
  un-loaded)
- Stopped the talking animals
- Fix for some navmesh problems when building walls
- Fixed dropped backpacks lose their items on save.

### 0.93.4

- Modified Blister Hill to make room for the holy lord phoenix
- Mostly small bug fixes with the AI

### 0.93.3

- A bunch of map content additions and fixes
- If you are knocked out in an animal nest, its now possible to sneak
  away when you recover if the animals are all sleeping.
- Pickpocketing from sleeping targets was way too easy.  Fixed now.
- NPCs and animals won't immediately go back to sleep after being woken
  up.
- Can no longer stealth knock-out animals

### 0.93.2

- reduced slave/shackle knockout time to almost nothing
- Farm harvesting times rebalanced and more reasonable
- AI cores were missing
- fixed characters randomly getting knocked out when they shouldn't be
  (probably)
- Cannibals more dangerous, added tribe chiefs
- greenfruit no longer so stackable
- fixed the "repeating talk to me" bug
- you no longer get thievery XP from anything with a 100% success chance
  (eg looting)

### 0.93.1

- Still finishing up the new content in the north of the map

<!-- -->

- Fixed Rebirth town
- Fixed hydroponic farms
- Filled out town populations in certain new places

### 0.93.0

- New world map sector unlocked, active area is now double the size.
   Lots of content to discover.  A little rushed, will contine to add
  final bits of content later.
- Added hydroponic indoor farming techs
- player characters should now attack anything eating their crops
- Stolen goods can be sold easier, shopkeepers can only detect if it was
  stolen from an ally faction. (before it was allies and neutrals)
- Rain now waters the farms and crops
- Updated some of the high-level research costs

## 0.92

### 0.92.2

- Fixed the huge bounty bug when unlocking shackles.  If you have a
  character with an insanely huge bounty then sorry I ruined his future.
- Fixed huge knockout times when wearing shackles
- sped up some of the super slow farm harvest times
- stopped the unusually long-range cannibal raids
- Fixed all the weapons having the wrong price
- Holy nation characters freak out more when they see Skeletons

### 0.92.1

- regenerated some of the navmesh-\> shorter load times and smaller save
  files
- Food store no longer drains power
- if you get hit while running away or wearing shackles there is a
  chance of you getting knocked down
- fixed some slave state and AI bugs

### 0.92.0

FEATURES

- Steam Workshop support added, new modding structure.  All mod files
  need to be in kenshi/mods/modname/ instead of kenshi/data/.  Other
  data files like textures should go in these folders too.
- Loads of new audio and new animal sounds
- Holy Nation Rebirth slave camp finished
- Added holy nation slave delivery caravan to take prisoners to rebirth
- Weather and birds systems improved
- Game speed \>\>\> button now speeds the game up to 5x instead of 3x

FIXES

- Fog islands were too foggy
- Big memory optimisation
- Lots of small technical fixes
- Fixed the/a random stopping AI bug when following roads

## 0.91

### **0.91.19**

- Have done a bit of tweaking to the sensory system.  You are now harder
  to see and hear when you are in a different building or on a different
  floor, this means for example that you could fight your way up a tower
  floor by floor without instantly triggering every enemy in the area.
- Spiders now eat you by sucking out your sweet sweet juices, instead of
  eating you from the legs up like everything else does.  There aren't
  any spiders in the current map, I just wanted to mention it.
- Fixed moving characters sometimes going under the terrain when loading
- Fixed items sometimes being dropped if you move them too fast
- Fixed an issue with preview building altitude
- Added cheek fatness slider (for now only human female characters)
- Much crash fixes

### **0.91.18**

- Quickfix for a possible freeze.  Not sure if it was a freeze, but
  quickfix just in case.

### **0.91.17**

- Hunger time is now 50% longer
- Fixed items missing from containerss in non-shop NPC buildings
- some fixes for building placement
- There was a bug a few versions back that damaged a setting on your
  interior buildings.  Symptoms would be the AI having trouble reaching
  the object, getting confused, standing on the wrong floor... You can
  fix it now by rebuilding the navmesh with ctrl+shift+F11 when in your
  base.  

### **0.91.16**

- NOTE: For modders, there are now skinned character model templates
  available on the lo-fi forums
- Added an optional "no hunger" mod for those who don't like starving to
  death cold and alone.
- Dogs have a little more meat on them (3 instead of 1)
- Fixed a bug where a character could become un-hittable in combat if
  not tagged as enemy
- Bunch of fixes for the law enforcement AI dealing with prisoners and
  loot confiscation
- Fixed blank items icons
- Fixed issues with upgrading and dismantling walls

### **0.91.15**

- Mainly crash fixes
- Fixed animal hair disappearing in character editor
- Fixed mouse tracing building through terrain
- Fixed harpoons material
- Fixed character visibility on upper floors

### **0.91.14**

- AI fixes for taking wrong materials from machines
- AI fix for getting confused with food deliveries when hungry
- Crash fixes

### **0.91.13**

- Emergency quickfix for a random crash

### **0.91.12**

- Fixed a display bug in the stat XP progress bars in the stats window.
  It should now show progress correctly
- Fixed the Dust King bounty exploit
- Some memory optimisations
- a few crash fixes

### **0.91.11**

- Fixed un-healable animals
- added new game start, and wandering trader starts with a pack animal
- a few more AI fixes

### **0.91.10**

- turret gunners change to better targets more often
- lots of fixes to the general crafting/hauling AI
- Added turrets with spotlights
- Fixed assassination dummy training wrong skill
- Fixed random crash when buying buildings

### **0.91.9**

- Fixed un-blockable animals
- Turret guards can now go and get food too
- Fixed AI pathfinder confusion with floors of objects
- Fixed AI taking all the food he can carry insteod of just one item

### **0.91.8**

- characters in home base now automatically get food from storage when
  they need to eat
- characters outside of home base share food with squadmates if it's in
  their backpack
- Fixed combat missing attacks when on steep slopes
- Fixed unable to build wall ramps
- Fixed "auto-arrange" button sometimes losing items
- Fixed the cheap research costs bug

### **0.91.7**

- building inventory is now imported when you import game
- More stumble fixes
- Fixed crash when starting with texture quality setting too low
- lots of small uninteresting fixes

### **0.91.6**

- AI doesn't get confused when the output of a crafting bench changes,
  will now clear out all the old items and continue working
- Improvements to item collection/delivery AI
- Fixed the combat stumble-toughness threshold, stronger characters
  should get stunlocked less
- Fixed up the building & wall placement, its a lot nicer now
- Added a few small buildings, like ceiling fans and electric light
  posts
- Shift-click on an animal corpse will create an auto-loot job for
  gathering meat & leather
- Fixed right click movement in wall ramps
- Fixed GUI threading issues
- Fixed dropped item losing STOLEN tag
- Can now move building previews again after placing them
- Fixed stolen items behavior
- lots of smaller bugfixes

### **0.91.4**

- Finished fixing up turrets.  They're a bit more powerful at higher
  skill levels
- Building doors have 3x more hitpoints
- NPCs no longer lose their short-term memory when you load a game
- Characters now prefer to eat higher level food items, so they won't
  eat up all the raw ingredients if they have a proper meal.  They also
  won't eat ingredients until they reach 200 hunger instead of 250.

### **0.91.3**

- Characters now defend their farms from river raptors and other pests
- Fixed a bug with stealing chance calculation when stealing from
  containers
- You can now eat while using turrets
- Fixed the turrets missing neutral targets

### **0.91.2**

- Game now runs on 2-core CPUs
- Hivers now react to crime
- NPCs react properly to failed knockouts
- Added hemp-based fabric loom
- You can now eat while using turrets
- Fixed character editor crash with ragdoll characters
- Other small tweaks and fixes

### **0.91.1**

- I've put v0.90.10 as a separate branch on steam, as that was quite a
  stable version and there are some big bugs going on in the latest
  versions
- crash fixes

### **0.91.0**

- Improved back-threaded resource loading, for slightly smoother load
  times
- Fixed a bug that was causing progressive framerate decay in the last 2
  updates
- Fixed batteries thinking they were wind generators

## 0.90 New World

### **0.90.15**

- fixed the missing audio
- player town location is now adjusted when you destroy buildings
- town walls are now passable until they are 80% complete, also the
  material now reflects this better
- Fixed engineers not doing anything if they didn't have the materials
  already

### **0.90.14**

- Stopped people freaking out so quickly when you enter their houses
- Fixed sometimes when you buy a house a resident remains and calls the
  guards
- Fixed a navigation bug with moving inside towns with walls
- Fixed assassination dummy upgrading to wrong thing, and the missing
  iron refinery III

### **0.90.13**

- Restored the muscle/skinny effect on characters
- Fixed the inability to build campfires, and they are now free to build
- Fixed the skeletons texture
- Fixed the bug with wrong damage amounts showing when hit by animals
- Fixed a farm AI bug
- Fixed the hovering turrets bug

### **0.90.12B**

- That didn't fix it, so here's an experiment to see if it's now fixed

### **0.90.12**

- It seems the last update added a random crash,  2 actually, and I
  fixed one of them but the other is more complicated to track down,
  lets see if this update has fixed it

### **0.90.11**

- Fixed underground interiors selection
- Removed already learned research from the research list.
- Fixed bug with adding building materials to certain buildings
- Performance optimizations
- crash fixes
- fixed characters flickering on some systems

### **0.90.10**

- Fixed some issues with mines
- Fixed fuel storage only storing 1 item
- Fixed crash when dismantling buildings
- Added crop yield values when placing farms (this should avoid placing
  farms that won't give crops)
- Fixed animals inventory weight.
- Fixed in crafting buildings: saving/loading of inputs and items,
  stacking outputs (when possible), crafting times
- Fixed the crazy long food crafting times
- weapons and backpacks are left behind if a character is eaten

### **0.90.9**

- Fixed the furnace's blown fuses and now is working again.
- Fixed empty named squads disappearing from the squad window.
- Fixed crash when loading or going near Stack town.
- Fixed mining buildings loaded with zero resources.
- Fixed some of the major navmesh issues in border zone
- bunch 'o crash fixes
- another improvement to load-time framerate slowdowns
- hivers no longer get injury penalties at full health
- fixed hunger penalty for some skeleton NPCs

### **0.90.8**

- added missing cooking stove
- night time is now less dark
- fixed camera refusing to descend

### **0.90.7**

- hunger now drains slower when you are KO
- fixed the repeat bounty exploit
- fixed beak things & bulls unable to attack
- eating stacked food no longer depletes the whole stack
- fixed imported squads having an empty build list
- bread is crafted much faster
- fixed crash with research bench lvl IV
- fixed player characters not updating properly offscreen
- bunch 'o crash fixes, particularly with the research window

### **0.90.6**

- Books are now a little more common, and can be found in the holy
  empire towns
- Fixed random buildings getting navmesh-blocked so nobody could get
  inside
- Added a mercenary squad to the Waystation bar to help the freedom
  seekers start

### **0.90.5**

- Fixed dialogue crash after stealing stuff.
- Fixed getting cooked food item from campfire.
- Fixed research consuming the required amount of items.
- Meat is worth more nutrition and cooks way faster
- Can't reproduce the Paladins in Wildlife faction bug, so I think it
  was because of the missing mod file before.  Will enforce save imports
  for this version and see if it still happens.
- Fixed animals unable to attack
- Fixed multiple characters showing all at once in the character editor

### **0.90.4**

- food now properly consumed from backpack
- Finished

fixing the long freezes and slowdowns properly. My previous solution
probably was causing bugs, which will now be fixed. Performance should
be smoother.

- Fixed the black stripes on the terrain some people were getting.
- random nest items no longer spawn under the floor in buildings

### **0.90.3**

- Added missing Dialog.mod file. Tons of content was missing there, and
  caused some crashes
- Fixed crash when purchasing buildings
- There are some big long slowdowns and freezes in the game at random
  times when zones are unloaded.  Optimized these in a gung-ho kinda way
  to get it out quick. Will go over it more carefully later.

<!-- -->

- robot repair kits now available at construction traders. Not in the
  holy empire though.
- Hive faction shop was missing tons of item types
- More fixes for starting in bad towns

### **0.90.2**

- Stopped new games starting in deadly towns.
- Fixed getting stuck when trying to add building materials
- Fixed some of the crashes at startup that some people were getting
- Pets no longer need to eat.  This is a temporary measure, later I will
  figure out a feeding method or something.

### **0.90.1**

- Imposed limitations and a fix for importing old-world savegames
- Enabled the missing playable races

### **0.90.0**

NEW WORLD (0.90.0) Due to the sheer size of the new map the first
release will be restricted to a certain area only.  This area will
gradually expand with more updates, but the main focus now is going to
be on stability and polish.This first build will be full of bugs and
instability, please send us crashdumps and bug reports so we can fix it
up.

**Content:**

- Entirely new world map.  More detailed and polished, new factions, new
  content, things to explore. Its' like Kenshi 2. Crazy. I should have
  called it Kenshi 2 and charged for it again, but I didn't.
- Entirely revamped research tech-tree, new technologies and balance. 
  Research is faster, but has a cost in items or artifacts.
- Totally new buildings.  Multiple floors, and you can mount turrets on
  the rooftops.
- New power system.  Generators require fuel, wind power fluctuates with
  the wind strength, batteries compensate for fluctuations. Fuel can be
  made

from crops.

- Revamped farming system and different crops.
- New animals, and new races with own strengths and weaknesses.
- There's water now.  Rivers to cross and oceans to drown in.
- Camping- You can build easy camp beds and fires for survival when
  traveling
- Things and places to find. Bandit bases, old labs, ruins.

**Gameplay:**

- Hunger is now a thing. You can die of starvation although it takes a
  long time. Your characters appearance reflects their state of physical
  strength or malnutrition.
- Buildings are now made with multiple materials.  Machinery requires
  iron and sometimes copper.
- Thievery is improved, buildings have things to steal, guards are more
  alert.
- Leather crafting now requires you to hunt for animal skins
- Nice new zoomable world map window. It's so nice.
- Your stats are now affected by injuries and malnutrition.
- Certain animals might now eat your crops, your dead bodies, and
  sometimes even your unconscious bodies.
- NPCs use the stuff in their homes, guards train, people sit etc
- Guards in buildings and shops now discreetly sort of follow you about,
  keeping an eye on you
- Fixed getting busted for stealing from accidental clicks. You can look
  inside unlocked containers, and lock picking has to be chosen through
  the right-click menu.
- Reduced labor/engineering speed penalty at level 1 from 0.25x to 0.5x.
  This will speed things up slightly at the lower levels when starting
  out
- Stealth skill is easier to train in non-hostile environments.  
- Increased trade profitability by 50%, this combined with thievery
  should provide decent alternatives to looting as a profession in the
  early game stage.
- Characters with a turret job will automatically use whichever turret
  has enemies in its line of fire.
- New long-distance move command, so you can click on distant terrain
  and your characters will run there
- Tons of bugfixes.

**Engine:**

- New fancy shadow system, looks nicer and more importantly runs faster.
- New terrain engine.  Runs faster, looks nicer and shows more detail
  for distant mountains
- Long-range pathfinding system.  You can click on any visible distant
  mountain and your characters will find their way there, following
  roads.
- A lot of fundamental engine optimizations have been done, this may
  temporarily cause new bugs, but hopefully speed things up
- Bit of an overhaul to the animation system, runs faster and combat

animation should be a little smoother and have more functionality

- Overhauled with a new PBR & HDR global lighting system, should make a
  great improvement to the visual quality
  - (Credit for this goes to Linda MacGill and Igor Frolov of Bug Zen!)

## **0.76**

### **0.76.6**

- an AI fix for operating automatic machines
- crash fixes

### **0.76.5**

- Added more content for slave buying/selling.  Buying slaves is now
  cheaper but it has random results.  You can also sell bandits or
  someone you're carrying.
- Fixed the thief fence.  He has more money, buys at a low price, and
  doesn't sell his own clothes.
- Fix for traders spawning under the floor
- various crash and performance fixes
- crash when stealing with right-click

### **0.76.4**

- Fixed some bugs with the AI invasions, and with vanishing AI squads,
  plus a related crash.
- Fixed a bug that caused huge loading times and performance hit to
  savegames where you had traveled a lot
- Fixed a possible trader crash
- Crashfix when occasionally picking up items from the ground
- There's a bug that only some people get where it crashes when saving. 
  I don't know why, so I tried some stuff that might help or might not. 
  I need more information, or a savegame if it happens only in a
  particular game.
- Some more stability fixes, and improvements to the formation movement

### **0.76.3**

- Fixed nests and camps not being spawned
- A few more random crash fixes that were reported
- You can now alt-tab out of fullscreen mode in DX11

### **0.76.2**

- Fixed the athletics skill not increasing
- Fixed the "location" of characters when they ragdoll and slide down a
  hill
- Fixed wandering trader AI jittering and freaking out after staying in
  a town more than 6 hours
- Fixed the BUY button on houses not functioning
- Fixed 2 random crashes
- Fixed the crashdump zip getting a truncated filename
- Fixed newly bought&freed slaves getting tagged as escapees when
  save/loaded
- Fixed again the walls, I had fixed the scales for them but there were
  still old, badly scaled collision files that i have now replaced
- Fixed the bugs with corpses, incorrect ragdolls, location etc

### **0.76.1**

Mainly a hotfix for the save bug, I will work on the other bugs next.

- Solved the savegame error where it didn't save your squad if most of
  them were knocked out
- Walls were scaled differently.  This was not supposed to be in the
  release version yet, they've been set back to normal again.  Sorry for
  breaking your base walls.  Super-sorry if you just rebuilt your base
  walls to match the new scales.
- Fixed issue with alt+tab and fullscreen.
- Fixed big fonts with resolutions larger than 1920.

### **0.76.0**

Apologies for the delay with this update, we are currently working a lot
on content for the new world map and hoping to release the first part of
it in the next major update.

- Huge optimization that uses more multi-threading for the game code and
  AI, improving performance significantly when there are a lot of
  characters around.
- AI War Campaigns, NPC factions can now launch proper missions.  This
  is similar to the faction assaults feature that was around in an older
  version, except the difference is it's now a fully dynamic system
- Random bandit camps
- Races now have different bonuses and penalties to certain stats
- Render optimization for the lights, it appears they were slowing
  things down a lot
- A new shadow system, with better performance and quality
- Bars now have a variety of random goons who all sit together:
  - mercenary groups
  - thieves, with fences to sell stuff to
  - bounty hunters
- colorization maps added to faction armours
- AI squads now move in formation
- The AI can capture slaves and make them fight as a conscripted army
- You can now buy and sell slaves
- You can now pay the bounty on a character to get him out of prison

FIXES

- Made our own game launcher (old one was a default part of Ogre
  engine), which hopefully fixes some of the config problems people had
  with DX11
- Fixed the shortage of nests
- Fixed being unable to use beds and cages
- Fixed the overpopulation of the slaver camp
- Fixed some more pathfinding/collision bugs
- Fixed a ragdoll display bug

## **0.75**

### **0.75.3**

- added lamp posts to the research
- shouldn't get bounties for attacking animals anymore
- fixed getting tagged as a criminal for attacking bounties
- Other small fixes and crashes

### **0.75.2**

- Fixed crash when trading to your backpack
- Police can't steal your bounties anymore when you walk into town
- Fixed the crafting list scrolling back to the top whenever you choose
  an item
- Fixed the invisible inventory icons i think
- tried removing a certain AI optimization to see if it solves the AI
  problem where NPCs idle too much or forget what they were doing
- fixed the "arm through the chest" animation bug
- possible fix for when an NPC squad gets unloaded while carrying a
  player character
- fixed not being able to place turrets on walls (you can add lights now
  too)
- fixed some armour in shops being un-graded, and having overpowered
  stats
- A rare-case gate fix
- A few crashes

### **0.75.1**

- Fixed loot window not appearing
- Fixed importing old savegames not working
- Fixed crash when building something with an emissive material
- Crash fix when looting people near nests

### **0.75.0**

- Town populations slowly regenerate when residents die.  Killing off a
  lot of NPCs that are affiliated with a nearby town will weaken that
  town slightly, it's possible to wipe out all the cannibal patrols
  roaming near a cannibal village for example.  Currently "homeless"
  factions like the bandits are not affected by this.
  - brought back the town info tooltip on the mapscreen to show
    population information.  I will rely on player feedback for
    balancing it.

<!-- -->

- Crime system in progress.
  - You can now steal from shops  
  - Crimes are recognised by the AI  
  - Police can put a bounty on your head and arrest you  
  - Civilians can raise the alarm and call police attention to a crime  
  - Pickpocketing: NPC is alerted if he notices you stealing from his
    inventory while he sleeps  
  - Selling stolen items has a chance of getting you in trouble,
    especially if you try to sell things back to the victim  
  - Sleeping NPCs are woken up by noise, but it's easier to rob them  
  - Police confiscate weapons and stolen goods.  Then they sell them.  

<!-- -->

- Updated traders inventory:  
- To trade with a shop you need to talk to the trader character.  
- Interacting with the containers, counters, chest, etc. will be
  considering stealing. (Work In Progress)  
- The traders inventory is infinite, so you can sell stuff more easily  
- The trader stores his shop inventory in the actual containers around
  the shop.  This means you can steal stuff from them.  
- Some item containers now have locks.  Traders keep the more valuable
  items in the more secure containers  
- Added a node system to building placement.  It ensures that any
  machines and storage you place is always accessible by characters and
  fixes a lot of bugs like when characters tried to access a storage box
  through a wall  
- Emissive lighting added  
- Added AI ability for super long-range pathfinding, even when zones in
  between start and destination are unloaded  

**FIXES**

- Fixed orders panel black text-on-black tooltips
- Fixed item labels not showing when loading a game with items on ground
- A few small movement system fixes
- Fixed undo when building walls
- Fixed game unpausing or closing the pause menu when autosaving.
- Fixed unpausing game possiblity while on the in-game main menu.
- Fixed/updated research window.

## **0.74**

### **0.74.32**

- Fix for the inverted "cant build near towns" range testing bug
- Another hopeful fix for the teleporting into the void bug
- Fixes for character portraits
- Some small fixes for navmesh and AI within town walls
- 1 more crashfix

### **0.74.31**

- More debug logging information added to track down the teleportation
  bug
- Stability fixes
- Slavers shouldn't capture police and soldiers anymore.
- Slave shops added to major towns.  Still a WIP.

### **0.74.30**

We are still trying to track down the problem with squads/characters
vanishing off the map or into the void, often when you load a game.
 We've added more debug information now, so if you load up your savegame
and find that it's missing anyone, either send us the save or just the
file called "save.log" that you should find in your save folder.  This
save.log file only appears if something bad was detected, so if you see
it, send it in!

- AI fix for engineers, they were picking the furthest instead of the
  closest target
- AI fix for wandering traders
- possible AI fix for move orders getting cancelled
- Fixed the police chief bounty hunting dialogue
- Some fixes for wall upgrading
- fix for spawning under floor in some buildings
- Fixed equip/drop item bug
- Fixed the crazy "man standing on my head" ragdoll bug when you save a
  game while carrying someone
- other small fixes

### **0.74.29**

- Added a mercenary guild that can be hired to guard your base.  Need to
  import a new game to see their shops appear in towns
- Fixed the "Day" always being 1 in some cases
- a fix for getting stuck in doors
- More stability improvements

### **0.74.28**

- 2nd AI fix for movement overshooting the destination
- bugfix that was causing increased loading times at startup
- small combat animation fix
- dogs are less bitey, have more time between attacks

### **0.74.27**

- AI fixes for the slave camp
- Another fix for "reset positions" not recovering all squads
- Fix for character movement overshooting the destination
- More small fixes for movement and AI
- Lights don't work until you finish building them

### **0.74.26**

- Walls now don't affect pathfinding until they are 20% built
- Another possible fix for characters vanishing into the void
- Some more auto-job AI fixes
- re-enabled civilian NPCs
- Moar stability
- Fixed characters running on the spot when the navmesh updates

### **0.74.25**

- Possible fix for characters vanishing into the void
- Fixes for the auto-jobs AI getting stuck.  If it still happens in any
  situations I will need someone to send me a savegame for it.
- Improvement to the "reset positions" import function that will recover
  missing squads
- Fix for when engineers stand idle as a result of an unreachable
  building
- A fix for the prospecting window
- A few more small things and stability fixes
- Fix for 32-bit mode not running

### **0.74.24**

- Fixed creature nests not spawning anything
- Fixed the suicidal follow AI behavior
- Fixed breaking shackles with brute strength
- Fix for the player outpost renaming
- Stability fixes

### **0.74.23**

- Fixed the bug where characters could still "see" their squadmates from
  miles away and would run across the map to help them
- Fixed re-captured slaves going back to escaped slave status
- fixed the "chase" mode order, so characters shouldn't run off so much,
  but it's not been tested much yet
- Bandits won't get so obsessed with picking up dropped items they cant
  get to
- a possible fix for characters getting teleported outside of the known
  world
- fixed the wandering trader AI doing nothing
- Fixed turrets doing 1 damage again. Naughty turrets.
- Fixed the dismantle all button on walls
- Fixed wall placement snapping to position the wrong way around
- Fixed character AI preferring melee to using turrets
- Lots of AI bugfixes relating to fighting with turrets, and attacking
  gates (WIP)

### **0.74.22**

- Fixes for wall placement
- Fixed 2 movement AI bugs making slavers and possibly town NPCs idle
  around some times
- Stability fixes
- Updated the prospecting GUI window

### **0.74.21**

Some savegame "corruptions" it turns out are caused by not importing
your savegame after update 0.74.14.  Import if you have problems, report
the bug if you still have problems.

- If you have a savegame with a missing squad or characters vanishing
  "into the void" then loading your game with "reset squad positions"
  will now recover everyone.  We are currently tracking down the root
  cause of this bug.
- Crashfix for certain situation deleting interiors
- Fixed a small typo in the perception system that made everybody not
  see other neutral NPCs
- Added audio to the perception system (work in progress)

### **0.74.20**

There seems to be a lot of bug reports lately of the game crashing when
loading certain savegames.  These are NOT caused by corrupted savegames,
but are crashes from loading certain stuff.  If you experience this,
send us your savegame, we will fix the bug and your savegame will work
again after the next update.

- Fix for randomly broken combat movement
- Fix for some of the loadgame crashes

### **0.74.19**

- Player characters can see better now, won't ignore things so much
- A fix for potential problems with navmesh backwards compatability in
  previous saves

### **0.74.18**

- Just stability fixes

### **0.74.17**

- possible fix for random situations where characters dont move
- Toned down the strength and number of the dog packs
- Fixed recruitment (and other dialog) "sorry i cant afford it" bug
- more fixing for player characters not loading if you load a game and
  they are far away
- there was a bug where excessive numbers of squads were being saved,
  causing bloated savegames
- Fixed a potential load crash

### **0.74.16**

- Totally new movement system:
  - eliminates the frame rate spikes
  - improves performance
  - stops NPCs always getting stuck and flickering back and forth
    (probably still get some bugs though, it's a new system)
  - stops the random crashes when changing map areas

<!-- -->

- Totally new AI sensory system:
  - all NPCs now use field of view and line of sight
  - you can avoid detection, fight a guard without raising the alarm etc
  - Its totally awesome and cleverly made so it doesn't hurt the frame
    rate with tons of characters all LOS checking eachother
  - Probably will cause a lot of new bugs because it's a fundamental
    system with far-reaching gameplay consequences
  - I didn't have time to add audio senses, only visual, so sneaking
    will be a bit too easy until next update.

<!-- -->

- Slave escapes:
  - You can free slaves and they'll react and escape and thank you and
    try to escape with you and sometimes join you once you get away.

**NOTES:**

- a change to the time system means you may end up with problems like
  getting stuck tagged as a slave for 99999 hours or a wandering trader
  that never leaves your town- import game to fix it.

### **0.74.15**

- Fixed some certain savegames crashing on load
- Fixed some certain savegames/imports getting stuck on the loading
  screen
- Fixed player buildings being un-built on import
- Fixed the missing Alt-key item labels
- Did a little internal rewrite that should stop the occasional various
  bugs arising from NPC or building handle IDs changing.  Might also
  cause unforseen bugs as it's a new untested system.

### **0.74.14**

- More stability fixes
- Fixed athletics penalty not showing in armour tooltip
- Paladin and mercenary guards should now protect you in towns
- Proper fix for character editor camera
- Fixed item labels on ground
- Fixed inventory item right click behavior
- Fixed weapon stacking losing its level
- Can no longer stack weapons

There are some known bugs with importing and loading games freezing up
or not loading.  This will be dealt with in the next update

### **0.74.13**

- Fixed crash when shooting animals with harpoon turret

### **0.74.12**

- Fixed the invisible in character editor bug

### **0.74.11**

- Fixed some of the flophouses not working
- Stopped (I think) towns errupting into civil war
- Fixed another crash. Keep sending those crashdumps.
- Fixed turrets only doing 1% of their damage
- Fixed NPCs tagging their allies as neutrals
- Escaped slave recognition is now based on an alertness-based timer,
  same as seeing through disguises
- Slavery status improved, you now have 4 states- free, slave, escaping
  slave, ex-slave.  Escaped slaves eventually lose their slavery status,
  and also don't get attacked on sight all the time.
- Fixed a crash when automatically hauling weapons or armour to a full
  container
- Fixed the random broken shopkeepers
- Fixed the stray outpost appearing on the map screen

### **0.74.10**

- Fixed the stray outpost showing on the map
- Fixed characters going back to open the gate when they go outside the
  base
- Fixed the bounty/slave panel position in the GUI
- Fixed an AI bug with crafting machines

### **0.74.9**

- Fixed a frequent crash loading certain buildings and savegames that
  was introduced in the last patch
- Fixed the instant building bug

### **0.74.8**

- Added separate farming and cooking skills
- Fixed lights.  You might have to switch all your lights back on
  manually.
- Fixed the remaining inventory item icons
- Fixed some random town buildings not being populated.
- Fixed crafting bench item crafting bug
- Mainbar now displays correct floor number
- Added panel in the build mode to change floors
- Bunch of other smaller bugs and crashes

### **0.74.7**

- Fixed newly built buildings not showing their interiors
- Can cancel crafting items properly now, and it shows the current item
  without having to operate it
- Fixed a crash when upgrading crafting benches
- couple more crashes
- Fixed outpost "open to public" status
- Item furnace takes stacked items into account
- Player characters don't instantly attack all NPCs who enter their base
- If you equip 2 katanas on your back, it shows on your character now
- Fixed AI bug for automatic machinery

### **0.74.6**

- Characters now haul properly for automatic mines and machines
- The slave camp was missing the slavers that actually make the slaves
  go to work everyday. Fixed now, but requires an import or new game.
- Optimised the static geometry, improves town load times and the
  framerate spikes when placing/removing buildings
- Fixed the bug where finishing building a wall section could cause a
  massive 2-minute freeze.
- Fixed some AI bugs with the permanent jobs, and the slavers
- Fixed crafting benches still working when they run out of resources
- Fixed doors not locking
- Added face morphs for the Shek in the character editor
- Engineer job now repairs things again, including doors and gates
- Adjusted the general contrast of the GUI for readability
- Fixed some more bugs with inventory stacking
- Fixed the Medicrate inventory being too small
- Fixed towns not populating when you start a new game from in-game
- Fixed walls missing their turret nodes
- Fixed the sleeping animal AI so they can wake up and attack you
- can no longer place furniture on walls
- Added mouse icon for lighting-type buildings
- Minor GUI fixes
- Fixed storage building inventory window grid size
- Fixed some inventory right click item issues
- Fixed inventory item stacking bug
- Dropped backpacks now save the items inside properly
- Improved equipping weapons for fighting
- Possible fix for the invisible backup weapon bug

### **0.74.4**

If you get crashing in the character editor in DX11 mode, switch to DX9
instead, it's more stable at the moment

- Fixed NPCs populating player buildings
- There were still spawns happening within walls, took extra measures to
  fix this
- Fixed the editor body limits for the Shek
- Fixed an AI bug that stopped shopkeepers opening up, jobs from
  working, and wandering traders doing their thing, and probably a lot
  of other problems too

### **0.74.3**

- Fixed the overly restrictive limits in the character editor
- Fixed the character editor applying the face morphs twice, resulting
  in deformed characters
- Towns are now populated dynamically on gamestart, rather than being
  pre-saved in the editor.  This means changes to the town/faction
  population list will take immediate effect on a new game.
- This also solves the absence of town guards bug.
- Fixed a bug with inventory when moving stacks with the mouse
- Fixed the corrupted Tin Can helmet mesh
- Fixed the buildmode tech level selector
- Fixed some problems with turret placement
- Fixed trader windows sometimes opening up empty

### **0.74.2**

Some of the DX11 issues we are still puzzling over.  Overall if you use
DX11 it will run faster, but if you run DX9 it will be less buggy.

**FIXES**

- Fixed backpack inventories not being loaded from a savegame
- Theoretically fixed NPC/animal squads spawning in towns and bases
- Fixed a couple more crashes, and found one more in the character
  editor too
- Fixed far away player squads not getting loaded
- Stopped the context menu going off the bottom of the screen
- Nice NPCs heal KO'ed neutrals they find

### **0.74.1**

Note that the GUI and character editor still have work to be done in the
future

**FIXES**

- Launching DX11 in fullscreen still crashes, but not if you run at your
  screens native resolution.  Still trying to figure out the cause
- Fixed a character editor crash
- Fixed getting stuck in editor when recruiting someone
- Fixed the white character portraits in DX11
- shops have more items in stock
- Fixed the inventory icons for items, not for armour yet
- Hostile patrols are 50% less likely to attack towns
- Cleaned up the launcher options
- Fixed some more AI system bugs, including animals not attacking
- Fixed characters getting stuck in idle mid-combat
- Fixed some random crashes

### **0.74.0  "So big"**

This is a super unstable version, it's not ready for release but because
there hasn't been a release for a long time I'm putting it out in the
"Experimental" branch so people who are interested can play around with
it. If I try to fix everything first then I'll just keep delaying it
more and more until the players lynch me.

**RECOMMENDATIONS:**

- Keep the "view distance" low, it has a drastic effect on performance.
  This is caused by the terrain engine, it's getting fixed in a future
  update
- Keeping the population size low will help performance too
- Run the game fullscreen, disable civilian NPCs, turn off shadows will
  all improve the frame rate
- Running the game in DirectX11 mode has a better frame rate

**SLAVERY!**

- There is a slave camp in the west.  Any newly captured slaves will be
  sent to the camp.  Escape attempts will be met with harpoons.
   Intruders will be captured.
- Slavers strip slaves and shave their heads.  Confiscated items are put
  into storage.  Slaves are kept in cages and made to work in the mines
  during the day.
- Slaves have shackles locked onto their feet.  They can't be removed
  unless lock-picked or broken with tools.
- Stolen items are now tagged and the original owner can recognise them
- More limits to trading/looting things at a distance, can't take items
  from other peoples storage without looting it directly
- Disguises- If you wear the uniform of another faction, NPCs will think
  you are one of them. Until you get recognised
- NPC towns can have gates, gate guards that challenge you on approach,
  and recognise unauthorised intruders and escaping prisoners

**OTHER FEATURES**

- New race added, the Shek (People keep complaining that we are adding
  races instead of fixing bugs- The guy who makes the races is an
  artist, he's not the same person as the ones fixing bugs!)
- New character editor that uses morph targets for the facial features
  instead of bones.  Looks better, gives more control, and has better
  in-game performance.
- Character models overhauled, male and female faces look much better,
  less piggy.
- New GUI re-skin and overhaul.
- Turrets are faster at aiming.  NPC guards can man turrets.
- Lots of upgrades and features added to the construction set
- Support added for level mods (to add towns and stuff to the map)
- Support added for physics object attachment to characters and animals
- AI system tune up- better performance and no task oscillation bugs
- Added auto-job for the corpse furnace (careful, they'll burn any loot
  too)

**RENDERERING**

- DX11 mode (DX9 still supported, but will look crappier and run slower)
- Lights! Night time is darker, buildings can have lights mounted on
  them
- New global illumination ambient lighting model, and BRDF material
  shaders

**FIXES OF NOTE**

- Improved the terrain collision accuracy
- NPCs won't loot someone who's being carried
- Fixed the bug where guards wouldn't protect you from bandits
- Ragdolls are now created on the background thread
- Fixed the invisible ragdoll bug
- Fixed missing upper body combat animations
- Fixed harpoons getting stuck in mid-air
- Stopped large animals trying to attack targets inside buildings

**NEXT UPDATES**

- Will be focused on bug-fixing and stabilisation
- Will have a new movement system to avoid the characters getting stuck,
  flickering, and random framerate drops caused by Havok, until then
  we've worked some quick-fixes into the current release to help things
  as best we can
- After the performance issues are sorted out the wall placement
  problems will be looked at

**CURRENT BUGS:**

- The gui is not 100% finished and full of cosmetic bugs
- The pathfinder is super broken right now (movement flickers, getting
  stuck, no collision, and performance drags) because we aren't quite
  finished with a re-write, it will be updated properly in about a week
- Still needs more features for the lights, like more techs, types,
  power-related light brightness and stat penalties for working in the
  darkness, personal lanterns
- Still needs more ways of getting enslaved
- Performance is terrible, it will improve drastically with 2 future
  updates:  The pathfinder (ETA: 1 week) and the terrain system fix
  (ETA: 1 month)

## **0.72**

### **0.72.1**

**BUGFIXES**

- Fixed animals not fighting
- Fixed squads getting the "Wildlife" faction and being hostile to all
- A few crashes that were introduced by 0.72

### **0.72.0**

This is mainly meant to be a bug-fixing update, but I got carried away
and added some AI stuff

- Wandering adventurers can be hired as bodyguards
- Unarmed NPCs can loot bodies for a weapon if needed.
- Assholes might just loot everything while they're at it.
- NPCs and bandits will equip gear they loot if it's better than theirs.
- Armour can be tagged as a uniform.  If a faction sees you wearing
  their looted uniforms...
- Sell value of loot has been halved.

**BUGFIXES**

- Animal backpacks can no longer be worn by people
- Fixed problem with characters stopping what they were doing after you
  place a building
- A lot of dialog system features and fixes, including the problem where
  you couldn't talk to following characters because they would run away
- Fixed characters forgetting their jobs or disabling machines when
  changing squad
- Pathfinding improvements for combat pushing NPCs off the navmesh, and
  NPCs getting stuck on corners of ramps
- Fixed import games with multiple squads
- Fixed the cannibals running back to the village and just getting stuck
  circling in the centre
- Fixed the chase behavior a bit

## **0.71**

### **0.71.3**

Quick fix for the annoying camera jumping around bug

### **0.71.2**

Mostly, this update just fixes lots of crashes

- Tab key cycles squads

**FIXES**

- Various crashes
- Grass was missing and I never even noticed.
- Fixed foliage stacking vertically in several places
- Fixed the "Rescue" button
- Fixed the duplicate character bug
- Fixed characters playing the get up animation when in bed
- Fixed AI not opening unlocked doors to pass through

### **0.71.1**

**BUGFIXES**

- Mostly fixing various crashes.  The notorious Havok crash is still at
  large.
- Fixed the crash with loading certain 0.71.0 savegames
- Dialog system now supports monologues and changable player_talk_to
  interruption dialogs
- Fixed the character editor FACE/BODY tabs being missing
- Fixed the turrets having 1 damage

### **0.71.0**

- Squad management! Multiple squads, character dismissal. Character cap
  increased to 50 and can be modded even higher.
- Made a SmellManager.  Bleeding and corpses now stink up the place and
  attract dangerous animals.  Wolves hunt by smell.

**BUGFIXES**

- Finally fixed the Havok loading area crash(?)
- Fixed speech boxes cutting off text at low resolutions
- Stealth state is now saved, and the checkbox is fixed
- Fixed NPCs not being visible when moving the camera around paused
- Fixed newgame window going off screen at low resolutions
- Fixed a crash related to building material storages
- Fixed the framerate drop when building certain walls
- Fixed a few more little crashes
- Fixed problem with correct floor visibility when building furniture

## **0.70**

### **0.70.6**

- Sam said "Oops, did you submit that patch yet?" and I had and he had
  forgotten to add something super important.

### **0.70.5**

- Fix for combat pathfinding (cannibals stuck in starting village)
- Took a step to temporarily prevent the occasional battle royales in
  towns, and guards attacking players
- Fixed one more random crash, and another experimental workaround for
  the main one, but to fix the main one we still need to wait for a
  software update from Havok.

### **0.70.4**

- Fixed another bug when recruiting new characters
- Fixed the problems with characters being unselectable
- Improved follow behaviour and made pack gars catch up after a fight
- Fixed a bug when dismantling
- Made a theoretical fix for the 10,000 storage items bug
- Performance improvment when lots of ragdolls are around
- Fixed furniture placement going through walls
- Fixed nests spawning extra squads on load
- Fixed some rare invisible building occurence
- Few little minor fixes with collision and an animal glitch
- Lots more crash fixes

### **0.70.3**

- Another possible stability improvement for the random crash, lets find
  out if it helps or not...
- Also fixed a few regular crashes
- Fixed armour quality resetting on load
- Shopkeeper "welcome" can now be interrupted
- Fixed nest items spawning too much when re-loading
- Fixed flophouse beds even more
- Fixed KO NPCs spotting sneaking characters
- Fixed too many NPCs having negative medic skill
- Fixed no-dialogue police chief
- Slavers wont try to capture animals now
- Fixed hair vanishing after wearing a helmet
- Fixed holes in character mesh when removing armour
- Stopped shopkeepers dropping items when restocking inventory
- Fixed crash when upgrading certain buildings
- Fixed the extra characters problem when importing a game with research
- Fixed the invisible cannibal cages bug

### **0.70.2**

- Fixed the worst moving-around-the-map random crash.
- Fixed some minor dialogue glitches
- Fixed cannibal cooking crash
- Fixed the flophouse beds not working
- Fixed the characters being ragdoll in cages
- Fixed crash when harpooning animals
- Fixed a few more smaller random crashes

### **0.70.1**

Fixes a bunch of, but not all, bugs.  More bugfixing updates coming
every few days.

The frequent random crash that comes from moving around the map is not
fixed yet, but it's our top priority.

**BUGFIXES**

- Fixed cannibals getting stuck in home buildings
- Fixed armour costing only 32 cats
- Fixed random armour stats bug
- Fixed a lot of the character movement bugs; stopping, leaving walkable
  areas
- Fixed access ramp out of Catun
- Fixed conversations randomly having no player reply buttons
- Fixed town guards not helping people, or wrongly attacking you during
  a battle
- Fixed time of day being corrupted
- Removed the "Capture" option, it wasn't supposed to be in the game yet
- Ctrl+shift+F11 regenerates pathfinding navmesh, handy for when loading
  an old savegame when level data has changed
- Fixed keybinding for camera zoom
- Fixed mysterious low number of female NPCs
- Fixed accessibility problems with saloon buildings
- Fixed flophouse layout
- Mostly fixed the shopkeeper-locks-you-in booby trap
- Fixed inventory auto-arrange crash (unconfirmed)
- Removed the option to pick up animals

### **0.70.0**

This is a massive update that changes a lot of stuff.  It was rushed out
to reassure people we're still working, expect it to be super unstable
and buggy while we spend the next few weeks stabilizing it.

Most players might want to wait another week or so before playing this
version.

**FEATURES**

- 64-bit version available. 32-bit version will continue, but will be
  less stable due to the memory limitations.
- Creatures are now mostly coded in.  Creatures will be introduced over
  time, currently we have:
  - The Beak Thing, a blind carnivorous giraffe/bird creature.
  - The Leviathan, a giant thing.
  - Big wolf things
- New dialog/AI hybrid system that takes into account situation details
  and remembers what you've done in the past.
- Thugs and bandits can now harass and rob you rather than always
  attacking on sight.  Thugs in town can insult you, then go outside the
  gates and jump you when you leave town.  NPCs can follow and chase you
  while they talk or threaten you, and know the difference if you are
  running away.
- Changes to relation system, fighting someone in the middle of nowhere
  has very little effect on faction relations.  Individuals can be
  perceived as temporary enemies or allies.
- A new terrain engine was necessary for the 64bit build (old one was
  32bit closed-source).  It looks way worse than the old one because
  we've run out of texture units for the smooth normals, but we will fix
  that soon.
- Dropped items no longer vanish underground, and they can be easily
  found with visible labels if you hold the ALT key.  They are also
  saved when you save your game.
- NPC AI now has a schedule.  They go to bed at night.  Shopkeepers shoo
  you out of their shop at closing time and lock up for the night.
- Replaced the pathfinding/movement engine with the Havok AI engine.
- New buildings available:
  - Corpse furnace, to dispose of bodies.
  - Smelter, to melt down old weapons and armour into iron
- Characters are less disadvantaged by being outnumbered, your lvl50
  warrior can now take out a group of starving bandits without getting
  mobbed. Basically they will miss more often as he moves around and
  dodges.
- More details added to the GUI, including visible calculations for
  character stats and penalties.
- Multi-threaded resource loading for smooth creation of models and
  textures.  Shorter loading hiccups when moving around the map.
- Ragdolls fixed up, less crazy ragdoll behavior.  Animation blending
  between ragdoll and non-ragdoll states.

**FEATURES ADDED NOT FINISHED PROPERLY OR USED MUCH YET**

- Buildings can now have multiple floors, but for now only the large
  house makes use of it.  The staircase will intersect furniture from
  old games.  Waiting on the shift to the new world map in a few months,
  with the new multi-story buildings to take things any further.
- Added stealth mechanics.

**BUGFIXES**

- AI follow behaviour has been improved, so squads don't tend to queue
  up behind the leader and do that stop/start thing
- It's now a little easier to click to enter buildings
- Minor GUI improvements to font size at lower resolutions
- Fixed NPC view range
- Fixes to the AI and pathfinder for dealing with walls and gates.
- Fixed some of the cannibal AI quirks
- Fixed bug where equipment with positive athletics bonuses weren't
  applied.
- Fixed modded dialogue not loading in the construction set
- Fixed the random crash when switching gender in the editor

## **0.69**

### **0.69.2**

- all NPC gear has a small chance of being +1 grade

**BUGFIXES**

- fixed crash when placing short walls attached to a gate
- chainmail crafting bench now actually uses chainmail sheets
- Fixed a bug where item stacks were being reduced to 1

### **0.69.1**

**BUGFIXES**

- upgrading walls now updates the pathfinding, and upgrades the ramps
  too
- Fixed walls having the "must be placed inside building" bug
- Fixed a crash in wall placement code
- Deleting walls now deletes the turrets on them too
- Fixed difficulty reaching lvl5 wall to build it
- All buildings now have a destroy button like walls do
- Fixed another bug with item stacking

### **0.69.0**

- Big frame rate boost!
- Totally revamped wall placement system
- Slightly better building placement in general.  Easier to place
  furniture inside buildings.
- Toughness now affects degeneration rate, meaning that rookies are more
  likely to die than veterans when defeated.
- Difficulty settings added to the New Game and Import Game windows.
  - Added an "Amount of death" slider to the new game options to
    increase difficulty.  Setting it higher than 1.0 makes ALL
    characters in the game more likely to die from their wounds (eg 2.0
    means bloodloss + wounds degenerate 2x faster).
  - "Easy prospecting" option: resources are adjusted by biome only.
  - Multipliers for research, building and production speeds
- Some subtle tweeks to the combat AI to help characters deal with being
  outnumbered slightly better.
- Bandits can now catch you if you are running away and can't run fast
  enough.
- Strength improves slightly faster from encumbrance
- "Max blood" stat is now influenced by character's strength.
- Heavy club was a bit overpowered, so I turned it down.
- Added Splint Kits to the research list
- Forgot to mention in last update, gun turrets now have an advantage
  when placed at a higher altitude than their target.  Put them on
  hills, on walls, and it will make them much more effective
- You can now upgrade or delete a whole chain of walls at once
- More SFX improvements

**BUGFIXES**

- Fixed the "reset position" for game imports
- Fixed some characters being invisible when dead or paused
- Fixed outnumbered characters causing a big freeze-up mid-battle
- You can't run away mid-stumble anymore
- Skin tone wasn't being randomised properly for NPC generation.
- Fixed a bug where splint kits sometimes cause healing to get stuck
- Fixed the high-velocity ragdolls bug
- Fixed research ETA, also daytime speed was running too fast when time
  was speeded up
- Can now delete ramps

## **0.68**

### **0.68.1**

Note that prospecting is a new feature and will undergo changes.  I have
temporarily added a "no prospecting" mod so that you can turn the
feature off if you really don't like it.

- Fixed the "Haul" job.  If you shift-click on a storage box then your
  character will automatically run around filling it with the outputs of
  other buildings.
- The AI should deal with automatic machines better now, as well as
  other little inventory/hauling related problems
- Made some tweaks to reduce the bug with the skipping ground collision
- Fixed AI bug with bandits when their squad is wiped out and they don't
  know what to do anymore.
- Fixed the world not loading properly when you started a new game from
  the in-game menu
- Fixed the sleeping upside-down animation bug
- Fixed the navmesh around the merc outpost

**NEXT UPDATE (soon):**

- Wall placement improvements
- more bugfixes

### **0.68.0**

**FEATURES**

The new pathfinder system isn't ready yet, but I have made a release of
the new features so far.  The same old bugs with the walls and collision
will persist until then I'm afraid, but it's on the way.

- Prospecting added.  The button in the bottom right makes your selected
  character analyse the surrounding terrain for resources, based on his
  science skill.
- Farming, wells, mines etc are now dependent on the available resources
  in the area they are built.  Mines from old savegames will be capped
  at a certain minimum value if they happen to be in a low or zero yield
  area.
- Random patrols passing by are now likely to attack your base and other
  towns
- Production rebalanced: Most machines and mines need way less workers,
  and also have a more pronounced efficiency improvement with each
  upgrade.
- Build speed doubled.
- Added 3 new walls and gates, levels 3-5
- Turrets now snap to fixed wall positions
- Added training turrets, so you can train your turret skills.
- Added harpoon turrets!  Including a double barrel and 6-shot version,
  if you can find the blueprints.
- Added "Enable civilians in towns" to the options.  Turning off
  civilians will improve performance a little bit.
- Added auto-save time to options

**BUGFIXES**

- You now own and can dismantle the furniture in buildings that you
  purchase
- Limited population slider options to 2x.  Too many people were setting
  it to 4 and wondering why the frame rate was so bad.  (you can still
  set higher than 2 by editing settings.cfg)
- Fixed the storage chest not working, as well as a visual bug for
  storage boxes inventory
- Fixed another inventory bug duplicating stacked items
- Changed the name of the town of Catan/Capan to Catun.  Ssshhhh...
- Made indoor buildings more tolerant and easier to place
- Stopped gates and walls appearing red before you place them
- Fixed the bug where clicking to attack an enemy that was too far away
  would make your characters just stand idle.
- Fixed a bug with the female character editor limits using the male
  limits

**HIGH-PRIORITY FOR FUTURE UPDATES:**

- 64-bit build, to prevent super-crashes
- New pathfinding/movement system
- Fixing the awkward wall placement interface

## **0.67**

### **0.67.2**

- Friendly fire that hits neutral NPCs by accident won't start a war
  anymore.
- Outdated weapons are removed from the weapon crafting list
- Leather tanning bench now makes leather out of fabric, instead of thin
  air. This is just temporary until animals are in the game.
- Fixed a nasty random crash in the last update

### **0.67.1**

- Added "auto-arrange" button to item containers

**BUGFIXES**

- Fixed a bug with duplicating swords in the inventory
- Fixed the bugs around buying buildings in towns and placing furniture
  in and around them etc. (Still buggy to import a game with purchased
  buildings though)
- Chain armour bench now actually uses chainmail as the resource
- Improved some of the error reporting details
- Fixed an occasional crash on loading from an existing game
- Fixed a portrait bug
- Found a few more smaller memory leaks that have been fixed

### **0.67.0 "Small things, stable things"**

- Added a cloth crafting bench, and a load of clothing blueprints to buy
- Added in Drifter Leathers armour set to crafting list
- Leather armour now needs leather to make it with, new leathermaking
  bench added.
- New storage box models
- New storage boxes for chainmail, leather, armour plates, wheat, water,
  hemp
- Tweaked the "Cannibal hunters" start, it was designed as a quickstart
  for players at Rezzed, so it's a little less easy now. Still too easy
  though.

**BUGFIXES**

- Fixed the crossbow upgrades not taking effect
- Fixed a memory leak and some bugs in the NPC squad spawning
- Fixed the cannibals being non-aggressive at home
- Fixed hair texture on head sometimes not showing
- Fixed the dark red inventory icons

## **0.66**

### **0.66.2**

- Hotfix for the research bug

### **0.66.1**

- Hotfix for the missing buildable buttons

### **0.66.0 "Player friendliness"**

- You can buy-back items you buy or sell at a trader for the same cost.
  No more losing money because you changed your mind or made a mistake.
- You can rotate the camera using any mouse button when in the character
  editor
- Build mode has a proper window at the top for confirm/cancel
- You can also exit build mode by pressing the speed buttons
- Research button on the town info panel opens the tech window
- Inventory item right-click first tries to equip the item
- Added lots more hairstyles and fixed the broken old ones

**BUGFIXES**

- Fixed a major memory leak that was causing the regular super-crashes.
- Fixed a problem where 1000 extra characters could spawn in the area,
  crippling the frame rate.
- Fixes to the character portraits
- Towns and research don't copy into other loaded games
- Fixed a lot of the hairstyles that were broken

## **0.65**

### **0.65.3**

- There is now an alternative exe file called "kenshi32bitOS.exe". If
  you have 32-bit windows and experience crashes, try running this one
  instead and see if things improve. (Also you should get 64-bit
  windows).
- Newgame available from the menu in-game
- Build speed is slower now.
- Build buttons look nicer, and you can build outdated tech too, not
  just the new stuff
- Improved the camera behaviour around walls
- Doors get bashed in quicker, and all the buildings have properly
  balanced door-health values.
- Sped up the door on the Small Shack

**BUGFIXES**

- Improvements to the gate-opening AI bug, but it's not perfect yet
  (waiting for pathfinder update). But it is a little better.
- Fixed a certain load game crash

### **0.65.1**

- Character stats weren't increasing, fixed now.
- Fixed the wall height bug when placing walls
- Fixed an inventory item duplication bug

### **0.65.0**

**FEATURES**

- New Walls and gates (level 1 & 2). Old walls are phased out. Levels
  3-5 are coming soon, along with defence towers.

**BUGFIXES**

- Fixed the corrupted character stats (usually dexterity) bug. Existing
  corrupted characters will be fixed, but stats will be guessed.
- Characters can't shoot themselves anymore
- Halved the number of targeted bandit assaults, as it's only a
  temporary system for now.
- Fixed build mode crash
- Few other small crash fixes

## **0.64**

### **0.64.2**

- Fixed turret category not showing in the build menu
- Hopefully fixed the rare occurrence of characters attaching to
  harpoons and getting shot off into the distance.
- Fixed duplicating inventory items bug
- Fixed a crash during building placement

### **0.64.1**

- Fixed map screen crash
- Fixed wall ramps

### **0.64.0**

- Added crossbow turrets!
- Added a get up off the floor animation, as a temporary improvement to
  the medical system feel
- Improved the encounter rate, so hopefully you will run into bandits
  more, like in older versions.
- Toughness XP is based on amount of damage received, instead of enemy
  attack skill. More pain = more gain.
- New sky system now in place
- Medkits in your inventory have GUI bars to show how full/empty they
  are.

**BUG FIXES**

- Combat sword hit-boxes and ranges have been refined, so less missing
  your targets
- Characters who cant carry anyone because they've got an injury will
  let you know, instead of just standing there
- Wounded arms now stop dangling once healed
- Stacking medkits won't re-charge them, they will merge instead.
- Fixed the AI for the "bodyguard" task. It can also now be
  shift-clicked to make it a permanent job.
- Renamed city of Catan to "Capan" since I found out "Catan" is already
  the name of a well-known boardgame.
- Fixed the vanishing hair bug

## **0.62**

### **0.62.1**

- Fixes crashes
- Makes the bandit attacks less frequent

### **0.62.0**

- Your base will get randomly assaulted by dust bandits, starving
  bandits, and sometimes cannibals.
- Sometimes the hungry bandits will try to rob you and take all your
  resources. Lock up your storage boxes in a safe building!

(Added the Splinting feature back in. Splint kits now work, but can only
be used on arms and legs. It's automatically done during first aid if
the medic has a splint kit.

- Added auto-save to the options
- Shopkeepers and their bodyguards won't keep running out to save the
  town, all town guards won't stray too far from a town when chasing
  down enemies
- Shortened some of the level 1 research, all research 25% faster,
  building speed 2x slower
- Added a new farming village, planning to do more with it later

**BUGFIXES**

- I fixed a pretty significant memory leak, so hopefully that fixes or
  at least improves the "super crash"s

dust bandit raids now go home after defeating you

- added in female backpack models and a few other clothing tweaks
- Fixed a ton of bugs in the faction assault system
- Fixed a bug that gave all hungry bandits a +5 to combat skills
- Fixed the "Failed to load compositor" crash that some systems were
  getting. (untested)
- Fixed the multiplying/vanishing shopkeepers when big changes made to
  the population options (import required to restore
  shopkeepers)(untested)
- Put error logging and "save failed" warning message to try and catch
  the cause of corrupt savegames
- Fixed KO time increasing when loading game
- Many crashes fixed from player crash dumps

## **0.61**

### **0.61.1**

**BUGFIXES**

- Fixed interior buildings vanishing when you build something
- Fixed population sliders affecting shopkeepers (import)
- Fixed first building sometimes getting linked to wrong town for power
  consumption

### **0.61.0**

- If a vital bodypart (head/chest/stomach) goes below 0, then it causes
  a knockout
- A knockout is based on a timer countdown. The time is a total of all
  the characters damage, including bloodloss (head counts for double
  time, limbs count for half)
- Once this timer counts down to 0, the character can get up again if
  his vital parts are still above -50
- Vital bodyparts slowly degenerate when they are below 0 (unless
  bandaged). So once its below -50, you will die without medical
  attention.
- Once a vital bodypart degenerates below the -50 point he will go into
  a coma and can't wake up until all vitals are above 0 again.
- If blood goes below 0, he will KO. However once the KO timer runs out
  and blood goes above 0 and he gets up again, the next KO point for
  bloodloss will be -25. This allows him to fight a bit more, gets him
  closer to risk of death, and prevents the "constantly getting up then
  going down again in one hit" problem.
- So a character can get up and fight again with, say, -30 chest damage.
  He will go down again instantly if he is hit in the chest, and it will
  be worsening the whole time if he doesn't get it bandaged
- As before if a vital bodypart reaches -100 then it means death
- If a non vital bodypart (eg an arm) goes below -100 then it will cause
  slow bloodloss until death. Eventually I will implement severance, so
  -100 will mean you lose the limb and will need a robotic replacement.

**The end result:**

- After a battle, some characters may die, some may lose limbs, some
  will go into prolonged comas, others will recover and heal themselves
  or die later. They never get stuck in a limbo state where they are
  unconscious forever. Battles are more interesting.

**New "Toughness" stat:**

- I said before that you reach a critical point of no return when your
  health goes below -50. That was a lie, the actual number is based on
  your toughness and can range from -10 to -80 if you are mega-tough.
- Toughness stat is increased primarily by getting hurt.
- Toughness has a huge XP bonus if you are fighting while critically
  wounded or crippled
- You earn a huge toughness XP reward if you force your characters to
  get up and fight again while they are down and "Playing dead" so that
  the enemy leaves. 'Cus that's a tough thing to do. The bonus is also
  multiplied by how many of them there are.
- Affects damage resistance instead of Melee Defence

**OTHER STUFF**

- Way more bandits
- Stats window has more useful information, derived stats and training
  advice
- blood recovery rate reduced from 0.5 to 0.3
- Cannibals use clubs so victims don't die on the way to the cages
- Cannibals are a little stronger to compensate for using clubs

**BUGFIXES**

- Fixed shopkeepers not coming back to their shops
- Fixed stats of Sleeveless longcoat
- Fixed that random crash that was going on
- Fixed some rare crash on load bug

## **0.60**

### **0.60.0**

- Assaults! Bandits and other factions will approach your base and talk,
  giving you a chance to grovel, pay, join or anger them. This way you
  can avoid impossible fights at the early stages. Diplomacy in Kenshi
  is all through face-to-face dialogue with NPCs. Only 1 assault type is
  in there to start with (dust bandits), more will be added over time,
  from different factions.
- Characters can give reasons why they are incapable of doing a task (eg
  the machine has no power).
- Bleed rate is now shown in the GUI with arrows instead of a confusing
  number.

**BUGFIXES**

- Fine-tuned the worlds population movements, so you should find you
  encounter way more bandits and stuff now.
- Cannibals kill their prisoners properly now.
- Fixed bug that made corpses vanish too fast
- Research tree is disabled with a helpful message when you don't have a
  research bench, easier for beginners to understand things then. Also
  default basic technologies are added back instead of needing the
  Outpost blueprint

## **0.59**

### **0.59.1**

- Experimenting with making it more deadly. Bleeding takes 33% longer to
  stop. Blood recovery rate reduced by 1/6th. Bleed rate increased by
  about 65%, negative bodypart bloodloss doubled.
- Bodyparts injured below 0 actually degenerate slowly until bandaged.
- Added steel bar storage box

**BUGFIXES**

- Some crash fixes
- Fixed the ragdolls not re-initialising on game load
- Fixed an AI bug that stopped the lockpick training working properly,
  and probably did other bad things too.
- Fixed up trader shopping AI a bit, haven't tested in all situations
  though
- Fixed the blunt damage levels of clubs

### **0.59.0**

- Added a direction arrow to the world map, so you can see which way you
  are facing
- Thievery skill is now active and applies to lockpicking success
- New lockpick skill training objects to be researched and built
- When a bodypart is wounded below 0 and left un-bandaged it will cause
  slow bloodloss until death.
- Upped the bloodloss rate again, due to popular request. It was mainly
  the horsechoppers that had a reduced blood-loss effect. The reduced
  bloodloss from cannibal cleavers is intentional, because they like to
  keep you alive...
- Upped the number of trader caravans a bit
- Improved trader and cannibal AI, stopped them standing around in the
  desert

**BUGFIXES**

- Fixed escaping from cages
- Fixed up the cannibal AI a bit more
- Fixed "reset squad positions" on import game
- NPC faction patrols heal you if allied
- Fixed the multiple plastic surgeon problem when turning up the squad
  sizes in the options
- You can no longer accidentally close shop doors

## **0.58**

### **0.58.5**

- Added 2 gameplay options, to increase the number of squads roaming the
  desert, and to increase the overall size of squads. It will have a
  strong effect on difficulty and fun, but beware that setting it too
  high will damage performance.
- fixed the ghost town bug. You will need to import to a new game of
  course.
- fixed crash when sometimes attaching walls to gates
- fixed a small crash
- You should now be able to put captured bounties directly in police
  station cages
- Fixed the inventory icons for shirts
- Tweeked the lighting to give less of a cell-shaded look

### **0.58.4**

- Fixed crash on loading savegames
- Flophouse beds now usable again
- Restored police chief in police stations
- Fixed the building interior/terrain clipping

### **0.58.3**

- city patrol spawns reduced by 2 thirds, more bandits
- Fixed cage-escaping
- Fixed respawning of the "homeless" squads such as dustbandits, so the
  desert doesn't end up deserted.
- Squads were wandering way off the world map and getting lost, making
  the desert empty. They'll start to wander back now, though it might
  take a day or two.

### **0.58.2**

- Fixed some import-game crashes
- Characters no longer try to lock-pick their own doors to open them
- Temporary fix for the lighting darkness problem
- Stopped the black dragon clan, they weren't supposed to be there
- recruit female chance upped to 40%

### **0.58.1**

- A temporary quick-fix for the blue screen bug. This forces "disable
  terrain cutting" in the options, so the side effect is that some
  buildings will have terrain penetrating the interiors.

### **0.58.0 "Cannibal!"**

- Female characters are now in the game (can't recruit females in demo
  version though)
- Cannibal faction: They capture people and take them back to their
  camps and put them in cages. In future versions they'll eat your guys
  one limb at a time until you can rescue them.
- All NPC squads and patrols are persistent throughout the game world.
  They don't spawn/unload, they wander seamlessly. If a town or faction
  suffers heavy losses, then you will notice there are less of them
  around.
- You can now pick locks on doors and cages. New "thievery" skill. No
  stealth system yet though.
- Beards!
- Your characters have proper portrait icons on the GUI
- More sound effects and tweaks
- New weapon type- Cleaver
- Weapon types now have different bleeding effect damage multipliers
- Some passing patrols will heal wounded strangers (ie you)
- World map color-codes towns and outposts so you know which are hostile

**BUGFIXES**

- Resource containers now have infinite capacity. This stops AI
  production from blocking up and confusing both players and AI, and I
  think is a nice easy alternative to DF style leaving excess resource
  items all over the floor.
- Fixed some bugs with Town markers, you're less likely to create
  multiple towns by accident, or see a town from a past game
- The game now keeps rendering when the window doesn't have focus. This
  will help those with multi-monitor setups
- The science skill was increasing 10x faster than it should, that is
  now fixed.
- Loading/saving fixed for when carrying characters / being carried
- Fixed the right-click menu on character portraits not working
- Fixed the game not being saved if you don't enter a save name
- Hopefully fixed the key-binding bug
- Fixed ceiling fans appearing on the floor, but it will only fix new
  games or towns you haven't visited yet
- Fixed faction relations not loading/saving properly.

## **0.50**

### **0.50.3**

- Improved responsiveness issue with mouse clicks
- Stopped the AI from opening your gates for no reason
- Fixed bugs with paying research fees
- You can now open/close/lock doors and gates with the GUI buttons
- Fixed font scaling in the orders window
- Fixed craft window list scroll bar not resetting, giving appearance of
  no items available
- Characters put their swords away when using machines
- Fixed the shops in towns vanishing when you build nearby
- Tried something that might fix or improve the random 'super crash' bug
  that is caused by running out of memory
- Fixed certain injuries not healing when bandaged to under 50
- As a temporary way of dealing with the problem of ragdolls falling
  through the terrain, it's now detected and the ragdoll gets frozen and
  teleported back to the surface, in a wierd-ass frozen pose.
- Doors and buildings now have a health value based on their materials
  cost.
- Sam tracked down a mean bug that caused some major random crash when
  moving around the map loads
- Fixed the foliage appearing in the dunes

### **0.50.1**

- Fixed the random crash bug
- Fixed the invisible drag-selection box
- NPCs stay in prison when save/load occurs
- Swords show on characters properly
- Fixed armour stun percentages not adding stun damage
- Improved crafting item drop-off AI
- Fixed AI bug where bodyguards would ignore personal attacks, or not
  help each other

### **0.50.0 "Ears"**

- Audio! Sound! Music! Sound effects will be added to in future updates.
- Armour crafting
- Overhaul to armour and stats.
- 11 new hats and helmets.
- New game start-off: "Rock Bottom"
- New character orders:
  - Non-combat mode: Character only fights for self-defence
  - Taunt mode: Character attracts more of the enemy attackers
  - Chase mode: Disabling this stops a character from chasing after
    fleeing enemies

**BUGFIXES**

- Fixed the bug with the inventory auto-arrange button permanently
  changing your character stats
- Fixed blueprints loading/saving properly in your inventory
- Fixed removing items from inventory not reducing encumbrance
- Fixed the discrepancy in displayed research times
- Improved crafting item delivery bugs
- Fixed neck thickness bug in the character editor
- Fixed GUI clipping on the crafting and research windows

## **0.47**

### **0.47.0 "Blueprints"**

- Inventory now has a handy "Auto arrange" button
- Various research can now be bought at shops in the form of blueprints.
   You have to buy the basic blueprints in order to build a base now.
   Get them from the construction trader, the guy who sells the building
  materials
- New shops for the construction trader.
- You can now craft medkits
- Researching the next Technology level now costs money.
- Different weapon types for crafting must be obtained via blueprints,
  available at weapon shops.
- Equipment shops vary based on the local faction.  For example, The
  Holy Nation specialises in cleavers.
- Crafting benches now have their own separate crafting queues, rather
  than having one queue that automatically chose a bench to assign the
  job to.
- You can mod the min/max character proportions by editing
  data/male_editor.cfg
- Item values are now calculated dynamically from the value of the
  materials they are made from

**NOTES**

- Can't build wells or farms anymore? You need to buy the blueprints
  now.
- The old medium and light plate armours have now been deleted, you
  might want to sell them before updating.

**BUGFIXES**

-
- Fixed building placement on other objects
- A few AI fixes for operating machines
- reduced chances of characters spawning under a buildings floor

## **0.46**

### **0.46.1**

Quck crash fixes

### **0.46.0 "Not Super Exciting"**

This update is mainly for fixing up some of the bugs with walls

- Proper load/save window, so you can have multiple save games.
- Configurable controls

**BUGFIXES**

- Fixed wall ramps appearing 100m up in the air
- Various usability fixes for wall placement
- Fixed the characters randomly opening your gates
- Fixed the bug for long walls having no collsion/pathing data
- Fixed linking final wall piece to a gate
- Research queue now shows you when you need a newer bench
- Game speed buttons are highlighted

## **0.45**

### **0.45.0 "Walls"**

- Added walls back, with an AI overhaul. Not 100% bug free yet, but good
  enough for you to play with for now.
- Added chain mail vests

**BUGFIXES**

- doors and gates are correctly open/closed after quickload.
- Fixed some bug with town border ranges
- Fixed some values vanishing from mod files in the constrution set.
- Research bench GUI updates now when you delete from the list
- If your gates are locked, characters wont try to open them to go out
  and fight if you are attacked.

## **0.44**

### **0.44.1**

Forgot to mention in last update: Characters will look more muscular as
their strength stat increases

- Fixed shirts, added some more ones too, vests and turtlenecks.
- Fixed players starting gear
- Fixed wandering traders behaviour some more
- Fixed weapon crafting getting stuck after one item is made
- Weapon smiths now automatically take finished weapons to the nearest
  Weapon storage. Make sure they wear a large backpack so they can
  transport larger weapons though, or they'll get stuck.

### **0.44.0 "Culture and stuff"**

This is a major overhaul to the items and artwork.  Many items are being
phased out and replaced, you may find some of your gear (like straw
hats) looks wrong, they need to be replaced.  NPCs will also be
geared-up wrong, so you will need to import your squad into a new game
world to fix everything up.

- New AI Job system.  Shift-click when giving an order and it will
  become a permanent job for that character.  Eg shift-rightclick on a
  half finished building and he will become an engineer, helping out
  with all building jobs that appear.  If you give him an order he will
  do it, then go back to building when he is done.  Jobs can be removed
  in the orders panel in the bottom right.
- Character AI jobs are also loaded and saved
- Face customisation added to character editor
- Hair for characters
- Wandering traders should now work and buy stuff from your shop
  counters.  They don't want your crappy looted swords though, they want
  food and booze and trade goods.
- Totally new male character model
- Entirely new bunch of armour and clothing, replaces most of the old
  stuff
- You can find plastic surgeons in bars, basically they just re-activate
  the character editor for you.
- Clothing and armour can modify your speed and combat skills
- Clothing worn by some factions is tagged as a uniform.  This reduces
  the re-sale value, and in future updates will have diplomatic effects
  too.
- NPCs are now more random and unique-looking

**MAJOR BUGFIXES**

- Traders no longer permanently run out of money
- Fixed the negative research progress bug
- Game pauses during character creation, so you don't get attacked
- Map screen now shows player towns again
- Fixed AI problem where characters would run back and forth without
  doing anything

## **0.42**

### **0.42.2**

- Integrated on-screen character name texts with GUI, so they don't
  appear on top of other panels.
- Characters now choose storage boxes to get resources from, before
  resorting to the machine outputs.
- Characters now choose the nearest storage box if there are several to
  choose from.
- Research speed is displayed at the top of the research window.
- Added Steel Refinery to make steel bars from.

**BUGFIXES**

- Fixed Holy Servants having no weapons.
- Fixed complications when multiple characters tried to pick someone up
  at the same time.
- Science skill now applies properly to research speed.
- Fixed building power on/off buttons.
- Fixed game freeze when building if you still had gates.
- Fixed characters sometimes freezing after build mode.
- Fixed newly crafted items not saving when left in bench.
- Fixed the shopkeeper inventory crash.
- Fixed the quickload problem when not all the map zones would be
  loaded.
- Fixed the crafting window list being too short.

### **0.42.0 "Crafting"**

- Weapon Crafting. Awesome.
- Ore mining.
- Stone/Ore mining upgrades, automated mines.
- Weapon types have been refangled around.
- Certain weapon types now give bonuses or penalties to attack/defence
  skills.
- New game start-off: "The Holy Sword".
- Characters will let you know if they don't have any inventory space to
  collect some goods, and all the storages are full
- When a character is working at something, the info window will show
  you which skill is being used, and the effect it has on his work
  output.

**BUGFIXES**

- Added extra Screen resolution option to the in-game options menu,
  because lots of people missed the one at startup.
- Fixed the bug where if you got negative money, you couldn't get paid
  for selling items
- Fixed crash when pressing the Rescue button

## **0.40**

### **0.40.5**

Only bug Fixes again, I'm afraid I have spent most of the since the
Steam release sorting out Steam keys and doing tech-support stuff. New
features coming next.

- More fixes to prevent situations where characters get stuck inside
  structures, you can also re-generate the path-finding data in an area
  by pressing ctrl-shift-F11 to fix it if your guys are stuck
- New orders section in the GUI, in preparation for future features
- Fixed a few rare crashes
- Fixed a bug with duplicating items and when changing some item numbers
  in the construction set
- Fixed that bug with the inventory item sticking to the mouse when
  closing the inventory

### **0.40.4**

- Characters won't get stuck in/on any newly built structures. If you
  have characters stuck in an old structure, build/dismantle something
  close by to re-generate the pathfinding data nearby. Or better yet,
  dismantle it and rebuild.
- Fixed occasional crashes just after game starts, but now wall-related
  AI won't work. That will be overhauled in the next major wall update.

### **0.40.3**

- Can now stop/start research without losing your progress
- Mods now work properly when you edit linked objects values in the
  construction set
- Fixed some crashes on loading a game
- A few other minor bug fixes

### **0.40.2**

- Weapon skills now level up properly.
- Added a special button to dismantle walls when they're selected
- Fixed pathfinding bugs caused by dismantling gates
- Repairing buildings and doors now works again
- Fixed training dummys, they weren't training properly.
- Fixed character movement glitches when running game at 4x speed
- Fixed some problems with characters getting stuck under the floor and
  unable to leave buildings
- Fixed some dismantling bugs/crashes
- I think that random crashing on save (leading to ghost towns on
  reload) is now fixed. No way for me to test it to know for sure, but I
  have a good feeling this time.

### **0.40.1**

- Disabled walls. They're too buggy, I will add them again soon.
- Fixed bug that gave you more money on every save/load
- Fixed newly recruited characters not fighting
- Fixed doors not being clickable after a reload
- Fixed the short character view distance
- Did something that may or may not have stopped those random crashes on
  load/save. We will see.
- Fixed some player furniture showing as "for sale"
- Inventory item placement is a little easier

### **0.40.0 "Mining, Farming and Research"**

**BIG FEATURES**

- Research - New research window, build a research bench to upgrade or
  unlock new buildings and technology.
- Mining - Mine stone and process it into building materials
- Farming & brewing - Farm crops and process into food or booze
- Shop ownership - Traders and civilians actually wander around buying
  stuff from shops, you can open a shop and sell food and drink
- Buying buildings - You can buy existing buildings in towns and use as
  a safehouse or open a shop.
- Electricity - Most buildings need power to operate, so you need to
  build generators and batteries to run them
- Starting points - If you start a new game there is now a choice of
  starting situations.  Many more will be added over time, and you can
  easily add your own with the mod tool.
- Advanced training dummies can be researched
- Defensive walls with town gates can be built.  Much more will be added
  to this later on.

**LITTLE STUFF**

- Added texture quality option.  Reducing quality will improve load
  times and possibly reduce random crashes on slower systems.
- Many characters building the same thing is less efficient.  The first
  builder works at full speed, the 2nd builders' contribution is halved,
  the 3rd guy is just a quarter speed and so on.
- Rate of strength increase is reduced to 25% for carrying and 50% for
  combat.
- Strength and all other stats have a different exponential calculation,
  so they progress more slowly at higher levels.
- Escape key closes all open windows before opening the menu on the
  second keypress
- Fixed some very rare cases of characters being teleported to the top
  of the map
- Building materials are half the price
- Performance improved when lots of characters are around

## **0.33**

### **0.33.0 "Oh wow it's the big update! ...Oh wait, no it's not ...that sucks."**

This is just a stability update, fixes tons of bugs to help you guys
suffer less while waiting for the big 0.40 update.

- Dead NPC corpses now decay and vanish after about a day.  This is
  mainly for performance, so your base doesn't end up with 1000 corpses
  around it.  As cool as that would be, it would kill performance.
- You can now rename your towns/outposts

**BUGFIXES**

- Fixed bug where dexterity could drop instead of increase
- Fixed building furniture sometimes appearing above or below the
  buildings floor
- Fixed bug where you couldn't put people in beds
- Properly fixed the failed ragdoll bugs now
- Fixed an inventory/stealing cheat
- Little bugs fixed: flashing grey box when you open inventory, physics
  running while game is paused, cage crashes
- Fixed the vanishing bounty character bug, when you carry a bandit a
  long way and he vanishes, or he vanishes from a cage
- You can now create more than one player town and it will save properly
- Fixed it when medics don't always move on to the next patient
- Fixed the blue inventory icons bug

## **0.32**

### **0.32.0 "Night & Day"**

- Added night/day cycle.  Its only cosmetic for now, but it gives a
  concept of time, which is needed for next updates.  Make sure you have
  "Fancy Shaders" turned on in the options to avoid ugly graphics bugs.

**BUGFIXES**

- Fixed bug with buildings not showing fully again after entering them
- Reduced the occurence of the bug when enemies don't go into ragdoll
  mode when they should.
- Minor performance boost, and possibly better stability in
  multi-threaded mode.
- Fixed inventory held by mouse cursor sometimes vanishing in certain
  curcumstances
- A few crash fixes
- Fixed bug where sometimes a character can't move after getting up from
  ragdoll state
- Fixed newly recruited characters being un-clickable
- You don't get bounty rewards from using your own cages now, and can
  only claim a bounty on a character once.
- Unconcious enemies no longer vanish when you save/load.  This might
  slow performance if you hang around in an area for a long time and the
  bodies start piling up.  Will add body decay or burial next update.

## **0.31**

### **0.31.0 "Bounty hunting"**

**FEATURES**

- Bounty hunting.  If you defeat an enemy with a bounty, carry them to a
  police station and either talk to the chief there or put them in one
  of the cages.
- Sexy new fog system.  I call it "Sexyfog".

**BUGFIXES**

- Fixed some bugs with cages and carrying.
- Fixed the Black Terrain bug for some rare video cards
- Shouldn't crash as much now
- Shouldn't crash on exit

## **0.30**

### **0.30.6**

- Properly found the actual source of the freezing bug now, I was just
  treating the symptom before.
- Fixed drag selection with the shift key pressed

### **0.30.3**

- Tweeked some combat variables, gangs that outnumber you will hit you
  more, carrying your buddies is a little lighter on encumbrance
- Fixed bug with characters sometimes teleporting short distances
- Fixed a crash and a lot of bugs importing with buildings
- Fixed 2 random crashes
- Fixed lots of bugs with building, and sleeping
- Fixed bug when dismantling.
- Other bugs fixed too, I forgot what though.

### **0.30.2**

Hunting the crashes, lots of crashes fixed.  0.30.1 was a pretty bad
release stability wise, I will continue fixing bugs at super sonic
speed.  There are still plenty of bugs around, but I wanted to get this
update out quickly.

- Outposts also act as flophouses now
- Sorted out the town populations, lack of traders etc.
- Can no longer carry people if your left arm is buggered.  In future
  you will be able to carry on right side instead.

### **0.30.1**

A big bunch of bugfixing **FEATURES**

- More options for importing your squad to a new game.  You can import
  your buildings too, or use it to just reset all your characters
  positions if someone gets stuck on a roof or something.

**BUGFIXES**

- Fixed lots of combat spazzing behavior, especially in 2 vs 1 fights,
  tweeks to the combat AI too
- Fixed crash on loading game
- Fixed the mental shopkeepers
- Fixed crash when you pick someone up
- Fixed the ghost town bug even more.  Now its like, 200% fixed.
- Other crash fixes
- I'm getting closer to fixing the Black terrain bug that some people
  are getting but this will take some time, as I am entirely dependant
  on help from people on the bug forums.

**NEXT UPDATE:**

- **Bounty hunting!**

### **0.30.0 "Re-Population"**

Lots of huge internal changes, but it won't seem like much has changed
gameplay wise **FEATURES**

- Massive code restructure.  Put entire physics system on the background
  thread, slight performance increase and world load times are now just
  a couple seconds.
- Flophouses added to some towns, you have to pay to use the beds.
- Made a town auto-population function so it will be easy to add new
  guilds and shops etc

**BUGFIXES**

- Fixed the new ghost towns bug (will need a restart/import to fix it if
  you have this bug)
- Fixed the level editor crash
- Enemy prisoners are now considered non-enemies, so passing squads
  won't attack them.
- Crash dumps give me a bit more information now, not that you really
  care.
- Lots of fixes

## **0.29**

### **0.29.7**

- Made weapon speeds less drastically affected by inventory encumbrance

**BUGFIXES**

- Traders don't visit your base and get in the way all the time
- Can heal someone or pick them up while they are in bed
- Fixed the bug where characters unlock the door before using a cage or
  bed, but only on newly built stuff
- NPCs in bed or in a cage will load and save correctly
- Made the startup config window show less useless options so its easier
  to notice the screen resolution setting

### **0.29.6**

- Made the GUI more clear about when your stats are being affected by
  your equipment.
- Fixed a few more bugs
- Importing squad only imports players faction relations.
- Did some magic that will help with some slowdowns
- Possibly improved the problem that causes hundreds of wandering
  traders to collect in an area

**SAVE CORRUPTION**

- Rearranged the savegame code so that it saves your squad 1st, so if it
  crashes you can still import your squad.
- Your previous savegame is backed up to a folder called "bak".  Rename
  the folder to replace "quicksave" if you want to restore the old save.

### **0.29.5 "Tuning"**

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
  a little from your combat stats.
- Tweek: Bleeding rate down 33%, bleeding clot rate up 50%. This brings
  more focus back to bodypart damage over plain boring bloodloss.
- Medkits drain twice as fast when used by a novice medic.
- You can build cages, and stick prisoners in there. Not much else to do
  yet, its still unfinished.

**BUGFIXES**

- Fixed crash when closing map window
- Made a fail-safe in the rare event that there is a certain crash while
  saving, so it will finish up before crashing and avoid corrupting your
  savegame.
- Fixed encumbrance affecting combat speeds
- Fixed bug with the pathfinder when demolishing structures
- Medkits now vanish from your inventory when used up.
- Improved the medic AI behaviour bugs when in battle
- Backpack contents affects total weight even if not equipped.

### **0.29.0 "Encumbrance"**

- Encumbrance has an effect now. Your inventory and gear will weigh you
  down, making you move slower. How much you can carry depends on your
  strength.
- Your encumbrance is shown in the inventory window.
- The stats panel in the corner shows you if you are gaining strength or
  athletics XP based on your encumbrance.
- Strength is also increased by walking about with a heavy inventory.
  The heavier it is, the faster the increase.
- Better look closely at your inventory now to see what you can still
  carry. If you are one of those sneaky people with a shopkeepers
  backpack, you might want to get rid of it now.
- Athletics skill is now functional. Running at full speed without any
  encumbrance will improve it.

**FIXES**

- Inventory item icons now have transparency
- Fixed the bug where 100's of caravan traders could swarm around an
  area. If you have this you will need to import to a new game to get
  rid of them. Or kill them all.
- Fixed another dialog system bug where you could hire Wingwang for
  free.
- Fixed bug where you couldn't lock your doors
- Fixed the bug where you sometimes couldn't loot bodies

## **0.28**

### **0.28.2**

- Fixed dialogue choices sometimes having the wrong result
- Fixed new NPC names not being loaded
- Squad recruitment capped at 20 for now, to stop the GUI overflowing
- strength increases at half the speed (preparation for next update...)

### **0.28.0 "Recruitment"**

- Bars now have a range of recruitable characters, a couple are unique,
  most are randomly generated. There will be a better range later once
  all the new character models have been made.
- Added a RESCUE button, next to the medic button. Selected characters
  will pickup their wounded allies and put them in a bed if any are
  available.
- Certain NPCs have unique names. The Indiegogo peoples names are now
  included.
- Fixed the Bodyguard behaviour. A character in Bodyguard mode will try
  to take the heat off their target by attacking his attackers, and
  staying close in battle. A good way to protect a new recruit.

**FIXES**

- Importing your squad to a new game now imports your faction relations
  too. Now you can't exploit it by robbing traders and importing to a
  new game to avoid the factions repurcussions. The traders guild is
  very sensitive.
- Fixed, or at least reduced, the bug where characters in defensive mode
  can get in a stalemate where nobody attacks.
- Fixed the missing Dust Bandits.

## **0.27**

### **0.27.2**

**BUGFIXES**

- Overhauled combat code, things should be smoother now
- Fixed characters spazzing out at their destinations sometimes
- Fixed a trader exploit
- Disabled key controls when typing into the faction name box
- Fixed a bug that may make NPC squads vanish.

### **0.27.0 "Options and Camera"**

- Changed the camera code based on player feedback. Its a little
  different now and won't drop off cliffs so easily.
- Added an options screen to main menu. Can invert camera controls and
  stuff.

**BUGFIXES**

- Fixed building dismantling bug
- Fixed furniture placement bug
- I disabled the quicksave backups, to see if it is the cause of the
  ghost-towns bug.
- Fixed the speed of the credits when not in vsync mode
- Fixed the mouse pointer sticking to screen edges in when camera
  tracking a character
- Fixed character portraits showing incorrect character state

## **0.26**

### **0.26.9**

You might have noticed some factions threatening you for money in the
last update. That was an accident, its been disabled because its not
finished yet, it will be enabled again in version 0.27 **BUGFIXES**

- Fixed player furniture sinking into the floor after many load-save
  cycles
- Stopped mouse cursor moving when rotating camera
- Fixed skills being capped at 20 for paid version of game
- Fixed npc recruitment bug
- Might have fixed the looting bug too, diddn't have a chance to test it

### **0.26.8**

- Fixed bug where you could only talk to traders once
- Added start of Faction window (via map screen) where you can re-name
  your faction

### **0.26.4**

**FEATURES**

- Swapped left and right mouse buttons when placing buildings. Look out
  for that one!
- Added progress bar when using training dummy
- GUI panel that shows basic faction relations, and shows a separate
  long-term and short-term relation status.
- Some NPCs like envoys and nobles can have higher diplomatic value, so
  actions against them will make factions much more angry. Works the
  other way too, eg a faction may consider its peasants worthless so
  raiding them wont affect relations much.
- Faction relations can now be influenced positively, by healing npcs or
  putting their wounded in beds to recover.

**BUG FIXES**

- Fixed inventory window cut-off bug
- Made certain animation movement smoother
- Mouse uses windows mouse motion. If you still find it laggy, you can
  set "hardware_mouse=1" in settings.cfg
- Stability and crash fixes.

### **0.26.3 "Building begins"**

This is the first building update. Its only the start, future updates
will be adding to it. Character names and NPCs from the indiegogo
campaign are not in yet, but the credits are done. If your name is
missing from the credits, you need to email me. **FEATURES**

- BUILDING: Get enough building materials and you can build your own
  structures outside of towns.
- If you own a building, you can now lock the doors (using the
  right-click menu). Enemies will be forced to bash their way in.
- You can build various item storage containers indoors.
- Healing rate is halved, but is 5x faster if resting in a bed. If
  unbandaged, resting in a bed will prevent the wounds from getting
  worse.
- You can carry an unconcious character and put them in a bed to
  recover.
- You can use training dummies to improve your attack skills
- Shopkeepers refresh their inventory every 20 minutes

**BUG FIXES**

- Fixed tooltip info on weapons and armour being cut off
- Fixed timer bug, character motions are smoother now
- Re-enabled trading

## **0.25**

### **0.25.5**

- Made a performance boost
- Fixed the right-click auto trade functions
- Fixed crash on shift-rightClick
- Again, think I fixed the random crash on quicksave.
- Fixed a crash when entering certain areas of the map

### **0.25.4**

- Traders backpacks have replaced with a new version, they are smaller
  but stack more items. Old ones will not be sold anymore.
- Bandits don't use katanas anymore.

### **0.25.0**

This is a mini-update to fix a couple of major bugs. I'm still working
on building and its almost ready.

- Overhauled the material system. Things are sexier now, like my beard.
- I think I fixed that nasty crash when you quick-save, at least it wont
  erase your savegame
- Tried something out to possibly fix that reccuring random crash.

## **0.24**

### **0.24.3**

- Tutorial window appears on your first play. To bring it up use the
  "Help" button, just below the map button.

**BUG FIXES**

- Characters get stuck less often
- A crash fixed
- Fixed the screenshot overwriting bug

### **0.24.1**

- Disabled BUILD button. It was enabled by accident in the last release.
- There is a problem with savegame corruption that I'm trying to track
  down. Until then I've installed a backup routine that will import your
  squad to a new game, although you will lose your money, so it gives
  you 10,000 in compensation.

### **0.24.0 "Exciting doors"**

Some of this will require you to start or import to a new
game. **WARNING!!**

- Price of trade goods has been reduced, I recommend you sell ALL your
  trade goods before you update the game.
- The purpose of this is to fill up your backpack more, and try to put a
  cap on the upper income of a high level trader. I want the big money
  to be earned from buildings.

**FEATURES**

- Doors! Please report it if characters are getting stuck or doors are
  impassable etc. Doors cant be locked yet.
- You can no longer buy the higher grade armour and weapons. You will
  have to research and craft them later on.
- Price adjustments. Low level items are cheaper, high-items are more
  expensive. Traders backpacks don't stack so many items.
- New mouse pointers

**BUG FIXES**

- Big framerate increase for some people
- Still fiddling with the pathfinding/movement system
- Fixed that outpost in the north, now it has a proper crew
- You now have to be within 200 meters to trade items with someone.

## **0.23**

### **0.23.5**

This is just a small stability fix until I release the next major update
coming very soon. **BUG FIXES**

- Fixed the "thread error" crash
- Fixed some new crashes
- Fixed some long delays in loading NPCs after quickload

### **0.23.3**

**FEATURES**

- started working on building placement, but you don't get that yet.
  Hahar!

**BUG FIXES**

- character movement is not so flickering and jerky
- game now runs on single-core CPUs
- Fixed various stupid movement bugs
- fixed a random crash
- fixed some bugs with carrying characters

### **0.23.2**

**BUG FIXES**

- tried doing something that may have fixed the savegames crash
- fixed bug where backpacks could vanish when trading
- fixed stats window showing all zeros
- made it a little easier to place items in the inventory
- fixed bug where characters dont move normally after combat

### **0.23.1**

**FEATURES**

- characters now have collision

**BUG FIXES**

- fixed AI for wandering traders

### **0.23.0**

This is purely a technical update, and adds no gameplay features. Sorry
about that, but it now paves the way for some fun-filled updates coming
up next. This was a big overhaul, so new bugs may have been
introduced. **FEATURES**

- Total pathfinding overhaul.
- Faster map loading times
- Improved frame rate
- reduced load times when entering buildings

**BUG FIXES**

- import squad to a new game now relocates your squad to the starting
  town.
- you can now set mouse horizontal/vertical speeds, use a negative
  number to invert the mouse control.
- Custom made launcher without any invalid options to choose.

**NEW BUGS**

- There is currently no character collision detection so they all stand
  in the same spot, I will add this back in asap.
- Splinting doesn't always work, I'm going to make it a separate action
  in the next update.

## **0.22**

### **0.22.0**

**FEATURES**

- Foliage system
- Characters bleed 3x faster, but bloodloss clots (slows down) 4x
  faster.
- Character skills now increase more slowly as they get higher

**BUG FIXES**

- If your characters are staying down but are not wounded, they will get
  up if you give them a move order (eg right-click somewhere)
- Fixed bug where splitting an item stack made the value skyrocket
- fixed bug where you couldnt heal neutral NPCs
- fixed backpack inventories being mis-aligned
- fixed carrying bug where you sometimes couldnt put someone down
- fixed visual bugs with ragdolls when carrying them
- fixed bugs with splinting. You can now only splint damage as high as
  40
- fixed the invisible npcs bug

**NEAR FUTURE PLANS**

- bug fixes, and foliage improvements
- optimisations
- sleeping in beds, then building ownership

## **0.21**

### **0.21.6**

- Minor stability fixes

### **0.21.2**

**FEATURES**

- You can now carry wounded people. Select someone healthy, hold down
  the right mouse button on a collapsed character and choose "Pick up".
  To put down again, use the right-click menu again on yourself and
  choose "Put down".
- As well as a medkit, you need a splint kit to make bodyparts (slightly
  more) useable again. Bandages now only cause healing.
- You now need both arms functional to use a heavy weapon.
- You need a one-handed weapon to fight while carrying someone.
- There is more to be done on this, like bed rest and more
  medical/damage stat effects, but for now I think its a good mid-way
  update.

**BUG FIXES**

- You no longer need to install PhysX.
- Fixed characters not getting up when healed
- Lots of little things

**FUTURE**

- I'm going to focus on the foliage system so that I can hire an
  environment artist. Then I will go back to the medical system for some
  more features.

### **0.21.1**

- hopefully fixed the "everything invisible" bug. let me know on the
  forums if its not fixed.
- medics now heal the vital bodyparts first

### **0.21.0**

**FEATURES**

- you can now bring up the right-click menu by clicking on a characters
  portrait.
- characters are now aware of what other characters in the squad are
  doing and are less likely to do things like heal the same target while
  someone else is bleeding to death.
- characters in a squad can communicate. If a character needs to heal,
  he can ask the squad to halt the patrol. If a character is wounded and
  has no medkits he can ask someone else to heal him.
- when a whole squad is defeated, any character that gains consciousness
  will stay down until all enemies are out of range.
- removed a few old items, added new ones. Chain head-wrap, martial
  artists Gi, and tricorner hat.
- Due to unpopularity, the plank has been changed to a lighter, hacker
  class weapon, but its still cool
- when you right-click an enemy it commands your character(s) to attack
  all of them, instead of targeting that single enemy. If you want to
  attack a certain enemy you can choose it from the right-click menu.
  This should stop newbies getting so confused.

**BUGFIXES**

- stopped graphical flickering bugs
- reduced video card requirements to vertex shader 2.0
- some people had a crash when opening shops, this may be fixed now.

## **0.20**

### **0.20 a11**

**FEATURES**

- combat is now more hectic, with less idle characters, however it also
  means that fighting will be harder when outnumbered. I welcome
  feedback on this change.
- added a menu when pressing escape
- 2 main factions now at war, feel free to pick a side and join in. I
  just threw this in temporarily, until factions and alliances get more
  complicated.

**BUG FIXES**

- fixed indoor combat
- fixed loading/saving of faction relations
- fixed duplicating items
- stopped people walking through walls, and climbing up the city walls
  of Capital.
- lots of little things
- police won't attack you for using violence to help them. This may also
  stop the towns errupting into accidental civil wars.

### **0.20 a9**

- Updated the construction set to 0.4. It now tracks which properties
  you have edited, and only those will override the original data. You
  can also now delete associated items.
- fixed lots of little things
- my cough got better

**NOTE:**

- the bug where your squad temporarily disappears if you move too fast
  across the map has not been entirely fixed, but you can now at least
  control your squad during this time and stop them running off to the
  ends of the map. If your squad vanishes, take it out of fast-forward
  mode and wait for the "loading" message to go away, and they will
  reappear

### **0.20 a8**

- That same random crash bug persists. I hunted down the queen bug, and
  gave her a taste of my mighty beard. Try this update, and see if it
  has fixed the crashes

### **0.20 a7**

- Fixed one little bug that was causing all the random crashes
- Fixed bug when importing squad made backpacks break
- Something else I forgot

**FUTURE:**

- Will sort out the construction set next

### **0.20 a6**

- fixed a random crash
- demo mode now allows you to recruit one extra character
- pressing the BLOCKS button toggles defensive combat mode. The
  character will not make attacks, but will have a +20 bonus to his
  melee defense.
- fixed a bug that messed up someones savegame, it loads fine now
- my cough is getting better
- modders, you can toggle the level editor with shift + F12, but you
  will have trouble figuring it out. Hint: you set a buildings faction
  and division by selecting it and then choosing from the menus down the
  left.

**NEAR FUTURE:**

- I need to fix some bugs in the construction set
- I will probably find more crashes to fix.
- focusing on stability and major bugs
- my cough will go away__NOEDITSECTION__

[Category:Kenshi Wiki](Category:Kenshi_Wiki "wikilink")