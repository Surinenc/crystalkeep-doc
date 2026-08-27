# The Warden

<p align="center"><img src="../assets/warden/warden.png" alt="The Warden" width="200"></p>

You are not a camera above the battlefield. You are a body in it, with a sword,
three spells, and a limited pool of Ward to spend on them.

The Warden's job is not to out-damage the keep. It is to be wherever the keep
is weakest, and to make the defenses hit harder while you are there.

## Health and Ward

You have two resources and they behave nothing alike.

**Health** falls when you are hit and does not regenerate on its own. If it
reaches zero you go down and respawn on a timer — **5 seconds during combat,
1.5 outside it** — and **the run continues**. A fallen crystal is the only
defeat condition in Crystal Keep. Dying is a setback, not a loss, and you
should be willing to spend yourself on a lane that matters.

**Ward** is a pool of **100** that refills at **6 per second**, constantly and
for free. Both numbers are bases — equipment scales the pool (`hero_ward`) and
the regeneration (`hero_ward_regen`) independently, as it scales your health
and sword damage. It pays for your spells and your dash. Because it regenerates and is
capped, Ward at full is Ward being wasted — if you are standing at 100 in the
middle of a wave, you are under-using your kit.

## Movement

| | |
|---|---:|
| Run speed | 6.5 m/s |
| Walk speed | 3.0 m/s |
| Jump | 7.7 |
| Dash speed | 14.0 m/s |
| Dash duration | 0.18 s |
| Dash cost | 15 Ward |
| Dash cooldown | 2.0 s |

The dash has **no invulnerability frames**. It is a repositioning tool, not a
dodge — it moves you out of where the damage will be, and does nothing about
damage already landing.

## The sword

A two-step combo dealing **30** base damage per swing in the **slash** channel,
with a reverse cut on the second step. Swings are **0.5 s** apart, and a
buffered attack turns into the second cut at **0.3 s** — pressed during
recovery it chains rather than being dropped, so committing to the first swing
does not cost you the second.

**The sword cleaves.** Each swing tests a sphere roughly **1.5 m** across,
centred about **1.35 m** in front of you, and damages **every** enemy inside it
— not the nearest one. Against a packed group of goblins one cut is one cut
per goblin. It also applies a small knockback to each.

This is why wading into a swarm is correct and duelling a single orc is not:
your damage scales with how many bodies are pressed together in front of you.

Slash is the wrong channel against orcs (0.55×) and bombardiers (0.70×), and
the right one against goblins (1.25×) and crossbowmen (1.25×).

Sword damage is a base too — `hero_power` on your equipment multiplies it.

## The three spells

| | | |
|:--:|:--:|:--:|
| <img src="../assets/spells/hex-medallion-v1.png" width="90" alt="Hex of Frailty"> | <img src="../assets/spells/mend-medallion-v1.png" width="90" alt="Mending Ward"> | <img src="../assets/spells/fireball-medallion-v1.png" width="90" alt="Fireball"> |
| **Hex of Frailty**<br>E · 35 Ward | **Mending Ward**<br>F · 30 Ward | **Fireball**<br>C · 45 Ward |

All three are **position-cast**: you aim at a point, there is a windup, and the
effect lands there. Casting roots you for the windup, so cast placement is a
commitment.

### Hex of Frailty — 35 Ward, 0.5 s windup, 14 m

Curses a **4 m** zone for **18 seconds**. Everything inside takes **30% more
damage from any source** — your sword, your traps, and every tower firing into
it.

**Hex zones never stack.** Two overlapping Hexes do not compound; the strongest
one applies. Casting a second Hex into the first is wasted Ward — the answer to
a bigger problem is a bigger lane, not a deeper curse.

The zone also **marks one enemy** near the cast point as a priority target, and
every tower that can see it retargets onto the mark. That mark is separate from
the zone and much shorter: **6 seconds, one enemy**. The 18-second field keeps
amplifying whatever walks through it long after the mark has expired.

