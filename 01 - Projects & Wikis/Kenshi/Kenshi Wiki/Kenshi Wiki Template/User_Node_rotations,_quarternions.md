## Guide for setting up user nodes around your object

By Cattrina

Quarternions are notoriously difficult to set up, because instead of
more logical XYZ axis and euler rotations we all are used to,
quartenions use four rotation axes in X formation against each other.
And there are six (actually infinite but this is easier to understand)
faces rotations can go: think of a D6, the six is on top, one down etc.
(see image). Kenshi is on plane 6, so we only need to use rotations
relevant to plane 6. But there are corresponding rotation sets for each
plane, and if you are making ceiling lamps you might need plane 1
orientations. Funnily enough if you make a new user node in FCS, the
default rotation (0,1,0,0) is upside down (plane 1).

<figure>
<img src="Rotation_Planes.png" title="Rotation_Planes.png" />
<figcaption>Rotation_Planes.png</figcaption>
</figure>

For everyone's sanity's sake this guide only focuses on plane 6
orientations.

Here a link to [Steam Workshop companion Modder's
Resource](https://steamcommunity.com/sharedfiles/filedetails/?id=2977389217),
where you can download the HD images and the mesh object relevant to
this guide.
![](User_Node_Orientation_Guide.png "User_Node_Orientation_Guide.png")

Node rotations are understood the easiest in relation to the object's
origo (usually at the center, if the modder has not edited it to
somewhere else); the nodes maintain their orientation to the origo even
if you rotate the object in world. If there is one node and it is in the
center of the object, any rotation is away from the center. But if the
node is located away from the center, it is important to take into
account if the character is going to use the object or are they going to
sit on the object, and orient the node accordingly.

There are rarely any occasions where the rotation (and position) of the
node actually matters, except on a bed. The user node is mostly there
just to help the player to understand how the item is used and how much
room (and where) they need to leave for the characters to access the
object.

### Rotations towards the object in the center (arrows in)

<table>
<thead>
<tr class="header">
<th><p><code>W 0,3556925</code></p>
<p><code>X -2,820028E-08</code></p>
<p><code>Y 0,9346039</code></p>
<p><code>Z -2,820028E-08</code></p></th>
<th><p><code>W 0,7155288</code></p>
<p><code>X -3,090637E-08</code></p>
<p><code>Y 0,6985834</code></p>
<p><code>Z-3,090637E-08</code></p></th>
<th><p><code>W 0,9082747</code></p>
<p><code>X -2,899485E-08</code></p>
<p><code>Y 0,418374</code></p>
<p><code>Z -2,899485E-08</code></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>W 0,009913659</code></p>
<p><code>X 2,163797E-08</code></p>
<p><code>Y -0,9999511</code></p>
<p><code>Z 2,163797E-08</code></p></td>
<td></td>
<td><p><code>W 0,999722</code></p>
<p><code>X -2,236551E-08</code></p>
<p><code>Y 0,02360464</code></p>
<p><code>Z -2,236551E-08</code></p></td>
</tr>
<tr class="even">
<td><p><code>W 0,4143499</code></p>
<p><code>X 1,083535E-08</code></p>
<p><code>Y -0,9101182</code></p>
<p><code>Z 1,083535E-08</code></p></td>
<td><p><code>W 0,7163444</code></p>
<p><code>X -4,06438E-10</code></p>
<p><code>Y -0,6977479</code></p>
<p><code>Z -4,06438E-10</code></p></td>
<td><p><code>W 0,9379124</code></p>
<p><code>X -1,291757E-08</code></p>
<p><code>Y -0,3468742</code></p>
<p><code>Z -1,291757E-08</code></p></td>
</tr>
</tbody>
</table>

### Rotations away from the object in the center (arrows out)

<table>
<tbody>
<tr class="odd">
<td><p><code>W 0,9379124</code></p>
<p><code>X -1,291757E-08</code></p>
<p><code>Y -0,3468742</code></p>
<p><code>Z -1,291757E-08</code></p></td>
<td><p><code>W 0,7163444</code></p>
<p><code>X -4,06438E-10</code></p>
<p><code>Y -0,6977479</code></p>
<p><code>Z -4,06438E-10</code></p></td>
<td><p><code>W 0,4143499</code></p>
<p><code>X 1,083535E-08</code></p>
<p><code>Y -0,9101182</code></p>
<p><code>Z 1,083535E-08</code></p></td>
</tr>
<tr class="even">
<td><p><code>W 0,999722</code></p>
<p><code>X -2,236551E-08</code></p>
<p><code>Y 0,02360464</code></p>
<p><code>Z -2,236551E-08</code></p></td>
<td></td>
<td><p><code>W 0,009913659</code></p>
<p><code>X 2,163797E-08</code></p>
<p><code>Y -0,9999511</code></p>
<p><code>Z 2,163797E-08</code></p></td>
</tr>
<tr class="odd">
<td><p><code>W 0,9082747</code></p>
<p><code>X -2,899485E-08</code></p>
<p><code>Y 0,418374</code></p>
<p><code>Z -2,899485E-08</code></p></td>
<td><p><code>W 0,7155288</code></p>
<p><code>X -3,090637E-08</code></p>
<p><code>Y 0,6985834</code></p>
<p><code>Z-3,090637E-08</code></p></td>
<td><p><code>W 0,3556925</code></p>
<p><code>X -2,820028E-08</code></p>
<p><code>Y 0,9346039</code></p>
<p><code>Z -2,820028E-08</code></p></td>
</tr>
</tbody>
</table>

Notice that the rotations are the same as they were on the opposite
square in the previous table.

[Category:Modding](Category:Modding "wikilink") [Category:Model
making](Category:Model_making "wikilink")
[Category:Furniture](Category:Furniture "wikilink")
[Category:Guides](Category:Guides "wikilink") [Category:Modding
Guide](Category:Modding_Guide "wikilink")
[Category:FCS](Category:FCS "wikilink")