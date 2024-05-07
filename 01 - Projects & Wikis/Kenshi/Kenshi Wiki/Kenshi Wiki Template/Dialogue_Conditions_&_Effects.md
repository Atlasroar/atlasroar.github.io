Things from [](Forgotten_Construction_Set.md)

See also: [Dialogue Targeting](Dialogue_Targeting.md "wikilink")

# Conditions

FCS deals most conditions as AND. There are some conditions that will be
OR if multiple options are available, such as personalities or money. If
using those and you want specific result on branches, use only one
condition per line. You can use empty lines (space bar). Also most
conditions tend to treat the player faction as one, meaning you met one
PC you have met them all. \[Cattrina\]

DC = Dialogue Condition or Dialogue Check

Example:

<table>
<tbody>
<tr class="odd">
<td><p><small><sup>Dialogue</sup></small></p>
<ul>
<li><small><sup>|c] <Empty> (condition T_TARGET_IF_PLAYER DC_RELATIONS
&gt; -1)</sup></small>
<ul>
<li><small><sup>[*] T_ME "It costs 1000 cats"[c] T_TARGET_IF_PLAYER
"I'll take it!" (condition T_TARGET_IF_PLAYER DC_PLAYERMONEY &gt; 999)
DA_TAKE_MONEY 1000</sup></small></li>
<li><small><sup>[c] T_TARGET_IF_PLAYER "I do not have that much"
(condition T_TARGET_IF_PLAYER DC_PLAYERMONEY &lt;
1000)</sup></small></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

- **DC_Bounty_Amount_Actual**
- **DC_Bounty_Amount_Perceived**
- **DC_Broken_Arm**
  - True if the character has an arm with health below 0.
- **DC_Broken_Leg**
  - True if the character has a leg with health below 0.
- **DC_Building_Is_Closed_And_Secured**
- **DC_Can_Afford_Bounty**
- **DC_Carrying_Bounty_Alive**
  - Returns true if the character is carrying someone with a bounty on
    them that is alive.
- **DC_Carrying_Bounty_Dead**
  - Returns true if the character is carrying someone with a bounty on
    them that is dead.
- **DC_Carrying_Someone_To_Enslave**
  - Returns true if the character is carrying someone that can be
    enslaved by **ME**.
- **DC_Cops_Around**
  - Returns true if there are law-enforcing guards or patrols nearby.
- **DC_Damaged_Head**
- **DC_End**
- **DC_Faction_Rank**
- **DC_Faction_Variable**
- **DC_Has_A_Base_Nearby**
- **DC_Has_AI_Contract**
  - Returns true if the player faction currently has any AI contract
    with the NPC talking (single NPC).
  - When the squad leader has the contract, it applies to the entire
    squad (such as with mercenaries). In this case the condition should
    also be run along with DC_IS_LEADER (if you have the same dialog
    with every squad member) so only the leader gets the 'talk to'
    prompt. All squad member should have DC_IS_LEADER == 0
    DA_TALK_TO_LEADER \[Cattrina\]
- **DC_Has_Illegal_Item**
  - Returns true if the character has an illegal item in their
    inventory. Does not include items inside backpacks.
  - Illegal items are determined by the town's trade culture.
  - If true, displays the notification "<Character> has been discovered
    smuggling <Item>." Even if the character is an NPC.
- **DC_Has_Robot_Limbs**
  - Returns true if the character has robotic limbs attached.
- **DC_Has_Tag**
  - **LT_None**
  - **LT_My_Intruder:** NPC only, returns true if the player is inside
    their non-public building
  - **LT_My_Lifesaver:**
  - **LT_Freed_Me:**
  - **LT_Stole_From_Me:** Returns true if the player has been caught
    stealing from ME before.
  - **LT_My_Captor:**
  - **LT_Friendly_Aquaintance:**
  - **LT_Defeated_My_Squad_Once:**
  - **LT_Killed_My_Friend:**
  - **LT_I_Screwed_This_Guy:**
  - **LT_Max:**
