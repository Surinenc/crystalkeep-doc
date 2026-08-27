# Nightmare

Nightmare is the difficulty ladder, and it has no top. You choose how high to
climb before the run starts.

## Two separate questions

Nightmare involves two mechanisms that are easy to confuse, and they answer
different questions.

**What may you select?** Your account tracks the highest tier you have reached.
Requesting a higher one is refused and clamped back down to it. Only **Keep
Assault** raises that ceiling — clearing all five waves at your selected tier
unlocks the next.

**What does the run actually use?** That is a per-mode answer, and it has
nothing to do with unlocking:

| Mode | Pressure used for spawning and loot |
|---|---|
| Keep Assault | Your selected tier, fixed for the run |
| Endless Siege | Your selected tier **plus depth** — `nightmare + max(0, wave - 4)` |
| Weekly Keep | **Forced to 0**, whatever you have unlocked |

Weekly pins it deliberately. In the game's own words, a Weekly is *"one shared
challenge, not a family of incomparable ladders"* — its map and its base combat
power are both fixed so that scores mean the same thing for everyone.

Pressure is what feeds monster level, which sets both enemy scaling and the
item-level band you roll against. So a mode that ignores your tier is also a
mode that ignores your usual loot ceiling.

## Both sides grow on the same curve

The reason an uncapped ladder works here is that enemy growth and player growth
belong to the same mathematical family. Enemy health scales as:

```
health multiplier = 1 + 0.52 × ln(1 + nightmare)
damage multiplier = 1 + 0.32 × ln(1 + nightmare)
```

Both are logarithmic, exactly like the [ratings curve](progression.md) your
equipment runs on. Sampled across the ladder:

| Nightmare | Enemy HP | Your defenses |
|---:|---:|---:|
| 10 | ×2.25 | ×1.42 |
| 100 | ×3.40 | ×2.56 |
| 1,000 | ×4.59 | ×4.10 |
| 10,000 | ×5.79 | ×5.71 |

The gap narrows and never inverts. **Gear is never finished, and the challenge
never stops tracking it.** There is no best-in-slot after which progression
simply stops.

Note the early rungs: the enemy curve *leads* at low Nightmare. The first
climbs are proportionally the hardest part of the ladder.

## What scales and what does not

Enemy **health** and **damage** scale. Enemy **speed does not** — at any
Nightmare level, an orc still moves at 2.2 m/s and a runner at 5.6 m/s.

This is why the [fairness contract](keeps.md) holds at every level. F2 and F3
are time-based — route metres divided by enemy speed — so a keep certified fair
at item level 1 is still certified fair at item level 200. Progression cannot
move the quantity the contract measures.

## Enemy counts grow logarithmically too

Wave populations increase with Nightmare, but on a log curve rather than
linearly:

```
count multiplier = 1 + 0.12 × ln(1 + nightmare) + 0.10 × ln(1 + attrition rank)
```

There is no population ceiling and no linear explosion — high levels are a
tactical problem, not a performance one.

## Nightmare Laws

Five Laws apply cumulatively, in a fixed order: **Shieldwall**, **Ember**,
**Giants**, **Siege**, **Attrition**.

One further Law activates every **10** Nightmare levels, so the first arrives
at 10 and all five are running by **50**. After that the cycle repeats and each
pass raises a Law's rank instead of adding a new one — so any given Law
strengthens every **50** levels.

| Nightmare | Active Laws |
|---:|---|
| 0–9 | none |
| 10 | Shieldwall |
| 30 | Shieldwall, Ember, Giants |
| 50 | all five, rank 1 |
| 60 | all five — Shieldwall now rank 2 |
| 110 | all five — Shieldwall rank 3, the rest rank 2 |

Each Law names its own pressure, its own answer, and its own reward:

| Law | Pressure | The stated answer | Its cache |
|---|---|---|---|
| **Shieldwall** | Shieldbearers lead and protect more formation packets | Flank the column, use Crush, or break its formation | Fortification |
| **Ember Host** | Fire Demons reinforce increasingly frequent mixed squads | Chill first, then use non-Cannon damage | Floor control |
| **Giant March** | Later waves add Colossi that demand Warden intervention | Kite, break armour, protect the defense line | Warden |
| **Siegecraft** | Ranged attackers and Sappers coordinate against structures | Spread defenses, break line of sight, intercept | Wall defense |
| **Attrition** | Assaults carry more bodies and recover less time between beats | Overlapping coverage, and preserve mana | Mixed arsenal |

**The cache column is not decoration.** Each Law's milestone reward rolls with
that Law's own loot preference — Shieldwall pays fortification stats,
Siegecraft pays wall-trap stats, Giant March pays Warden stats. The pressure
that beat you is also the pressure that arms you against it, and the ladder
therefore pushes your gear toward answering the thing currently pushing back.

Note that Attrition's answer mentions preserving mana for repairs. Repairs are
free in a normal run; that advice is aimed at the Endless **Iron Levy**
contract, where they are not.

Laws are previewed rather than hidden: you see the roster and the events before
you commit to the climb.

## Rewards

Item level bands scale with Nightmare, so climbing is how you reach higher roll
ranges. A tier's band runs from `nightmare × 10` to `nightmare × 10 + 13`, so
**adjacent tiers overlap by about 23%** — a lucky roll one tier down can still
beat an unlucky roll one tier up, and climbing is a shift in the distribution
rather than a hard cutover.

Every victory pays an item and **100 + 20 per Nightmare level** in gold.

**Milestone caches** are the real prize, and they are stricter than they look.
You get one only when both things are true:

- the Nightmare level is a **multiple of 10**, and
- it is a **first clear at your ceiling** — the run that unlocks the next tier.

Replaying a milestone level you have already beaten pays an ordinary victory.
The cache is a one-time reward for arriving, not a farm.

When one does land it is **guaranteed Legendary or better**, rolled with the
preference of the Law that milestone activated, and it carries a gold bonus of
**250 per milestone tier** — +250 at N10, +500 at N20, +750 at N30 — on top of
the ordinary victory gold.

Because the band is `nightmare × 10` with no cap, there is always a next one.

## See also

- [Progression](progression.md) — the ratings curve on your side of the equation
- [Game modes](game-modes.md) — where Nightmare applies
- [Keeps](keeps.md) — why the fairness contract survives the ladder
