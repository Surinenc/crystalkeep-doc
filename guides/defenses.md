# Defenses

Ten defenses, three schools, one purse. Mana is the only construction resource
in Crystal Keep — there is no separate build currency, no per-type cap, and no
population limit. Everything you place competes with everything else you might
have placed instead.

Defenses are **permanent**. They do not expire, they have no cooldown, and they
do not occupy an ability slot. What you build stays built until it is destroyed
or you sell it.

## You do not start with all ten

Defenses unlock with progress, and the ladder is short:

| Progress | Available |
|---|---|
| Initiation not finished | **Blockade, Ballista** — the two the tutorial teaches |
| Initiation complete | **+ Cannon, Frost Rune, Wall Maul** (5) |
| 1 Keep Assault cleared | **+ Spikes, Tar, Wall Blades** (8) |
| 2 Keep Assault clears | **+ Springboard, Harpoon** (all 10) |

Two things worth knowing about that table.

**Skipping the Initiation unlocks everything immediately.** A skipped tutorial
is treated as "you already know this" and hands you all ten at once, while
finishing it hands you five. If you skip, you get the whole toolbox and none of
the teaching.

**Only Keep Assault clears count.** Weekly runs are normalized and do not
record a clear, and Endless has no clear to record — so the last five defenses
come from winning the campaign twice, and nothing else advances them.

## The three schools

| | | | | |
|:--:|:--:|:--:|:--:|:--:|
| <img src="../assets/defenses/blockade-v1.png" width="82" alt=""> | <img src="../assets/defenses/slow-v1.png" width="82" alt=""> | <img src="../assets/defenses/ballista-v1.png" width="82" alt=""> | <img src="../assets/defenses/cannon-v1.png" width="82" alt=""> | <img src="../assets/defenses/tar-v1.png" width="82" alt=""> |
| Blockade | Frost Rune | Ballista | Cannon | Tar |
| <img src="../assets/defenses/spikes-v1.png" width="82" alt=""> | <img src="../assets/defenses/spring-v1.png" width="82" alt=""> | <img src="../assets/defenses/wall_blades-v1.png" width="82" alt=""> | <img src="../assets/defenses/harpoon-v1.png" width="82" alt=""> | <img src="../assets/defenses/wall_maul-v1.png" width="82" alt=""> |
| Spikes | Springboard | Wall Blades | Harpoon | Wall Maul |

**Fortifications** mount on the floor and hold ground.
**Floor traps** mount on the floor and trigger on contact or proximity.
**Wall traps** mount on walls, which turns vertical surface into build space.

Every defense has HP. Nothing is indestructible — including the Blockade.

## Fortifications

| Defense | Cost | Channel | Range | Notes |
|---|---:|---|---:|---|
| <img src="../assets/defenses/blockade-v1.png" width="34" alt=""> Blockade | 60 | — | — | 350 HP. Reroutes enemies; does not attack. |
| <img src="../assets/defenses/slow-v1.png" width="34" alt=""> Frost Rune | 80 | — (chill) | 3.5 m | Aura. 40% slow. 150 HP. |
| <img src="../assets/defenses/ballista-v1.png" width="34" alt=""> Ballista | 100 | Pierce | 3.5–14 m | 90° arc, 15% crit at 2.0×. 220 HP. |
| <img src="../assets/defenses/cannon-v1.png" width="34" alt=""> Cannon | 125 | Crush | 4.0–12 m | 360° arc, 3.25 m splash, staggers. 220 HP. |

**Minimum range is real.** The Ballista cannot hit anything closer than 3.5 m
and the Cannon nothing closer than 4.0 m. A tower placed on top of a choke has
a hole where the fight is.

**Aim gating.** Targeted defenses hold fire until the head is within **8° of
the target**. Traverse speed therefore matters: the Ballista swings at 120°/s,
the Cannon at 60°/s. A Cannon covering a fast lane spends much of the wave
turning.

**Cannons carry further downhill.** A Cannon adds **1 m of range for every
metre it stands above its target**, capped at **+25%** — so a 12 m Cannon
reaches 15 m from a high enough perch. Nothing else gains this: a flat
trajectory has no height dividend, so the Ballista's reach is the same uphill
or down. While you are placing, the ghost draws the bonus as an amber ring and
hides it on flat ground, so the elevation is priced before you commit.

## Floor traps

