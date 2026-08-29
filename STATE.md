# STATE

## WAITING ON HUMAN

- [ ] Buy spoonmath.com on Porkbun: https://porkbun.com/checkout/search?q=spoonmath.com
- [ ] Add DNS records at Porkbun (after purchase):
      A     @    185.199.108.153
      A     @    185.199.109.153
      A     @    185.199.110.153
      A     @    185.199.111.153
      CNAME www  mytrill.github.io
      (delete Porkbun's default parking A/ALIAS/CNAME records first)
- [ ] After DNS works (site loads at spoonmath.com): say "wake up" so I enable
      HTTPS enforcement and prep Search Console.
- [ ] Google Search Console: add property "spoonmath.com" (domain property,
      verify via DNS TXT record at Porkbun), then submit sitemap
      https://spoonmath.com/sitemap.xml. I'll remind with exact steps when DNS is live.

## NEXT (priority order)

1. Once domain live: enforce HTTPS on Pages (gh api), swap any github.io
   references, walk Anthony through Search Console + sitemap submission.
2. Add tools: butter-converter (sticks/cups/grams/tbsp), dry-to-fresh yeast
   converter, sourdough-hydration-calculator, measurement-substitutions page.
3. Programmatic pages: generator script in tools/ that emits
   /cups-to-grams/<ingredient>/ pages from the density table in
   docs/cups-to-grams/index.html (keep one source of truth: move densities to
   tools/densities.json, generator reads it; main converter page keeps its
   inline copy in sync via the generator). ~40 pages, each with per-amount
   table (1/4, 1/3, 1/2, 2/3, 3/4, 1, 1.5, 2 cups). Main SEO play.
4. About page + privacy page (needed for AdSense later).
5. When Search Console shows impressions: analyze queries, build tools/pages
   for what's actually searched. Seasonal: turkey-thaw + turkey-cooking-time
   calculators must be live by late October.
6. At ~20 pages and first traffic: queue AdSense application for Anthony.

## SESSION LOG (newest first)

### 2026-08-29 — setup (Fable)
Decisions locked with Anthony (see _plans/2026-08-29_12:45_spoonmath-setup.md).
Built v1: homepage + 5 tools (cups-to-grams, recipe-scaler, cake-pan-converter,
oven-temperature-converter, air-fryer-converter), style.css, sitemap, robots,
404, CNAME. Made repo public, enabled Pages from main:/docs with custom domain
spoonmath.com. Live check OK on github.io.
