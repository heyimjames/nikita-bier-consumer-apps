---
name: nikita-bier-consumer-apps
description: >
  A tactical growth-advisor skill that packages Nikita Bier's playbook for building viral consumer
  iOS/mobile apps. Runs a short intake, then gives specific, numbered, benchmarked recommendations on
  viral loops, onboarding and permission flows, activation, iOS surface exploitation (Live Activities,
  App Clips, iMessage, PiP), App Store conversion, paywall timing, monetisation, retention, and launch
  sequencing. Use this skill whenever the user is building, designing, reviewing, teardown-ing, or
  planning a consumer mobile app — social apps, utilities with a share moment, or anything chasing
  organic growth. Also trigger when the user mentions: viral growth, user acquisition without ads,
  K-factor, invite loops, onboarding funnels, activation rate, App Store conversion, consumer social,
  teen/Gen-Z audiences, cold start, shareability, App Clips, iMessage apps, Live Activities, or
  paywall placement. Even if the user just says "review my app idea" or "do an Explode-style
  teardown" — use this skill.
---

# The Nikita Bier Consumer App Playbook

A tactical playbook, not a philosophy deck. Every recommendation below carries a **when**, a **how
many**, a **what gates what**, and a **metric that tells you it worked**. If a piece of advice can't
be argued with, it isn't advice — cut it.

Derived from Bier's Lenny's Podcast appearance, his X threads, and public teardowns of tbh, Gas,
Explode, and Death Clock. Sources listed at the bottom.

---

## 0. INTAKE — ASK THIS FIRST. DO NOT SKIP.

**Never dump the playbook before running intake.** Advice for a Network app actively harms a Utility
app and vice versa. Ask these five questions, in one message, and wait for answers.

> 1. **Shape** — is this a **Network** app (value comes from other people being on it), a **Utility**
>    (value works alone, on first open, for one person), or a **Hybrid** (solo value, social
>    distribution)?
> 2. **Audience age band** — 13–17, 18–22, 23–34, or 35+? Give me the real median, not the deck.
> 3. **Core aha, one line** — "the user opens the app and within N seconds they ______." If you can't
>    say it in one sentence, that's the finding.
> 4. **Loop today** — what actually happens after a user gets value? Nothing / they share manually /
>    they invite to unlock something / the content itself carries the app to a new person?
> 5. **Ask type** — which do you want: idea validation, onboarding/activation audit, viral loop
>    design, monetisation & paywall, launch plan, retention, or an **Explode-style teardown**
>    (screen-by-screen funnel breakdown)?

### Intake shortcuts

- If the user gives you only a screenshot, a TestFlight link, or a URL: still ask Q1, Q2, Q5. You can
  infer Q3 and Q4 yourself and confirm your inference back to them.
