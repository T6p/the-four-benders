# Commands and config

## Commands anyone can use

| Command | What it does |
|---|---|
| `/avatar master <player>` | ask a player to be your master for your next element |
| `/avatar master accept\|decline <student>` | answer a student's request |
| `/avatar teach accept\|decline <teacher>` | answer an offer to learn a form |
| `/avatar teach use\|keep` | put a learned form on its key, or keep your own |
| `/avatar school [name <name> \| close]` | name at least two of your forms as a school, or close it |
| `/avatar power <1-10>` | set your water power meter |
| `/avatar look fire pixel\|smooth` | pixel or smooth fire |
| `/avatar look air blue\|white` | colour of air effects |
| `/avatar look tattoos on\|off` | airbending tattoos on masters |
| `/avatar look shake <0-2>` | screen shake from impacts |
| `/avatar look water …` | how bent water looks to you: `vanilla\|ours`, `surface smooth\|classic`, `slim <0-0.6>`, `cubes <0.3-1.5>`, `smooth\|free\|shader\|outline on\|off` |

The `look` and `power` commands only change your own client.

## Operator commands (permission level 2)

| Command | What it does |
|---|---|
| `/avatar element <earth\|water\|fire\|air\|none> [players]` | set a player's element |
| `/avatar basic learn\|forget <player> <basic\|all>` · `basic list <player>` | manage someone's basics (`earth.pull`, …) |
| `/avatar train <basic>` | start a training drill |
| `/avatar reborn [players]` | start a new life: a new birth, practice cleared |
| `/avatar mastery [max \| reset \| set <element\|stance\|all> <0-1>]` | view or set mastery (the mastery card) |
| `/avatar affinity [<player> [here \| reset \| set <affinity> <0-1>]]` | view or set affinities |
| `/avatar stance none\|<stance>` | set your stance |
| `/avatar trait give\|take <players> <trait>` · `trait list [player]` | give or take traits (styles, flight, blue fire) |
| `/avatar cycle [learn <element> \| avatar \| reset \| wake \| mend]` | Avatar cycle controls |
| `/avatar chi full` · `chi endless on\|off` · `chi max <1-100000>` | fill chi, endless chi, or everyone's full chi |
| `/avatar npc <element> <novice\|adept\|master> [teacher\|resident]` | spawn a bender NPC where you look |
| `/avatar comet [start [minutes] \| stop]` | start, stop or check the comet |
| `/avatar eclipse [solar\|lunar [minutes] \| stop]` | start, stop or check an eclipse |
| `/avatar built clear \| practice <0-1>` | wipe or set practice on builder moves |
| `/avatar clear [radius]` | remove every physics body and bent water and lava nearby (default 64 blocks) |
| `/avatar water vanilla\|blocks\|particles\|toggle` · `waterstyle show\|fluid` | server-wide look of bent water |
| `/avatar flow on\|off\|where\|stats\|…` | the world-water engine |
| `/avatar lag on\|off` · `probe [radius]` | lag log and body probe, written to the server log |

## Config files
The mod writes two files into your `config` folder the first time it starts:

- **`avatar-client.toml`**: how things look to you. Each player has their own.
- **`avatar-common.toml`**: the server's rules and the numbers for every move. On a server, the server's copy is the one that counts.

Every option in the files has a comment and a range. These are the ones most people look for.

### Client (`avatar-client.toml`)

| Section | Option | Default | What it does |
|---|---|---|---|
| `[water]` | `waterPower` | 4 | the water power meter level (1-10) |
| `[water]` | `waterVanillaLook` | true | bent water looks like vanilla water |
| `[water]` | `smoothWater` | true | vanilla water eases between levels |
| `[water]` | `waterShader` | false | the water shader look |
| `[stances]` | `stanceTapTicks` | 6 | how short a Left Alt tap must be to go back to your plain element |
| `[looks]` | `firePixels` | 16 | fire pixel size (0 = smooth fire) |
| `[looks]` | `airBlue` | true | blue air effects |
| `[looks]` | `impactShake` | 1.0 | screen shake from impacts (0-2) |
| `[looks]` | `airTattoos` | true | airbending tattoos |
| `[combos]` | `comboStrip` | true | the combo strip under the crosshair (and `comboStripSound`) |

### Server (`avatar-common.toml`)

| Section | Option | Default | What it does |
|---|---|---|---|
| `[training]` | `bornAs` | "random" | a newcomer's element: `"random"`, or `"choose"` to pick it in the N menu |
| `[bending]` | `liftTerrain` | true | **off: nobody can tear blocks out of the world** (the main anti-grief switch) |
| `[bending]` | `grabReach` / `holdRange` | 9 / 24 | how far you can grab, and hold matter |
| `[chi]` | `maxChi` / `chiRegen` | 100 / 12 | base chi and refill per second |
| `[limits]` | `mergeBack` | true | resting matter turns back into blocks |
| `[limits]` | `restoreTerrain` | false | on: bent blocks go back to their original holes |
| `[limits]` | `bodiesPerPlayer` / `debrisPerPlayer` | 8 / 32 | caps on each player's physics bodies and debris |
| `[limits]` | `bodyLifetimeSeconds` | 60 | how long a body lives |
| `[water]` | `maxWaterBlocks` | 480 | the top of the water power meter |
| `[flow]` | `engine` | false | the finite-water engine (off: vanilla water) |
| `[performance]` | `waterThreads` | -1 | water worker threads (-1 automatic, 0 = all on the server thread) |
| `[mastery]` | `on` | true | off: everyone is a full master |
| `[mastery]` | `scale` | 120000 | how slowly mastery grows (bigger = slower) |
| `[cycle]` | `cycleMastery` | 0.6 | mastery needed before learning the next element |
| `[cycle]` | `brokenCycleDays` | 30 | how long a death in the Avatar State breaks the cycle |
| `[avatarState]` | `avatarStateSeconds` / `avatarStateRestMinutes` | 30 / 10 | Avatar State length and rest |
| `[sky]` | `cometEveryDays` | 30 | days between comets (0 = only by command) |
| `[sky]` | `solarEclipseEveryDays` / `lunarEclipseEveryDays` | 20 / 25 | days between eclipses |
| `[creatures]` | `bisonSeats` | 4 | riders on a saddled bison |

Hundreds of per-move numbers follow in the same file, one section per element and stance.
