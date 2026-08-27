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
wave-clear line.

In Endless Siege the bonus follows depth sublinearly:

```
bonus = 140 + 85 × sqrt(wave cleared)
```

It never stops growing, but it deliberately cannot outrun enemy stat pressure —
income rises with the square root of depth while pressure rises linearly with
it.

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

The game does not tell you which is right, and deliberately offers no advisor.
Coverage and concentration should produce comparable output; which one you want
depends on the keep and the wave.

## Gold

Gold persists across runs and pays for Workshop operations — rerolling,
modification, and crafting. Salvaging unwanted items yields materials rather
than gold.

## See also

- [Defenses](defenses.md) — what each placement costs
- [Workshop](workshop.md) — what gold is for
- [Waves](waves.md) — the debrief that tells you where the mana went
