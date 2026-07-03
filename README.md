# Mario Kart World — Stats Calculator

A fast, dependency‑free stats calculator for **Mario Kart World**, in the spirit of the
MK8DX build calculators. Everything is a single static `index.html` — no build step, no
frameworks, no external requests. It opens instantly and runs with zero lag.

## Features

1. **Builder** — pick a character and a vehicle, see the combined stats as bars + numbers.
2. **Pareto frontier** — choose any two stats (e.g. Speed vs Acceleration) and instantly
   see the builds where you can't improve one without sacrificing the other. Great for
   "what's the best mini‑turbo I can get at this speed?".
3. **Combo finder** — pick a base build, mark which stats must be `>` (strictly better) or
   `≥` (not worse), optionally require a *true upgrade* (never worse in anything), and get
   every build that beats yours, with the stat deltas highlighted.
4. **Reference tables** — every character / vehicle stat group in full.

## How the stats work

Each build's stat = **character value + vehicle value**. Speed and Handling each split into
three terrain types — **Road** (solid), **Off‑Road** (coarse/rough) and **Water** (liquid).
**Acceleration** also drives mini‑turbo; **Weight** also affects coin capacity. Characters or
vehicles that share an identical stat line are grouped onto one row.

## Running it

Just open `index.html` in any browser. That's it.

## Free hosting with GitHub Pages

GitHub Pages hosts static sites like this one **for free**. To turn this repo into a live website:

1. On GitHub, go to the repo's **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Pick the branch that has `index.html` and the folder **`/ (root)`**, then **Save**.
4. Wait ~1 minute; the page will be published at
   `https://<your-username>.github.io/Mario-Kart-World-Stats-Calculator/`.

No payment or extra setup is required — Pages is free for public repositories.

## Data source

Stat values are community stat rips for Mario Kart World (base character values plus vehicle
modifiers, with the three terrain sub‑stats). Cross‑checked against public stat guides
(Game8, Dexerto, VULKK) — e.g. Bowser is the fastest/heaviest, the Swooper group the lightest,
the Stellar Sled has the highest speed. If Nintendo patches stats, edit the `CHARS` and
`KARTS` arrays near the top of the `<script>` block in `index.html`.
