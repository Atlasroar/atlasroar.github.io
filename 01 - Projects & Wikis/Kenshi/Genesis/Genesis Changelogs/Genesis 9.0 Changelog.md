---
date: 2024-04-18T19:39
tags:
  - Genesis
  - changelog
---
[[Genesis]]
![](https://cdn.gilcdn.com/ContentMediaGenericFiles/19a76af5049af13de03ef2532480c6d5-Preview.webp?w=1440&h=810&Expires=1713501547&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZG4uZ2lsY2RuLmNvbS8qIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzEzNTAxNTQ3fSwiSXBBZGRyZXNzIjp7IkFXUzpTb3VyY2VJcCI6IjI0LjE5OS4xNTIuMjM4In19fV19&Signature=D75IeuXQCMVedfF8AThdDs94pQKNAmkGMXojD3CgcH-tO-nMJW%7EDvpNX8xhBy-xWe47KcvFXadVojfgk5uyVCQkgvEn2zWOz3V8pOJVTFUkGBdiY8cW5g8daP%7EIoueun5tLHv-5kjWifcl7BkPbB-7WaRR0rgNqiJEKxMV1QPIe3wmhFMmx%7EmOTvvdShrR2OVIjLjVx29Qw4J4ZFg7cOq9i8XE80XvVVe37LHVEqmtyv%7ExSGiXEh3vtrTGevbBbhDbJus5p%7E-eVBOwf8inaEHORQAmBeIZIeFMxx0mMFGg2uBWHcl80JBCHvTmfmgcORZv-m58-b3GAfMFULhCUzgA__&Key-Pair-Id=K1FFKFZRWAZSB)

# The Tech Overhaul

--Changes (Chronological Order)--

Some changes may not be fully reflective. with an update this large, stuff is bound to change, so it's only representative as a chronlogical list of what was changed when it was changed.

Going on in the future changes will be properly organized by category and will be edited or added to to clarify changes as they evolve over time

- -adjusted the swamp "vines" again. Reduced them again to a density of 1. this should allow them to sparingly spawn but should improve load times, as well as navmesh.
- -removed the shek ranch on the edge of vain north of admag. caused loading loops of all assets in the area which caused huge loading spikes. It will be moved further west.
- -moved all hive buildings EXCEPT the hive robotics into the hive category.
- -adjusted farming in dreg. there is now a farming rank of 10% green and 10% water. THe area is slightly richer in iron (by 5%). This should allow players to base their now and live naturally without outright being forced to rely on hydroponics. You'll just require MUCH more farms and wells.
- -adjusted and changed all western hiver villages (i think). since all hive villages share the same template this allowed for very easy and different village looks. some are heavily guarded, some are just farmers, others will be a mix of all of the above.
- -all western hive villages can now spawn with mercs "recruit variant",
- -all hive villages will spawn with hive caravans that travel from town to town. this should allow those who live in the area to trade much more easily as well as slightly increase the chance to have hivers show up to your base in the area as well as other towns.
- -hiver villages now have a police station. it's aptly named "justice station".
- -hiver villages are now decently lit (through torches and lanterns)
- -upgraded the "distant" hive villages. the one in sinkuun is much more city like and the one in the great desert is a little larger. Due to their general proximity to other factions you'll find more bar squads, more traders and more roaming squads for them in the areas they are in (spawning from their villages)
- -made a custom "worker" stat package. they'll average 15-20 combat stats but will have 100 in farming and labor this should make them able to produce much more stuff (like they should if they just work their whole damn life). This'll have a couple benefits of them being able to curb players "taking" from farms. Has been added to western hive drones and generic NPC's
- -started changing the adventurers guild rally points. Instead of tiny platforms they'll now be solo shacks. This should completely eliminate the "permanent" spawned campaings from them as well as allowing some other benefits.
- -deleted the (HH) hat variants. Without knowing what they are MEANT to look like i'd rather avoid the obscene texture and mesh tearing that happens when NPC's wear them.
- -updated string. Now only includes the wayfarers bar and various bar residents
- -updated brink town utilities are outside of the city. Plenty of stuff outside the city. though the wells are far away from the city
- -brink is now a sizeable village and not a full city. Though due to it's size it has no houses for sale.
- -touched up black scratch (still waiting on some assets to touch up the great library)
- -moved and remade moon cultist village. Removed the external buildings. Now everyone live in the giant pyramid.
- -added a legal system to the skeletons. They now properly have a legal system which will make them punish thieves
- -changed the iron mine 1/2 to now act like the copper mine does. Given it's primitive tech it will work slower than normally and require more laborers but it works based off stone. So it should be somewhat easier to farm resources in areas with high stone but less resources of other types. (you can now use the stone/copper/iron mines as low tech alternatives to farm from stone the proper resource you may need in an area that is lacking it)
- -removed black beards gully and compressed it into his fort.
- -moved black beards fort. Look to the sea to find it.
- -moved and rebuilt all of tortuga.
- -removed a bunch of the inter factions in tortuga. The NPC's should fight much less.
- -removed all residents and replaced with the generic and squatter lists
- -figured out and fixed the loading issue surrounding the city of todai dera.
- -added a new more generous resource spawn type for farming based off the mountains in stobes garden. Playing mountain top monks should be friendlier.
- -changed the interior of the smugglers bar
- -added more bar squads to the smugglers bar
- -adjusted the pathing around the smugglers bar to fix an issue seen in @KevWasHere video series
- -added a town generator to the last waystation as described by @pattmaster
- -locked squad sizes of citizens (They won't randomize or grow through setting changes)
- -randomized the sohei wandering squad more. Renamed them to samurai as well. This should cause a "trickled" lore effect. Samurais will have various weapons and gear exclusive to them. This should also allow a nice blend of armors in the area AND as they are traveling around without them being bright red/blue beacons.
- -removed small barrels
- -removed booze barrels
- -removed booze barrel
- -removed "five" booze barrels
- -removed armour storage (small metal chest)
- -removed food stores (greyish barrel)
- -removed large basket
- -removed small crate (small box)
- -deleted booze barrel table
- -updated the grey desert waystation. It's now using the waystation four name. it's also been moved slightly south west. it's been completely overhauled.
- -updated old village
- -renamed south stone camp to "Grind stone"
- -upgraded slave farm N
- -adjusted sheer cliff to be more ruin like
- -renamed "the groggery" to Semolina.
- Semolina is the coarse, purified wheat middlings (intermediate milling stage) of durum wheat mainly used in making couscous, pasta, and sweet puddings.
- -deleted crab villages
- -deleted shipwright village (it's been merged into tortuga)
- -rebuilt grogery
- -hated the new grand bazaar so much i yeeted it and the new manhunter base only to move the bazaar into the wetlands (the sole trade center there, north of clownsteady) and reverted the manhunters base to it's original shape and size just with more buildings
- -removed and replaced the hasher faction
- -removed the clowns faction
- -added more vendors of various factions to the bazaar
- -renamed the grand bazaar to "Carsi". Carsi in turkish means "market". more or less.
- -overhauled and rebuilt catun from scratch to fix dozens of issues. Lore related and gameplay related.
- -remerged the updated CM-Roads & CM-roads-ADDON pack to include and optimize the new stuff added and updated.
- -updated the icons and stuff for fogmen to use the new version from fog hunt.
- -replaced the pathing for item dependencies to reference the already included work from camels mods.
- -noticed an error with severed hive limbs. Renamed and repathed all of them
- -made a polish pass on swordran with some of the new assets. replaced the old bar with the new bar1 setup.
- -pulled a bunch of the city of swordran (resident hourses) inside it's walls. this should make it less likely citizens will pull grievewraiths into the city.
- -rebuilt a bunch of the navmesh and tweaked the road and pathing in and around the city, the new road assets allow straight vertical drops through built in stairs which allows less models to be rendered. TLDR: no more long ramps to gain elevation.
- -Reduced the amount of citizens and houses in the city of swordran. Much more condensed and lighter on performance.
- -added a new copy of the low arid resources. bumped the farming height by 200. (this should allow basically everywhere around the main castle to be farmable)
- -cleaned up a leftover town from the great shun purge
- -tweaked 42 sections of the shun road network (a lot of it runs through water alonside the banks of the rivers, i just pulled the road out of the river areas)
- -added two new forks in the shun road networks. should cull travel time across the region when traveling long distance.
- -removed the roaming squads from swordran and added them as bar squads. this ensures they will spawn and will patrol
- -adjusted the gate guard squad. added a squad 2, added rangers to both squads, added more relevant medical items to all tertius guards
- -adjusted the patrol squads size
- -new holy nation start was added and expanded upon with the HN redux merge.
- -renamed holy hessian uniform (from HN redux) to Holy Hessian Pants - Padded
- -renamed Stout Hessian pants (vanilla) To Holy Hessian Pants
- -changed "sacred rags" to > Holy Hessian Skirt
- -edited all cannibals to now carry less armor (% wise) certain types like tenderizers/leaders etc will still wear armor in full force. this should slightly tweak cannibals back to relying on numbers and their many new various weapon setups.
- -edited many cannibals of "lower" orders to carry the new weapons.
- -many cannibals have been adjusted to be more or less prevalent in certain areas.
- -added new cannibal spawns to create infighting in the area
- -culled the new "cannibal" squads to be smaller to ensure a lively north but not massive loot everywhere.
- -removed cogs crow nest and merged it into gearcove
- -rebuilt gearcove. it's more compact....but it's also, so damn cool. had a lot of fun with this hidden ruin design.
- cleaned up remaining locations of dyers guild towns. they'll be added back in on player request to existing towns.
- -made most of the volcanos around spring completely accesible. they're a little small but can provide some nice looking bases should players wish. (edit: Look for bridges/ramps going up the volcanos)
- -upped the skeleton bandits limb qualities. i noticed that with the addition of the skeleton limbs they tended to be much much weaker than they were meant to be. I also balanced their stats to be flat. 45 > combat instead of 42.
- -added more limb variations to skeleton bandits. some at lower quality and some at higher. this should provide a decent fight every time as the limbs mix to create different stats
- -fixed the floating sign in flats lagoon under the platform as pointed out by @Mobile Kek Suit
- -rebuilt the fishing platforms from scratch. should now much better reflect the people living there. Made a duplicate generic fisherman (from the deadcat people). They'll now roam around or spawn at fishing platforms whereever they may be. they now appropriately wear the new fishing gear by cat
- -after a day or so of crashing fixed an error with the pathing for the new fishermans gear. Changed the items from "shirts" to "body" armor. Removed the shirt texture layer to prevent a black body.
- -fixed the bob haircut. A texture channel was wrong. which caused flickering on a bunch of other hairs when GPU was even slightly strained. Mesh and texture now show correctly. mind you. this wont solve the texture flickering. Unsure at this time what causes it but this change seems to lessen the problem significantly
- -After 4 days of consistent crashing, having to force quit, and trying to manually rebuild the entirety of the navmesh in and around mongrel. I said F this. Rebuilt the entirety of mongrel. Which allowed for a slight style change in walls and utilities. The town is a sizeable bit smaller too. Much closer to it's vanilla counterpart with a little more love in the design than before. While simpler i stuck to the last versions design choices.
- -The road network in and around mongrel was overhauled. There's less branching paths to nowhere and most of the road network loops back into itself. This should make auto pathing a little more consistent.
- -caught a texture crash as a result of the texture pathing of the simpler mills. fixed now.
- -Made a secondary pass around the fog islands. Upped the nest spawns from 0 to 3. This should reintroduce a number of fogmen spawns and randomize them a little bit
- -upped the number of homeless squads from 3 - 10, reduce the scavenger homeless spawn to a weight of 1, upped the spawn of praetorian squads to a weight of 10,
- -adjusted the range of mongrel as a town.
- -removed two static deathyards right next to mongrel. this caused a "dead" loop with other towns in the area in which roaming and "bar" squads would no longer spawn.
- -upped the roaming squad and bar squad counts for the death yards. decreased them for the nest spawns.
- -increased the weight of the slough hyenas spawning in the area.
- -added some debris to the static deathyards. should be plenty of bones and bit laying around.
- -dropped the max altitude by 200 for boneyard spawns. increased the max slope, increased the building density. With these adjustments it's probably around...20%-ish more common now to find them. (though with the max slop increase they can be harder to reach now)
- -for those aware of it. changed the input/output and operators of the ancient forge. it is no longer automated. it also needs 5 people to craft anything. needs tech 6. it needs 50 old cpus per "item". Hunger rate is set to 3.5. Will probably be ramped up even more in the future.
- -Added loot randomization to fogmen nests and the static deathyards.
- -changed the nest spawned deathyards to have much more condensed "buildings". they'll spawn less in a wide range and closer to the center of the nest.
- -Moved Stone camp south. Thus creating a logical trail of "slaves" and caravans from south to north. stone camp is now situated directly south of stoat. who's main focus as redesigned is a "slavers trading grounds"
- -made some minor tweaks to the cactus den. tightened up the "town" so it now has an even smaller range and impact. removed some of the lighting in the town to make it much less obvious from a distance.
- -tweaked fort mirage. reduced the radius, removed the foliage range. moved the city up on top of the hill, added some more power, upped the squad count, removed the randomization with player settings,
- -renamed stone camp to wrought. Wrought is now a heavy industry iron mine for the UC
- -moved port south to the hook. it's now situated in between drifters last and clownsteady to fill in the crucial gap of "slavers" in the area.
- -adjusted the roads around port south to now travel across a bridge
- -pulled all of the road networks in the hook out of water unless there is very little of it at depth. this should allow npcs and players to travel easier through and across the map in the area.
- -deleted mechamoor
- -deleted the bonepile
- -deleted gale
- -cleared some of the bottom floor of the "trashed" outpost interior. Purged all guard nodes except from the bottom floor. Great white gorillo should now only roam a very tiny area on the bottom floor. This will prevent him from despawning, or getting stuck. He will still however try to chase you throughout the building. As such i've also cleared much of the interior or pushed all the trashed items into larger piles.
- -cleaned up all of mourn. removed some exterior items to reduce loading, removed and condensed some housing. replaced some squads and fleshed out many others. there should now be less infighting however many NPC's have "rebel/outlaw/drifter" dialouge. so they'll complain and make snarky comments and threaten each other.
- -adjusted the guards for the gates and replaced the ai with the new genesis package. this should somewhat save mourn from issues as the ai will now purge bodies and heal each other and the city
- -deleted lycus
- -simplified how the bonefield bandits will work. Players will start off either allying or fighting the bonepack. When the leader is dead the marrows will move in, when the marrows leader is dead the gutter gang will move in. Once all bosses are dead, the factions will dissapear and the outpost will turn into a smugglers den. Each leader killed will wipe out their faction. Each leader has unique rewards. The factions will be common as homeless/nest squads until their leader and base is wiped out.
- -cage has been overhauled to be much much simpler and cleaner.
- -polished up the bonepacks clothing, weapon and dog selection.
- -cleaned up the gutter gang, and the marrows bandit squads.
- -adjusted the worldstates for CAGE to now stack. One must happen before the other to ensure no bugs.
- -adjusted the stats and weapons of all bandit groups. they're now much weaker. but still decently balanced around being "mid game" bosses.
- -removed most crossbows and turrets from cage squads.
- -removed beak things from gutter gang squads, they now only have a town spawn (for dead bodies)
- -adjusted the relations between gutters and gutter gang to 100 for both. this should avoid them killing each other.
- -overhauled lure, gale was semi compressed into it. (one shelter). The town now has a MUCH smaller footprint. The questline will be rewritten to accommodate the sacred band quest. this will give life to part of the south eastern world lore. it'll also help polish up some Holy nation world lore through the interactions with the sacred band and why they are leading the fish islanders
- -activated distant mesh for all towns.
- -removed ronin weapons BP from all squads, added back to seth
- -cleaned out vendors who sold ronin weapons, as previously discussed on discord they're now sold at market vendors
- -Deleted the dialogue causing the "..." elipsis problem
- -Removed the floating light from skinners roam as reported by @Master-chan
- -made a pass on the ark reaver HQ it should have a proper generated navmesh now
- -changed scraphouse respawn to 1 week
- -deleted hope (haha no hope, go fuck yourself)
- -fixed the tree in urusai as pointed out by @Mak
- -fixed two scraphouse placement bugs where furniture was inside of other furniture as pointed out by @Master-chan
- -changed dack and quin to unique as pointed out by @shade0180
- -deleted the wool cap as reported by @Lenin's Cat to avoid the graphical errors it causes
- -cut the verglas hound scale down from 1.2 to 1 even
- -fixed cannibal lord weapon manufacturer levels
- -removed the item called "tech" as reported by @HorHorHor
- -fixed brood town area
- -deleted the cannibal minion
- -renamed some cannibals from more serious names to more inline with what they appear to be in lore, new spiky and meat beater cannibals
- -started working on okrans shield, overhauled how all squads work so that all HN citizens are easy to identify. Each church now has it's own guards and staff with unique armor sets. The military now has exact and cleaned up roles.
- -overhauled bad teeth, refreshed the city design to be cleaner and replaced all the unique squads with generic squads
- -overhauled stack, refreshed the city design
- -added a new holy church sign mesh for the......churches from @Boron
- -replaced genesis tengus palace with the vanilla tengus palace, thus fixing the crossbow level bug @Master-chan noticed
- -fixed the minor housing issues in squin
- -finished up the adjustments on squin, squin now uses it's vertical height a lot more for the town to flesh it out and fill it up
- -overhauled vainspass and moved it father into vain. Reworked the entire city to be much cleaner.
- -moved stenn desert waystation farther south
- -moved and rebuilt berserker village south
- -moved and rebuilt the great fortress east of its location
- -moved and rebuilt last stand west of its location.
- -moved and rebuilt admag west of its original location
- -added back in and cleaned up the shek ranches
- -added all animations to xavage
- -added cattrinas CBT hair fix mod.
- -added restful base props (the rest of the mod) by snugsnug
- -added buildings mod by snugsnug
- -added stowage packs mod (by snug - unreleased public)
- -per request of @Para added and increased the sniper spawn rates in sniper valley. Now holding a 70% weight to spawn two per zone is roughly a 30% chance. and roughly 50% chance to spawn one alone. added skeleton limbs to them as well thus further randomizing their skill levels.
- -reorganized the categories and sub categories of a couple hundred items again. condensed even further into cleaner categories
- -merged workbench variations. Mod allows players to upgrade many storage options into 2nd and 3rd tiers. It also randomizes its look for many benches while overhauling many generic storage objects so that players can visually identify whats inside common vanilla barrels. Like greenfruit sitting on top of a greenfruit storage barrel. Iron ore being in iron ore storage.
- -added snugsnug weapon mod. it added in some holy nation weapons and civilian weapons left out from earlier phases of genesis.
- -reduced the nest spawns in the hook
- -adjusted the homeless spawns to be much smaller in grouping.
- -changed what the tertius roaming patrols spawn with. they no longer spawn with skeleton grade weapons, they now spawn with catun level.
- -patched the dust king tower worldstates to properly stack instead of grouping together. Mercs should no longer spawn randomly.
- -Rebuilt crab town to be much more compact
- -merged radiant animal subspecies
- -striped bulls renamed to banded bulls, now spawn in hook, spider plains, vain. Rare chance to spawn in shek ranches
- -changed shek ranches to now use domesticat bulls
- -new boneyard dogs only spawn at nomad camps and merchants (with their scarfs)
- -new green skimmer reduced in size to about the size of a small bug. they'll now spawn in squads of 5-10 in wooded areas. they're not dangerous....kind of just dont get swarmed
- -replaced most of the blood spiders in the swamps with the new green spider variants... Good luck 🙂
- -iridescent beak things added to vain, replaces all vain squads. Now replaces the squads in leviathan coast too.
- -new land bats will replace all landbat variants in darker areas. The black landbats will be the majority with the white landbats being a rare albino variant now.
- -dark garru, now spawn in shun, crater, grid area, leviathan coast.
- -deleted longfellow, his lore will be implemented in headshots dialogue to flesh him out more
- -purged all of the hidden isles
- -moved avalon....north east and rebuilt it to be much tighter and lighter
- -moved avalon ruins south east into the hidden isles
- -merged economy skeletons mod by subarashi one. they'll be very rare, long lost forgotten robots.
- -merged samurai armor expanded by subarashi one
- -merged cattrinas new faction furniture mod
- -removed the "is recruitable" condiiton from ranes dialogue to fix the bug of not being able to talk to her
- -fixed limb vendors not recognizing you steal from them.
- -tweaked ashi to be more uniform with the area. it now will host old empire supply posts as a base template complete with gear to loot sharing with empire supply posts.
- -changed ashi from an outpost into a ruin (town type) to reflect it's status
- -rebuilt leviathan from scratch. now an old outpost hidden away in the midst of ruins players will find all sorts of oddities hidden in the town.
- -deleted tin town.
- -rebuilt sanctuary from scratch and buffed it a bit
- -added in building replacements for UC, they now can spawn sohei houses (storm house & small shack) in towns. This provides a mix of buildings as would be indicated by their standing in the world.
- -added building replacements for shek. They now replace storm houses. Giving shek a rustic and beaten town life.
- -changed some world features around squin. It now looks like its spawned in a canyon overhung by rocks. (Tldr: a cave).
- -overhauled western hive capital with new hive assets.
- -compressed hundreds of new items into relevant subcategories. (May need community feedback for further tweaking. May make a color variatons main category for eases of use)
- -added new building categories. UC, HN, SHEK. will now hold relevant furniture and buildings assigned to them for cleaner access. This follows suit with buildings - hive and buildings - sohei.
- -noticed on stream that the storehouse was pulling to much resource time. Rebuilt its interior with the new assets and cleaned up its interior
- -sanctuary now provides mercs and traders for players in the area. This follows suit with adding more random bar squads to populate the world while traveling.
- -adjusted naming conventions of categories. Following suit with other categories all furniture is now in town - interior, all roads and such are now in town - exterior. Walls are now under town - walls. Thus grouping major categories into a hanful of main titles. Buildings, town (decorations & additions like roads and bridges, furniture), crafting, farming, camping, & tech. Categories and building organization will come with a full written guide players can use.
- -deleted the small backpack
- -merged backpacks expanded
- -added the new shield roll to UC samurais

-changed materials stack & size

Iron plates - 3x3 / stack 10

copper alloy 3x3 / stack 10

building materials 3x6 / stack 5

stone 3x3 / stack 5

copper 3x3 / stack 5

iron 3x3 / stack 5

- -Deleted the large backpack
- -deleted the wooden backpack
- -deleted empty ruins
- -deleted empty ruin
- -Renamed ruined farm (HN) to Abandoned Farm. Players can find Farming/food related materials here
- -Renamed Ruine Mines (HN) to Abandoned Village. Players can find building related materials here.
- -Renamed Ruined Waystation to Abandoned Waystation. Players can find tech related materials here
- -deleted leaning tower ruins across the map.
- -Created a new faction. "Ruins". Unless lore related most ruins will fall under this new "not real" faction. Allowing for simpler edits when it comes to the ruins and allowing better blanket changes to be adjusted across ruins.
- -all ruins will now be unified under the unexplored name of "Ruins". This should provide a sense of mystery and give more reason to actually explore each ruin.

-Ruins will now fall into one of 4 categories.

--Ruins. In general these wont be very desirable except in the early game. Players will generally be able to tell what these are by the fact they hold collapsed ruins and the loot is strewn about.

--Lost. These structures have been lost to time and dont appear on any maps until they are found. Players will find a large range of items and enemies in these ruins. Rusting but still standing these hold a larger amount of desriable wealth and items.

--Ancient. These ruins are challenges. Hosting harder enemies guarding more desirable wealth and items. Maps for these come with warnings and are expensive.

--Vaults. These host unique items, bosses and sometimes recruits. These will eventually have their own tie together lore. Their own advancements through the ranks of the tech hunters and machinists.

- -deleted restful peak
- -deleted northfall mine
- -deleted black cinder mine
- -deleted alden
- -deleted ruvanil
- -deleted cragrock mine
- -deleted crimson stronghold
- -deleted tintown
- -replaced the town "gate" in the grid named post ancient workshop with the correct town name and type : Post ancient workshop > Gate
- -moved the winged beak ogre thing nest to spawn as a nest in the shrieking forest
- -replaced puple sands enviormental resource data. it now acts like a desert except it is worse for farming overall.
- -adjusted and scaled down the races the scavengers can be. They'll now prioritize the human like (Sentient) Species. Greenlander, scorch, hiver, shek. etc
- -fixed the race issue with howlers. now single gender they will no longer pop up showing they are missing races
- -deleted the blackshifters vault
- -deleted the library outpost ruin
- -deleted the infested village
- -removed the gusoku armors from vendors they were accidentally applied to.
- -merged cats clothing overhaul
- -Removed some items in favor of the more flavorful ones ("geared items").
- -adjusted the HN citizens to have more clothes from the above overhaul.
- -Adjusted the bags on HN citizens. They'll now exclusively have the new bags from the overhaul.
- -removed over 100 squads across the game that were no longer used and were being replaced with more default squads per faction
- -Merged tengu mod by catt:
- -added a new vendor to tengus palace. Tengus old robes and mask now rest there. (it should theoretically spawn multiple, will also include blueprints for those items).
- -tengus new clothes and weapon are 100% unique. They will not be craftable. He will also still carry his crossbow.
- -merged antiquity sheks (Partially):
- -Esata and Seto now share a unique breastplate. Flying bull has a unique breastplate.
- -Esata now has a unique shirt and head piece. Seto now has a unique headpiece.
- -Bayan now has new gear.
- -all gear non unique gear will be added to vendors and BP's for the shek.
- -Removed some genesis shek armors (snugsnug created). Cleaned up the spawnable armors for sheks
- -replaced shek guards (shek warriors) with hundred guardians in most stores
- -place the warriors on gate guard duty as squad 2.
- -adjusted the ai for shek gate guards. Now uses the new heal/disposal setup
- -adjusted armor spawns across the shek squads.
- -deleted hounds hash factory. had taken to much space for to little purpose
- -merged macrotaz mud and clay
- -overhauled mud town. cleaned up more of the swamp.
- -added multiple material buildings to wood skimmer nests. making them have multiple resources to look out for. Reeds however will only be available in the swamp and the southern wetlands.
- -mud town squads belong to the "swampers". they have unique loot and gear and are a tribal people. Eventually a one part quest world state will be added that adds a unique recruit. after recruiting the recruit the town will fall to a mysterious illness. D:
- -overhauled Rot. Now uses a base template of lower tech. Still controlled by the hounds in many ways but now more a generic swamper town. swamper members there use leaves as armor (from cats civilian overhaul)
- -overhauled the swamper shop
- -moved the cannibal and other nest item (tents) into A new building group _nests thus cleaning up the camping area for players.
- -Removed all tents intended for nest use from player research
- -after recent merges some tent items were duplicated. Deleted all duplicate entries from tents.
- -removed the shelter bed (metal piece laid over a camp bed) from player buildable structures. moved into nest items.
- -deleted quarry a/b variants 2-4
- -deleted the quarry tent as it did not work
- -deleted the individual book keeping items like "Storage: Engineering Research" etc. With the new bookshelves they are already properly setup to receive all unique books AND research artifacts excluding AI cores.
- -renamed Storage category to "Town - Storage" Thus pairing it with interiors and exterior furniture for easy swapping back and forth.
- -Compressed the "buildings ancient" category into the "BUILDINGS - OUTPOST" category. I.e. Outpost size buildings are large or massive building types large enough to be an outpost on their own.
- -Moved the pyramids to the buildings - outpost category.
- -moved the ashdomes to buildings outpost category
- -moved the big shack (deadcat/cannibal asset) to the buildings rebel category
- -renamed buildings metal category to buildings rebel
- -compressed all citadel, lab and outpost ramps into one sub category. (should automatically snap to the right kind per building)-removed limm from it's original spot, moved it inside shark
- -renamed limm to twinblade's outcrop, a tiny POI inside shark now hosts all your illicit organic and cheap robotics needs
- -merged CBT leisure Furniture
- -moved leisure objects to Town interiors - Animated gaming /tables/stools sub category
- -modified leisure objects to also be placeable outside
- -overhauled shark from scratch adding in 100 new assets
- -added coexistence with some swamp factions like swampers, hounds and blackshifters
- -hemp is stackable to 5 now
- -adjusted the new backpacks to all appear in their respective bench (backpack bench crafts).
- -moved belt specific items for the player to the backpack bench as well.
- -deleted the dilipidated ironside (carried the bag variant)
- -deleted old ironsides i3 copper restored rig
- -deleted dilipidated v2 frame
- -deleted v2 frame bags restored and rusted
- -deleted driven h2 ironside
- -deleted functional ironside types. their frames will be lootable and craftable through vaults and their bosses.
- -added enforcers to the error police Squads.
- -added zagan back in. Zagan now hangs out around squin. You need 100k to unlock his recruitment dialogue (on you) and then you need 80+ relations with the SHEK to recruit him. Otherwise you're just an arrogant ass who thought you could challenge him.
- -moved vault 1 to iron trail
- -edited a new interior for vault 1
- -made a quick and dirty balance pass on loot spawns
- -added deimos to vault 1
- -moved vault two to sinkuun. Replacing "new deadcat" with the vault.
- -added kenji as a bar squad spawn in Vault 2.
- -added more residents to the vault 2 resident list to reward players who seek out this vault.
- -fixed a western hiver raid bug that @OmegaXII and @KySoto pointed out
- -fixed a southern hiver raid bug in vains pass that was noticed while testing the western hiver raid bug.
- -Reduced the chance of crossbows for slaver caravan guards as reported by @KySoto this should make crossbows a bit rarer for them to carry but still possible. added the tooth pick to their repitoire and removed the three shot ranger. They still have the ranger.
- -fixed a flipped gate in mourn.
- -fixed a interior issue with no lights in the hive justice spire.
- -fixed the shinobi smuggler dialogue as pointed out by @Cirdanoth . the rank is now properly detected.
- -fixed the weapons in the western hive exiles start. fixed the squad spawns as well. Modified the start to now put you at -10 with the western hive.
- -adjusted the western hiver caravan material trader to now have 15k cats.
- -updated the library ruin interior to use the new bookshelves.
- -removed the physical cats spawn from the lost armoury ruins
- -deleted and merged the ruin types of the armourys. The only one now in game is "Lost Armoury"\
- -adjusted the weights of crab limbs and their quality on crab raiders as noticed by @Keywee They should spawn rarer on most of the crab raiders excluding the crab raider captains. The quality chance has been lowered across the board. Also added custom stats to the crab raiders and captains. Making them tankier and slower. Adjusted the weapon spawns to now almost fully use the crab maul and the crab vairant of the man slayer.
- -overhauled the grid. added more gates and added old machine spawns to them.
- -added 5 post ancient workshops which now spawn a wealth of engineering research
- -added skeleton legion patrols to the grid.
- -added enforcers to the gates
- -changed the spire name from "the spire" to "Spire"
- -changed the town of spire to now originally be held by old machines
- -added marbas the insane to the spire, he will play a key role in the future for the machinists to take over the town
- -added more homeless spawned ironsides to the grid. Recruitable and not.
- -fixed the traders guild not having any cats to trade with or buy player items with.
- -compressed the ancient tech lab into the "lab". will now serve as a template for ruins
- -cleaned up some left over towns (again) from cheaters run.
- -RE-rebalanced All Backpacks. Smaller bags now provide benefits, or no negatives (gear dependent), Medium Size Bags have slight negatives, large backpacks even more so and "trader" bags or otherwise Massive bags generally have huge penalties that make them a high price for combat.
- -Animal bags now have obvious bonuses. Smaller animals will get 100% weight reduction but they also can barely hold enough food. Mid animals (goats/anetelopes) are fast but only get a 90% reduction in weight. Bulls/Garru/Skimmers all get the same exact bag bonuses, so you can pick your favorite pack animal. Cage Beasts Now get 100% reduction and have a larger inventory and stack 20x20.
- -The changes to all bags will push players out of their comfort zone, paired with the eventual Speed changes in the Genesis mod for all races this should push players to use "trade" animals more and "trade" bags less unless they can overcompensate for the detriments of the new stats.
- -Thanks to @DreXav for the bug reports on the bags beta
- -Thanks to @Ranger|.\\ for the updated info on the bags.

BAGS: https://www.guilded.gg/Genesis/groups/dQGnZ5P3/channels/3334141c-c6a2-4eb1-85af-d163c44a6010/docs/374244

Doc

![Atlas's avatar](https://cdn.gilcdn.com/UserAvatar/354bfb05f3e6015b68da7fc9eb9052d6-Small.webp?w=80&h=80&Expires=1713501547&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZG4uZ2lsY2RuLmNvbS8qIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzEzNTAxNTQ3fSwiSXBBZGRyZXNzIjp7IkFXUzpTb3VyY2VJcCI6IjI0LjE5OS4xNTIuMjM4In19fV19&Signature=D75IeuXQCMVedfF8AThdDs94pQKNAmkGMXojD3CgcH-tO-nMJW%7EDvpNX8xhBy-xWe47KcvFXadVojfgk5uyVCQkgvEn2zWOz3V8pOJVTFUkGBdiY8cW5g8daP%7EIoueun5tLHv-5kjWifcl7BkPbB-7WaRR0rgNqiJEKxMV1QPIe3wmhFMmx%7EmOTvvdShrR2OVIjLjVx29Qw4J4ZFg7cOq9i8XE80XvVVe37LHVEqmtyv%7ExSGiXEh3vtrTGevbBbhDbJus5p%7E-eVBOwf8inaEHORQAmBeIZIeFMxx0mMFGg2uBWHcl80JBCHvTmfmgcORZv-m58-b3GAfMFULhCUzgA__&Key-Pair-Id=K1FFKFZRWAZSB)

Bags

C- CRAFT

NC - NO CRAFT

B - Buyable

...

![](https://cdn.gilcdn.com/TeamAvatar/5312df1b7b07e9abc6781e5f6e3817be-Large.png?w=450&h=450&Expires=1713501547&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZG4uZ2lsY2RuLmNvbS8qIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzEzNTAxNTQ3fSwiSXBBZGRyZXNzIjp7IkFXUzpTb3VyY2VJcCI6IjI0LjE5OS4xNTIuMjM4In19fV19&Signature=D75IeuXQCMVedfF8AThdDs94pQKNAmkGMXojD3CgcH-tO-nMJW%7EDvpNX8xhBy-xWe47KcvFXadVojfgk5uyVCQkgvEn2zWOz3V8pOJVTFUkGBdiY8cW5g8daP%7EIoueun5tLHv-5kjWifcl7BkPbB-7WaRR0rgNqiJEKxMV1QPIe3wmhFMmx%7EmOTvvdShrR2OVIjLjVx29Qw4J4ZFg7cOq9i8XE80XvVVe37LHVEqmtyv%7ExSGiXEh3vtrTGevbBbhDbJus5p%7E-eVBOwf8inaEHORQAmBeIZIeFMxx0mMFGg2uBWHcl80JBCHvTmfmgcORZv-m58-b3GAfMFULhCUzgA__&Key-Pair-Id=K1FFKFZRWAZSB)

Genesis • Posted in #Genesis FAQ & Changelogs

![Kenshi group avatar](https://cdn.gilcdn.com/GroupAvatar/6a88e1ab142e9e47840ef37d8a260c79-Small.png?w=126&h=126&Expires=1713501547&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZG4uZ2lsY2RuLmNvbS8qIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzEzNTAxNTQ3fSwiSXBBZGRyZXNzIjp7IkFXUzpTb3VyY2VJcCI6IjI0LjE5OS4xNTIuMjM4In19fV19&Signature=D75IeuXQCMVedfF8AThdDs94pQKNAmkGMXojD3CgcH-tO-nMJW%7EDvpNX8xhBy-xWe47KcvFXadVojfgk5uyVCQkgvEn2zWOz3V8pOJVTFUkGBdiY8cW5g8daP%7EIoueun5tLHv-5kjWifcl7BkPbB-7WaRR0rgNqiJEKxMV1QPIe3wmhFMmx%7EmOTvvdShrR2OVIjLjVx29Qw4J4ZFg7cOq9i8XE80XvVVe37LHVEqmtyv%7ExSGiXEh3vtrTGevbBbhDbJus5p%7E-eVBOwf8inaEHORQAmBeIZIeFMxx0mMFGg2uBWHcl80JBCHvTmfmgcORZv-m58-b3GAfMFULhCUzgA__&Key-Pair-Id=K1FFKFZRWAZSB)

- -fixed the black texture overlay with the topboard wood as reported by @Bugivugic and @Kifyi
- -fixed the sex issue as pointed out by @Lam with lady aguri, shes now set as 100% female
- -fixed meat lord stats as reported by @looksharpbesharp
- -added a named variable to the citizens from cats overhaul as reported by @Kifyi
- -merged randiant primordial hivers by Shiroho:
- -added the new races to mud town due to their tribal nature. Added some new hiver setups using the black carapace set. this will fall into lore related to the southern and western hivers.
- -mud town is now slightly more defended with new guard setups.
- -moved ark a touch south to avoid navmesh issues from where it currently is. It's not situated in one chunk instead of 4.
- -filled out a southern hive village that had no buildings as reported by @Kifyi
- -deleted bone dog alphas
- -added hard capped stats around 25 to all non alpha dogs
- -removed alphas from pack squad variants. Making alphas only native to most den types for specific dogs
- -fixed the upgrade path for the defense dummy as pointed out by @Tenoz
- -fixed the upgrade path for friendly fire training
- -adjusted the wood skimmer to carry less loot
- -adjusted the wood spider to carry less loot
- -removed the worldstate from nomar as pointed out by @dreadarm it's bugged and makes the town spawn as shek
- -changed vains pass to western hive, addded in new buildings to reflect that.
- -fixed the worldstates on the hive dispora bandits as reported by @Ranger|.\\
- -moved one of the dreg gatherer villages down into southern dreg
- -combined one dreg gatherer village into the settled nomad village.
- -expanded the settled nomad village to include more funtionality
- -tweaked cannibals again to spawn with even less of a chance at armor.
- -replaced old village in cannibal plains with anbandoned village type ruin
- -added another abandoned village type ruin to the cannibal plains coast.
- -added new default ruined building spawns to all cannibal towns in darkfinger instead of populating ruins
- -added a abandoned farm generic ruin to sinkuun
- -replaced some spawned building types for the towns in bast with ruined nest versions. Meaning all buildings now spawn a small amount of loot
- -added an abandoned farm to the great desert in the north western area to flesh out the desert a bit more
- -added a lost library to berserker country
- -added two labs, one library and one abandoned waystation to the floodlands, added a lab ruin and a library ruin to the floodlands as well
- -added an abandoned farm to the hidden forest
- -added an abandoned waystation to skimsands
- -added an abandoned farm to heng
- -removed regret
- -added a lab ruin in place of regret
- -added a deadland workshop to iron valley
- -added two ruined holy outposts to HN territory. they'll play a part in the HN world states at a later date
- -rebuilt ironhaven, pulled it closer to the borderzone, added back in the limb vendors
- -added a abandoned village and abandoned farm to storm gap coast
- -added ruined waystation loot to dust king tower, fixed the navmesh issues, lowered the assets spawned in
- -tweaked the interiors and interior spawns of the ruins of venge.
- -add two destroyed labs to venge.
- -tweaked the inventory of ark to now spawn with high tech loot
- -added the ancient lab and ruined farm back to the burning forest.
- -added two armouries and one library to stobes gamble
- -added a lost library in the crags
- -changed the price of ancient military documents to 10k up from 1k
- -adjusted the spawns across the game to make them incredibly rare except in lost libraries.
- -changed the vendor list of the iron hq. it now spawns with lab loot.
- -deleted skimmer nymphs
- -changed skimmers to spawn much MUCH smaller as babies.
- -updated the base bolt box to be 6 wide to cover the issue of harpoon bundles not fitting as reported by @Terak
- -every bolt box and subsequent storage type will be additive of the first base model's stats. I.e. bolt box one is 25 stack multiplier/10 height/6 width, second level is 50 stack/20 height/12 width, third level is 75 stack/30 height/18 width
- -deleted twinblades lockup
- -added the lost lab outpost back in the swamps
- -moved the infested lab more north wards.
- -merged mini fishmen
- -finished the addition of the southern ruin sets first pass
- -deleted dead hive queen.
- -deleted cyborg dead hive worker
- -deleted cyborg hive prince
- -deleted the cyborg south hive drone
- -deleted cyborg south hive soldier
- -deleted cyborg west drone
- -removed all faces plus faces from all races as playable. Theyre still spawnable throughout the world and will be reduced down to specific factions over time as will hair but now they no longer clog up the player menu

----a secondary unlock mod will be made and included in the nexus version to unlock everything

-reduced the amount of races playable down to mk1 skeletons and separated hive races down again.

- -fixed an issue with upgrading gate 4 to gate 5's as pointed out by @Tenoz
- -merged 2pn8's faction shields expanded. samurai, shek and thieves guild now spawn with shirt variants that are wearable by npc's
- -edited legendary quest owner kratch to now have a secondary building in tengus palace. he will wait there (for now will be a 24h shop), other faction legendaries will follow suit with new buildings and ai when the towns they spawn in are done.

https://www.guilded.gg/Genesis/groups/dQGnZ5P3/channels/3334141c-c6a2-4eb1-85af-d163c44a6010/docs/380450

Doc

![Atlas's avatar](https://cdn.gilcdn.com/UserAvatar/354bfb05f3e6015b68da7fc9eb9052d6-Small.webp?w=80&h=80&Expires=1713501547&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZG4uZ2lsY2RuLmNvbS8qIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzEzNTAxNTQ3fSwiSXBBZGRyZXNzIjp7IkFXUzpTb3VyY2VJcCI6IjI0LjE5OS4xNTIuMjM4In19fV19&Signature=D75IeuXQCMVedfF8AThdDs94pQKNAmkGMXojD3CgcH-tO-nMJW%7EDvpNX8xhBy-xWe47KcvFXadVojfgk5uyVCQkgvEn2zWOz3V8pOJVTFUkGBdiY8cW5g8daP%7EIoueun5tLHv-5kjWifcl7BkPbB-7WaRR0rgNqiJEKxMV1QPIe3wmhFMmx%7EmOTvvdShrR2OVIjLjVx29Qw4J4ZFg7cOq9i8XE80XvVVe37LHVEqmtyv%7ExSGiXEh3vtrTGevbBbhDbJus5p%7E-eVBOwf8inaEHORQAmBeIZIeFMxx0mMFGg2uBWHcl80JBCHvTmfmgcORZv-m58-b3GAfMFULhCUzgA__&Key-Pair-Id=K1FFKFZRWAZSB)

Crossbow Changes

--Crossbows should follow this theme:

-Power : Old World Mk1/Mk2/Harpoon

-Accuracy : Areblast/Eagles Cross/jezzazil Bow

...

![](https://cdn.gilcdn.com/TeamAvatar/5312df1b7b07e9abc6781e5f6e3817be-Large.png?w=450&h=450&Expires=1713501547&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZG4uZ2lsY2RuLmNvbS8qIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzEzNTAxNTQ3fSwiSXBBZGRyZXNzIjp7IkFXUzpTb3VyY2VJcCI6IjI0LjE5OS4xNTIuMjM4In19fV19&Signature=D75IeuXQCMVedfF8AThdDs94pQKNAmkGMXojD3CgcH-tO-nMJW%7EDvpNX8xhBy-xWe47KcvFXadVojfgk5uyVCQkgvEn2zWOz3V8pOJVTFUkGBdiY8cW5g8daP%7EIoueun5tLHv-5kjWifcl7BkPbB-7WaRR0rgNqiJEKxMV1QPIe3wmhFMmx%7EmOTvvdShrR2OVIjLjVx29Qw4J4ZFg7cOq9i8XE80XvVVe37LHVEqmtyv%7ExSGiXEh3vtrTGevbBbhDbJus5p%7E-eVBOwf8inaEHORQAmBeIZIeFMxx0mMFGg2uBWHcl80JBCHvTmfmgcORZv-m58-b3GAfMFULhCUzgA__&Key-Pair-Id=K1FFKFZRWAZSB)

Genesis • Posted in #Genesis FAQ & Changelogs

![Kenshi group avatar](https://cdn.gilcdn.com/GroupAvatar/6a88e1ab142e9e47840ef37d8a260c79-Small.png?w=126&h=126&Expires=1713501547&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZG4uZ2lsY2RuLmNvbS8qIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzEzNTAxNTQ3fSwiSXBBZGRyZXNzIjp7IkFXUzpTb3VyY2VJcCI6IjI0LjE5OS4xNTIuMjM4In19fV19&Signature=D75IeuXQCMVedfF8AThdDs94pQKNAmkGMXojD3CgcH-tO-nMJW%7EDvpNX8xhBy-xWe47KcvFXadVojfgk5uyVCQkgvEn2zWOz3V8pOJVTFUkGBdiY8cW5g8daP%7EIoueun5tLHv-5kjWifcl7BkPbB-7WaRR0rgNqiJEKxMV1QPIe3wmhFMmx%7EmOTvvdShrR2OVIjLjVx29Qw4J4ZFg7cOq9i8XE80XvVVe37LHVEqmtyv%7ExSGiXEh3vtrTGevbBbhDbJus5p%7E-eVBOwf8inaEHORQAmBeIZIeFMxx0mMFGg2uBWHcl80JBCHvTmfmgcORZv-m58-b3GAfMFULhCUzgA__&Key-Pair-Id=K1FFKFZRWAZSB)

- -deleted the temporary police station from the scraphouse.
- -fixed an issue with the grid gate as reported by @Terak
- -removed a town from the outlands that had no purpose or town marker as reported by @𝓢𝓷𝓸𝔀 ℬ𝓪𝓵𝓵
- -reworked carsi to fix FPS issues and foliage spawn issues as reported by @Krivasran
- -fixed a dialogue bug with surgeons when traded as pointed out by @HorHorHor
- -added more animal races to desert sabre
- -tweaked the slave dialogue. it should now properly detect some characters by race and all other slave prices have been tapered at a flat 200 cats.
- -updated confusion start to be less meme-y and more clear as per suggestion from @HorHorHor and voted on by the community
- -merged borons HN assets, merged snugsnugs building variations.
- -rebuilt the HN and templated the interiors for ease of modification later down the line
- -attached some buildings to share interiors from borons HN additions. i.e. two different buildings (look different) can now use and share interiors.
- -fixed a bug in the floodlands ancient lab where navmesh generation would break due to being split in half by zones thanks to @Slug
- -fixed a bug with the strong starving bandits. level 40's are meant to spawn after all 3 borderzone bosses are dead. they were set to spawn while they are alive thanks to @Aesthetic
- -fixed an overspawn issue as indicated by @Regalia in the hub bar. Bar now refreshes every 12 hours and only holds up to 30 items at a time.
- -fixed some polish issues in vains pass as noted by @Regalia
- -fixed an issue with the sacred guard spawning as women. dark beasts 😠
- -overhauled pagunder, needs polish
- -Overhauled nomar, added guard tower along with barracks and an inn closer to the road side. should help facilitate traveling squads
- -overhauled dustirmiril. added an inn, farm shop, moved it slightly away from the valley
- -overhauled reduna. likely needs another polish pass

^ Released on Steam/Nexus 7/5/2023 ^

- -fixed an issue with cattrinas Cozy chairs. swapped max operators to 1. should fix duplicated sitting positions
- -changed knifes combat skills to be 20 max per skill instead of 25. thus less than 75, which should make them recruitable.
- -added water avoidance of 3 for cyber hives (TS variants).
- -added new graveyard wolves to the canine plate as @Regalia had described in their bug report
- -Changed the swampers travel store in shark to now be inside the L-house thanks to a bug report from @Regalia
- -rotated a bar in grind stone near the north wall to avoid navmesh issues as reported by @Royal
- -removed the cannibals properly from the swamp
- -added authentic skeleton repair kit to shinobi guards for mongrel. fixing a bug reported by @Regalia
- -Fixed nomad bar camp according to a bug report from @Regalia modified the building type for settled nomads from swamp round 1 to swamp round 2
- -changed cannibals and skavs to now eat raw fish, foul meat and raw meat from a suggestion from @Alkimos
- -deleted the floating books from a bug report by @Costeer
- -thanks to @Regalia changed the slavers in HN to be men led
- -cloned the slavemaster squad and renamed it to Holy Workmaster,
- -cloned the slaver to be called work master,
- -duplicated the Holy servant clothing, armor and weapons to the new Workmaster
- -cleaned up a bug with the ILAM stats according to a bug report from @Regalia
- -added new workmaster to rebirth to ensure slaves are used and worked throughout the day (including the player).
- -added mines back into rebirtht to balance out active spots of usage for slaves and the player. Should fix AI issues in rebirth.
- -adjusted the thiefs guild fence and smuggler. Reworked conditions to now properly reflect your level. you will still need to be level 2 or above to trade with them, however they both now say as much.
- -added thieves knapsacks and empty vendors to the thieves guild fence and smuggler.
- -though temporary, fixed the arbiter dialogue and duplication glitch.
- -though temporary added the wanderer start member to the leader for the ironside squad.
- -made some tweaks to deadcat thus it should fix the deadcat cannibal issue of not being able to get to the boss
- -fixed an issue according to a bug report from @Regalia
- -fixed a bug with spawns in tadpole
- -made small animal feeders only placeable outside.
- -fixed an issue with vains pass walls. adjusted the north eastern battlements to face less inwards and thus pushing them across one zone change instead of four
- -moved vault 3 to the left more to pull it off the zone lines it was sitting on. it should prevent it from having broken navmesh
- -added an ai package to the rusted v1 homeless squad as reported by @Lato it didnt have an ai package making them not react to attacks and be stationary.
- -added a outpost 1 back to the scout post in hidden forest.
- -fixed an incomplete holy military post in okrans gulf thanks to @Regalia
- -Fixed an incomplete library in leviathans coast with a bug report from regalia
- -fixed overspawning with albino landbats they were meant to be rare
- -made a balance pass at the dust bandit cut weapons
- -made a balance pass on scav weapons
- -attemtpted to fix HN thieves guild
- -fixed hn color of the sentinels
- -added doctor chung to the swamper spawn list
- -added oron to the shady bar recruits list. Allowing them to spawn everywhere from swamps to the UC, Most commonly in Tech Hunter Cities
- -fixed a bug with library ruins spawning with full but empty buildings as reported by @Mihokyo
- -added trade signs to the outside of large holy house.
- -added a name to the building holy trade goods.
- -added hemp buildings to illegal buildings for HN
- -added hemp items to illegal goods and forbidden goods of the HN
- -added various packages to slaves regarding escapes and slavery as reported by @Regalia this change will be temporary until i start working on dialogue.
- -attempted a fix on hivers spawning as thieves guild members in the HN
- -fixed eye socket furniture bugs
- -updated racial restrictions for hiver armor.
- -fixed a bug on how stubs spawns and what he spawns as as reported by @imObvioslycrazy
- -changed slave lord rens group speed to no change status as per bug report from Para
- -added a secondary path to VP for npcs to traverse into and out of the city as per suggestion from @imObvioslycrazy
- -fixed a visual bug with the Z9 race per a report from @Spriteanon
- -fixed a interior bug as reported by @Mihokyo for the bar1 squad. players should no longer get trapped between beds
- -nomads and settlers are now allies and should defend each other. while only a temporary fix it should allow them to not masscre each other as reported by @Regalia
- -lowered the amount of security spiders in lost amouries as per a report from Para
- -added a new stat set to outlaw farmers as per @Regalia bug report. hovering around 5-10 combat stats and 50 ish in non combat.
- -added the merc armor set from cat's mod properly to the vendor list for blackdog hq per a report from @Geodarian
- -made some detail adjustments to vainspass. a hivers house was blocked off with the last change, rectified by pulling the house ramp onto the new road
- -changed hive factories to now have a hive trader that sells armor and weapons.
- -adjusted some foliage in the swamps to help with navmesh generation
- -locked some hiver squads in vains pass so they don't grow exponentially with player settings

Back from break 11/30

- merged unique animal hides and skins into "animal" hide. So beyond trophy items players will not have multiple crafting stations to work through. all animals will have "animal skin" as a default item. (excluding some obvious ones, like bugs)
- added mud pits as a resource to most forested lands. Swamps, hidden forest, the burning forest, wetlands, (early game material)
- added moth borers as a resource to most forested lands. Swamps, hidden forest, the burning forest, wetlands (early game crossbow crafting)
- added termite mounds to most forested lands. Swamps, hidden forest, the burning forest, wetlands

Merged Mods:

- https://steamcommunity.com/sharedfiles/filedetails/?id=2371344547
- https://steamcommunity.com/sharedfiles/filedetails/?id=2456515727
- https://steamcommunity.com/sharedfiles/filedetails/?id=2371365498
- https://steamcommunity.com/sharedfiles/filedetails/?id=2390756295
- https://steamcommunity.com/sharedfiles/filedetails/?id=2223867724
- https://steamcommunity.com/sharedfiles/filedetails/?id=2457830380
- (New races hidden)
- https://steamcommunity.com/sharedfiles/filedetails/?id=1489675661
- https://steamcommunity.com/sharedfiles/filedetails/?id=1501880679
- https://steamcommunity.com/sharedfiles/filedetails/?id=1902172624
- https://steamcommunity.com/sharedfiles/filedetails/?id=2355540931
- https://steamcommunity.com/sharedfiles/filedetails/?id=2162904332
- https://steamcommunity.com/sharedfiles/filedetails/?id=2467997525
- (only the buildings)
- https://steamcommunity.com/sharedfiles/filedetails/?id=2425159105
- https://steamcommunity.com/sharedfiles/filedetails/?id=2348103277
- https://steamcommunity.com/sharedfiles/filedetails/?id=1870773796
- https://steamcommunity.com/sharedfiles/filedetails/?id=2332647932
- https://steamcommunity.com/sharedfiles/filedetails/?id=2321974486
- https://steamcommunity.com/sharedfiles/filedetails/?id=2381564824
- https://steamcommunity.com/sharedfiles/filedetails/?id=1671502407
- https://steamcommunity.com/sharedfiles/filedetails/?id=2421898739
- https://steamcommunity.com/sharedfiles/filedetails/?id=1741331999
- https://steamcommunity.com/sharedfiles/filedetails/?id=2412497702
- https://steamcommunity.com/sharedfiles/filedetails/?id=2549561183
- https://steamcommunity.com/sharedfiles/filedetails/?id=2452035761
- https://steamcommunity.com/sharedfiles/filedetails/?id=2495652142
- https://steamcommunity.com/sharedfiles/filedetails/?id=2508412096
- https://steamcommunity.com/sharedfiles/filedetails/?id=2543174982
- https://steamcommunity.com/sharedfiles/filedetails/?id=2802266634
- https://steamcommunity.com/sharedfiles/filedetails/?id=2817703165
- https://steamcommunity.com/sharedfiles/filedetails/?id=2797192806
- https://steamcommunity.com/sharedfiles/filedetails/?id=2117877487
- https://steamcommunity.com/sharedfiles/filedetails/?id=2861359197
- https://steamcommunity.com/sharedfiles/filedetails/?id=2846933782
- https://steamcommunity.com/sharedfiles/filedetails/?id=2822767279
- https://steamcommunity.com/sharedfiles/filedetails/?id=2875287426
- https://steamcommunity.com/sharedfiles/filedetails/?id=2550832666
- https://steamcommunity.com/sharedfiles/filedetails/?id=2910649298
- https://steamcommunity.com/sharedfiles/filedetails/?id=2545328388
- https://steamcommunity.com/sharedfiles/filedetails/?id=2655761977