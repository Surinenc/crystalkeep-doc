# Keeps

A normal run plays a **generated keep** — a fortress the game builds from a
seed and then proves fair before you ever see it. No two runs hand you the same
ground, and the ground is the first thing you should read.

## What a keep is made of

The generator works on a macro grid of authored tiles, collapsed under
constraint until the whole board is consistent. One macro cell is 18 metres, so
the grid width sets the size of the keep:

| Grid | Span |
|---|---|
| 7 × 7 | 126 m |
| 8 × 8 | 144 m |
| 9 × 9 | 162 m |

Width is chosen per seed. Doors follow the shape rather than a fixed number:
**2, 3 or 4** gates, selected from the finished topology by which ones open
ground the others do not. A keep whose second gate would walk the same corridor
as the first simply does not get one.

The crystal sits at the centre, and its surrounding sanctuary is protected
ground you cannot build on.

## The fairness contract

Every generated keep is validated against a named contract before it is
offered. This is the promise that randomness is not noise: a keep you have
never seen is still winnable, and losing is your fault rather than the
generator's.

**Contract version 5.** The rules that shape what you will meet:

| Rule | Guarantee |
|---|---|
| F2 | The fastest enemy needs **at least 8 s** from any gate to the crystal |
| F3 | The slowest enemy arrives **within 45 s** |
| F4 | Lane times differ by **at most 5 s** — fronts arrive together |
| F5 | Every lane narrows to **at most 8.5 m** somewhere |
| F6 | No choke is narrower than **2.6 m** — an orc plus margin |
| F7 | Blockading every lane costs **at most 540 mana** |
| F8 | The crystal keeps **3.5 m** of clear ground |

F7 is the one worth internalising. It is why a keep never has five doors: at 60
mana per blockade the burden of sealing every lane has to stay recoverable, and
a fifth front breaks that.

A keep that fails any rule is discarded and another seed is tried. You never
see the rejects.

## Reading a keep

Before the first wave, spend the build phase looking:

- **Route ribbons** on the ground show each gate's path to the crystal.
- The **tactical map** (Tab) shows the whole keep at once, including which
  gates attack next.
- **Chokes** are where lanes narrow. F5 guarantees each lane has one.

The question a keep asks is always the same: where does traffic have to pass,
and what do I want waiting there?

## Landmarks that change the ground

Some keeps carry landmarks that alter traversal **during the run**. About one
keep in four has one.

| Landmark | Behaviour |
|---|---|
| Collapsing Aqueduct | Collapses on a scheduled wave — routes change |
| Sealed Breach Gate | Opens on a scheduled wave — a new route appears |
| Counterweight Bridge | You raise or lower it between waves |
| Siege Lift | You operate it for vertical movement |

Scheduled changes announce themselves before the wave that triggers them —
`COLLAPSING AQUEDUCT COLLAPSES · ROUTES CHANGE`. The wave it fires on is
derived from the seed, so it is not always the same wave.

A topology change is a **redeployment problem**. The defenses you placed for
the old route are now covering ground the enemy no longer walks.

## Blockades, rerouting, and breaching

Blockades carve the navigation mesh. An enemy compares the detour against
smashing through: if a reasonable detour exists it takes the long way; if the
detour is absurd, or you have sealed the keep completely, it **breaches** the
cheapest wall instead.

Sealing every lane is legal. It is also expensive, and F7 exists precisely to
keep that option affordable rather than mandatory.

## The authored keeps

Six hand-authored keeps sit alongside the generator, reachable with
`--keep <name>`:

| Keep | Archetype id | Notes |
|---|---|---|
| fortress | `fortress` | The gate's default fixture |
| plaza | `plaza` | Open lanes, compensated per contract C3 |
| sprawl | `sprawl` | |
| caldera | `hazard` | |
| bastion | `verticality` | |
| **twin_keep** | `twin_keep_12x12` | **144 m, and two crystals** |

A seventh, `initiation`, backs the tutorial.

The archetype id is not always the file name — bastion is `verticality` and
caldera is `hazard`. That matters because Endless records are filed by
archetype.

These keeps carry no sanctuary data, so the crystal no-build zone does not
apply on them.

### Twin Keep has two crystals

Every other keep in the game defends one crystal. Twin Keep defends two —
**West** at one end and **East** at the other, 30 m apart on a 144 m board.

**Losing either one ends the run.** The game does not check whether the other
still stands — the first crystal to fall ends it. There is no fallback
objective and no partial credit.

One purse, two objectives, and the same wave budget. It is the sharpest test of
whether you can read a keep before committing, because splitting your defenses
evenly is rarely the answer and committing entirely to one side is never one.

The generator never produces two crystals — `structural_synthesis.gd` emits no
`crystals` block at all, so every generated keep falls back to a single
objective at the centre. Twin crystals are an authored-keep feature.

## Seeds

Every generated keep comes from a seed, and the same seed always produces the
same keep. `--seed N` solves one live. The seed is printed with the level line,
so any run can be reproduced exactly.

## See also

- [Defenses](defenses.md) — what you can put on this ground
- [Waves](waves.md) — what walks the routes you just read
- [Game modes](game-modes.md) — Keep Assault, Endless Siege, and the Weekly
