# Onboarding & First-Session UX — Deep Reference

## Table of Contents
1. The Inverted Time to Value
2. Permission Flow Design
3. Screen-by-Screen Onboarding Architecture
4. The Onboarding-to-Viral Bridge
5. Common Onboarding Killers

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

### The Permission Stack (in order of friction)

1. **Notifications** — Ask early, frame as "get alerts when friends interact with you."
   Use a pre-permission screen with a clear value prop BEFORE the iOS system dialog.
2. **Contacts** — Frame as "find friends already here." Show the number of friends found
   IMMEDIATELY after granting. iOS 18+: expect ~65% approval. Plan alternatives.
3. **Camera** — Frame as core to the experience. If denied, the app should still be usable
   (or clearly explain why it's essential). Use Apple-style UI to build trust.
4. **Location** — Only ask if genuinely needed. Never ask on first launch without context.

### Permission Flow Best Practices

- **Pre-permission screens:** Always show a custom screen explaining WHY before triggering
  the system dialog. This increases approval rates by 20-30%.
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

## 4. The Onboarding-to-Viral Bridge

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

## 5. Common Onboarding Killers

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
