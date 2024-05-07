---
date: 2024-04-21T15:44
tags: 
cssclasses:
  - center-images
  - page-kenshi
---
[[Kenshi Modding Wiki]]
[[The FCS - A Complete Guide]]

Conditions added here use AND logic.

If you add three conditions, this line will only play if all the conditions return true.

Where multiple lines are possible and you haven’t modified the line Score, Kenshi will pick lines from the most to the least number of conditions.

Talker Enums

T_ME

- The character who initiated this dialogue event.

If used inside a wordswap, T_ME refers to the character who is actually speaking this line.

If used on an interjection node, T_ME refers to the interjector.

T_TARGET

- The target of the dialogue event if it has one.

T_TARGET_WITH_RACE

- The target of the dialogue event if it has one & you’ve specified a target race condition on that line. Returns a race matching the target race specified, otherwise doesn’t play.

T_TARGET_IF_PLAYER

- The target of the dialogue event if it has one & it’s a player character.

T_INTERJECTOR1/2/3

- The interjector you specify after you’ve added interjectors via an interjection node.

T_WHOLE_SQUAD

- Anybody in the dialogue initiator’s squad.

Special Note:

WHOLE_SQUAD checks for anybody and not everybody.

For instance,

T_WHOLE_SQUAD / DC_IN_COMBAT / = 1

will return true if anybody in the speaker’s squad is in combat.

See the advanced dialogue section on using Empties for how to use these checks properly.

Non-Functional Checks

- DC_FACTION_VARIABLE
- DC_REPUTATION

Dropdown Checks

- The checks selected from the dropdown at the top right of the dialogue window. Most of these checks use OR logic.

Has Package (OR)

Refers to T_ME. If used on an interjector node, searches for an interjector with that package.

Has package checks whether a character has a given dialogue package in their full dialogue set.

See the section on Empty Packages for how to use dialogue packages to differentiate types of characters effectively.

Is Character (OR)

Refers to T_ME. If used on an interjector node, searches for an interjector who is that specific character. Can also be used on interjector nodes to force characters with “dumb” set to true to speak (like Agnu).

In Town Of (OR)

Will be true if the speaker is currently in any town belonging to the faction you list.

My Faction (OR)

Target Faction (OR)

Checks for relevant factions of the speaker and the speaker’s target.

Useful to make factions interact with one another.

Using the “Nameless” faction here refers to the player’s faction.

My Race (OR)

My Subrace (OR)

Checks for the race of T_ME. My Race looks at all races in a race group, so checking for a Greenlander will check for any human. Use My Subrace is you want to differentiate between Greenlander/Scorchlander or Hiver types.

Target Has Item (OR)

Target Has Item Type (OR)

Checks if anybody in the target’s squad has a given item in their inventory. Target has item type looks only in inventory; target has item checks worn backpacks as well.

Has Item Type checks whether anybody in the target’s squad has an item with the same function (e.g. ITEM_FOOD) in their inventory (not a backpack).

+9*8//-+

Listing multiple items checks for any of them.

Target Race (OR)

No Target Race (AND)

Checks whether the target’s squad has/does not have any of the listed races in it.

Combining target race with a speaker set to TARGET_WITH_RACE will force a target with that specific race to speak.

See the section on Unique NPCs for more information on how to use TARGET_WITH_RACE properly.

World State (AND)

Checks the given world states you list.

An empty world state will always return true.

See the section on World States for complex World State checks.

Complex Checks

- Other conditions are self-explanatory.
- The following conditions check for multiple things at once or have extra hidden functions.

DC_I_LOVE_THIS_GUY

DC_I_HATE_THIS_GUY

These two conditions check all of the long-term tags (e.g. LIFESAVER) at once.

I_LOVE_THIS_GUY will be true if the player has saved a character’s life or freed them from prison before and I_HATE_THIS_GUY is false.

I_HATE_THIS_GUY will be true if the player has beaten a character’s squad in combat, killed a character’s squadmate, or thrown them in prison before.

DC_I_SHOULD_HELP_THIS_GUY

DC_I_SHOULD_SCREW_THIS_GUY_OVER

These checks weigh up I_LOVE_THIS_GUY/I_HATE_THIS_GUY and look at character personalities - as well as the player’s standing with a faction, and NPC type.

I_SHOULD_SCREW_THIS_GUY_OVER will be true if a character is traitorous and the player isn’t an ally, or if the character is of the OT_BANDIT type and not Honourable. It will also be true if the character’s faction hates the player or I_HATE_THIS_GUY is true.

I_SHOULD_HELP_THIS_GUY will be true if I_LOVE_THIS_GUY is also true, or if the player is allied to a character’s faction. It will also be true if the player is wearing a disguise that hasn’t been blown, or if the NPC is the same character type (i.e. OT_ADVENTURER) as the player. Note that all player characters change to the OT_ADVENTURER type when recruited.

DC_TARGET_IN_TALKING_RANGE

This checks to see if the target character is relatively close - i.e. close enough to have a conversation with.

If this check is called on the same line as the effect, DA_FOLLOW_WHILE_TALKING, then the character will automatically stop following the target if no longer in talking range.

