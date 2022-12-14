---
stub: true
tags:

- game client

---

# Client

## Introduction

osu!(lazer) is the next major update to the game. It is the culmination of several years of work behind the scenes to painstakingly reimplement the game.

The eventual goal is that this version will be released as an update which will completely supersede the existing stable version of the game, but there's still some work to be done before that is feasible. At the end of the day, **the players** will dictate when this happens and we will continue to support the previous release until users have migrated across.

## Feature comparison

Following is a comprehensive list of the **current state** of lazer in comparison to stable. Note that this is a moving target – the end goal is to implement all the features that players care about over time.

### Compatibility and performance

|                              |                 stable                  |                               lazer                                |
|:-----------------------------|:---------------------------------------:|:------------------------------------------------------------------:|
| Windows 8.0 and lower        |                    ✅                    |                                 ❌                                  |
| macOS / linux                |           🟠<br/>(using wine)           |                                 ✅                                  |
| Direct X / Vulkan            | 🟠<br/>(directx via compatibility mode) |                        ❌<br/>(coming soon)                         |
| Mobile support               |                    ❌                    |                                 ✅                                  |
| Multithreaded architecture   |                    ❌                    |                                 ✅                                  |
| UI scaling                   |                    ❌                    |                                 ✅                                  |
| Custom rulesets (game modes) |                    ❌                    |                     🟠<br/>(manually via dll)                      |
| De-duped file store          |                    ❌                    | ✅<br/>(beatmaps and skins will share files and save on disk space) |

### Gameplay and skinning

|                      | stable |         lazer          |
|:---------------------|:------:|:----------------------:|
| Skin support (osk)   |   ✅    | 🟠<br/>(gameplay only) |
| In-game skin editing |   ❌    |           ✅            |
| Mod presets          |   ❌    |           ✅            |
| Per-mod settings     |   ❌    |           ✅            |
| New "fun" mods       |   ❌    |           ✅            |

### Online systems

|                                       |               stable                |                                lazer                                 |
|:--------------------------------------|:-----------------------------------:|:--------------------------------------------------------------------:|
| Score submission                      |                  ✅                  |           🟠<br/>(scores will be reset to ensure balance)            |
| Beatmap leaderboards                  |                  ✅                  | 🟠<br/>(scores will be reset, currently isolated from stable scores) |
| Profile statistics                    |                  ✅                  |                                  ✅                                   |
| Medals                                |                  ✅                  |                                  ❌                                   |
| Performance points                    |                  ✅                  | 🟠<br/>(scores will be reset, currently isolated from stable scores) |
| Real-time chat                        |                  ❌                  |                                  ✅                                   |
| Wiki / News / Changelog / Rankings    |                  ❌                  |             ✅<br/>(native access to most online content)             |
| Beatmap listing                       | 🟠<br/>(osu!direct, supporter only) |                                  ✅                                   |
| Changelog                             |                  ❌                  |                                  ✅                                   |
| Unlimited size multiplayer rooms      |        ❌<br/>(16 player max)        |                                  ✅                                   |
| Multiplayer spectating                |                  ❌                  |                                  ✅                                   |
| Tag coop                              |                  ✅                  |                                  ❌                                   |
| Playlists (user-curated leaderboards) |                  ❌                  |                                  ✅                                   |
| Updating beatmaps with online changes |          🟠<br/>(map only)          |                          ✅<br/>(all files)                           |

### Editor

|                     | stable |                                               lazer                                                |
|:--------------------|:------:|:--------------------------------------------------------------------------------------------------:|
| osu!taiko editor    |   ❌    |                                                 ✅                                                  |
| osu!catch editor    |   ❌    |                                                 ✅                                                  |
| osu!mania editor    |   ✅    |                                                 ✅                                                  |
| Open as reference   |   ✅    |                                                 ❌                                                  |
| Beatmap submission  |   ✅    |                                                 ❌                                                  |
| Cross-compatibility |   ✅    | 🟠<br/>(some editor features will cause beatmap to play incorrectly in stable, will be fixed soon) |

## Switching to lazer

So you've decided you want to give lazer a shot? Great!

TODO

## FAQ

### Is stable going away? Am I going to be forced to switch?

### Can I import all my data from stable to lazer?

Currently, beatmaps, skins, scores, replays and collections can be imported into lazer. Of note, **settings are not yet imported** so you will need to set them up from scratch.

### If I install lazer, will I be able to return to stable?

Yes, lazer always installs alongside stable. Unless you choose to delete one or the other, both will be accessible.

### If I set a score on lazer, will it show on my profile?

Scores will show under "recently played" but not in "best performance" yet.

### If I set a score on lazer, will it contribute to my pp?

Scores will already have pp calculated (you can see this in "recently played"), but it will not contribute to your total "pp" value yet.

### Does lazer use ScoreV2?

### If I set a score on lazer, will it remain forever?

While we will try to preserve as many scores as possible, we **offer no guarantee that scores will remain indefinitely**. At any point we may choose to wipe a subset or all scores in order to preserve game balance.

### Will scores set on stable eventually show in lazer?

Yes. Once we finish balancing the combination of lazer and classic scores, both will be visible.

### How do I access my songs folder?

### Now that "osu!direct" is available to all players, will supporters have any new benefits?

### Will all mods be "ranked"?

### I don't like the new gameplay mechanics. Can I restore the old gameplay mechanics like on stable?

### If I cheat on lazer will I be banned?

Suck a dick, yes you will be banned.

### Where are the micro-transactions?
