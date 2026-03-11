# iOS Platform Hacks & App Store Optimisation — Deep Reference

## Table of Contents
1. Underused iOS APIs for Growth
2. App Store Page Optimisation
3. Permission Flow Hacks
4. Platform Risk Management

---

## 1. Underused iOS APIs for Growth

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

## 2. App Store Page Optimisation

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

## 3. Permission Flow Hacks

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

## 4. Platform Risk Management

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
