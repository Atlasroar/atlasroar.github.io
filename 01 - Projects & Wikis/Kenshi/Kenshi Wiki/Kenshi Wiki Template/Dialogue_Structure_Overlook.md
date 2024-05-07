by Cattrina

# Forewords

The dialogue system is the 'scripting' us modders have for Kenshi. It is
by no means perfect or even sufficient enough to actually do anything
one wants, but it's the one we got.

### Limitations

- Cannot do actual scripting, only has a limited set of premade enums,
  effects and conditions
- Cannot add custom effects, conditions or enums
- Condition set up is a bit iffy, cannot rely on those conditions
  working 100% of the time
- Triggers are also iffy, won't trigger reliably
- The player faction is always considered a whole in conditions, so it
  is not 'is this player character currently speaking kind' it is rather
  'does the player squad have this personality character among them'
  regardless if they are currently speaking to the NPC or not. Same with
  items.

Some of the limitations are, in no doubt, because of the one-thread
engine of the game. Meaning it cannot keep up if multiple things are
happening at once, which results the engine dropping some of the
'fluff'.

**Lesson no 1:** Keep your dialogue trees simple. It is not just easier
for you to bug hunt, but it is also easier on the engine and results in
less drop outs. Use loop-backs sparingly, never make an unending loop.

### Features (aka tips what you can do in the dialogue tree)

- A dialogue line can be referenced multiple times (script loop-back)
  **by holding shift and dragging the line under another line** you want
  to loop back from. The 'to', is dragged under the 'from'.
- Three kinds of dialogue types possible (read more below): conversation
  with a player, bar talk and monologue
- A dialogue can unlock and lock other dialogues the **current speaker
  NPC has in their dialogue pack.** This can be used reliably in
  conversation, but does not trigger reliably on monologues or bar talk.
  A NPC cannot lock or unlock dialogues they do not have in their pack.
- A dialogue is used to trigger and change AI events, do trigger on
  monologues and bar talk
- All lines connected to the same previous line (branches from the same
  trunk) are treated as equal, unless a line has conditions. When a NPC
  speaks, a random line from the equal valid options is chosen. The
  player gets to pick from all the options available where conditions
  are met. If a condition is not met, the player does not see that
  option in game.

### Looking for a specific line to study or replace?

Use this guide: [](How%20to%20Find%20Specific%20Dialogue.md)

# Dialogue types

### Bar talk (interjectors)

