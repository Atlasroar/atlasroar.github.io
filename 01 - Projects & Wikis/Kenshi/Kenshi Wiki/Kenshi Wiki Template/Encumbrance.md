<figure>
<img src="Encumbrance.png" title="Encumbrance.png" />
<figcaption>Encumbrance.png</figcaption>
</figure>

**Encumbrance** is the term used to define the amount of weight you can
carry, and at what speed you can do so. Every [item](Items.md "wikilink")
in the game has a weight value which contributes to your encumbrance.
Encumbrance is defined by multiple factors, such as
[Strength](Strength.md "wikilink") and location of the items in your
inventory. Penalties for exceeding your carry weight include loss of
movement speed, combat speed, martial arts, dodge and increased Hunger
Rate.

## Calculating Encumbrance

There a few factors to consider when calculating encumbrance, but the
main things to consider are:

- Strength directly affects your carry weight at a ratio of 1:1.
- When worn, items in your [backpack](Backpacks.md "wikilink") weigh less
  depending on the backpack. However, for a majority of them this comes
  at a reduction in combat skills and combat speed.
- [Equipment](Items.md#Equipment "wikilink") counts against your carry
  weight.
- Carrying a body counts as 30 weight.

To calculate base carry weight before backpacks are factored in, use
this formula.

> *`CharacterLevel+15`*

## States of Encumbrance

There are multiple different states of encumbrance, each which affect
your character's performance.

- Weightless - Anything less than 120% of your maximum carry weight is
  considered Weightless.
- Lightweight - Anything between 120% and 150% of your maximum carry
  weight is considered Lightweight.
- Moderate - Anything between 150% and 200% of your maximum carry weight
  is considered Moderate.

## Penalties

Dodge = Reduced by 1% per 1% Encumbrance. Max Penalty achieved once at
60% Encumbrance for a total of -60% Dodge.

Movement Speed = Reduced by 1% per 1% Encumbrance. Max Penalty achieved
once at 100% Encumbrance for a total of -100% movement speed (Shown
speed is 2mph at this point)

Hunger Rate = Increased by 0.007 per 1% Encumbrance. Max Penalty
achieved once at 100% Encumbrance for a total of +0.7x Hunger Rate.

Martial Arts = Reduced by 0.8% per 1% Encumbrance. Max Penalty achieved
once at 100% Encumbrance for a total of -80% Martial Arts.

Combat Speed = Reduced by 0.235% per 1% Encumbrance. Max Penalty
achieved once at 100% Encumbrance for a total of -23.5% Combat Speed.
(In other words, 0.765x Combat speed)

[Category:Guides](Category:Guides "wikilink")