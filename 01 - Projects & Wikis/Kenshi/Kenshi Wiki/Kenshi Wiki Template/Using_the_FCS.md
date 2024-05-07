This article is pulled from the 'Using the FCS.pdf' file located in your
game's installation directory as of version 1.0.57.

## Introduction

### What’s an FCS?

The [](Forgotten_Construction_Set.md), is an application used to
create and modify data used to create the world of Kenshi. Almost
everything in Kenshi can be modified using this tool, with the exception
of terrain and visual effects.

### Where can I find the FCS?

\Steam\steamapps\common\Kenshi\forgotten construction set.exe

FCS can also be opened through steam. When launching the game, select
the *Launch Modding tool* option. ![](Game_editor.PNG "Game_editor.PNG")

### Why is it called FCS?

FCS stands for **F**orgotten **C**onstruction **S**et. Kenshi was
previously called “Forgotten” in early development. Really this
application should be called KCS, but it’s been out for so long that
it’s too late to change it now.

### Useful non-official guides

We’re a bit late to this whole documentation thing, over the years our
community has done a wonderful job of documenting a variety of uses for
FCS, which we will shamelessly link to below:

- [Save Editing 101 By
  Shidan](https://steamcommunity.com/sharedfiles/filedetails/?id=1370334383)
  - See also Shidan's [compilation of
    notes](https://steamcommunity.com/sharedfiles/filedetails/?id=2570870493)
    on game and FCS mechanics
- [Kenshi Modding 101: FCS and Dialogue By
  Boron](https://steamcommunity.com/sharedfiles/filedetails/?id=1444279946)
- [How to Find and Edit Mods By
  Canin](https://steamcommunity.com/sharedfiles/filedetails/?id=1608980474)

## Layout

### Opening a mod

When first loading up FCS you’ll be greeted with a screen which will
look something like this: ![](Opening_Mod.PNG "Opening_Mod.PNG")

Note the location of the **\*ACTIVE\*** text, this is where your changes
will be saved (should you decide to make any).

It is highly advised that you create your own mod for testing purposes
where any changes can remain isolated from any core game data.

Mods that are currently set to be loaded by the game will already be
ticked. You should leave the mods that will be loaded after your mod
ticked as you will be able to see any changes that could be overriding
your mod.

When ready, click **DONE** to open a mod

### Navigating and locating data

From the *Game World* window, you’ll be able to find almost everything
that can be modified in Kenshi. The exception being the following 2
things found in the navigation bar at the top of the window.

- Global game settings
- Artifacts settings
  - This contains a list of unique, non-respawnable items that will be
    scattered around the world

<figure>
<img src="Navbar.PNG" title="Navbar.PNG" />
<figcaption>Navbar.PNG</figcaption>
</figure>


====The Game World window====
<img src="FCS_Game_World_Window.png" title="FCS_Game_World_Window.png"
width="622" height="622" alt="FCS_Game_World_Window.png" />

1.  Object categories and subcategories
    - NOTE: the root category does not necessarily contain all of the
      items found in the subcategories. E.g. *Dialogue Package* does NOT
      contain all the items found in *Word Swaps* or *Dialogue*
    - This layout can be modified in **fcs_layout.def** (found in the
      same folder as **forgotten construction set.exe**)
2.  The items in the selected category
    - Double click on items here to open and modify them
    - If you have multiple items selected, press return to open them all
3.  Object property columns
    - Click to sort items
    - Right click to add columns
    - See [Custom Columns](Using_the_FCS.md#Custom_Columns "wikilink")
4.  The search box for narrowing the results shown in panel **2**
    - See the [](Using_the_FCS.md#Searching_for_data) section below
      for an in depth look at this feature and how to use it

#### Colour coding

The colour of the items in the list dictate the state of the item. This
colour code system is also used for properties of the items.

- Black - Value is from a base mod
- Blue - Value is modified by the active mod
- Green - Value was created by the active mod
- Grey - Item is deleted by the active mod, or by a later mod.
- Orange - Item is created by a later mod. You can’t modify these in the
  active mod

#### Custom Columns

You can add additional columns to the item list to display any item
property from the right click menu.

<figure>
<img src="Custom_Columns.PNG" title="File:Custom Columns.PNG" />
<figcaption><a href="File:Custom">File:Custom</a>
Columns.PNG</figcaption>
</figure>

The default options shown above are as follows;

- String ID - The unique ID of the item
- Ref - Number of other items that reference this item
- Type - The object type e.g. CHARACTER, BUILDING, RESEARCH
- State - The item state indicated by its colour coding (see previous
  section)

All of these columns (as well as any custom ones you might add) can be
used to sort the items in the current display section by clicking on the
column header. Columns can also be re-arranged via drag and drop and
resized however you see fit.

The Add/Add List options allow users to add columns for any property an
item may have.

The ‘Add List’ option will open the dialog window seen below and allows
you to view reference data at a glance.

<figure>
<img src="Add_list.PNG" title="File:Add list.PNG" />
<figcaption><a href="File:Add">File:Add</a> list.PNG</figcaption>
</figure>

The Items and values options determine what to display (see image below
for example). If neither are checked the column will display the number
of items in that list.

If you want to change these options after adding the column, just add
the list again with the new options.

<figure>
<img src="Custom_columns2.PNG" title="File:Custom columns2.PNG" />
<figcaption><a href="File:Custom">File:Custom</a>
columns2.PNG</figcaption>
</figure>

To remove any column, right click the header bar, go to columns and
select the column you’d like to add or remove. The ‘Reset’ option will
remove all additional columns.

### Object view

Double clicking on an item in the game world list will open up the
object and give a view which will look something like this;

<figure>
<img src="Object_view.PNG" title="File:Object view.PNG" />
<figcaption><a href="File:Object">File:Object</a> view.PNG</figcaption>
</figure>

**NOTE**: If an object does not open this window by default, using ALT +
Double click will open the item with this menu.

The properties on display will be different for each type of object
available (e.g. a dialogue package won’t have an *unarmed* stats
property, but a character will).

1.  The value properties for this object
    - Numbers, names, file paths and Enum dropdown
2.  Object reference lists
    - Anything referencing another object
3.  A description of the highlighted property

The \[...\] button in the top right corner contains some extra actions
to run on this item:

- Show References - display all items that link to this item.
- Copy Data From Item - Sets all properties in this item to match
  another item
- Add ToDo List item - Adds an entry for this item in the notes window
- Duplicate item - Makes a copy of this item
- Add missing fields - Add any properties defined in fcs.def that are
  missing from this item
- Remove obsolete fields - Delete any properties in this item that are
  no longer defined in fcs.def. This is the same as the ‘Clean item’
  action in the Game World context menu.

## Data management tools

### Searching for data

The search box can be used in a multitude of ways to help locate data.

#### Search by Name or StringID

The default behaviour for text in this box. In the below example you can
see everything in the Building category with the word “dome” in the
name.

**NOTE**: This search is NOT case sensitive

<figure>
<img src="Search.PNG" title="File:Search.PNG" />
<figcaption><a href="File:Search.PNG">File:Search.PNG</a></figcaption>
</figure>

#### Search by value

Operators can be used to search for objects with certain values.

**NOTE**: Searching by value IS case sensitive for the property and is
NOT case sensitive for your search term.

##### Equal to

- Operator =
- Gives an exact match on a property

<figure>
<img src="Equal_to.PNG" title="File:Equal to.PNG" />
<figcaption><a href="File:Equal">File:Equal</a> to.PNG</figcaption>
</figure>

##### Not Equal to

- Operator !=
- Does the opposite of the above

##### Greater/Less than

- Operators \> \< \>= \<=
  - More than
  - Less than
  - More than or equal
  - Less than or equal
- For comparing numeric values

<figure>
<img src="GreaterLess_than.PNG" title="File:GreaterLess than.PNG" />
<figcaption><a href="File:GreaterLess">File:GreaterLess</a>
than.PNG</figcaption>
</figure>

- Can also be used for list sizes, such as the example below.
  - Showing all squads with more than 1 reference in the *faction* list

<figure>
<img src="GreaterLess_than2.PNG" title="File:GreaterLess than2.PNG" />
<figcaption><a href="File:GreaterLess">File:GreaterLess</a>
than2.PNG</figcaption>
</figure>

##### Contains

- Operator :
- For showing items with properties containing the given value
- E.g. below, all lines of dialogue which contain the word “Hello”

<figure>
<img src="Contains.PNG" title="File:Contains.PNG" />
<figcaption><a
href="File:Contains.PNG">File:Contains.PNG</a></figcaption>
</figure>

For indexed fields such as dialogue lines where you have text0, text1,
etc, you can search specifically by text0, or search all of them by
omitting the number.

##### Does not contain

- Operator !:
- Provides the opposite result of the Contains operator mentioned above
- E.g. below, all crossbows with descriptions that don’t include
  “quality”

<figure>
<img src="NotContains.PNG" title="File:NotContains.PNG" />
<figcaption><a
href="File:NotContains.PNG">File:NotContains.PNG</a></figcaption>
</figure>

##### Regex

- Operator ?
- Matches a string field to the provided regex
- Refer to <https://regexr.com/> for how to use this and proper syntax.
- If you think I’m documenting regex here you’ve got another thing
  coming.

<figure>
<img src="Regex.PNG" title="File:Regex.PNG" />
<figcaption><a href="File:Regex.PNG">File:Regex.PNG</a></figcaption>
</figure>

#### Combining multiple search terms

The semi-colon operator can be used to use multiple search terms. In the
example below, we’re searching for Buildings with “*outpost*” in the
name and need over 100 building materials to complete construction.

<figure>
<img src="Combined_search.PNG" title="File:Combined search.PNG" />
<figcaption><a href="File:Combined">File:Combined</a>
search.PNG</figcaption>
</figure>

#### Special properties

These are case sensitive.

- Ref - filter on number of references to the item, same as the Ref
  custom column
- Type - filter on item type.
- State - filter on item state

You can filter by references in a number of ways:

- Filter by reference count - ‘things \> 5’ will get all items with more
  than 5 references in a list called things. All numeric operators will
  work.
- Filter by reference target - ‘things = item name’ will get all items
  that reference an item called ‘item name’. This can be the name or
  string id of the item.
- Filter by reference values: ‘things.v0 = 4’ will get all items with
  the first value of any referenced item in the things reference list
  being 4. This works with all numeric operators, and keys v0, v1 and v2
  match the three potential values.
- Filter by property of referenced item: ‘things.property = blah’ will
  match all items that contain a reference to an item in its things list
  that would match a filter of ‘property = blah’. This also works with
  the special properties mentioned above.
- This system is fully recursive so you can chain multiple lists
  together, eg \`dialogs.lines.lines.effect \> 0\`

#### Recursive reference searching

Properties of objects referenced by list items can also be searched for
using the period operator.

In the example below, we search for the list of characters for those
part of a faction which are anti slavery.

<figure>
<img src="Recursive.PNG" title="File:Recursive.PNG" />
<figcaption><a
href="File:Recursive.PNG">File:Recursive.PNG</a></figcaption>
</figure>

This method is fully recursive. Below is another example demonstrating
this. The search is for all interior buildings with a functionality
reference object that consumes items with a value of over 500 cats.

<figure>
<img src="Recursive2.PNG" title="File:Recursive2.PNG" />
<figcaption><a
href="File:Recursive2.PNG">File:Recursive2.PNG</a></figcaption>
</figure>

### Set Field

Another useful function that allows setting a specific value in all
selected items. This is found in the right click menu.

<figure>
<img src="Set_field.PNG" title="File:Set field.PNG" />
<figcaption><a href="File:Set">File:Set</a> field.PNG</figcaption>
</figure>

As well as setting the value for multiple items at once, numerical
fields can also be modified through multiplication, division, addition
and subtraction.

There’s also support for adding and modifying reference values in bulk

<figure>
<img src="Set_field_2.PNG" title="File:Set field 2.PNG" />
<figcaption><a href="File:Set">File:Set</a> field 2.PNG</figcaption>
</figure>

### Find and Replace

You can run find and replace on any text or filename field. The function
is located in the right click menu in the Game World window and will run
on all selected items.

Running it on dialogue items will affect all lines in that dialogue. You
can also access it within the dialogue window where it will also run on
all the lines.

It has the option to use [regular
expression](https://en.wikipedia.org/wiki/Regular_expression) searches.

### Spellcheck

The spell check option can be found in the top toolbar of the
application, the conversation editor window and in the right click
context menu of the navigation window.

<figure>
<img src="Spellcheckbar.PNG" title="File:Spellcheckbar.PNG" />
<figcaption><a
href="File:Spellcheckbar.PNG">File:Spellcheckbar.PNG</a></figcaption>
</figure>

The toolbar button will run the spell check operation for all items.
![](Spellcheckcontext.PNG "Spellcheckcontext.PNG") The right click
context menu option will run the spell check operation for all selected
items.

Spelling checks are done against the two dictionary files
**Dictionary.txt** and **Dictionary_custom.txt**.

Currently these dictionaries are only set up to support english. For
other languages, we recommend amending or replacing the contents of
**Dictionary.txt** with words from your preferred language. FCS
developers are currently only native english speakers, so we’re not the
best judges of what constitutes a good dictionary in any other language.



## Managing your mod

### Item colour key

- Green - New item
- Blue - Modified existing item
- Grey - Deleted item
- Orange - Changes to this item in a later mod
  - These changes can be merged but they will have no effect since a
    later mod will change the values anyway.
- Red - Merge conflict
  - This means the item has been modified in both your mod and the mod
    you are merging since you last merged so the system cannot
    automatically detect which change is more recent.
  - They are generally not an issue but you should check the values to
    verify if you want to accept or reject the change.
- Purple - Modified remove item
  - Combination of Blue and Red states

### Loading your mod in game

<figure>
<img src="Loadorder.PNG" title="File:Loadorder.PNG" />
<figcaption><a
href="File:Loadorder.PNG">File:Loadorder.PNG</a></figcaption>
</figure>

Order is very important in this file. Entries at the top will be loaded
before entries lower down.

For example;

- FasterBeakThings.mod
- SlowerBeakThings.mod

The SlowerBeakThings.mod will take precedence over the
FasterBeakThings.mod. If this isn’t the desired effect, swap them over
so SlowerBeakThings.mod is first in the list.

### Merging Mods

You can merge data from another mod file using the merge tool from the
top bar

<figure>
<img src="Merge_mod.PNG" title="File:Merge mod.PNG" />
<figcaption><a href="File:Merge">File:Merge</a> mod.PNG</figcaption>
</figure>

First select a mod to merge with the active file. You can either select
a mod from the list, or load any data file with the ‘\*’ button.

You will not be able to merge a mod that is open as a dependency of the
active mod, but you can merge mods that are later in the list.

The check boxes have three states:

- ![](Ignorebox.PNG "Ignorebox.PNG") : Ignore - these changes will not
  be merged or discarded. This is the default.
- ![](Selected_Box.PNG "Selected_Box.PNG") : Selected - these changes
  will be applied to to the active mod
- ![](Deselected_Box.PNG "Deselected_Box.PNG") : Deselected - these
  changes will be skipped and will not show up again next time you merge
  this mod. The Show Skipped Changes button will display changes that
  were previously skipped.

You can tick multiple boxes at once by selecting multiple items and
clicking a checkbox, or from the right click menu. The right click menu
also has recursive commands that will check or uncheck the selected item
and any items referenced by that item. This allows easily selecting a
complete dialogue and all of its lines.

The fix references command will ensure that any new items will also be
merged if you have selected any references to them.

If a mod contains level data, that can also be merged with the merge
level data checkbox. It will be disabled if there is no level data to
merge.

### Cleanup

The cleanup button in the top bar allows deleting unnecessary or
obsolete data from the active mod.

<figure>
<img src="Cleanup.PNG" title="File:Cleanup.PNG" />
<figcaption><a href="File:Cleanup.PNG">File:Cleanup.PNG</a></figcaption>
</figure>

- Remove deprecated fields
  - Remove all item properties that are not defined in fcs.def This
    ignores items that have no definitions at all
- Remove deleted items
  - Delete items that were created by the active mod and removed by a
    later mod
- Delete orphaned items
  - Delete items that are flagged as owned by another item and have no
    references. This includes things like dialogue lines that are
    somehow not part of a dialogue
- Remove invalid references
  - Delete any references to missing items
- Remove undefined items
  - Delete all items with types that are not defined in fcs.def This
    will not affect items that are referenced by other items.

The cleanup function when you right click on items in the Game World
window runs the ‘Remove deprecated fields’ task on the selected items.

## Errors

If any errors are detected, the error window will display when you load
your mod. This window is also available from the tool strip.

<figure>
<img src="Errors.PNG" title="File:Errors.PNG" />
<figcaption><a href="File:Errors.PNG">File:Errors.PNG</a></figcaption>
</figure>

Double clicking on an error will open the associated item.

Right clicking will show some options to resolve the error:

- Delete item - This will delete the associated item.
- Remove Invalid references. This will delete any references to invalid
  items that the associated item contains.
- Clear changes - This will revert any changes the active mod makes to
  this item.
- Ignore - This temporarily marks the error resolved. It may come back
  again later.

By default only errors associated with the current mod are displayed.
You can show all errors with the show from all mods option. Some errors
do not know which mod caused the problem so will always be shown.

If you open an item and get the ‘Dialogue line is not associated with
any dialogue’ message, the item is an orphaned dialogue object and can
just be deleted.

The errors list is only updated when a mod is loaded. The scan button
can rescan the active mod for any new errors.

### Types of Errors

- Undefined reference - The item contains references to items that do
  not exist. This could be from a mod dependency that is not loaded. If
  not you can clear them with the ‘Remove Invalid references’ option.
- Reference to deleted item - The item contains a reference to an item
  that has been deleted by the active mod. You should delete this
  reference or restore the deleted item.
- Reference to incorrect item type - The definition file has probably
  changed or the mod is corrupt. You should delete these invalid
  references from the item.
- No closing decorator tag. They must be closed with \</\> - Incorrect
  dialogue formatting. Double clicking the error will highlight the line
  in question.
- Word swap not terminated - Word swaps must be /SWAP/. This could be a
  false positive if ‘/’ is used in another context.
- Empty word swap - A dialogue line contains ‘//’ for some reason
- Missing word swap - Dialogue contains a word swap that does not exist
  in the word swaps list
- Multiple primary references to dialogue line - This can only happen if
  dialogue links have been messed up. This was caused by a bug that
  should have been fixed. It can be resolved by manually editing the
  link tags.
- No primary reference to dialogue line - Similar link corruption as the
  above multiple primary references error.
- Orphaned dialogue object - Dialogue lines or conditions not attached
  to any dialogue - just delete it or run cleanup.
- Reference list contains too many items - Reference lists can have a
  limit to the number of referenced items. You should delete the extra
  references.
- Item has changed type - Possible data corruption or mod conflict.
  Somehow a mod has changed the type of an item.
- Value was the wrong type and has been converted - The definition file
  has probably changed. A value has been converted to a new type. You
  should check if it is correct.
- Value is the wrong type and could not be converted. - The definition
  file has probably changed. The value has been reset to its default.
  You may need to update this value.
- Modified item undefined. - This mod has changes in an item that does
  not exist. A mod dependency may not be loaded or the item has been
  deleted from a mod dependency. The item will likely show up missing
  most of its values. To resolve it, you can use the clear changes
  option.
- Item with id has already been defined by mod - This item conflicts
  with one from another loaded mod. This can be a false positive error
  if the mod has recently been merged with another. If this is the case
  the error will go away as it will automatically be resolved when you
  save.
- New values have been added - The item definition file has changed to
  add new properties to an item. You may want to edit them but in
  general just ignore this message.

[Category:Modding](Category:Modding "wikilink")
[Category:Guides](Category:Guides "wikilink")