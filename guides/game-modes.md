# Game modes

Three modes, reached with **M**. They differ in what carries over, what ends
the run, and whether your accumulated power comes with you.

## Keep Assault

> Five waves. One keep. Win or lose.

The progression campaign. Clear all five waves at your selected Nightmare tier
to unlock the next. Your persistent power applies, and this is the only mode
that unlocks Nightmare tiers.

This is the default run and the one everything else is balanced against.

## Endless Siege

> Build until the keep breaks.

The siege continues past wave five. Monster level, composition and pressure
rise indefinitely, and your deepest secured wave is recorded.

**Endless does use your selected Nightmare tier.** It is the starting pressure,
and depth is added on top of it:

```
pressure = nightmare + max(0, wave - 4)
```

The authored arc owns waves 1–5, so every wave you secure beyond the fourth
advances one further pressure level. Starting Endless at Nightmare 20 and
reaching wave 30 puts you at pressure 46 — and pressure is what sets monster
level, which sets the item-level band you are rolling against.

Starting from Standard is legitimate: with Nightmare at 0 the pressure still
climbs one level per wave, so depth alone carries the run.

What Endless does **not** do is unlock the next Nightmare tier. Only Keep
Assault does that. Persistent power applies as normal.

Endless is also where **Siege Contracts** appear.

## Weekly Keep

> One pinned keep. Equal power. Seven days.

A deterministic weekly map with **normalized** Warden and defense ratings —
persistent power does not apply. Everyone plays the same keep at the same
power, and your best local score is kept for the week.

**Weekly forces Nightmare to 0** regardless of the tier you have unlocked. Both
your gear and the difficulty are pinned, because a Weekly is one shared
challenge rather than a family of incomparable ladders. A score set at tier 40
would not be comparable with one set at tier 4, so neither is allowed.

The seed derives from the week itself, so the rotation runs without anyone
having to turn a handle. A missed week is not possible.

## Siege Contracts

Endless Siege draws seeded contracts that change how a wave has to be answered.
They are **previewed before the wave they affect** — planning problems, not
hidden inflation.

| Contract | Effect | Its stated answer |
|---|---|---|
| Withered Grace | Warden healing received −50% | Intervene safely; preserve health before the assault |
| Grinding Gears | Tower and trap attack/reset intervals +30% | Add coverage; favour control, area damage, or consolidation |
| Iron Levy | Field repairs cost 50% of the defense's base construction mana | Prevent damage, repair selectively, or sell and rebuild |
| Specialist Rush | Specialists move and acquire defense targets 20% faster | Control early; intercept or focus specialist coverage |
| Searing Host | Fire enemies more common, and they resist 30% of control strength | Frost setup, Pierce, wall control, or Warden focus |
| Rime Host | Frost enemies more common, and they resist 30% of control strength | Fire, Crush, displacement, or Warden focus |
| Spent Mechanisms | Every compatible landmark has one fewer usable charge | Save charges, or cover the keep's static routes |
| Short Muster | The build phase ends after 45 seconds of active planning | Prioritise the threatened lane; bank rather than rebuild |

Every contract ships with its own answer, and the game shows it to you
alongside the effect. This is the same principle as the wave telegraphs: you
are told what is coming and what beats it, and the decision left to you is what
to do about it.

Two of them are worth reading twice. **Searing Host** and **Rime Host** are
mirrors — one floods the lane with fire enemies, the other with frost — and
both cut control strength by 30%. A build that leans on a single control
channel meets one of these eventually.

**Specialists** are the six roles that make a lane collapse rather than bleed:
Shieldbearer, Sapper, Frostbound, Fire Demon, Crossbowman and Bombardier.
Specialist Rush makes all of them faster, including how quickly Sappers find
your defenses.

## What persists

Two different axes, easy to conflate:

| | Keep Assault | Endless Siege | Weekly Keep |
|---|---|---|---|
| Persistent power (gear) | Yes | Yes | **No — normalized** |
| **Uses** your Nightmare tier | Yes, fixed | **Yes**, plus depth | **No — forced to 0** |
| **Unlocks** the next tier | Yes | No | No |
| Ends at wave 5 | Yes | No | Yes |

Unlocking a tier and using a tier are unrelated. Endless never raises your
ceiling but spawns and drops against it; Weekly leaves your ceiling untouched
and ignores it entirely.

## See also

- [Nightmare](nightmare.md) — the ladder Keep Assault unlocks
- [Waves](waves.md) — the five-wave shape
- [Progression](progression.md) — the power that Weekly normalizes away
