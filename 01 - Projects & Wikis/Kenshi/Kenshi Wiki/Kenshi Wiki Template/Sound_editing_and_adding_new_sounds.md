*I myself have no experience on sound editing, these tidbits have been
collected from the mod development section in Kenshi Discord (and
reddit). The knowledge is from BoronGorax(Boron). trulythepawn and
Paladin Big Bollocks. And
[this](https://www.reddit.com/r/Kenshi/comments/v2iach/sound_modding_cracked/)
reddit post* -Cattrina

## Facts (so far, may be subject to change)

- The program to compile .bnk files: Wwise [Wwise
  website](https://www.audiokinetic.com/en/products/wwise/) They have
  plenty of video tutorials.
- Learn how wwise handles events and overrides.
- Make sure you own the rights to the sounds you are compiling.
- No program can open .bnk files and give you the names of the files
  (compiling to .bnk encrypts the files)
- The creators of Re_Kenshi are working on a list of ingame sounds, but
  it is not top on their to-do list
- As the game engine does not load sound files from mods, the end user
  either needs to manually place the new.bnk file in the installation
  folder, or to use Re_Kenshi, which will do the placing automatically.
  If the latter, you as a modder must set that up.
- You can edit the resources.cfg file to allow your mod to path to new
  audio files.
- You cannot make new **emitters** for buildings (at least we currently
  do not know how), so all you can do is to replace a vanilla sound (use
  the same vanilla filename for the sound in Wwise) and atm we do not
  know many actual sound file names
- You can attach sounds to animations and it looks like the FCS allows
  you to use any file name you want. These are called **'events**'. So
  instead of continuous sound the emitters make, event is a one time
  play only.
- In each .bnk there are scores of sounds and 4-5 variations of each
  sound, which makes replacing them with new original sounds pretty
  tedious. And as we do not know their names, impossible atm.

### About vanilla file editing

At this time we cannot really overwrite vanilla files. We cannot unpack
the vanilla .bnk sound files legally and even if we did, we would not
know the names of the individual sounds (that is a feature of the.bnk,
it encrypts file names). The only legal method we have to use is to play
the sound in game knowing which sound we set it to play. Re_Kenshi makes
this a bit easier, but I am not sure if that feature is released yet.
What makes this hard is the variations of the sounds. So playing
'reload' will give a different sound randomly each time and we do not
know if they all have the same name in the .bnk or what.

To be able to replace one vanilla sound, we need to figure all the names
of the sounds and variation in the same .bnk so we could overwrite the
entire vanilla .bnk in the game files with a complete list of new sounds
we made ourselves. It will not help to have a new bank with one file in
it, cause to overwrite vanilla files, we would need to name it
identically to a vanilla .bnk, effectively deleting all the other sounds
that were in that .bnk from the game.

In an older version of Kenshi, you can opt into through the beta
settings, actually **has part of the early soundbanks decoded in a text
file.** We are allowed to peruse that.

So, at this time, we can only add new sounds that will play along with
an animation.

## How to get rid of the sound at the start of the game

*"You can use states. They reset when you shut down the game but I used
a state to have a different sound for starting new game from menu vs.
loading a quicksave"*. -Boron

\[to be included an actual how to when I figure this out\]

## How to adjust sfx volume (to hear when zoomed out)

In
[this](https://www.reddit.com/r/Kenshi/comments/f9f854/how_to_increase_the_sounds_npc_wildlife_enemies/)
reddit post on Feb 25th 2020 the user erikmalkavian gives us the how to
edit sfx sound volumes, so you can hear the sounds when the camera is
further away.

- Open Settings.cfg in Administrator Mode with Notepad
- Adjust the Settings.cfg sounds.
- Footsteps to 50 and SFX to 15.

## From Media about sounds and music in Kenshi

[Initial Audio Demo](https://www.youtube.com/watch?v=jgz-89c8fXI) by
Kole Audio Solutions June 26th 2013

[A Full Explanation of Kenshi's Music
System](https://www.youtube.com/watch?v=wPEJRJWHz4k) December 2013 by
Kole Hicks

[Revealing the Score - Kenshi: Main
Title](https://www.youtube.com/watch?v=TB9T0gLI5g0) August 2014 by Kole
Hicks

[Audiokinetic blog January 17,
2017](https://blog.audiokinetic.com/en/gdc17-around-the-corner-game-audio/)

*[“Unscoring the World of
'Kenshi',”](https://www.youtube.com/watch?v=I2rmPPdrKfQ) \[filmed 2017
in GDC talk, video reuploaded 2021\] by Kole Audio Solutions Composer &
Sound Designer Kole Hicks, and Lo-Fi Games Ltd. Creator Chris Hunt, is
another important presentation that will demonstrate the project’s audio
system in Wwise."*

*"Silence is good"* -Kole Hicks 2017

You can see some of the early music and sound file names in the video.

This bit of info is from the sound track DLC:

*"The music system in Kenshi has been designed in such a way, that as
you play through the game the engine randomly selects from a handful of
different musical elements to create new compositional excerpts. It is
this ambient approach and "non-player interactivity" of the music that
reinforces Kenshi's indifferent tone. Obviously for a traditional
Soundtrack release we can not recreate the randomization of this music
system (yet). However, we can get close and musically sculpt each track
with wide brushstrokes to capture the same feeling."*

## Quotes on sound editing

\[Cattrina's notes in square brackets\]

### August 2018 AMA Chris Hunt on sounds

In the
[AMA](https://www.reddit.com/r/IAmA/comments/cnmwen/my_names_chris_hunt_game_developer_behind_kenshi/)
August 2018 Chris Hunt talks briefly of Wwise:

**spacefiddle:** *"What are the plans regarding modding for the sequel,
in general? I am especially interested in getting at sounds."*

**Chris:***"The audio system uses Wwise, which unfortunately packs
everything up so they can't be modded. It might be possible to add
overrides in the new engine"* \[talking about K2\]

This is basically all we got about sound editing in Kenshi. Chris does
not say anything for or against it. Just that it is rather impossible.

### January 2023 Paladin and Boron discuss about how to on Discord

**Paladin Big Bollocks:** *"Well okay so, I generated the .bnk file with
the sound effect I wanted to use in wwise, but where I'm confused is how
to point that to a mod (shoddy firearms in this case). Is that done
through the json file? Because in FCS under the "gun stuff" section for
crossbows, you have your usual sounds from the original stock file, but
I'm totally at a loss as to how to point this new sound to that"*

**Boron:** *"SFX are called by animations, so add you bank to the JSON
and then make an animation call it Oh that. So for LITA I had to rebuild
the whole attack event (for animals and weapons) but you could Change
the reload anim for the muskets with a bang"*

**Paladin Big Bollocks:** *"Has anyone tried decompressing the stock
.bnk files and adding new entries?"*

**Boron:** "*Soundbanks don't work like that. Each event uses IDs and
they're encrypted on build. There's no way to reverse the encryption or
add new stuff to compiled banks. It is possible to swap out sounds
inside a bank but it's an annoying and tedious process. **Making new
banks is the easiest and fastest way of doing it**. That being said, the
IDs are referenced by Kenshi by name internally and **ReKenshi has an
option to print the string names of event IDs, states, and switches in
the debug log"***

*
***Paladin Big Bollocks:** So far I've assigned the sound fx from wwise
by going into the reload animation, and then adding an event to that.
The event has the sound fx assigned to it....not sure if I'm going about
this right So far it's not registering the sound effect so it's either
I'm going about this wrong, or I exported the sound file in the wrong
wav format but I don't think its that

Edit; I figured out what I was doing wrong. When I went into wwise I
gave the file a random name instead of a proper one to replace like
"Reload". It works but now I need to bind the sfx to a better trigger
than reload. Probably end up using the harpoon turret for that.

[Category:Wip](Category:Wip "wikilink") [Category:Modding
Guide](Category:Modding_Guide "wikilink")
[Category:Modding](Category:Modding "wikilink")