- If the user refuses to answer or says "just tell me everything": pick the **most likely shape from
  their description**, state the assumption out loud in one line ("Assuming Hybrid, 18–22 — correct me
  if not"), and proceed. Do not stall.
- If the answers reveal the idea fails the Kill Test (§2), say so in the first paragraph of your
  response. Don't bury it.

### Tag every recommendation

Prefix each recommendation you give with its applicability. This is mandatory — it's how the user
knows what to ignore.

- **[Network]** — only worth doing if value requires other users
- **[Utility]** — only worth doing if the app works for one person alone
- **[Universal]** — do this regardless of shape

---

## 1. THE THREE AXIOMS

1. **Every tap is a miracle.** Each screen, field, and permission must earn its place or be deleted.
2. **The product IS the marketing.** If the share mechanic isn't in the core loop, you will buy every
   user forever.
3. **Consumer products live and die in the pixels.** Not the backend, not the deck.

---

## 2. APP SHAPE — PICK ONE, THEN FOLLOW ITS COLUMN

Most bad advice comes from applying Network tactics to a Utility. Find your column and stay in it.

| | **Network** | **Utility** | **Hybrid** |
|---|---|---|---|
| **Value source** | Other users on the app | Works alone, first open | Solo value + social artefact |
| **Examples** | tbh, Gas, BeReal | Death Clock (pre-rename), calculators | Explode, Locket, Death Clock (post-rename) |
| **Cold start** | Brutal — empty app is worthless | None — works on install | Mild — solo value carries you |
| **Primary growth lever** | Invite loop, K-factor | Paid ads, ASO, content | Shareable output artefact |
| **Target age** | 13–22 or don't bother | Any — 25–45 monetises best | 16–30 |
| **Aha target** | ≤3s, but needs ≥1 friend present | ≤3s, unconditional | ≤3s solo, share prompt ≤60s |
| **Launch shape** | Geofence one dense community, 40%/24h | Wide, ASO + content volume | Narrow test, then content volume |
| **Monetisation** | Curiosity unlock (God Mode) | Subscription on core function | Invite-OR-pay dual unlock |
| **Kill signal** | K < 1 after fixing invite friction | CAC > LTV with no content lever | Artefact isn't shared unprompted |
| **Realistic ceiling** | Winner-take-all or zero | Steady, ad-financed, sellable | High spike, hard retention |
| **If you're 23+ audience** | **Don't build Network.** Go Utility or Hybrid. | Fine | Fine |

### The Kill Test (run before writing code)

Four questions in sequence. Each must be **yes** for the next to matter.

1. **Latent demand?** Are people already doing this badly, with a workaround, today?
2. **Reach without ads?** Name the channel for the first 1,000 users.
3. **Will they invite?** Does sharing make it better *for the sharer*, not just the recipient?
4. **Monetise without killing the loop?** Is there a natural paywall that doesn't block the aha?

A "maybe" counts as a no. Stop and rethink.

### The fragment tax

Every additional thing that must be true — every conditional layer, every extra setup step, every
third-party dependency — raises your probability of failure by roughly **50% per fragment**. Four
fragments is the practical ceiling. Explode's iMessage-extension setup step was a whole fragment, and
it was the single biggest drop-off in the funnel — which is why it got PiP, a progress bar, a "Not
Now" escape, and a "Return to Explode" button, all for one step.

**Count your fragments before you build. If it's more than four, cut features until it isn't.**

---

## 3. AUDIENCE — THE INVITE ECONOMICS ARE FIXED, PLAN AROUND THEM

Bier's headline number: **invitations sent per user drop ~20% for every additional year of age from
13 to 18.** It compounds. This isn't a preference, it's arithmetic.

| Age | Relative invites/user | What it means for you | Your growth engine |
|---|---|---|---|
| 13 | 100% (baseline) | Highest K possible. Densest graphs (schools). | Organic invite loop |
| 14 | ~80% | Still explosive | Organic invite loop |
| 15 | ~64% | Still works | Organic invite loop |
| 16 | ~51% | Half the fuel of a 13yo | Invite loop + content |
| 17 | ~41% | Needs a strong curiosity gap to compensate | Invite loop + content |
| 18 | ~33% | One third of baseline | Content-led, invites assist |
| 19–21 | Declining, messaging volume peaks ~21 | Last window for a new comms channel | Content + shareable artefact |
| 22 | **The cut-off.** People largely stop adopting new social products. | Network apps stop working here | Hybrid or Utility only |
| 23+ | Negligible organic invites | **Expect to buy every user with ads.** | Paid + ASO + content volume |

### Consequences you must accept

- **[Network]** If your audience is 23+, you do not have a Network app. You have a Utility that
  needs an ad budget. Reposition now, not after the launch fails.
- **[Universal]** Teens see each other every day. That daily physical density — not the design — is
  the single biggest driver of viral spread. If your audience doesn't physically co-locate daily,
  your loop must complete via content, not invites.
- **[Universal]** Getting 7 adult friends to install anything on a reproducible basis is genuinely
  hard. Don't design a loop that assumes it.
- **[Utility]** Older audiences are worse at inviting and better at paying. Trade K for ARPU
  deliberately: charge more, earlier, and stop apologising for the paywall.

### The ~7 opens rule

A new app gets roughly **7 opens** to prove itself before the user quietly stops opening it. Every
one of those 7 needs a reason to exist — a notification worth tapping, new content, a social
obligation. Map opens 1 through 7 explicitly:

- Open 1: the aha (≤3s)
- Open 2–3: notification-driven, personal, emotional ("someone said…", "your photo was viewed")
- Open 4–5: social obligation (someone is waiting on you)
- Open 6–7: habit has to be forming, or it isn't going to

If you can't name what pulls the user back on open 4, you have a demo, not a product.

---

## 4. ONBOARDING & ACTIVATION — HARD NUMBERS

### The three benchmarks

| Metric | Target | How to measure | If you miss |
|---|---|---|---|
| **Time to aha** | **≤3 seconds** from first open | Stopwatch on a cold install, on a real phone | Cut screens until you hit it |
| **Viral bridge** | First share prompt **≤60 seconds** | Timestamp of share-sheet impression | Move the prompt earlier, not later |
| **Activation** | **≥40%** install → first meaningful action | Cohort funnel, day 0 | Onboarding has too much friction |

After the first session, the probability a user *ever* invites someone collapses. **Front-load the
viral moment.** There is no "we'll add invites in v2" — v2 is too late for the v1 cohort.

### The ~6 screen ceiling

Generalised max flow. If you have more than six, delete until you don't.

| # | Screen | Rules | Cost of getting it wrong |
|---|---|---|---|
| 1 | **Welcome / value demo** | Real photo of your actual ICP using the app. One sentence. One CTA. No carousel. | Dead on arrival |
| 2 | **Account** | Phone + SMS code. First name. Last name. **Nothing else.** | −5–10% completion *per extra field* |
| 3 | **Permissions** | Soft-ask → system dialog, in the order in §5. Progress indicator. | −20–30% approval without soft-ask |
| 4 | **Social graph / context** | Show friends found, or community code, or QR. Never an empty state. | Empty state = churn |
| 5 | **First value moment** | The aha. The core loop, live, with real data. | This is the product |
| 6 | **Viral bridge** | Share prompt framed as a bonus, with progress ("1 of 3"). Never a gate. | K stays under 1 |

### Fixed rules

- **[Universal] SMS > email.** iOS auto-fills the SMS code with no app-switching. Email means leaving
  your app, finding a message, copying a code, coming back. Each of those steps bleeds 10–20%.
- **[Universal] Every form field costs 5–10% of completion.** Phone, first name, last name is the
  floor Explode ships with. Justify every field beyond it or delete it.
- **[Universal] No feature tour.** If you're considering one, the UI has failed. Fix navigation,
  hierarchy, empty states, and copy instead — even at the cost of power users. You need users before
  you can have power users.
- **[Universal] No empty states, ever.** Pre-populate with real or representative content.
- **[Universal] "Not Now" on every non-critical step.** A hard gate converts a soft skip into an
  uninstall.
- **[Universal] Reframe the ask.** Paul Graham's move: not "would you like to use our product?" but
  "would you like to keep the thing you just made?" If onboarding *creates* something, completion
  jumps.

---

## 5. PERMISSIONS — ORDER, PATTERN, AND EXPECTED RATES

### Never trigger a system dialog cold

The soft-ask pattern, in full:

```
Your custom screen (soft-ask):
  "Get notified when a friend sends you a photo"
  [Turn On Notifications]   ← primary, full-width
  [Not Now]                 ← secondary, grey, small

  ↓ only if they tap the primary ↓

iOS system dialog:
  "[App] Would Like to Send You Notifications"
  [Allow] [Don't Allow]
```

**Why:** a "Not Now" on *your* screen costs nothing — the system prompt is still unspent and you can
ask again later. A "Don't Allow" on the *system* screen is permanent and only reversible via Settings.
Users who clear your soft-ask have already committed mentally: **system approval often runs 80%+**.
Across the flow, the soft-ask pattern is worth **+20–30% approval** versus a cold prompt.

### Order matters — ask in this sequence

| Order | Permission | When to ask | Frame it as | Expected | If denied |
|---|---|---|---|---|---|
| 1 | **Notifications** | Immediately, pre-aha | "Get notified when a friend ___" | High with soft-ask | Continue; re-ask after first social event |
| 2 | **Contacts** | After first value, never before | "Find your friends already here" — show a count first | **~65% on iOS 18+** (higher teen, lower adult) | Fall back to community code / QR / deep link |
| 3 | **Camera** | At the moment of first use, not before | Core to the experience; show a preview of the UI | High if contextual | Explain necessity, path to Settings |
| 4 | **Location** | **Last, and only if genuinely required** | Specific benefit, never "improve your experience" | Low | Ship without it |

### Rules

- **[Universal]** Show the *result* of granting immediately — friend list populated, count revealed.
  A permission with no visible payoff trains users to deny the next one.
- **[Universal]** Use Apple-native-looking UI and calm/pastel colour for sensitive asks. Trust
  signals measurably move approval.
- **[Network]** iOS 18+ broke contact-led growth. Build **at least two** of these before you need
  them: community/school codes, QR invites, deep links carrying group context, phone-number matching
  (asks less than full contact access).
- **[Universal]** Never ask for location on first launch. It is the single fastest way to get deleted.

---

## 6. VIRAL LOOP — FIVE STAGES, MEASURED

**K = (invites sent per user) × (conversion per invite). You need K > 1, and you need the loop to
complete in hours, not days.**

| Stage | What happens | Gate | Instrument it |
|---|---|---|---|
| 1. **Value** | User gets something emotionally rewarding | Must land ≤3s | % reaching first value |
| 2. **Gap** | User wants more — curiosity, completion, or access | Must be *unclosable* without others | % who engage the gap |
| 3. **Invite** | Only way to close the gap is bringing someone in | ≤2 taps, in-flow, never a settings screen | Invites sent per user |
| 4. **Recipient value pre-install** | Recipient gets intrigue or actual value *without* installing | This is the whole ballgame | Invite → view rate |
| 5. **Install & restart** | Recipient installs, hits stage 1 | ≤3s again | View → install rate |

**Time through loop is the metric nobody tracks and everybody should.** Optimise for hours.

### The four share patterns, and when each applies

| Pattern | Mechanic | Gate | Best for | Case |
|---|---|---|---|---|
| **Curiosity gap** | Partial info; reveal requires invite or pay | Identity of sender | [Network] anonymous/social feedback | Gas God Mode |
| **Completion gate** | Progress bar; final steps require shares | N shares in a time window | [Hybrid] freemium | Explode: 3 shares / ~1h |
| **Content-as-distribution** | The core artefact is inherently shareable off-platform | None — remove all friction | [Hybrid] [Utility] creative/result apps | Death Clock death-date |
| **Mutual benefit** | Both sides get something ("give a month, get a month") | Referral completion | [Utility] subscription apps | Standard SaaS referral |

### Anti-patterns — these do not work, stop proposing them

- **Spotify Wrapped syndrome** — an annual share moment. Phantom validation. True virality needs
  high-frequency sharing of your *core* content.
- **The settings-menu "Invite Friends" screen** — nobody has ever tapped this. Delete it.
- **Server-sent invites on the user's behalf** — unethical, and regulation already killed it (Gas had
  to rebuild the entire loop onto native device compose windows, testing nine variations before
  school-hopping worked again).
