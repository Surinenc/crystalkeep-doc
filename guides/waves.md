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

Most keeps have one crystal. Twin Keep has two, and losing either ends the run
just the same.

## See also

- [Combat](combat.md) — the channel and immunity rules behind every counter
- [Keeps](keeps.md) — the routes the wave will walk
- [Economy](economy.md) — bounties, wave bonuses, and what to do with them
- [Siege Doctrines](doctrines.md) — the choice offered after waves 2 and 4
