# Keeps

A normal run plays a **generated keep** — a fortress built from a seed by the
constraint solver and proved fair before you ever see it. The ground is the
first thing you should read.

**They are solved ahead of time, not while you wait.** The build ships with a
set of keeps the generator has already solved and validated, and a run picks one
at random. Solving live takes seconds and cannot be threaded in the web export,
which would put that wait in front of every launch. `--seed N` still solves one
live if you want a specific keep, and every shipped keep records the seed it
came from, so any of them can be regenerated exactly.

## What a keep is made of

The generator works on a macro grid of authored tiles, collapsed under
constraint until the whole board is consistent. One macro cell is 18 metres, so
the grid width sets the size of the keep:

| Grid | Span |
|---|---|
| 7 × 7 | 126 m |
| 8 × 8 | 144 m |
| 9 × 9 | 162 m |

Width is chosen per seed, and the shipped set leans small: it is mostly **8 × 8**
with a handful of 7 × 7. A 9 × 9 is possible from the generator but does not
appear in the current build, so in practice you are reading a 126 m or 144 m
board. Doors follow the shape rather than a fixed number:
**2, 3 or 4** gates, selected from the finished topology by which ones open
ground the others do not. A keep whose second gate would walk the same corridor
as the first simply does not get one.

The crystal sits at the centre, and its surrounding sanctuary is protected
ground you cannot build on.

**Door count is a timing statement, not a volume one.** A wave is always four
packets, dealt round-robin across the gates — so a two-door keep sends two
packets per gate in sequence, while a four-door keep sends all four at once,
one per gate. The same enemies arrive either way. What changes is whether you
get a second beat to react in. Read a four-door keep as *less time*, not *more
enemies*. See [Waves](waves.md#waves-arrive-as-squads-not-as-a-crowd).

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

**Every generated keep carries at least one landmark**, and roughly **45%**
carry a second. They are not a rare flourish — assume one is present and go
find it.

The catalogue holds **twenty**, and which ones a keep can draw depends on its
archetype, so a foundry keep and a rime keep offer different furniture. Fifteen
of the twenty appear across the shipped set:

| Landmark | Charges | Radius |
|---|---:|---:|
| Iron Portcullis | 2 | 14 m |
| Collapsing Aqueduct | 1 | 22 m |
| Sealed Breach Gate | 1 | 18 m |
| Siege Lift | 2 | 12 m |
| War Horn Rostrum | 2 | 16 m |
| Wind Vent | 2 | 12 m |
| Floodgate Cistern | 2 | 15 m |
| Oil Channel | 2 | 14 m |
| Powder Magazine | 1 | 11 m |
| Chain Anchor | 2 | 10 m |
| Stoneward Shrine | 2 | 10 m |
| Watch Gallery, Rime Basin, Fallen Bell Tower, Oath Plaza | — | — |

The last row is different in kind: those have **no charges and no radius**. They
are terrain and cover — ground that shapes a fight without being operated.

**Only three landmarks change routes**: the Collapsing Aqueduct, the Sealed
Breach Gate, and the Counterweight Bridge. Everything else changes what happens
where the routes already run.

| Route-changer | Behaviour |
|---|---|
| Collapsing Aqueduct | Collapses on a scheduled wave — routes change |
| Sealed Breach Gate | Opens on a scheduled wave — a new route appears |
| Counterweight Bridge | You raise or lower it between waves — press **T** |

Scheduled changes announce themselves before the wave that triggers them —
`COLLAPSING AQUEDUCT COLLAPSES · ROUTES CHANGE`. The wave it fires on is
derived from the seed, so it is not always the same wave.

Interactive landmarks are operated with **T**, and only between waves — they
spend a charge each time, so a two-charge landmark can be used twice in a run
and a one-charge landmark is a single irreversible decision. (The **Spent
Mechanisms** siege contract removes one charge from every compatible landmark,
which turns the one-charge ones off entirely.) Read the banner before you touch one: it names the verb, the current
state, the charges left, and when the change takes effect.

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

Six hand-authored keeps sit alongside the generator — but **none of them is
normal-play content.** A regular run always calls for a generated keep; the
authored ones are fixtures, kept because the test bot needs ground that holds
still and reproducing a bug needs a map that is the same tomorrow.

They are reachable only with `--keep <name>` on the command line, or from the
dev console. No menu offers them, and restarting or switching modes carries
your **current** keep forward rather than selecting a different one:

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

> **You will not meet Twin Keep in a normal run.** It is an authored fixture,
> reachable only with `--keep twin_keep`. Generated keeps — which is what every
> regular run plays — always defend a single crystal at the centre. What
> follows describes the fixture.

Every other keep in the game defends one crystal. Twin Keep defends two —
**West** at one end and **East** at the other, 30 m apart on a 144 m board.

**Losing either one ends the run.** The game does not check whether the other
still stands — the first crystal to fall ends it. There is no fallback
objective and no partial credit.

One purse, two objectives, and the same wave budget.

**Each wave event commits to one crystal.** Events do not switch target
mid-packet and the choice is never hidden — a packet announced against the West
crystal goes to the West crystal. And the enemies come from the **two gates
nearest that objective**, not from wherever the round-robin lands, so an event
aimed West uses the western corridors.

**The schedule teaches one district before asking you to rotate:**

| Wave | Events target |
|---|---|
| 1 | West, West |
| 2 | East, East |
| 3 | West, East |
| 4 | East, West, East |
| 5 | West, East, West, East |

The first two waves let you learn each side on its own. From wave 3 the events
alternate, and Twin Keep becomes a **rotation problem** — you are not defending
two lanes so much as deciding what can hold without you while you are at the
other end of a 144 m keep.

That is why splitting your purse evenly is rarely right and committing entirely
to one side is never right. What you need is one side that survives unattended
and the mobility to be at the other.

The generator never produces two crystals — `structural_synthesis.gd` emits no
`crystals` block at all, so every generated keep falls back to a single
objective at the centre. Twin crystals are an authored-fixture feature, and
since normal play only ever loads generated keeps, **the two-crystal defense is
not part of the shipped run.**

## Seeds

Every generated keep comes from a seed, and the same seed always produces the
same keep. `--seed N` solves one live. The seed is printed with the level line,
so any run can be reproduced exactly.

## See also

- [Defenses](defenses.md) — what you can put on this ground
- [Waves](waves.md) — what walks the routes you just read
- [Game modes](game-modes.md) — Keep Assault, Endless Siege, and the Weekly
