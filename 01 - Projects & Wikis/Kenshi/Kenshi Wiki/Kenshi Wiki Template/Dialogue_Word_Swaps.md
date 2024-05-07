See also: [Simple Dialogue Modding
Guide](https://steamcommunity.com/sharedfiles/filedetails/?id=804686889)

Use word swaps to give flare to your speaker.

They can react to many conditions or the speaker may have specific
personality. So instead everyone greeting 'Hi' make the grumpy ones say
'What?' and the kind ones say ' Hi Hello, nice to meet you'. And maybe
honorable ones say: 'How can I serve?' You can also make a list of
greetings to be shuffled every time.

It will also be convenient to you, as you do not have to make every (if
speaker is kind, then say this) line for every personality in the main
script, you can have just this one option with word swap taking care of
the personalities. Keeps the tree cleaner and easier to bug hunt too.

How to: Make a new word swap file, give it a name in caps fe.
DRIFTERRECRUITGREETINGS. And whenever you want an option raffled in
dialogue, you refer to it like this ''/DRIFTERRECRUITGREETINGS/, state
your business'. Caps, because it makes it easier for you to later see it
is a word swap.

There are also couple of word swaps not listed anywhere, they are:

/MYNAME/ - Displays current speaker’s name (the player char or the host,
not interjector)

/YOURNAME/ - Display’s current target’s name

/TARGETFACTION/ - Displays current target’s faction

/PLAYERFACTION/ - (Fallback for /TARGETFACTION/) Display’s player’s
faction name, use on passive monologues where the player has not
clicked.

/COST/ - Displays value used in conditions for that dialogue line

[Category:Dialogue](Category:Dialogue "wikilink")