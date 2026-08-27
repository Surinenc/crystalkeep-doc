# Economy

Two currencies, and they do different jobs. **Mana** builds the keep during a
run and resets between runs. **Gold** persists and pays the Workshop.

## Mana

You start a run with **400 mana**. It is the only construction resource — there
is no separate build currency and no cap on how many defenses you may own.

Mana arrives from two places:

**Bounties.** Every kill pays, and the rate reflects the threat:

| Enemy | Bounty |
|---|---:|
| Runner | 12 |
| Goblin | 14 |
| Frostbound | 20 |
| Crossbowman | 20 |
| Fire Demon | 22 |
| Sapper | 25 |
| Shieldbearer | 28 |
| Orc | 45 |
| Bombardier | 45 |
| Colossus | 420 |

**Wave bonuses.** Each cleared wave pays a lump sum, announced with the
wave-clear line. In Keep Assault it grows by 60 each wave:

| Wave cleared | Bonus |
|---|---:|
| 1 | 200 |
| 2 | 260 |
| 3 | 320 |
| 4 | 380 |
| 5 | — |

Clearing the fifth wave wins the run, so it pays no build bonus; there is
nothing left to build for.

In Endless Siege the bonus follows depth sublinearly:

```
bonus = 140 + 85 × sqrt(wave cleared)
```

It never stops growing, but it deliberately cannot outrun enemy stat pressure —
income rises with the square root of depth while pressure rises linearly with
it.

## Repairs are free

Repairing a damaged defense costs **nothing**. There is no attrition tax in a
normal run — a tower that survives a wave at 10% health is worth exactly as much
as one that was never touched, and leaving damage standing is never correct.

The single exception is the **Iron Levy** siege contract in Endless, which
charges **50% of the defense's base build cost** per repair. Iron Levy is the
only time "sell it and rebuild" beats "repair it", and the only time damage has
a price.

## Selling returns 60%

Selling a defense refunds **60% of everything invested**, upgrades included.
The 40% you lose is the cost of changing your mind, and it is deliberately
cheap enough that redeploying after a topology change is a real option rather
than a punishment.

Press **X** while aiming at a defense, or use the build wheel's sell segment.

## What to spend on

The wave debrief reports **damage per mana** for every placement. That number
is the honest answer to "was this worth it", and it is the one to read before
committing the next purse.

Two ways to spend, and they are genuinely different:

- **Another Tier 1** covers more ground.
- **An upgrade** adds range and power to ground you already cover.

The game does not tell you which is right, and deliberately offers no advisor —
but the numbers are knowable. A tower's damage and fire rate both scale with
tier, compounding to **×1.94 sustained output at T2 and ×3.64 at T3**.

Four Tier 1 Ballistas therefore out-damage one Tier 3 Ballista — **×4.00
against ×3.64** — for the same 400 mana. Coverage wins the raw-throughput
argument outright.

What concentration buys instead is **18% more range, 2.5× the health, and the
Masterwork mechanic** at T3. That last one is not a percentage: it is a new
behaviour, and on a Cannon or a Frost Rune it is worth more than the damage you
gave up.

So the honest rule is: spread while you still have uncovered lanes, and
concentrate only once every lane is answered and you need one position to hold
without you.

## Gold

Gold persists across runs. Unlike mana, **nothing you do inside a wave earns
it** — kills pay mana, not gold. Gold comes from finishing things:

| Source | Gold |
|---|---|
| Winning a run | **100 + 20 per Nightmare level** |
| Winning at a Nightmare **milestone** (every 10 levels) | **+250 per milestone tier** — +250 at N10, +500 at N20, +750 at N30 |
| Every 5th Endless wave from wave 10 | **30 + 4 per wave** — 70 at wave 10, 90 at wave 15 |

Those Endless milestones also **grant a guaranteed item**, so wave 10 is a real
target even on a run you do not expect to survive much past it.

Gold pays for Workshop operations — rerolling, modification, and crafting — and
for **respeccing your allocated rating points**, which costs `25 × points
spent`, minimum 100. Respec gets more expensive the deeper you have committed,
so it is cheap to correct early and costly to reverse late.

Salvaging unwanted items yields materials rather than gold.

## See also

- [Defenses](defenses.md) — what each placement costs
- [Workshop](workshop.md) — what gold is for
- [Waves](waves.md) — the debrief that tells you where the mana went
