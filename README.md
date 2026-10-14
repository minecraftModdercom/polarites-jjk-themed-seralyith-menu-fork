# Jujutsu Menu

A Jujutsu Kaisen and Deltarune themed fork of [Seralyth Menu](https://github.com/Seralyth/Seralyth-Menu) 5.0.2 for Gorilla Tag. It adds a **Jujutsu Mods** category with Hakari's Door, domain expansions, Blue / Red / Purple, Black Flash and more, plus three JJK menu themes.

> **Fan-made and unofficial.** This project is not affiliated with Seralyth, Another Axiom (Gorilla Tag), or the creators and publishers of Jujutsu Kaisen. All Jujutsu Kaisen names and characters belong to their respective owners.

## Features

### Jujutsu Mods

| Mod | What it does |
| --- | --- |
| **Hakari's Door** | Spawns a door in front of you. Walk through it to start the Idle Death Gamble. Roll **777** for a timed speed boost and golden aura. |
| **Summon Hakari's Door** | Moves the door in front of you again. |
| **Unlimited Void** | Gojo's domain: a black dome full of stars grows around you. |
| **Malevolent Shrine** | Sukuna's domain: a crimson dome with a shrine and endless red slashes. |
| **Limitless Techniques** | Blue pulls you toward your hand, Red blasts you away, Hollow Purple charges and dashes you forward. |
| **Black Flash** | Stop a fast punch short for a chance at a Black Flash and a short "Zone" speed boost. |
| **Dismantle** | Fast right-hand swings leave red slash lines. |
| **Cursed Energy Aura** | Cursed energy rises off your body in a color you choose. |
| **Six Eyes** | A glowing blue orb with sparkles floats in your view. |

### Settings

- **Change Jackpot Odds:** 1/239 (canon), 1/100, 1/50 or 1/10
- **Change Jackpot Duration:** 15s, 30s, 60s or 4 min (canon)
- **Change Black Flash Chance:** 5%, 15%, 30% or 100%
- **Change Aura Style:** Blue (Limitless), Red (Reversal), Gold (Hakari), Black Flash or Menu Theme

### Themes

Pick these under **Settings > Menu Settings > Change Menu Theme**:

- JJK: Gojo Limitless
- JJK: Sukuna Shrine
- JJK: Hakari Jackpot

### Deltarune Mods

| Mod | What it does |
| --- | --- |
| **Jarona Aura** | Blue, 50% transparent afterimages of your body that last 0.2 seconds. They only appear while you **hold B** and are moving. |
| **Flowey's Aura** | Rainbow afterimages of your body that fly out of your back. |
| **Roaring Knight** | Holds the Roaring Knight's black knife in your hand. Fast swings leave sword afterimages. |

Settings: **Change Sword Hand** (right or left) and **Change Sword Size** (small to huge). Two themes are included: **Deltarune: Dark World** and **Deltarune: Roaring Knight**. The knife model is baked from a `.glb` with `tools/bake_glb.py`.

## Controls

Defaults are shown. All of them can be changed under **Settings > Menu Settings**.

### Menu

| Action | Input |
| --- | --- |
| Open / close the menu | Hold the **Y** button (left controller secondary) |
| Press a button | Touch it with your right index finger |
| Bind a mod to an input | Hold **left grip**, then touch the mod |
| Add / remove from Quick Actions | Hold **left trigger**, then touch the mod |
| Favorite a mod | Hold **right grip**, then touch the mod |

Other layouts are available: Change Menu Button, Right Hand, Both Hands, Joystick Menu, Wrist Menu and Watch Menu.

### JJK mods

| Mod | Input |
| --- | --- |
| Hakari's Door | Walk through the door with your head |
| Blue | Hold **left trigger** |
| Red | Hold **right trigger**, aim with your right hand, release to blast away |
| Hollow Purple | Hold **both triggers** for about 2 seconds, then release to dash |
| Black Flash | Swing a hand fast and stop it against a wall, the floor or your other hand |
| Dismantle | Swing your right hand fast |
| Jarona Aura | Hold **B** (right controller) while moving |
| Flowey's Aura / Roaring Knight | Toggle only. Swing the knife fast for slash afterimages |

The domains, Cursed Energy Aura and Six Eyes are toggle only. Only one domain can be active at a time.

## Installation

1. Install [BepInEx](https://github.com/BepInEx/BepInEx) for Gorilla Tag.
2. Put the DLL from the [Releases](../../releases) page into `Gorilla Tag/BepInEx/plugins`.
3. Remove any other Seralyth Menu DLL from `plugins` so two copies don't load.
4. Launch the game and open the menu with the **Y** button.

## Building from source

The JJK changes live in three files on top of the Seralyth Menu 5.0.2 source:

| File | Change |
| --- | --- |
| `Mods/Jujutsu.cs` | New. All of the JJK mods. |
| `Mods/Deltarune.cs` | New. All of the Deltarune mods. |
| `Resources/Client/roaringknight.bin` | New. The baked Roaring Knight knife model. |
| `Menu/Buttons.cs` | Adds the **Jujutsu Mods** and **Deltarune Mods** categories and their main menu buttons. |
| `Mods/Settings.cs` | Adds the JJK and Deltarune themes at the end of the theme list. |

1. Clone this repository.
2. Open `SeralythMenu.sln` in Visual Studio, or run `dotnet build -c Release`.
3. Copy the built DLL into `BepInEx/plugins`.

The project's NuGet publicizer needs internet access the first time you restore.

## Notes

- **Use private rooms.** Hakari's Door, Limitless Techniques and Black Flash change your movement speed or momentum. Using movement mods in public lobbies can get an account flagged or banned.
- Everything added here is client-side. Domains, doors, orbs and slashes are only visible to you, and nothing touches other players or the network.
- Hakari's jackpot, the Black Flash Zone and the existing Speed Boost mod all change the same jump values, so running them together can conflict.
- The mods have been compile-checked but not extensively playtested. The numbers for pull strength, dash speed and punch detection may need tuning. Please open an issue if something looks off.

## License and credits

This project is a fork of [Seralyth Menu](https://github.com/Seralyth/Seralyth-Menu) and is licensed under the **GNU General Public License v3.0**, the same as the original. See [LICENSE](LICENSE).

Thanks to the Seralyth team for the base menu. Please support the original project.
