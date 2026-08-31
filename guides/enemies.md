# Enemies

Eleven enemy roles. Each has a channel it fears, a channel it shrugs off, and —
in several cases — something it is flatly immune to. Reading this table is
cheaper than losing a wave to it.

Speed is metres per second and does not change with Nightmare. Health and
damage do.

## The roster

| | | | | |
|:--:|:--:|:--:|:--:|:--:|
| <img src="../assets/enemies/goblin.png" width="110" alt="Goblin"> | <img src="../assets/enemies/runner.png" width="110" alt="Runner"> | <img src="../assets/enemies/orc.png" width="110" alt="Orc"> | <img src="../assets/enemies/shieldbearer.png" width="110" alt="Shieldbearer"> | <img src="../assets/enemies/sapper.png" width="110" alt="Sapper"> |
| **Goblin** | **Runner** | **Orc** | **Shieldbearer** | **Sapper** |
| <img src="../assets/enemies/frostbound.png" width="110" alt="Frostbound"> | <img src="../assets/enemies/emberbound.png" width="110" alt="Fire Demon"> | <img src="../assets/enemies/crossbowman.png" width="110" alt="Crossbowman"> | <img src="../assets/enemies/bombardier.png" width="110" alt="Bombardier"> | <img src="../assets/enemies/colossus.png" width="110" alt="Colossus"> |
| **Frostbound** | **Fire Demon** | **Crossbowman** | **Bombardier** | **Colossus** |

The Frostbound and the Fire Demon are the same mesh in two colours. That is
not an accident of the art — it is what the game does, and it matters.

### Runner — 35 HP, 5.6 m/s, 6 damage, 12 mana

The fastest thing in the game. Fragile, and takes **1.25× from pierce** but
only 0.90× from slash. Highly susceptible to control: 1.50× displacement, 1.25×
stagger, 1.20× tar. Springboards and Tar handle runners better than raw damage
does.

### Goblin — 60 HP, 3.4 m/s, 8 damage, 14 mana

The baseline. Takes **1.25× from slash** and 1.10× from fire. No resistances
worth planning around. Wave 1 is goblins so you can learn the controls against
something forgiving.

### Crossbowman — 55 HP, 3.2 m/s, 12 damage, 20 mana

Attacks at range and needs line of sight. Takes **1.25× from slash**, resists
pierce (0.90×). Break the sightline or close the distance — a wall between it
and its target is worth more than another tower.

### Frostbound — 65 HP, 4.8 m/s, 8 damage, 20 mana

Fast, and **immune to chill** — a Frost Rune does nothing to it. Takes
**1.50× from fire**. Fireball and Tar are the answers; the Frost Rune is not.

### Fire Demon — 72 HP, 4.5 m/s, 9 damage, 22 mana

The mirror of the Frostbound: **immune to fire**, and takes **1.50× control
from chill**. A Cannon deals it exactly zero. Chill it, then kill it with the
Warden, a Ballista, or a Wall Maul.

> **Frostbound and Fire Demon are the same mesh.** `enemy.gd` builds both from
> one model and separates them by tint — the Fire Demon takes a 58% shift
> toward ember orange plus an emissive glow, against the Frostbound's 18% cool
> grey. Every other enemy in the game gets 18%; the Fire Demon is tinted three
> times harder precisely so you can tell them apart at speed.
>
> They arrive in the same waves and want opposite answers. Colour is the only
> thing telling you which mistake you are about to make.

### Sapper — 80 HP, 3.8 m/s, 10 damage, 25 mana

**Targets your defenses, not the crystal.** Fast and fragile; takes 1.35× from
pierce and 1.20× from slash, resists crush (0.80×). Left alone it will
dismantle the lane you paid for. Intercept it.

### Unbound — 270 HP, 1.45 m/s, 0 damage, 60 mana

It never attacks. It carries no weapon and deals nothing to you, your defenses
or the crystal, and it walks at a Colossus's pace. It is still the most
dangerous body in the wave, because of what everything standing near it gains.

**It is not fragile.** At 270 HP it carries three times a Sapper's health, and
a trap line will not quietly remove it for you. Reaching it is meant to cost
you something.

Its aura reaches **6 m** — the same radius as your own Commander aura, and for
the same reason: it must not be able to cover two chokes at once.

**Its level rises on its own clock.** Every **6 seconds** it pulses and gains a
stack, whether or not anything is in range and whether or not you are near it.
Its age is the threat, so a caster you ignored for a minute is not the caster
that walked in. Each level keeps every level beneath it:

| Level | What nearby enemies gain |
|---:|---|
| 1 | Immunity to **stagger** |
| 2 | Immunity to **tar** |
| 3 | Immunity to **displacement** |
| 4 | Immunity to **chill** |
| 5 | Regeneration — 1.5% of maximum health per second |
| 6 | **×1.25 damage** |
| 7 | Attack cooldowns **cut by 23%** |
| 8 | **20% less damage taken** |

