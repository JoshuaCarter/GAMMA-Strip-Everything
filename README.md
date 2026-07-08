# Dorn's Fieldstrip All Keybind

For **S.T.A.L.K.E.R. G.A.M.M.A.** — an MCM keybind that field-strips a weapon in one press.

## Demo

https://github.com/JoshuaCarter/GAMMA-Field-Strip-All-Keybind/raw/main/stripper.mp4

## What this mod does

Hover your cursor over a weapon (your own inventory, or a corpse/crate you're looting) and press the configured key. It detaches the scope, silencer, and GL, then removes all Weapon Parts Overhaul parts (trigger group, bolt, etc) — same as right-clicking each option by hand, just automatic.

Optionally, it can also catch you trying to disassemble a weapon that isn't fully stripped yet and field-strip it instead, so you never accidentally disassemble a weapon with parts still on it.

## Installation

1. Download the latest release (when published) or install the folder via MO2
2. Load late in your load order (script is named `zzzz_`) so it plays nicely with other UI/weapon mods
3. Enable in Mod Organizer 2 like any other mod
4. Open MCM → Dorn's Fieldstrip All Keybind → bind the field-strip key

## Options (MCM)

- **Field-strip key** — the key to press while hovering a weapon (default: unbound — bind it to enable the mod)
- **Field-strip instead of disassembling** — redirect disassembly of a not-yet-fully-stripped weapon into a field-strip instead (default: on)
- **Keep stripped parts in the weapon's inventory** — spawn removed WPO parts into the weapon owner's inventory instead of always dumping them into yours (default: on; applies to right-click field strip too, not just the keybind)
- **Debug log** — log every step to the game log file
