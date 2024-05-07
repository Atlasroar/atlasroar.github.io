Blunt resistance, Cut resistance, Cut resistance efficiency *(previously
Stun)*, Harpoon resistance, and Coverage are statistics on pieces of
armour that affect how much [Damage](03%20-%20Projects%20&%20Wikis/Kenshi/Kenshi%20Wiki/Kenshi%20Wiki%20Template/Damage.md "wikilink") a unit takes
from another unit's attack.

## Coverage

Coverage is simply the chance that armour will protect against a hit to
that limb. So a 100% chest coverage will apply its resistances on every
hit to the chest. While a 50% coverage will only do it half the time.
Meaning that 80% coverage does not translate to covering 80% of the
Damage Taken calculated for this hit, but that for 20% of hits the
armour will offer no protection.

### Layering

In the case of overlapping coverage areas, damage resistance is
determined based on the slot the items use. It will run through them in
order of: Head, Armor (Chest), Pants, Shirt, and then Boots.
Environmental resistances are a sum total.

## Damage Resistance

#### **Blunt Resistance**

Whenever an attack successfully hits a unit, the damage is theoretically
calculated as follows:

AD: Attack damage / "Raw damage"
BR : Blunt/Cut resistance / "Armour effect"
DR: Damage resistance / "Toughness effect"

> *Damage taken = AD \* (1 - BR) \* (1 - DR)*

For example, say a 100 Blunt Damage attack is going to hit your
character's chest (not blocked) while they are wearing a Standard Grade
[Plate Jacket](Plate_Jacket.md "wikilink"), which has 14% blunt resistance.
Your unit has a toughness of 70, which gives a 26% (0.26x damage
resistance). So, our final number would look like this:

> *100 \* (1 - 0.14) \* (1 - 0.26) = 100 \* 0.86 \* 0.74 = 63.64 damage
> taken*

#### **Cut Resistance and Efficiency**

Cutting Damage uses the same initial calculation, but triggers a Damage
Conversion calculation. All *resisted* cut damage is then applied
against the Cut Resistance efficiency (CRE) statistic to determine how
much of the resisted damage is carried over as unmitigated Blunt
(*previously calculated as Stun*) damage. 90% is the maximum cut
resistance possible on a single piece of armour.

For example, lets use 75% cut resistance and 60% cut resistance
efficiency with no Toughness modifier for simplicity. Your character is
hit for 50 cut damage. The armour negates 37.5 damage applying the
formula above, sending the remaining 12.5 to be applied to any
overlapping armour. The 37.5 resisted cut damage goes through the
following (*Stun)* calculation:

> (*Stun) Damage = Resisted Cut Damage \* (1 - CRE) = 37.5 \* (1 - 0.60)
> = 37.5 \* 0.4 = 15 damage*

This (*Stun)*damage will be converted to blunt and instantly applied
(ignoring any other armour). This means that if you had no other armour
you took a total of 27.5 damage, 12.5 cut and 15 blunt. Keep in mind
though, this (*Stun)*damage ignores further layers of armour. So you may
want to avoid armour with a low Cut resistance efficiency value in slots
that get hit early on in the order.

The total cut resistance of an armor is CR \* CRE, which is 45% for the
example above.

Also, there are other factors to consider for damage calculation, as
[Shidan](User:Shidan "wikilink") explains in this thread (*outdated*):

<https://steamcommunity.com/app/233860/discussions/2/133261907145702720/>

## Harpoon Resistance

This is simply the amount of damage points that goes through the armour
pieces cut resistance/efficiency when hit by a harpoon or crossbow on a
body part this armour covers. Unlike cut damage you will not receive any
of the cut the resistance did not prevent until going past the value an
armour piece has. Example, if hit in the chest by a crossbow for 20
damage and the armour you have on has 15 harpoon resist then 15 will go
through the cut resist/eff of the armour to find how much stun damage
you take, and the remaining 5 will be taken as unmitigated cut damage.
If you happen to be wearing an armour piece with 100% cut efficiency you
will take 0 stun damage from the shot.

## Penalties and Bonuses

Most armours have penalties to certain skills. These are shown as 0.67x
or something similar. This means that skill will only function at that
percentage of your skill level. So a 50 skill would only function at
33.5 using the previous number as an example. If you have multiple
penalties across all your armour all the factors are multiplied, e.g.
two equipped items with a 0.9x: 1 - (0.9\*0.9) = 1-0.81 = 19% penalty.
Some penalties are reduced at higher armour qualities.

## Armour Penetration

While this stat is for weapons, it is still should be noted as this stat
can make a difference. Basically, the % of armour penetration (AP) of
weapon will directly affect the current BR/CR of the armour of their
enemy. Ex: You have 50 Toughness (0% DR) and are wearing a
\[Masterwork\] [Crab Armour](Crab_Armour.md "wikilink"). It has 66.5% blunt
resist, 90% cut resist and 90% cut efficiency.

If struck by an enemy with a weapon which has 30% armour penetration for
100 blunt damage you would take 53.45 damage. As the weapon had 30%
armour penetration your blunt resistance when hit was treated as 46.55%
as 66.5(1-0.3)=46.55. In the end the result is 100(1-0.4655) which ends
up as 53.45.

If the enemy also did 100 cut damage to us with the 30% armour
penetration weapon the result would be 37 cut and 9 stun damage. At the
90% cut resist multiplied by 1-0.3 would treat it as if it was only 63%
cut resist. The usual cut damage it would have mitigated before armour
penetration is still applied, which is why we take 9 stun damage instead
of taking 6.3.

A lot of weapons have negative armour penetration, which can be
extremely useful however it can also be useless. A single piece of
armour cannot resist more than 90% of cut damage received. As a result
of that, if we were to take 100 cut damage from a weapon with -30%
Armour Pen (Like a [Katana](Katana.md "wikilink")), we would still receive
10 cut and 9 stun damage just as if we were hit by an attack which had
no negative armour penetration at all. Oddly enough if you were to
instead wear \[Specialist\] Crab Armour (78% Cut resist) you would end
up taking less damage than wearing the Masterwork version. The 30%
armour pen would affect the 78% cut resist like so; 1.3x0.78 = 101.4. Of
course, you cannot have more than 90% cut resist but the important thing
to note is that you will still take only 7.8 stun damage due to the fact
that the armour penetration does not impact the cut resist into cut
efficiency formula as mentioned above. Resulting in a total damage taken
of 10 cut + 7.8 stun as opposed to 10 cut + 9 stun.

__NOTOC__ __NOEDITSECTION__

[Category:Guides](Category:Guides "wikilink")
[Category:Combat](Category:Combat "wikilink")