A bar talk is a 'monologue' with two or more NPCs, typically in a bar.
It does not involve the player. It triggers when a player character
arrives in the vicinity of the host NPC. It uses the
EV_I_SEE_NEUTRAL_SQUAD, the EV_BAR_TALK trigger is not used. It is meant
to give background information to the player or just to create ambiance.
The dialogue is written in one dialogue window with interjectors as
speakers. An interjector is chosen randomly amongst the squad members,
who meets the conditions given, of the host. It is possible no NPC gets
triggered, which will make the entire bar talk fail. If the talk is
important, use 'is character' as interjector condition and make sure
they get spawned to the bar (see [Creating New Towns#Step 4: Interiors
and
Exteriors](Creating_New_Towns#Step_4:_Interiors_and_Exteriors "wikilink")).
![](Example_of_Bar_talk.png "Example_of_Bar_talk.png")**When to use**:
Use bar talk whenever you want two or more NPCs to talk to each other.
Examples of use: bar patrons discussing changes that happened by the
player action (Bar patrons random faction comment on world state)

### Conversation

The main dialogue type, where a pop-up window opens and the NPC and the
player portraits appear. Has all functions available. Triggers either by
the player clicking on the NPC possessing the dialogue pack, or via
sight of a squadmate, who then prompts talk to leader effect, which then
opens EV_PLAYER_TALK_TO_ME. Always under EV_PLAYER_TALK_TO_ME.

A three or more person conversation is possible within player
conversation, see [](Three%20Person%20Conversations%20with%20Player.md)

See our script library here: [Script Library](Script_Library.md "wikilink")

See here Boron's marvelous dialogue making guide: [Kenshi Modding 101:
FCS and
Dialogue](https://steamcommunity.com/sharedfiles/filedetails/?id=1444279946)

### Monologue

Single NPC talking alone, usually prompting the player to talk directly
(conversation) to the NPC. It can be triggered by sight, by campaign or
by the player engaging with NPC-owned items (stealing, training dummies
etc.). Is a response or a lure, can trigger campaigns.
![](Example_for_Monologue.png "Example_for_Monologue.png")**When to
use**: use monologue when you want to make the NPC to speak at the
player, without forcing them in conversation. Example uses: prayer day
announcement (Priest announce), Beep sees player for the first time
(beep following), bartender welcoming patrons (shop welcome customer).

If you are making a looping monologue, make sure to add the
PLAYER_TALK_TO_ME dialogue as an interrupt on the first line of the
dialogue. Otherwise the loop continues on forever. The interrupt option
is on the right side drop down menu of the effects.

*"Oh boy, how one wishes the prayer day would force you into
conversation, being a monologue makes it so easy to miss!"* -you,
probably

# Triggers/Events

A trigger is the initial event, that starts the dialogue-AI-event-tree.
Starts events in motion, if you will. They are selected from the left
hand list of the dialogue pack window and are marked with the nominator
EV in front. Requires a loaded region (aka player character present
nearby). There are several different triggers, some of them requiring
other conditions to be met as well. See; [](Dialogue_Events.md) for more info.

1\) First, and easiest to learn for a newbie modder is the
EV_PLAYER_TALK_TO_ME. It is self-explanatory. If the player right-clicks
the NPC, a conversation is triggered. **Pre-requisite**; a dialogue
package with unlocked player talk dialog option has to be assigned
either on a squad- or on a character level to the NPC. Also all/at least
one conditions set to the dialogue must be met.

2\) EV_SEE_NEUTRAL_SQUAD (also SEE_ALLY_PLAYER and SEE_ENEMY_PLAYER)

This is the most 'dangerous' of the triggers, game engine burden wise,
and must be carefully thought of. You see, this is a **scanner,** which
returns true every time it hits a character, being it an NPC or PC. And
the ray is sent multiple times a second. **It is very important** to set
up as many conditions that apply as possible, to restrict the flood of
positive returns, as they can **lag** the engine and cause frame rate to
drop. Luckily this is a **cone**, and not a sphere, locked to the
character's vision field. Requires an unlocked dialogue set to the
dialogue pack's see neutral slot and the dialogue pack assigned to the
NPC, either on squad or on character level. Also all/at least one
conditions set to it must be met. See ally and see enemy just add
automatic detection if the player is either of those, never triggering
on NPCs, and thus making them slightly lighter burden wise.

Use the EV_SEE_NEUTRAL_SQUAD with the condition T_TARGET DC_IS_PLAYER ==
1 to restrict the scanner to player characters only.
![](DialoguePackageSeeNeutralConditions.png "DialoguePackageSeeNeutralConditions.png")3)
EV_USING_MY_TRAINING_EQUIPMENT

The training dummy with the function BF_TRAINING, must be in the same
town the NPC is, and the ownership of the town must belong to the same
faction the NPC belongs to. The NPC also needs to be on the same side of
the building the dummy is, in or out. And the usage must align with the
NPCs cone of view (the NPC must witness the happening).

And as always, the unlocked dialogue must be set to the correct slot in
the dialogue pack and the pack assigned to the NPC either on squad or
character level. And all/at least one conditions met. This will trigger
the dialogue only, if you want the NPC to react, they also need the
corresponding AI pack and goal, which can be switched on (change AI) via
dialogue, or it can be on always.

4\) EV_CROWD_TRIGGERED

Is triggered by a dialogue event, usually from a conversation (effect
condition crowd trigger), but can be also triggered from bar talk or
monologue. A monologue goes in its slot. Something like 'wohoo'. It can
be longer, but I have not been able to make this crowd triggered
dialogue to trigger anything else (except DA_JOIN), so end of a tree
branch.

You can use this to make a random (or selected with conditions)
character or several all at once, from the NPC's squad, to join the
player faction. Use only DA_JOIN_SQUAD_FAST, cause if you have several
people join, only the first will get the editor and it is possible the
joining for others fails.