Stagger goes first on purpose: the clock opens by taking your own instrument
away before the expensive answers are needed. By level 4 every control channel
in the game is switched off inside that circle and your keep is reduced to raw
damage. The reduction at level 8 is deliberately bounded — it can never reach
an effective zero, and it never inverts a counter law.

**It grants all of that and holds none of it.** The Unbound is the most
control-vulnerable body in the roster — **1.60× displacement, 1.50× chill,
1.40× stagger, 1.30× tar** — and takes 1.25× from both slash and pierce. It
also has **no sprint**: it is slow in every direction, fleeing included. If it
wanders into your guns it dies, and that is the intended trade.

Its protection is position, not evasion. It walks at the back of its wave, and
reaching it means going there.

### Shieldbearer — 150 HP, 2.8 m/s, 12 damage, 28 mana

**Frontal pierce deals zero.** Not reduced — zero, at any tower level. Takes
1.15× from crush, and resists displacement (0.65×) and stagger (0.60×). Flank
it, or use crush.

### Bombardier — 210 HP, 2.0 m/s, 30 damage, 45 mana

Slow, heavy, and hits hardest of the regular roster. Takes **1.35× from
pierce**, resists slash (0.70×) and is nearly immovable (0.20× displacement).
Can be interrupted — worth **+5 Ward**.

### Orc — 280 HP, 2.2 m/s, 22 damage, 45 mana

The wall. Takes **1.40× from crush** and 1.15× from fire, but only 0.55× from
slash *and* pierce — so both the sword and the Ballista are working at barely
half rate. **Immune to stagger**, and 0.15× displacement.

Orcs are why a keep needs a Cannon.

### Colossus — 1700 HP, 1.45 m/s, 72 damage, 420 mana

Arrives on wave 5. **Immune to displacement**, heavily resistant to chill
(0.45×), tar (0.35×) and stagger (0.30×). Takes 1.35× from crush. Slow enough
to prepare for and too large to solve by position alone.

The 420 bounty is real: killing it funds the rest of the wave.

## How hard each one hits your buildings

Damage to defenses is a separate role from damage to the crystal, and the
spread is wide. A runner chips; a Sapper dismantles.

| Enemy | Structure damage | Reads as |
|---|---:|---|
| Sapper | **×3.00** | The dedicated demolition counter |
| Colossus | ×2.25 | Breaks what it walks through |
| Orc | ×1.50 | A breaker |
| Bombardier | ×1.20 | |
| Shieldbearer | ×0.75 | |
| Crossbowman | ×0.65 | |
| Frostbound / Fire Demon | ×0.55 | |
| Goblin | ×0.35 | Chips only |
| Runner | ×0.25 | Barely scratches |

Any class can divert to an exposed defense, but only Sappers, orcs and the
Colossus meaningfully destroy one. If a Ballista is dying, look for those three
before blaming the swarm.

The Unbound is absent from this table and the two below it because it never
attacks anything. It cannot damage a defense, and no defense is ever occupied
holding it off.

## How far each one looks

Perception is the radius within which an enemy notices an exposed defense;
detour is how far it will leave its route to reach one. Both vary by class, and
the gap between them is the class's patience.

| Enemy | Perception | Detour |
|---|---:|---:|
| Sapper | 14 m | 14 m |
| Bombardier | 13 m | 9 m |
| Crossbowman | 11 m | 6 m |
| Colossus | 16 m | 12 m |
| Orc | 10 m | 9 m |
| Shieldbearer | 8 m | 6 m |
| Frostbound / Fire Demon | 7 m | 4 m |
| Goblin | 5 m | 5 m |
| Runner | 3.5 m | **1.5 m** |

The Sapper is the only class that will detour as far as it can see — it hunts.
The runner effectively does not: it notices almost nothing and leaves its lane
by a metre and a half, so runners go for the crystal and ignore your towers.

## How many can attack at once

Defenses and the Warden can only be engaged by so many at a time. Runners,
Frostbound, Fire Demons, crossbowmen and bombardiers commit **one** attacker;
orcs, shieldbearers, sappers and the Colossus commit **two**.

## Quick answers

| If you see | Bring |
|---|---|
| Runners | Pierce, Springboard, Tar |
| Orcs | Crush — Cannon, Wall Maul |
| Shieldbearers | Crush, or flank the shield |
| Sappers | Pierce, and intercept personally |
| Crossbowmen | Slash, or break line of sight |
| Frostbound | **Fire** — never chill |
| Fire Demons | **Chill**, then any valid damage — never Cannon |
| Bombardiers | Pierce, and interrupt |
| **Unbound** | **Reach it early** — displacement and chill land hardest on it |
| Colossus | Crush, and everything else you own |

## See also

- [Combat](combat.md) — the channel system and the hard-zero laws
- [Waves](waves.md) — when each of these arrives
- [Defenses](defenses.md) — which defense carries which channel
