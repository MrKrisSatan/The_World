# Compatibility

## Supported host games

The World declares Red, Blue, Yellow, Gold, Silver, and Crystal support under
Gen1Recomp++ API 2. Host-specific save and content keys keep Gen 1 and Gen 2
state separated where map IDs or mechanics differ.

## Embedded or conflicting projects

Do not install separate copies of systems already absorbed by The World:

| Project/mod ID | Reason |
| --- | --- |
| `weather_fx` | Weather FX is embedded |
| `ai_rivals` | AI Rivals is embedded |
| `Kanto-Reforged` | Kanto Reforged content is embedded |
| `national_dex` | National Dex content is embedded |
| `wonder_trade` | Wonder Trader behavior is embedded |
| `GameShark` | World Shark behavior is embedded |
| `double_battles` | The World owns overlapping battle behavior |

The manifest marks Weather FX and AI Rivals as incompatible and the remaining
overlapping packages as conflicts so Mod Manager can warn before boot.

## Optional integrations

The manifest contains compatibility paths for sprite packs, voxel/3D hosts,
battle presentation mods, encounter providers, randomizers, companion tools,
and content extensions. Examples include Dramatic Shape, Dramaless Shape,
Potato Voxel, HGSS/Gold-Silver sprite packs, Kanto Companion, Gen 3 Battle UI,
Crystal 251, Vanilla Plus, Universal Randomizer, and New Game Plus.

Optional does not mean every combination of several large overhauls has been
tested together. Add one major mod at a time and keep a known-good save.

## Wild encounter ownership

`WILD ENCOUNTERS` can be set to:

- **AUTO / COMPATIBLE** — The World yields when a supported encounter provider
  should own the result.
- **THE WORLD** — The World applies its regional, generation, weather, and WX
  encounter rules.
- **EXTERNAL / VANILLA** — ordinary encounter substitutions are disabled while
  the rest of The World remains active.

## Tilesets

Kanto and Johto preserve their native tilesets. The World's authored Sevii,
Almia, Sinnoh, Hoenn, and custom-region additions use only tilesets supplied by
the active host, with Kanto/Johto approximations selected for location-specific
events.

## Reporting a compatibility bug

Include the exact enabled mod list and versions, load order if configurable,
host game, map, The World options, and the full Lua error. A screenshot without
the complete error text is useful context but may not identify the responsible
hook or module.
