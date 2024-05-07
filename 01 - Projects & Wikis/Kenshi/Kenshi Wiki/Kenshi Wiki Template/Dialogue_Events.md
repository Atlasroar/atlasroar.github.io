This page is lists the various events connected to the [](Forgotten_Construction_Set.md) dialogue
system, along with some information about that event if available.

## Events

- **EV_Player_Talk_To_Me**
  - If the conditions for this dialogue are met, allows for the player
    to talk the this character by clicking on them. Can also be
    triggered by the "DA_TALK_TO_LEADER" effect.
  - ME is the character that the player is talking with. TARGET is the
    player
- **EV_Acid_Feet**
  - Triggers* *when a barefoot character walks in an acid biome
- **EV_Acid_Rain**
  - Triggers when a character without 100% acid resistance runs around
    in acid rain
- **EV_Acid_Water**
  - Triggers* *when a character without 100% acid resistance swims in
    acid water

<!-- -->

- **EV_Almost_Woke_Up**
  - Triggers only on NPCs and is used as a fluff
- **EV_Announcment**
  - Dialogue that is used for announcing arrivals of raids/visits to
    player bases. NPC only.
- **EV_Assassination_Failed**
- **EV_Bar_Talk**
  - Triggers only on NPCs, that are spawned inside a bar building
    (BD_BAR indicator in squad file), is used to create ambience
- **EV_Being_Healed_Finished**
  - Triggers on characters, who have just been healed by the player,
    sometimes on PCs who have been healed by a NPC
- **EV_Being_Healed_Start**
- **EV_Betrayal**
  - Triggers on an NPC when the player attacks after having made a
    contract with them, such as when hiring mercenaries.
- **EV_Bought_Me_From_Slavery**
  - Triggers on NPCs only, is used to play a reaction and possible
    joining to the player faction
- **EV_Bounty_Spotted**
  - Triggers in NPCs only, is used to react to player characters with
    bounty on their heads
- **EV_Burning**
  - Triggers in fire, lava and acid situations, a reaction with screams
- **EV_Contract_Job_Ended**
  - Triggers in NPCs only, when the contract AI timer has run to end,
    the dialogue in this slot will be triggered
- **EV_Crowd_Triggered**
  - Triggers from within some dialogue, fe. the leader's conversation
    with the player, or from a campaign (fe. assault stage). Triggers
    everyone owning the dialogue pack that has been called (meet the
    conditions).
- **EV_Eating_My_Crops**
  - Triggers when a character spots an animal in their field
- **EV_Eating_Something_Sounds**
  - Used by fogmen when eating.
- **EV_Enter_Biome**
  - This is used in player dialogue only and it triggers when the player
    squad first enters to a biome, only one event per biome and they are
    all already in vanilla
- **EV_Enter_Town**
  - Triggers* *upon entering a town or nest.
- **EV_Escaped_Ex_Slave_Spotted**
- **EV_Escaped_Prisoner_Spotted**
- **EV_Escaping_Slave_Spotted**
- **EV_FirstAid_Kit_Empty**
  - Triggers upon using the last charge of their last First Aid Kit
- **EV_Get_Up_Fight**
  - Triggers after being KOed, when a squadmate is still fighting
- **EV_Get_Up_Peace**
  - Triggers after being KOed, when there are no more enemies around or
    no squad members fighting
- **EV_Get_Up_Unneccessary_Fight**
- **EV_Give_Up_Chase**
  - Triggers in NPCs, when the attacker is running
- **EV_Harrassment_Shouts**
  - Used by the United Heroes when hurling insults at non-human players.
- **EV_Healing_Other_Finished**
- **EV_Healing_Other_Start**
- **EV_I_Defeated_Squad**
  - Triggers* *when a squad defeats another squad
  - ME is the character who made the final blow for the winning faction,
    TARGET is the character who was defeated. Typically the target will
    be KOed.
- **EV_I_See_Ally_Player**
  - Triggers when the character spots an allied player character.
  - ME is the character that spotted the player, TARGET is the player
    character that was spotted.
- **EV_I_See_Animal_Squad**
  - Triggers when the player squad has only animal characters. Some NPCs
    can join the Player squad when noticing only animals in a squad.
    This is to give the player the option to keep on playing even after
    all humanoids are dead.
- **EV_I_See_Enemy_Player**
- **EV_I_See_Illegal_Player_Building**
- **EV_I_See_Neutral_Squad**
  - Triggers once every second while a neutral character is spotted
  - ME is the character that spotted the target. TARGET is the character
    that was spotted.
  - Does not trigger while the ME character is imprisoned in a cage, if
    the target has been imprisoned, or if the target has been knocked
    out.
- **EV_I_See_Player_Nice_Building**
- **EV_I_See_Ragdoll**
  - This event is redundant, does not trigger

<!-- -->

- **EV_I_See_Uniform_Imposter**
  - Triggers when the player character is wearing an uniform piece of
    the NPC's faction. It is used to 'notice a strange face among my
    kin'. Does not trigger in other factions, only in the faction the
    uniform belongs to.
- **EV_Introducing_New_Slave**
  - Is used as a fluff, triggers when a player is nearby and the slave
    caravan has reached its destination
- **EV_Intruder_Found**
  - Triggers when a house is set as non-public or after closing time of
    a shop and the player is still inside. Is used to shush the player
    away from the building, usually results in an alarm
- **EV_Kidnapping_My_Ally**
  - Triggers when the ally NPC is picked up by an outsider/not ally of
    the faction, even if the intention is to put them on a bed to heal.
- **EV_Launch_Attack**
- **EV_Looting_Everything**
- **EV_Looting_Weapon_Only**
- **EV_Lost_Arm**
  - Triggers when an arm of the character has fallen to the ground, does
    not trigger on -100 hp, only if it is separated
- **EV_Lost_Leg**
  - Triggers when a leg of the character has fallen to the ground, does
    not trigger on -100 hp, only if it is separated
- **EV_Marked_For_Death**
  - Triggers when the character is in a cannibal cage or similar and has
    been selected to be the next one killed.
- **EV_Poison_Gas**
  - Triggers* *when a character without 100% gas resistance enters a gas
    cloud.
- **EV_Prisoner_Free_To_Go**
- **EV_Recapturing_A_Slave**
- **EV_Screaming_Torture**
  - Triggers when a character is being tortured. (Cannibals, Fogmen,
    Peeler)
- **EV_Shoo_From_My_Building**
  - Triggers* *when a shop is about to close and the player is still
    inside.
- **EV_Shout_At_Slave_Worker**
- **EV_Slave_Delivery**
- **EV_Slave_Escape_Opportunity_Alone**
- **EV_Slave_Escape_Opportunity_Savior**
- **EV_Sound_The_Alarm**
  - Response to the alarm
- **EV_Speech_Interrupted_Attacked_By_Strangers**
- **EV_Speech_Interrupted_Attacked_By_Target**
- **EV_Squad_Broken**
- **EV_Taken_Over_Player_Town**
- **EV_Thief_Caught_Stealing_From_Me**
  - Triggers when an NPC catches the player stealing from them.
- **EV_Unlock_My_Cage_Attempt**
- **EV_Unlock_My_Cage_Or_Shackles**
- **EV_Using_My_Training_Equipment**
- **EV_Windy**
- **EV_Witness_Generic_Assault**
- **EV_Witness_Looting_Ally**
- **EV_Witness_Thief_Or_Lockpick**
- **EV_Worshiping_Something**
  - Used by fogmen.

[Category:Modding](Category:Modding "wikilink")
[Category:Dialogue](Category:Dialogue "wikilink")