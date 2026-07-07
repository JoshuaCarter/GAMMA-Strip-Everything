# Dorn's Fieldstrip All Keybind

For **S.T.A.L.K.E.R. G.A.M.M.A.** — an MCM keybind that field-strips a weapon in one press.

## What this mod does

Hover your cursor over a weapon in any inventory list — your own gear, a corpse or crate you're looting, a trade screen — and press the configured key. Every addon on that weapon gets detached in one go:

- Scope
- Silencer
- Grenade launcher

Detaching reuses the exact same functions the right-click "Detach Scope / Silencer / GL" context-menu entries call, so the result is identical: the addons pop back out as separate items, the normal detach sounds play, and the UI refreshes — just without having to right-click each addon individually.

## Installation

1. Download the latest release (when published) or install the folder via MO2
2. Load late in your load order (script is named `zzzz_`) so it plays nicely with other UI/weapon mods
3. Enable in Mod Organizer 2 like any other mod
4. Open MCM → Dorn's Fieldstrip All Keybind → bind the field-strip key

## Options (MCM)

- **Field-strip key** — the key to press while hovering a weapon (default: unbound — bind it to enable the mod)
- **Debug log** — log which weapon was field-stripped and how many addons were removed
