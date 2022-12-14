---
stub: true
tags:

- game client

---

# Client

## Introduction

osu!(lazer) is the next major update to the game. It is the culmination of several years of work behind the scenes to painstakingly reimplement the game.

The eventual goal is that this version will be released as an update which will completely supersede the existing stable version of the game, but there's still some work to be done before that is feasible. At the end of the day, **the players** will dictate when this happens and we will continue to support the previous release until users have migrated across.

"lazer" is a codename and will eventually be dropped as it becomes the primary release of the game. The rest of this document will refer to osu!(lazer) as "lazer" and osu!(stable) as "stable" for simplicity.

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

|                            | stable |         lazer          |
|:---------------------------|:------:|:----------------------:|
| Skin support (osk)         |   ✅    | 🟠<br/>(gameplay only) |
| Song select grouping modes |   ✅    |           ❌            |
| In-game skin editing       |   ❌    |           ✅            |
| Mod presets                |   ❌    |           ✅            |
| Per-mod settings           |   ❌    |           ✅            |
| New "fun" mods             |   ❌    |           ✅            |

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
| User profiles                         |                  ❌                  |                                  ✅                                   |
| Beatmap listing                       | 🟠<br/>(osu!direct, supporter only) |                                  ✅                                   |
| Changelog                             |                  ❌                  |                                  ✅                                   |
| Unlimited size multiplayer rooms      |        ❌<br/>(16 player max)        |                                  ✅                                   |
| Multiplayer spectating                |                  ❌                  |                                  ✅                                   |
| Tag coop                              |                  ✅                  |                                  ❌                                   |
| Playlists (user-curated leaderboards) |                  ❌                  |                                  ✅                                   |
| Updating beatmaps with online changes |          🟠<br/>(map only)          |                          ✅<br/>(all files)                           |

### Editor

|                     | stable |                                                lazer                                                |
|:--------------------|:------:|:---------------------------------------------------------------------------------------------------:|
| osu!taiko editor    |   ❌    |                                                  ✅                                                  |
| osu!catch editor    |   ❌    |                                                  ✅                                                  |
| osu!mania editor    |   ✅    |                                                  ✅                                                  |
| Open as reference   |   ✅    |                                                  ❌                                                  |
| Beatmap submission  |   ✅    |                                                  ❌                                                  |
| Cross-compatibility |   ✅    | 🟠<br/>(some editor features will cause beatmaps to play incorrectly in stable, will be fixed soon) |

## Switching to lazer

So you've decided you want to give lazer a shot? Great!

You can find it for download [here](https://github.com/ppy/osu#running-osu). In the near future, you will be able to switch to lazer from stable (from the "Release stream" setting) and find the download on the osu! website.

## FAQ

### "stable" and "lazer"

#### Is stable going away? Am I going to be forced to switch?

Stable will continue to be maintained as long as users are using it. At very least, it will be maintained for several years.

#### Can I import all my data from stable to lazer?

Currently, beatmaps, skins, scores, replays and collections can be imported into lazer. Of note, **settings are not yet imported** so you will need to set them up from scratch.

#### If I import my beatmaps to lazer, will it use double the disk space?

If you have both lazer and stable on the same drive, we use [hard links](todo) to avoid using extra disk space.

In all other cases, importing beatmaps will use double the disk space.

#### If I delete lazer will it break my stable install?

No.

#### If I delete stable will it break content in lazer that was imported from stable?

No.

#### If I install lazer, will I be able to return to stable?

Yes, lazer always installs alongside stable. Unless you choose to delete one or the other, both will be accessible.

#### Can I import data from lazer to stable?

No. This will not be supported.

That said, individual scores and beatmaps can be exported from lazer and manually imported into stable for now.

### Gameplay and scoring

#### If I set a score on lazer, will it show on my profile?

Scores will show under "recently played" but not in "best performance" yet.

#### If I set a score on lazer, will it contribute to my pp?

Scores will already have pp calculated (you can see this in "recently played"), but it will not contribute to your total "pp" value yet.

#### Does lazer use ScoreV2?

Lazer currently uses a new experimental score implementation which is similar to ScoreV2 but not the same. This is still in development and we are looking for more feedback on how it feels in various contexts (solo play, leaderboards, tournaments etc.)

#### If I set a score on lazer, will it remain forever?

While we will try to preserve as many scores as possible, we **offer no guarantee that scores will remain indefinitely**. At any point we may choose to wipe a subset or all scores in order to preserve game balance.

#### Will scores set on stable eventually show in lazer?

Yes. Once we finish balancing the combination of lazer and classic scores, both will be visible.

#### Will all mods be "ranked"?

#### I don't like the new gameplay mechanics. Can I restore the old gameplay mechanics like on stable?

### Skinning and UI

#### Will old skins eventually work in song select and results screens?

We'll do our best to bring back as much of this as we can without blocking new functionality. This will come later on.

#### Can I use my skin cursor in the menus as well?

We will likely bring back support for this in the future due to popular demand.

### Feedback

#### A feature is missing that I depend on!

There's a very high chance we are already aware of this and tracking it for future implementation! Please search [here](https://github.com/ppy/osu/issues) and [here](https://github.com/ppy/osu/discussions). If you can't find any matching discussion threads, feel free to [open a discussion](https://github.com/ppy/osu/discussions/new).

#### Something has changed and I don't like it. What should I do?

There's a very high chance someone else has the same feedback and we are aware of it! Please search [here](https://github.com/ppy/osu/issues) and [here](https://github.com/ppy/osu/discussions). If you can't find any matching discussion threads, feel free to [open a discussion](https://github.com/ppy/osu/discussions/new).

#### I have found a bug, what's the best way to report it?

There's a very high chance someone else has the same feedback and we are aware of it! Please search [here](https://github.com/ppy/osu/issues) and [here](https://github.com/ppy/osu/discussions). If you can't find any matching discussion threads, feel free to [open a discussion](https://github.com/ppy/osu/discussions/new).

Do note that we are already tracking over 1,000 issues of varying priorities, and it may take us some time to fix issues that only affect a small number of users.

### Other things

#### How do I access my songs folder?

#### Now that "osu!direct" is available to all players, will supporters have any new benefits?

Some filters in the beatmap listing are still supporter only.

There are also some additional benefits already:

- Supporters can create playlists that last longer

We do intend to look into new benefits in the future, but our focus is currently on feature parity with stable so please use your supporter tag purchase as a way to.. support the game's development!

#### If I cheat on lazer will I be banned?

Yes.

#### If I find someone cheating on lazer how should I report them?

The same way you usually would.

#### Where are the micro-transactions?