So Hex does two jobs on different clocks. Cast it on ground you expect traffic
to cross, and the field pays for the whole wave; cast it on the thing you want
dead now, and the mark redirects your towers for six seconds.

This is your strongest spell and it deals no damage at all. Hex is how you tell
a lane full of defenses where to concentrate.

### Mending Ward — 30 Ward, 0.4 s windup, 14 m

Heals the nearest defense **120 HP over 8 seconds** and grants it **−25% damage
taken** while active. Saving a defense that was about to die pays **+3 Ward**,
which is most of the cast back.

**Mend also primes the defense — and this is the half nobody reads.** Every
cast cuts the target's cooldown, and how much depends on its tier:

| Target tier | Cooldown removed |
|---|---|
| T1 | 0.30 s (tower) / 0.25 s (trap) |
| T2 | 0.80 s (tower) / 0.75 s (trap) |
| **T3 — Masterwork** | **all of it — the defense fires immediately** |

So Mend on a Masterwork Cannon is not a heal. It is a **second shot, on
demand**, for 30 Ward. On a Masterwork Wall Maul it is a free trigger the
instant something walks past. The screen tells you it happened —
`MECHANISM PRIMED` on a tower, `TRAP PRIMED` on a trap.

From **T2 upward** a mended tower also **drops its current target and picks a
new one immediately**, which is the cheapest way to pull a tower off something
it cannot hurt.

Mend is therefore three spells wearing one name: a heal, a damage reduction,
and a trigger. Against a Masterwork board it is the trigger that matters most,
and holding a Mend for the moment a Colossus enters the Cannon's arc is a
better use of 30 Ward than repairing anything.

### Fireball — 45 Ward, 0.8 s windup, 20 m

A travelling projectile — **22 m/s**, up to 20 m — that bursts for **30
impact damage** in a **3 m** radius and sets everything it catches **burning**:
**4 damage every 0.5 s for 6 seconds**, or **48 more**. Both halves are the
**fire** channel.

So a clean Fireball is **78 damage** to a single target, and 78 to each target
in the burst. That is its real weight, and the burn is most of it.

Burn **refreshes rather than stacks** — a second Fireball on the same enemy
resets the 6 seconds instead of doubling the rate. Spreading Fireballs across
new targets is worth more than stacking them on one.

Note the two enemies that care most: a Frostbound takes **1.50×** from fire,
and a Fire Demon takes **zero** — from the impact *and* the burn. Fireball is a
specialist answer, not a general one.

## Counterplay pays Ward

Skilled interventions refund into the pool that funds them:

| Act | Ward |
|---|---:|
| Interrupt a Giant | +8 |
| Interrupt Artillery | +5 |
| **Intercept a Sapper** | **+4** |
| Save a defense with Mend | +3 |
| Flank a Shieldbearer | +2 |
| Colossus last assault | +2 |
| Keeper's Rhythm | +1 |

The loop closes on purpose: support the towers, earn Ward, cast more support.
Ward's cap keeps it from becoming an economy.

## Controls

| Input | Action |
|---|---|
| WASD + mouse | Move and look |
| Space | Jump |
| Shift | Dash |
| Left mouse | Sword / lock placement / confirm facing |
| E / F / C | Hex / Mend / Fireball |
| 1–0, or B / middle mouse | Select a defense, or open the build wheel |
| R / Q, or right mouse | Adjust facing / back out or cancel |
| X | Sell the defense under the crosshair |
| **T** | **Interact with a landmark, or inspect an item drop** |
| G | Start the next wave |
| I / K / M | Ledger / Workshop / game modes |
| Tab | Tactical map |
| **N** | **New generated keep** (before wave 1) |
| **Enter** | **Restart after victory or defeat** |
| F4 | Recall the last wave debrief |
| **[ ]** | **Cycle the loot filter** — only while the tactical map is open |
| Esc | Pause |

## See also

- [Combat](combat.md) — channels, immunities, and what each enemy refuses
- [Defenses](defenses.md) — what your Hex is amplifying
- [Progression](progression.md) — how equipment changes the Warden
