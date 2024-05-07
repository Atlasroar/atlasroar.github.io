


This page explains how the goals in [](Forgotten_Construction_Set.md) AI system work, along with
lists of relevant information, if available.

## AI Goals

**AI Goals are the specific actions a character can take.**

**They can be given to the actor via squad AI Packages, the race menu, character menu, AI contracts, or the “change AI“ dialogue effect.**

---


## Classification

**How important is this action?**

- Urgent
  - Eg player orders, combat, first aid.
- Non-urgent
  - Eg sleep, eating, surgery. The stuff you don’t consider on the
    battlefield.
- Fluff
  - Ambient stuff that achieves nothing eg chatting.
- Just Action
- Obedience
- Max Size

## Ending

**What happens when the task is completed? Does it get removed for
myself, the whole squad, or does it remain active?**

- Nothing
  - This is what the vast majority of goals use.
- Remove Mine Only
  - As an example, this is used by the "Run away!" goal.
- Remove Whole Squads
  - As an example, this is used by the "Assault on Target Squad" goal.

## Targeting

**Who to use the action on. For example, do you heal yourself or someone
else?**

- Target Specific
  - TARGET is chosen either by the AI package's signal function or the
    AI goal's enum, depending on the enum
- Target Self
  - Character does the action on themself
- Target Leader
- Target Squad Mission
  - TARGET is whoever is the target of the AI contract
- Target Home Gate
  - TARGETS the gates of the current town.
  - Used for gate guards. Can also be used with their respective enums
    to dismantle or repair the main gates.

## Enums

**Actions that can be taken by NPCs and/or player characters.**

Tip: You can quickly cycle through enums by typing the first letter of
the enum that you want to find.

- Null Task
- Move on Free Will
- Build
- Pickup
- Melee Attack
- Focused Melee Attack
- Equip Weapon
- Unequip Weapon
- Find Weapon
- Choose Enemy and Attack
- Choose Attacker of Ally
- Attack Character’s Attacker
- Player Talk To
- Attack Attackers Of
- Idle
- Protect Allies
- Attack Enemies
  - Attack enemies when they are spotted.
- Protection
- Raid Town
- Go Homebuilding
- Stand At Shopkeeper Node
- Attack Enemies and Neutrals
  - Causes the character to start attacking any enemy or neutral
    character in sight.
- Patrol
  - Character patrols around the area. Used with the Start_Patrol signal
    function by AI packages.
- Attack Town
- Wanderer
- First Aid Order
- Loot Target
- Crouch
- Stand Up
- Move Cus Ordered
- Hold Position
- Stay Close to Target
- Self Preservation
  - Character reacts to charging enemies once they get close.
- Quell Aggression
- Attack Trouble Makers
- Run Away
- Patrol Town
- Wander Town
- Stand at Guard Node Homebuilding
- Wandering Trader
  - Character will move at a walking pace towards nearby villages and
    towns. Used with the Wandering_From_Town_To_Town signal function by
    AI packages.
- Get Near To
- Attack Enemies of My Slavemaster
  - Makes slaves fight for their enslavers during combat, such as with
    the Reavers.
- Not Be Unarmed
- Stay In Home
  - Character stays at home, occasionally interacting with some, but not
    all, types of machinery.
  - When the character does interact with machinery, it will produce
    gear if the input resources are put into it.
- Follow Player Order
  - Character will follow the TARGETED person
- Bodyguard
- Chase
- Stand at General Node
- Stand at Defensive Node
- Stand at Building Guard Node
- Stand at Building Defensive Node
- Stand at Node
- __aoeu__
- Travel to Target Town
  - Travel to the TARGET if it is a town.
- Rest
- Recruit at Jobcenter
- Switch Follow Me Mode On
- Job Repair Robot
- Job Medic
- Get Ready for Action
- First Aid Robot
- Unprovoked Focused Melee Attack
- Stand Still
- Squad Wait For Me
- Make Target Stand Still
- Get Up
- Force Get Up
- Move On Free Will Fast
- Lift Person
- Put Down Object
- Put Down Character in Bed
- Add Material to Building
- Open Door
  - Open the door TARGETED by the goal
- Close Door
  - Close the door TARGETED by the goal
- Open Door Here
- Close Door Here
- Pick Lock
- Lock Door
  - Lock the door TARGETED by the goal
- Unlock Door
  - Unlock the door TARGETED by the goal
- Bash Door
- Move to Building Door
- Move to Current Location Building Door
- Open Door for Current Location
- Open Door for Destination
- Open Up Shop Doors
- Operate Machinery
- Deliver Resources
- Job Keep Everything Running
- Unjam All Machines
- Unjam Machine
  - Allows NPCs to take resources out of machines when the output is
    full. Does not work with slaves.
- Collect Output Resource
- Fill Machine
  - Allows NPCs to fill machines with their input resource.
