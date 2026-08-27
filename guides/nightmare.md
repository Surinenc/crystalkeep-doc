# Nightmare

Nightmare is the difficulty ladder, and it has no top. You choose how high to
climb before the run starts; the level does not move during it.

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

Above the early bands, ranked Laws apply cumulatively and cycle every ten
levels. They are previewed rather than hidden: you see the roster and the
events before you commit to the climb.

## Rewards

Item level bands scale with Nightmare, so climbing is how you reach higher roll
ranges. Milestone clears in the high bands pay first-clear caches with
guaranteed Epic-or-better contents and one-time gold premiums.

Because the item-level band is `nightmare × 10` with no cap, there is always a
next band.

## See also

- [Progression](progression.md) — the ratings curve on your side of the equation
- [Game modes](game-modes.md) — where Nightmare applies
- [Keeps](keeps.md) — why the fairness contract survives the ladder
