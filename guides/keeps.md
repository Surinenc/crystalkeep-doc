# Keeps

A normal run plays a **generated keep** — a fortress built from a seed by the
constraint solver and proved fair before you ever see it. The ground is the
first thing you should read.

**Where that keep comes from depends on the mode.**

| Mode | Keep source |
|---|---|
| Keep Assault | One of a set the generator solved ahead of time, drawn at random |
| Endless Siege | The same set, drawn at random |
| **Weekly Keep** | **Generated live from the week's own seed** |

Assault and Endless play pre-solved ground because solving live takes seconds
and cannot be threaded in the web export — that wait would sit in front of every
launch. The Weekly pays it once, for one keep, and in exchange it reaches the
**generator's full range** rather than a fixed shortlist.

`--seed N` also solves live, and every pre-solved keep records the seed it came
from, so any of them can be regenerated exactly.

## What a keep is made of

The generator works on a macro grid of authored tiles, collapsed under
constraint until the whole board is consistent. One macro cell is 18 metres, so
the grid width sets the size of the keep:

| Grid | Span |
|---|---|
| 7 × 7 | 126 m |
| 8 × 8 | 144 m |
| 9 × 9 | 162 m |
| 10 × 10 | 180 m |

Width is chosen per seed from the archetype's own range: Broken Causeway and
High Gallery run 7 or 8, Foundry Channels and Sunken Court are always 8,
Ringwall runs 8 or 9, the Underkeep is always 9, and the two-crystal Split
Bastion runs **9 or 10**. The pre-solved set Assault and Endless draw from holds
fourteen 8 × 8 keeps, nine 9 × 9, four 7 × 7 and one 10 × 10, so in those modes
you may be reading anything from a 126 m board to a 180 m one. The **Weekly
generates fresh** and rolls whatever width its archetype allows. Doors follow
the shape rather than a fixed number:
**2, 3 or 4** gates, selected from the finished topology by which ones open
ground the others do not. A keep whose second gate would walk the same corridor
as the first simply does not get one.

The crystal sits at the centre — or, on a Split Bastion, two crystals sit
**72 m** apart on either side of it — and the sanctuary around each is
protected ground you cannot build on.

**The ground is stacked.** A keep rises in bands, each a full storey of
**4 m**, joined by ramps. Where a band edge is open the generator may cut a
**drop**: a gap in the wall line where enemies step off the upper band onto the
lower one and cannot climb back. A keep carries at most two, spaced apart and
never next to a crystal, and the fairness contract times routes through them
like any other ground. Twenty of the twenty-eight pre-solved keeps have one.
Read the lip, not the landing: a drop is a route that does not show as a
corridor.

**Door count is mostly a timing statement.** A wave is always four packets,
dealt round-robin across the gates — so a two-door keep sends two packets per
gate in sequence, while a four-door keep sends all four at once, one per gate.
The same troops arrive either way. What changes is whether you get a second
beat to react in, so read a four-door keep first as *less time*.