- Want to Fill Machine
- Repair
  - Repair the building TARGETED by the goal, such as damaged gates.
- Dismantle
  - Dismantle the building TARGETED by the goal.
- Use Training Dummy
- Use Bed
- Put Someone in Bed
- Get Put in Bed
- Defeat Squad
  - Attack the TARGETED squad.
- Seek and Talk and Send Signal
- Make Announcement
- Always Impossible task
- Find and Rescue
  - Character will go to nearby squad member, slave, or allied/faction
    member to begin bandaging if they are injured.
- Find Bed and Put In
  - If the character is carrying an unconscious squad member, slave, or
    some other character, this goal will tell them to put the carried
    person into the nearest bed.
- Use Cage
- Put in Cage
- Knockout Prisoner
- Release Prisoner
- Breakout Prisoner
- Find Cage and Put in
- Empty Machine Outputs
- Get Rid of Resources in My Inventory
  - Character will walk around and put resources that are inside their
    inventory (such as building materials, raw stone, fuel, etc.) into
    the nearest available machine or storage container.
- Find Some Building Materials
- Get Out of Bed
- Find a Shop
- Shopping
  - Character will start walking into random buildings. If it happens to
    be a shop, they might buy something from the counter.
  - Buying an items as a player will remove cats during the purchase,
    but will not give you any items.
- Buy Shit
- Move Inside Building
- Move to Fortification Gate
- Open Fortification Gate
- Bash Gate
- Operate Storage
- Job Builder
- Talk To Nearest Player Character
- Run Away Hometown
- Retreat Hometown
- Make Announcement Fast
- Travel to Target Town Fast
- Loot Food and Stuff
- Find and Kidnap
- Get Out of Cage Legit
- Kill Cage Occupant
- Kill a Random Cage Occupant
- Feed Corpse into Machine
- Dead Guys Go in the Pot
  - Character will dispose of dead bodies using a [](Corpse_Furnace.md).
- Find a Dead Guy
- Eat a Random Cage Occupant
  - Character will eat people that have been imprisoned by their
    faction.
- Unlock Door Player Order
- Follow Squadleader
  - Follow the current leader of the squad
- Find and Rescue Leader
- Protect Own Squad
  - Fight people who are attacking your squad members
- Territorial Aggression But Don’t Leave Home
- Get Re Equipped
- Use Turret
- Stumble Task Forced
- Find and Rescue if There’s Beds
  - Character will go to nearby squad member, slave, or allied/faction
    member to begin bandaging if they are injured. If the character is
    unconscious, they will carry them and put them into the nearest bed.
- Man a Turret
- Prospecting
- Emptying Machine
- Operate Automatic Machinery
- Go Home and Go to Bed
  - Character goes to sleep
- Go to the Bar and Drink
- Lock All My Doors
- Enter Building
- Stand at Guard Node Hometown Outside
- Shoo Strangers Out of My Building
  - Activates the "Shoo_Strangers_Out_Of_My_Building" dialogue event if
    a neutral character enters their building
- Send Dialogue Signal
- Send Dialogue Signal Repeat
- Send Dialogue Signal Without Moving
- Lock Door from Inside
  - Character locks their home's door, but makes sure that they are
    inside when they do it.
- Move to Building Door InsidePOS
- Follow While Talking
- Town Stalker
- Chain Target
- Capture New Slaves
- Carry Wounded Slaves
  - Tells slavers to pick up and carry unconscious slaves.
  - Should be given priority in packages, else slavers make ignore this
    goal.
- Put Down Carried Dude if They can Walk
  - If the character is carrying an unconscious squad member, slave, or
    some other character, this goal will tell them to put the carried
    person down once they've healed up enough to walk.
- Lift Object but Heal First
  - Carry the TARGET person, but heal them before doing so.
- Follow Slavemaster
  - Makes slaves follow their enslavers, such as with slave trader
    caravans.
- Slave Get in My Master’s Cage
- Gather Slaves from Cages
- Get Slave
- Sleep on Floor
- Hunting Bloodsmell
- Loot the Dead
- Loot to Replace Missing Weapon
- Hunt My Thief
- Man the Gate
- Strip Target’s Weapons
  - The character will remove any weapons the TARGET has on them.
  - Will cause the characters to attack the TARGET if they are not
    unconscious.
  - Will continue to run while goal is active, regardless of whether or
    not the TARGET has a weapon on them or was already stripped of one.
- Process and Strip New Slave
- Slave Watching
- Put Loot in Storage
- Cut Shackles
- Brute Force Shackles
- _Slave Obedience
- Work the Slaves
- Auto Laboring Mines
  - Character will operate random machinery and produce the output.
- Auto Laboring Mines Pretend
  - Character will operate random machinery, but not produce an output.
    Allows characters to operate a machine even if it is full.
