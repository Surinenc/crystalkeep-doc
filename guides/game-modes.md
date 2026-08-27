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
rise indefinitely, and your deepest secured wave is recorded. Persistent power
applies; Nightmare tiers do not unlock here.

Endless is also where **Siege Contracts** appear.

## Weekly Keep

> One pinned keep. Equal power. Seven days.

A deterministic weekly map with **normalized** Warden and defense ratings —
persistent power does not apply. Everyone plays the same keep at the same
power, and your best local score is kept for the week.

The seed derives from the week itself, so the rotation runs without anyone
having to turn a handle. A missed week is not possible.

## Siege Contracts

Endless Siege draws seeded contracts that change how a wave has to be answered.
They are **previewed before the wave they affect** — planning problems, not
hidden inflation.

| Contract | Effect |
|---|---|
| Withered Grace | Warden healing received −50% |
| Grinding Gears | Tower and trap reset intervals +30% |
| Iron Levy | See in-game preview |
| Specialist Rush | See in-game preview |
| Searing Host | See in-game preview |
| Rime Host | See in-game preview |
| Spent Mechanisms | See in-game preview |
| Short Muster | See in-game preview |

<!-- TODO: verify — fill remaining contract effects from siege_contracts.gd -->

Each contract carries a stated **response** alongside its effect. Withered
Grace tells you to intervene safely and preserve health before the assault;
Grinding Gears tells you to add coverage and favour control, area damage, or
consolidation. The game is telling you how to answer it.

## What persists

| | Keep Assault | Endless Siege | Weekly Keep |
|---|---|---|---|
| Persistent power | Yes | Yes | **No** |
| Unlocks Nightmare | Yes | No | No |
| Ends at wave 5 | Yes | No | Yes |

## See also

- [Nightmare](nightmare.md) — the ladder Keep Assault unlocks
- [Waves](waves.md) — the five-wave shape
- [Progression](progression.md) — the power that Weekly normalizes away
