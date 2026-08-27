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

### Endless pays out every fifth wave

From **wave 10**, every fifth wave secured (10, 15, 20, 25…) grants a
**guaranteed item** — rolled against your current pressure — plus **30 + 4 per
wave** in gold. Wave 10 pays 70, wave 15 pays 90, and so on.

That cadence gives a losing run a target. Reaching wave 10 banks something
real; dying on wave 14 banks nothing beyond what wave 10 already paid.

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

**The schedule is fixed:**

- Nothing before **wave 8**. The first eight waves are contract-free.
- Contracts run in **blocks of four waves** — 8–11, 12–15, 16–19, and so on —
  and are previewed during the build phase of the wave before a block starts.
- **One contract at a time until wave 16**, then **two** for the rest of the
  run.
- Consecutive blocks never draw the identical set, so a contract cannot silently
  persist across a block boundary by chance.
- **Searing Host and Rime Host can never be active together.** The two mirrors
  are mutually exclusive by rule, not by luck.

**Contracts pay you for taking them.** Each active contract adds **12%** to the
reward premium on Endless milestone rewards — so a single contract is +12% and
the two-contract era from wave 16 is **+24%** on the item level you roll
against. The difficulty and the payout rise together, which is why the deep
game is worth playing rather than merely survivable.

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

## Siege Doctrines

Both Keep Assault and Endless offer **Siege Doctrines** — a choice of three
after clearing wave 2, and another after wave 4. They are run-long and free,
and each one is worth roughly a 200-mana upgrade.

Endless does **not** keep offering them as it goes: a wave-40 Endless run has
exactly the same two doctrines a five-wave campaign gets. See
[Siege Doctrines](doctrines.md).

## What persists

Two different axes, easy to conflate:

| | Keep Assault | Endless Siege | Weekly Keep |
|---|---|---|---|
| Persistent power (gear) | Yes | Yes | **No — normalized** |
| **Uses** your Nightmare tier | Yes, fixed | **Yes**, plus depth | **No — forced to 0** |
| **Unlocks** the next tier | Yes | No | No |
| Ends at wave 5 | Yes | No | Yes |
| Siege Doctrines | Yes (waves 2, 4) | Yes (waves 2, 4) | Yes (waves 2, 4) |
| Siege Contracts | No | **Yes, from wave 8** | No |

Unlocking a tier and using a tier are unrelated. Endless never raises your
ceiling but spawns and drops against it; Weekly leaves your ceiling untouched
and ignores it entirely.

## See also

- [Nightmare](nightmare.md) — the ladder Keep Assault unlocks
- [Waves](waves.md) — the five-wave shape
- [Progression](progression.md) — the power that Weekly normalizes away
