# iOS Platform Hacks & App Store Optimisation — Deep Reference

> Expands `SKILL.md` §7 (iOS Surfaces) and §8 (Explode Teardown). `SKILL.md` is the source of truth —
> if anything here contradicts it, `SKILL.md` wins. Run the §0 intake first and tag every
> recommendation **[Network] / [Utility] / [Universal]**.

## Table of Contents
1. Surface Selection: Use-When and Risk
2. Underused iOS APIs for Growth
3. The Explode Stack (worked example)
4. App Store Page Optimisation
5. Permission Flow Hacks
6. Platform Risk Management

---

## 1. Surface Selection: Use-When and Risk

Don't adopt a surface because it's clever. Adopt it because your loop needs it. This table is the
short version of `SKILL.md` §7.

| Surface | Use it when | Concrete play | Risk | Mitigation |
|---|---|---|---|---|
| **iMessage extension** | Core action is send-to-a-specific-friend | Asymmetric install: only the sender needs the app | Setup is a fragment — real drop-off | Preview + progress + "Not Now" + PiP & return button |
| **App Clips** | Recipient needs value before installing | Recipient hits the **aha in <10s**, no install | Limited discovery | Pair with iMessage/link distribution |
| **Live Activities** | You have a genuinely time-boxed offer | Countdown on lock screen / Dynamic Island | **Grey area** — promotional use isn't the intended purpose | **Server-side feature flag** + push/in-app fallback |
| **Picture-in-Picture** | A step forces the user out of your app | Guidance video stays visible in Settings/Messages | Minor | Pair with return-detection |
| **Widgets / Lock Screen** | You need ambient daily presence | Streaks, progress, teasers; deep-link on tap | Low | — |
| **Contacts** | [Network] You need an instant social graph | Show friend count *before* asking | ~65% approval iOS 18+, declining | Community codes, QR, deep links |
| **SharePlay** | Co-use is the value | Multiplayer inside FaceTime | Low adoption | Don't build a business on it |
| **Siri Shortcuts / Spotlight** | Habit formation is the retention play | Voice/Spotlight triggers | Low | — |

**Rule:** if a surface is grey-area (Live Activities for promotion, aggressive ASO naming), it must
be **toggleable server-side** so compliance is a config change, not an App Store review cycle.

---

## 2. Underused iOS APIs for Growth

### Live Activities (iOS 16.1+)

**Standard use:** Real-time updates on the lock screen (sports scores, delivery tracking).
**Bier use:** Create urgency for promotional offers directly on the lock screen.

**Explode example:** A Live Activity widget announces that the premium offer (unlocked after
sharing 3 photos) is about to expire. This creates urgency without requiring the user to
open the app.

**Risks:** Apple's guidelines don't intend Live Activities for promotional purposes. This is
a grey area that may be shut down. Use while it works, but have a fallback.

**Growth applications:**
- Countdown timers for limited offers
- Real-time social notifications ("3 friends just joined")
- Progress trackers for invite/share goals
- Event countdowns (launch day, new feature drops)

### Picture-in-Picture (PiP)

**Standard use:** Video playback while using other apps.
**Bier use:** Guide users through multi-step setup processes that require leaving your app.

**Explode example:** When users need to enable the iMessage extension (which requires going
to Settings), a PiP overlay from Explode stays visible, guiding them through each step.
This prevents the "left the app and forgot" dropout.

**Growth applications:**
- Onboarding steps that require system settings changes
- Tutorial overlays during external setup flows
- Persistent branded presence during referral flows

### iMessage Apps / Extensions

**Standard use:** Stickers, simple games within Messages.
**Bier use:** Full product distribution through the world's most used messaging platform.

**Explode example:** The core product IS an iMessage extension. Only the sender needs the app
installed — recipients view ephemeral photos natively in their Messages app. Every message
sent is an organic advertisement for the app.