- **DC_I_Hate_This_Guy**
- **DC_I_Love_This_Guy**
- **DC_I_Should_Help_This_Guy**
- **DC_I_Should_Screw_This_Guy_Over**
- **DC_Im_Unarmed**
  - Returns true if **ME** has a sword equipped or in their inventory.
    Does not include swords in backpacks.
  - Returns true if **ME** is equipped with a crossbow, even the
    character does not have any bolts. Crossbows inside the character's
    inventory or backpack are not included.
  - NPC only
- **DC_Imprisoned_By_Other**
  - NPC only
  - Returns true if the NPC is inside a cage of another NPC faction
- **DC_Imprisoned_By_Target**
  - NPC only
  - Returns true if the NPC is inside a cage of the player or the other
    NPC faction, that has been targeted by AI
- **DC_Imprisonment_Is_DeathRow**
- **DC_In_A_Non_Player_Town**
  - Returns true if the NPC is not inside or nearby player base
  - Can be used for player characters too for screams of pain etc. See
    Amputation Table mod by Cattrina
- **DC_In_A_Player_Town**
  - see above
- **DC_In_Combat**
- **DC_In_My_Building**
- **DC_Is_A_Trader**
  - Returns true if this character is marked as being a trader.
- **DC_Is_Ally**
  - Returns true if these characters are allies.
- **DC_Is_Dead**
- **DC_Is_Enemy**
- **DC_Is_Escaped_Slave**
  - Returns true is this character is marked as being an escaped slave.
- **DC_Is_Female**
  - Returns true if this character is female.
- **DC_Is_Imprisoned**
- **DC_Is_In_Locked_Cage**
- **DC_Is_Indoors**
  - Returns true if the character is inside a building.
- **DC_Is_KO**
- **DC_Is_Leader**
  - Returns true if the character is the squad leader.
  - For example the squad leader of a trade caravan is usually the main
    trader that all the animals and caravan guards follow.
- **DC_Is_Nearly_KO**
  - Broken. Always returns true. Use "DC_Nearly_KO" instead.
- **DC_Is_Outnumbered**
- **DC_Is_Player**
  - Returns true if the character is a member of the player’s faction.
  - Use == 0 on I_SEE events to rule the player out from results
- **DC_Is_Recruitable**
- **DC_Is_Running**
  - True if the character is both at a running speed and is moving away
    from **ME.**
  - Always returns true when run on **ME.**
- **DC_Is_Same_Race_As_Me**
  - Returns true if these two characters are the same race.
  - Keep in mind that subraces are different than races. So Greenlanders
    and Scorchlanders should both be considered as being the same race.
- **DC_Is_Slave**
  - Returns true if this character has been enslaved.
- **DC_Is_Sneaking**
  - Returns true if the character is sneaking.
- **DC_Met_Target_Before**
  - Triggers if the NPC has spoken with a player character before. Does
    not matter which character. The entire player faction is then known.
    \[Cattrina\].
  - Used with the "DA_Remember_Character" dialogue effect.
- **DC_Mixed_Gender_Group**
  - Returns true if the squad has both male and female characters in it.
- **DC_My_Mission_Is_Friendly**
- **DC_Nearly_KO**
  - Checks if the character is low on health.
  - Not affected by hunger meter.
- **DC_None**
- **DC_Num_Backpacks**
  - Returns the number of backpacks in the character's squad.
- **DC_Num_Dialogue_Event_Repeats**
- **DC_Personality_Tag**
  - Returns true if the character has this personality tag. (treated as
    an "or" condition)
  - PT_None, PT_Honorable, PT_Traitorous, PT___, PT__, PT_Smart,
    PT_Dumb, PT____, PT_____, PT_Brave, PT_Fearful,
    PT_Warm_Kind, PT_Cold_Cruel, PT_Normal, PT_Maniacal, PT_End
- **DC_Player_Tech_Level**
  - Returns the player's tech level (1 to 6).
- **DC_PlayerMoney**
  - Returns the number of cats the player has (does not count physical
    money items)
- **DC_Players_Best_Town_Level**
- **DC_Relations**
  - Returns the relationship value with target faction. \[Cattrina\]
  - fe. condition T_TARGET_IF_PLAYER DC_RELATIONS \> -1 \[Cattrina\]
  - I have used this and it works. It is just better to have ONE
    condition per line, looks like FCS deals several conditions as OR
    not as AND \[Cattrina\]
  - Still, might be better to use DC_IS_ALLY anyways
