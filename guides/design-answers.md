# Design answers

This genre has a long record, and most of its games fail in the same handful of
ways. Those failures are well documented by the people who played them — in
reviews, in forum threads that ran for years, in postmortems written by the
studios themselves.

This page lists the recurring ones and the mechanism in Crystal Keep that
answers each. No game is named; the point is the failure, not the culprit.
Where we are only partly covered, it says so — a page like this is worth
nothing if it only lists wins.

Every answer below is a system that ships. Nothing here is a plan.

## Generated ground that feels arbitrary

**The pitfall.** Procedural maps that read as noise. A layout the generator
found but nobody checked, where losing feels like the seed's fault rather than
yours, and the player learns nothing from the loss.

**The answer.** Every generated keep is validated against a **versioned
fairness contract** before it is offered, and a keep that fails any rule is
discarded and another seed tried. You never see the rejects. The contract is at
**version 6**, and it is data rather than sentiment. The rules that shape what
you meet:

| | |
|---|---|
| Fastest enemy needs **at least 8 s** from any gate to the crystal | You always get time to react |
| Slowest arrives **within 45 s** | No lane is a marathon that never threatens |
| Lane times differ by **at most 5 s** | Fronts arrive together; splitting attention is possible |
| Every lane narrows to **at most 8.5 m** somewhere | Every lane can be answered with position |
| No choke narrower than **2.6 m** | Nothing wedges; the geometry cannot trap a wave |
| Sealing **every** lane costs **at most 540 mana** | Turtling is always affordable |
| The crystal keeps **3.5 m** of clear ground | There is room to make a last stand |

