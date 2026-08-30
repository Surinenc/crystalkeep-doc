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
| 4 | Goblins, orcs, shieldbearers, sappers, crossbowmen, bombardiers | Can you flank, intercept, and protect what you built? |
| 5 | All ten roles, including a Colossus | All of it, at once |

Wave 3 is where crush becomes mandatory — it is the first wave with orcs, who
take 0.55× from both slash and pierce. Wave 4 adds the two specialists that
punish a static plan: sappers go for your defenses, bombardiers hit for 30.

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

So a four-door keep does not send more enemies. It sends the **same** enemies,
across more fronts, with **less time between the first contact and the last**.
A two-door keep gives you a second beat to react in; a four-door keep spends
that time up front and asks whether every lane can hold unattended.

Within a packet, members spawn **0.2 s apart**. Packets sharing a gate are at
least **2.2 s apart**.

### Shield columns march together; everything else strings out

**A packet containing a Shieldbearer moves at a shared 2.8 m/s** — the
Shieldbearer's own speed. The whole column is speed-locked to its leader, which
is exactly why the pierce-immunity aura is so punishing: the squad stays inside
the shield's cover for the entire approach instead of outrunning it.

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
