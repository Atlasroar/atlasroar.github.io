WIP

Here I list some of the results of our pursuit to make a workaround for
returning quest items. The NPCs of Kenshi cannot take items, so some
item returning box is needed.

##### Currently the only somewhat working system (not elegant)

NPC can unlock a dialog option based on the fact an item is inside a
player inventory. NPCs cannot check if the object is NOT in player
inventory, but with careful locking and unlocking dialogues it is
possible to default to 'player had this item and now has not' deduction.
However the player can do whatever they want with the item, a) drop it
on the ground or b) put it in a box. The result is the same, the player
can always pick it up again later. So it is important to make the quest
item nonfunctional and have no monetary value.

##### Cannot make a house sellable & with a function

*The idea behind this was to have a machine that takes the quest item as
a material and produces the reward. Cause the player cannot operate a
NPC machine, I tested if one could sell the ownership of the machine to
the player. It does not work. Putting a function to a house makes it
unsellable. Apparently you cannot have two click-events in one
building.*

[Category:Wip](Category:Wip "wikilink")
[Category:Modding](Category:Modding "wikilink")