**Growth applications:**
- Asymmetric install: sender needs app, recipient doesn't (but will want to)
- Each message is a micro-advertisement
- Zero-friction sharing — already in the conversation
- Content previews that tease full app experience

### App Clips

**Use for growth:** Let users experience your app's core value without a full install.
- Share App Clip links in messages, QR codes, NFC tags
- The App Clip should deliver your "aha moment" in under 10 seconds
- Include a clear path to full app install after value is demonstrated
- Available via links, QR codes, NFC, Safari, Maps

### Widgets (Home Screen & Lock Screen)

- Persistent presence on the user's most-viewed screen
- Use for: streaks, progress, social notifications, content teasers
- Widget taps deep-link into the app at the relevant content
- Lock screen widgets (iOS 16+) are prime real estate for habit formation

### Other Underexplored Features

| Feature | Growth Potential |
|---|---|
| **SharePlay** | Social experiences within FaceTime calls — co-usage drives adoption |
| **Siri Shortcuts** | Voice-triggered habits; appears in Spotlight suggestions |
| **Apple Wallet Passes** | Gamified loyalty cards, status passes, event tickets |
| **Focus Filters** | App content that adapts to Focus modes (work/personal) |
| **StandBy Mode** | Widgets on charging iPhone — ambient presence |
| **Interactive Widgets (iOS 17+)** | Perform actions without opening the app |
| **Journal Suggestions API** | Surface your app's content in Apple's Journal app |
| **Contact Posters** | Custom contact cards that showcase app-generated content |

---

## 3. The Explode Stack (worked example)

Explode (Jan 2025) used four surfaces in one funnel. It did **not** win — ~20K downloads, a one-day
spike then a sharp dip — because its "Snapchat replacement" positioning capped the market. **Steal
the stack, not the positioning.** Full funnel, steal checklist, and do-not-cargo-cult list:
`SKILL.md` §8.

| Surface | How Explode used it |
|---|---|
| **iMessage extension** | The product itself. Only the sender needs the app — every message sent is a free ad. Setup was previewed upfront with progress, a "Not Now", PiP guidance, and a "Return to Explode" button |
| **PiP** | A guidance video stayed visible while the user was inside Messages adding the extension — killing the "left the app and forgot" dropout on the funnel's worst step |
| **App Clips** | Recipients viewed disappearing photos with **no install**, screenshots blocked, then a clear CTA to get the app |
| **Live Activities** | On backgrounding, a countdown appeared: "send 2 more photos" to unlock the free month. The offer **genuinely expired** after ~1 hour |

**Product chrome worth copying:** camera-first home with near-zero navigation; native iOS toggles and
controls throughout (familiarity buys trust exactly where it converts — permissions and payment);
signup limited to phone + first + last.

**Pricing:** Explode+ at **~$39.99/year or $7.99/month**, unlocking screenshot alerts, screenshot
blocking, replaying sent photos, and locking photo viewing after send — all features that only become
meaningful *after* you've sent something. The paywall sells depth on an action already taken, never
access to the action itself.

**ASO:** the developer account was named **"Tap Get Inc."**, so the App Store renders "Tap Get" beside
the download button.

**Do not cargo-cult:** the Live Activity promo is a grey area (flag it server-side); the "spite app"
narrative backfired and capped the market; skip the iMessage extension entirely if your core action
isn't send-to-a-specific-friend, because the setup step is a genuine fragment.

---

## 4. App Store Page Optimisation

### The Zero Ratings Problem

If your app has zero ratings, you're losing approximately 2/3 of potential conversions.
Social proof on the App Store page is the single highest-leverage ASO factor.

**How to get initial ratings:**
- Prompt for ratings AFTER a positive in-app moment (received a compliment, completed a goal)
- Use Apple's native SKStoreReviewController (appears as a system dialog — higher completion)
- Time the prompt for when the user has just experienced peak value
- Never prompt during onboarding or on first session
- Consider asking "Are you enjoying [app]?" first — only route to the rating prompt if yes

