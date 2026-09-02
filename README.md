# Going to the Farm 2026 (Year 5)

Trip reference for eight men at Big Cedar Lodge, Ridgedale MO, October 1–4 2026.

**Live site:** https://4schmidtyonline-ux.github.io/TheFarmCup2026/

`index.html` is the whole site. No build step, no dependencies, nothing to install.
Fonts load from Google Fonts; everything else is inline.

## Updating it

Edit `index.html` in the repo (pencil icon), commit to `main`. Pages redeploys in
about a minute. Hard-refresh your phone if you still see the old version.

## Pages settings

Settings → Pages → Source: **Deploy from a branch**, Branch: **main**, folder: **/ (root)**.
If a deployment gets stuck or fails with a 500, that is GitHub's side, not the repo.
Push any trivial commit to enqueue a fresh run, or switch Source to **GitHub Actions**,
which uses a different deployment path.

## Note on visibility

A GitHub Pages site is public to the internet on Free and Pro plans, even when the
repository itself is private. Private Pages needs GitHub Enterprise Cloud.

Scrubbed for public hosting: no full names (nicknames only), no personal mobile
numbers, no lodging reservation number. What remains is nicknames, handicaps, the
schedule, and Big Cedar's own published business numbers.