Do note, if the leader joins, the my squad is broken event is triggered
and a new leader is chosen, often resulting the crowd trigger chain to
be broken and the conversation starting all over again. Make the leader
join last by using T_ME DC_IS_LEADER == 0 on the squad line and another
line for the leader with T_ME DC_IS_LEADER == 1 and DC_SQUAD_SIZE == 1.

And naturally, the unlocked dialogue must be set to the correct slot in
the dialogue pack and the pack assigned to all the NPCs to be triggered
either on squad or character level. And all/at least one conditions met.

# Booleans

Now as an avid aspiring coder your ears perked up, amIright? *"Booleans
oh boy, the good stuff!"*

Well, technically Kenshi does not have booleans, nor it has global
values you can change and compare against from inside a dialogue. What
we have is *faction relations, world states, items and fake factions*
(the latter which is the smart way, but the others have their uses).

### Using Real Faction Relations as Boolean

There are some set backs to using faction relations as boolean; it
cannot be changed in secret, there will be an announcement in game when
the player gets allied or removed as an ally. Also it fluctuates by
happenings in game. And you cannot really build any relationship with
the faction, when it needs to reset to zero to keep the script working.

It is 'ally', 'enemy' and 'neutral' to the faction of the NPC (you are
talking with) you can compare against. So one faction, four booleans: is
ally/is not ally, is enemy/is not enemy. So it is recommended to always
have two conditions on the same dialogue line, to condition both; fe. to
check if player is neutral: T_TARGET_IF_PLAYER DC_IS_ALLY ==0 and
T_TARGET_IF_PLAYER DC_IS_ENEMY ==0

**So how does this works in a dialogue?**

A scenario:

Player clicks on the salesman:

<table>
<tbody>
<tr class="odd">
<td><p><strong>Bull salesman</strong>: Welcome customer! Do you want to
buy a bull?</p>
<p><strong>Player:</strong> "Yes, I would like a bull, here's the money"
DA_TAKE_MONEY 6000</p>
<p><strong>Bull salesman</strong> "Excellent, thank you" effect
condition; change relations with <em>bull salesman faction</em> with
+100 (makes ally)</p></td>
</tr>
</tbody>
</table>

Player clicks on the bull, after talking to the salesman:

<table>
<tbody>
<tr class="odd">
<td><p><strong>Bull</strong>(<em>bull salesman
faction)</em><strong>:</strong> Line 1: (checks if player is ally)
T_TARGET_IF_PLAYER DC_IS_ALLY ==1: "Moo" effect condition; change
relations with <em>bull salesman faction</em> with -100 (removes
ally)</p>
<p>Line 1:2 Player input: "You are mine now"</p>
<p>Line 1:2:1 (check if we are still allies) T_TARGET_IF_PLAYER
DC_IS_ALLY ==1, change relations with <em>bull salesman faction</em>
with -10 loop back to 1:2:1</p>
<p>Line 1:2:2 (check if we are still allies) T_TARGET_IF_PLAYER
DC_IS_ALLY ==0; DA_JOIN_SQUAD_FAST</p></td>
</tr>
</tbody>
</table>

Now while you can change the faction relations value by smaller amounts,
you cannot really control the fluctuation of it. Small things can affect
it, stealing, fighting, healing, trespassing. It is far easier to deal
with is ally, is not ally, than 'if faction relations \> 10'. But you
can, if you need to. Unfortunately we cannot reset the relations
directly to 0 (that would be great), we need a back-loop checking we
definitely went under ally range (50+) and taking small increments off
until we are under it before the bull joins. Carefully, not to go over
to the enemy range (varies what each faction thinks an enemy is, you
should set yours according what you need).

You might also want to set up a pacifier or something else to counter
for the happenstance if the player starts a fight with your bull
salesman faction and makes themselves an enemy to the faction. That
would break the bull sales boolean from operating. Unfortunately a NPC
can only check against their own faction. They can alter relations to
other factions, but they cannot check what the other faction relations
value to player is (Using the main conditions set up, see fake factions
below). They cannot even check their own faction's status against
another faction when they are talking to the player. They can check
their own faction's relations to other NPC's factions if the target is
the other NPC. So while targeting player, no checking other NPC factions
(with main conditions window).

