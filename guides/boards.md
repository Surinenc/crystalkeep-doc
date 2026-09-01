# Boards

**LEADERBOARD** on the main menu opens five boards. You are already on them —
there is nothing to sign up for, no name to enter, and no account.

## Who you are on a board

Your save carries an opaque identifier, minted once and kept. Your **display
name is derived from that identifier**, never chosen and never stored: two
words from a 64-word vocabulary and a number, so `WYRM YEW 18` or
`GALLERY TEMPEST 43`. The same id always produces the same name, on your
machine and on the server, with no lookup between them.

That is a design decision rather than a missing feature. Because no
player-supplied text ever reaches a public board, there is nothing to moderate,
no profanity filter to write, and no way to impersonate anybody. A server can
render any row without ever storing a name.

Wherever your row lands, it reads **`MY RANK`**.

The identifier names a save and nothing else. It is deliberately not the id
your local telemetry uses — that stream stays local and was never meant to
become a public handle.

## The five boards

| Board | What it ranks |
|---|---|
| **HALL OF KEEPS** | The keeps themselves |
| **THE WEEKLY** | This week's pinned keep |
| **ENDLESS** | How deep, and at what Nightmare tier |
| **WARDENS** | Lifetime totals |
| **YOUR RECORD** | You, against yourself |

Every board except the last carries a **GLOBAL / ME** toggle — the same
board, filtered to everyone or to you. `YOUR RECORD` is personal by definition
and has no global form.

## The Hall of Keeps ranks the ground, not the players

In a game where the map is generated, the map is the antagonist. This board
puts the keeps in order and reports how often each one wins.

Two things keep it honest. **Only concluded runs count** toward a keep's
ratio — a walk-away is reported separately, because leaving is not the keep
beating you. And the number of distinct wardens who have fought a keep is
printed alongside its percentage, so a keep that one person has attempted once
says so instead of posing as a ranking.

It was also the first board built, because it needs no identity, no trust and
no crowd: it is interesting with three players, where a board of people is a
blank page until there are many.

## The Weekly, and the streak

The Weekly board ranks by score and then **refuses to show it**. `187,340` is
not a number you can reason about; `CLEARED · 5/5 waves · 197 crystal · 4m 12s`
tells you exactly how you were beaten and what to do about it. See
[Game modes](game-modes.md#weekly-keep) for what the score actually weighs.

**Weeks you lost stay on the board.** The Weekly exists to be shown up on, and
hiding the failures would let a streak look unbroken when it is not.

A **streak** is consecutive weeks played. The current week not being played
yet does not break it — the week is not over. A missing week behind you does.

## Lifetime totals

The Wardens board reads a running record your profile keeps:

- Sieges played, won, lost and **abandoned**, counted apart from each other —
  a walk-away still counts as played, and is not filed as a loss
- Defenses placed
- Enemies defeated
- Damage dealt

These accumulate during a run and are written **once**, when it ends in
victory, defeat or abandonment. A save from before the boards existed starts
these at zero rather than guessing backwards.

## When the network is not there

The boards are not a reason to be online. GLOBAL reports itself as
**unavailable** rather than emptying every board, ME keeps working, and a score
you earned offline is submitted later — a result survives the process closing,
the service being down, and a run played with no connection at all.

## See also

- [Game modes](game-modes.md) — the Weekly, Endless, and what a score weighs
- [Nightmare](nightmare.md) — the ladder the Endless board reports
- [Progression](progression.md) — the level and item level a Wardens row shows
