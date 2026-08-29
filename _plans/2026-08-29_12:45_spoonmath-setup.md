# SpoonMath — master plan

Autonomous project: build and grow spoonmath.com, a hub of fast, free kitchen
calculators, until it earns ~200 EUR/month (ads first, donations later,
premium/SaaS only if a tool takes off).

## Decisions (locked with Anthony, 2026-08-29)

- Niche: cooking/baking micro-tools. Broad non-technical audience, low adblock,
  good food-ad rates, huge long-tail ("grams to cups X", "air fryer conversion").
- Domain: spoonmath.com (Anthony buys on Porkbun, ~11 EUR/yr). Canonical host:
  apex `https://spoonmath.com`.
- Hosting: GitHub Pages, public repo Mytrill/claude-creative, serve from
  `main:/docs`. Migrate hosting only when a premium tier needs a backend.
- Monetization order: nothing -> AdSense once domain + ~20 pages + some traffic
  -> donations link -> premium only with proven demand.
- Stack: plain HTML/CSS/JS, no framework, no build step. Each tool page is
  self-contained (inline JS). One shared style.css. A generator script is
  allowed only when programmatic pages (per-ingredient converters) begin.

## Phases

1. v1 (this session): 5 tools + homepage, sitemap, robots, deploy live.
   Tools: cups-to-grams, recipe-scaler, cake-pan-converter,
   oven-temperature-converter, air-fryer-converter.
2. Foundation week: domain live, Search Console verified + sitemap submitted,
   about page, 3-5 more tools (butter converter, yeast converter, sourdough
   hydration, measurement substitutions).
3. Programmatic long-tail: per-ingredient pages (/cups-to-grams/flour/ etc.)
   generated from the density table (~50-150 pages). This is the main SEO play.
4. Iterate on Search Console data: double down on whatever gets impressions.
   Seasonal tools ahead of spikes (turkey thaw calculator before November).
5. Monetize when justified: AdSense application, then Ko-fi.

## Operating model

- Anthony says "wake up" on a fresh (Sonnet, low effort) session. That session
  follows CLAUDE.md: read STATE.md, do the top NEXT item(s), update STATE.md,
  commit, push, verify live.
- Keep sessions cheap. Spawn a higher-effort subagent only for building big
  features or writing many pages at once.
- Human tasks live in STATE.md "WAITING ON HUMAN" and get repeated at the end
  of every session until done.

## SEO rules

- One query family per page, exact phrase in title/h1/url.
- Minimal prose (tool + data table + short FAQ), fast pages, no cookie banners.
- Never change a live URL. Update sitemap.xml on every page add.
- Internal links: every tool page links home + 3 related tools in footer.