- **DC_Reputation**
  - Is not implemented, obsolete \[Cattrina\]
- **DC_Squad_Is_Down**
- **DC_Squad_Only_Animals**
  - This is for I_SEE events when a NPC spots a player squad containing
    only animals. Those NPCs then autojoin the player, to keep the
    player's game ongoing despite the fact all their humanoid characters
    are dead.
- **DC_Squad_Size**
  - Returns the number of people in that target’s squad. T_ME, T_TARGET
    or T_TARGET_IF_PLAYER
- **DC_Starving**
  - Returns true if the character has low hunger (hunger meter is below
    200).
- **DC_Stronger_Than_Me**
  - True if this character has higher stats than **ME.**
  - Unclear how exactly this is calculated.
  - Seem to only work on fighting stats.
- **DC_Target_Character_Exists**
- **DC_Target_In_Talking_Range**
  - Checks to see if the **TARGET** is nearby.
  - Used for things like gate guards, so that they don’t talk to someone
    that’s far away.
- **DC_Target_Is_My_Mission_Target**
- **DC_Target_Is_Slave_Of_My_Faction**
- **DC_Target_Last_Seen_X_Hours_Ago**
  - Triggers if the NPC has not seen a player character within the time
    limit. Does not matter which character. Use with
    DA_Remember_Character 0 to save the time. If used without the
    condition it will trigger constantly. \[Cattrina\]
  - Used with the "DA_Remember_Character" dialogue effect.
  - Is meant to prevent a monologue from triggering constantly. Was also
    meant to work as 'not enough time has passed, talk to me later' but
    this set up has never worked correctly. See character Riddly's
    dialogue where the timer on her second trunk line prevents the third
    line being used, just because the timer is constantly refreshed.
- **DC_Town_Has_Fortification_Walls**
- **DC_Town_Level_Current_Location**
- **DC_Town_Walls_Locked_Up**
- **DC_Using_My_Training_Equipment**
  - Triggers when the target is using an object with the BF_TRAINING
    functionality in the same town the NPC is and if the NPC's faction
    owns the town. Also both the object and the NPC must be on the same
    side of a building (inside or outside) and the act of using must
    fall within the NPC's view cone.
- **DC_Weaker_Than_Me**
  - True if this character has lower stats than **ME.**
  - Unclear how exactly this is calculated.
- **DC_Wearing_Locked_Shackles**
  - Returns true if the character is wearing locked shackles,
- **DC_Within_Town_Walls**
- **Null_Null____DC_Target_Squad_Size** Obsolete

# Dialogue Actions AKA Effects

DA = Dialogue Action

- **DA_None**
  - Cannot actually be added to dialogue.
- **DA_Trade**
  - Opens a trade window with the character
  - Contents of the trade window depends on the vendor options set to
    the NPC's squad (randomly selected items from all the vendors in the
    set, by the chance % of each vendor of the set).
- **DA_Talk_To_Leader**
  - Used on I_SEE events on squad members. **Forces** the
    EV_PLAYER_TALK_TO_ME event with the squad leader to happen (no click
    from the player)
  - cannot be triggered from a conversation with the player, must be a
    monologue
- **DA_Join_Squad_With_Edit**
  - Character joins squad and opens the character editor for that
    character. (make sure this is at the end of the dialogue or it will
    lock the game.)
- **DA_Affect_Relations**
- **DA_Affect_Reputation**
  - Obsolete \[Cattrina\]
- **DA_Attack_Chase_Forever**
  - NPCs only, attacks the target squad and follows it. The forever
    means until the NPC is KO or game imported, nothing else, even
    reloading the save, does not end it.
- **DA_Go_Home**
  - NPC only.
  - NPC disengages and walks towards nearest base owned by their
    faction.
  - If arriving to unloaded region the NPC despawns.
- **DA_Take_Money**
  - Takes away the specified number of cats from the player. Should be
    used with Target_if_player DC_Playermoney \> (desired sum -1) first
    \[Cattrina\]