### Using Other World States as Boolean

Another boolean type we have is world states. These are eternally linked
to certain unique NPCs and their statuses as 'imprisoned' or 'alive'. Or
a town's similar status. And as such cannot really be toggled on or off
from inside a dialogue, oh no, these need to actually happen in the game
world.

World states, however can alter the game world drastically! A death of
the faction leader of the Brismotheens and poof now the town of Brismoth
is owned by the Swamp Ninjas, who were their enemies. While the player
was away... Below an actual in game example: When Seta, Esata and
Valtena are dead, and Tengu and Longer are alive, Bad Teeth, which used
to belong to Holy Nation, has changed owners to the UC.
![](TownOverrideBadTeeth.png "TownOverrideBadTeeth.png")What comes to
dialogue making, you can use these wold states to prompt up new and
interesting dialogue options. Make your bar talks to reference them!
Players love when their actions are under the gossip! Make your
bartenders show respect and your shop vendors to venerate the player.
They have heard the gossip and now they are giving the proper
acknowledgement to the player.

### Checking against items in inventory

Another boolean you can use is if the player squad has a certain item in
their inventory. The item must be of item type and not an article of
clothing or weapon. The only exception to this is belt slot items,
however they cannot be worn while checking against, they must be in
inventory. Item needs to be in main inventory not in a back bag.

**How to use**: The NPC can check if the player squad has fe. the Holy
Flame book before unlocking a line of dialogue.

Unfortunately the NPC cannot take items, they can only give non-wearable
items, and check player inventory. And that is *the entire Squad's at
once*. It is enough one PC has the item, the speaker need not to have
it. It makes hiding contraband items in your friends pockets while the
guard checks your bag a bit difficult XD

There is no option for 'has not' you must make sure you have all the
other dialogue options designed so they'll work when the player does not
have the item, and only have special result for the situation when they
have the item. However you can unlock and lock dialogues for the effect
they already had the item. So have dialogue 1 for the events 'characters
hear about this item the first time' and dialogue 2 'we have the item',
which starts as locked.

Then you can lock dialogue 1 and unlock dialogue 2, where the NPC knows
they have(d) the item. Thus if they do not have it now, maybe they put
it in a box I indicated. Naturally nothing prevents the player from
dropping the item on the ground and then just picking it up later. Just
make the item utterly useless and worthless so the player has no need
selling it. Dialogue 1 being now locked forever, every time the player
clicks the NPC, they get the dialogue 2, unless you make a dialogue 3 to
be unlocked... If two or more dialogues are unlocked at the same time
and their conditions are met, the game chooses one randomly (Altho
experience has taught me it usually is the first option top of the
list).

See **Target Has Item** for more info on [](Dialogue_Conditions_&_Effects.md)

### Using Fake Factions and Faction Relations World States as Boolean

Now this is the best boolean we have, characters in dialogue can check
against it and it does not matter what the NPC's own faction's status is
to player faction (unless they are hostile). And as the fake faction
does not actually have any characters or towns, the relations do not
fluctuate by in game happenings at all.

It requires a bit hassle to set up; you have to make a fake faction and
the corresponding (two) world state(s) per each boolean you need,
because using the same boolean in every conversation would defeat the
purpose.

If you keep proper documentation for yourself, or you can keep track of
many things at once in your head, technically you could set different
numerical values to every status, fe. 'is enemy' could mean five in your
script, 'neutral' 10 and 'ally' 15. You would use this fe. in bull
selling situation to determine how many bulls the player paid for. Or,
if you use several fake factions you could have as many values you need
(naturally each value would require a line of dialogue each). As said,
this gets quite complicated the more booleans you have, as you need to
keep track on which line you change the value and make sure all booleans
get reseted after the transaction is over.

Yes, you still need a 'is ally' == 1 change relations; Boolean Bull
Sales is Ally -10 loop for every boolean you used up in this
conversation, to make sure each value gets reset. Not because the
faction relations to a fake faction fluctuates, but because you are
human and there might be a line that you did not set right and because
of that mistake, the ally value keeps on adding up instead of
resetting... and it just is good practice to plan for failures.