| Defense | Cost | Channel | Trigger | Notes |
|---|---:|---|---|---|
| <img src="../assets/defenses/tar-v1.png" width="34" alt=""> Tar | 65 | — (tar) | Contact | 40% slow. Drains on contact. 160 HP. |
| <img src="../assets/defenses/spikes-v1.png" width="34" alt=""> Spikes | 70 | Pierce | Proximity | 55 power, 1.6 s cycle. 130 HP. |
| <img src="../assets/defenses/spring-v1.png" width="34" alt=""> Springboard | 90 | Crush | Proximity | Displaces. 2.2 s cycle. 140 HP. |

## Wall traps

| Defense | Cost | Channel | Trigger | Notes |
|---|---:|---|---|---|
| <img src="../assets/defenses/wall_blades-v1.png" width="34" alt=""> Wall Blades | 105 | Slash | Proximity | 63 power, 1.25 s cycle. 165 HP. |
| <img src="../assets/defenses/harpoon-v1.png" width="34" alt=""> Harpoon | 125 | Pierce | Proximity | 128 power, **50% armour pierce**, 12 m. 150 HP. |
| <img src="../assets/defenses/wall_maul-v1.png" width="34" alt=""> Wall Maul | 135 | Crush | Proximity | 158 power, staggers, 3.0 s cycle. 180 HP. |

The Wall Maul is the heaviest single hit available and it staggers — which is
why it is one of the few good answers to a Shieldbearer column, and why it does
nothing useful against a runner it cannot catch.

## What towers shoot at

A targeted defense picks the **nearest** enemy inside its envelope — within
range, outside minimum range, and inside its firing arc. Two corrections are
applied before that choice.

**A tower will not spend a shot on something it cannot hurt.** An enemy the
tower's channel reads as a hard zero is skipped outright: a Ballista does not
aim into a Shieldbearer's front, and a Cannon does not aim at a Fire Demon. It
services another target instead. This does not soften the counter law — it
means the missing counter is yours to bring, rather than something a tower will
waste itself against while the lane walks past.

**Ballistas and Cannons prefer their own counters.** Each weights certain roles
ahead of raw distance:

| Tower | Serviced first | Left for last |
|---|---|---|
| **Ballista** | Fire Demon, then Bombardier and Sapper, then Runner | Shieldbearer, Orc |
| **Cannon** | Shieldbearer and Orc, then Crossbowman and Goblin | Runner |

The weighting outranks distance within the envelope, so a Ballista will leave a
closer orc alone to answer the sapper behind it. Damage, range, rate and
immunity are untouched — only the order of service changes.

The Warden's mark overrides both. If an enemy in the envelope carries a **Hex**
mark, the tower takes that one instead — by the same reckoning if several are
marked. That is the whole mechanism behind Hex as a command: you are not
buffing the tower, you are choosing its target.

## Traps wear out

Every trap trigger costs the trap durability — 2.0 per trigger for Spikes,
Springboard and Wall Blades, 2.5 for the Harpoon, 3.0 for the Wall Maul. Tar
and Frost Runes drain continuously while something stands in them rather than
per trigger.

**Tier 3 halves wear.** A fully upgraded trap degrades at half rate, which is a
second reason to concentrate rather than spread in a heavily-trafficked lane.

## Repair is free

Repairing a damaged defense costs **nothing** in a normal run. There is no
reason to leave a damaged tower standing, and no reason to sell and rebuild one
that is merely hurt.

The exception is the **Iron Levy** siege contract in Endless, which charges
50% of the defense's base build cost per repair. That contract is the only
time the sell-and-rebuild calculation is worth making.

## Placement rules

A ghost shows where the defense will land. It refuses for concrete reasons:

- **Surface mismatch.** Floor defenses need a near-level surface; wall traps
  need a near-vertical one. The preview will not lie to you about this.
- **Flat ground, for Blockades only.** Floor traps keep the slope allowance and
  will sit on a ramp; the Blockade demands ground that is genuinely level. It
  works by carving the navigation mesh that the detour-versus-breach decision
  is read from, and on the 12.5° ramp of a 4 m storey that carve means nothing.
  If a ghost refuses on a slope where a trap was accepted, this is why.
- **Distance.** You must be within **14 m** of the spot.
- **Overlap.** The footprint must be clear of world, enemies, other defenses
  and the crystal.
