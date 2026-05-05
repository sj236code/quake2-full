# Quake II Zelda Mod

## Overview

This project modifies Quake II into a Zelda-inspired gameplay mod. The implementation keeps the original Quake II code structure and reuses existing weapon and monster systems to keep the mod simple and stable.

So far, two major features have been implemented:

1. Replace Quake II weapons with Zelda-themed weapons
2. Retheme five Quake II monsters as Zelda beasts with weapon-specific weaknesses

---

## Feature 1: Zelda Weapon Replacement

The original Quake II weapons were renamed and modified to behave like Zelda-style weapons. The display names were changed while keeping the original internal Quake II weapon names so existing maps, pickups, and console commands still work.

### Weapon Mapping

| Original Quake II Weapon | Zelda Weapon | Internal Command |
|---|---|---|
| Blaster | Deku Slingshot | `use blaster` |
| Shotgun | Kokiri Sword | `use shotgun` |
| Super Shotgun | Master Sword | `use super shotgun` |
| Machinegun | Boomerang | `use machinegun` |
| Chaingun | Hero's Bow | `use chaingun` |
| Grenade Launcher | Bomb Bag | `use grenade launcher` |
| Rocket Launcher | Fire Rod | `use rocket launcher` |
| HyperBlaster | Magic Wand | `use hyperblaster` |
| Railgun | Light Arrow | `use railgun` |

### Weapon Behavior Changes

| Zelda Weapon | Base Weapon | Behavior Change |
|---|---|---|
| Deku Slingshot | Blaster | Fires a slower reusable projectile |
| Kokiri Sword | Shotgun | Stronger, tighter close-range slash-style attack |
| Master Sword | Super Shotgun | Stronger version of the Kokiri Sword with tighter spread |
| Boomerang | Machinegun | Single reusable shot with cooldown and return message |
| Hero's Bow | Chaingun | Single accurate arrow shot instead of rapid spray |
| Bomb Bag | Grenade Launcher | Launches slower, heavier bombs |
| Fire Rod | Rocket Launcher | Fires slower fireballs with wider splash radius |
| Magic Wand | HyperBlaster | Fires visible magic bolts |
| Light Arrow | Railgun | Stronger limited-range piercing shot |

### Weapon Feedback Messages

To make testing clearer, feedback messages were added when weapons are used.

Examples:

```text
Kokiri Sword fired!
Master Sword fired!
Boomerang thrown!
Boomerang returned!
Hero's Bow fired!
Bomb Bag launched a bomb!
Fire Rod cast a fireball!
Magic Wand released magic bolts!
Light Arrow pierced the target!

## Feature 2: Zelda Monster Retheme

Five Quake II monsters were rethemed as Zelda-style beasts. The original Quake II monster models are reused, but each monster now has a Zelda name and specific weapon weakness. 

### Monster Mapping
| Original Quake II Monster | Zelda Beast | Internal Command | Weakness Weapon | Weapon Hotkey |
|---|---|---|---|---|
| monster_soldier_light | Bokoblin | spawn_bokoblin | Kokiri Sword | 2 |
| monster_berserk | Moblin | spawn_moblin | Bomb Bag | 6 |
| monster_mutant | Lizalfos | spawn_lizalfos | Boomerang | 4 |
| monster_flyer | Keese | spawn_keese | Hero's Bow | 5 |
| monster_tank | Lynel | spawn_lynel | Light Arrow | 9 |
