# SUA SPONTE

> *Sua Sponte* — Latin, "of their own accord." Motto of the 75th Ranger Regiment.
> The one who doesn't need to be told. The one who goes.

A single-file, offline-first daily operating system for Ranger prep and real mind work. No server. No login. No algorithm. No confetti. Just the log.

## The point

The floor gets men into Ranger School. The mental engine is what gets them through it. This app is built around that distinction.

The PT targets are not RAP Week minimums. They're hard goals — numbers you train *toward*, not *past once* at selection. That's how you build the engine. Athletes know this: the kid running 4:20 miles wasn't born doing it; he trained where 4:40 felt honest-hard until it didn't.

The mind work is not operator LARP. It's clinical — CBT (Beck, Burns) and DBT (Linehan) — because that's what actually moves the needle on rumination, emotion regulation, and hard conversations. If you are doing real work on I-statements with your dad, the DEAR MAN planner in MIND is the structured version of what you are already doing.

## The daily loop

1. **BRIEF** — at dawn, lock the mission, see your engine score, read the stanza.
2. **PT / LEDGER / MIND** — train the body, run the habits, use the cognitive tools when thoughts or emotions are spiking.
3. **AAR** — at night, four questions. Plan vs. actual. Gap. Lesson. Close the day.
4. **Sleep.** The next day starts empty. The log carries the continuity.

## The six tabs

| Tab | Purpose |
|---|---|
| **BRIEF** | Morning lock-in — mission, score against hard goals, stanza of the day, PLEASE body-basics, today's habits, **recovery row** (sleep / RPE / soreness), **phase switcher**, **export/import** |
| **PT** | Log against hard-goal targets. **Readiness Map** (two tiers, auto-ticked). **Trends** (30-day / 90-day / all-time bests per event). |
| **LEDGER** | Build habits / Break habits — streaks. Cue-routine-reward, not willpower. |
| **MIND** | One-tap **"I'm spiking"** emergency button. CBT thought record · DBT Check-the-Facts / Opposite Action · TIPP · Box breathing + Cyclic sighing (Stanford 2023) · DEAR MAN planner. Quick-pick chips on every emotion field. |
| **AAR** | Four-question After-Action Review (FM 7-0, Appendix K) + two gratitudes. Quick templates: Strong / Flat / Rough / Same as yesterday. |
| **CREED** | Full Ranger Creed with stanza-by-stanza interpretations · "Where I stand today" preamble · cognitive distortions reference · DBT cheat sheet · **Sources card** (full citations). Each operational tab also carries an inline anchor of the relevant stanza. |

## Phases (long-arc context)

| Phase | When |
|---|---|
| **Base building** | 8–16 weeks of general fitness, habit foundation. Volume over intensity. |
| **Specific prep** | Ranger-shape training. Targets in sight. |
| **Peak / pre-school** | Last 4–6 weeks. Volume drops, intensity peaks, recovery is sacred. |
| **In-school** | At Fort Moore. Survival mode. App use optional. |
| **Active duty** | Maintain the engine on a unit's schedule. |
| **Recovery / injury** | Repair phase. Reduced load. Habits and mind work continue. |
| **Maintenance** | Off-cycle. Hold the floor; don't lose the engine. |

Reference: Bompa & Haff, *Periodization* (6th ed., 2018).

## PT targets vs. the floor

| Event | Target (hard goal) | Ranger School floor (reference only) |
|---|---|---|
| Push-ups (2 min) | **100** | 49 |
| Sit-ups (2 min) | **100** | 59 |
| Chin-ups (dead-hang) | **20** | 6 |
| 2-mile run | **12:00** | ~15:42 |
| 5-mile run | **32:00** | 40:00 |
| 12-mile ruck (47 lb) | **2:15** | 3:00 |

Your "engine score" is the composite of your bests vs. the targets. Hit 100% and raise the targets — the engine needs resistance to keep growing.

## Running it

**Option 1 — Just open it.** Double-click `index.html`. Data persists via `localStorage`.

**Option 2 — Serve it (recommended; enables install-to-home-screen):**
```bash
python3 -m http.server 8000
# or
npx serve .
```
Open `http://localhost:8000` on your phone (same Wi-Fi) → Safari/Chrome → "Add to Home Screen". Installs standalone.

**Option 3 — Host it.** Drop the four asset files into any static host (GitHub Pages, Netlify, Cloudflare Pages).

## Files

```
index.html      The whole app. HTML/CSS/JS inline.
manifest.json   PWA manifest.
sw.js           Service worker — offline.
icon.svg        App icon.
README.md       This file.
```

## Dropping into a repo

1. Copy the four assets into a `/app/`, `/public/`, or `/docs/` folder.
2. Commit.
3. Point the host at the folder.

## Data & backup

Stored locally under `suasponte.v3` in `localStorage`. **Use the BRIEF tab → Long arc → Export JSON** to download a snapshot of every metric — bests, recovery, AAR history, mind-work entries, habit streaks, mission logs, phase — as a single JSON file. **Import JSON** restores from that file on any device. Do this monthly. Local storage is fragile; lifetime data needs portable backup.

## Verification

`smoke.js` runs a jsdom smoke suite — loads the page, renders every tab, exercises saving PT and AAR, checks that the target/floor semantics are wired right. Run:
```bash
npm install jsdom
node smoke.js
```
110 assertions currently pass.

## Sources

Full citations live in-app on the **CREED tab → Sources card**. Highlights:

- **CBT** — Beck (1979); Beck (2020); Burns (1980).
- **DBT** — Linehan (2014).
- **Cyclic sighing** — Balban et al., *Cell Reports Medicine* (2023).
- **Box breathing** — SEALFIT, Mark Divine; pranayama traditions.
- **AAR** — U.S. Army FM 7-0, Appendix K.
- **Periodization** — Bompa & Haff (2018); Friel (2018).
- **Sleep** — Walker (2017); Hirshkowitz et al. (2015).
- **RPE** — Borg (1982).
- **Sleep quality** — Buysse PSQI (1989), simplified.
- **Habits** — Gollwitzer (1999); Fogg (2019); Clear (2018).
- **Stress inoculation** — Meichenbaum (1985).
- **Ranger doctrine** — U.S. Army Ranger Training Brigade.
- **Ranger Creed** — CSM Neal R. Gentry, 1974.

## RLTW

Rangers lead the way. Sua sponte.
