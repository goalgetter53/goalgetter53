# Hussain Singapuri

**GTM engineer who writes real code.** I build the systems that find, reach and win customers: signal ingestion and entity resolution, learned enrichment routing, guarded AI agents, CRM sync and attribution.

3 years (2023–2026) as a full-stack developer at a US medtech company (web apps, a CRM, 5 Android apps live on Google Play, security testing). Now I work on the revenue side: Clay, n8n, HubSpot, Instantly, Python and the Claude API.

**Portfolio:** [goalgetter53.github.io](https://goalgetter53.github.io) · [LinkedIn](https://www.linkedin.com/in/hussain-singapuri-18437225a/) · [X @hussain_gtm](https://x.com/hussain_gtm) · Hussainsingapuri24@gmail.com · Pune, India, open to remote

---

## GTM engineering

| Project | What it does | Measured |
|---|---|---|
| [**signalgraph**](https://github.com/goalgetter53/signalgraph) | Public buying signals (SEC Form D, job boards, GitHub, news) → entity resolution → time-decayed account scoring. DuckDB, FastAPI. | **Real (Wikidata, 5,044 records):** F1 0.400 vs 0.291 naive join. Synthetic: 0.974 vs 0.784. 809 live signals |
| [**waterfall-optimizer**](https://github.com/goalgetter53/waterfall-optimizer) | Enrichment orchestrator: Thompson-sampling provider routing per segment, crash-safe queue, rate limits, circuit breakers, cost ledger. | **Real prices + published hit rates:** −17.2% ± 4.2 pp cost per verified email vs cheapest-first (outcomes simulated) |
| [**ai-sdr-crew**](https://github.com/goalgetter53/ai-sdr-crew) | Multi-agent outbound copilot on Claude: cited facts only, prompt-injection defences, regression evals, Bayesian A/B, human approval queue. | **Real attacks (3 public datasets):** detector catches 44.8%, 0 false alarms on benign data; in-house suite 0/14 got through |
| [**crm-sync-engine**](https://github.com/goalgetter53/crm-sync-engine) | Bi-directional warehouse ↔ HubSpot sync: YAML mappings, per-field conflict policies, terraform-style plan/apply, dead-letter + replay. | **Real (11,082 Wikidata companies, 10 yrs of changes):** 52.7× fewer API calls; 0 mismatches under injected faults (fake HubSpot) |
| [**gtm-attribution-lab**](https://github.com/goalgetter53/gtm-attribution-lab) | Attribution engine (heuristics, Markov, Shapley) validated against synthetic ground truth; DuckDB SQL layers; Kaplan-Meier funnel timing. | **Real (Criteo, 16.5M impressions):** models disagree most under Markov (ρ 0.93 vs last touch). Synthetic: last-touch gives organic 17–21% credit when its true effect is 0 |

Every number comes from an actual run. Real-data results (Wikidata, Criteo, public attack datasets, real vendor prices) are listed first; simulation, synthetic and fake-API results are labelled in each README.

---

## Websites & products

### [Lumen: Spring '27 Release](https://github.com/huss2003/lumen-release) · [live site](https://lumen-release.vercel.app)

[![Lumen: Spring '27 Release](https://raw.githubusercontent.com/huss2003/lumen-release/main/docs/cover.jpg)](https://lumen-release.vercel.app)

A scroll-driven launch site for a fictional AI creative suite, told as one continuous scroll story. A glass lens drawn live on canvas splits its halo into twelve colour bands; the bands hand off seamlessly into a pinned section where each one opens into an iridescent glass panel for one tool, then settles into a filterable grid. Panels tilt with a holographic foil on hover and open into a detail sheet that grows from the click point.
**Stack:** Next.js, TypeScript, GSAP (ScrollTrigger, snapping), Lenis, Canvas 2D, Vercel

### [Kilnwood Roasters](https://github.com/huss2003/kilnwood-roasters) · [live site](https://kilnwood-roasters.vercel.app)

[![Kilnwood Roasters](https://raw.githubusercontent.com/huss2003/kilnwood-roasters/main/docs/hero.jpg)](https://kilnwood-roasters.vercel.app)

A motion-led, editorial site for a fictional coffee roastery. An opening sequence deals real coffee photos onto a card while the brand name splits around it, then the last photo opens out to become the hero. Smooth scrolling, a pinned horizontal product lineup, a scroll-driven process timeline, and scroll-velocity marquees.
**Stack:** Next.js, TypeScript, GSAP (ScrollTrigger, SplitText), Lenis, Vercel

### Cairnmoor · [live site](https://cairnmoor.vercel.app)

A calm-luxury website for a fictional Highland thermal-baths retreat. Mist parts over a dawn loch before the name rises letter by letter; a pinned intro morphs photo frames between organic shapes while text screens fade in and out; sections wipe open in layers; a tilted 3D map follows the pointer and pops up photos on its pins; and a pinned panorama pans across the glen with drifting mist. Dedicated mobile layouts and a reduced-motion version.
**Stack:** Next.js, TypeScript, GSAP (ScrollTrigger, SplitText, MorphSVG), Lenis, Vercel

### [Lowlight Video Club](https://github.com/huss2003/lowlight-video-club) · [live site](https://lowlight-video-club.vercel.app)

[![Lowlight Video Club](https://raw.githubusercontent.com/huss2003/lowlight-video-club/main/docs/home.jpg)](https://lowlight-video-club.vercel.app)

An interactive website for a fictional film-restoration club that lives inside an old CRT television, where every film is a VHS tape. A 3D tape deck in three.js runs on hand-written spring physics (drag, fling, scroll, keyboard); each sleeve is painted live from a film still and aged procedurally; WebGL and page content share one screen-curve distortion; and pages change with a channel-switch transition. Fallbacks for phones, reduced motion and slow graphics cards.
**Stack:** HTML, CSS, JavaScript (no framework), three.js, WebGL, View Transitions, Vercel

### [PageForge](https://github.com/huss2003/pageforge) · [live demo](https://pageforge-hazel.vercel.app/abm)

Account-based marketing pages with evidence behind every claim. A marketer turns an account brief into a branded landing page for one target account; AI drafts only from approved facts and the account's public pages, a deterministic validator flags unsupported numbers, a reviewer signs off claim by claim, and engagement flows to analytics and the CRM.
**Stack:** Next.js 16, React 19, Tailwind v4, Sanity, Supabase, Gemini, PostHog, HubSpot

---

## AI systems

| Project | What it is | Stack |
|---|---|---|
| [**nanoserve**](https://github.com/huss2003/nanoserve) | LLM inference engine from scratch: paged KV cache, prefix caching, continuous batching with preemption, speculative decoding, OpenAI-compatible streaming API. 3.1x throughput over sequential decoding in benchmarks. | Python, PyTorch, FastAPI |
| [**multi-agent-research-crew**](https://github.com/huss2003/multi-agent-research-crew) | Planner, parallel researchers, writer and verifier agents on a custom DAG orchestrator with retries, timeouts, token budgets and claim-level citation checking. | Python, asyncio, Claude |
| [**site-to-agent**](https://github.com/huss2003/site-to-agent) | Turn any website into a grounded chat agent: crawler, hybrid BM25 + vector retrieval with RRF, cited answers, SSRF-hardened fetching, eval harness. | Next.js, TypeScript, pgvector |
| [**ai-lead-receptionist**](https://github.com/huss2003/ai-lead-receptionist) | AI receptionist for home-service businesses: missed-call text-back, SMS/web chat that qualifies and books jobs, owner dashboard. | Next.js, Twilio, Claude, Supabase |
| [**lead-intel-engine**](https://github.com/huss2003/lead-intel-engine) | Discover, enrich and score local-business leads with a robots-aware, rate-limited crawler and transparent scoring. | Python, FastAPI, SQLite |
| [**contractor-ai-ops-dashboard**](https://github.com/huss2003/contractor-ai-ops-dashboard) | Multi-tenant analytics with signed event ingestion, funnel metrics, anomaly alerts and number-checked AI weekly summaries. | Next.js, Recharts, Postgres RLS |
| [**supportai**](https://github.com/huss2003/supportai) | LLM-powered customer support assistant. | Python |

---

## Also building

- **[NeuroNetworks AI Ed](https://github.com/huss2003/NeuroNetwrks.com)**, CTO & Principal Course Architect: AI and tech programmes for students after Class 10, plus [Neuromind Lab](https://github.com/huss2003/Neuromind-lab), a browser-based practice lab with an AI tutor.
- **[cybersecurity-portfolio](https://github.com/huss2003/cybersecurity-portfolio)**: SOC analyst labs and write-ups.

---

## Stack

**AI:** LLM inference, RAG, multi-agent systems, tool use, evals, prompt-injection defence
**Front end:** Next.js, React, TypeScript, Tailwind, GSAP, Lenis, Canvas, motion and interaction design
**Backend:** FastAPI, Node.js, PostgreSQL, Supabase, Sanity
**GTM:** Clay, n8n, Make, Zapier, HubSpot, Instantly, Smartlead, Apollo, Apify, deliverability (SPF/DKIM/DMARC)
**Automation:** workflow automation, webhooks and CRM integrations
**Infra:** Docker, Vercel, GitHub Actions
**Security:** app penetration testing, SSRF hardening, auth and webhook signing

## Certifications

- Claude Certified Developer – Foundations (CCDV-F)
- Claude Certified Orchestrator – Foundations (CCAO-F)
- Google Cloud Generative AI Leader

## Work with me

Hiring a GTM engineer, or need outbound, enrichment or CRM automation built? I also build websites, AI agents and internal tools.
Reach me on [LinkedIn](https://www.linkedin.com/in/hussain-singapuri-18437225a/) or open an issue on any repo.
