# Dorn's Fieldstrip All Keybind

For **S.T.A.L.K.E.R. G.A.M.M.A.** — an MCM keybind that field-strips a weapon in one press.

## What this mod does

Hover your cursor over a weapon in your own inventory or a corpse/crate you're looting, and press the configured key once. It queues up every applicable step below and runs them one at a time, a couple of frames apart, until the weapon's fully stripped:

1. **Detach Scope** (if attached)
2. **Detach Silencer** (if attached)
3. **Detach GL** (if attached)
4. **Field strip → Remove all** — every internal weapon part tracked by the Weapon Parts Overhaul mod (trigger group, bolt, etc, excluding the barrel), removed in one go

Each step reuses the exact same function its right-click context-menu entry calls, so results are identical to doing it by hand. Only one native UI action happens per render frame — chaining several in the same synchronous call was found to crash the game, since the engine expects the UI to settle between actions. So instead this spreads them out (~2 frames apart) via the same per-frame hook the inventory window itself uses for its own updates, which finishes in well under a second while staying safe. If you move the cursor off the weapon mid-burst, the remaining steps are cancelled. Step 4 is skipped automatically if the Weapon Parts Overhaul mod isn't installed, or if its own precondition check errors on a given weapon.

## Installation

1. Download the latest release (when published) or install the folder via MO2
2. Load late in your load order (script is named `zzzz_`) so it plays nicely with other UI/weapon mods
3. Enable in Mod Organizer 2 like any other mod
4. Open MCM → Dorn's Fieldstrip All Keybind → bind the field-strip key

## Options (MCM)

- **Field-strip key** — the key to press while hovering a weapon (default: unbound — bind it to enable the mod)
- **Debug log** — log every step (hover resolution, addons removed, parts removed) to the game log file