DC_IS_RECRUITABLE

This condition is used in Vanilla to prevent the player from getting new recruits who are too strong. It’s automatically false for any NPC of the OT_MILITARY, OT_LAW_ENFORCEMENT, OT_DIPLOMAT, and OT_TRADER types.

It’s also false if the character has combat stats > 25 OR if the total of a character’s Attack, Defence, Strength, Martial Arts, Dodge, and Toughness exceeds 75.

DC COPS_AROUND

This condition checks if there are any NPCs of the OT_MILITARY or OT_LAW_ENFORCEMENT type nearby who aren’t KO.

DC_HAS_ILLEGAL_ITEM

This condition checks whether the target is carrying anything defined as contraband in a faction’s assigned trade culture.

DC_HAS_ROBOT_LIMBS

This condition checks whether a character has robotic limb replacements equipped or if the character’s race type has “is robot” set to true.

DC_IMPRISONMENT_IS_DEATHROW

This condition will be true if a character is in a peeler or is imprisoned in a town where the owning faction kills/eats its prisoners.

DC_IS_OUTNUMBERED

This condition checks whether a character is facing off against multiple opponents while in combat.

DC_IS_RUNNING

This checks if the target is running away from the speaker.

DC_NUM_DIALOG_EVENT_REPEATS

Checks how often this character has repeated this dialogue event. The condition will be “=1” on the first repetition, and so forth. The check applies to the whole event, not an individual line of dialogue.

Particularly useful for intelligent AI (e.g. repeated gate guard or crime-witnessing dialogue). Doesn’t work on the first line of dialogue - see the segment on using Empties to use this check properly, or place it on a second line.

Non-Functional Dialogue Effects

- DA_AFFECT_REPUTATION
- DA_MATES_KILL_ME
- DA_MERGE_WITH_SIMILAR_SQUADS*
- DA_ATTACK_TOWN
- DA_LOCK_THIS_DIALOG
- CHOOSE_CONSCRIPTION
- CHOOSE_RECRUITING
- CHOOSE_HIRING_CONTRACT

*Probably

Dialogue Effects

Effects selected from the “Dialogue Effects” dropdown. Most are temporary AI overrides that allow you to command an NPC to do something without using an AI contract.

They work on interjectors and T_TARGET speakers - but they’ll default to T_ME if used inside a talkto event. For instance, if you call a knockout on a player line, it’ll still default to the NPC and not the player character.

The value N here refers to the number with each effect. Most effects don’t have a number that does anything.

DA_TRADE

Opens a trade window with the target and won’t play the dialogue line that triggers the trade effect. Will display everything in the target’s building if a resident or everything in backpacks if a wandering squad.

DA_TALK_TO_LEADER

Makes the speaker talk to the target (not the leader of the target’s squad).

Often combined with unlockable dialogue or interrupt dialogue events.

DA_JOIN_SQUAD_WITH_EDIT

Join the target’s squad by first opening the character editor screen.

Should not be used for NPCs joining other NPC squads.

DA_AFFECT_RELATIONS (N)

Change the relations with the target faction by N.

Won’t display relations change messages to the player, except for where changes in enemy/ally status occur (“United Cities are now your allies”).

DA_ATTACK_CHASE_FOREVER

Attack the target squad until the target squad is out of sight.

DA_GO_HOME

Sends the speaker back to their home building or town.

DA_TAKE_MONEY (N)

Reduces the player’s money by N.

DA_GIVE_MONEY (N)

Adds N to the player’s money.

DA_PAY_BOUNTY

Pays the player the bounty for the character they’re holding.

DA_CHARACTER_EDITOR

Opens the character editor for the target character (like when you visit a plastic surgeon).

DA_FORCE_SPEECH_TIMER (N)

Forces this line to wait for N seconds before moving to the next line.

Kenshi changes the length of time a line displays automatically based on the number of characters it contains. This effect can only increase (and not decrease) that amount of time.

DA_DECLARE_WAR

Reduces relations with the target faction to -30 (the “enemy” threshold) if not already enemies. Displays a message to the player that the two factions are at war.

DA_END_WAR

Increases relations with the target faction so that they’re neutral again.

Doesn’t display a message.

DA_CLEAR_AI

Clears the AI’s current goal.

DA_FOLLOW_WHILE_TALKING

Follow the target character until the dialogue event is over.

If used on a line where DC_TARGET_IN_TALKING_RANGE is set to true, will automatically stop following if the target gets too far away.

Tends to override other goals set through AI contracts.

DA_THUG_HUNTER

Wait for the target outside the town gates or follow them around if not in a town.

Once following and outside the town gates, will cause the speaker to trigger EV_HARRASSMENT_SHOUTS. The town’s gate must be the same faction as the town’s owner.

DA_JOIN_SQUAD_FAST

Join the target squad immediately.

Can be used to make NPCs join other NPC squads. Can also be used to make a PC join an NPC squad. Will change the character’s faction to that of the target.

DA_REMEMBER_CHARACTER

Makes an NPC remember a target character permanently.

Note: Requires further testing

DA_FLAG_TEMP_ALLY

