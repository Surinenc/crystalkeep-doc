# Co-op

Two Wardens, one keep, two crystals. Co-op is a **Twin Siege**: a keep that
defends a crystal at each end, a wave that attacks both, and two commanders who
cannot be in the same place.

It is account-free. One of you hosts and reads out a room code; the other types
it in. Nothing is registered, nothing is stored, and the pairing lasts exactly
as long as the siege does.

## Getting in

Co-op is not in the game-modes screen. It has its own main-menu entry:
**CO-OP**. If you are standing on a keep with only one crystal, the game
reloads into a two-crystal one before opening the lobby, so that host and guest
cannot pair from two unrelated maps and discover the mismatch after readying.

That reload lands on the authored **Twin Keep** — flat ground, two crystals
30 m apart. If the host was already standing on a generated
[Split Bastion](keeps.md#the-seven-archetypes), the pair plays that instead,
and it is the better ground: vertical, dressed, and 72 m between crystals.

| Then | |
|---|---|
| **HOST SIEGE** | The relay hands you a room code — three parts, like `EMBER-COURT-47` |
| **COPY JOIN LINK** | Puts a browser link on your clipboard. Opening it joins the room directly |
| **JOIN** | Type a partner's code into the field and join theirs |

The host's keep is the keep. A guest who was standing somewhere else reloads
into the host's ground and rejoins the same room automatically — you will see
`LOADING THE KEEP…` while it happens.

**One of you is the authority.** The host simulates the siege; the guest sends
input and receives the result. This is invisible while the connection holds,
and it decides what happens when it does not — see below.

### Ready means two different things

The **first** time both Wardens are ready, the siege begins: the lobby closes
and you are handed a build phase with nothing built yet. Every both-ready after
that starts the **next wave**. Agreeing to play is not agreeing to fight.

Readiness clears itself after the siege opens, so nobody starts wave 1 merely
by having joined.

If a wave does not start when you both believe you are ready, press ready
again. The message that says so can be lost, and pressing it again re-announces
your state rather than doing nothing.

### The Nightmare dial stops at the lower unlock

Only the host turns it, only during the first build phase, and it stops at the
**lower of the two Wardens' highest unlocked tier**. A veteran cannot drag a
newcomer into content they have not earned, and a newcomer does not hold a
veteran to Standard for any tier the newcomer has already cleared.

## The keep asks for more than twice as much

A two-player wave is expanded to **1.8×** the size of the same wave solo,
rounded up, and its fronts are dealt alternately to the two crystals. You do
not get a lane each and a quiet half — you get close to twice the enemies, split
across two objectives that both have to hold.

Either crystal falling ends the run for both of you. There is no half-loss.

Everything else about waves is unchanged: the same composition, the same
telegraphs, the same [crystal purge](waves.md#the-crystal-ends-a-wave-that-will-not-end)
if a wave cannot finish itself.

## Two purses, one keep

You each hold **your own mana**, and the keep is shared. That combination is
most of the co-op decision-making.

**Income is not split.** Every bounty orb and every wave-clear bonus pays its
**full** amount into **each** purse. Two Wardens are twice the economy, which is
what pays for a wave 1.8× the size.

**You spend from your own.** Building and upgrading draw on the purse of
whoever pressed the button, and the debrief records who invested what.

| Act | Rule |
|---|---|
| **Build** | Anywhere on the keep, from your own purse. The defense is yours |
| **Upgrade** | **Anyone may upgrade anything.** The investor pays; the owner does not change |
| **Repair** | Free, as in solo, and either of you may do it |
| **Sell** | Needs the **owner's consent** if it is not yours |

**Selling refunds everything in co-op.** A sold defense returns **100%** of
what was invested in it — build cost and every upgrade — rather than the 60% a
solo run returns, and it goes to the **owner's** purse rather than the seller's.
Co-op experiments are meant to be fully reversible, because two people
committing to one board will disagree about where the board should be.

A sell request on your partner's defense opens a prompt on their screen for
**5 seconds**. They press **G** to approve. Silence declines it — the request
times out rather than passing by default.

### Handing over mana

Aim at your partner from within **12 m** and hold **T**. Mana moves in
**25-point** parcels every **0.5 s** — 50 per second held — out of your purse
and into theirs. You cannot gift to a Warden who is down.

This is how a co-op board actually gets built: one of you commits to a heavy
tower now, the other funds it and builds cheap next wave.

## When a Warden falls

**Going down in combat costs 15 seconds in co-op**, not the 5 a solo Warden
pays. The run does not end — the crystal is still the only defeat condition —
but a lane held by nobody for fifteen seconds is a real hole.

There are two ways out of it, and they cost different things.

| | How | Cost | Result |
|---|---|---|---|
| **Revive** | Your partner stands within **2 m** and holds **T** for **3 s** | Their time, not their mana | Up at **50% health, full Ward** |
| **Buy-back** | Press **V** yourself while down | **75 mana**, +25 for each previous death | Respawn timer cut to 5 s |

**A revive breaks if the reviver is hit.** Taking any damage during the three
seconds resets the channel to zero and says `REVIVE INTERRUPTED`. Reviving in
the open, mid-wave, with a front still walking, is usually the wrong call —
clear the ground first, or pay the buy-back and keep fighting.

The buy-back price climbs with your own deaths, not your partner's, so the
Warden who keeps dying is the one who pays for it.

## Auras compose, families do not

Both of you carry a [Commander aura](warden.md#the-commander-aura), and a
defense can be bonded to both at once.

**Different families stack.** A tower standing in a Tempo ring and a Precision
ring fires faster *and* crits more. Two Wardens running different relics is
strictly better than two running the same one.

**The same family does not.** If your partner already holds a defense with
Tempo, your Tempo bond on that same defense reads as **held** — it grants
nothing, and the meter does not fill for you there. Stand somewhere else and
bond something they are not already covering. If the earlier commander walks
away, the bond does not transfer: the second Warden earns it from zero, like
anyone else.

The practical rule: **split your relics, and split your ground.** Two Tempo
Wardens standing in the same choke are one Tempo Warden with a spare body.

## Talking without talking

**Ping** with **P** or the **middle mouse button**. The ping reads what you are
aiming at and names itself:

| Aimed at | Reads |
|---|---|
| An enemy | `THREAT` |
| A defense | `REINFORCE` |
| A crystal | `FALL BACK` |
| Anything else | `WATCH LANE`, with the nearest gate's number |

You get **three pings every four seconds**. It is a pointing finger, not a
chat, and the limit is what keeps it readable.

**Salute** with **H**. It does nothing tactical; within 12 m your partner sees
a spark. It is there because a siege that goes well deserves acknowledging.

You also see **your partner's placement ghost** while they are choosing a spot
— the defense, the position, the facing, and whether the game will accept it.
Watching where they are about to build is how you avoid buying the same corner
twice.

## Loot and experience are yours alone

Nothing in co-op is a race for the pickup.

**Drops are instanced.** Each Warden rolls their own loot from the same kill,
and you can neither see nor claim your partner's. There is no ninja-looting to
design around because there is no shared drop.

**Experience is paid in full to both of you.** It is not divided. A co-op kill
advances two Wardens by what it would have advanced one.

## If someone drops out

The relay **holds the room** for a grace window — five minutes by default — and
the disconnected partner can rejoin with the same code.

If it is the **guest** who drops, the host **absorbs their mana** so the purse
is not stranded on an absent Warden: `PARTNER LEFT · n MANA RETURNED`. When
they return they are handed a **rejoin stipend** — 140 mana, plus 60 for each
wave past the first — and a full authoritative restore of the keep: defenses,
crystals, wave and phase, rather than an empty board.

If it is the **host** who drops, the guest waits too, but there is nothing
simulating the siege while they are gone. The host is the authority; a guest
alone in a held room is a paused siege, not a solo one.

## Controls

Everything from the [Warden's control list](warden.md#controls) still applies.
Co-op adds five:

| Input | Action |
|---|---|
| **T** (hold, within 12 m) | Gift mana to your partner, 25 every 0.5 s |
| **T** (hold, within 2 m) | Revive a fallen partner over 3 s |
| **V** | Buy back your own respawn while down |
| **P** / middle mouse | Contextual ping |
| **H** | Salute |
| **G** | Approve a partner's request to sell your defense |

**T** is one key doing three jobs and it resolves them in order: reviving a
fallen partner first, gifting to a standing one second, and the ordinary
landmark or loot interaction last. You cannot accidentally operate a landmark
while standing over your partner's body.

## See also

- [Keeps](keeps.md#the-seven-archetypes) — the two-crystal Split Bastion, and what a twin keep asks
- [The Warden](warden.md#the-commander-aura) — the aura both of you are carrying
- [Economy](economy.md) — bounties and refunds, in their solo form
- [Waves](waves.md) — the wave shape co-op multiplies
