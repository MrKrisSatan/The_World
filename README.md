# The World

> A living, multi-region Pokémon campaign for Gen1Recomp++.
> Your rivals do not wait for you. The world keeps moving.

[![Latest release](https://img.shields.io/github/v/release/MrKrisSatan/The_World?label=latest&color=gold)](https://github.com/MrKrisSatan/The_World/releases/latest)
[![Supported games](https://img.shields.io/badge/games-Red%20%7C%20Blue%20%7C%20Yellow%20%7C%20Gold%20%7C%20Silver%20%7C%20Crystal-3b82f6)](#supported-games)
[![Gen1Recomp++](https://img.shields.io/badge/host-Gen1Recomp%2B%2B-7c3aed)](https://github.com/bryanthaboi/gen1recomp)

**Current release: 6.54.15**

[Download the latest release](https://github.com/MrKrisSatan/The_World/releases/latest) ·
[Installation](docs/INSTALLATION.md) ·
[Features](docs/FEATURES.md) ·
[Compatibility](docs/COMPATIBILITY.md) ·
[Report a bug](https://github.com/MrKrisSatan/The_World/issues/new?template=bug_report.yml)

The World expands Pokémon Red, Blue, Yellow, Gold, Silver, and Crystal into a
connected campaign spanning Kanto, Johto, the Sevii Islands, Almia, Sinnoh,
and Hoenn. It combines authored regional progression with autonomous trainers,
dynamic weather and seasons, WX Pokémon, modern optional mechanics, scripted
world events, achievements, transportation networks, and persistent factions.

## Highlights

- Start in any supported region and complete regions in any order.
- Explore six regional campaigns with towns, routes, buildings, interiors,
  Gyms, caves, transport links, Elite Four challenges, and scripted events.
- Encounter autonomous AI rivals who travel, catch and train Pokémon, earn
  regional badges, challenge each Elite Four, and pursue their own careers.
- Experience Team Rocket operations, Pokémon Ranger responses, rival
  relationships, tournaments, world news, ecology, and regional incidents.
- Use the embedded Weather FX system with seasons, battle weather, terrain
  effects, 2D/3D presentation, and weather-dependent WX Pokémon.
- Track 632 categorized achievements and 48 regional badges/seals through
  dedicated Start-menu screens.
- Configure live convenience settings from **Start → QOL OPTIONS**, including
  seasonal notices, achievement popups, the Gen 1 EXP bar, AI simulation,
  weather presentation, and encounter ownership.
- Travel between regions by appropriate ships, trains, aircraft, and physical
  HM-gated connections.

## Supported games

| Game | Support |
| --- | --- |
| Pokémon Red | Full Gen 1 host path |
| Pokémon Blue | Full Gen 1 host path |
| Pokémon Yellow | Full Gen 1 host path; Pikachu/WX Pikachu starter policy |
| Pokémon Gold | Full Gen 2 host path |
| Pokémon Silver | Full Gen 2 host path |
| Pokémon Crystal | Full Gen 2/Crystal host path |

The manifest supports Gen1Recomp++ host versions `>=0.1.37` and `<2.0.0`.

## The regions

| Region | Campaign role | Visual foundation |
| --- | --- | --- |
| Kanto | Native campaign plus custom districts | Native Kanto tilesets preserved |
| Johto | Native/imported regional campaign | Native Johto tilesets preserved |
| Sevii Islands | Island circuit, services, routes, and League content | Host Kanto/Johto tileset approximations |
| Almia | Ranger-focused regional campaign | Host Kanto/Johto tileset approximations |
| Sinnoh | Regional Gyms, story and League progression | Host Kanto/Johto tileset approximations |
| Hoenn | Regional Gyms, story and League progression | Host Kanto/Johto tileset approximations |

Generated regions intentionally use only tilesets supplied by the active host.
Kanto and Johto retain their native map tilesets.

## Living-world simulation

Persistent rivals are trainers participating in the same world rather than a
sequence of fixed boss fights. Depending on their personality, class,
relationships, resources, and recent history, they can:

- travel between regions and towns;
- catch, train, evolve, trade, and lose Pokémon;
- challenge NPCs, other rivals, Gyms, tournaments, and regional Leagues;
- form friendships, rivalries, alliances, and grudges;
- pursue careers and quests or become involved with Team Rocket;
- react to weather, ecology, thefts, Rangers, and world events;
- black out and run to the nearest Pokémon Center when out of usable Pokémon.

The first-install flow lets an existing save decide whether rivals should
simulate all regions or visited regions only.

## Weather, seasons, and WX Pokémon

Weather FX is embedded directly into The World. Weather can change encounters,
battles, move behavior, terrain bonuses, AI decisions, quests, and regional
ecology. Seasonal weighting follows the configured clock and hemisphere.

WX Pokémon are persistent weather-associated forms with their own appearance,
typing, encounter conditions, and supported starter/tutor behavior. They can
be disabled independently without invalidating WX Pokémon already stored in a
save.

Version 6.54.15 restores the location-and-season HUD on clear frames and gives
achievement unlocks compact, gold-framed presentation plaques.

## Starters and progression

- Yellow always starts with exactly one Pikachu-family Pokémon, including a WX
  Pikachu when the WX choice is enabled.
- Red, Blue, Gold, Silver, and Crystal receive an appropriate starter for the
  selected starting region.
- Pokémon-generation scope and the intro WX choice are respected when the
  starter is generated.
- AI rivals begin in the same region as the player.
- Regional HMs are obtainable and Gym-gated within each campaign, with
  traversable alternatives and transport links between regions.

## Installation

1. Open the [latest release](https://github.com/MrKrisSatan/The_World/releases/latest).
2. Download `The_World_v6_54_15_full.zip`.
3. Import or extract it using the normal Gen1Recomp++ mod workflow. The folder
   containing `manifest.json` must be the mod root.
4. Enable **The World** in Mod Manager, then start or load a supported game.
5. Back up an important save before upgrading a large, actively developed mod.

See [the complete installation and upgrade guide](docs/INSTALLATION.md).

## Compatibility

The World absorbs several formerly separate projects. Do not enable standalone
copies of the following alongside it:

- Weather FX
- AI Rivals
- Kanto Reforged
- National Dex
- Wonder Trade
- GameShark
- Double Battles

The manifest also contains optional integration paths for popular sprite,
voxel, UI, encounter, randomizer, and content mods. See the
[compatibility guide](docs/COMPATIBILITY.md) before combining large overhauls.

## Save compatibility

The World keeps expanded species, forms, moves, and items registered where
needed so disabling an optional mechanic does not make existing save data
unreadable. Existing-save onboarding records per-save choices for AI, regional
simulation, and weather.

Back up saves before major upgrades. When reporting a migration problem, state
both the previous and current The World versions.

## Reporting problems

Use the [bug report form](https://github.com/MrKrisSatan/The_World/issues/new?template=bug_report.yml)
and include:

- game and Gen1Recomp++ version;
- The World version;
- new save or migrated save;
- current region and exact map;
- enabled optional mods;
- relevant QOL/weather/WX settings;
- reproduction steps;
- screenshots and the complete Lua error or `lua-error.log`, when available.

## Development status

The World is an active, large-scale mod. New-region content, cross-generation
behavior, runtime NPCs, map transitions, and persistent simulation interact in
ways that ordinary content replacements do not. Reproducible bug reports are
especially valuable.

Release 6.54.15 passes the project release gate, Lua 5.1 syntax validation,
module-resolution audit, and the 37-check regional completion harness.

## Credits

The World incorporates and adapts work from AI Rivals, Weather FX, Kanto
Reforged, and the bundled Kanto/Johto foundations. Battle backdrops include work
credited to CDRX73, DerxwnaKapsyla, http404error, and Game Freak. Weather audio
uses the credited Relic Castle tutorial pack and royalty-free Pixabay sources.
The 3D atmosphere integration is adapted from Kanto Dynamic Weather by Campo
(`1-Camp0-1`). Additional notices remain bundled with the distributed mod.

Pokémon and related names and imagery belong to their respective owners. This
is a fan-made project and is not affiliated with or endorsed by Nintendo,
Creatures Inc., or GAME FREAK.

---

Traditional Pokémon games wait for the player. **The World does not.**
