# Nikita Bier Consumer Apps — Claude Skill

A Claude AI skill that packages Nikita Bier's complete playbook for building viral consumer iOS/mobile apps. Derived from his podcast appearances (Lenny's Podcast, My First Million), X/Twitter threads, product teardowns of tbh, Gas, and Explode, and published analyses of his methods.

## What It Does

When activated, this skill turns Claude into a consumer app growth advisor channelling Bier's frameworks. It covers:

- **Viral loop design** — K-factor engineering, share mechanic patterns, natural incentive alignment
- **Onboarding optimisation** — 3-second time-to-value, permission flow design, activation funnels
- **Launch strategy** — Geofenced rollouts, content-first distribution, the 40% penetration rule
- **iOS platform hacks** — Live Activities, PiP, iMessage apps, ASO tricks, App Clips
- **Monetisation** — The God Mode pattern, dual-unlock (invite OR pay), subscription timing
- **Retention** — Content scarcity, push notification strategy, fighting the retention cliff
- **Product psychology** — FOMO, social validation, latent demand detection, idea validation

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

### Frameworks
- **Idea Validation** — Latent demand detection, the Bier Test (4 questions), media-first product-second
- **Audience & Network Strategy** — The age gradient, dense network targeting, cold start solutions
- **Viral Loop Design** — Natural incentive alignment, K-factor checklist, 5 share mechanic patterns
- **Onboarding** — The 3-second rule, permission flow design, screen-by-screen architecture
- **Launch Strategy** — Geofenced rollouts, the 40% penetration rule, content-first distribution
- **iOS Platform Exploitation** — Live Activities, PiP, iMessage apps, ASO hacks, App Clips
- **Monetisation** — God Mode pattern, dual-unlock model, subscription timing
- **Retention** — Content scarcity, push notification strategy, fighting the retention cliff

### Decision Trees
- "Should I build this app?"
- "Why isn't my app growing?"

### Quick Reference
Rules of thumb with specific numbers: time to value (3 seconds), MVP build time (8 weeks), penetration targets (40% in 24 hours), invite decay rates (-20% per year of age), and more.

## Sources

Synthesised from Nikita Bier's public content:
- Lenny's Podcast appearance (Aug 2024)
- My First Million podcast
- X/Twitter threads on consumer app growth
- Product teardowns of tbh, Gas, and Explode
- TEDx Boston talk
- Published analyses and case studies

## License

MIT
