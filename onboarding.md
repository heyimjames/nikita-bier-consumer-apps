# Onboarding & First-Session UX — Deep Reference

> Expands `SKILL.md` §4 (Onboarding & Activation) and §5 (Permissions). `SKILL.md` is the source of
> truth — if anything here contradicts it, `SKILL.md` wins. Run the §0 intake before giving any of
> this advice, and tag every recommendation **[Network] / [Utility] / [Universal]**.

**The three numbers this file serves:** aha ≤3 seconds · first share prompt ≤60 seconds ·
activation ≥40% (install → first meaningful action).

## Table of Contents
1. The Inverted Time to Value
2. Permission Flow Design
3. Screen-by-Screen Onboarding Architecture
4. The Explode Onboarding Funnel (worked example)
5. The Onboarding-to-Viral Bridge
6. Common Onboarding Killers

---

## 1. The Inverted Time to Value

Traditional apps: User signs up → explores → eventually finds value.
Bier approach: User opens app → immediately receives value → THEN signs up.

### Principles

- **Show, don't explain.** If you need to explain what your app does during onboarding,
  the app design has failed.
- **Deliver the "aha moment" before asking for anything.** The user should understand
  the value proposition from the first screen — ideally through experiencing it, not reading
  about it.
- **Pre-populate with real data.** Don't show an empty state. Show what the experience
  looks like when it's working (real polls, real compliments, real content from the user's
  network if possible).

### The Activation Benchmark

Bier targets 40%+ activation rates from install to first meaningful action. If you're below
this, your onboarding has too much friction. Every percentage point of activation rate
improvement compounds through your viral loop.

---

## 2. Permission Flow Design

### The Permission Stack — ask in this order, never reorder

| Order | Permission | When | Frame | Expected | If denied |
|---|---|---|---|---|---|
| 1 | **Notifications** | Immediately, pre-aha | "Get notified when a friend ___" | High with soft-ask | Continue; re-ask after first social event |
| 2 | **Contacts** | After first value, never before | "Find your friends already here" — show a count first | ~65% on iOS 18+ (higher teen, lower adult) | Community code / QR / deep link |
| 3 | **Camera** | At the moment of first use | Core to the experience; preview the UI | High if contextual | Explain necessity, path to Settings |
| 4 | **Location** | **Last, and only if genuinely required** | A specific benefit, never "improve your experience" | Low | Ship without it |

Location on first launch is the single fastest way to get deleted. Camera is asked at the moment of
use, not upfront — Explode puts its camera soft-ask in onboarding only because the camera *is* the
home screen.

### Permission Flow Best Practices

- **Pre-permission screens (the soft-ask):** Always show a custom screen explaining WHY before
  triggering the system dialog. This is worth **+20–30% approval** across the flow. A "Not Now" on
  YOUR screen costs nothing — the system prompt is unspent and you can ask again. A "Don't Allow" on
  the SYSTEM screen is permanent and only reversible in Settings. Users who clear your soft-ask have
  already committed mentally: **system approval often runs 80%+**.
- **"Why do you need this?" links:** Provide a clear, honest explanation. Users who
  understand the reason approve more often.
- **Animated guidance:** Use "Tap Here" chevrons and highlight animations to direct
  attention at critical permission moments.
- **Graceful degradation:** If a permission is denied, don't dead-end. Offer an alternative
  path or a "Not Now" that lets them continue.
- **Trust signals:** Pastel colours, clean Apple-inspired UI, real photos of people using
  the app — all increase permission approval rates.

### iOS 18+ Contact Access Strategy

The new contact permission flow is significantly more restrictive. Mitigation strategies:
- **Community codes:** Let users enter a school/group code instead of sharing contacts
- **QR code invites:** Quick in-person sharing without contact access
- **Deep links with context:** Share links that carry identity/group information
- **Phone number matching:** Ask for the user's own number, match against others who've
  shared theirs (requires less permission)

---

## 3. Screen-by-Screen Onboarding Architecture

**Hard ceiling: ~6 screens.** If you have more than six, delete until you don't. Every form field
beyond phone + first name + last name costs **5–10% of completion**.

### The Bier Onboarding Sequence (generalised)

```
Screen 1: Welcome / Value Demonstration
├── Show a real photo of people using the app (not stock illustrations)
├── One sentence explaining the value proposition
├── Single CTA button
└── NO text-heavy explanations

Screen 2: Account Creation
├── Phone number (SMS verification — iOS auto-fills)
├── Name + basic profile
├── Absolute minimum fields
└── Every field must justify its existence for the core experience

Screen 3: Permission Requests (stacked)
├── Notifications → pre-permission screen → system dialog
├── Contacts → pre-permission screen → system dialog
├── Camera (if needed) → pre-permission screen → system dialog
└── Progress indicator: "Step 2 of 3"

Screen 4: Social Graph / First Connection
├── Show friends already on the app
├── Or: enter a community code / scan QR
├── Or: browse content that demonstrates value
└── The user should see their network populated

Screen 5: First Value Moment
├── Immediately engage with the core loop
├── First poll, first send, first interaction
├── This is where the viral loop begins
└── Transition to the viral/share prompt while energy is high

Screen 6: Viral Bridge (the share/invite prompt)
├── "Get premium free: share with 3 friends"
├── Or: "Invite friends to make [app] better"
├── Clear progress tracking (1 of 3 shared)
└── This should feel like a BONUS, not a gate
```

