This short guide will help new players and modders to enable to craft
vanilla game armour using the [](Holy_Chest_Plate.md) and the [](Empire_Samurai_Armour.md) as examples.

## Starting FCS

When you start then FCS there's a welcoming menu that appears, showing a
list of mods listed under FCS. There are some "default mods" that are
part of the game that need to be enabled. The items that need to be
ticked (they are by default, but just in case):

- gamedata.base
- Newwworld.mod
- Dialogue.mod
- rebirth.mod

Click on the topmost icon on the right part of the menu to "create new
mod file". Enter mod name. In our case "Holy Chest Plate Blueprint Mod".
Once you click "create" this new mod will become the ACTIVE mod (meaning
changes can be made to it), which is what we want. Click on the big DONE
button.

## Creating New Research for the vanilla item

You are welcomed by the general modding menu listing all assets within
the game (in expandable lists). After you have familiarised yourself
with them left-click on "Research" button. This will bring up all the
research options available in the game, as part of the research tree or
blueprints. We want to create a new research so we mouse over the right
part of the box (where all research is listed) and right-click on an
empty space to bring up a menu. In this menu we choose "New Item". We
now have a RESEARCH item menu appear.

It is a good practice to name this research so we left-click on the box
next to the name field and erase the default "RESEARCH" name. The new
name will be "Holy Nation Chest Plate Blueprint". Clicking away from the
field should save the new name. We then choose the field "blueprint
only" and enable "True" instead of the default "False" in the drop down
menu. This way the new research appears only as a blueprint in the
game.You can of course leave this option on "False" and this way once
you research a certain level of [Technology](Technology.md "wikilink") the
research option will appear under your faction's research menu. The only
thing left to do is to set a price for it by going to the "money" box an
entering a number. 15000 credits seems fair for this blueprint. If you
only want the blueprint research option you can move on to the next
section of this guide and close the research window (which should save
it).

If you want to enable this blueprint as a research option for your
faction there are still a few steps left to do. Set the "category" to
"Smithing", set the level to whatever you think the level should be
(from 1-6). 3 seems fair to me for this research. Also set time in hours
this tech would take to research. I have left the default 12 hours. NB
do not forget to set the "blueprint only" option to "False". Close the
research window. You can now find this item under your faction's
research after you have saved the mod and enabled it before loading the
game. Note that some items are not enabled to be crafted in the default
game, in this case skip to the final section of this guide.

## Adding new blueprint to vendor lists

In case we have chosen the blueprint option we now need to add it to
vendor lists so that they would appear in game. The Holy Chest Plate
should appear in Holy Nation shops so we go to the "Vendor Lists" option
in the main menu. Vendors have different names, but in our case we need
the "armor vendor holy" and click on it. In the menu that appeared we go
to the drop down menu on the top-right section of the "amor vendor holy"
menu that appeared. It should say "armour blueprints" and we need to
left-click on the "Add" button next to it to add the blueprint we just
created. Now we look for the "Holy Nation Chest Plate Blueprint" we just
created and click on it to add it to the available objects list. For now
we want the chance to appear to be a 100% so we input a 100 into the
numerical box to the right of the newly added item.

Upon saving the mod, The Holy Chest Plate should appear both under the
HN Armourer trading box and under the Heavy Smithy crafting menu so our
task of adding this vanilla item to the game is complete. However, some
items are not enabled to be crafted in base game so for that we pass to
the last step of this guide.

## Adding a new crafting option for the correct crafting station

The Empire Samurai Armour does not appear under the crafting menu if all
previous steps are followed. In this case it needs to be enabled under
the crafting station's menu. We go to Buildings-\>Functionality-\>Armour
Plate under the big menu to enable crafting options on a Heavy Smithy.
Once opened we can add an item similarly to how we added blueprints.
Select "armour crafts" from the top-right's drop down menu and click on
"Add". The menu that appears should offer you the option to add the
item, in our case Empire Samurai Armour. No further changes are needed
at this stage and upon saving the mod you should be able to craft this
item in the Heavy Armour Smithy.

[Category:Modding](Category:Modding "wikilink")
[Category:Guides](Category:Guides "wikilink")