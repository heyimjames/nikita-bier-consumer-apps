# Viral Loops & Shareability Mechanics — Deep Reference

> Expands `SKILL.md` §6 (Viral Loop). `SKILL.md` is the source of truth — if anything here
> contradicts it, `SKILL.md` wins. Run the §0 intake first, and tag every recommendation
> **[Network] / [Utility] / [Universal]** — a Utility with a 30-year-old audience should ignore most
> of this file and read the Death Clock artefact play in `SKILL.md` §11 instead.

**Targets:** K > 1 · loop completes in **hours**, not days · first share prompt **≤60 seconds** into
the first session.

## Table of Contents
1. The Anatomy of a Bier Viral Loop
2. K-Factor Engineering
3. Share Mechanic Patterns (with implementation notes)
4. Anti-Patterns to Avoid
5. Case Studies: tbh, Gas, Explode

---

## 1. The Anatomy of a Bier Viral Loop

A Bier-style viral loop has five stages. Each must flow into the next without friction:

**Stage 1: Value Delivery**
The user receives genuine value — a compliment, a result, a piece of content. This is not
optional. If the first moment isn't emotionally rewarding, the loop dies here.

**Stage 2: Curiosity or Completion Gap**
The user wants MORE of what they just got. This desire is the fuel. Examples:
- "Who said I was the best dressed?" (curiosity)
- "Share 3 photos to unlock premium" (completion)
- "Invite 3 friends to skip the waitlist" (access)

**Stage 3: Invitation as the Bridge**
The only way to close the gap is to invite someone. Critically: the invite must feel like a
natural action, not a chore. The user is sharing something THEY want to share, not doing the
app a favour.

**Stage 4: Recipient Value Without Download**
The invited person receives some value or intrigue before installing. They see a preview,
a compliment notification, a teaser. This is the hook. If the invite is just "download this
app" with no context, conversion plummets.

**Stage 5: Recipient Download & Loop Restart**
The recipient installs, experiences Stage 1, and the loop restarts.

### Critical Metric: Time Through Loop

The faster a user moves from Stage 1 back to Stage 1 (via a new user), the faster you grow.
Bier optimises for loops that complete in HOURS, not days or weeks.

---

## 2. K-Factor Engineering

**K-Factor = (invitations per user) × (conversion rate per invitation)**

To achieve viral growth, K > 1. Every user, on average, must bring in more than one new user.

### Levers to Increase K-Factor

**Increase invitations per user:**
- Make inviting part of the core experience (not a separate "invite friends" button)
- Use contact list access to pre-populate invite targets
- Gate premium features behind invite counts
- Create natural share moments throughout the session

**Increase conversion per invitation:**
- Ensure the invitation carries context (not just a link)
- Show the recipient what they're missing (the curiosity gap)
- Let recipients experience value before download (web preview, iMessage app)
- Social proof: "15 of your friends are already here"

### K-Factor by Audience Age (Bier's data)

| Age | Relative Invite Rate |
|-----|---------------------|
| 13 | 100% (baseline) |
| 14 | ~80% |
| 15 | ~64% |
| 16 | ~51% |
| 17 | ~41% |
| 18 | ~33% |
| 22+ | Negligible organic invites |

This is why Bier targets teens first. The K-factor is structurally higher.

**The consequence, stated plainly:** if your audience is 22+, you do not have a Network app. You have
a Utility that needs an ad budget — expect to buy every user. Reposition to Hybrid (solo value, social
artefact) or accept paid acquisition. See `SKILL.md` §2 for the shape comparison and §11 for the
Death Clock play, which is how a single-player utility for older users got its CAC down to pennies
without a social graph.

---

## 3. Share Mechanic Patterns

### Pattern A: The Curiosity Gap Share

**How it works:** User receives partial information. To reveal the rest, they must engage
friends or pay.

**Implementation:**
- Deliver a compelling but incomplete notification ("Someone thinks you're...")
- Make the "reveal" action require inviting friends or purchasing premium
- The share itself should carry the curiosity gap forward to the recipient

**Best for:** Social apps, Q&A apps, anonymous feedback apps

### Pattern B: The Completion Gate

**How it works:** User progresses toward a reward. Final steps require sharing.

**Implementation:**
- Show clear progress (e.g., "Share with 3 friends to unlock" → "1 of 3")
- **Time-box it to the first session.** Explode gates on **3 sends within ~1 hour**. This is
  deliberate: after session one, the probability a user ever invites anyone collapses
