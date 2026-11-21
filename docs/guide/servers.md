# Servers and multiplayer

## Installing on a server
- Put **Avatar, Sable and GeckoLib** in the server's `mods` folder (NeoForge 21.1.228 or newer, Minecraft 1.21.1). playerAnimator is only needed on clients.
- **Every player needs the mod** (and Sable, GeckoLib and playerAnimator). Players without it can't join.
- Bending is decided on the server, so it works the same for everyone.
- Server rules live in the server's `config/avatar-common.toml`. See [Commands and config](commands-and-config.md#server-avatar-commontoml).

## PvP, griefing and claims
The mod has **no PvP switch of its own**. It follows the server:
- **PvP:** with the server's `pvp=false`, bending doesn't hurt other players, and chi-blocking, energybending and metal pulling don't work on them. Bending damage counts as the bender's own, so vanilla's rule stops it. With PvP off, `/avatar master` can't ask a player to be your master (NPC masters still spar).
- **Building rights:** every block a bender changes is checked like a player breaking or placing it, so spawn protection and claim mods that cancel block breaks are respected. Lava landings and pool draws ask too (`respectClaims`, on by default).
- **Mobs:** bender NPCs only change terrain when the `mobGriefing` game rule allows it.
- **No terrain at all:** set `liftTerrain = false` in `[bending]` and nobody can tear blocks out of the world.
- **Put it back:** `restoreTerrain = true` in `[limits]` sends bent blocks back to their original holes.

## Who gets what
- New players are born with a random element. Set `bornAs = "choose"` under `[training]` to let each player pick theirs in the N menu.
- Only one player per world can be the Avatar.
- Operators can set anyone's element with `/avatar element`, and everything else with the [operator commands](commands-and-config.md#operator-commands-permission-level-2).

## Performance
- Earth chunks are physics bodies. Each player is capped at `bodiesPerPlayer = 8` bodies and `debrisPerPlayer = 32` pieces of debris, and bodies merge back into blocks once they settle or after `bodyLifetimeSeconds = 60`.
- **Water at power 9-10** from several benders at once is the costliest thing in the mod. Lower `maxWaterBlocks` in `[water]` if your server struggles.
- `waterThreads` in `[performance]` moves water work off the main thread (automatic by default).
- If the world-water engine is on (`[flow] engine = true`), its `budget` keeps it from pushing a server tick past 40 ms.
- `/avatar clear [radius]` removes every body and all bent water and lava nearby.
- `/avatar lag on` writes lag lines (starting with `lag:`) to the server log, to help find what's slow.

## Before you open it to friends
- **Back up the world.** Bending moves real blocks.
- Decide on `liftTerrain`, `restoreTerrain`, `bornAs` and the server's `pvp`.
- Make sure everyone has the same mod versions.
