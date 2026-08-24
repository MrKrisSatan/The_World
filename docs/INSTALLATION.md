# Installation and upgrades

## Requirements

- A supported Gen1Recomp++ host version (`>=0.1.37`, `<2.0.0`).
- Pokémon Red, Blue, Yellow, Gold, Silver, or Crystal imported through the
  host's normal game setup.
- The latest The World release ZIP.

The World does not provide game ROMs or copyrighted game data.

## New installation

1. Download `The_World_v6_54_15_full.zip` from the
   [latest release](https://github.com/MrKrisSatan/The_World/releases/latest).
2. Use the host's mod import action, or extract the archive into the host's mod
   directory.
3. Confirm `manifest.json`, `main.lua`, `ai/`, `lib/`, and `reforged/` are all
   in the same mod root. Avoid an extra nested directory after extraction.
4. Open Mod Manager and enable **The World**.
5. Start a supported game. New saves receive the normal region, starter, WX,
   weather, and rival setup flows.

## Upgrading

1. Back up the save.
2. Close Gen1Recomp++ completely.
3. Replace the complete old The World mod directory with the new release.
   Do not merge new files over an old directory; removed or renamed modules can
   otherwise survive and load unexpectedly.
4. Confirm Mod Manager shows version 6.54.15.
5. Load the save and answer any first-install or migration prompts.

For an existing save, the migration flow asks whether AI trainers and dynamic
weather should be enabled and whether rivals may simulate unvisited regions.

## First launch checklist

- Open **Start → QOL OPTIONS** and verify the desired Gameplay, World, Rivals,
  and Display settings.
- If using WX Pokémon, verify the WX setting before accepting a starter.
- If using optional 3D presentation, start with weather presentation on AUTO.
- Enter an outdoor map and confirm the location/season notice appears.
- Make a fresh save before adding further large overhaul mods.

## Uninstalling

Back up the save first. Saves containing expanded species, WX forms, moves,
items, regional location data, or active scripts can depend on The World's
registered content. Removing the mod from such a save is not guaranteed to be
safe.

## Troubleshooting

### The mod is not listed

Check that `manifest.json` is at the extracted mod root and not inside a second
`The_World_*` directory.

### Mod Manager reports a missing module or syntax error

Delete the old mod directory and perform a clean extraction. Do not combine
files from two release ZIPs.

### A migrated save enables unexpected regional simulation

Open **Start → QOL OPTIONS → RIVALS** and change **SIMULATE UNVISITED REGIONS**.
Version 6.54.15 also records the onboarding answer per save.

### Season or achievement notifications are unwanted

Open **Start → QOL OPTIONS → DISPLAY**. `SEASON NOTE` and
`ACHIEVEMENT POPUPS` can be controlled independently.
