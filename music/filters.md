---
title: Filters, Equalizer & Presets
description: Advanced Discord music bot features - Equalizer, filters, and presets with Cakey Bot. Professional audio setup guide.
published: 1
date: 2024-12-04T06:23:30.785Z
tags: 
editor: markdown
dateCreated: 2022-10-18T08:06:53.977Z
---

# Custom Equalizer

You can set custom equalizer bands using the `/equalizer <band> <value>` command. There are 15 bands (**0-14**) that can be changed. gain is the multiplier for the given band. The default value is **0**. Valid values range from **-0.25** to **1.0**, where **-0.25** means the given band is completely muted, and **0.25** means it is doubled.

# Equalizer Presets <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>
You can also use our presets for those of you who just want a quick and easy solution by typing `/eqpreset <preset>`. Our presets include:

* Lowpass
* Highpass
* Bandpass
* None
* Extrabass
* Extratreble
* Bassandtreble
* Electronic
* Soft
* Pop
* Ear Rape

# Custom Filters <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>

You can also set custom filters on your music using the `/filter <name> <options>` command. If you'd like to revert these changes you can also type `/filter <name> reset`. If you run the `/nowplaying` command, it will show all of your currently applied filters as well. Our possible filters include:

* Distortion
  * Sin Offset - Default: 0
  * Sin Scale - Default: 1
  * Cos Offset - Default: 0
  * Cos Scale - Default: 1
  * Tan Offset - Default: 0
  * Tan Scale - Default: 1
  * Offset - Default: 0
  * Scale - Default: 1
* Karaoke
  * Level - Default: 1
  * Mono Level - Default: 1
  * Filter Band - Default: 220
  * Filter Width - Default: 100
* Lowpass
  * Smoothing - Default: 20
* Rotation
  * Frequency - Default: 0
* Timescale
  * Speed - Default: 1
  * Pitch - Default: 1
  * Rate - Default: 1
* Tremolo
  * Frequency - Default: 2
  * Depth - Default: 0.5
* Vibrato
  * Frequency - Default: 2
  * Depth - Default: 0.5
* Channel Mix
  * Left to Left - Default: 1
  * Left to Right - Default: 0
  * Right to Left - Default: 0
  * Right to Right - Default: 1

> All filters will show minimum and maximum values in the command descriptions.
{.is-info}

# Filter Presets <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>
* **Nightcore** is a special effect that speeds up the music while applying a slightly higher pitch to it. You can toggle this preset with the `/filterpreset nightcore` command.
* **Vaporwave** is a special effect that slows down the music while applying a slightly lower pitch to it. You can toggle this preset with the `/filterpreset vaporwave` command.
* **8D Audio** is a special effect that 'rotates' the music to provide a more interesting listening experience. You can toggle this preset with the `/filterpreset 8d` command.
* **Reverb** is a special effect that makes use of echo to create a more dynamic sound space for a song. You can toggle this preset with the `/filterpreset reverb` command.
* **Bass Boost** is a special effect that boosts the overall bass for the song. You can toggle this preset with the `/filterpreset bassboost` command.
* **Chipmunk** is a special effect that speeds up the music and icnrease the pitch to provide a more iconic listening experience. You can toggle this preset with the `/filterpreset chipmunk` command.
* **Darth Vader** is a special effect that deepens the music to provide a more ominous listening experience. You can toggle this preset with the `/filterpreset darthvader` command.
* **Slow Mo** is a special effect that slows down the music to provide a more interesting listening experience. You can toggle this preset with the `/filterpreset slowmo` command.
* **Speed** is a special effect that speeds up the music to provide a more faster listening experience. You can toggle this preset with the `/filterpreset speed` command.
* **Vibrate** is a special effect that 'vibrates' the music to provide a more interesting listening experience. You can toggle this preset with the `/filterpreset vibrate` command.

# Related Commands
Usage Key: `<required>` / `[optional]`
| Command                     | Description                                         | Usage                                                | Permission |
| :-------------------------- | :------------------------------------------------- | :-------------------------------------------------: | :--------: |
| /eqpreset | Applies a preset qualizer to the current song. | N/A | None | 
| /filter channelmix          | Applies a channelmix filter to the current song.   | \<leftotoleft> \<leftotoright> \<righttoleft> \<righttoright> | None       |
| /filter distortion          | Applies a distortion filter to the current song.   | \<Sin Offset> \<Sin Scale> \<Cos Offset> \<Cos Scale> \<Tan Offset> \<Tan Scale> \<Offset> \<Scale> | None       |
| /filter karaoke             | Applies a karaoke filter to the current song.      | \<level> \<monolevel> \<filterband> \<filterwidth>      | None       |
| /filter lowpass             | Applies a lowpass filter to the current song.      | \<smoothing>                                         | None       |
| /filter rotation            | Applies a rotation filter to the current song.     | \<rotation>                                          | None       |
| /filter timescale           | Applies a timescale filter to the current song.    | \<speed> \<pitch> \<rate>                              | None       |
| /filter tremolo             | Applies a tremolo filter to the current song.      | \<frequency> \<depth>                                 | None       |
| /filter vibrato             | Applies a vibrato filter to the current song.      | \<frequency> \<depth>                                 | None       |
| /filterpreset 8d            | Applies an 8D audio effect to the current song.    | N/A                                                 | None       |
| /filterpreset chipmunk      | Applies a chipmunk effect to the current song.     | N/A                                                 | None       |
| /filterpreset darthvader    | Applies a darth vader effect to the current song.  | N/A                                                 | None       |
| /filterpreset nightcore     | Applies a nightcore effect to the current song.    | N/A                                                 | None       |
| /filterpreset reverb        | Applies a reverb effect to the current song.       | N/A                                                 | None       |
| /filterpreset slowmo        | Applies a slow mo effect to the current song.      | N/A                                                 | None       |
| /filterpreset speed         | Applies a speed effect to the current song.        | N/A                                                 | None       |
| /filterpreset vaporwave     | Applies a vaporwave effect to the current song.    | N/A                                                 | None       |
| /filterpreset vibrate       | Applies a vibrating effect to the current song.    | N/A                                                 | None       |