<img src="LoFi_Group_Photo.png" title="LoFi_Group_Photo.png" width="250"
alt="LoFi_Group_Photo.png" /> Players start Kenshi with a set number of
player characters to customize depending on their selected [](Game_Starts.md). Across the world of Kenshi, there are
many characters who can become player characters after certain
interactions. After recruiting any number of these characters, players
can control each squad member as well as all of them at once.

The maximum number of characters you can control is 30. This can be
increased with [mods](Modifications.md "wikilink") fairly easily. Once
players have reached 30 characters total, dialogue options will no
longer appear for recruitable characters. Instead, they may notice
drifters hanging around and even protecting your town without a word.
Note that having more characters is more computationally demanding and
can affect game performance.

Most characters that can join the player must also be "Recruitable".
Which means that they must have 25 or lower in Strength, Dexterity,
Melee Attack, Melee Defence, Martial arts, and Dodge or lower than 75
cumulative total in those stats, if any of them are above 25. They also
must not be a [Diplomat](Diplomatic_Status.md "wikilink"), Law Enforcer,
Military, or Trader class character. Though there are a few exceptions
to these rules, due to dialog loopholes.

## Hiring Characters

Most Recruits join the [Player Faction](Nameless.md "wikilink") through
dialogue options found in towns. Recruits for Hire can be found
patrolling town or hanging out in a bar. These recruits have a set fee
for joining and become Player Characters immediately after receiving
that money. This fee is generally between 3,000 to 7,500 cats.

Characters for Hire can be randomized [](Generic_Recruits.md) or [](Unique_Recruits.md). Most randomized recruits start
with very low stats, rag clothing, a simple weapon, and hunger. Unique
recruits often have a few elevated stats (10-15) depending on their
specialty (i.e. Medic) but are still relatively weak.

## Rescuing Characters

[Slavery](Slavery.md "wikilink") is prevalent across the world of Kenshi.
Some Slaves are happy to serve their masters, but most are very
appreciative to be freed by the Player. After freeing Slaves and
Prisoners, they will become allied to the Player. They will appear green
on the Map and will follow around the character who freed them. If they
are kept safe for a while, they can potentially become Player
Characters. Otherwise, they will run off into the wilderness to join
back up with their faction.

In some locations such as [Tengu's Vault](Tengu's_Vault.md "wikilink") and
the [Dust King Tower](Dust_King_Tower.md "wikilink"), [](Unique_Recruits.md) are being kept prisoner. They will
join the Player Faction after being freed.

## Purchasing Characters

[Slaves](Slave_Recruits.md "wikilink") and Animal Player Characters can be
purchased from their owners. After Slaves are purchased from their
[Slaver Boss](Slaver_Boss.md "wikilink"), they will be Allies. If they are
kept safe for a while, they can potentially become Player Characters.
The [Unique Recruit](Unique_Recruits.md "wikilink") [Ray](Ray.md "wikilink")
is an exception to this. After purchasing Ray from his
[master](Bar_fly.md "wikilink"), he is automatically a Player Character
despite still wearing [](Hive_Prisoner_Shackles.md).

Animals purchased from [Nomads](Nomads.md "wikilink"), [](Farm_Shop.md), or [Holy Farms](Holy_Farms.md "wikilink")
automatically become Animal Player Characters and do count towards your
character limit. More information on purchasable animals can be found on
[Guide to Animals](Guide_to_Animals.md "wikilink").

## Saving a Character's life

You can recruit a character by triggering a "You saved my life!"(FCS
name) dialog.

Conditions:

"LT_MY_LIFESAVER" tag on your character; (Which probably means you have
to heal them from the "dying" state. I didn't test this as i found this
by accident during my ~3rd playthrough)

"DC_TARGET_LAST_SEEN_X_HOURS_AGO" \> 24

saved character can have any "DC_PERSONALITY_TAG" except
"PT_TRAITOROUS";

