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



## FAQ

### Now that "osu!direct" is available to all players, will supporters have any new benefits?
