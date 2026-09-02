# Going to the Farm 2026 (Year 5)

**https://farmcup2026.github.io**

Trip reference for eight men at Big Cedar Lodge, Ridgedale MO, October 1–4 2026.

## The two files

| File | What it is | How often it changes |
|---|---|---|
| `index.html` | The whole app. Schedule, courses, matches, money, resort info. | Rarely, and never during the trip |
| `results.json` | Live scores. Cup standings, skins payouts, a one-line headline. | After each round |

No build step, no dependencies. Fonts come from Google Fonts; everything else is inline.

## During the trip — the only thing you do

1. Send Claude a photo of the scorecard plus each player's course handicap.
2. Claude sends back a finished block of text.
3. Open this link on your phone:
   **https://github.com/FarmCup2026/FarmCup2026.github.io/edit/main/results.json**
4. Select all, paste, **Commit changes**.

The site updates in about a minute. You never type JSON yourself — Claude hands you
the entire file, valid, every time. If you fumble it, paste `{}` and the live
sections simply disappear; nothing else on the site breaks.

## How results.json behaves

- Missing, empty, or malformed: the page renders exactly as it does with no file at all.
- A match named in `matches` overrides whatever anyone tapped on their own phone.
- A match *not* named still shows each viewer's own tap, so the buttons stay useful.

Valid match ids are `s1a s1b s2a s2b s3a s3b s4 f1 f2 f3 s5a s5b s5c s5d`.
Valid values are `Cleveland`, `World`, `Halved`. Anything else is ignored.

## Updating the app itself

Edit `index.html` in the repo (pencil icon), or **Add file → Upload files** and drop
in a new copy. Commit to `main`. Pages redeploys in about a minute.

Hard-refresh your phone afterward or you'll keep seeing the cached version.
`results.json` is fetched with a cache-buster, so it always comes back fresh.

## Pages settings

Settings → Pages → Source: **GitHub Actions**. If a deployment fails with a 500,
that's GitHub's side, not the repo — push any trivial commit to enqueue a fresh run.

## Visibility

A GitHub Pages site is public on Free and Pro plans, even from a private repo.
Private Pages needs Enterprise Cloud.

Scrubbed for public hosting: nicknames only, no full names, no personal mobile
numbers, no lodging reservation number. What remains is nicknames, handicaps, the
schedule, and Big Cedar's own published business numbers.