### Handling Steps That Leave Your App

When onboarding requires actions in iOS Settings or other apps (e.g., enabling iMessage
extensions), use:
- **Picture-in-Picture overlay:** Keep your app visible while the user navigates Settings
- **Clear progress tracking:** "Almost done — just one more step"
- **"Not Now" escape:** For non-critical steps, always offer a skip option
- **Return detection:** When the user comes back, acknowledge completion and celebrate

---

## 4. The Explode Onboarding Funnel (worked example)

The most complete public Bier funnel. Full teardown including product chrome, the steal checklist,
and the do-not-cargo-cult list lives in `SKILL.md` §8 — this is the onboarding-specific slice.

| # | Step | What Explode does | Copy this? |
|---|---|---|---|
| 1 | Notification permission | A **faux notification prompt** styled like the real thing, then the real system Allow | The soft-ask yes; the *fake* dialog no — it's a dark pattern and the honest soft-ask gets the same lift |
| 2 | Welcome | Authentic photo of two real friends (the actual ICP) + one line of copy | Yes. Real ICP photo, one sentence, one CTA. Never stock illustration |
| 3 | Camera soft-ask | Pre-permission screen before the system camera dialog | Yes — soft-ask every permission |
| 4 | Signup | **Phone, first name, last name.** No email, no password, no account creation | Yes. This is your field-count floor |
| 5 | iMessage setup | Steps **previewed upfront**, **progress indicator**, **"Not Now"** escape, **PiP video guidance** that stays visible inside Messages, **"Return to Explode"** button in the extension | Yes — stack all four whenever a step leaves your app |
| 6 | Camera home | Lands directly on the camera; core action is **one tap** | Yes. Land on the core action, not a feed |
| 7 | Share gate | **3 sends within ~1 hour** → 1 month premium free → **auto-transitions to annual trial** | Yes. Time-box to session 1 |
| 8 | Recipient experience | **App Clip** — real value, no install. Screenshots blocked. Clear install CTA | Yes. Value before the install tax |
| 9 | On backgrounding | **Live Activity countdown** on lock screen / Dynamic Island: "send 2 more photos" | Yes, but **behind a server-side flag** — promotional Live Activities are a grey area |
| 10 | Expiry | Wait the hour and the offer is **genuinely gone** | Yes. If you show a timer, honour it |

**Step 5 is the lesson.** The iMessage setup was Explode's single biggest drop-off point — any step
that forces the user out of your app is a fragment, and fragments raise failure odds by roughly 50%
each. Explode's response was to stack four separate friction-killers on one screen. Do the same.

**Step 7 is the other lesson.** The share gate is time-boxed to roughly one hour because the first
session is the only session where users reliably invite anyone. After session one, the probability a
user ever invites someone collapses.

---

## 5. The Onboarding-to-Viral Bridge

The transition from "new user" to "user who's invited someone" is the most critical
conversion in your entire funnel. Bier designs onboarding to flow directly into the
first share action.

### The Bridge Pattern

```
User completes onboarding
→ Immediately experiences first value moment (compliment, content, etc.)
→ Is prompted to share while emotional response is high
→ Share is framed as getting MORE of what they just experienced
→ Share mechanic is 1-2 taps maximum
```

### Timing Matters

The first share prompt should happen within the first 60 seconds of the app experience.
Not in a popup. Not in a modal. Woven into the natural flow of the first session.

After the first session, the likelihood of a user ever inviting someone drops dramatically.
Front-load the viral moment.

---

## 6. Common Onboarding Killers

### The Email Signup
SMS verification outperforms email for mobile by a wide margin. iOS auto-fills SMS codes;
email requires app-switching, finding the email, copying the code. Every extra step loses
10-20% of users.

### The Feature Tour
Carousel slides explaining features are a signal that your UI is too complex. If you need
a tour, redesign the interface. Make it so obvious that even a distracted, one-handed user
on a bus can figure it out.

### The Empty State
Launching into an empty feed, empty inbox, or blank screen after onboarding is devastating.
Pre-populate with content, suggested connections, or sample experiences.

### The Premature Paywall
Showing a subscription screen before the user has experienced value. Always let the user
taste the core experience first.

### Too Many Fields
Every form field you add to signup reduces completion rate by 5-10%. Collect only what's
essential for the core experience. Everything else can be gathered progressively.

### The Desktop Mindset
Designing flows that assume a focused, seated user with a mouse and large screen. Mobile
users are distracted, one-handed, and impatient. Design accordingly.
