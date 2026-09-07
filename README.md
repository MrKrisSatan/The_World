# The World

> A living, multi-region Pokémon campaign for Gen1Recomp++.
> Your rivals do not wait for you. The weather does not stay still. The world keeps moving.

[![Latest release](https://img.shields.io/github/v/release/MrKrisSatan/The_World?label=latest&color=gold)](https://github.com/MrKrisSatan/The_World/releases/latest)
[![Supported games](https://img.shields.io/badge/games-Red%20%7C%20Blue%20%7C%20Yellow%20%7C%20Gold%20%7C%20Silver%20%7C%20Crystal-3b82f6)](#supported-games)
[![Gen1Recomp++](https://img.shields.io/badge/host-Gen1Recomp%2B%2B-7c3aed)](https://github.com/bryanthaboi/gen1recomp)

**Current release: 6.75.1**

[Download the latest release](https://github.com/MrKrisSatan/The_World/releases/latest) ·
[Installation](docs/INSTALLATION.md) ·
[Features](docs/FEATURES.md) ·
[Compatibility](docs/COMPATIBILITY.md) ·
[Report a bug](https://github.com/MrKrisSatan/The_World/issues/new?template=bug_report.yml)

The World expands Pokémon Red, Blue, Yellow, Gold, Silver and Crystal into a connected, persistent campaign spanning **11 regions** plus their Mirror counterparts. It combines regional progression, autonomous AI rivals, Weather FX, WX Pokémon, modern optional mechanics, Team Rocket campaigns, dynamic ecology, transport networks, double battles, tournaments, achievements and the signature **Atmospheric Resonance** battle mechanic.

## What is new in 6.75.1

6.75.1 is the Crystal / Gen 2 rival-challenge hotfix for [issue #3](https://github.com/MrKrisSatan/The_World/issues/3).

- Fixed World rivals failing to battle when challenged in Pokémon Crystal.
- Gold, Silver and Crystal now launch World-rival trainer battles through the host's native `World:startBattle` path.
- Both the interaction-menu **CHALLENGE** command and the older A-press challenge route use the same safe Gen 2 handoff.
- Rival dialogue and battle launch are separate stages, preventing the unsupported Gen 2 script-level trainer battle path from being called.
- Failed native battle launches release the rival transaction cleanly instead of leaving the interaction locked.
- All 6.75.0 Atmospheric Resonance, WX, ecology, Yellow, Johto, map/interior and Potato Voxel fixes are retained.

## Atmospheric Resonance 🌩️

Atmospheric Resonance is The World's signature battle mechanic. The Pokémon **does not transform**. Its bond with its trainer empowers the atmosphere around it.

High-friendship Pokémon can **RESONATE** once per battle, temporarily upgrading the current weather into a Resonant Field. The Pokémon keeps its normal sprite, form and typing throughout.

| Weather | Resonant Field | Temporary Resonance Move |
| --- | --- | --- |
| Rain | Resonant Rain | Monsoon Burst |
| Sun | Resonant Sun | Solar Eruption |
| Storm | Resonant Storm | Thunderheart |
| Snow / Hail | Resonant Snow | Whiteout |
| Sandstorm | Resonant Sand | Desert Wrath |
| Wind | Resonant Gale | Gale Rush |
| Fog | Resonant Fog | Phantom Mist |

Friendship controls the basic Resonance tier, from Minor through Perfect. Every individual Pokémon also develops persistent **Weather Affinity** by legitimately participating in battles under different weather conditions. Two Pokémon of the same species can therefore become specialists in completely different weather.

At maximum friendship, **Perfect Resonance** unlocks the strongest field tier and can use **Atmospheric Calling** when no battle weather exists. Matching WX Pokémon gain **True Resonance**, a modest specialist bonus rather than a giant raw multiplier.

AI trainers, Gym Leaders, major rivals and autonomous World rivals understand the mechanic. Resonance state is temporary, never permanently alters the four-move set, and is cleaned up on switch, faint, capture, fleeing and battle end.

## Eleven-region campaign

A fresh adventure can begin in:

- Kanto
- Johto
- Sevii Islands
- Almia
- Sinnoh
- Hoenn
- Unova
- Kalos
- Alola
- Galar
- Paldea

Regions can be completed in different orders. Later campaigns scale around the team you bring with you while retaining each region's local difficulty curve. Enemy trainers remain capped at level 100 until three regional Champion clears, after which high-end opponents may reach level 120. Player Pokémon remain capped at level 100.

Every region has its own Team Rocket campaign and regional progression. The additional regions are custom retro World campaigns built from the host's available map systems and tilesets. They are not intended to be exact reproductions of the original region-specific games.

Mirror-region counterparts and the wider Mirror Universe content are also integrated into the World campaign.

## Living AI rivals

World rivals are persistent trainers participating in the same campaign rather than fixed NPC battle scripts. Depending on personality, class, resources, relationships and recent history, they can:

- travel through towns, routes, caves and regional connections;
- catch, train, evolve, trade and store Pokémon;
- use Centers, Marts, TMs, HMs and the Robot Market;
- challenge trainers, Gyms, tournaments, Leagues, the player and one another;
- form friendships, rivalries, alliances and grudges;
- react to weather, ecology, Team Rocket activity and regional events;
- black out and recover instead of teleporting forward;
- develop Weather Affinity and use Atmospheric Resonance in legitimate battles.

When a rival accompanies the player, supported wild encounters can become companion double battles. The accompanying rival can make its own capture decision, spend its own Poké Ball and place the caught Pokémon into its own party or PC.

Performance budgets remain configurable so Android and handheld users can reduce autonomous simulation load.

## Weather FX and WX Pokémon

Weather FX **8.1.59** is embedded directly into The World. It drives dynamic overworld atmosphere, battle weather, seasons, regional weather identity and the environmental side of Atmospheric Resonance.

The World keeps a strict shelter policy: buildings, caves, dungeons, gates and ships do not receive outdoor environmental precipitation, fog, debris, lightning tint or weather-biased encounters.

WX Pokémon are persistent weather-associated forms with their own appearance, typing, abilities and encounter conditions. The 6.75 line restores The World's WX registration and encounter integration around Weather FX 8.1.59 while preserving compatibility with older saves.

WX support is defensive. Atmospheric Resonance still works when WX integration is disabled, absent or only partially available.

## Wild Pokémon and ecology

Ordinary generated route ecology is now intentionally conservative:

- legendary, mythical and event Pokémon are excluded from routine wild seeding;
- starter gift species are excluded from routine random population injection;
- fossils are excluded from ordinary habitat seeding;
- fully evolved and other evolution-target species are not injected as routine low-level wildlife;
- regional and authored encounter data remains the authority where explicitly defined.

This prevents early grass from turning into a roulette wheel of Regigigas, Shaymin, Feraligatr and other progression-breaking encounters.

Migration, extinction, regional populations, weather variants and persistent named encounters continue to operate through the World ecology layer.

## Yellow compatibility

Pokémon Yellow has additional protection because The World can introduce later-generation species and mechanics into a Gen 1 host.

- Random encounters are suppressed during the vulnerable pre-starter Oak sequence so the player cannot be spawn-killed before receiving Pikachu.
- Later-generation Pokémon receive functional compatibility learnsets rather than being stripped down to unusable Gen 1 leftovers when Modern Moves is disabled.
- Growth follows the active stat rules. Unsplit Gen 1 raises SPECIAL; split World / Gen 2 behavior raises Sp. Atk.
- Modern Pokémon party icons and summary screens use The World's hardened renderer path, including compatibility for species such as Dragapult.

## Johto repair layer

Imported Johto geometry is supplemented with World-owned progression where original Gold/Silver/Crystal map scripts are not available to the mod.

The 6.75 repair pass restores the early Elm → Mr. Pokémon → Elm progression and removes only the two Route 30 battle-scene blockers once that opening errand is complete. Ordinary trainers remain intact.

## Maps, buildings and regional navigation

The World preserves authored regional geometry instead of flattening generated towns and routes into a common lawn/grid layout. Interior creation includes return-warp validation so ordinary houses, Centers, Marts, labs and regional service buildings retain a usable exit.

The **MAPS** system always exposes the player's current region, even if a regional chart has not already been collected, and regional transport links continue to unlock as the campaign expands.

## Supported games

| Game | Support |
| --- | --- |
| Pokémon Red | Full Gen 1 World path |
| Pokémon Blue | Full Gen 1 World path |
| Pokémon Yellow | Full Gen 1 World path plus Yellow-specific starter and compatibility safeguards |
| Pokémon Gold | Full Gen 2 World path |
| Pokémon Silver | Full Gen 2 World path |
| Pokémon Crystal | Full Gen 2 / Crystal path, including the 6.75.1 rival-challenge hotfix |

The manifest supports Gen1Recomp++ host versions `>=0.1.37` and `<2.0.0`.

## Major systems

The current World package includes or integrates:

- Atmospheric Resonance and Weather Affinity
- 11 regional campaigns plus Mirror counterparts
- autonomous AI rivals and Mini Ultron planning
- Team Rocket stories in every region
- Weather FX 8.1.59
- WX Pokémon and WX abilities
- National Dex / modern Pokémon integration through Gen 9 content
- physical/special split support
- abilities and held items
- double battles and companion battles
- Robot Market, Wonder Trade and Mystery Gift
- regional TMs, HMs and department-store machine catalogs
- adaptive cross-region level scaling
- Nuzlocke options for player/rivals
- tournaments, relationships, factions and world news
- achievements, titles, classes and progression tracking
- migration, extinction and named persistent encounters
- Potato Voxel 1.9.6 compatibility

Most large systems are feature-detected so missing optional graphics or companion integrations fail soft instead of preventing the game from booting.

## Settings

World settings are designed to persist through Oak/Elm introductions, save/load and region transitions. The 6.75 repair pass restores the full option surface after a regression that could reset intro choices or leave rivals effectively stuck under Nuzlocke rules.

Important configurable systems include:

- Atmospheric Resonance
- WX Pokémon
- weather presentation
- abilities
- physical/special split
- rival simulation/performance budget
- rival Nuzlocke behavior
- generation scope
- EXP and UI conveniences
- optional battle and overworld presentation features

## Installation

1. Open the [latest release](https://github.com/MrKrisSatan/The_World/releases/latest).
2. Download `The_World_v6_75_1.zip`.
3. Import or extract it using the normal Gen1Recomp++ mod workflow.
4. Make sure the directory containing `manifest.json` is the actual mod root.
5. Enable **The World** in Mod Manager and start or load Red, Blue, Yellow, Gold, Silver or Crystal.
6. Back up an important save before upgrading a large active mod.

See the [complete installation and upgrade guide](docs/INSTALLATION.md).

## Compatibility

The World absorbs several formerly separate projects. Do **not** enable standalone duplicate copies of these alongside it unless a release note explicitly says otherwise:

- Weather FX
- AI Rivals
- Kanto Reforged
- National Dex
- Wonder Trade
- GameShark
- Double Battles

Optional integrations are capability-detected where practical. Potato Voxel 1.9.6 is explicitly supported, including its current first-person / 3D host exports and live battle HUD API.

See [docs/COMPATIBILITY.md](docs/COMPATIBILITY.md) for the repository compatibility guide.

## Save compatibility

Existing saves are intended to continue working across the 6.75 update line.

- Missing Weather Affinity begins safely at zero.
- Atmospheric Resonance battle state is never stored as permanent Pokémon form/type/moveset data.
- Existing WX Pokémon remain readable when WX spawning is disabled.
- New settings and compatibility metadata initialise lazily when absent.
- 6.75.1 does not require a new save for the Crystal rival-challenge fix.

Back up important saves before major updates. For migration reports, include both the previous and current World versions.

## Validation

The 6.75.1 release gate includes:

- Crystal / Gen 2 issue #3 challenge runtime: **28/28 checks passed**;
- Atmospheric Resonance matrix: **34/34 passed**;
- World structural harness: **33,071 checks, 0 failures**;
- generated-region geometry: **495 maps validated**;
- Weather FX validator: **124 passed, 0 failed** plus the dedicated 8.1.59 snow runtime **9/9**;
- Potato Voxel 1.9.6 compatibility and companion-double runtime checks;
- accompanied AI-rival catching regression checks;
- Lua syntax validation: **741 files, 0 failures**;
- final ZIP extraction and post-package smoke testing.

These automated/runtime harnesses are broad but do not replace device playtesting across every map and optional-mod combination. Reproducible player reports remain extremely useful.

## Reporting bugs

Use the [bug report form](https://github.com/MrKrisSatan/The_World/issues/new?template=bug_report.yml) and include:

- game and Gen1Recomp++ version;
- The World version;
- whether the save is new or migrated;
- current region and exact map;
- enabled optional mods and versions;
- relevant World / WX / weather / Nuzlocke settings;
- reproduction steps;
- screenshots and the complete Lua error or `lua-error.log` when available.

## Credits

The World incorporates and adapts work from AI Rivals, Weather FX, Kanto Reforged and bundled Kanto/Johto foundations. Battle backdrops include work credited to CDRX73, DerxwnaKapsyla, http404error and Game Freak. Weather audio uses the credited Relic Castle tutorial pack and royalty-free Pixabay sources. The 3D atmosphere integration is adapted from Kanto Dynamic Weather by Campo (`1-Camp0-1`). Additional notices remain bundled with the distributed mod.

Pokémon and related names and imagery belong to their respective owners. This is a fan-made project and is not affiliated with or endorsed by Nintendo, Creatures Inc. or GAME FREAK.

---

Traditional Pokémon games wait for the player. **The World does not.**
