---
title: Filters, Equalizer & Presets
description: 
published: 1
date: 2025-04-30T10:46:07.963Z
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

## Distortion
| Parameter   | Default Value | Min Value | Max Value |
|-------------|---------------|-----------|-----------|
| Sin Offset  | 0             | 0         | 5        |
| Sin Scale   | 1             | 0         | 5        |
| Cos Offset  | 0             | 0         | 5        |
| Cos Scale   | 1             | 0         | 5        |
| Tan Offset  | 0             | 0         | 5        |
| Tan Scale   | 1             | 0         | 5        |
| Offset      | 0             | 0         | 5        |
| Scale       | 1             | 0         | 5        |

## Karaoke
| Parameter     | Default Value | Min Value | Max Value |
|---------------|---------------|-----------|-----------|
| Level         | 1             | 0        | 5        |
| Mono Level    | 1             | 0        | 5        |
| Filter Band   | 220           | 0        | 220        |
| Filter Width  | 100           | 0        | 100        |

## Lowpass
| Parameter  | Default Value | Min Value | Max Value |
|------------|---------------|-----------|-----------|
| Smoothing  | 20            | 0.5        | 20        |

## Rotation
| Parameter  | Default Value | Min Value | Max Value |
|------------|---------------|-----------|-----------|
| Frequency  | 0             | 0        | 5        |

## Timescale
| Parameter | Default Value | Min Value | Max Value |
|-----------|---------------|-----------|-----------|
| Speed     | 1             | -1        | -1        |
| Pitch     | 1             | -1        | -1        |
| Rate      | 1             | -1        | -1        |

## Tremolo
| Parameter | Default Value | Min Value | Max Value |
|-----------|---------------|-----------|-----------|
| Frequency | 2             | -1        | -1        |
| Depth     | 0.5           | -1        | -1        |

## Vibrato
| Parameter | Default Value | Min Value | Max Value |
|-----------|---------------|-----------|-----------|
| Frequency | 2             | -1        | -1        |
| Depth     | 0.5           | -1        | -1        |

## Channel Mix
| Parameter       | Default Value | Min Value | Max Value |
|------------------|---------------|-----------|-----------|
| Left to Left     | 1             | -1        | -1        |
| Left to Right    | 0             | -1        | -1        |
| Right to Left    | 0             | -1        | -1        |
| Right to Right   | 1             | -1        | -1        |


> All filters will show minimum and maximum values in the command descriptions.
{.is-info}

# Filter Presets <span style="background-color: rgb(253, 172, 65); color: black; padding: 3px 7px; font-size: 12px; border-radius: 5px;">Premium Only</span>

| Preset Name   | Description                                                                                                                                                   | Command                        |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Nightcore     | Speeds up the music while applying a slightly higher pitch.                                                                                                  | `/filterpreset nightcore`     |
| Vaporwave     | Slows down the music while applying a slightly lower pitch.                                                                                                  | `/filterpreset vaporwave`     |
| 8D Audio      | 'Rotates' the music to provide a more interesting listening experience.                                                                                      | `/filterpreset 8d`            |
| Reverb        | Adds echo to create a more dynamic sound space.                                                                                                               | `/filterpreset reverb`        |
| Bass Boost    | Boosts the overall bass in the song.                                                                                                                          | `/filterpreset bassboost`     |
| Chipmunk      | Speeds up the music and increases the pitch for a playful, iconic sound.                                                                                      | `/filterpreset chipmunk`      |
| Darth Vader   | Deepens the music to provide a more ominous, dark tone.                                                                                                       | `/filterpreset darthvader`    |
| Slow Mo       | Slows down the music to create a dramatic, slow-motion effect.                                                                                                | `/filterpreset slowmo`        |
| Speed         | Speeds up the music for a faster listening experience.                                                                                                        | `/filterpreset speed`         |
| Vibrate       | Applies a vibration effect to the music for an unusual and dynamic experience.                                                                                | `/filterpreset vibrate`       |

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