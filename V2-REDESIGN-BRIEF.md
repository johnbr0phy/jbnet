# johnbrophy.net v2 — Redesign Brief & Handoff

> Handoff doc so we can pick up the v2 redesign in a fresh session. Written 2026-07-25.
> Wireframes artifact: https://claude.ai/code/artifact/b14fd26c-a393-432a-b167-973763f7a1f6

## The goal (in John's words)

Take johnbrophy.net from a 6-item nav down to **two pages**. Make it "way more simple" and
"way less like a resume, more like a beautiful stunning scrollable overview." Higgsfield will be
used to generate new imagery.

- **Resume → "My Story"** — a scrollable career narrative from **DSI (Don't Stay In) to Stensul**,
  walking through the work and showing **projects and core metrics along the way**. Proudest-moments
  feel, not a CV.
- **AI Creations → "Current Projects"** — the live things being built now, with real numbers.
- **Retire:** Photos, Doodles.
- **Homepage** = My Story. Contact collapses into the footer of both pages.

## Status

- [x] Reviewed current site + resume content
- [x] Produced 3 wireframe directions (artifact above)
- [x] Gave a recommendation
- [x] **Built all three in high fidelity** — working two-page prototypes in `v2/`
      (`v2/index.html` is the chooser; `option-a.html`, `option-b.html`, `option-c.html`).
      Serve with `python3 -m http.server` and open `/v2/`. Live site untouched.
- [ ] **NEXT: John picks a direction (or confirms the A-story + B-projects mix)**
- [ ] Generate/collect Higgsfield imagery for the chosen direction (prompts are printed
      inside each image slot in the prototypes)
- [ ] Confirm the Stensul ARR figure — brief says $500K+, live site redacts to $XXXK+
- [ ] Fold the winner into the root `index.html`, rebase on main, ship to GitHub Pages

## The three directions

| Option | Name | One-line | Build | Maintenance |
|---|---|---|---|---|
| **A** | The Documentary | Long-form editorial feature; full-bleed era imagery, metrics as pull-stats | High | Rewrite per chapter |
| **B** | The Ledger | Builder's log; sticky year rail, claim→numbers→artifact; Projects = live dashboard + changelog | Medium | Append a changelog line |
| **C** | The Gallery | Art-book minimal; one full-viewport plate per era, one number each; poster wall for projects | Med-high | New poster per project |

**Recommendation given:** Option **A's story page** + Option **B's projects page**. My Story is read
once and deeply → spend the beauty there. Current Projects must stay live/honest → make it the Ledger
(live totals + dated changelog, ~30 sec to update, never rots). Both share a **mono-numeral metric
treatment** so the site feels like one thing.
Fallback if John wants one pure direction: **B** — most differentiated from other product-leader
portfolios, and the numbers carry it.

## Shared content spine (same for all options — differs in telling, not content)

### My Story — six chapters

| Chapter | Years | Proud moment | Core metric |
|---|---|---|---|
| Don't Stay In (DSI) | 2003–10 | Co-founded a social network from a London flat; built the viral loop; sold it | 2M monthly uniques · 12M photos · 20M forum posts · grew team to 15 |
| Spotify | 2010–17 | Employee ~200; rebuilt signup, premium & download flows through hypergrowth | millions of registrations · company grew 20× |
| Kaplan Test Prep | 2017–20 | Built & led kaptest.com team; new CMS; mentored associate → senior PM | new product line for professional-cert exams |
| Hearst | 2020–22 | Migrated CMS frontend (React) under 60+ live sites without dropping traffic | 60+ sites · 500M monthly impressions |
| Whalar | 2022–24 | Shipped AI Profiles + ORCA brand-safety tool; led 3 PMs across global teams | −10% off-platform collabs |
| Stensul | 2024–now | Landing-page builder zero→one; MCP server; taught the org to build with AI | $500K+ ARR · creation time → ~1 hr · doubled output/customer |

Human beats to keep (don't let the edit strip them):
- Testimonials — Shirley Lee (Whalar), Felix Bouleau (Spotify), Grace Larosa (Spotify design). Trim to
  one line each, place inside the era they belong to.
- The Daily Mail helicopter story (tech-obsessive color). Camping / outdoors.
- Certs: Claude Code for PMs (fullstackpm), AI Product Management (Product Faculty / Miqdad Jaffer,
  OpenAI), Advanced PM Skills (Crystal Training).

### Current Projects — roster

| Project | One-liner | Live metric |
|---|---|---|
| TigerTest.io | Free DMV practice tests, built nights/weekends with Claude Code | 9,480 users · 278,478 questions answered · $829.17 revenue (Stripe) · 62,081 questions in June alone |
| Course Builder | A course factory — hands-on lessons generated for any topic, graded by Claude | learn-by-doing |
| LLM-Wiki | Turns transcripts, emails & docs into a queryable wiki, automatically | auto-structured knowledge |
| Ace That Interview | Company-specific interview prep pages (e.g. /google/product-manager) | programmatic SEO play |
| OpenClaw | An agent optimizing TigerTest on its own; long-term goal: earn $100K for an Optimus body | (video exists: videos/openclaw-okr.mp4) |
| Smaller | Banksy Print Tracker · AI PM Course · New Parent Qbank | collapse into an index row |

## Higgsfield image briefs (per direction)

**A — Documentary (~6 hero scenes):**
- 35mm flash photo, sweaty London indie club night 2004, crowd mid-dance, motion blur, no faces in focus
- Golden-hour NYC office window reflection, 2012, MacBook with green glow, shallow depth of field
- Overhead desk at midnight: two monitors, terminal open, coffee, warm lamp — the nights/weekends builder
- Quiet Montclair street at dawn, cinematic, wide — the "now" chapter

**B — Ledger (minimal; mostly screenshots):**
- Macro shot of a receipt printer printing metrics; paper ledger textures (filler only)
- Isometric clay-render of a tiny workbench with 9 miniature glowing machines (one per project)
- Flat-lay of printed charts + index cards on a desk, harsh daylight, documentary style

**C — Gallery (~15 matched pieces):**
- Poster series, one per project, same 3-color palette across all nine (tiger for TigerTest, stacked
  blocks for Course Builder, etc.)
- Era plates, consistent painterly style: club queue in the rain (2003), wall of gig posters, single
  desk lamp in the dark (2026)
- All 4:5 ratio, muted palette matched to site neutrals + one accent

## Design system notes (starting point, not locked)

- **Voice:** first person, plain, confident, understated — let the numbers brag (like the existing
  TigerTest post). No hype.
- **Metric treatment (shared across both pages):** mono / tabular-nums, consistent format across all
  23 years. This is the connective tissue between the two pages.
- **Nav:** "John Brophy" left; "My Story · Current Projects" right. Contact → footer (email +
  Instagram/YouTube/LinkedIn/Spotify/GitHub socials).
- Palette explored in the wireframe: warm paper neutrals + a single vermilion/red accent, full
  light + dark theming. NOT locked — revisit per chosen direction.
- Per-option type ideas: A = editorial serif display + quiet grotesque + mono years; B = one sharp
  grotesque + mono for all numbers/dates, no serif; C = one display face at two extreme sizes only.
- **Avoid** the AI-generated default look (cream #F4F1EA + serif + terracotta is on the do-not-default
  list — the current wireframe leans warm-paper + red, so if we keep it, make it deliberate/distinct).

## Technical / codebase facts

- Repo: `/Users/johnbrophy/jbnet` — a single `index.html` static site (no build step),
  hand-written CSS + a vanilla-JS IIFE at the bottom. Deliberately light-only in v1.
- Deploy: **push to `main` → GitHub Pages**. Remote sometimes has other work landed (a
  thumbnail-layout PR merged mid-session on 2026-07-24) — `git pull --rebase` before pushing.
  End commit messages with the Co-Authored-By trailer.
- Routing today: hash-based one-page router. `pages = ['hello','resume','ai','adventures',
  'photos','doodles','contact']`, a `show(id)` function toggles `.on` sections + `.active` nav,
  `window.scrollTo(0,0)`, driven by `hashchange` + a nav-click handler we added on 2026-07-24
  (fixed the double-click-jumps-past-header bug). For v2 this collapses to two sections
  (`story`, `projects`) — reuse the same pattern.
- Contact form posts to a Google Form (`docs.google.com/forms/d/e/1FAIpQLSeQM2STqdhr6bkO...`)
  via `fetch` no-cors. Keep it.
- Resume PDF lives in Google Drive (file id `1DP2hnZG-xbEuH10QsesM7zvLPMtekXFa`) and is linked
  from the current resume section.
- Existing image dirs: `images/ai-creations/`, `images/hello/`, `images/adventures/`, etc.
  New Higgsfield assets will need a home (suggest `images/story/` + `images/projects/`).

## First actions for the fresh (Opus) session

1. Read this file.
2. Ask John which direction (or confirm the A-story + B-projects mix).
3. Build a working HTML prototype of both pages with placeholder image slots sized for the chosen
   ratios, real copy from the spine above, and the mono-numeral metric system.
4. Tighten Higgsfield prompts for the winning direction; John generates, we drop them in.
5. Rebase on main, test locally (the site is served with `python3 -m http.server`), ship.
