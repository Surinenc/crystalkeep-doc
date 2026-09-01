# Waves

A run is five waves. You start each one yourself — the game never begins a wave
for you, and unspent build time is time you chose not to use.

## The build and combat rhythm

**Build phase.** Spend mana, read routes, place and aim. Press **G** when
ready.

**Combat phase.** Enemies pour from the announced gates toward the crystal. You
can still build and sell mid-fight, and mana keeps arriving from kills.

## The five waves

Composition escalates, and each wave asks a different question. This is
authored, not random — the same five shapes arrive every run, on whatever
ground the generator handed you.

| Wave | Composition | The question |
|---|---|---|
| 1 | Goblins | Can you hold a lane at all? |
| 2 | Goblins, runners | Can you catch something fast? |
| 3 | Goblins, runners, orcs, crossbowmen | Do you have crush, and can you break line of sight? |
| 4 | Shieldbearers, sappers, goblins, crossbowmen, bombardiers, **Unbound** | Can you flank, intercept, and protect what you built? |
| 5 | All eleven roles, including a Colossus | All of it, at once |

Wave 3 is where crush becomes mandatory — it is the first wave with orcs, who
take 0.55× from both slash and pierce.

**Wave 4 is built as a demolition wedge.** Its two heavy lanes are nothing but
shields and Sappers — two of each on the first, three of each on the second —
and every shield spawns ahead of every Sapper, so what arrives is a front rank
of cover with a rear rank of demolition behind it. The orcs are gone; this wave
is not asking whether you own crush, it is asking whether you can get past a
wall of pierce immunity to reach what is dismantling your keep.

**Wave 4 is also where the Unbound arrives**, and it changes what the last two
waves are asking. At most one walks in per lane, near the front of it, and two
never arrive together on different lanes.

It arrives early on purpose. At 1.45 m/s it is the slowest thing in the game,
so **everything spawned after it overtakes it** — and being overtaken is the
mechanic, because the bodies passing it are the ones it stamps. An Unbound that
came in late would trail a wave it could never catch and buff nothing, so the
game would rather a lane went without one.

