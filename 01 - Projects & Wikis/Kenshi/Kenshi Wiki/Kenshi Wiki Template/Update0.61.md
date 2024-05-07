**Version 0.61** was an overhaul to the
[medical](Field_Medic.md "wikilink"), knock-out, bloodloss and body part
systems. It also introduced the [Toughness](Toughness.md "wikilink") stat.

__TOC__

## 0.61.0

I had a random moment of genius and came up with this idea to revamp the
medical system, I think it improves the combat and game balance pretty
nicely.

I’ve rushed it out already because there are important crash fixes that
needed releasing, but I also intend to implement leg damage properly, so
you have to crawl if your legs are damaged.

### The new rules to the medical system

- If a vital bodypart (head/chest/stomach) goes below 0, then it causes
  a knockout
- A knockout is based on a timer countdown. The time is a total of all
  the characters damage, including bloodloss (head counts for double
  time, limbs count for half)
- Once this timer counts down to 0, the character can get up again if
  his vital parts are still above -50
- Vital bodyparts slowly degenerate when they are below 0 (unless
  bandaged). So once its below -50, you will die without medical
  attention.
- Once a vital bodypart degenerates below the -50 point he will go into
  a coma and can’t wake up until all vitals are above 0 again.
- If blood goes below 0, he will KO. However once the KO timer runs out
  and blood goes above 0 and he gets up again, the next KO point for
  bloodloss will be -25. This allows him to fight a bit more, gets him
  closer to risk of death, and prevents the “constantly getting up then
  going down again in one hit” problem.
- So a character can get up and fight again with, say, -30 chest damage.
  He will go down again instantly if he is hit in the chest, and it will
  be worsening the whole time if he doesn’t get it bandaged
- As before if a vital bodypart reaches -100 then it means death
- If a non vital bodypart (eg an arm) goes below -100 then it will cause
  slow bloodloss until death. Eventually I will implement severance, so
  -100 will mean you lose the limb and will need a robotic replacement.

*The end result:*

After a battle, some characters may die, some may lose limbs, some will
go into prolonged comas, others will recover and heal themselves or die
later. They never get stuck in a limbo state where they are unconscious
forever. Battles are more interesting.

### New [Toughness](Toughness.md "wikilink") stat

- I said before that you reach a critical point of no return when your
  health goes below -50. That was a lie, the actual number is based on
  your toughness and can range from -10 to -80 if you are mega-tough.
- Toughness stat is increased primarily by getting hurt.
- Toughness has a huge XP bonus if you are fighting while critically
  wounded or crippled
- You earn a huge toughness XP reward if you force your characters to
  get up and fight again while they are down and “Playing dead” so that
  the enemy leaves. ‘Cus that’s a tough thing to do. The bonus is also
  multiplied by how many of them there are.
- Affects damage resistance instead of Melee Defence

### OTHER STUFF

- Way more bandits
- Stats window has more useful information, derived stats and training
  advice
- blood recovery rate reduced from 0.5 to 0.3
- Cannibals use clubs so victims don’t die on the way to the cages
- Cannibals are a little stronger to compensate for using clubs
- Fixed shopkeepers not coming back to their shops
- Fixed stats of Sleeveless longcoat
- Fixed that random crash that was going on
- Fixed some rare crash on load bug

<figure>
<img src="0.61_announcement_screenshot.jpg"
title="0.61_announcement_screenshot.jpg" />
<figcaption>0.61_announcement_screenshot.jpg</figcaption>
</figure>

## 0.61.1 - fixes

- Fixed interior buildings vanishing when you build something
- Fixed population sliders affecting shopkeepers (import)
- Fixed first building sometimes getting linked to wrong town for power
  consumption

[Category:Updates](Category:Updates "wikilink")