### Developer Account Name Hack

Bier named the Explode developer account "Tap Get Inc." In the App Store search results,
this displays as "Tap Get" right next to the download button, creating a subliminal CTA
that increases tap-through rate.

**How to apply:**
- Your developer account name appears in search results
- Choose a name that functions as a call-to-action or value prop
- Keep it short and action-oriented
- Test different names (you can update your developer account name)

### App Title & Subtitle

- Title should communicate what the app does in the fewest possible words
- Subtitle (30 chars max) should reinforce the value prop or add context
- Include high-value search keywords naturally
- The title can change once the user taps into the full listing — use this for a longer description

### Screenshot Strategy

- First screenshot must communicate the core value in one glance
- Show the app in use, not just the UI (real scenarios, real data)
- Include social proof elements (user counts, ratings, press logos)
- Demonstrate the "aha moment" visually
- Use text overlays sparingly — the visual should speak for itself

### App Preview Videos

- Auto-play in search results (powerful for attention capture)
- First 3 seconds must hook — show the product's best moment immediately
- Demonstrate the viral loop in action (someone receiving and sending)
- Keep it under 30 seconds
- No voiceover needed — make it visually self-explanatory

---

## 5. Permission Flow Hacks

### The Pre-Permission Pattern

Never trigger a system permission dialog cold. Always show a custom screen first:

```
Your Custom Screen (soft ask):
"[App] would like to send you notifications when
friends interact with you."

[Allow Notifications] ← Primary CTA
[Not Now] ← Secondary, de-emphasised

↓ If user taps Allow ↓

iOS System Dialog:
"[App] Would Like to Send You Notifications"
[Allow] [Don't Allow]
```

**Why this works:**
- If the user taps "Not Now" on your custom screen, you've saved the system permission
  for later (you can ask again)
- If the user taps "Allow," they've already mentally committed — system dialog approval
  rates jump to 80%+
- You can frame the value proposition in your own words, not Apple's generic copy

### Contact Permission Framing

Post-iOS 18, contact access is harder to get. Optimise the ask:
- Show a count of how many friends are already on the platform BEFORE asking for contacts
  (even if estimated: "Students from [school] are already here")
- Frame as "find your friends" not "access your contacts"
- Explain exactly what you will (and won't) do with the data
- Show that granting access leads to immediate value (their friend list populated)

### Camera Permission Design

- Use an Apple-native-looking interface for the permission screen
- Explain the camera is essential for the core experience
- Show what the camera experience looks like (preview of the UI)
- If denied, explain that the app needs camera access and provide a path to Settings

---

## 6. Platform Risk Management

### The SnapKit Lesson

Gas was removed from Snapchat's SnapKit platform after a meeting with Snap's CEO. A single
platform decision halted growth overnight. Lessons:

- Never depend on a single third-party platform for your core distribution
- Build redundant growth channels from day one
- Own your user relationships (email, phone number, push tokens)
- If a platform offers APIs for growth, use them but don't build solely on them

### OS Update Risk

Each iOS version can break existing growth mechanics:
- iOS 18 contact permission changes (~65% approval vs. higher previously)
- Potential Live Activities policy changes for promotional use
- App Tracking Transparency (iOS 14.5) already decimated ad-based acquisition

**Mitigation:**
- Monitor Apple Developer beta releases starting June (WWDC)
- Test every growth mechanic on each iOS beta immediately
- Maintain 2-3 alternative growth channels at all times
- Design growth loops that don't depend on any single API or permission

### App Store Review Risk

Apple's review process can reject apps using aggressive growth tactics. Bier's approach
involves pushing boundaries (Live Activities for promotions, developer name hacks) but
always maintaining a fallback:
- Have a "clean" version ready that passes review if your primary version is rejected
- Don't document grey-area tactics in your App Store description
- Build features that can be toggled via server-side flags (no app update needed to comply)