However proper resetting gets very difficult when you have multiple
booleans in operation. Sometimes one just have to trust to oneself and
hope all values are reseted correctly after each transaction.

And yes, the player will get a notification in game whenever the status
of a fake faction is changed.

**Setting up:**

1\) Create a new faction, name it so you remember what function it is
for. Fe. I am making one for bull selling, so I name it 'Boolean Bull
sales' (it is good practice to have them all be sorted in a row
alphabetically, so you see them all with one glance on the faction list.
You can make it not real:TRUE, although it does not matter much as this
faction will never get any people you can crime against. None of the
values matter, you only need the name.

2\) Create two world state files, one for is ally and one for is not
ally (remember neutral is an option, so you need both).

To make is ally world state: Select 'player ally' from the drop down
menu and pick the boolean fake faction you just created and keep the 1
after it

To make is NOT ally world state: Select 'player ally' from the drop down
menu and pick the boolean fake faction you just created and change the 1
to 0.![](SettingWorldStateBoolean.png "SettingWorldStateBoolean.png")

Optionally you can make just one boolean, and use the 0 and 1 in the
dialogue line to toggle it on and off, see How to use below. Just mind
the three options (ally, not ally, neutral).

**How to use:**To use this on a dialogue line, select the line and then
the World State condition boolean on the right drop down menu and pick
the correct version of your boolean world state.
![](WorldStateBooleanUsage.png "WorldStateBooleanUsage.png")

In this example we use the negative of Not Ally to make it a
double-negative == is ally. If you use this method, you really only need
one world state 'is ally' per fake faction.

However I find it easier to have two, ally and not ally, so both can be
1 (which is default when adding) so I can't mess it up by forgetting to
change it to 0. Use whatever method works best with your brain.

**How to change the value of the world state** (to make the fake faction
ally or not)

In the dialogue line, just add the 'change relations' effect condition
on the right drop down menu, pick the fake faction in question and a
value change you want after it. '-100' = reduce 100 from current value.
'100' = add 100 to current value. If the value starts on 0, -100 makes
it an enemy and +100 would make it an ally. Ally limit is the same (+50)
to all factions, but enemy limit can be set separately per faction. TIP:
you can change several relations at once.

For example:

<table>
<tbody>
<tr class="odd">
<td><p>Bull salesman: "How many bulls you want to buy?" Player
options:</p>
<p>"One" DA_TAKE_MONEY 6000 change faction relations; Boolean One Bull
+100, Boolean Two Bulls 0, Boolean Three Bulls 0, Boolean Four Bulls
0</p>
<p>"Two" DA_TAKE_MONEY 12000 change faction relations; Boolean One Bull
0, Boolean Two Bulls +100, Boolean Three Bulls 0, Boolean Four Bulls
0</p></td>
</tr>
</tbody>
</table>

And in the bull's dialogue (all bulls in the squad have this same
dialogue):

<table>
<tbody>
<tr class="odd">
<td><p>Bull:</p>
<p>Line 1: Condition Boolean One Bull == 1 "I am bought" change faction
relations; Boolean One Bull -100 DA_JOIN_SQUAD_FAST</p>
<p>Line 2; Condition Boolean Two Bulls == 1 "I am bought" change faction
relations; Boolean Two Bulls -100, Boolean One Bull +100
DA_JOIN_SQUAD_FAST</p>
<p>Line 3: Condition Boolean Three Bulls == 1 "I am bought" change
faction relations; Boolean Two Bulls +100, Boolean Three Bulls -100
DA_JOIN_SQUAD_FAST</p></td>
</tr>
</tbody>
</table>

# Word Swaps

When you start modding dialogue and opening vanilla dialogues to see how
everything is done, you bump into lines that look like this; /MEUS/,
/HELLO/. These are word swaps. There is a corresponding swap dialogue
under the word swap tab with the same caps as a title. The game engine
replaces the /INSERTYOURSWAPNAMEHERE/ with a single dialogue line picked
up from the INSERTYOURSWAPNAMEHERE file according the conditions you
set. A word swap can be just one line with multiple options, or
elaborate condition tree for as many situation you want. On one dialogue
line in the swap you can have as many sentences you can have with a
normal dialogue line. One word trigger, but the result can be quite
long.