- **DA_Give_Money**
  - The NPC gives the player the specified amount of cats.
  - The NPC's wealth is not calculated, all NPCs in dialogue have all
    the money in the world
- **DA_Pay_Bounty**
- **DA_Character_Editor**
  - Opens a character editor for the player character currently speaking
    with the NPC.
- **DA_Force_Speech_Timer**
  - Forces the line of dialogue to last for the specified amount of
    time.
  - Next line of dialogue is spoken only after the timer for the
    previous line is ended
  - If you want 'silence' in between spoken lines without the previous
    line just hovering, use a line with space(spacebar) on every other
    line, timers on each line. The character will speak 'an empty
    bubble' but at least no text.
- **DA_Declare_War**
- **DA_End_War**
- **DA_Clear_AI**
  - Use on **previous** line before changing the AI \[Cattrina\]
  - Clears all ongoing AI tasks in preparation for AI change
- **DA_Follow_While_Talking**
  - Causes character to say following dialogue at the target while
    following them.
  - Use a monologue loop and speech timer (and an interrupt) to make the
    NPC follow the PC as long as you want.
- **DA_Thug_Hunter**
- **DA_Join_Squad_Fast**
  - Character joins squad without opening the character editor for that
    character.
  - Can be triggered from a Crowd trigger
- **DA_Remember_Character**
  - Used for the "Met_Target_Before" and "Target_Last_Seen_X_Hours_Ago"
    conditions to work properly.
- **DA_Flag_Temp_Ally**
- **DA_Flag_Temp_Enemy**
- **DA_Mates_Kill_Me**
- **DA_Make_Target_Run_Faster**
- **DA_Give_Target_My_Slaves**
- **DA_Tag_Escaped_Slave**
- **DA_Free_Target_Slave**
- **DA_Merge_With_Similar_Squads**
- **DA_Separate_To_My_Own_Squad**
- **DA_Arrest_Target**
  - Causes the character to try and arrest the target by attacking them
    and sending them to a cell.
- **DA_Arrest_Targets_Carried_Person**
  - For bounties
- **DA_Attack_Town**
- **DA_Assign_Bounty**
- **DA_Crime_Alarm**
- **DA_Run_Away**
  - Causes the character to run away. Does not work on player characters
    \[Cattrina\]
- **DA_Increase_Faction_Rank**
- **DA_Lock_This_Dialogue**
- **DA_Assault_Phase**
- **DA_Retreat_Phase**
- **DA_Victory_Phase**
- **DA_Enslave_Targets_Carried_Person**
- **Choose_Slaves_Selling**
  - Opens a separate window shop with portraits of the characters in the
    squad's slave squad or choosefrom list
- **Choose_Slaves_Buying**
  - Opens a separate window shop with portraits of the characters in the
    squad's slave squad or choosefrom list
- **Choose_Prisoner_Bail**
- **Choose_Conscription**
- **Choose_Recruiting**
  - Opens a separate window shop with portraits of the characters in the
    squad's choosefrom list
- **Choose_Hiring_Contract**
- **Surrender_Non_Humans**
- **Choose_Animals_Buying**
- **DA_Clear_Bounty**
- **DA_Player_Sell_Prisoners**
- **DA_Player_Surrender_Member_Different_Race**
- **DA_Summon_My_Squad**
- **DA_Remove_Slave_Status**
  - NPC removing the status from the player character currently speaking
- **DA_Open_Nearest_Gate**
- **DA_Attack_Stay_Near_Home**
- **DA_Massive_Alarm**
  - Calls for all nearby NPCs of their faction to attack the target
  - Only characters with the same dialogue in their pack will respond
- **DA_Attack_If_No_Coexist**
- **DA_Knockout**
  - Knocks out the NPC in the dialogue. The value number is the length
    of the KO in seconds. \[LeCheech/Kodi Sky\]
  - Does not trigger hostilities if allies are near by. \[LeCheech/Kodi
    Sky\]
  - If done to an allied NPC and you have Help/Rescue allies set in your
    ingame squad AI, there will be an issue where your characters will
    automatically pick up the KO'd character on the ground, every time
    they are dropped a KO timer resets. To break out of the loop without
    changing your Squad's AI in settings, you can place them in a bed
    and they will instantly wake up. \[LeCheech/Kodi Sky\]
  - Untested but, common sense is this should only be used at the end of
    a conversation tree to avoid potentially unwanted side effects.
    \[LeCheech/Kodi Sky\]
