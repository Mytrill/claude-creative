# SpoonMath — autonomous project

You (Claude) run this project. Anthony only says "wake up" and handles the
human-only tasks you queue for him. Full context: `_plans/2026-08-29_12:45_spoonmath-setup.md`.

## Wake-up protocol

1. Read `STATE.md`. Do NOT re-read the plan or old sessions unless needed.
2. Do the top unblocked item(s) in NEXT. One or two items per session is fine.
3. Update STATE.md: append a 2-4 line session log entry, adjust NEXT,
   update WAITING ON HUMAN.
4. Commit and push. Verify the live site still works
   (`curl -s https://spoonmath.com/ | head -20` or the github.io URL).
5. End by telling Anthony: what you did, what's next, anything in WAITING ON HUMAN.

## Hard rules

- Site lives in `docs/`, served by GitHub Pages from main:/docs.
  Live at https://spoonmath.com (fallback https://mytrill.github.io/claude-creative/).
- Plain HTML/CSS/JS only. No frameworks, no build step, no npm. Tool pages are
  self-contained with inline JS. Shared `docs/style.css`.
  Exception: `tools/` may hold small node generator scripts for programmatic
  pages (they write static HTML into docs/, committed).
- Never change or remove a live URL. New page => add to sitemap.xml and link it
  from the homepage + related pages' footers.
- Minimal prose on pages: tool first, data table, short FAQ. No filler text.
- SEO: exact query phrase in title/h1/url; unique title + meta description +
  canonical per page.
- Keep tokens cheap: you are usually Sonnet on low effort. Spawn ONE
  higher-effort subagent only when building something big (many pages, tricky
  JS). Never fan out multiple agents.
- Verify math/data before publishing (ingredient densities, temperatures).
  Wrong numbers on a cooking site kill trust and rankings.
- Money: no spending, no new accounts, no publishing to external services
  beyond this repo/GitHub Pages without queueing it for Anthony.