**The exception is the Unbound.** From wave 4 at most one walks in per lane, so
a four-door keep can receive four casters where a two-door keep receives two.
Two keeps at the same wave and the same Nightmare tier are therefore no longer
the same fight — gate count now buys the enemy something, and it is the one
thing on the board that gets worse the longer you leave it.
See [Waves](waves.md#waves-arrive-as-squads-not-as-a-crowd).

## The seven archetypes

Every generated keep belongs to an **archetype**, named on the level line
alongside its own title — *Foundry Channels · Ashen Run*, *Ringwall · Golden
Ward*. The archetype is the useful half: it tells you the shape of the tactical
problem before you have walked it, and it decides which landmarks the keep can
carry.

| Archetype | The problem it sets | Landmarks it can draw |
|---|---|---|
| **Foundry Channels** | Parallel channels split and reconverge — cover moving fronts, not one splash choke | Oil Channel, Foundry Crucible Pool, Wind Vent, Powder Magazine |
| **Broken Causeway** | Exposed spans can change route — keep alternate coverage ready between waves | Counterweight Bridge, Collapsing Aqueduct, Chain Anchor, Sealed Breach Gate |
| **Split Bastion** | Two crystals anchor two districts — hold one side with what you built, be at the other | Iron Portcullis, Watch Gallery, Stoneward Shrine, Sealed Breach Gate |
| **Sunken Court** | A low basin and an upper rim compete for control — preserve a safe vertical rotation | Floodgate Cistern, Rime Basin, Execution Pit, Collapsing Aqueduct |
| **High Gallery** | Overlooks grant range but hide the lower approaches — defend both elevation bands | Siege Lift, Fallen Bell Tower, Watch Gallery, Signal Brazier |
| **Ringwall** | Several spokes feed one oath court — rotate and overlap rather than overcommit | Oath Plaza, War Horn Rostrum, Rune Pylon, Iron Portcullis |
| **The Underkeep** | Three tiers of ground — surrendering a band is a decision, not a defeat | Descent Gate, Echo Well, Root Bridge, Buried Shrine |

**Only three archetypes can change their own routes mid-run.** Broken Causeway
is built for it — three of its four landmarks are route-changers — while Sunken
Court and Split Bastion carry one each. On **Foundry Channels, High Gallery,
Ringwall and the Underkeep the routes you read in the first build phase are the
routes for the whole siege**, so a placement there is a commitment you will not
be asked to revisit.

**The Split Bastion is the two-crystal keep.** Its crystals stand 72 m apart,
west and east or north and south by seed, and losing either one ends the run.
Wave 1 attacks one crystal, wave 2 the other, and from wave 3 the fronts within
a wave alternate between them. An attack on a crystal comes from the **two
gates nearest that crystal**, so pressure arrives through the local corridors
rather than crossing the keep. The briefing is literal: build to hold one side,
and be at the other.

That is the single most useful thing the archetype name tells you. Read
*Broken Causeway* and hold mana back; read *Ringwall* and spend it.

All seven appear in the pre-solved set, four keeps each — twenty-eight in all.

## The fairness contract

Every generated keep is validated against a named contract before it is
offered. This is the promise that randomness is not noise: a keep you have
never seen is still winnable, and losing is your fault rather than the
generator's.

**Contract version 6.** The rules that shape what you will meet:

| Rule | Guarantee |
|---|---|
| F1 | Every gate has a walkable path that arrives **within 3 m** of the crystal |
| F2 | The fastest enemy needs **at least 8 s** from any gate to the crystal |
| F3 | The slowest enemy arrives **within 50 s** |
| F4 | Lane times differ by **at most 5 s** — fronts arrive together |
| F5 | Every lane narrows to **at most 8.5 m** somewhere |
| F6 | No choke is narrower than **2.6 m** — an orc plus margin |
| F7 | Blockading every lane costs **at most 540 mana** |
| F8 | The crystal keeps **3.5 m** of clear ground |
| F9 | Every gate opens onto clear ground — a **3 × 3 m** box, unobstructed |

**F1 and F9 are the rules you will never notice**, and that is their job. They
do not shape a tactical problem; they refuse keeps that are broken rather than
hard — a gate that opens into rock, or a route that never reaches the crystal
at all. The rest of the contract only means something once these two hold.

F7 is the one worth internalising: sealing every lane is always affordable, so
turtling stays a real option rather than a fantasy. (The four-door ceiling is a
separate, deliberate cap in the generator — `DOORS_MAX := 4` — not something F7
produces on its own.)

**F2 and F3 measure the classes that actually apply pressure.** Two are exempt:
the Colossus and the Unbound. Both are slower than any troop, and neither
threatens anything by arriving late — the Colossus is a milestone that advances
on its own schedule, and the Unbound deals no damage at all. Letting either set
the bound would have stretched every lane's measured time without a single
enemy becoming more dangerous.

Version 6 changed how the rules are measured, not the numbers. Route times are
taken over the finished navigation graph, **drops included**, so a one-way
shortcut counts against F2 and F3 like any corridor. On a two-crystal keep each
gate is timed against its **nearer** crystal, F4 is checked within each
crystal's own group of gates rather than across the whole keep, and F8 is
checked at every crystal.

A keep that fails any rule is discarded and another seed is tried. You never
see the rejects.

## Reading a keep

Before the first wave, spend the build phase looking:

- **The level line** names the archetype. That is your first read, and it is
  free — it tells you whether the routes can change on you.
- **Route ribbons** on the ground show every path the coming wave will walk —
  each gate to the crystal it attacks.
- The **tactical map** (Tab) shows the whole keep at once, including which
  gates attack next and, as an arrow from lip to landing, every **drop**.
- **Chokes** are where lanes narrow. F5 guarantees each lane has one.

The question a keep asks is always the same: where does traffic have to pass,
and what do I want waiting there?

## Landmarks that change the ground

**Every generated keep carries at least one landmark**, and just over half —
**15 of the 28** pre-solved keeps — carry a second. They are not a rare
flourish — assume one is present and go find it.

The catalogue holds **twenty-four**, and which ones a keep can draw depends on
its archetype, so a foundry keep and a rime keep offer different furniture. All
twenty-four appear across the shipped set:

| Landmark | Charges | Radius |
|---|---:|---:|
| Iron Portcullis | 2 | 14 m |
| Collapsing Aqueduct | 1 | 22 m |
| Sealed Breach Gate | 1 | 18 m |
| Counterweight Bridge | 2 | 16 m |
| Siege Lift | 2 | 12 m |
| War Horn Rostrum | 2 | 16 m |
| Wind Vent | 2 | 12 m |
| Floodgate Cistern | 2 | 15 m |
| Oil Channel | 2 | 14 m |
| Powder Magazine | 1 | 11 m |
| Chain Anchor | 2 | 10 m |
| Stoneward Shrine | 2 | 10 m |
| Signal Brazier | 2 | 12 m |
| Rune Pylon | 2 | 7 m |
| Watch Gallery, Rime Basin, Fallen Bell Tower, Oath Plaza, Foundry Crucible Pool, Execution Pit, Descent Gate, Echo Well, Root Bridge, Buried Shrine | — | — |

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

## Development fixtures

Seven hand-authored keeps exist in the build, and **none of them is normal-play
content.** They are fixtures: the test bot needs ground that holds still, and
reproducing a bug needs a map that is the same tomorrow. A regular run always
loads a generated keep.

Most are reachable only with `--keep <name>` or from the dev console, and
restarting or switching modes carries your **current** keep forward rather than
selecting a different one.

`fortress` (the test default), `plaza`, `sprawl`, `caldera`, `bastion`,
`twin_keep`, and `initiation`. Two of the seven a player does meet: `initiation`
backs the Initiation tutorial, and `twin_keep` is what the **CO-OP** entry loads
when you open it from a keep with only one crystal.

Two details matter if you ever load one. Their archetype ids do not always match
their file names — bastion is `verticality`, caldera is `hazard` — which is
visible because Endless records are filed by archetype. And they carry no
sanctuary data, so the crystal's no-build zone does not apply on them.

`twin_keep` has two crystals, West and East, 30 m apart on flat ground — the
hand-built ancestor of the Split Bastion, and the ground most
[co-op](co-op.md) sieges are fought on. In a solo run the two-crystal keep you
meet is the generated Split Bastion described above, not this fixture.

## Seeds

Every generated keep comes from a seed, and the same seed always produces the
same keep. `--seed N` solves one live. The seed is printed with the level line,
so any run can be reproduced exactly.

## See also

- [Defenses](defenses.md) — what you can put on this ground
- [Waves](waves.md) — what walks the routes you just read
- [Game modes](game-modes.md) — Keep Assault, Endless Siege, and the Weekly