- **Over-gamified invites divorced from value** — users resent being made to work for you.
- **A bare "download this app" invite** — with no context or preview, conversion collapses.

---

## 7. iOS SURFACES — WHAT TO USE, WHEN, AND THE RISK

| Surface | Use it when | Concrete play | Risk | Mitigation |
|---|---|---|---|---|
| **iMessage extension** | Your core action is send-to-a-friend | **Asymmetric install:** only the sender needs the app. Every message is a free ad. | Setup is a fragment — biggest drop-off in the funnel | Progress UI + PiP + "Not Now" + "Return to App" button |
| **App Clips** | Recipient needs value before installing | Recipient hits the **aha in <10s** with no install; then a clear install CTA | Discovery is limited; App Clip must be genuinely useful | Pair with iMessage/link distribution |
| **Live Activities** | You have a genuinely time-boxed offer | Countdown for a share-unlock offer on lock screen / Dynamic Island | **Grey area.** Promotional use is not the intended purpose — Apple can shut it down | **Server-side feature flag** so you can disable without shipping an update. Have a fallback. |
| **Picture-in-Picture** | A step forces the user out of your app | Keep a guiding video overlay visible while they're in Settings/Messages | Minor; feels novel | Pair with return-detection and celebration |
| **Widgets / Lock Screen** | You need ambient daily presence | Streaks, progress, content teasers; deep-link on tap | Low | — |
| **Contacts** | [Network] You need an instant social graph | Show friend count *before* asking | ~65% approval iOS 18+, declining | Community codes, QR, deep links |
| **SharePlay** | Co-use is the value | Multiplayer inside FaceTime | Low adoption | Don't build a business on it |
| **Siri Shortcuts / Spotlight** | Habit formation is your retention play | Voice/Spotlight triggers | Low | — |
| **Push** | Always | Personal-validation copy, at peak windows only | Fatigue above 3–5/day | Granular user controls |

