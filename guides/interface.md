# Interface

Crystal Keep draws most of its interface directly rather than using stock
widgets, which is why it looks engraved rather than assembled. What follows is
what each surface is for.

## During a run

**Route ribbons** lie on the ground during the build phase, tracing the paths
enemies will walk. You are shown **every gate the coming wave uses**, not only
the one its first front arrives through, and on a two-crystal keep each ribbon
runs to the crystal that front actually attacks. When you place a Blockade the
ribbons update — that is the fastest way to confirm a reroute worked before you
commit the rest of your purse.

Once combat starts the ribbons narrow to the front that is spawning now, so
what lies on the ground mid-fight is the live lane rather than the whole wave.

**The crystal meter** shows the objective's remaining health — the only number
that ends the run. A Split Bastion shows two, one for each crystal, and either
one reaching zero ends it.

**The wave strip** names what is coming next and how many lanes it arrives on.

**Nameplates** appear on defenses you aim at: tier, health, and contribution.

**Floating numbers** carry the outcome of every hit. Size is the hierarchy, not
colour — an ordinary hit is smaller than a critical, and a hit that was soaked
by armour is smaller still and muted, so weak hits recede on their own. A
hard-zero reads explicitly: `CANNON IMMUNE — 0`.

## The build wheel

**B** or **middle mouse** opens the wheel. Flick toward a segment and release.

Aiming at a **placed defense** when you open it changes the wheel into a
three-option context menu: **upgrade**, **sell**, or select that defense type
for building.

Placement is two steps: lock the location, then aim the facing. The range and
dead-zone preview rotate with you, before any mana is committed.

## The tactical map

**Tab** shows the whole keep at once — routes, gates, defenses, landmarks,
**drops** drawn as an arrow from the lip enemies leave to the ground they land
on, and which fronts attack next. Its header carries the wave, the phase, and
your Nightmare tier as `· N12` whenever you are above Standard. It stays live:
combat continues while it is open.

It also tracks the loot lying on the field — `LOOT ON FIELD · n CLAIMED /
m REMAIN` — because items are never picked up automatically and it is easy to
finish a wave without noticing what you left behind.

**The bracket keys `[` and `]` cycle the loot filter**, and they only work
**while the map is open**. Three settings:

| Filter | Shows |
|---|---|
| **ALL** | Every drop on the field |
| **RARE+** | Rare and better only |
| **SET / UNIQUE** | Only set pieces and uniques |

This is a display filter for the map markers — it hides clutter so you can find
the one drop worth crossing the keep for. It does not affect what drops, and
nothing filtered out is lost any faster.

## The Warden Ledger

**I** opens the ledger, which carries inventory and equipment, Warden
progression, and the Nightmare ladder. Items show their real stat lines with an
equipped comparison — gains, tradeoffs, and explicitly which stats you would
lose.

The ledger is also where you set your **loot preference**, which biases what
your items roll. See [Progression](progression.md#loot-is-claimed-never-collected).

`Options → Accessibility → Item details` switches between Concise and Full.
Concise is the default decision surface; Full adds rolls and provenance for
when you want the arithmetic.

## The Workshop

**K**. See [Workshop](workshop.md).

## Game modes

**M**. See [Game modes](game-modes.md).

## The wave debrief

After each wave, per-defense evidence: damage, kills, control, blocked hits,
absorption, DPS, and damage per mana. This is the record that answers whether a
placement earned its cost.

**F4** recalls the latest debrief during the build phase.

## Options

Audio, controls, accessibility and video. Two worth knowing:

- **Streamer-safe audio** mutes the licensed soundtrack while leaving ambience
  and effects alone.
- **Build wheel** can be switched from Hold to Toggle, which removes the
  sustained middle-mouse press and pauses fully while open.

## Language

English, Spanish and Catalan. Selectable in Options.

## See also

- [Getting started](getting-started.md) — the loop these surfaces serve
- [The Warden](warden.md) — the full control list
