# FAQ and troubleshooting

**I pressed a key and nothing happened.**
You haven't learned that key's basic yet. The action bar says so. Press **N**, choose **Practice**, and do the drill for that key. Your element's pull (**V**) drill is open from the start. Also check that bending is on (**K**).

**My moves are tiny.**
That's normal at first. New bending only does a small first stage until it grows. Keep using all your keys: each move grows with use, and so does your chi.

**I stopped getting stronger.**
Mastery only grows when you use all of your bending. One move alone tops out at about 0.3. Use different keys, with and without Shift, and fight things that fight back (bender NPCs teach far more than plain mobs).

**Can I learn a second element?**
Through the Avatar cycle: reach Expert (0.6) in your element, then beat the master of the next element (water → earth → fire → air) in a spar. See [Progression](progression.md#the-avatar-cycle).

**Do the sky bison, badgermoles, dragons or moon give me bending?**
No. You are born with your element. Those teachers give a bender of their own element a lasting **style** (a bison bond, the badgermole sense, the dragons' fire, the moon's blessing).

**I want to pick my element instead of getting a random one.**
On a server, the owner sets `bornAs = "choose"` in `avatar-common.toml`. An operator can also set it with `/avatar element`.

**I ran out of chi and can't bend.**
At zero chi you are exhausted until it refills to a quarter. Earthbenders have twice the chi. In the spirit stance, holding **R** still refills it faster.

**Firebending (or waterbending) suddenly stopped working.**
Probably an eclipse: a solar eclipse stops all firebending for 5 minutes, a lunar eclipse all waterbending. See [The sky](world.md#the-sky).

**Where are the masters?**
In the four nation homes: an Air Temple on mountain peaks, a Water Tribe village in the snow, an Earth Kingdom fort on the plains, and a Fire Nation temple in badlands and deserts. See [Structures](world.md#structures).

**How do I find out my mastery?**
In this version there is no screen for it: you notice it as your moves grow, and each breakthrough to a new level gives a sound and a burst. An operator can show the mastery card (each element's rank and ten marks, and each stance's stage) with `/avatar mastery`.

**Leftover rocks or water are lying around.**
Bodies merge back into blocks once they settle and expire after a minute. An operator can clean up with `/avatar clear`.

**The server lags when we use water.**
Big amounts of water at power 9-10 are expensive. See [Servers > Performance](servers.md#performance).

**Can I use this in a modpack or a video?**
Yes. You may play it, run it on servers, include it unmodified in free modpacks and show it in videos. See the LICENSE file.

**I found a bug.**
Please report it with your `logs/latest.log` (in your game folder) attached, and say what you did just before.
