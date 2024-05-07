---
date: 2024-04-23T14:44:00
tags:
  - kenshi
  - modding
cssclasses:
  - page-kenshi
  - center-images
---
[[Kenshi Modding Wiki]]


## How the vendor lists work:

For the purpose of this guide I am calling the person holding the vendor
list (fe. a barman) **a seller** and the combination of all vendor lists
**a shop inventory.** A shop window is the UI window that the player
sees when they buy and sell things, the result of all the randomization
pulls from all the lists.

- A seller is a NPC character, usually a leader of a squad. They do not
  have to be a leader, but being a leader has its benefits. Sometimes
  you want the leader to have other dialogue with the player, so in
  those cases you might want a non-leader to held the shop inventory. Or
  you could set up a housemate.
- A seller must have **a shop keeper dialogue** to be able to sell items
  (DA_TRADE in a dialogue line in PLAYER_TALK_TO_ME event)
- There can be **only one shop inventory per squad**, so if you need
  multiple sellers with different inventories for your shop building,
  you must set up **housemates**.
- One shop inventory can pull from several vendor lists (and usually
  does)
- Faction trade culture affects the shop inventory contents. So, all
  illegal items set in the trade culture will be omitted from the
  inventory, even if they are set up in a vendor list that is included
  in the seller's squad. Some **factions without a trade culture will
  obey the region's main faction trade culture.**
- Each item has a % chance to appear (rarity) and the chance is
  calculated against all the other items on the same vendor list AND all
  the other vendor lists on the inventory.
- Most shops and vendor lists **are shared** between several places in
  game, so **if you edit one in any way you edit them all**. For this
  reason, replace with a copy before starting your edits. This way the
  alterations affect only the shop you are working on.
- A **special item** is an item that will always be picked for the shop,
  and they will take one item spot from the *item count* each (if
  multiple).
- Items in vendor lists with a spawn chance of 0 are treated like a 100
  chance.
- A vendor list is also the **loot item list** for the building chests
  and shop counters.
- If a vendor has their "is trader" value set to TRUE then the amount of
  items they have for sale is based off their "vendor fill total
  amount". A shop will have between 0.8x to 1.2x whatever value is set.
  (So 100 would range between 80 to 120)
- Each vendor list has a max item number called **items count**. This
  max item number is only used if the vendor has trader set to FALSE.
  This value will then replace the vendor fill amount total to determine
  the items spawned. Unlike "vendors fill total amount" the value is not
  randomized. **PUT YOUR RAREST CHANCE ITEMS ON TOP OF THE LIST** (yes,
  the die rolls against the chance per item one at a time from top
  down).
  - Important to add that if the vendor is a wandering trader (And
    trader is set to false) their "items count" will be multiplied by
    however many animals they have that are carrying their inventory.
    Using the (Holy nation variant) "[](Caravan_Trader_Boss.md)" squad as an example. They can
    have between 1 to 3 Packbulls. Their vendor list has 40 items. So
    they will have 40, 80 or 120 items for sale depending on if they
    have 1, 2 or 3 bulls.

See also [Creating New Towns](Creating_New_Towns.md "wikilink") for info on
squad spawning in specific houses and about housemates and [Creating a
Special Placeable/Lootable Item for Your
Town](Creating_a_Special_Placeable/Lootable_Item_for_Your_Town "wikilink").

## Simplest way to add desired items to an existing inventory of an existing shop:

1.  Find the vendor list name you'd like to add, or make a new vendor
    list
2.  Open the squad file of the person you want this list to be added to
    (they must have also a shop keeper's dialogue)
3.  In the top a drop down menu, find vendors (second to bottom)
4.  Choose the list you want to add
5.  Adjust the percentage on the squad list of all vendors in the
    squad's list. They are in relevance to each other. You can go like
    400 on them if you want your vendor list to be more prevalent
    (pulled from 4 times more often)

The more vendor lists a squad has on their shop inventory, the less one
of the vendors list contents will be present in the shop window. This is
why I suggest having a housemate seller to just sell fe. construction
goods, if you want to be certain that shop has that item (type) exactly.
![](SellerVendorList.png "SellerVendorList.png")

## In detail:

The following instructions are from timor1234 on the Steam forum post:
<https://steamcommunity.com/app/233860/discussions/3/1739980540120440391/>
with additions by Cattrina (me). -Frankiewuzhere added some extra info.

#### **Creating a vendor list**

1.  Find the Vendor Lists menu, it is at the bottom of the Game World
    left panel.
2.  Right click on any item on the list, pick new item (or duplicate if
    you want to make a variation list).
3.  Give the list a name.
4.  Add items to the list. Select an item type from the drop down menu
    and click add button. Press add and find it in the list or use a
    search word in the bottom of the list to find it even easier.
5.  Give each item a chance % of them appearing. 400% means four items.
    0.5% means every other die roll no item is picked.

#### **Adding a list to a seller**

1.  Find the shop you want to add the new vendor list to
2.  Double click the shop, pick 'vendors' from the drop down menu in the
    right top corner and press add.
3.  Pick 'new item' in the list that appears and create your vendor list
    OR select an already made vendor list here.

### If you want to add something to only one specific shop in one specific town (resident)

1.  Find that shop (resident) in the town menu and replace it with a
    copy, enter it by double clicking (to prevent altering all shops
    with the same name)
2.  Give that shop a slightly different name
3.  Add the vendor list you made to that shop (do not add that item to
    an existing vendor list because they are shared).
4.  You can alternatively add that item to that shop as **a special
    item**.

Most shops and vendor lists are shared between several places in game,
so if you edit one in any way you edit them all, but if you replace
those with copies you are now only editing your copy. **Be cautious:**
even in your copy almost every squad member, AI package, vendor list,
dialogue package etc*,* should be replaced with copies before editing
them, unless you **want to** apply those changes in other places as
well, because they are shared. Very few things are unique and apply only
to one place or squad. **So, to be sure, replace with a copy.**

Tip: when you are in town window, vendor window, squad window etc, just
click on something in the menu and see if an explanation on what it does
appears on the bottom of the window, most times it will.

#### **Blueprints in shops**

Each blueprint of a certain item (e.g. "Wakizashis" or "Iron Hat") can
spawn only ONCE per Vendor List (but can still spawn multiple times per
Vendor, if Vendor has several Vendor Lists containing that blueprint.)

[Category:Wip](Category:Wip "wikilink") [Category:Modding
Guide](Category:Modding_Guide "wikilink")
[Category:Vendors](Category:Vendors "wikilink")
[Category:Loot](Category:Loot "wikilink")