Because the rules are numbered and versioned, a change to them is a visible
event rather than a silent retune. See
[the fairness contract](keeps.md#the-fairness-contract).

## Maps you cannot funnel, or that funnel themselves

**The pitfall.** Two opposite failures with the same cause — nobody checked.
Boards so open that no defense placement matters, and boards with exactly one
solved corridor that every player finds in a week.

**The answer.** The contract enforces both ends. Every lane must narrow
somewhere (so position always matters) **and** never pinch below an orc's
width plus margin (so the ground never solves itself by accident). Sealing
every lane is guaranteed affordable, which keeps the turtle a real option
rather than a fantasy — and **blocking is your verb, not the generator's**. The
keep offers chokes; you decide which ones become walls.

Seven archetypes, four widths from 126 m to 180 m, and a landmark catalogue of
twenty-four keep the shapes from converging. See [Keeps](keeps.md).

## Gear that eventually eats the game

**The pitfall.** The most reliable way this genre dies. Loot inflates, numbers
climb, and eventually the towers are decoration around a hero who deletes the
wave. The tower game becomes optional in a tower game.

**The answer.** Two rules, and the second is the one that matters.

**Ratings are compressed, not inflated.** Every rating passes through a
logarithmic curve before it becomes a multiplier. A **thousandfold** increase in
rating buys roughly **four times** the power. Growth never stops, and it never
runs away.

**Some matchups are exactly zero, and no item changes that.** A Ballista deals
nothing through a Shieldbearer's front. A Cannon deals nothing to a Fire Demon.
No item level, rarity, rating or critical hit buys past a hard zero. This is
what makes the ladder equipment-proof: the answer to a wave is always a
decision, never a bigger number. See [Combat](combat.md) and
[Progression](progression.md#ratings-are-compressed-not-inflated).

## The hero who replaces the keep

**The pitfall.** The hybrid's own disease. Give a player a body in the fight
and a stat line, and personal damage quietly becomes the correct strategy —
until the defenses are scenery.

**The answer.** The Warden's power is channelled **into** the defenses rather
than competing with them.

There is **no weapon-damage stat**. The sword scales on **Defense Power** — the
same rating that arms your towers — and is deliberately pegged at roughly the
worth of one mid-tier tower. You cannot specialise into being the keep.

The [Commander aura](warden.md#the-commander-aura) is the structural half: a
6 m ring that bonds nearby defenses to you and makes them measurably better
while you hold that ground. It is smaller than a Ballista's reach on purpose —
you can hold one choke cluster, not two. **Positioning is the hero skill**, and
the strongest thing you can do for a lane is stand in it.

The aura is visible by contract: a ring on the ground, a light pillar on every
bonded defense. A hidden multiplier would make positioning unlearnable.

## Waves that stall and sour their own ending

**The pitfall.** One enemy stuck on unreachable ground, and a won fight becomes
several minutes of hunting for it. Every game in this genre has a thread about
it.

**The answer.** Each combat phase carries a **120-second** countdown that runs
while enemies are alive or queued. It warns at 60, 30 and 10 seconds, and at
zero the crystal annihilates everything on the field. No wave can soft-lock a
night, whatever the cause.

It is **exploit-proof by construction**: an enemy killed by the purge pays no
experience, no bounty, no loot and no kill credit. Waiting out the clock is
never a strategy, so the failsafe can be generous without becoming a tactic.
See [the crystal purge](waves.md#the-crystal-ends-a-wave-that-will-not-end).

## Difficulty that invalidates the build you just paid for

**The pitfall.** A wave arrives with a resistance nobody mentioned, the plan
you spent your economy on is now worthless, and the game calls that difficulty.

**The answer.** **Every wave event announces its own counter before it
arrives** — `ARMORED COLUMN → CRUSH / BRITTLE`, `FROSTBOUND FRONT → FIRE /
TAR`. In Endless, Siege Contracts are previewed during the build phase of the
wave *before* the block they affect, and each one ships with its stated answer
alongside its effect.

Adaptation is meant to be a conversation. You are told what is coming and given
an untimed build phase to answer it; ignoring the telegraph is a choice you
made. See [Waves](waves.md#wave-events-announce-their-own-counter).

## Build phases on a timer

**The pitfall.** A countdown during the only part of the game that is about
thinking, which converts planning into panic and punishes the player who wants
to read the board.

**The answer.** **The build phase is untimed and you start the wave yourself**,
with **G**. The game never starts one for you, and unspent build time is time
you chose not to use.

The single exception is opt-in and named: the **Short Muster** siege contract in
Endless ends the build after 45 seconds of active planning. It is previewed
before the block it applies to, like every other contract.

## Co-op economies that start arguments

**The pitfall.** Shared build budgets that turn into fights over who spends;
contested pickups that turn allies into racers; last-hit rewards that make
kill-stealing correct play.

**The answer.** Every one of those has a specific counter in
[co-op](co-op.md#two-purses-one-keep):

- **Separate purses, undivided income.** Every bounty and wave bonus pays its
  **full** amount into **each** Warden's wallet. There is no pool to argue over
  and no cut to collect.
- **Loot is instanced.** Each Warden rolls their own drop from the same kill
  and cannot see or take the other's. There is no pickup race to design around.
- **Experience is not divided.** A co-op kill advances two Wardens by what it
  would have advanced one.
- **Gifting is first-class.** Aim at your partner inside 12 m, hold **T**, and
  mana moves at 25 per half-second. Funding the other player is a designed verb,
  not an etiquette convention.

## Co-op griefing, and the trust that prevents it

**The pitfall.** Anyone can sell anyone's work, so a bad actor can dismantle a
defense mid-wave. Permission systems get bolted on, and they never quite fit.

**The answer.** **Anyone may build and upgrade anything** — collaboration
should not need permission — but **selling another Warden's defense requires
their consent**, offered as a 5-second prompt that declines on silence rather
than passing by default.

Underneath that sits the real safeguard: **in co-op a sold defense refunds
100%** of everything invested, to the owner's purse. Reversibility, not
permission, is what makes two people editing one board safe. A disagreement
costs a conversation, never an economy.

## Co-op that scales the wrong number

**The pitfall.** A second player who makes the game easier, or a second player
answered with an HP multiplier so the same fight takes twice as long. Both mean
the game was balanced for exactly one player count.

**The answer.** A two-player wave carries **1.8× the force**, pressed against
**both crystals at once**. No enemy gains a point of health for your partner
being there. More bodies means more simultaneous fronts — a second commander is
answered with a second problem, not a longer one.

The keep itself is the two-player map: a twin-crystal keep where either crystal
falling ends the run, so the stake is genuinely shared.

## Sessions destroyed by a disconnect

**The pitfall.** A long run voided because someone's connection dropped, with
no rejoin and no recovery — the complaint that outlived several sequels.

**The answer.** The room is **held for a grace window** — five minutes by
default — and the missing Warden rejoins with the same code, receiving a full
authoritative restore of the keep rather than an empty board. While they are
gone their mana is returned to the purse rather than stranded, and on return
they are handed a stipend rather than nothing.

## Where we are not covered

An honest list is worth more than a complete one.

**Meta narrowing.** Ten defenses, hard zeros in both directions, and per-keep
choke variety make one dominant answer structurally hard. They do not make it
impossible, and communities find the single best answer faster than designers
do. This is watched, not solved.

**Depth of pressure.** Waves are budgeted to push past the first choke, and
drops let a wave commit downward into the keep. Whether pressure reliably
reaches past that first choke on a winning night is a question for measurement,
not assertion.

**Split-screen.** Ruled out rather than promised. The genre's most-loved
co-op feature is also its most-broken promise, and a promise we cannot keep is
worse than one we never made.

## See also

- [Keeps](keeps.md) — the contract in full, and the ground it produces
- [Combat](combat.md) — the hard-zero laws the whole ladder rests on
- [Progression](progression.md) — the curve that stops gear eating the puzzle
- [Co-op](co-op.md) — the two-Warden siege
