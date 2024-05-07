This page explains how the packages in the [](Forgotten_Construction_Set.md) AI system work, along with
lists of relevant information if available.

## AI Packages

AI Packages are lists of goals that a squad is using. Goals can be given
to leaders, squad members, animals, or slaves. They are activated based
on priority, usage, and time of day.

## Clears Existing Jobs

**A boolean condition of some sort. All previous tasks end.**

- True
- False

## Signal Function

**Controls how this package starts / ends. Also controls how the package
chooses its main TARGET.**

- None
- Retreat Cannibal Raid
- At Safe Town
- At Home Town
- Cannibal Start Patrol
- Squad Not Intact
- Start Patrol
- Diplomat Mission
- Defeat Squad
- Home Owner Keep Locked
- Gather Up All Local Prisoners
- Slaver Ship to Workcamp
- Bodyguard
- Become Ex Slave
- Out of Danger
- Defend Player Town Timed
  - Makes the player's town the TARGET for goals.
  - Used for merc contract jobs.
- Wandering Town to Town
- Hang Out at Bar
- Raiding Weak Villages
- War Gather Forces
- War Assault Town
- War Battle Meeting
- Refugee Disband
- Start Patrol Running
- Gather Up All Local Prisoners Unholy
- Retreat Cannibal Raid to Nearest Nest
- Hang Out Outdoors Only
- Cannibals At Home
- Slaver Ship to Anywhere Close
- Passing By Town Assault
  - Used by attacking patrols when they happen across a player base.
- Occupy Conquered Town
  - Seems to be activated by selecting this as the "Leads To" package
    from a different package. Presumably mostly used by packages with
    the "Passing By Town Assault" signal function.
- Defend Player Town Campaign
- War Assault Town Cannibal
- Timed Contract
  - Package is given to the squad by the "AI Contract" dialogue effect.
    The TARGET of the package is the same as the target of the dialogue
    event (So if the squad spots a random neutral and receive a contract
    to bodyguard them in that event, they will protect whichever neutral
    character it was that they spotted).
  - Ends when the specified amount of hours in the dialogue effect has
    passed.
  - Usually what is used by contract jobs

## Unloaded Function

**What does this package do if the character is not in the loaded
area?**

- None
  - Presumably the character does nothing
- Patrol Town
- Patrol Shortrange
- Patrol Longrange
- Go Home
- Travel Target
  - Travels to the target destination, such as when mercenaries travel
    to the player town when they are hired to defend it.
- Travel Target Fast
  - Same as Travel Target, but at a running pace.

[Category:Modding](Category:Modding "wikilink")