### App Store conversion

- **[Universal] Zero ratings costs you roughly two-thirds of your conversions.** This is the single
  highest-leverage ASO fix. Get ratings *before* you scale spend or launch.
  - Prompt via `SKStoreReviewController` **after a peak positive moment**, never in onboarding or the
    first session.
  - Gate it: ask "Enjoying [app]?" first, and only route yes-answers to the rating prompt.
- **[Universal] The developer-name hack.** Bier named Explode's developer account **"Tap Get Inc."**,
  so the App Store listing renders "Tap Get" next to the download button — a free subliminal CTA.
  Your developer name is editable. Use it.
- **[Universal] Title = value prop in the fewest possible words.** Not your brand story.
- **[Universal] Screenshot 1 must show the aha**, in use, with real data. App preview video must hook
  in 3 seconds, no voiceover, under 30 seconds.

---

## 8. EXPLODE TEARDOWN — THE MOST COMPLETE PUBLIC BIER FUNNEL

Explode (Jan 2025) is the highest-resolution public example of Bier building a funnel. Disappearing
photos/texts sent through iMessage, positioned openly as a "spite app" aimed at Snapchat. It did
**not** win — roughly 20K downloads, a one-day spike then a sharp dip, and Bier himself posted a
post-mortem agreeing the Snapchat-replacement positioning was the problem. **Steal the funnel, not
the positioning.**

### The funnel, step by step