- Make the reward genuinely valuable (premium access, exclusive content)
- Auto-transition the reward into a paid conversion (Explode: **free month → annual subscription
  trial**, automatically, with clear cancellation)
- Use a Live Activity countdown to carry urgency outside the app — **behind a server-side flag**,
  because promotional Live Activities are a grey area
- **Honour the expiry.** Explode's offer really does disappear after the hour. A timer that resets
  trains users to ignore every timer you ever show them

**Best for:** Any app with a freemium model

### Pattern C: Content-as-Distribution

**How it works:** The core content users create/consume is inherently shareable to other networks.

**Implementation:**
- Every piece of content should have a native share action (1 tap)
- Content must look good when shared to Instagram Stories, TikTok, iMessage
- Include subtle app branding on shared content (watermark, attribution)
- The shared content should be a complete experience for viewers (not just an ad)

**Best for:** Creative tools, social apps, fitness/progress trackers

### Pattern D: Mutual Benefit Sharing

**How it works:** Both the sharer and recipient get something valuable.

**Implementation:**
- "Give a friend 1 month free, get 1 month free"
- Make the referral feel like a gift, not a sales pitch
- Track and display referral impact ("You've helped 5 friends join")

**Best for:** Subscription apps, utility apps

---

## 4. Anti-Patterns to Avoid

### "Spotify Wrapped Syndrome"
Annual or one-off share moments that create phantom validation. You might top the charts
for a day, but it doesn't mean your core loop is viral. True viral growth requires
HIGH-FREQUENCY sharing of your core content to other networks.

### The Disconnected Invite Button
A standalone "Invite Friends" screen buried in settings. Nobody uses these. Invitations
must be woven into the core experience.

### Spam Invites
Sending messages on behalf of users without explicit consent. This is both unethical and
increasingly illegal. Bier learned this the hard way — server-sent SMS invites were shut
down by regulation, forcing a redesign for Gas.

### Over-Gamifying Invites
If inviting feels like a chore or a game mechanic divorced from the core value, users will
resent it. The invite must feel natural and desirable.

### Ignoring the Recipient Experience
If the person receiving the invite sees a generic "download this app" message, conversion
will be terrible. The invite must carry context, intrigue, and ideally a preview of value.

---

## 5. Case Studies

### tbh (2017) — Sold to Facebook for ~$30M in 9 weeks
- **Core loop:** Anonymous compliment polls in high schools
- **Viral mechanic:** Users chose friends from their contact list to answer polls about.
  Selected friends got notifications that someone said something nice.
- **Share channel:** Snapchat messages and Twilio SMS invites
- **K-factor driver:** You needed friends on the app for polls to be interesting
- **Peak:** 360,000 downloads/day, 5M users in 2 months
- **Key insight:** Only positive interactions. No negativity, no bullying vector.

### Gas (2022) — Sold to Discord
- **Core loop:** Same as tbh, rebuilt from scratch with new growth systems
- **Viral mechanic:** "God Mode" ($6.99/week) — hints at who sent compliments. Also: invite
  friends to skip the waitlist.
- **Share channel:** Device-sent SMS (regulation change from tbh era)
- **Revenue:** ~$7M from God Mode in 3 months
- **Key insight:** Monetisation aligned with the curiosity gap. Payment was the alternative
  to inviting — both closed the same loop.

### Explode (2025) — iMessage disappearing photos
- **Core loop:** Send ephemeral photos/texts via iMessage
- **Viral mechanic:** Only the sender needs the app; recipients view via App Clip with no install and
  screenshots blocked. **3 sends within ~1 hour → 1 month premium free → auto-converts to an annual
  subscription trial.**
- **Platform exploitation:** Live Activity countdown for urgency (fires on backgrounding, and the
  offer genuinely expires), PiP to survive the iMessage-extension setup step, App Clips for recipient
  value, "Tap Get Inc." developer account name for ASO
- **Pricing:** Explode+ at ~$39.99/year or $7.99/month — screenshot alerts, screenshot blocking,
  replays, post-send photo locking
- **Key insight:** Asymmetric install. The sender's content acts as marketing to every recipient, who
  then wants to send their own.
- **But it failed, and the reason matters:** ~20K downloads, a one-day spike then a sharp dip. Bier
  posted a post-mortem agreeing the "Snapchat replacement" positioning was the problem — defining
  yourself against an incumbent caps you at that incumbent's dissatisfied users. **Steal the funnel
  (`SKILL.md` §8), not the positioning.**