- **Sanctuary.** The ground around the crystal is protected — see below.

### The sanctuary is protected ground

On generated keeps, the floor around the crystal is a no-build zone, announced
in the game as *"Sanctuary floor is protected"*. It is not a radius: it is the
set of crystal and sanctuary cells, and the blocked area grows with the
footprint of what you are trying to place. A wide defense is refused further
out than a small one.

The authored keeps reached with `--keep` carry no sanctuary data, so the rule
does not apply there. That asymmetry is a property of those keeps, not a design
choice about the crystal.

## Tiers and selling

Defenses upgrade through **three tiers**, paid from the same purse. The cost is
derived from the build cost rather than fixed:

| Step | Cost |
|---|---|
| T1 → T2 | the defense's base cost |
| T2 → T3 | **twice** the base cost |
| T3 | no further upgrade |

So a Ballista at 100 costs 100 to reach T2 and 200 more to reach T3 — 400 mana
in total for one fully upgraded tower, against 400 for four T1 Ballistas
covering four times the ground.

### What a tier actually buys

Upgrading is not a flat power bump. Towers scale on four axes at once:

| | T1 | T2 | T3 |
|---|---:|---:|---:|
| Damage | ×1.00 | ×1.55 | ×2.35 |
| Fire rate | ×1.00 | ×1.25 | ×1.55 |
| Range | ×1.00 | ×1.08 | ×1.18 |
| Health | ×1.00 | ×1.55 | ×2.50 |

Damage and rate compound, so **sustained output is ×1.94 at T2 and ×3.64 at
T3**. Traps take a single effect multiplier instead — **×1.55 at T2, ×2.25 at
T3** — applied to their control strength.

Now the central trade can be answered honestly. Four T1 Ballistas out-damage
one T3 Ballista on raw throughput (×4.00 against ×3.64) for the same 400 mana.
Concentration is not buying you damage. It is buying **18% more range, two and
a half times the health, one target it cannot lose**, and the masterwork
mechanic below.

Spread wins when you have ground to cover and lanes to answer. Concentration
wins when there is one choke everything must walk and you need it to hold
without you.

### Masterwork mechanics

Tier 3 is called **Masterwork**, and it is where a defense stops being a bigger
version of itself and gains a new behaviour:

| Defense | At T2 | At Masterwork (T3) |
|---|---|---|
| **Ballista** | Bolts pierce through one enemy | Flank hits **fork** to a second target for 45% damage |
| **Cannon** | Shells stagger for 0.16 s | Stagger 0.24 s, plus a **concussive outer ring** |
| **Springboard** | Adds 0.12 s stagger | 0.20 s stagger on top of the launch |
| **Frost Rune** | — | Crushing a **Brittle** enemy releases a shatter pulse |
| **Tar** | — | Fire on an **oiled** enemy spreads the coating |

This is the real argument for a third tier, and it is why the answer changes by
defense. A Masterwork Frost Rune gains a mechanic that did not exist before; a
Masterwork Blockade is just a tougher wall.

**Masterwork also changes what Mending Ward does to it.** Mend primes any
defense, cutting its cooldown — but on a Masterwork defense it removes the
cooldown entirely and the defense fires at once. That turns your heal into an
on-demand trigger, and it is the strongest reason to take one key defense to
T3 rather than two to T2. See [The Warden](warden.md#mending-ward--30-ward-04-s-windup-14-m).

Selling returns **60%** of everything invested — including upgrades.

There are two ways to sell: press **X** while aiming at a defense, or open the
build wheel while aiming at one and choose the sell segment.

## Upgrading

Aim at a placed defense and open the build wheel. It becomes a three-option
context menu — **upgrade**, **sell**, or select that defense type for building.

**The wheel is the only way to upgrade.** Aiming at a defense shows a nameplate
prompting `E  UPGRADE` with a cost, but **E** casts Hex of Frailty; there is no
upgrade binding in the control map at all. Pressing it spends 35 Ward and
upgrades nothing. Use the wheel.

## See also

- [Combat](combat.md) — channels, immunities, and what each enemy refuses
- [Economy](economy.md) — mana income, bounties, and refunds
- [The Warden](warden.md#the-commander-aura) — the aura that bonds to what you built
- [Keeps](keeps.md) — the ground you are building on
- [Siege Doctrines](doctrines.md) — free Masterwork mechanics, twice a run