Flags the target character as a temporary ally until not seen for a few hours.

Will disable EV_I_SEE_NEUTRAL events from playing and also won’t count for EV_I_SEE_ALLY_PLAYER as (if used on a player who’s neutral/enemy) the player is now in limbo, neutral-not-neutral state.

Characters using this effect should have betrayal events.

DA_FLAG_TEMP_ENEMY

Flags the target as a temporary enemy.

Usefulness is limited but required sometimes for dummy factions when attacking the player.

DA_MAKE_TARGET_RUN_FASTER

Makes the target (slave) move faster.

Note: Requires further testing

DA_GIVE_TARGET_MY_SLAVES

Give all slaves commanded by me to the target squad.

DA_TAG_ESCAPED_SLAVE

Tags the target as an escaping slave.

DA_FREE_TARGET_SLAVE

Frees the target from slavery.

DA_SEPARATE_TO_MY_OWN_SQUAD

Causes the speaker to create their own squad with themselves as the only member. That character will no longer participate in a running dialogue chain (eg for an Interjector) but the dialogue chain will still continue.

DA_ARREST_TARGET

Makes the speaker pick up the target if unconscious, or attack and then pick them up if conscious. Used by town guards a lot.

DA_ARREST_TARGETS_CARRIED_PERSON

Makes the speaker pick up whoever the target is carrying.

DA_ASSIGN_BOUNTY (N)

Assigns N bounty which defaults to the “Assault” crime enum.

DA_CRIME_ALARM and AI in general automatically assigns bounties, so this is only needed where you want to forcibly assign an additional bounty.

The bounty faction is defined under Legal System in a faction.

DA_CRIME_ALARM

Flags the target as a criminal and calls a relevant crime enum for their actions based on the dialogue event (EV_WITNESS_LOCKPICK, EV_WITNESS_KIDNAPPING_ALLY, etc).

If used after DC_HAS_ILLEGAL_ITEM, will flag the target as having the “Smuggling” crime enum. Defaults to “Assault” if nothing else is known.

DA_RUN_AWAY

Makes the speaker run away in a random direction and in a short radius for a while.

DA_INCREASE_FACTION_RANK

Increases the player’s faction rank by 1 each time it’s called (the number doesn’t matter - calling DA_INCREASE_FACTION_RANK 1 is the same as DA_INCREASE_FACTION_RANK 100). Faction rank is saved to the .save file in each faction. Calling it on an NPC-NPC encounter will still increase the player's rank. There’s no way to decrease it again because this is Kenshi.

DA_ASSAULT_PHASE

For War Campaigns.

Tells the AI involved to transition to Phase II.

DA_RETREAT_PHASE

For War Campaigns.

Tells the AI involved to transition to the Retreat Phase if you need a fallback or an additional event. However, Retreat Phase will automatically be called after a set time, or if the attacking faction is defeated.

DA_VICTORY_PHASE

For War Campaigns.

Tells the AI involved to transition to the Victory Phase.

DA_ENSLAVE_TARGETS_CARRIED_PERSON

Makes the speaker turn whoever the target is carrying into a slave.

CHOOSE_SLAVES_SELLING

Opens a dialogue window allowing the player to sell people or carried people as slaves.

CHOOSE_SLAVES_BUYING

Opens a dialogue window allowing the player to purchase slaves from the speaker’s squad.

CHOOSE_PRISONER_BAIL

Opens a dialogue window allowing the player to bail anybody imprisoned out by paying their bounty.

SURRENDER_NON_HUMANS

Gives all characters who are not part of the Human race group to the target’s squad as slaves.

CHOOSE_ANIMALS_BUYING

Opens a dialogue window to purchase any of the animals in the speaker’s squad.

DA_CLEAR_BOUNTY

Removes the target’s bounty.

DA_PLAYER_SELL_PRISONERS

Opens a dialogue window allowing the player to sell the characters in the player’s cages.

Only works in player towns.

Note: Requires more testing.

DA_PLAYER_SURRENDER_MEMBERS_DIFFERENT_RACE

Surrenders all characters who are not the race of the target as slaves.

DA_SUMMON_MY_SQUAD

Forces everybody in the speaker’s squad to converge on their position once.

DA_REMOVE_SLAVE_STATUS

Removes the slave status of the target entirely.

DA_OPEN_NEAREST_GATE

Makes the character run to the nearest gate and open it if locked.

DA_ATTACK_STAY_NEAR_HOME

Makes the character attack the target squad but break off quickly if they get too far.

Triggers the EV_GIVE_UP_CHASE dialogue event when this happens.

DA_MASSIVE_ALARM

Forces every nearby ally* to converge on the target.

All involved characters will keep chasing the target until they reach them, so they’ll chase a player forever if the player is running away. This effect tends to be pretty messy and look ridiculous in-game. Use AI contracts instead.

*Might not call every NPC Type

DA_ATTACK_IF_NO_COEXIST

Makes the speaker attack the target squad if there is no coexistence defined with the target faction.

DA_KNOCKOUT (N)

Causes the speaker to become unconscious for N seconds. Will end a dialogue chain.