It is announced like any other beat, and the telegraph is unusually literal:
`UNBOUND — KILL THE UNBOUND`, countered by `CONTROL DIES WHILE IT LIVES`. Every
second it survives raises what its escort costs you. See
[Enemies](enemies.md#unbound--270-hp-145-ms-0-damage-60-mana).

## Waves arrive as squads, not as a crowd

A wave is **four packets**, and a packet is a squad with an authored
composition — wave 1 is four pairs of goblins, wave 4 leads with
shieldbearer/goblin/orc/sapper columns.

The squad is the unit that matters, because **squad auras only cover
squadmates**. A Shieldbearer protects the enemies it arrived with, not whatever
happens to be standing nearby.

**Packets are dealt round-robin across the keep's gates**, and the count does
not change with the number of gates. This is worth understanding properly:

| Gates | How the four packets arrive |
|---:|---|
| 2 | Two per gate, in sequence — a second wave-front behind the first |
| 4 | One per gate, **all starting at the same moment** |

So a four-door keep does not send more troops. It sends the **same** troops,
across more fronts, with **less time between the first contact and the last**.
A two-door keep gives you a second beat to react in; a four-door keep spends
that time up front and asks whether every lane can hold unattended.

**One thing does scale with gates.** The Unbound is dealt one per lane from
wave 4, so a four-door keep can carry four of them and a two-door keep two. That
is a deliberate exception: it deals no damage, so it adds no direct pressure,
and the extra difficulty is entirely in what it protects.

Within a packet, members spawn **0.2 s apart**. Packets sharing a gate are
**3 to 9 s apart** — long enough for a clump to clear the gate, short enough
that you are never watching an empty lane. The same wave on the same keep
always breathes the same way.

### Shield columns march together; everything else strings out

**A packet containing a Shieldbearer moves at a shared 2.8 m/s** — the
Shieldbearer's own speed. The column holds that pace while the shield is doing
its job, which is exactly why the pierce-immunity aura is so punishing: the
squad stays inside the cover for the approach instead of outrunning it.

**A Sapper only waits while the shield is actually protecting it**, and breaks
to its own 3.8 m/s the moment it is not:

| It matches the shield when | It runs at full speed when |
|---|---|
| The shield is ahead of it, within **6 m**, and the threat is pierce the shield covers | The shield falls behind or drops out of cover — it sprints to catch up |
| | It closes to **4.25 m** of what it came to demolish |
| | The threat is not pierce, so the shield answers nothing |
| | Its squad has no living Shieldbearer at all |

So the escort is a condition, not a leash. Kill the Shieldbearer and the
Sappers behind it do not slow down in mourning — they speed up. Break the
formation for the pierce immunity, not to strand the demolition.

**A shield-and-Sapper packet also picks its target together.** Once one member
has legitimately acquired a defense, the rest of the packet can commit to that
same defense and stay committed within **20 m** while the slower shield closes
on it. Each still walks its own reachable path — nothing teleports — but what
arrives is a wedge converging on one of your buildings rather than four enemies
choosing separately.

**Every other packet keeps individual speeds.** Runners leak ahead of their
own squad on purpose, arriving alone and early while the goblins behind them
are still walking. That leak is deliberate design, not a spacing accident — it
is what stops a single well-placed answer from catching an entire packet.

The practical rule: if the packet has a shield, you are fighting a formation and
should break it. If it does not, you are fighting a queue and should meet the
front of it.

## Wave events announce their own counter

Each wave carries named tactical beats, and each one tells you what answers it
before it arrives:

```
SWARM PROBE               →  SLASH / BLAST
RUNNERS AT THE GATES      →  PIERCE / TAR
ARMORED COLUMN            →  CRUSH / BRITTLE
CROSSBOW LINE FORMING     →  BREAK LOS / CLOSE
SAPPERS UNDER SHIELDS     →  INTERCEPT / CRUSH
BOMBARDIER ENTERING       →  SPREAD / INTERRUPT
FROSTBOUND FRONT          →  FIRE / TAR
UNBOUND                   →  CONTROL DIES WHILE IT LIVES
SIEGEBREAKER COLOSSUS     →  CRUSH ARMOR / FLANK SEAL
```

This is deliberate design: adaptation should be a conversation, not a gotcha.
You are told what is coming and given a build phase to answer it. Ignoring the
telegraph is a choice.

## Specialists worth naming

**Sappers** target your defenses rather than the crystal. They are fast (3.8
m/s), fragile (80 HP), and take 1.35× from pierce. Left alone they will
dismantle the lane you spent your purse on.

**Crossbowmen** shoot from range and need line of sight. Break it or close the
distance — they take 1.25× from slash and resist pierce.

**Bombardiers** are slow (2.0 m/s) and heavy (210 HP) and hit for 30. They can
be interrupted, and interrupting one pays **+5 Ward**.

**The Unbound** arrives from wave 4 and never touches you — no weapon, no
damage, 270 HP, walking at 1.45 m/s. What it does is switch your control
channels off one at a time for everything within 6 m of it, and it gets
stronger simply by staying alive. It cannot run and it takes 1.25× from slash
and pierce, but it has the health to survive a trap line, so the question it
asks is whether you can reach the back of a wave while the front of it is still
arriving.

**The Colossus** arrives on wave 5 with 1700 HP and 72 damage. It cannot be
displaced at all, resists most control, and takes 1.35× from crush. It is the
one enemy that will not be solved by position alone.

## Between waves

When a wave clears you receive:

- **Bonus mana**, announced with the wave-clear line
- Any **loot** you picked up during the fight
- A **wave debrief** — per-defense damage, kills, control, and damage per mana
- **Intel** on the next wave's composition and counters
- On some keeps, a **landmark epoch** that changes the routes

The debrief is the honest record of which placements earned their cost. Read it
before spending the next purse — a defense with high damage per mana deserves
an upgrade, and one contributing nothing deserves selling.

## A fallen crystal is the only loss condition

Enemies that reach a crystal damage it; it has 300 health. When it falls, the
run ends. Your own death is a respawn timer — 5 seconds in combat, 1.5 outside
it — and nothing more.

Most keeps have one crystal. A **Split Bastion** has two, 72 m apart, and
losing either one ends the run just the same — waves alternate which of them
they attack. See [Keeps](keeps.md#the-seven-archetypes).

## The crystal ends a wave that will not end

Each combat phase starts a **120-second** countdown, which runs while any enemy
is alive or still waiting to spawn. The crystal warns you at 60, 30 and 10
seconds — *"The crystal thrums with gathering power…"* — and at zero it
annihilates every enemy on the field and empties what was still queued.

This is a failsafe against a wave that cannot finish — a straggler stalled on
ground it cannot leave, a remnant that cannot path to you — so that nothing
soft-locks a night. It is priced so it never becomes a tactic: **an enemy the
purge kills pays nothing at all.** No experience, no bounty, no item roll, no
kill credit for the defense that had been grinding it down, and no aura
signature. A wave you hand to the crystal is a wave you were not paid for.

In an ordinary wave you will never see the countdown. If the warnings start
arriving while you are otherwise winning, something is stuck out there.

## See also

- [Combat](combat.md) — the channel and immunity rules behind every counter
- [Keeps](keeps.md) — the routes the wave will walk
- [Economy](economy.md) — bounties, wave bonuses, and what to do with them
- [Siege Doctrines](doctrines.md) — the choice offered after waves 2 and 4
