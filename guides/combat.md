# Combat

Every enemy in Crystal Keep has an opinion about how it wants to be killed, and
the game does not hide it from you. Damage is not one number applied to one
health bar. It travels through a **channel**, and the channel decides whether
your investment lands, glances, or does nothing at all.

## The four damage channels

| Channel | Sources |
|---|---|
| **Slash** | The Warden's sword, Wall Blades |
| **Pierce** | Ballista, Spikes, Harpoon |
| **Crush** | Cannon, Springboard, Wall Maul |
| **Fire** | Fireball, burning |

Each enemy multiplies incoming damage per channel. An orc takes 1.40× from
crush and 0.55× from slash or pierce — the same ballista bolt that shreds a
runner is doing barely half its printed damage to the thing behind it.

## The four control channels

Control is tracked separately from damage and multiplies the same way.

| Channel | Sources |
|---|---|
| **Chill** | Frost Rune |
| **Tar** | Tar |
| **Displace** | Springboard, Wall Blades, Harpoon |
| **Stagger** | Cannon, Wall Maul |

Control is not damage. A chilled Fire Demon is still a Fire Demon; something
else has to kill it. What control buys is time, and time is what lets a slower,
better-aimed answer arrive.

**All four can be switched off while an Unbound lives.** That caster's stacks
remove them one at a time — stagger, then tar, then displacement, then chill —
for every enemy within 6 m of it. It is the only thing in the game that takes a
channel away from you mid-wave. See [Enemies](enemies.md#unbound--90-hp-145-ms-0-damage-60-mana).

## Hard-zero laws

Some matchups deal **exactly zero**. Not reduced — zero. No item level, no
defense tier, no critical hit, and no amount of rating changes it. These are
the rules the game will not let you buy your way out of, and they are the
reason a build of one defense loses.

| Law | Result |
|---|---|
| Cannon into a **Fire Demon** | 0 — fire immunity |
| Pierce into a **Shieldbearer's front** | 0 — the shield blocks it |
| Pierce into a squadmate **covered** by a Shieldbearer | 0 |
| Chill on a **Frostbound** | 0 control |
| Stagger on an **orc** | 0 control |
| Displace on a **Colossus** | 0 control |

When a hard-zero happens the game tells you plainly: the hit reads
`CANNON IMMUNE — 0` in the enemy's own colour, with its own sound. If you see
that during a wave, the answer is not more of the same defense.

**Every law above is innate. The Unbound makes new ones.** Its control
immunities are granted rather than born, they stack one channel at a time as it
ages, and they end the moment it dies. A zero you cannot fix by rebuilding is
the roster; a zero that appeared this wave and can be undone by reaching one
body is that caster. They read identically on screen, so check whether anything
is tethered before you conclude a channel was the wrong choice.

**Frontal pierce is about facing, not position.** A Ballista behind a
Shieldbearer works perfectly well. The shield only covers the front. Flank it,
or use a channel the shield does not stop.

### The shield in full

Only the Shieldbearer has a facing rule, and it is a **120° frontal cone**
measured from where it is looking — not a 180° wall. A hit from the side is
already a flank.

| Channel, into the front | Multiplier |
|---|---:|
| Pierce | **×0.00** |
| Slash | ×0.40 |
| Crush | ×0.75 |
| **Fire** | **×1.00** |

**Fire ignores the shield completely.** It is the one channel that does not
care which way a Shieldbearer is facing, which makes Fireball and burning the
positional-free answer to a shield wall.

Everything outside the cone takes **×1.25 on every channel** — flanking is not
merely "the shield stops working", it is a 25% damage bonus on top. A flanked
Shieldbearer takes full pierce and a quarter more of it, and the first flank
also pays **+2 Ward**.

That cone is why the Shieldbearer is a *positioning* puzzle rather than a
*channel* puzzle. You can beat it with fire without moving, or with anything at
all by getting behind it.

## Squad auras — the part that punishes a single answer

Three enemies extend their own resistance to everything travelling with them,
within their squad. This is why a lane built around one channel fails against a
mixed packet rather than merely underperforming.

| Aura | Range | Effect on squadmates |
|---|---:|---|
| **Shieldbearer** | 6 m ahead, 3.25 m wide | Pierce into anyone it covers deals **zero** |
| **Fire Demon** | 4 m | Fire damage to squadmates is cut to **20%** |
| **Frostbound** | 4 m | Squadmates **cannot be chilled at all** |

So a Shieldbearer at the head of a column is not one hard target — it is a
moving pierce immunity for everything behind it, and your Ballista line stops
working until the column is flanked or broken.

A Fire Demon does not merely resist your Fireball; it protects the goblins
walking beside it. A Frostbound shuts off your Frost Rune for the whole packet,
not just for itself.

The auras are squad-scoped: an enemy from a different packet standing nearby
gets nothing.

**The Unbound is the exception, and it is why it is dangerous.** Its 6 m circle
covers *every* enemy inside it, whatever packet they arrived with — the only
aura in the game that ignores squad lines. It does not stack with another
Unbound, which take nothing from each other, and the game draws a tether from
the caster to each body it is holding. Those threads are the read: follow them
back and you have found what to kill.

## The enemy roster

Speed is metres per second. Bounty is the mana you are paid for the kill.

| Enemy | HP | Speed | Damage | Bounty | Wants | Refuses |
|---|---:|---:|---:|---:|---|---|
| Runner | 35 | 5.6 | 6 | 12 | pierce, displace | slash |
| Crossbowman | 55 | 3.2 | 12 | 20 | slash | pierce |
| Goblin | 60 | 3.4 | 8 | 14 | slash | — |
| Frostbound | 65 | 4.8 | 8 | 20 | **fire** | chill (immune) |
| Fire Demon | 72 | 4.5 | 9 | 22 | chill, crush | **fire (immune)** |
| Sapper | 80 | 3.8 | 10 | 25 | pierce, slash | crush |
| Unbound | 90 | 1.45 | **0** | 60 | displace, chill, slash, pierce | — |
| Shieldbearer | 150 | 2.8 | 12 | 28 | crush, flanking | frontal pierce |
| Bombardier | 210 | 2.0 | 30 | 45 | pierce | slash, displace |
| Orc | 280 | 2.2 | 22 | 45 | **crush**, fire | slash, pierce, stagger |
| Colossus | 1700 | 1.45 | 72 | 420 | crush | displace, most control |

Two entries deserve reading twice. The **Frostbound** takes 1.50× from fire and
cannot be chilled at all; the **Fire Demon** is the mirror — 1.50× control from
chill, and fire does nothing. They arrive in the same waves. A lane built to
answer one of them is a lane that has surrendered to the other.

## Counterplay pays

Skilled interventions pay you **Ward**, the currency your spells run on:

| Act | Ward |
|---|---:|
| Interrupt a Giant | +8 |
| Interrupt Artillery | +5 |
| **Intercept a Sapper** | **+4** |
| Save a defense with Mend | +3 |
| Flank a Shieldbearer | +2 |
| Colossus last assault | +2 |
| Keeper's Rhythm | +1 |

The loop is deliberate. Support the towers well, earn Ward, cast more support.
Ward is capped and regenerates on its own, so this cannot spiral — you cannot
farm it into an economy.

## The Warden is a multiplier, not a rival

Two of your three spells exist to make the defenses better rather than to
replace them.

- **Hex of Frailty** curses a **4 m** zone for 18 s. Everything that takes
  damage inside it takes **30% more** — including tower fire. It also marks one
  enemy for **6 s**, and towers retarget onto the mark. Hex zones never stack.
- **Mending Ward** heals a defense, grants it **−25% damage taken**, and
  **primes it** — cutting its cooldown, or resetting it entirely if the defense
  is Masterwork.

The keep kills things. You decide where it kills them hardest.

## See also

- [The Warden](warden.md) — your kit, Ward, and the three spells
- [Defenses](defenses.md) — costs, channels, and mounting rules
- [Waves](waves.md) — what arrives, when, and what it announces
