# Roof Pitcher

Tyler Mentges' roofing sales training, coaching, and ops business. Built with Astro + Tailwind + MDX. Deploys to Cloudflare Pages.

## Stack

- **Astro 5** — content-first, ships near-zero JS by default
- **Tailwind CSS** — design system in `tailwind.config.mjs` (torch/ink/steel palette, "Anton" display font for the blue-collar punch)
- **MDX** — for blog/resources when you want React-style components in markdown
- **@astrojs/sitemap** — auto sitemap.xml

## Local dev

```bash
npm install
npm run dev      # http://localhost:4321
npm run build    # outputs to ./dist
npm run preview  # serves the build locally
```

## Deploy (Cloudflare Pages)

Same pattern as the other migrations in this account:

- Build command: `npm run build`
- Output directory: `dist`
- Environment: Node 20+

Push to GitHub and connect the repo in the Cloudflare Pages dashboard. Set `roofpitcher.com` as the production custom domain.

## Site map

| Route | Purpose |
|---|---|
| `/` | Home: hero, method, services tease, testimonials, resource tease |
| `/about/` | Tyler's story + operating principles |
| `/services/` | All 3 tiers + comparison matrix |
| `/zero-to-50/` | Flagship program landing |
| `/resources/` | Free resource hub index |
| `/resources/scripts/` | D2D + insurance + retail scripts |
| `/resources/playbooks/` | Storm response, hiring, owner replacement |
| `/resources/calculators/` | Live JS calculators (appt math, ROAS) |
| `/resources/glossary/` | Insurance + technical glossary |
| `/case-studies/` | Real numbers with before/after |
| `/blog/` | Field Notes |
| `/podcast/` | The Pitcher Podcast |
| `/partners/aaron-chat/` | Marketing partnership page |
| `/book/` | Pitch Audit form |

## Service tiers (business model)

| Tier | Price | Cadence | Audience |
|---|---|---|---|
| Pitch Pack | $497 | one-time | Solo reps, owner-ops |
| Crew Builder | $2,497/mo | recurring | 3–15 rep shops |
| **Zero to 50** | **$25K + $5K/mo** | 12-mo min | Owners wanting marketing + sales + ops |

Zero to 50 marketing is fulfilled by [aaron.chat](https://aaron.chat). Sales/training/ops by Tyler.

## To-do before launch

- [ ] Replace `https://formspree.io/f/REPLACE_ME` in `book.astro` with real endpoint (Formspree, HubSpot, Cal.com, etc.)
- [ ] Add a real headshot of Tyler on `/about/`
- [ ] Wire podcast platform links
- [ ] Drop real Stripe checkout link in `/services/#pitch-pack`
- [ ] Generate `/og-default.png` (1200x630) for OpenGraph
- [ ] Write 3–5 real blog posts in `src/content/blog/` (MDX)
- [ ] Set up email capture for the Resource Hub

## Brand notes

- **Tone**: blue-collar punch. Short sentences. No fluff. Tyler talks like he sits in trucks for a living because he does.
- **Visual language**: hard 2px borders, hard offset shadows (shadow-hard), Anton display font, hi-vis torch orange (#f97316) on ink black. Construction-site / safety-vest energy.
- **No emojis in copy** except sparingly as bullet icons in marketing-partner sections.

## Competitor landscape (positioning rationale)

- **Adam Bensman / The Roof Strategist** — owns content + podcast. We compete on done-WITH-you (he's done-by-you).
- **Sam Taggart / D2D Experts** — owns the D2D bootcamp niche. We compete on full-business (marketing + sales + ops).
- **Chuck Thokey / Top Rep** — owns "close more $20K+ jobs" angle. We compete on appointment volume + retention.
- **CertainPath / Pro Contractors Network** — own franchise-style business systems. We compete on size (smaller shops) and unbundled marketing.

Roof Pitcher's wedge: **only player bundling marketing fulfillment + sales training + ops in one contract with a written appointment-flow guarantee.**
