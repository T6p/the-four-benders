# Getting started

## Install
You need Minecraft **1.21.1** with **NeoForge 21.1.228 or newer**, and Java 21. Put these jars in your `mods` folder:

| Mod | Version | Where |
|---|---|---|
| Avatar: Bending | 0.1.0 | client and server |
| [Sable](https://modrinth.com/mod/sable) | 2.0.6 or newer | client and server |
| [GeckoLib](https://modrinth.com/mod/geckolib) | 4.8 or newer | client and server |
| [playerAnimator](https://modrinth.com/mod/playeranimator) | 2.0.4 or newer | client (a server can skip it) |

Nothing is bundled inside the Avatar jar. **Back up your worlds**: bending moves real blocks.

## You are born a bender
The first time you join a world, you are **born with an element at random: earth, water, fire or air**. A chat card tells you which one, for example *"You were born an earthbender. The element is in you, but you know nothing of bending yet."*

- If the server sets `bornAs = "choose"`, you pick your element instead: press **N** and choose one of the four sigils.
- The element is in you, but at first **you know no basics**. A key whose basic you haven't learned does nothing and says so on the action bar.
- Players who were already bending before this system came keep everything they had.

## Your first basics
A **basic** is one key's meaning for your element. There are six:

| Basic | Key | Earth | Water | Fire | Air |
|---|---|---|---|---|---|
| pull | **V** | Pull earth | Draw | Breathe | Pull |
| push | **Left click** | Push | Push | Strike | Push |
| shape | **Right click** | Shape | Shape | Shape | Shape |
| raise | **R** | Raise | Raise | Raise fire | Raise |
| change | **G** | Change | Freeze and thaw | Heat | Change |
| feet | **Z** | Stamp | Flow | Kick | Feet |

You learn each one in a short **training drill**:

1. Press **N** and choose **Practice**.
2. Your element's **pull** drill is open from the start. Pick it and press **Begin**.
3. Finish the drill and that basic is yours. More drills open as you learn (see [Progression > Training](progression.md#training)).

A hostile creature nearby pauses a drill. Dying, logging out or walking away cancels it.

## Small at first
New bending is weak. Until a move has grown a little, its key only does a first, tiny stage: a block strains part-way out of its hole, a few drops of water, sparks, a breath. You also start with only a quarter of your full chi, and it grows to the full pool as your six keys grow. Keep using everything you know and it all gets bigger. See [Progression](progression.md).

## Next steps
- Open the **J** scroll to read every move for your element, shown with your own keys.
- Read [Controls](controls.md) for how the bending grammar works.
- Find your element's teacher creature for a lasting style (see [Progression > The four teachers](progression.md#the-four-teachers)).
- To learn a second element, you need the Avatar cycle (see [Progression > The Avatar cycle](progression.md#the-avatar-cycle)).

**Operators** can skip all of this with `/avatar element <earth|water|fire|air> [players]`, or `/avatar basic learn <player> all`.

## Not a bender?
If your bending is taken (energybending) or an operator sets you to `none`, you fight as a chi-blocker: three quick jabs at someone block their chi. See [Controls > Without bending](controls.md#without-bending).