| # | Step | What Explode does | Why it works | What to copy |
|---|---|---|---|---|
| 1 | **Notification permission** | A **faux notification prompt** shown first, styled like the real thing, then the real system Allow | Primes the tap pattern so the real dialog is muscle memory | The soft-ask, yes. The *fake* dialog is a dark pattern — use a clearly-yours soft-ask instead (§5) |
| 2 | **Welcome** | Authentic photo of two real friends (the actual ICP) + one line on what the app does | Visual proof beats explanation; shows *who it's for* | Real ICP photo, one sentence, one CTA. Never stock illustration |
| 3 | **Camera soft-ask** | Pre-permission screen before the system camera dialog | Same +20–30% logic as notifications | Soft-ask every permission, in §5 order |
| 4 | **Signup** | **Phone number, first name, last name. That's all.** No email, no password, no separate account creation | Every field costs 5–10% completion | This is your field-count floor. Beat it if you can |
| 5 | **iMessage setup** (the hard one) | "Add Explode to iMessage" — shown **upfront as a preview of the steps**, with a progress indicator, a **"Not Now"** escape, **PiP video guidance** that stays visible while the user is in Messages, and a **"Return to Explode"** button in the extension | This is the app's biggest drop-off point and it gets four separate friction-killers stacked on one screen | Whenever a step forces the user out of your app, stack all four: preview, progress, Not Now, PiP + return path |
| 6 | **Camera home** | Lands directly on the camera. Core action is **one tap** | The aha is the product, immediately | Land on the core action, not a feed or a dashboard |
| 7 | **The share gate** | Send photos to **3 people within ~1 hour** → unlock **1 month premium free** → which **auto-transitions into an annual subscription trial** | One mechanic drives distribution *and* monetisation. The hour window forces it into session 1 — where the only invites you'll ever get happen | The dual-unlock. Time-box it to the first session |
| 8 | **Recipient experience** | Recipient views via **App Clip** — real value, no install. Screenshots are **blocked**. Clear CTA to get the app | Asymmetric install: the sender's content is the ad. Recipients feel the product before paying the install tax | Give recipients genuine value with zero install, then a single obvious CTA |
| 9 | **Live Activity on close** | The moment you background the app, a **Live Activity countdown** appears on lock screen / Dynamic Island: "send 2 more photos", offer expiring | Urgency follows the user out of the app — the offer keeps selling while the app is closed | Powerful and grey. Ship it **behind a server-side flag** |
| 10 | **The offer really expires** | Wait the hour and the offer is genuinely gone | Real scarcity. Fake countdowns that reset train users to ignore you | If you show a timer, honour it |

### Product chrome

- **Minimal home screen** — camera-first, near-zero navigation. Nothing competes with the core action.
- **Native iOS toggles and controls** throughout — familiarity buys trust at exactly the moments
  (permissions, payment) where trust converts.
- **Explode+ pricing: ~$39.99/year or $7.99/month.** Paid unlocks screenshot alerts, screenshot
  blocking, replaying sent photos, and locking photo viewing after send — all features that are
  *only* meaningful once you've already sent something. The paywall sells depth on an action you've
  taken, never access to the action itself.
- **Developer account: "Tap Get Inc."** — renders as "Tap Get" beside the App Store download button.

### Steal checklist — 7 things to lift directly

1. **Cut signup to phone + first + last.** Delete every other field.
2. **Soft-ask before every system permission**, in the §5 order.
3. **Land on the core action** — camera, composer, whatever it is — not a feed or dashboard.
4. **Stack four friction-killers on any step that leaves your app**: step preview, progress
   indicator, "Not Now", and PiP guidance with an explicit return button.
5. **Time-box the share gate to the first session** (Explode: 3 shares, ~1 hour). This is the only
   session where users invite anyone.
6. **Chain the reward into the subscription** — free month → annual trial, automatically, with clear
   cancellation.
7. **Give recipients real value with no install** (App Clip / web preview), then one obvious CTA.

### Do not cargo-cult

- **Live Activities for promotions is a grey area.** Apple's guidelines don't intend them for
  marketing countdowns. Use it while it works, but put it behind a **server-side feature flag** so
  compliance is a config change, not an App Store review cycle. Have a non-Live-Activity fallback
  (push + in-app banner) ready.
- **The "spite app" narrative is optional and it backfired here.** Defining yourself as a
  replacement for an incumbent caps you at the incumbent's dissatisfied users — a small market.
  Explode's downloads spiked and collapsed for exactly this reason. Controversy buys a news cycle,
  not retention.
