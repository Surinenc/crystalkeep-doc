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

## Hard-zero laws

Some matchups deal **exactly zero**. Not reduced — zero. No item level, no
defense tier, no critical hit, and no amount of rating changes it. These are
the rules the game will not let you buy your way out of, and they are the
reason a build of one defense loses.

| Law | Result |
|---|---|
| Cannon into a **Fire Demon** | 0 — fire immunity |
| Pierce into a **Shieldbearer's front** | 0 — the shield blocks it |
| Pierce into any **covered** target | 0 |
| Chill on a **Frostbound** | 0 control |
| Stagger on an **orc** | 0 control |
| Displace on a **Colossus** | 0 control |

When a hard-zero happens the game tells you plainly: the hit reads
`CANNON IMMUNE — 0` in the enemy's own colour, with its own sound. If you see
that during a wave, the answer is not more of the same defense.

**Frontal pierce is about facing, not position.** A Ballista behind a
Shieldbearer works perfectly well. The shield only covers the front. Flank it,
or use a channel the shield does not stop.

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
| Save a defense with Mend | +3 |
| Flank a Shieldbearer | +2 |
| Colossus last assault | +2 |

The loop is deliberate. Support the towers well, earn Ward, cast more support.
Ward is capped and regenerates on its own, so this cannot spiral — you cannot
farm it into an economy.

## The Warden is a multiplier, not a rival

Two of your three spells exist to make the defenses better rather than to
replace them.

- **Hex of Frailty** marks a zone. Everything that takes damage inside it takes
  **30% more** — including tower fire. It also marks a priority target, and
  towers retarget onto it.
- **Mending Ward** heals a defense and grants it **−25% damage taken** while
  active.

The keep kills things. You decide where it kills them hardest.

## See also

- [The Warden](warden.md) — your kit, Ward, and the three spells
- [Defenses](defenses.md) — costs, channels, and mounting rules
- [Waves](waves.md) — what arrives, when, and what it announces