- **DA_End**
  - No obvious effects when run.

# Editable Properties AKA Effect Conditions

- **AI Contract**
  - *“Activates the given AI package as a contract job, val0 is the
    number of hours it lasts for.”*
- **Change AI**
  - *“Permanently changes the AI package, doesn’t affect the AI
    Contract. BE CAREFUL, remember it will change the whole squad,
    slaves and masters. May want to use with DA_SEPARATE_TO_OWN_SQUAD”*

<!-- -->

- **Change Relations**
  - *“Adjusts the relations with the given faction by this amount.”*
    Player faction to any NPC faction. Cannot alter the speaker NPC's
    faction towards another NPC faction.
- **Crowd Trigger**
  - *“Triggers the given dialogue to start on all other squad members.
    Use this for things like group cheering, laughing, and war cries.
    Should usually be 1 liners. The number is % of squad members to
    trigger.”*
  - Both the triggerer and the triggered must have the dialogue in their
    packet. You can make the 'is leader == 0' condition if you do not
    want the leader to be triggered. Use 'is character' to trigger only
    characters using those chosen character templates. Cannot be used to
    trigger more events. Can trigger effects such as DA_JOIN_SQUAD_FAST.
- **Give Item**
  - *“Action: Give target this item. Will conjure the item out of thin
    air.”*
  - Will provide the player with a “received item” notification, even
    when the item was given to a NPC instead.
  - NPC can give to Player, Player cannot give to NPC and NPC cannot
    take from the Player \[Cattrina\]
  - Items such as weapons, armor, and limbs cannot be selected to be
    given (wearables), the only exception is belt slot items.
  - You can make a machine, that consumes an object and produces the
    reward, if you want to make quests. (remember to remove aggression
    on looters from the quest giver NPC) \[Cattrina\]
  - If you want to make a fetch quest. You can also make the "reward"
    for the quest to be to sell the item after completing the quest
    (showing the item to the NPC) rather than giving the player
    something. \[LeCheech/Kodi Sky\]
- **Has Package**
  - *“Condition: Has a specific dialogue package. Refers to speaker
    only, unless its on an interjection node.”*
  - Use to restrict the dialogue line to only some of its users (a
    dialogue can be added to several packages)
- **In Town Of**
  - *“Adds a condition: That we must currently be in town/base belonging
    to the given faction.”*
  - True when inside or near a town owned by the given faction
- **Interrupt**
  - *“If the player interrupts us with a talking event, this will be the
    conversation chosen. Reset at the end of conversation, or until
    changed.”*
  - Commonly used for characters that are trying to talk with the
    player, such as guards when they want to search you.
  - Use in monologues and bar talks. You can make a monologue loop and
    have an interrupt ON THE FIRST LINE of the loop to make an out of
    the loop when spoken to.\[Cattrina\]
- **Is Character**
  - “Condition: Is a specific character. Refers to speaker only, unless
    its an interjection node.”
  - Returns true with all the characters who are spawned from the same
    template. FCS says 'named' meaning unique, but that is false
    \[Cattrina\]