saved character must have "DC_IS_RECRUITABLE" tag or ("PT_BRAVE
DC_PERSONALITY_TAG" and "Npc TOUGH Merc Basic 1" dialogue package)

If saved character has "DC_IS_RECRUITABLE" tag it must have
"PT_HONOURABLE" "DC_PERSONALITY_TAG" or one of these dialogue packages:

- civilian normal
- civilian tough
- Fresh Ronin
- Wandering citizen
- wandering trader (civilian combo)

<!-- -->

- or "All leaders are alive = 0" condition must be met (at least one of
  the following leaders must be dead: Tengu, Longen, Esata, Phoenix,
  Bugmaster)

note: Due to these conditions it is possible to recruit characters with
very high skill and attribute levels, such as named anti-slaver jonins
(~80 stats in almost all skills and attributes (not counting racial
bonuses which can boost them up to 90+)). \[game version 1.0.51\]

## 'Is Recruitable' Tag

To be considered recruitable by the *DC_IS_RECRUITABLE* tag, a character
must **not** be one of the following classes:

- Diplomat
- Law Enforcer
- Military
- Trader

Furthermore, no combination of these three stat pairs can be 75 or
higher:

([Strength](Strength.md "wikilink") or [Dexterity](Dexterity.md "wikilink")) +
([Melee Attack](Melee_Attack.md "wikilink") or [](Martial_Arts.md)) + ([](Melee_Defense.md) or [Dodge](Dodge.md "wikilink"))

In each pair, it will use whichever one is higher. If the total from all
three is 75 or higher, the character is not recruitable.

But it will also use only one stat in each of those pairs. So, for
instance, a character with 70 Strength and 70 Dexterity would still be
considered recruitable, as long as their other pairs sum up to less than
5. Also remember that while a character's stats might display 25, they
could actually be 25.99, which would make the math off by 2 or 3.

## List of Playable Characters (Wip)

This is a comprehensive list of every character that can possibly be
recruited in vanilla, race, their method of recruitment, and price if
applicable.

| Character                                             | Race                                              | Recruitment Method                    | Price | Notes                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------|---------------------------------------|-------|---------------------------------------------------------------------------------------------------------|
| Adventurer                                            | [Greenlander](Greenlander.md "wikilink")             | Game Start                            | N/A   | Cannibal Hunters Game Start                                                                             |
| Adventurer with skill                                 | [Greenlander](Greenlander.md "wikilink")             | Game Start                            | N/A   | Cannibal Hunters Game Start                                                                             |
| [Agnu](Agnu.md "wikilink")                               | [Soldierbot](Soldierbot.md "wikilink")               | Dialog, Rescue                        | N/A   |                                                                                                         |
| [Baker](Baker.md "wikilink")                             | Random                                            | Rescue (Cannibal)                     | N/A   |                                                                                                         |
| [Band of Bones](Band_of_Bones_(Character).md "wikilink") | [Shek](Shek.md "wikilink")                           | Rescue                                | N/A   | Ignores Recruitable requirements. Only if honourable or maniacal [Personality](Personality.md "wikilink"). |
| [Bar Fisherman](Bar_Fisherman.md "wikilink")             | Random                                            | Rescue, Purchase from Slavery         | N/A   |                                                                                                         |
| [Bar fly](Bar_fly.md "wikilink")                         | Random                                            | Rescue, Purchase from Slavery         | N/A   |                                                                                                         |
| [Bar Thug](Bar_Thug.md "wikilink") (Traitorous)          | [Greenlander](Greenlander.md "wikilink")             | Rescue, Purchase from Slavery         | N/A   |                                                                                                         |
| [Bar Thug](Bar_Thug.md "wikilink") (Crazy)               | [Greenlander](Greenlander.md "wikilink")             | Rescue, Purchase from Slavery         | N/A   |                                                                                                         |
| [Bar Thug](Bar_Thug.md "wikilink") (Drunken)             | [Greenlander](Greenlander.md "wikilink")             | Rescue, Purchase from Slavery         | N/A   |                                                                                                         |
| [Bard](Bard.md "wikilink")                               | [Greenlander](Greenlander.md "wikilink")             | Dialog, Rescue, Purchase from Slavery | 3,000 |                                                                                                         |
| [Barman](Barman.md "wikilink")                           | Random                                            | Rescue (Cannibal)                     | N/A   |                                                                                                         |
| [Beep](Beep.md "wikilink")                               | [Hive Worker Drone](Hive_Worker_Drone.md "wikilink") | Dialog                                | Free  |                                                                                                         |
| [Berserker](Berserker.md "wikilink")                     | [Shek](Shek.md "wikilink")                           | Rescue                                | N/A   | Ignores Recruitable requirements. Only if honourable or maniacal [Personality](Personality.md "wikilink"). |
| [Big Fang](Big_Fang.md "wikilink")                       | [Scorchlander](Scorchlander.md "wikilink")           | Rescue, Purchase from Slavery         |       |                                                                                                         |
| [Big Gray](Big_Gray.md "wikilink")                       | [Greenlander](Greenlander.md "wikilink")             | Rescue                                |       | Depends on stats.                                                                                       |

__NOTOC__ __NOEDITSECTION__

[Category:Guides](Category:Guides "wikilink")