- Go to Nearest HQ
- Go to Somewhere for Delivering Slaves
- Capture Escaping Slaves
- Lock All the Cages
- Beat Cage Occupant
- Lock All My Doors from Outside
- Lock Door From Outside
  - Character locks their home's door, but makes sure that they are
    standing outside when they do it.
- Move to Building Door OutsidePOS
- Leave Building
- Pick Lock on Shackles
- Total Escape
- Arrest Target
- Hunt Bounties
- Arrest Target’s Carried Person
- Find Cage and Put in if Bounty
- Get Out of Cage Escape
- Get Out of Bed if it’s Emergency
- Investigate Alarms
- Investigate Alarms Allies Only
- Police Free Prisoners When Done
- Loot Stolen Goods
- Lift Person Snatching Allowed
- Relax in Town Package
- Travel to Target Package
- Run Around Town Looking for People
  - Character will run into random buildings then quickly leave,
    including private residences. Unsure if there is any additional
    functionality to this.
- Gather Slaves from Cages if it’s an Export Town
- Give All My Slaves to if it’s an Import Town
- Take Off My Shackles
- Eat Target Alive
  - Characters will eat the TARGET if they are unconscious.
  - Enum works with humans, too.
- Pretend to Operate Machinery
- Man a Turret on Building
- Pickup Intruders
- Take Intruder Outside
- Lift Person Player Order
  - Character will carry the TARGETED person.
  - Seems to work even if the TARGET isn't unconscious. (Perhaps this is
    only the case if the TARGET is a player character?)
- Bash Door Player Order
- Melee Attack Animal
- Stealth Knockout
- Stealth Kill
- Eat a Random Dead Body
  - Used by animals that only eat dead bodies.
- Eat Crops
- Find Crops to Eat
- Eat a Random KO Body
  - Character will eat random unconscious bodies that they find, even if
    they are still alive.
  - When given to a squad, only one member will be eating at any one
    time.
  - Can be used by both animal and human characters. Humanoids will use
    the fogman chewing animation.
- Man a Turret Player Job
- Shoot at Target
- Worship Target
- Fogman Worship Victim
- Loot Animals Job
- Go Home and Go To Bed Secure
- Lift Person Snatching Allowed in Town Only
- Loot Resource Items We have Storage for
- Ditch All Resources
  - Character will walk around and put resources that are inside their
    inventory (such as building materials, raw stone, fuel, etc.) into
    the nearest available machine or storage container.
  - Unclear if there are any differences to the "Get Rid of Resources in
    My Inventory" enum
- Acquire Food at Homebase
- Grab One Food
- Gather Slaves From Cages if Female or Beast
- Kidnap Order
  - Character will carry the TARGET if they are unconcious.
- Collect Output Resource Building Mats
- Defeat Squad Limit Chase Rangekidna
- Splint Order
- Splint Job
  - Character will go to nearby squad member, slave, or allied/faction
    member to begin splinting if their limbs are damaged.
- Escape Kidnap
- Escape Kidnap Str
- Follow Urgent Escape
- Final Kidnapper Cage Job
  - Character will search for unconscious people to carry, then
    supposedly put them inside a cage they own.
- Sit on Throne
- Get Out of Cage Opportunistic
- Get Out of Bed Once Healed
- Use Bed Order
- Eat Food on Ground
- New Slave Processing
- Sleep on Floor Fake Ambush
- Ranged Attack
- Ranged Attack Focused
- Equip Crossbow
- Unequip Crossbow
- Ranged Attack Focused Unprovoked
- Move in Bow Range
- Stand at Guard Node Homebuilding Indoors Only
- Heal My Legs
- Assault Fortifications Prefer Gates
- Assault Fortifications Prefer Walls
- Smash Building
- Pickup Intruders Town
- Take Intruder Outside Town
- Sit Around
- Liberate All the Prisoners
  - Character will run to all nearby cages and let prisoners out, as
    long as the cage does not belong to their faction .
  - Prisoners seem to jump right back into the cage. Not sure if this is
    part of the enum or the result of some other package.
- Animal Fetch a Limb
- Play Because I have a Limb in Mouth
- Chase Ally Dogs with Mouth Limbs
- Run Away Forced
- Find Cage and Put Deadguy in
- Eat a Random Cage Occupant Measured Rate
- Shoo Strangers Out of My Building if Private
  - Activates the "Shoo_Strangers_Out_Of_My_Building" dialogue event if
    a neutral character enters their building and it is marked as
    private.
- Loot Container
- Cut Lock
- Brute Force Lock
- Bash Door Here
- Protect Allies Stay in Town

## AI Goals and their Weights

The larger the third value, the higher the importance of the task/goal.
The smallest importance is 1.

Zero has been reserved to short lasting important tasks/goals, such as
medical aid. It is an urgent override, so only assign a weight of 0 if
the goal has a natural end. For example, do not assign patrol tasks a
weight of 0, if you do the NPC or NPCs will never move on to the next
task.

[Category:Modding](Category:Modding "wikilink")