- **Lock Campaign**
  - \`“Essentially sets the campaign’s \[territorial\] setting to
    false.”
  - Does not affect on campaigns without territorial setting.
    \[Cattrina\]
- **Locks**
  - *“Locks the given dialogue, use for special cases when you gotta
    lock something?”*
  - Use with unlock to make elaborate dialogue trees where the
    communication with the NPC can evolve \[Cattrina\]
  - The dialogue to be locked needs to be also assigned to the NPC
    speaker who does the locking \[Cattrina\]
  - This will only lock the dialogue for the NPC that triggered it. So
    if you have multiple NPCs with the same dialogue tree, this will not
    lock it for all of them. This is the case even if it's the same type
    of NPC. This "limitation" actually has some very good applications
    when it comes to making "randomized" encounters from the same
    dialogue tree. *<small>To lock dialogues for other NPCs than the one
    that the player is speaking to, use dummy Relations/Faction and a
    Worldstate and make the worldstate a condition.</small>*
    \[LeCheech/Kodi Sky\]
- **My Faction**
  - *“Adds a condition: I belong to the given faction.”*
  - Use to restrict lines for characters of that specific faction or
    factions
- **My Race**
  - *“Adds a condition: My race is any of the given races. Multiple
    races are treated as an OR condition.”*
  - Returns true for the general race. So selecting hive prince, worker
    drone, or soldier drone will all return true regardless of which
    type of hiver the character is. Same situation for greenlanders and
    scorchlanders.
- **My Subrace**
  - *“My specific sub-race. Multiple races are treated as an OR
    condition.”*
  - Refers to NPCs only.
- **No Target Race**
  - *“Adds a condition: Target squad has NO member who is any of the
    given races. Multiple races is treated as an OR condition.”*
  - Subraces are treated as one
- **Target Carrying Character**
  - *“Adds a condition: Target is carrying a specific character. Refers
    to target.”*
  - AI target (not dialogue target) is used.
  - specific character template, does not have to be unique \[Cattrina\]
- **Target Faction**
  - *“Adds a condition: Target belongs to the given faction.”*
- **Target Has Item**
  - *“Adds a condition: Target has this item, or any of these items.”*
  - Items such as weapons, armor, and limbs cannot be selected (only
    exception is belt slot items held in inventory)
  - Items attached to gear slots cannot be detected, items need to be in
    the inventory slot or back bag.
  - PLAYER DIALOGUE OPTION LINE (speaker: T_TARGET_IF_PLAYER ): Returns
    true if any character of the player squad nearby has the item, does
    not need to be on the person who speaks \[Cattrina\]
  - NPC DIALOGUE OPTION LINE (speaker: T_ME): Returns true if the
    speaker PC has the item
- **Target Has Item Type**
  - *“Adds a condition: Does the target have an item of the same TYPE as
    this one (eg. narcotics, meds, food)”*
  - Items such as weapons, armor, and limbs cannot be selected
- **Target Race**
  - *“Adds a condition: Target squad has a member who is any of the
    given races. Multiple races is treated as an OR condition.”*
  - Subraces are treated as equals. If the greenlander is triggered, so
    is scorchlander. If you want to trigger them separately, use
    subrace. \[Cattrina\]
- **Trigger Campaign**
  - *“Triggers the given campaign, which will start after a random
    number of hours between val0-val1, val2 is %chance (is absolute
    chance, so if you list 2 things which total to less than 100, then
    there is a chance of nothing)”*
- **Unlock But Keep Me**
  - *“Unlocks the given dialogue, must be actually in the NPC’s dialogue
    package somewhere for it to work. Will NOT cause the dialogue to
    then become locked.”*
- **Unlock Campaign**
  - *“Essentially sets the campaign’s \[territorial\] setting to true,
    so doesn’t actually trigger it, just makes it possible.”*
- **Unlocks**
  - *“Unlocks the given dialogue, must be actually in the NPC’s dialogue
    package somewhere for it to work. Will cause THIS dialogue to then
    become locked. Used for conversations that progress to other
    conversations in stages.”*
  - Does not work for <empty> dialogue lines. There needs to be actual
    text to be spoken.
  - Use with lock to make elaborate dialogue trees where the
    communication with the NPC can evolve \[Cattrina\]
  - This will only lock the dialogue for the NPC that triggered it. So
    if you have multiple NPCs with the same dialogue tree, this will not
    lock it for all of them. This is the case even if it's the same type
    of NPC. This "limitation" actually has some very good applications
    when it comes to making "randomized" encounters from the same
    dialogue tree. *<small>To unlock dialogues for other NPCs than the
    one that the player is speaking to, use dummy Relations/Faction and
    a Worldstate and make the worldstate a condition. This type of work
    around is used in Vanilla to make Tinfist have a specific dialogue
    if you have joined the Rebel Farmers.</small>* \[LeCheech/Kodi Sky\]
- **World State**
  - *“Adds this world state as an AND condition. 1=true, 0=false”*

[Category:Modding](Category:Modding "wikilink")
[Category:Dialogue](Category:Dialogue "wikilink")