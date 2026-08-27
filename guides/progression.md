# Progression and equipment

Crystal Keep is a tactical fortress puzzle with persistent progression — not an
infinite loot RPG that can overpower the puzzle. That ordering is the design,
and it is enforced by maths rather than by good intentions.

Gear changes **how you express a valid solution**. It never removes the need
for one.

## The rule gear cannot break

A Ballista may become faster, longer-ranged, and better at covering a difficult
angle. It still deals **exactly zero** through a Shieldbearer's front. A Cannon
may become enormous. It still deals **zero** to a Fire Demon.

No item level, no rarity, no rating, and no critical hit changes a hard-zero
law. See [Combat](combat.md) for the full list.

## Ratings are compressed, not inflated

Item affixes scale linearly with item level, but they do not reach you that
way. Every rating passes through a logarithmic curve before it becomes a
multiplier:

```
effective = 100 × ln(1 + rating / 100)
multiplier = 1 + effective × coefficient
```

For defense power the coefficient is 0.007. What that means in practice:

| Rating | Multiplier |
|---:|---:|
| 50 | ×1.28 |
| 200 | ×1.77 |
| 1,000 | ×2.68 |
| 5,000 | ×3.75 |
| 50,000 | ×5.35 |

A **thousandfold** increase in rating buys roughly **four times** the power.
This is deliberate. Numbers that scale without limit are what killed the tower
game in this genre's ancestors, and the curve is the defence against it.

## Levels and rating points

Kills pay experience as well as bounty. Experience is **not** a per-run
resource — it persists, and it is the second half of your power alongside gear.

**XP per kill** is `round(sqrt(monster level))`, tripled for a **specialist**
(Shieldbearer, Sapper, Frostbound, Fire Demon, Crossbowman, Bombardier). So the
enemies that threaten your keep most are also worth three times the progress,
and deeper content pays more per kill without paying explosively more.

**Each level grants one rating point.** The cost of the next level is
`100 + 35 × level^0.68`, which grows sublinearly — level 10 costs about 270 XP,
level 100 costs about 900. Levelling slows down, but it never stops meaning
anything.

Points go into eight ratings, and it is a real allocation decision:

| Warden | Defense |
|---|---|
| Warden Power | Defense Power |
| Warden Vitality | Defense Fortitude |
| Ward Capacity | Defense Rate |
| Ward Regeneration | Defense Reach |

Allocated points enter **the same rating pool as your gear**, which means they
pass through the same logarithmic curve. A point is therefore worth far more in
a rating you have neglected than in one your equipment has already pushed high —
the curve makes specialisation self-limiting and breadth quietly efficient.

You can undo an allocation at the Workshop. **Respec costs `25 × points spent`
gold, minimum 100**, and it refunds everything at once. Correcting course early
is cheap; reversing a hundred levels of commitment is not.

**The Weekly Keep awards no experience at all.** Normalized runs pay no XP and
no levels, because the mode exists to compare play rather than accumulate.

## Rarity and item level do different jobs

**Rarity** controls how many stats an item carries. Seven tiers: Common,
Uncommon, Rare, Epic, Legendary, Mythic, Ancestral.

**Item level** controls the roll range of those stats.

A high-rarity low-level item has many weak stats; a low-rarity high-level item
has few strong ones. Neither strictly dominates.

## What the stats do

Warden stats: **Warden Power** (weapon and spell damage), **Warden Vitality**
(maximum health), **Ward Capacity**, **Ward Regeneration**.

Defense stats: **Defense Power**, **Defense Fortitude**, **Defense Rate**,
**Defense Reach**, plus specific ones — Blockade Health, Ballista Traverse,
Ballista Critical, Cannon Area, Projectile Speed, Trap Reset, Trap Wear
Resistance, Springboard Impulse, Harpoon Pull, Status Duration.

Defense stats are tagged by school, so an affix tagged `fortification` does
nothing for your wall traps.

## Loot is claimed, never collected

Items drop on the field during a wave and **stay there**. Proximity lets you
inspect one; it enters your vault only when you explicitly choose to Loot it.
Nothing is picked up automatically.

Unclaimed items are lost when the run ends. The victory screen reports what you
claimed and what you left behind, honestly.

## Sets and uniques

Six equipment sets — Warden's Oath, Bastion Foundry, Windlass Covenant, Powder
Court, Underkeep Mechanism, Chainwright Arsenal — grant bonuses at **2, 4, 6
and 8 equipped pieces**. There are eight slots, so a full set is achievable and
all four tiers stack when it is.

Warden's Oath, as an example of the shape:

| Pieces | Bonus | Grants |
|---:|---|---|
| 2 | OATHBOUND EDGE | Warden Power |
| 4 | UNBROKEN BEARER | Warden Vitality |
| 6 | WARDEN'S AEGIS | Ward Capacity and Regeneration |
| 8 | KEEP'S CHAMPION | Warden Power and Ward Capacity |

### Set bonuses scale with resonance — and resonance is an average

A set bonus is not a fixed number. Each tier grants `coefficient × resonance`
rating, and **resonance is the average item level of the pieces of that set you
have equipped**.

That single word — average — is the mechanic. Adding a piece to reach the next
tier can make you *weaker overall* if that piece is far below the level of the
rest: it drags the mean down, and the mean multiplies **every** active tier at
once, not just the one you unlocked.

So the real question is never "do I have four pieces". It is "do I have four
pieces of comparable level". A tight four-piece set at high level beats a
ragged six-piece set carrying a levelling relic.

Sixteen uniques carry named attributes rather than rolled stats, and are their
own reason to build around.

## See also

- [Nightmare](nightmare.md) — the infinite ladder these curves are tuned against
- [Workshop](workshop.md) — modifying, rerolling, and salvaging
- [Combat](combat.md) — the laws gear cannot buy past
