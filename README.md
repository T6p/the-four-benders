# Avatar: Bending

Bend earth, water, fire and air with your hands. Grip the ground and pull, and a pillar follows your hand
up. Sweep your look across a lake, and the ice runs after it. Draw a circle, and the wind winds into a
tornado. Moves come from what your hands and your look actually do, not from a hotbar of fixed spells,
and the earth you throw is real physics, powered by Sable.

An unofficial fan mod for **Minecraft 1.21.1 on NeoForge**.

This repository holds the **[player guide](docs/guide/README.md)** and the place to
**[report bugs](https://github.com/T6p/avatar-bending/issues)**. The mod's source code is not public.

## Download

[Modrinth](https://modrinth.com/mod/avatar-bending)

## What it adds

- **Four elements on the same keys.** Every element uses one grammar: **V** takes hold, **R** raises,
  **left click** strikes, **right click** shapes with your hand, **G** changes state (freeze, melt, heat),
  **Z** is your feet. Shift means wider or more. Holding a key makes the bigger version.
- **Bending by motion.** A grip held still spreads. A slow pull lifts, a hard jerk of the mouse shoots,
  a sweep spreads, a circle winds. How far and how fast you move decides how big the move is, not how
  long you wait.
- **Earth** on real physics bodies: tear chunks loose and throw them, raise pillars and walls to the height
  of your hand, spikes, burrows, pits, the earth wave you ride, stone armor and gloves, rock barrages,
  sand when you fall.
- **Water** from lakes, rain, plants and a water skin: streams that stay joined to the lake, whips, the
  ring, waves and floods, geysers and whirlpools, ice walls and spikes, freezing a lake along your look,
  a water spout, running on water. A power meter (B) sets how much you take.
- **Fire**: punches that grow while held, flame streams, a shield drawn with a circle of your look,
  walls and rings of fire, jets to fly, heat that melts and smelts.
- **Air**: pushes and pulls, currents that follow your sweep, updrafts, tornadoes wound by circling,
  the air ball and scooter, the spout, leaps, dives and dashes.
- **Stances (sub-bending)** on a wheel (Left Alt): lava, metal, plants, blood, healing, lightning,
  combustion and the spirit. Each is found and grown through play.
- **A world that bends back.** Bender NPCs with their own village fighting customs, masters who teach and
  spar, practice drills, sky bison, badgermoles and dragons to learn from, temples, forts, ruins and
  shrines, the sun, moon, comet and eclipses changing how strong each element is.
- **You grow by using it.** You are born with an element and learn its basics one key at a time in
  short training drills (N). Your bending gets stronger the more varied your practice is. Repeating one move over and over stops teaching you.
- **J** opens a scroll listing every move with your own key bindings. **K** turns bending off.

## Requirements

| Mod | Needed | Where it runs |
|---|---|---|
| [NeoForge](https://neoforged.net) 21.1.228 or newer | required | client and server |
| [Sable](https://modrinth.com/mod/sable) 2.0.6 or newer | required | client and server |
| [GeckoLib](https://modrinth.com/mod/geckolib) 4.8 or newer | required | client and server |
| [playerAnimator](https://modrinth.com/mod/playeranimator) 2.0.4 or newer | required | client (servers may skip it) |

Java 21. Install the mods your launcher doesn't add for you. Nothing is bundled inside the mod's jar.

## Install

1. Install NeoForge for Minecraft 1.21.1.
2. Put `avatar-1.21.1-<version>.jar`, Sable, GeckoLib and playerAnimator into the `mods` folder.
3. Start the game. In a new world you are born a bender: press **N**, choose **Practice** and do your first
   training drill. **J** lists every move. Operators can set anyone's element with
   `/avatar element <earth|water|fire|air>`.

**Servers:** put the same jar and Sable and GeckoLib on the server. Every player needs the mod too.
Bending is decided on the server, so it works the same for everyone.

**Back up your worlds.** This is an early release. Bending moves real blocks.

## Player guide

[docs/guide](docs/guide/README.md): getting started, controls, every move for each element, stances,
progression, the world, [commands and config](docs/guide/commands-and-config.md), servers and an FAQ.

## Reporting a bug

Open an issue on the [Issues](https://github.com/T6p/avatar-bending/issues) page and include:

- the versions of Minecraft, NeoForge, Avatar: Bending, Sable, GeckoLib and playerAnimator, and any other mods;
- what you did, what you expected and what happened instead;
- `logs/latest.log` from your game folder (and the file in `crash-reports/` if the game crashed).

## Known issues

- Early version: balance is rough and some stance moves have seen little play.
- Very large amounts of bent water (power meter at 9-10) cost the server real time with several benders
  at once.

## Credits

- Built on [Sable](https://modrinth.com/mod/sable) by ryanhcode and contributors (physics bodies),
  [GeckoLib](https://modrinth.com/mod/geckolib) (models and animations) and
  [playerAnimator](https://modrinth.com/mod/playeranimator) by KosmX (player animations).
- Inspired by *Avatar: The Last Airbender* and by the ProjectKorra server plugin's idea of bending.
- **AI disclosure:** this mod's code, and the scripts that draw its textures and synthesise its sounds,
  were written with an AI coding assistant (Anthropic's Claude), directed, designed and play-tested by T6p.
  No AI image or audio generator was used.

## License

The mod and this guide are All Rights Reserved, with permission to play the mod, run it on servers,
include it unmodified in free modpacks and show it in videos. See [LICENSE](LICENSE).

This is an unofficial, non-commercial fan work. It is not affiliated with, endorsed by or sponsored by
Nickelodeon, Paramount, Avatar Studios, Mojang Studios or Microsoft.