**Limitations**

- word swaps cannot be used as a condition, you can use conditions in
  them, but the result of a swap cannot be used as a condition
- you cannot save a swap result. The next time you use the same swap a
  new result is randomized again from the options available according to
  the conditions set.

**Word swaps are used to:**

**1) To specify how the character refers to their squad, or their gender
in plural or in single format.**

Fe. MEUS is used like this:

NPC: "Hi, I was wondering if you might have some work for /MEUS/ in your
town?"

The MEUS word swap file has two lines. On line 1 there is 'me' and on
line 2 'us' with the condition T_ME SQUAD_SIZE \> 1. Not having a
condition on the line 1 means both options are available when there is
more than one character in the squad. The choice is made randomly. An
alone character cannot refer themselves as 'us' using MEUS. You need to
make a new swap for that without the condition, or just type the us
directly on the dialogue.

So in game the player never sees the /MEUS/ written, they would see
either 'me' or 'us' depending on the NPC's squad size.

There are already set up swaps for I vs. we IWE, I am vs. we are IWEARE
and many many more! Use them on your dialogue.

All the non calculation ones are found under the word swap tab.
Alongside them the following swaps are used. These require some code to
work, so they are inbuilt to the game code:

- /MYNAME/ - Displays current speaker’s name
- /YOURNAME/ - Display’s current target’s name
- /TARGETFACTION/ - Displays current target’s faction
- /PLAYERFACTION/ - Display’s player’s faction name
- /COST/ - Displays value used in conditions for that dialogue line

**2) To make the conversation to <u>have varied</u> <u>synonyms</u> or
sentences so dialogues that will repeat many times would have a bit of
variation.**

Fe. /HELLO/ has several different greetings, just under a single line
there without conditions. The engine just picks one each time. In my
Random Joiners mod I use this type of swap to give flare to a
conversation, by listing different types of attackers a NPC might have
survived from. I have listed animal and faction names there, as well as
'bandits', 'outlaws' and 'slavers'.

|                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NPC: \[ the /MANWOMAN/  looks around /HIMHER/ suspiciously\] "/IWEWERE/ attacked by /RANDOMATTACKER/ a bit ago, I am pretty sure they did not follow /MEUS/. Could /IWE/ maybe recuperate here a while? Please? /IWEARE/ desperate!" |

If you need to refer to the same attacker more than once you need to
make the conditions so the same option will be picked. This might be
hard to do, so easiest is just to refer them once and use the
'they/them' to refer to them again later.

**3) To give either speaker's or target's personality or location based
answers**

This is to aid your dialogue to be clean. If you want different
personalities to have different words used, you set up a swap so you do
not have to make a line for each variation on the actual dialogue. This
way you can be sure all variations will have the exact same next step,
be it a player's reply or an event. If you had several line options (one
per personality) you might by accident forget to add the next step to
it, thus creating a bug.

How to use:

Fe:

Line on dialogue: "I do not care /PERSONALITYMUCH/ about your crops"

The choices in PERSONALITYMUCH file could be:

Line 1: T_ME DC_PERSONALITY_TAG == 1 PT_WARM_KIND "a lot"

Line 2: T_ME DC_PERSONALITY_TAG == 1 PT_COLD_CRUEL "a fuckton"

etc.

If you wanted the player to use those options, you would make it to have
T_TARGET_IF_PLAYER instead. T_ME refers always to the NPC speaker.

**4) To allow multiple dialogue branches to end up with the same varied
ending, without using a loop-back (see features on top).**

# Targeting

Targeting is important for the AI to be able to determine on what the
action should be directed against. You cannot change the target for AI
from inside a dialogue. The target is always chosen **via the trigger
event.** Target inside a dialogue is used to determine which side
conditions to be checked against, player side or NPC side. There is
never a third option.

The EV_PLAYER_TALK_TO_ME event will always set the player character
currently selected, as the target for the AI. The EV_I_SEE events can
target also NPCs, so if you use one, make sure to direct it to the
player with the condition T_TARGET_IF_PLAYER or DC_IS_PLAYER == 1.

