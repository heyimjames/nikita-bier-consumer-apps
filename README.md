# Nikita Bier Consumer Apps — Claude Skill

A Claude AI skill that packages Nikita Bier's complete playbook for building viral consumer iOS/mobile apps. Derived from his podcast appearances (Lenny's Podcast, My First Million), X/Twitter threads, product teardowns of tbh, Gas, and Explode, and published analyses of his methods.

## What It Does

When activated, this skill turns Claude into a consumer app growth advisor channelling Bier's playbook. It's built as a **tactical playbook, not a philosophy deck** — every recommendation carries a *when*, a *how many*, a *what gates what*, and a *metric that tells you it worked*.

**It asks before it answers.** The skill runs a mandatory five-question intake (app shape, audience age band, core aha, current loop, ask type) before giving advice, then tags every recommendation `[Network]` / `[Utility]` / `[Universal]` so you know what to ignore.

It covers:

- **App shape classification** — Network vs Utility vs Hybrid, with a comparison table that changes every downstream recommendation
- **Audience economics** — the −20%/year invite decay table from age 13 to 18, the age-22 cut-off, and what to do instead when your audience is older
- **Onboarding & activation** — ≤3s aha, ≤60s viral bridge, ≥40% activation, the ~6 screen ceiling, the 5–10% cost of every extra form field
- **Permission flows** — soft-ask → system pattern (+20–30%, and 80%+ system approval after a cleared soft-ask), plus the fixed ask order
- **Viral loop design** — five instrumented stages, K > 1 in hours, four share patterns and when each applies
- **iOS surfaces** — a use-when + risk table for Live Activities, App Clips, iMessage, PiP, widgets, and contacts
- **The Explode teardown** — a full ten-step funnel breakdown, product chrome, a seven-item steal checklist, and an explicit do-not-cargo-cult list
- **Monetisation** — paywall placement table (three "never" slots), God Mode, dual unlock, real pricing
- **Retention** — the ~7 opens rule, content scarcity, push ranking and timing
- **Launch** — the tbh sequence, 40%/24h pass-fail, the Death Clock play for utilities, and crisis planning from the Gas hoax

## How to Install

### Claude Projects (easiest)

1. Create or open a Project on [claude.ai](https://claude.ai)
2. Add the `SKILL.md` file to the project knowledge
3. Optionally add the reference files for deeper detail
4. Claude will activate the skill automatically when you ask about consumer apps, viral growth, onboarding, etc.

### Claude Code

```bash
mkdir -p .claude/skills
cd .claude/skills
git clone https://github.com/heyimjames/nikita-bier-consumer-apps.git
```

### Manual

Paste the contents of `SKILL.md` into a Claude system prompt or project instructions. Include whichever reference files are relevant to your use case.

## File Structure

```
nikita-bier-consumer-apps/
├── README.md              ← You are here
├── SKILL.md               ← Core skill — frameworks, decision trees, rules of thumb
├── viral-loops.md         ← Viral loop anatomy, K-factor, share patterns, case studies
├── onboarding.md          ← Permission flows, screen architecture, activation benchmarks
├── launch-strategy.md     ← Geofenced rollout playbook, content distribution, scaling
├── ios-hacks.md           ← Live Activities, PiP, iMessage, ASO, platform risk
├── monetisation-retention.md ← God Mode pattern, subscriptions, push notifications, streaks
└── product-psychology.md  ← FOMO/validation psychology, testing machine, ethical boundaries
```

## How It Works

The `SKILL.md` frontmatter contains a `name` and `description` that Claude uses to decide when to activate the skill. When triggered, Claude reads the main SKILL.md for frameworks and decision trees, then selectively loads the relevant reference files for deeper guidance.

The skill uses **progressive disclosure** — it doesn't dump the entire playbook at once. It identifies which frameworks apply to your specific situation and pulls in the right material.

## What It Covers

### The Three Axioms
1. Every tap is a miracle
2. The product IS the marketing
3. Consumer products live and die in the pixels

### Comparison Tables
The skill leads with tables rather than prose, because the right answer usually depends on one variable:

| Table | Decides |
|---|---|
| App shape — Network / Utility / Hybrid | Everything downstream: growth lever, target age, launch shape, kill signal |
| Age invite economics (13 → 22+) | Whether an organic invite loop is even available to you |
| Paywall timing | The three moments that are always wrong, and the five that work |
| Permission pattern & order | Approval rates and what to fall back to when denied |
| iOS surfaces — use-when + risk | Which platform hacks are worth the fragment, and which need a kill switch |
| Explode funnel, steps 1–10 | A concrete reference funnel to score your own against |

### Decision Trees
- "Should I build this app?"
- "Why isn't it growing?" (branches on activation first, then K-factor)

### Quick Reference
One table of every number in the playbook: ≤3s aha, ≤60s share prompt, ≥40% activation, ≤6 onboarding screens, 3 signup fields, −5–10% per extra field, +20–30% soft-ask lift, ~65% contacts approval on iOS 18+, −20%/year invite decay, ~7 opens to prove yourself, 40%/24h launch target, ~3 exposures, Gas God Mode at $6.99–7/week (~$7M in 3 months, ~$11M total), Explode+ at ~$39.99/yr or $7.99/mo, tbh's ~$30M exit in ~9 weeks, and the ~50% failure risk added per fragment.

## Sources

Synthesised from Nikita Bier's public content and published teardowns:

- [Lenny's Podcast — *How to consistently go viral: Nikita Bier's playbook for winning at consumer apps*](https://www.lennysnewsletter.com/p/how-to-consistently-go-viral-nikita-bier) — invite decay, latent demand, teen density, tbh/Gas history, the trafficking hoax
- [julianivaldy.com — Explode product analysis](https://julianivaldy.com/explode-product-analysis-by-nikita-bier) — onboarding funnel, viral loop, Live Activities
- [retention.blog/p/explode](https://www.retention.blog/p/explode) — screen-by-screen onboarding teardown
- [TechCrunch, 15 Jan 2025 — Explode launch](https://techcrunch.com/2025/01/15/creator-of-gas-and-tbh-makes-an-app-for-disappearing-photos-via-imessage/) — Explode+ pricing, feature set, SnapKit history
- Gas — Wikipedia and public revenue figures (~$11M pre-acquisition, God Mode pricing)
- Nikita Bier's X thread on Death Clock — rename, death-date artefact, CAC to pennies
- Nikita Bier's X threads on inverted time-to-value, why shares decrease with age, and why people download apps
- My First Million podcast; TEDx Boston talk

## License

MIT