- **Skip the iMessage extension entirely if your core action isn't send-to-a-specific-friend.** The
  setup step is a genuine fragment with real drop-off. It only pays for itself when the asymmetric
  install (sender has the app, recipient doesn't) is the whole growth model.
- **The faux notification prompt is a dark pattern.** The soft-ask gets you the same lift honestly.

**Sources for this section:** [julianivaldy.com — Explode product
analysis](https://julianivaldy.com/explode-product-analysis-by-nikita-bier) ·
[retention.blog/p/explode](https://www.retention.blog/p/explode) · [TechCrunch, 15 Jan 2025 — Creator
of Gas and tbh makes an app for disappearing photos via
iMessage](https://techcrunch.com/2025/01/15/creator-of-gas-and-tbh-makes-an-app-for-disappearing-photos-via-imessage/)

---

## 9. MONETISATION — PAYWALL PLACEMENT IS THE WHOLE GAME

### When to show the paywall

| Moment | Show? | Why |
|---|---|---|
| During onboarding | **Never** | User has no value context. Kills activation outright |
| Before the aha | **Never** | You're charging for a promise |
| Mid-core-action | **Never** | Interrupting the thing they came for |
| Immediately after a peak emotional moment | **Yes** | "Someone said you're the best dressed — want a hint who?" |
| At the natural edge of the free tier | **Yes** | The boundary explains itself |
| On completing a share/invite gate | **Yes** | Free month → annual trial (Explode) |
| Passive settings/upgrade screen | **Yes, always available** | Costs nothing, catches intent |
| Time-boxed offer after first value | **Yes** | Live Activity countdown — but honour the expiry |

### The two patterns that have actually made money

**God Mode (Gas)** — **[Network]**
Free tier fully functional and genuinely good: receive anonymous compliments. Paid tier
(**$6.99–7/week**) satisfies the curiosity the free tier deliberately manufactures: *hints about who
sent it*. Result: **~$7M in 3 months**; **~$11M total revenue before the Discord acquisition**, on
zero venture funding.

Why it works: the free experience *creates* the desire, the paid tier *satisfies* it, and paying
users gain information rather than power — so free users aren't degraded and keep feeding the network.

**Dual unlock (Explode)** — **[Hybrid]**
Two doors to the same reward: **invite friends** *or* **pay**. Price-sensitive users take door one and
drive growth; convenience-seekers take door two and drive revenue. Explode: 3 shares in ~1 hour →
month free → annual trial. Explode+ at ~$39.99/yr or $7.99/mo.

### Pricing rules

- **[Universal]** Weekly pricing lowers the commitment barrier ($6.99/wk *feels* smaller than
  $27.96/mo, which is the point). Migrate habituated users to annual to maximise LTV.
- **[Universal]** Gate the free trial behind a viral action. A trial you hand out for free buys you
  nothing; a trial you unlock with 3 shares buys you 3 impressions.
- **[Utility]** Older audiences: charge more, charge earlier. You're trading K for ARPU on purpose.
- **[Universal]** Validate willingness to pay from day one. If users won't pay **and** won't invite,
  kill it this week.

---

## 10. RETENTION

- **[Universal] Content scarcity beats content volume.** tbh unlocked only **4 polls a day** and
  expired them in 24 hours. Scarcity prevents binge-and-burnout, manufactures anticipation, and turns
  the app into a daily ritual instead of a one-night stand.
- **[Universal] Notifications are the product** for a large share of users — they don't open
  proactively, the notification pulls them in. Ranked by effectiveness:
  1. Personal validation ("someone said you're the funniest person they know")
  2. Curiosity ("a new poll about you is live")
  3. Social proof ("5 friends just voted")
  4. Progress ("you're 1 share from unlocking premium")
  5. Milestones ("you've received 50 compliments")

  Never: "you haven't opened [app] in 3 days." Guilt increases uninstalls.
- **[Universal] Timing.** Teens: 3–5pm (after school) and 7–9pm. Adults: 12–1pm, 5–6pm, 8–9pm. Never
  during school/work hours or after 10pm. Volume: higher in days 1–3, then 2–3/day, then only when
  there's real personal value. Above 3–5/day you get switched off permanently.
- **[Network] Social obligation retains better than app loyalty.** "3 friends are waiting on your
  vote" brings people back for their friends, not for you. That's much stickier.
- **[Universal] Design for distracted, one-handed, sub-2-minute sessions**, instantly resumable. If
  it can't be used on a bus or a toilet, habit formation has fewer chances to happen.
- **[Universal] The retention cliff is real.** Single-mechanic social apps burn bright and fade. Your
  options: evolve the loop (new formats, events, seasons), deepen connections (anonymous →
  semi-known → known), build community identity (school leaderboards, milestones), layer new value
  props, or add visible status systems. Bier's own answer was usually to **sell at peak** — tbh to
  Facebook for **~$30M in ~9 weeks**, Gas to Discord. Building durable social retention is, in his
  framing, a black-swan event.

---

## 11. LAUNCH

### Rules

- **[Universal] If you can't launch from your couch, don't launch.** No flyers, no paid ads, no
  dependencies on other people.
- **[Network] Target 40% penetration of one dense community in 24 hours.** This is pass/fail. Miss it
  and the product or the distribution is broken — iterate or kill, don't scale.
- **[Universal] ~3 exposures** before someone downloads. Saturating one small community beats a thin
  spread across a large one, every time.
- **[Hybrid] [Utility] 50+ short videos/day across multiple accounts** — but only if the product
  demonstrates visually in a few seconds. Dupe.com hit $100K MRR in 60 days on this. Content should
  *demonstrate* value, never explain it.
- **[Universal] Never buy installs to fix a rank drop.** Rewrite copy and tune notifications first.

### The tbh launch sequence (still the template)

1. Pick the community that starts its cycle **earliest** (tbh chose the US high school with the
   earliest start date, because the company was nearly out of money).
2. Create community-specific Instagram accounts (`@app_[schoolname]`). Set them **private**.
3. Follow every student with the school in their bio. Accept **zero** follow requests.
4. Bio: "You're invited to [app] at [School]. Stay tuned." Let curiosity build 1–3 days.
5. At **~4pm** (school dismissal), simultaneously: switch public, drop the App Store link in the bio,
   and accept **all** pending requests at once.
6. Hundreds of notifications fire in the same minute. The app appears in everyone's feed at once —
   manufactured social proof cascade.
7. Geofence and cap each new area until infrastructure holds. The cap itself creates exclusivity and
   a waitlist of evangelists.
8. Let demand **pull** you into adjacent communities. Never push outward.

### The Death Clock play — for Utilities that "can't" go viral

Health apps are single-player utilities for older audiences: structurally the worst possible growth
profile. Bier advised two changes and drove **CAC down to pennies**:

1. **Renamed it** from "Most Days" to **"Death Clock."** The name itself became the hook — it drove
   word-of-mouth *and* got picked up by national press (including a Colbert mention).
2. **Manufactured a shareable artefact**: a survey predicting your death date, plus a projection of
   what you'll look like as you age. This made an abstract value prop viscerally tangible **and**
   generated personalised content users wanted to show people.

Result: **No. 6 in iOS Health.** The lesson for **[Utility]** apps: you don't need a social graph,
you need (a) a name people repeat and (b) an output artefact worth showing someone.

### Crisis planning — the Gas hoax

At peak, a viral hoax claimed Gas was involved in human trafficking. **3% of users deleted their
accounts every day.** The counter-offensive: secure press headlines debunking it, call police chiefs
directly, and embed a debunking video **inside the account-deletion screen** — intercepting churn at
the exact moment of decision. Deletions fell to **0.1%/day**.

**[Universal]** If you build for teens, assume a negative narrative will come. Your rebuttal must be
more viral than the accusation, and it must be placed at the point of churn, not in a blog post.

---

## 12. DECISION TREES

### "Should I build this?"

```
Latent demand — are people already doing this, badly?
├── NO → Stop. You're inventing a need.
└── YES → Can you reach the first 1,000 without ads? (name the channel)
    ├── NO → Stop, or accept you're a paid-acquisition Utility.
    └── YES → Does sharing make it better FOR THE SHARER?
        ├── NO → Not a Network app. Go Utility/Hybrid, plan a budget.
        └── YES → Can you hit aha in ≤3 seconds?
            ├── NO → Cut features until you can.
            └── YES → Fragments ≤ 4?
                ├── NO → Cut dependencies and setup steps.
                └── YES → Build it in ≤8 weeks. Test ONE hypothesis.
```

### "Why isn't it growing?"

```
Is activation ≥40% (install → first action)?
├── NO → Onboarding problem. Check in order:
│   ├── Aha >3s?           → cut screens
│   ├── >6 screens?        → delete to 6
│   ├── >3 signup fields?  → delete to phone+first+last
│   └── Cold permission prompts? → add soft-asks (+20–30%)
└── YES → Are users inviting?
    ├── NO → Is the core content shareable?
    │   ├── NO → Redesign the loop, or manufacture an artefact (Death Clock move)
    │   └── YES → Is the share ≤2 taps and in-flow?
    │       ├── NO → Remove friction; kill any settings-menu invite screen
    │       └── YES → Does the recipient get value WITHOUT installing?
    │           ├── NO → Add App Clip / web preview / curiosity gap
    │           └── YES → Audience too old or too dispersed. Check §3.
    └── YES → K still <1?
        ├── Invites/user low?  → move the share prompt to ≤60s, time-box it
        ├── Conversion low?    → invites carry no context or preview
        └── Loop too slow?     → compress to hours; add urgency (§7)
```

---

## 13. QUICK REFERENCE

| Metric | Number |
|---|---|
| Time to aha | ≤3 seconds |
| First share prompt | ≤60 seconds |
| Activation (install → first action) | ≥40% |
| Onboarding screens | ≤6 |
| Signup fields | 3 (phone, first, last) |
| Cost per extra form field | −5–10% completion |
| Soft-ask lift over cold prompt | +20–30% |
| System approval after a cleared soft-ask | often 80%+ |
| Contacts approval, iOS 18+ | ~65% |
| Invite decay | −20% per year of age, 13→18 |
| Age cut-off for new social products | 22 |
| Opens to prove yourself | ~7 |
| K-factor | >1, loop completing in hours |
| Explode share gate | 3 shares / ~1 hour → month free → annual trial |
| Explode+ | ~$39.99/yr or $7.99/mo |
| Gas God Mode | $6.99–7/week → ~$7M in 3 months |
| Gas total revenue pre-Discord | ~$11M |
| tbh exit | ~$30M to Facebook in ~9 weeks |
| Zero App Store ratings | costs ~2/3 of conversions |
| Launch penetration target | 40% of one dense community in 24h |
| Exposures needed to convert | ~3 |
| Short-form video volume (if it fits) | 50+/day across accounts |
| MVP build time | ≤8 weeks |
| Fragment tax | ~+50% failure risk per fragment; cap at 4 |
| Gas hoax churn | 3%/day → 0.1%/day after the counter |
| Push volume ceiling | 3–5/day |

---

## 14. ADVISOR SEQUENCE

1. **Run intake (§0).** Five questions. Wait. Do not dump the playbook first.
2. **Classify the shape (§2)** and say it out loud. Everything downstream depends on it.
3. **Run the Kill Test and count fragments.** If it fails, lead with that.
4. **Check age against §3.** If it's a Network app aimed at 23+, that's the headline finding.
5. **Time the aha and the share prompt.** ≤3s and ≤60s. Give the actual number you'd expect them to
   measure.
6. **Audit the funnel** against the ≤6 screens and §5 permission order.
7. **For Hybrid or Explode-like asks — and for any request for a teardown — run the §8 steal
   checklist item by item**, scoring the user's app against all 7, then flag anything from the
   do-not-cargo-cult list they're about to walk into.
8. **Map the loop's five stages (§6)** and name the stage where it breaks.
9. **Place the paywall (§9).** Most apps have it in one of the three "never" slots.
10. **Name what pulls the user back on opens 2 through 7 (§3).** If you can't, say so.
11. **Tag every recommendation [Network] / [Utility] / [Universal].**

Be direct. Be numbered. Kill bad ideas in the first paragraph. The reproducible testing system is
worth more than any single idea — a team with more shots at bat beats a team with an audacious
vision.

---

## DEEPER REFERENCE

These files sit alongside this one at the repo root. This file is the source of truth; if anything
below contradicts it, this file wins.

| Topic | File |
|---|---|
| Viral loop anatomy, K-factor, share patterns, case studies | `viral-loops.md` |
| Onboarding, permissions, screen architecture, activation | `onboarding.md` |
| Launch sequencing, geofencing, content distribution | `launch-strategy.md` |
| iOS surfaces, App Store conversion, platform risk | `ios-hacks.md` |
| Paywall placement, pricing, retention, push | `monetisation-retention.md` |
| Psychology, idea validation, testing machine, ethics | `product-psychology.md` |

## SOURCES

- Lenny's Podcast — *How to consistently go viral: Nikita Bier's playbook for winning at consumer
  apps* (invite decay, latent demand, teen density, tbh/Gas history, the trafficking hoax)
- [julianivaldy.com — Explode product analysis](https://julianivaldy.com/explode-product-analysis-by-nikita-bier)
- [retention.blog/p/explode](https://www.retention.blog/p/explode) — screen-by-screen onboarding teardown
- [TechCrunch, 15 Jan 2025 — Explode launch](https://techcrunch.com/2025/01/15/creator-of-gas-and-tbh-makes-an-app-for-disappearing-photos-via-imessage/) (Explode+ pricing, feature set, SnapKit history)
- Gas — Wikipedia and public revenue figures (~$11M pre-acquisition, God Mode pricing)
- Nikita Bier's X thread on Death Clock (rename, death-date artefact, CAC to pennies)
- Nikita Bier's X threads on inverted time-to-value, why shares decrease with age, and why people
  download apps
