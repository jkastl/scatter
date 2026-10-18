# Changelog

Versions follow [semver](https://semver.org/). See [README.md](README.md#versioning).
Releases before 1.8.0 used two-part versions and are listed as they were shown.

## 1.9.1 · 2026-10-18

### Changed
- Pages now record an anonymous visit count (GoatCounter, no cookies) and carry a canonical
  link and link-preview tags. The README says the count is the only network call.

## 1.9.0 · 2026-09-26

### Added
- Pressing **Enter** (or **Next** on a phone keyboard) in an answer jumps to the next
  category. On the last category it closes the keyboard rather than submitting the
  turn.

## 1.8.0 · 2026-09-26

### Fixed
- Categories are now dealt with a fair shuffle. The old shuffle favored the top of each
  list: the first category showed up about 16% of the time instead of about 6%.
- The same category can no longer appear twice in one round. Removed duplicate
  entries from both lists: Card Games, Things in a Hospital and Things in a Garden,
  plus the near-duplicates Musical Genres (same as Types of Music) and Things on a
  Farm (same as Things at a Farm).
- Ties between three or four players now name every tied player, and all tied players
  get the same rank and medal. The label says "Winners!" when there's a tie.
- Ending a game before any round is scored goes back to the menu, instead of an
  all-zero "tie" screen.
- Answers match regardless of surrounding quotes or punctuation, so `"Jaws"` is no
  longer flagged as the wrong letter or missed as a duplicate of `jaws`.
- The How to Play text for the stop button now matches what it does: it shows the
  final scores.

### Changed
- Letters don't repeat within a game.
- Pinch-to-zoom is allowed again.
- The version label uses semver: `v1.8.0 · 2026-09-26`.

### Internal
- Removed unused code: the `COLORS` constant, `resetToSetup()`, `beginPlayerTurns()`
  and unused CSS classes.
- Pause, resume and the turn timer share one countdown function.
- All game state is declared up front, player name labels are linked to their inputs,
  and the page has a meta description.
- Added README and CHANGELOG, and updated the version rule in CLAUDE.md.

## 1.7 · 2026-04-03

- Hid the **End Game Early** button on the scoreboard after the last round.
- Added the date to the version label.

## 1.6 · 2026-04-02

- Added a player color picker to setup.

## 1.5 · 2026-04-02

- Added the version number to the home screen.
