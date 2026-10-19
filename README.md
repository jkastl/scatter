# Scatter!

A pass-the-phone category game for 2–4 players. Each round rolls a letter, and everyone
races the clock to name something in 10 categories that starts with it.

**[jkastl.github.io/scatter](https://jkastl.github.io/scatter/)**

One file, no build step, no dependencies, no backend. The page loads an anonymous
[GoatCounter](https://www.goatcounter.com/) visit counter (no cookies) and works without it. The whole game is
[`index.html`](index.html), served by GitHub Pages from `main`.

## How a game works

1. **Setup:** pick Standard or Kids categories, 2–4 players (each with a name and
   color), 1–5 rounds and a 1–5 minute timer.
2. **Roll:** each round shows a letter and deals 10 random categories. Letters don't
   repeat within a game.
3. **Turns:** players take turns one at a time in secret, then pass the phone. **⏸**
   hides the answers and stops the clock. **■** ends the game. **Enter** (or **Next**
   on a phone keyboard) jumps to the next category.
4. **Scoring:** everyone reviews all the answers together. Answers are pre-approved
   automatically, and tapping one toggles it.
   - **Duplicate:** two players gave the same answer in a category. Neither scores.
   - **Repeat:** one player used the same answer in two categories. Only the first
     use scores.
   - **Wrong letter:** the answer doesn't start with the round's letter. It's off by
     default, and tapping it overrides that.

   Matching ignores capitals, extra spaces and surrounding punctuation, so `"Jaws"` and
   `jaws` count as the same answer.
5. **Winning:** the most points after the last round wins. Tied players share the win
   and the medal.

Ending a game early shows the final scores. If no round has been scored yet, it goes
back to the menu instead.

## Categories

The two lists, `CATS_STANDARD` and `CATS_KIDS`, are near the top of the `<script>`.
Each round draws 10 different categories at random from the active list. To add a
category, put it in the fitting group. Duplicates are ignored, but keep the list clean.

## Working on it

- **Keep it simple.** The game is deliberately one file, with no package manager, build
  step, tests, linters or CI. Don't add any of that without a good reason.
- **Keep it public-safe.** This is a public repo, so no API keys, credentials, personal
  data or internal URLs in any file or commit.
- **Commit straight to `main`.** No feature branches or pull requests unless there's a
  reason for one. Pages deploys from `main`.

## Versioning

The version and date on the home screen (the `.version-label` div in `index.html`) are
**updated by hand**. Nothing bumps them automatically. Change both in the same commit
as the change they describe, add an entry to [`CHANGELOG.md`](CHANGELOG.md), and follow
[semver](https://semver.org/):

- **Patch** (`1.8.0` → `1.8.1`): bug fixes and wording tweaks.
- **Minor** (`1.8.0` → `1.9.0`): new features, categories or rule changes.
- **Major** (`1.8.0` → `2.0.0`): a redesign, or a change to how a game fundamentally
  plays.

The date is the day of the change, in `YYYY-MM-DD` format.
