This page expands the dialogue guide, see the main page [](Dialogue_Structure_Overlook.md)

### Target options in Conditions



#### T_ME

The host NPC to whom the dialogue is attached to (owner of dialogue), is
always a NPC

#### T_TARGET

Can be a NPC or player, requires some trigger that determines the
target, fe. ev_see_neutral_squad.

Is the Player, if happened through ev_player_talk_to_me event

#### T_TARGET_IF_PLAYER

Specifies that the target is actually a player character. Handy when
doing broad scans like ev_see_neutral_squad

#### T_INTERJECTOR (1,2,3)

Makes interjector the target, please note that an interjector is seldom
a specific character as it is randomly (with conditions) selected from
the available NPCs around the speaker. Interjectors work only on free
speech (monologue, bar talk), they do not work in conversation dialogues
where player gets options.

T_TARGET_WITH_RACE

Should only trigger if the target is or is not a specific race, I have
not tested this

[Category:Dialogue](Category:Dialogue "wikilink")
[Category:Modding](Category:Modding "wikilink")