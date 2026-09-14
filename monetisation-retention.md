# Monetisation & Retention — Deep Reference

> Expands `SKILL.md` §9 (Monetisation) and §10 (Retention). `SKILL.md` is the source of truth — if
> anything here contradicts it, `SKILL.md` wins. Run the §0 intake first and tag every recommendation
> **[Network] / [Utility] / [Universal]**.

**The one rule that matters most:** never show a paywall during onboarding, before the aha, or in the
middle of a core action. Nearly every consumer app that "can't monetise" has it in one of those three
slots.

## Table of Contents
1. The God Mode Monetisation Pattern
2. Subscription Design for Consumer Apps
3. Retention Mechanics
4. The Retention Cliff and How to Fight It
5. Push Notification Strategy

---

## 1. The God Mode Monetisation Pattern

### How It Works

The core app is free and fully functional. The premium tier satisfies a curiosity or desire
that the free experience deliberately creates.

**Gas Implementation** — **[Network]**
- Free: Receive anonymous compliments via polls. Know someone said something nice about you.
- God Mode (**$6.99–7/week**): Get HINTS about who sent each compliment
- Result: **~$7 million in 3 months**, and **~$11 million total revenue before the Discord
  acquisition** — on zero venture funding

**Why this is brilliant:**
- The free experience creates the desire (curiosity about who sent the compliment)
- The paid tier satisfies the desire without diminishing the free experience
- Non-paying users still contribute to the ecosystem (sending compliments, participating in polls)
- Paying users don't get an unfair advantage — they just get more information

### The Dual-Unlock Model

Offer TWO paths to premium features:
1. **Invite friends** (drives growth)
2. **Pay** (drives revenue)

Both paths satisfy the same desire. Users self-select based on their preference:
- Price-sensitive users invite friends → growth
- Convenience-seeking users pay → revenue
- Either way, the app wins

**Explode Implementation** — **[Hybrid]**
- Send photos to **3 people within ~1 hour** → unlock 1 month premium free
- The free month **auto-transitions into an annual subscription trial**
- A Live Activity countdown carries the offer outside the app; the offer genuinely expires
- **Explode+ pricing: ~$39.99/year or $7.99/month** — screenshot alerts, screenshot blocking,
  replaying sent photos, locking photo viewing after send. Every paid feature is only meaningful
  *after* you've sent something: the paywall sells depth on an action already taken, never access
  to the action itself
- This simultaneously drives viral distribution AND converts to paid

---

## 2. Subscription Design for Consumer Apps

### Pricing Strategy

- Weekly subscriptions create urgency and low commitment ($6.99/week feels smaller than $27.96/month)
- Annual subscriptions maximise LTV — convert from weekly after users are habituated
- Free trials should be gated behind a viral action (shares, invites) not given away. A trial you
  hand out buys you nothing; a trial unlocked by 3 shares buys you 3 impressions
- The trial-to-paid conversion should be automatic with clear cancellation options
- **[Utility]** Older audiences invite less and pay more. Trade K for ARPU deliberately: charge more,
  charge earlier, stop apologising for it
- **[Universal]** Validate willingness to pay from day one. If users won't pay **and** won't invite,
  kill it this week

### Paywall Timing

| Moment | Show? | Why |
|---|---|---|
| During onboarding | **Never** | No value context. Kills activation outright |
| Before the aha | **Never** | You're charging for a promise |
| Mid-core-action | **Never** | Interrupting the thing they came for |
| As an interrupting modal | **Never** | Reads as a tax, not an upgrade |
| Immediately after a peak emotional moment | **Yes** | "Someone said you're the best dressed — want a hint who?" |
| At the natural edge of the free tier | **Yes** | The boundary explains itself |
| On completing a share/invite gate | **Yes** | Free month → annual trial (Explode) |
| Passive settings/upgrade screen | **Yes, always available** | Costs nothing, catches intent |
| Time-boxed offer after first value | **Yes** | Live Activity countdown — but honour the expiry |

### The Urgency Layer

Use time-limited offers to create conversion pressure:
- "Premium free for 24 hours if you share now"
- Live Activity countdown on lock screen showing offer expiration
- Discreet in-app timer that creates FOMO without being aggressive
- The timer should feel like a bonus opportunity, not a pressure tactic

---

## 3. Retention Mechanics

### The ~7 opens rule

A new app gets roughly **7 opens** to prove itself before the user quietly stops opening it. Every
one of those opens needs a reason to exist. Map them explicitly:

- **Open 1** — the aha (≤3 seconds)
- **Opens 2–3** — notification-driven, personal, emotional ("someone said…", "your photo was viewed")
- **Opens 4–5** — social obligation (someone is waiting on you)
- **Opens 6–7** — the habit is forming, or it isn't going to

If you can't name what pulls the user back on open 4, you have a demo, not a product.

### Content Scarcity

Deliberately limit the amount of content/interactions per day to create habitual return:

**tbh/Gas approach:**
- Only 4 poll questions unlocked per day
- Polls disappear after 24 hours
- Users feel pressure to vote NOW or miss out
- Creates a daily habit: open app → answer polls → check results