Do note, that if you set your target with EV_I_SEE_NEUTRAL_SQUAD and
T_TARGET DC_IS_PLAYER == 0 you will get multiple positive hits a second
and might not get the exact NPC as target you wanted. Fe. it might
actually take the police as target where you wanted the criminal to be
targeted. So careful condition set up needed (you can use 'is character'
as a condition). All NPC vs. NPC interaction also requires an active
region ie. a PC nearby to happen.

In dialogue targeting is used mostly to specify which side conditions we
are looking at, the speaker NPC, or the player squad. Target for AI is
not the same thing as target in conditions for dialogue. In dialogue the
player target is always the entire squad. But for the AI events, the
target is the PC currently speaking.

So it is not 'is this player character currently speaking kind' it is
rather 'does the player squad have this personality character among
them' regardless if they are currently speaking to the NPC or not. So if
your player has all kinds of personalities in their squad, all
personality options would always be available when talking to the
speaker NPC.

See also [Dialogue Targeting](Dialogue_Targeting.md "wikilink")

# Text formatting

One can only use color to make dialogue text emphasis. See [](Dialogue_text_formatting,_colors,_italics_etc.md).

# Conditions and Effects

See [](Dialogue_Conditions_&_Effects.md)

# Glossary

|                                            |                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Branch**                                 | In scripting a dialogue, a branch is the (unique) follow up of a dialogue option, a path. It can branch onwards, but it usually has its unique ending. **A branch must either have an ending or it has to loop back.**                                                                                             |
| **Dialogue pack, Dialogue, Dialogue line** | Dialogue pack is the main file with all the triggers, it contains all the dialogues for all the characters who use the same pack. A Dialogue is one dialogue window which contains the actual writing of the piece. A Dialogue line is one step on the path, one entity of speech.                                 |
| **Dialogue tree**                          | The map of paths/branches the conversation can take. All the options, all the results. It is traditionally contained in one dialogue window, but in complex scripting a dialogue tree can amass several dialogues, each locked and unlocked in turn.                                                               |
| **Host**                                   | The NPC who has the dialogue pack (or single dialogue) on their file. Usually a leader, but can be any squad member, prisoner or slave.                                                                                                                                                                            |
| **Interjector**                            | A randomly chosen (conditions apply) NPC from the host's squad file, to say pieces of conversation in the middle of a host's monologue. Is used to make the monologue to look like a conversation for flare.                                                                                                       |
| **Line**                                   | In dialogue, a line is one set of speech spoken at once by one speaker (Player or NPC). A line can branch out to have more branches, have a single row of single lines following it (alternating speakers) or it can be the end of a branch (or to loop back).                                                     |
| **Loop back**                              | The branchline has ended without conclusion, so a loop back to an earlier option is added. Meaning the player gets to see the chosen line of dialogue again, and maybe follow a different path this time. Hold shift and drag the earlier line under the last line of the branch.                                  |
| **Root/Trunk**                             | In scripting a dialogue, the root of the dialogue is the word 'dialogue' on the beginning of a dialogue window. On word swaps it is the word 'Word Swaps'. A trunk is any line of the main bunch of options, more important than a branch. A dialogue tree can have several trunks or branches, but only one root. |
| **Scripting**                              | In Kenshi, the act of writing a dialogue with AI effects and condition syntax, thus making the dialogue more akin to coding than just mere creative writing. It's all scripting in Kenshi, a piece of dialogue is never just dialogue, you always set at least some conditions.                                    |
| **Slot**                                   | Not an official term. I use it with events/triggers to emphasize the fact there is space for several dialogues under the tab of each event. Click open the event and you see the 'slot'.                                                                                                                           |
| **Trigger/Event**                          | These are used interchangeably. Technically an event is the action that triggers the dialogue. You can find the triggers on the left of a Dialogue Pack. In front on a trigger's name is 'EV_'. A line in dialogue can cause an event AKA trigger next dialogue tree or an AI event.                              |

[Category:Modding](Category:Modding "wikilink")
[Category:Dialogue](Category:Dialogue "wikilink")
[Category:Guides](Category:Guides "wikilink")