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
Court, Underkeep Mechanism, Chainwright Arsenal — grant escalating bonuses as
you equip more pieces of the same set.

Sixteen uniques carry named attributes rather than rolled stats, and are their
own reason to build around.

## See also

- [Nightmare](nightmare.md) — the infinite ladder these curves are tuned against
- [Workshop](workshop.md) — modifying, rerolling, and salvaging
- [Combat](combat.md) — the laws gear cannot buy past