**Why scarcity works:**
- Prevents content fatigue (users don't binge and burn out)
- Creates anticipation (looking forward to tomorrow's polls)
- Drives daily return visits (time-limited content)
- Turns the app into a ritual, not a binge

### Notification-Driven Re-engagement

Push notifications are dopamine delivery vehicles. Every notification should:
1. Deliver positive emotional value ("Someone just said you're amazing")
2. Create curiosity ("A new poll about you is live")
3. Arrive at the right time (not 3 AM, not during school/work hours — peak engagement windows)
4. Be actionable (tapping should lead directly to the relevant content)

**Anti-patterns:**
- "You haven't opened [app] in 3 days" — guilt-based, ineffective, increases uninstalls
- Generic marketing pushes — feel corporate, reduce trust
- Too frequent — more than 3-5/day causes notification fatigue and disabling
- Misleading notifications — destroy trust permanently

### Streak Mechanics

- Daily streak counters reward consistent usage
- Loss aversion (breaking a streak) is a powerful motivator
- Display streaks prominently but don't punish breaks too harshly
- Allow "streak freezes" as a premium feature (monetises the retention mechanic)

### Social Obligation Loops

When the product creates interpersonal obligations, retention is natural:
- "3 friends sent you compliments — respond by voting in their polls"
- Users return not because of the app, but because of their friends
- This converts app-loyalty into social-loyalty (much stickier)

---

## 4. The Retention Cliff and How to Fight It

### The Problem

Consumer social apps with a single novel mechanic burn bright and fade fast. The initial
dopamine hit wears off. The novelty fades. Users churned from tbh and Gas after weeks/months.

### Why Bier's Apps Hit the Cliff

- Single mechanic (anonymous compliment polls) has a ceiling of novelty
- Once you've received enough compliments, the curiosity gap closes
- The experience doesn't evolve or deepen over time
- Post-acquisition, the small team culture that enabled rapid iteration was absorbed by
  large company processes

### Strategies for Fighting the Cliff

**1. Evolve the core loop:**
- Add new interaction types over time (new poll formats, new content types)
- Introduce challenges, events, or themed periods
- Let the community shape the direction (user-generated poll questions)

**2. Deepen social connections:**
- Move from anonymous to semi-anonymous to known interactions over time
- Create group dynamics (friend groups, teams, classes)
- Enable direct messaging or deeper interactions between matched users

**3. Foster community identity:**
- School/group leaderboards
- Community milestones ("Your school has sent 10,000 compliments!")
- Shared rituals and traditions within the app
- User-generated content that becomes community culture

**4. Layer new value propositions:**
- Start with polls → add direct messaging → add content sharing
- Each layer addresses a different need (validation → connection → expression)
- The core mechanic is the hook; layers are what create a daily habit

**5. Create status systems:**
- Visible levels or badges based on engagement
- Premium status indicators
- "Founding member" or "Day 1" badges for early adopters
- Status should be VISIBLE to others (social motivation)

### Bier's Counter-Strategy: Sell at Peak

Bier's actual approach to the retention cliff: don't fight it. Sell the company while charts
are still high. This is a legitimate strategy (he's done it twice for $30M+ combined).
Building durable retention in social apps is a "black swan event."

---

## 5. Push Notification Strategy

### The Notification as Product

In Bier's framework, the push notification IS the product for many users. They don't open
the app proactively — the notification pulls them in. Design accordingly.

### Notification Types (ranked by effectiveness)

1. **Personal validation:** "Someone said you're the funniest person they know" — highest
   open rates, most emotional impact
2. **Curiosity triggers:** "A new poll about you is live" — creates urgency
3. **Social proof:** "5 of your friends just voted" — FOMO + activity signal
4. **Progress updates:** "You're 1 share away from unlocking premium" — completion drive
5. **Milestone celebrations:** "You've received 50 compliments!" — positive reinforcement

### Timing Strategy

**For teen audiences:**
- Peak: 3-5 PM (after school), 7-9 PM (evening social time)
- Dead zones: during school hours, after 10 PM
- Weekends: more flexible, but avoid early morning

**For adult audiences:**
- Peak: Lunch (12-1 PM), Evening commute (5-6 PM), Post-dinner (8-9 PM)
- Dead zones: during typical work meetings (10 AM - 12 PM), after 10 PM

### Notification Volume Rules

- **Day 1-3:** Higher frequency acceptable (user is in discovery mode)
- **Day 4-14:** Reduce to 2-3 per day, focused on highest-value triggers
- **Day 15+:** Only send when there's genuine personal value to deliver
- **Always:** Let users control notification preferences granularly

### Rich Notifications

iOS supports rich notifications with images, actions, and previews:
- Include a preview of the content (e.g., the poll question, blurred hint of who sent a compliment)
- Add action buttons that let users respond without opening the app
- Use rich media to increase visual appeal in the notification tray
- Rich notifications have 2-3x higher tap-through rates than text-only
