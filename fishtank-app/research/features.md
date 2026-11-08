# Fish Tank: feature benchmark, V3 priorities and V2 UI review

Prepared 7 November 2026 from the V2 prototype (`fishtank-app/fishtank.html`, read in full) and web research.

**How to read this.** Most competitor facts come from the companies' own pages, app-store listings or trade press, so they describe what the company says it offers, not what independent audits found. Where sources disagree, the cell says so. "PitchConnectUs" could not be found under that name. The nearest matches were pitch-and-feedback apps (PitchConnect concept, Pitch Me, EI Connect), so they stand in for that column ([S18]). Sources are numbered [S1]–[S23] at the end.

---

## 0. The short version

1. **No competitor offers vernacular, voice-first investing in small local businesses.** Indian P2P apps (LenDenClub, Faircent) are English-first, form-heavy and built around personal loans. Vernacular leaders (Khatabook, Meesho, ffreedom) don't move investment money. Fish Tank can own the space between them, but V2 translates only menus and setup and then switches to English.
2. **Kiva has already proven "your own circle backs you first".** Its Private Fundraising Period and Trustee endorsements are a working form of social underwriting ([S9]). Wefunder's community rounds and "friends invest first" windows do the same for US startups ([S12]). In V2 this is a self-declared toggle worth +12 points. It should be a real flow, shared on WhatsApp.
3. **Several V2 features are below what users already expect.** Indian P2P apps already offer auto-invest with diversification (LenDenClub says 70%+ of lenders use it, with slices from ₹100 [S1][S2]), auto-debit (NACH) repayment with reminders (Faircent [S6]) and referral rewards (LenDenClub, Kiva, Republic [S3][S9][S11]). V2 has none of these.
4. **Regular updates from the business are where every crowdfunding platform falls short.** Wefunder can't force founders to post updates, and reviewers complain they miss them ([S12]). Honeycomb reviews describe silent defaults ([S10]). A required, 3-tap monthly health report would set Fish Tank apart and costs little to build.
5. **Indian regulation changes the design.**
   - The RBI's August 2024 P2P amendment bars platforms from marketing P2P as an investment product, offering liquidity options or assuring returns. It also requires money in escrow to move within one business day (T+1) [S19].
   - SEBI treats equity crowdfunding to the public as unauthorised [S20].
   - V2 conflicts with this in three places:
     - its "money waits in escrow for 30 days" copy;
     - showing a "~15.0% a year" headline on feed cards;
     - an in-app "Invest" button on an equity pitch.

   These are copy and flow fixes, and they are listed in V3. **None of this is legal advice. Get a fintech lawyer's opinion before any real money flow.**

---

## 1. Feature matrix

Legend: **●** strong or core feature · **◐** partial or basic · **○** absent or not found · n/a means it doesn't apply to that model. Each cell gives the specific evidence.

### 1a. Money platforms (investing and lending)

| Feature | LenDenClub (IN, P2P) | Faircent (IN, P2P) | Rang De (IN, social P2P) | Kiva (global, 0% loans) | Honeycomb Credit (US, local-business loans) | Republic (US, equity and more) | Wefunder (US, Reg CF) | StartEngine (US, Reg CF/A+) | **Fish Tank V2** |
|---|---|---|---|---|---|---|---|---|---|
| **Discovery** | ◐ Loan list with risk/tenure; most money placed by auto-invest [S1][S2] | ◐ Borrower listings with risk grade; lenders bid on loans [S6] | ◐ Borrower profiles sourced by field partners, browse by cause [S8] | ● Browse and filter by country, sector, gender; baskets; teams [S9] | ◐ Local campaigns, "Main Street" business pages [S10] | ● Curated deals across startups, real estate and other assets, low minimums [S11] | ● Campaign pages, categories, "testing the waters" reservations [S12] | ● Campaigns; paid Venture Club gives 48 h early access [S13] | ◐ Feed with 5 filter chips; no search, no "near me", no sort |
| **Trust / verification** | ◐ Digital KYC; monthly factsheet publishes "loss of principal since launch" [S1] | ● 120+ checks, 400+ data points, home and business visits [S6] | ● Field partners vet borrowers and handle follow-up [S8] | ● Social underwriting: Trustee endorsements plus friends-and-family lending first [S9] | ◐ SEC Form C disclosures; loans often secured by a lien or personal guarantee [S10] | ◐ Form C/A filings, platform due diligence [S11] | ◐ Form C filings; founder disclosures [S12] | ◐ Form C/A filings [S13] | ◐ Aadhaar, selfie and ₹1 bank check; team video call; **proof is self-declared toggles**; Fish Score shown but not explained |
| **Investor protection** | ◐ Diversification slices; lenders acknowledge principal can be lost [S1] | ◐ Trustee-run escrow, OTP on withdrawals, legal notice on default (costs borne by lender), no recovery assurance [S6] | ◐ RBI-regulated; says it cannot guarantee repayment [S8] | ◐ Lender bears risk; 0% interest [S9] | ◐ Secured loans; investors vote on how to resolve a default [S10] | ● Cancel up to 48 h before close; annual investment limits [S11] | ● Reg CF annual limits; cancellation window [S12] | ● Cancel button until 48 h before close [S13] | ◐ ₹50k-per-borrower note, 2 consent boxes, "report pitch", staged payout claim. Nothing on what happens in a default |
| **Repayment and auto-debit** | ● Monthly repayments to lenders; reinvestment features (curtailed after RBI 2024) [S1][S19] | ● NACH mandate debits EMIs; reminders 3–5 days before due; penal charges [S6] | ● Borrower repayments via Razorpay Smart Collect; Auto UPI top-ups for investors [S8] | ● Monthly partial repayments credited; re-lend or withdraw [S9] | ● Business pays monthly; investors paid quarterly; notification on first repayment [S10] | n/a (equity) | n/a mostly (some debt deals) | n/a mostly | ○ The "share of UPI sales" mechanism is mentioned in one Q&A answer only. No mandate set-up, repayment calendar or reminders |
| **Secondary market / liquidity** | ○ Not allowed: RBI bars "liquidity options" [S19] | ○ Same [S19] | ○ | ○ | ○ | ● Secondary market for eligible companies; the Note trades on a partner venue [S11] | ○ None yet [S12] | ● SE Secondary trading system: 12-month lock-up, thin trading [S13] | ○ Correct for loans; do not build |
| **Community / social** | ◐ City workshops [S4] | ○ | ◐ Student challenges, field visits [S8] | ● Lending teams with team pages [S9] | ● "Community investors"; perk tiers (e.g. "invest $1,000, get 10% off for a year") [S10] | ◐ Note-holder perks, events [S11] | ● Community rounds; "friends invest first" windows; reservations [S12] | ◐ Venture Club perks [S13] | ◐ Public Q&A only |
| **Content / education** | ◐ Blog, city workshops [S4] | ◐ FAQs | ◐ Borrower stories [S8] | ● Borrower stories and updates timeline [S9] | ◐ Founder guides (perks, repayment) [S10] | ◐ Learn hub | ◐ Founder playbook [S12] | ◐ Education pages [S13] | ◐ 4 Learn cards; 4 guide stubs |
| **Vernacular / voice** | ○ English-first (none found) | ○ English-first | ○ English-first | ◐ Volunteer-translated profiles | ○ | ○ | ○ | ○ | ◐ Menus and setup only in Hindi/Telugu; the rest is English; no voice |
| **Mentoring** | ○ | ○ | ◐ Field partners | ◐ Trustees vouch rather than mentor [S9] | ◐ Founder coaching on campaigns [S10] | ○ | ◐ Founder playbook [S12] | ○ | ● Bookable mentors with price and languages; a mentor app. Ratings are a sample only |
| **Onboarding length** | ◐ Fully digital [S5] | ◐ Long for borrowers: documents, NACH, physical visit [S6] | ◐ | ● Email sign-up, lend in a few taps | ◐ Account plus investor questionnaire | ◐ Account, KYC, investor limits | ◐ Same | ◐ Same | ◐ 4 short screens plus 3 verify taps (good), but no phone/OTP and verification can be skipped |
| **Notifications** | ◐ App alerts | ● Pre-EMI reminders [S6] | ◐ | ● Monthly digest email [S9] | ● First-repayment and payout alerts [S10] | ◐ | ◐ Updates often not emailed; investor complaints [S12] | ◐ | ○ The bell always says "No new notifications" |
| **Referral programme** | ● Referee gets ₹100 after a first lend of ₹1,000; tiered rewards since Oct 2025 [S3] | ◐ Affiliate/DSA partner programmes [S7] | ○ | ● $25 credit for invites (undated page) [S9] | ◐ Investor referral page [S10] | ● $2,500 for referring a startup; Note-holder referrals [S11] | ◐ | ◐ | ○ |

### 1b. UX references (vernacular, first-time users, pitching)

| Feature | Khatabook | Meesho | ffreedom / Boss Wallah | Shark Tank India (SonyLIV) | Pitch-feedback apps (stand-ins for "PitchConnectUs") | **Fish Tank V2** |
|---|---|---|---|---|---|---|
| **Discovery** | n/a (ledger) | ● Catalogue plus **Vaani** voice search; colloquial and code-switched queries [S15] | ● Courses by language and sector, ~1,000 courses [S16] | ◐ TV show; registration windows [S17] | ◐ Pitch feeds, matchmaking [S18] | ◐ Feed and chips |
| **Trust / verification** | ◐ Shared digital ledger as proof between parties | ◐ Seller ratings | ◐ "Expert mentors" (claimed 800) [S16] | ◐ KYC and identity documents at application; no fee [S17] | ○ | ◐ See 1a |
| **Repayment / auto-debit** | ● WhatsApp/SMS payment reminders with amount and pay link [S14] | n/a | n/a | n/a | n/a | ○ |
| **Community / social** | ◐ Reminders shared to customers | ● Reselling loop on WhatsApp; "our users are our biggest marketers"; sharing optimised for speed [S15] | ◐ Community features [S16] | ● Mass audience; "pitch on TV" aspiration | ◐ Peer feedback on pitches [S18] | ◐ Q&A |
| **Content** | ◐ Business tips blog | ◐ Seller education | ● Video courses in 5 Indian languages plus English, new each week [S16] | ● Episodes as entertainment-education | ◐ | ◐ |
| **Vernacular / voice** | ● 11–13 Indian languages (counts vary by source) [S14] | ● Voice use went from ~10% to ~40% of users with Vaani; Hindi/English, more rolling out (Telugu unconfirmed) [S15] | ● Hindi, Kannada, Telugu, Tamil, Malayalam, English [S16] | ◐ Hindi/English | ○ | ◐ |
| **Mentoring** | ○ | ○ | ● "Mentor-Connect" calls within ~3 hours; Expert-connect for subscribers [S16] | ● Sharks mentor after a deal | ◐ Mentor office hours on premium [S18] | ● |
| **Onboarding length** | ● Phone number and go | ● Seller onboarding "within 12 hours" [S15] | ● Phone/OTP | ◐ OTP, form, pitch video, KYC later [S17] | ◐ | ◐ |
| **Notifications** | ● Reminders are the product | ● Heavy push and offers | ◐ New-course alerts | ◐ Registration windows | ◐ | ○ |
| **Referral** | ◐ | ● Referral bonuses, WhatsApp sharing [S15] | ◐ | n/a | ○ | ○ |

**Ecosystem signal for voice in payments:** NPCI's Hello! UPI introduced voice payments in Hindi and English in 2023, with more languages planned [S22]. Research with low-literacy users in India found text-only interfaces "unusable" for first-time low-literacy users [S23]. Both support voice-first and icon-plus-audio design for Fish Tank.

### 1c. What the benchmark tells us

| Pattern | Who does it well | Fish Tank V2 | Implication |
|---|---|---|---|
| Friends and family back you before strangers | Kiva PFP and Trustees [S9]; Wefunder "friends invest first" [S12] | Self-declared toggle | Build a real circle round with WhatsApp sharing |
| Auto-diversification | LenDenClub (70%+ use auto-invest) [S2]; Kiva auto-lending [S9] | A "spread across 10" nudge with no tool | One-tap "Spread my money" |
| Auto-debit repayment plus reminders | Faircent NACH [S6]; Khatabook WhatsApp reminders [S14] | Missing | Repayment calendar with UPI AutoPay set-up |
| Updates after funding | Weak everywhere [S10][S12] | Missing | Required monthly health report |
| Voice and vernacular | Meesho Vaani [S15]; ffreedom [S16] | Menus only | Voice pitch, read-aloud, full translation |
| Transparent loss data | LenDenClub "loss of principal" in factsheets [S1] | Risk meter only | Publish platform-level repayment stats on Learn |
| Liquidity | Only US equity platforms, and trading is thin [S13] | None | Don't build for loans (RBI) [S19] |

---

## 2. What to add or change (prioritised)

Impact: H/M/L for winning target users and building trust. Effort: S/M/L **for the prototype** (in brackets: for the real product). "Type" is one of: **Table stakes** (competitors have it and we lack it), **Differentiator** (competitors lack it or do it badly) or **Fix** (V2 has it but it's wrong or weak).

| # | Add / change | Type | App(s) | Why (evidence) | Impact | Effort | Decision |
|---|---|---|---|---|---|---|---|
| 1 | **Voice-first pitch in Telugu/Hindi with auto-subtitles.** Speaking fills in the pitch form. | Differentiator | Business | Voice adoption ~10%→40% at Meesho [S15]; text unusable for low-literacy users [S23]; no money platform does this | H | M (L) | **V3** |
| 2 | **Circle round: friends and family first, shared on WhatsApp** (7 days before the public feed) | Differentiator | Business, Investor | Kiva PFP [S9]; Wefunder [S12]; Meesho WhatsApp loop [S15] | H | M (M) | **V3** |
| 3 | **Fish Score explained, and proof backed by evidence** (photos/documents, "Checked by Fish Tank" stamp) | Fix | Business, Investor, Partner | V2 proof is self-declared; Kiva Trustees and Faircent visits show what real verification looks like [S6][S9] | H | S (M) | **V3** |
| 4 | **Repayment calendar and UPI AutoPay set-up**, with WhatsApp reminders and a working notifications bell | Table stakes | Business, Investor | Faircent NACH and reminders [S6]; Honeycomb payout alerts [S10]; Khatabook reminders [S14] | H | M (M) | **V3** |
| 5 | **Monthly health report from the owner** (3 taps plus photo or voice note), shown as an Updates feed | Differentiator | Business, Investor | Update gaps are the top complaint on Wefunder and Honeycomb [S10][S12] | H | S (S) | **V3** |
| 6 | **Milestone payouts with photo proof** (each tranche released against a bill plus a photo) | Differentiator | Business, Investor | V2 claims "in stages against bills" but shows nothing. Note: funds can't sit in escrow under T+1 [S19], so model tranches as investor-approved debits | H | M (L) | **V3** |
| 7 | **Auto-invest: "Spread ₹10,000 across 10 businesses"** | Table stakes | Investor | LenDenClub [S1][S2], Kiva [S9]; V2 nudges but gives no tool | H | M (M) | **V3** |
| 8 | **Full vernacular and read-aloud, plus low-data mode** | Table stakes for the target users | All | Khatabook 11–13 languages [S14]; ffreedom 5 [S16]; V2 drops to English after setup | H | M (L) | **V3** (core screens) |
| 9 | **Compliance copy and flow fixes**: no 30-day escrow promise; returns not used as the headline; equity pitches become "request intro" | Fix | Investor, Business | RBI Aug 2024 [S19]; SEBI on crowdfunding [S20]; UPI one-time mandate blocks funds in the payer's own account for up to ~60 days [S21] | H (risk) | S | **V3** (rides along) |
| 10 | **Scam-alert education in the flow** (e.g. "Fish Tank will never call to ask for money", shown on the invest sheet and in chat) | Differentiator | All | V2 hides this in a guide accordion | M | S | V3 copy only; full module next |
| 11 | **Referral rewards** (investor: ₹100 credit after a friend's first ₹1,000; owner: badge plus fee waiver for referring a business that goes live) | Table stakes | Investor, Business | LenDenClub [S3], Kiva [S9], Republic [S11], Meesho [S15] | M | S | Next |
| 12 | **Mentor ratings and reviews** after each call; "calls done" count; verified profession | Table stakes | Mentor, Business | V2 shows "4.9 (sample)" only to the mentor; ffreedom's paid mentor connect [S16] | M | S | Next |
| 13 | **Franchise brand "Verified" badge** with plain disclosure (fees, royalty, outlets open/closed, payback months) | Differentiator | Partner, Business | No Indian equivalent of a franchise disclosure document; trust gap for franchise starters | M | M | Next |
| 14 | **"Graduate to a bank loan"**: after 6+ on-time months, share the repayment record with lenders, plus a pre-filled MUDRA application | Differentiator (revenue) | Business, Lender | V2 lender pipeline expects this but there is no owner-side flow | H | M | Next (show a teaser card in V3 calendar) |
| 15 | **Success stories** (video, with repayment record) | Content | Investor, Business | Kiva and Rang De stories [S8][S9] | M | S | Next |
| 16 | **Live local pitch events** ("Fish Tank Nalgonda, Sat 6 pm"): RSVP, watch live, ask questions | Differentiator | All | Shark Tank's appeal [S17]; LenDenClub city workshops [S4] | M | M | Later |
| 17 | **Near me / district filter and search** in Discover | Table stakes | Investor | Kiva filters [S9]; local trust | M | S | V3 small fix |
| 18 | **Platform repayment stats page** ("Out of 100 loans: 91 on time, 6 late, 3 not repaid") | Differentiator (trust) | Investor | LenDenClub publishes loss of principal [S1] | M | S | Next |
| 19 | Secondary market / early exit | — | — | RBI bars liquidity options for P2P [S19] | — | — | **Do not build** |

---

## 3. V3 build list (8 items, plus ride-along fixes)

Copy is given in English. Hindi and Telugu are given for the key lines only. **Have a native speaker check every translation before testing.** Everything is simulated in the prototype; no real speech-to-text or payments.

### V3-1 · Speak your pitch (voice-first builder)
- **App / screen:** Business → My pitch → builder. A new **Step 1, "Tell us in your words"**. The current steps 1–5 become "Check what we understood", "What you give back", "Proof" and "Preview".
- **What it does:**
  1. A big mic button and a language chip (తెలుగు / हिंदी / English).
  2. Three prompts play as audio and show as text, one at a time:
     - "What is your business?"
     - "How much do you need, and for what?"
     - "How will you pay it back?"
  3. The owner holds to talk, up to 30 s per prompt.
  4. A moving waveform shows while recording. The transcript appears as subtitles.
  5. A confirm screen fills the fields (name, city, amount, spending list) as big cards. Each card has **Yes, correct** and **Change** (re-record or type).
  6. Video is optional ("Add a video. Pitches with a face get 2× more views (demo)").
  7. Auto-subtitles go on the pitch video in the speaker's language, with a one-tap English or Hindi translation for investors.
- **Prototype:** Hold the mic for 2 s and canned Telugu or Hindi text "types" into a subtitle box. The confirm cards fill from sample data (the Lakshmi parlour).
- **Copy:**
  - Title: "Tell us about your business, in your own language" · HI: "अपने बिज़नेस के बारे में अपनी भाषा में बताइए" · TE: "మీ వ్యాపారం గురించి మీ భాషలోనే చెప్పండి"
  - Mic: "Hold and speak" · HI: "दबाकर बोलिए" · TE: "నొక్కి పట్టి మాట్లాడండి"
  - Confirm: "Did we hear this right?" · HI: "क्या हमने सही सुना?" · TE: "మేము సరిగ్గా విన్నామా?"
  - Below the fold: "No need to type. You can change anything later."
- **On the investor detail:** a "Subtitles: Telugu → English" chip on the poster, and a transcript in an expandable block.

### V3-2 · Circle round: your own people first (WhatsApp)
- **App / screen:** Business → My pitch (after review and before going live) shows a new state, **"Circle round · 7 days"**. Investor gets a new entry point: a shared link opens the pitch in **Visitor** mode with a circle banner.
- **What it does:**
  1. The owner picks a goal: "Get 10% (₹45,000) from people who know you" (default 10% of the ask).
  2. **Share on WhatsApp** opens a prefilled message with a card image and link.
  3. Progress shows as faces/initials plus an amount: "6 people · ₹31,000 of ₹45,000".
  4. Each circle backer can add a one-line **vouch** ("I've bought milk from Lakshmi for 6 years"), shown publicly like a Kiva Trustee endorsement.
  5. The pitch reaches the public feed when the circle goal is met or the 7 days end. A tag on the investor card reads "Backed by 9 people who know her".
  6. Vouches from verified users add to the Fish Score; anonymous ones don't.
- **Prototype:** The share button shows a WhatsApp-style preview sheet. "Simulate friends" (presenter panel) adds backers.
- **Copy:**
  - Heading: "First, your own people" · HI: "पहले अपने लोग" · TE: "ముందు మీ వాళ్ళు"
  - Sub: "When people who know you invest first, strangers trust you more."
  - WhatsApp message: "Namaste! I'm opening a dairy parlour near Nalgonda bus stand. I'm raising ₹4.5 lakh on Fish Tank, and I'd like the people who know me to back me first. Even ₹1,000 helps. See my 1-minute video: fishtank.app/p/lakshmi"
  - Investor banner: "Lakshmi shared this with you. You're seeing it before the public."
  - Vouch prompt: "How do you know Lakshmi? (one line, shown publicly)"

### V3-3 · Fish Score explained, and proof that's checked
- **App / screen:**
  - **Business → builder "Proof" step:** each proof card now has **Add photo/document**, then status "Checking (within 24 h)", then "Checked by Fish Tank". Points apply only once checked. A ghost "+15" chip shows what it will add.
  - **Investor:** the Fish Score ring on cards and the detail page becomes a button that opens a **"Why 81?"** sheet.
  - **Partner:** the same sheet opens from Pipeline candidates.
- **"Why 81?" sheet:** stacked bars for each part:
  - ID verified +8
  - Proven format +15 (brand approval letter, checked 3 Nov)
  - Own circle +12 (9 backers, ₹54,000)
  - Real demand +12 (lease signed, photo)
  - Mentor +10 (Ravi Kumar, 3 calls)

  Then "What's missing": "No sales history yet (new business)". Footer: "The Fish Score is not a guarantee. It shows how much has been checked, not whether the business will succeed."
- **Copy:**
  - Button: "Fish Score 81 · What does this mean?"
  - Sheet title: "How we got 81"
  - Proof card: "Shop lease signed. Add a photo of the first page."
  - Status: "Checking · usually within a day" / "Checked by Fish Tank on 3 Nov"

### V3-4 · Repayment calendar and AutoPay
- **App / screen:**
  - **Business → Home (after funding):** the journey card becomes a "Money" card: "Next repayment ₹6,210 on 5 Dec · AutoPay on". A new **Repayments** screen (from Home) shows a month-by-month calendar: paid ✓, due, upcoming.
  - **Investor → Portfolio:** a new "Coming to you" strip ("₹347 on 5 Dec from Kavya's salon") and a calendar view. Each holding shows "On time · 3 of 36 paid", "Late 4 days" or "Missed".
  - **Bell:** a real list. "Repayment received ₹347", "Kavya posted her November update", "Payment due in 3 days" (owner).
- **Owner AutoPay set-up** (after the goal is reached): a 3-step sheet.
  1. Choose bank account (verified).
  2. Approve the UPI AutoPay mandate (simulated UPI PIN screen).
  3. Confirm.

  WhatsApp reminders go out 3 days before ("like Faircent", but in the owner's language). For share-of-sales deals the calendar shows a range: "₹4,000–₹9,000, depends on sales".
- **Late payment path** (shown to investors): "Late 1–15 days: we remind the owner daily. 15–30 days: their mentor calls. 30+ days: legal notice and recovery, cost shared across investors." Copy this from your actual policy; Faircent passes recovery costs to lenders [S6].
- **Copy:**
  - "Your next payment: ₹6,210 on 5 December. It goes automatically from your bank."
  - Investor: "Money coming to you" · HI: "आपको मिलने वाला पैसा" · TE: "మీకు వచ్చే డబ్బు"
  - Teaser at the bottom of the owner's calendar (for V3-14 later): "Pay on time for 6 months and banks can see it. Unlock a bank loan offer."

### V3-5 · Monthly health report
- **App / screen:** Business → Home shows a task card on the 1st of each month: "Post your November update (2 minutes)". Investor → pitch detail gets a new **Updates** section above Q&A. Portfolio gets a combined Updates feed.
- **Flow (3 taps plus optional media):**
  1. "How was this month?" → 😀 Good / 😐 Okay / 😟 Hard (big icon tiles with words).
  2. "Sales this month" → chips (Less than ₹1L / ₹1–2L / ₹2–3L / more) or "Use my UPI total" (simulated).
  3. "Add a photo or voice note" (optional).

  The update posts with a date. A missed update shows to investors after 10 days as "No update for November", and the owner's Fish Score drops 2 points until they post.
- **Copy:**
  - Owner card: "Your investors want to hear from you. Post a 2-minute update."
  - Investor empty state: "Lakshmi posts an update every month. The first one comes in December."
  - Missed: "No update for November yet. We've reminded Lakshmi."

### V3-6 · Milestone payouts with photo proof
- **App / screen:** Investor → pitch detail. "Where the money goes" becomes a **milestone tracker**: ① Franchise deposit ₹1.8L (bill ✓, photo ✓, released 2 Nov), ② Freezers ₹1.7L (waiting for bill), ③ Opening stock ₹1L (locked). Business → My pitch (funded state) gets a "Next payout" card: "Upload the freezer bill and a photo of the freezers in your shop to release ₹1,70,000".
- **Rules shown:** a photo must be taken in-app (with time and location), and the bill must match the seller named in the pitch. A Fish Tank checker approves within 24 h.
- **Prototype:** The owner taps "Upload bill" then "Take photo" (both canned). The milestone moves to ✓ and the investor detail updates.
- **Compliance note (internal, not UI):** under T+1 [S19] the platform can't hold lenders' money across milestones. Model each milestone as a separate tranche debited from the investor's UPI block or mandate [S21] when it is approved. Legal sign-off is needed, including whether paying suppliers directly is allowed.
- **Copy:** "Money is released in 3 steps, only after Lakshmi shows the bill and a photo." · Owner: "Show the bill, get the money. We check within a day."

### V3-7 · Auto-invest: spread across 10
- **App / screen:**
  - **Investor → Discover:** a top card "New here? Spread ₹10,000 across 10 businesses in one tap". It uses the onboarding answers (amount, "monthly vs growth"), which V2 collects but never uses.
  - **Investor → Portfolio:** an "Auto-invest" toggle row.
- **Sheet:**
  1. Amount (₹5,000 / ₹10,000 / ₹25,000).
  2. "How many businesses" (fixed at 10, explained).
  3. Preferences: chips for Near me / Women-led / Monthly income / Lower risk only.
  4. A preview list of the 10 picks at ₹1,000 each; the investor can remove any.
  5. Consents; then **Invest ₹10,000 in 10 businesses**.

  Auto-invest stays on for new matching pitches, with a "pause any time" switch.
- **Guardrails shown:**
  - "We never put more than ₹1,000 of this in one business."
  - "RBI limit: at most ₹50,000 to one borrower across all P2P apps."
  - "You choose the rules; we don't promise returns."
- **Copy:** "Spread your money" · HI: "पैसा बाँटकर लगाइए" · TE: "డబ్బును పంచి పెట్టండి". Sub: "If one business fails, you lose ₹1,000, not ₹10,000."

### V3-8 · Every word in your language, read aloud, and a low-data mode
- **App / screen:** All apps. Translate every screen of the Business app and the investor card, detail and invest flow into Hindi and Telugu, and remove the "rest of the app is in English" note. Add a 🔊 **Listen** button to:
  - each H1 screen intro;
  - each pitch story;
  - the "If you put in ₹10,000" box;
  - each consent line.

  It uses the browser's speech synthesis with `hi-IN`/`te-IN` voices, and falls back to a pre-recorded clip in a real build.
- **Language as the first screen:** three big tiles, "తెలుగు", "हिंदी", "English", each speaking its name on tap. This replaces the small chips on the splash.
- **Low-data mode (Me → "Save mobile data"):** posters become still photos; pitch videos play as audio plus subtitles until tapped; feed images load on tap. A tag shows "Low-data mode on · saves about 80%" (demo figure). V3 can label the offline banner "You're offline. Showing what you saw last."
- **Copy:** "Listen" · HI: "सुनिए" · TE: "వినండి". "Save mobile data" · HI: "मोबाइल डेटा बचाइए" · TE: "మొబైల్ డేటా ఆదా చేయండి".

### Ride-along fixes in V3 (copy and small flow, no new feature)
- **Escrow copy:**
  - Current text: "Money waits in the licensed partner's escrow until you reach your goal" and "If the business doesn't reach its goal in 30 days, you get all of it back".
  - New text: **"Your money stays blocked in your own bank account until the goal is reached. If it isn't reached in 30 days, the block is released. Nothing is taken."** This uses a UPI one-time mandate pattern [S21]; check with the payments partner.
- **Returns as the headline:** on feed cards, lead with how you get paid ("Pays monthly"), then "15% interest · not guaranteed". Show the **first or default** option, not the highest-rate one (`bestOpt()` currently sorts by rate, highest first).
- **Equity pitch (Rahul's millet snacks):** replace "Invest in this business" with **"Ask for an introduction"** and the note "Ownership deals are private offers made outside the app, with a lawyer. They're not open to everyone." Remove the "Growth share" filter or rename it "Growth (intro only)" [S20].
- **Scam line on the invest sheet:** "Fish Tank staff will never call or WhatsApp you asking for money or an OTP."
- **"Near me" chip** in Discover.

---

## 4. V2 UI/UX review (problem → fix)

The visual identity stays as it is: teal business, gold investor, plum helper; Bricolage Grotesque for headings and Figtree for body. Function names refer to the V2 file.

### 4a. Clarity and copy

| # | Problem | Fix |
|---|---|---|
| 1 | The business Home heading **"Free money you may get"** sits over MUDRA and CGTMSE, which are loans and guarantees. That is misleading and could cause harm (`bizHome`). | "Government loans and subsidies for you". Add a type tag per scheme: **Loan**, **Loan + subsidy**, **Grant**. |
| 2 | The **Fish Score** appears on every card, detail page and pipeline but is never explained. "Fish Score" next to "~15% a year" reads like a rating of returns. | Make it tappable and open the "Why 81?" breakdown (V3-3). On first view, show a one-line coach mark: "Fish Score = how much we've checked." |
| 3 | The feed card's biggest number is **"~15.0% a year"** in gold. `bestOpt()` picks the **highest**-rate option, the most flattering one, and RBI bars presenting P2P as an investment with assured returns [S19]. | Lead with "Pays monthly" / "Share of sales" / "One payment at the end". Show the rate as small secondary text with "not guaranteed". Use the default option. |
| 4 | Jargon a first-time user won't follow: "1.25×", "escrow", "cap", "lump", "₹2.79L", "P2P", "Ownership grows with the company". | "until ₹12,500 comes back for every ₹10,000"; "a locked account at our partner bank"; "₹2.79 lakh"; "loan between people (P2P)" only in the legal line. |
| 5 | **Verify screen:** "Continue" is enabled with nothing verified, and does exactly what "Do this later" does (`onbVerify`, both call `finishOnb`). | Primary: "Verify now (2 min)", which starts the first unfinished check. Secondary: "Look around first". Say what's locked: "You can browse, but you can't invest or go live until this is done." |
| 6 | "I already have an account" lands on the same "What do you want to do?" screen. There is no phone/OTP step anywhere. | Add a **mobile number + OTP** step (OTP auto-read), and route "I have an account" to it. |
| 7 | Investor setup asks "How much?" and "What would you like back?", then never uses the answers (`S.ans.size` is never read). | Use them: pre-fill Auto-invest (V3-7) and set the default Discover filter. Otherwise remove the questions. |
| 8 | "Menus and setup are translated. The rest of the app is in English for now." For Telugu/Hindi-first users, the app becomes unusable right after setup. | V3-8: translate core screens and add Listen buttons. |
| 9 | **Demo controls look like product UI:** "Skip the wait (demo)", "Show a day passing (demo)" and "Tap" tags on verify rows. | Move them to the presenter panel under "Demo controls". If one must stay on the phone, give it a dashed outline and a "DEMO" label. |
| 10 | The Learn screen shows a placeholder price, "₹[299] a month (price to be tested)". | "Fish Tank Pro · coming soon" with no price. |
| 11 | "Money goes to their sellers, not their pocket" (Discover intro) sounds like suspicion of the owners. | "Money is paid to suppliers against bills, step by step." |
| 12 | The invest "done" screen promises a 30-day escrow refund. This conflicts with T+1 [S19]. | Use the ride-along copy in §3 (money blocked in your own account). |
| 13 | Me → Safety shows **"Hide my phone number"** with a switch that can't be operated (`span` with `aria-hidden`). It looks broken. | Show it as a fixed fact with a lock icon: "Your number stays hidden until a deal is signed · Always on". |
| 14 | Owner has no default-path copy: what happens if they can't pay? Investors don't see it either. | Add a "If payments are late" accordion on the detail page and in the owner's Repayments screen (V3-4). |

### 4b. Hierarchy

| # | Problem | Fix |
|---|---|---|
| 15 | Each screen opens with an eyebrow plus a 27px H1, and the eyebrow repeats the tab label ("MY PITCH" above, "My pitch" in the tab bar). With the app bar, that is about 150px of chrome on a 640px-tall budget phone. | Drop eyebrows that repeat the tab. H1 at 24px. Merge the app bar and the screen title on secondary tabs. |
| 16 | The app bar repeats the logo and mode pill on every screen. | Compact bar: screen title on the left, language and bell on the right. Show the logo only on the first tab. The mode is already clear from the accent colour. |
| 17 | The investor card gives about 8 facts equal weight: city/type, risk tag, title, rate, score ring, bar, raised, investors. | Three tiers: (1) photo, title, owner name; (2) one line, "Pays monthly · Medium risk · Fish Score 81"; (3) bar with "62% · 12 days left". Put investor count and city in small text. |
| 18 | Pitch detail order buries the decision content: risk, then funding, then uses, then proof, with Q&A last and no updates. The funding deadline isn't shown anywhere. | Order: video, then story, then **₹10,000 outcome**, then **risk with "Why 81?"**, then proof, then milestones (V3-6), then updates (V3-5), then Q&A. Add "12 days left" beside the funding bar. |
| 19 | Business Home is the same onboarding stepper after the pitch is live or funded, so it stops being useful. | Make Home change with the stage. Before live: the journey. Live: "This week" tasks (answer 2 questions, share with 5 people). Funded: next repayment, update due, milestone to unlock. |
| 20 | Builder step 3, "What will you give back?", has 3 switches each with 2 chip rows. That is a lot of decisions for a first-timer. | Recommend one: "Most shops like yours choose **share of sales, 5%**". Put the other options under "Other ways to pay back". Show a "What investors see" preview for the recommended one only. |
| 21 | The portfolio's big gold "Invested ₹25,000" card with an "Example" tag can be mistaken for real money. | Empty state: "You haven't invested yet", a short illustration, and an "Auto-invest ₹10,000" CTA. If an example is shown, use grey with no accent fill. |

### 4c. Simplicity for first-time users

| # | Problem | Fix |
|---|---|---|
| 22 | The pitch builder is text-first (name, city, typed amount, free-text spending) and puts the video last. That is the hardest order for low-literacy users [S23]. | Voice-first (V3-1). Speaking fills the fields, and the owner confirms with Yes/Change. |
| 23 | "What will you spend it on?" is a free-text box. | Item chips (Machine, Freezer, Shop rent, Stock, Fit-out, Licence, Other), each with an amount and an optional photo of the quote. The total adds itself up. |
| 24 | Proof switches add points instantly, which teaches people to "tap for points" with no evidence. | Proof needs a photo or document, then shows "Checking" and finally "Checked" (V3-3). |
| 25 | The amount field is a raw number input. "300000" gives no sense of lakh. | Read back "₹3,00,000 (3 lakh)" live, with a Listen button. Keep the chips as the main input. |
| 26 | Discover has no "near me", district or search. Local trust is the point of the product. | Add "Near me" and "My district" chips, plus search by town or business type. |
| 27 | Posters are gradients with initials, so every pitch looks the same and nobody shows a face. | Photo thumbnails (owner at the shop), a language badge ("Telugu · subtitles") and duration. Keep the "Sample" tag. |
| 28 | Investors must work out alone what "spread across 10" means. The tool to act on it doesn't exist. | Auto-invest (V3-7). |
| 29 | The splash makes language a small chip row. For these users it's the most important choice. | A full-screen language picker with big tiles that speak their names (V3-8). |

### 4d. Accessibility

| # | Problem | Fix |
|---|---|---|
| 30 | **Tap targets below 48dp:** `.icon-btn` 38px; `.btn.sm` about 36px; `.chip` about 40px; `.back` has 0 padding (about 24px tall). | `min-height:48px` on all interactive elements; `.back{padding:12px 8px}`; icon buttons 48px; keep 8px gaps between targets. |
| 31 | **Small text:** tab labels 12px, tags 12.5px, mode pill 12px, and many key lines at 13–13.5px (risk note, consent context, RBI limit, Q&A meta). Telugu script needs more room than Latin at the same size. | Body 16px, minimum 14px. Key numbers 16px or more. `line-height:1.6` and +1px when `lang` is `te` or `hi`. Avoid fixed heights so OS font scaling works. |
| 32 | **Contrast failures** (computed): `.tag.good` #17803D on #DDF2E4 is **4.27:1**, `.tag.warn` #A35F00 on #FBECD6 is **4.31:1** (both under 4.5:1 for small text). Input, chip and card borders #D9E3E1 on white are **1.31:1** (UI boundaries need 3:1). | Good text #12692F (5.8:1). Warn text #9A3412 on #FDEBDC (6.3:1). Input and unselected chip borders #869794 or darker (3.06:1 on white). Card borders can stay light because cards aren't controls. |
| 33 | **Colour collision in the investor app:** the accent is gold #A35F00 and `--warn` is also #A35F00. The "Medium risk" tag, the rate, the score ring and the risk meter bars (`.risk i.on` uses `--acc`) all share one colour, so risk can't be told apart from branding. | Never use the accent for risk. The risk meter uses semantic colours: lower = good, medium = rust #9A3412, higher = bad. Always pair colour with a word and an icon. The score ring stays neutral ink. |
| 34 | Every click re-renders the whole app with `innerHTML`, so **focus is lost**. Screen readers restart and keyboard users jump to the top. Sheets don't move focus in, trap it, or return it on close. | After render, restore focus to the element with the same `data-act` and `data-arg`. On opening a sheet, focus its heading and trap Tab; on close, return focus to the trigger. Announce changes in an `aria-live` region. |
| 35 | The proof and option toggles are buttons with `aria-pressed` that look like switches. The womenOnly switch is a `button` with no state role. | Use `role="switch"` with `aria-checked`, or real checkbox inputs styled as switches. |
| 36 | Toasts disappear after 3 s, which is too short for slow readers and for actions like "Accepted". | 5–6 s, with an Undo where possible ("Not now" → Undo). Keep `role="status"`. |
| 37 | Pitch videos have no captions or transcript. | Auto-subtitles plus a transcript (V3-1). |
| 38 | `html lang` switches, but English strings inside a Hindi page will be read by a Hindi voice. | Add `lang="en"` on untranslated spans until they are translated. |
| 39 | Good already: `prefers-reduced-motion` is respected, dark mode tokens exist, `:focus-visible` is styled, and forms have labels. | Keep these. |

### 4e. Consistency between the apps

| # | Problem | Fix |
|---|---|---|
| 40 | Tab structures differ. Business has Home/My pitch/Help/Me (4), investor Discover/Portfolio/Learn/Me (4), mentor Requests/Profile/Me (3), partner Pipeline/Listing/Me (3). Only business has a "today" Home. | Use one pattern everywhere: **Home (today) · main work · Learn/Help · Me**. Investor Home shows money coming, updates and auto-invest status. Mentor Home shows today's calls and new requests. Partner Home shows new candidates. |
| 41 | Mentors, brands and lenders share the plum "helper" app and one door, "Mentor or partner with businesses", even though a bank is not a helper. | Keep plum, but split the door into two doors: **"Guide business owners (mentor)"** and **"Find franchisees or borrowers (brand or bank)"**, with separate icons and pills ("Mentor" / "Partner"). |
| 42 | Button roles are inconsistent. Equal-level actions use `.btn.ghost.sm` ("See all"), `.btn.soft.sm` ("Book a call", "Ask") and `.btn.primary.sm` ("Send", "Accept"). | Define three roles: **Primary** (one per screen, filled), **Secondary** (soft), **Tertiary** (text link with chevron, used for "See all"). Apply them across all four apps. |
| 43 | The mentor sees their "4.9 rating (sample)", but owners browsing mentors see no ratings at all. | Show "★ 4.8 · 37 calls" on `mentorCard`, and collect a rating after each call (item 12). |
| 44 | Tag meanings overlap: the warn colour marks "In review", "Example" and "Example data"; the accent colour marks "In escrow" and "Fits you". | Status tags: review = info (neutral blue-grey), live and repaying = good, late = warn, missed = bad. Sample and example labels are neutral grey. |
| 45 | Money formats are mixed on the same screen: `inr()` gives ₹2,79,000 and `lakh()` gives ₹2.79L. | One rule: amounts of ₹1 lakh or more in summaries read "₹2.79 lakh"; exact amounts the user pays or receives use the full ₹ form. Never use "L". |
| 46 | The Fish Score appears in brand pipeline cards, but every lender candidate has the same hard-coded "Repaid on time" and "6 months on Fish Tank". | Vary the sample data and show repayment streaks ("11 of 12 on time"). Open the same "Why 81?" sheet. |

### 4f. Visual polish

| # | Problem | Fix |
|---|---|---|
| 47 | Almost everything is a pill: buttons, chips, tags, segments, mode pill, so you can't tell what's tappable from what's a label. | Tags become 6px-radius rectangles with no border. Chips stay bordered pills. Buttons stay filled pills. |
| 48 | Cards use one radius family (16–22px) but mixed inner padding (10/12/14/16) and many inline styles. | Tokens: `--r-card:20px`, `--r-inner:14px`, `--pad:16px`. Move the inline `style=` sizes into classes. |
| 49 | Gradient posters with initials look like placeholders even in the presenter demo. | Use 6 royalty-free shop photos for the sample pitches (with "Sample" kept) so the feed reads as real. |
| 50 | Success moments (invest done, call booked) all use the same check circle and plain text. | Add the specific next step ("First repayment: 5 Dec · ₹347") and a small celebratory fish motion, respecting reduced motion. |
| 51 | The KPI tiles (Views / Interested / Funded) show no trend or context. | Add a tiny delta ("+96 today") and a next action ("9 interested · reply to 2 questions"). |

---

## 5. Sources

- **[S1] LenDenClub**
  - [Factsheet, Aug 2024](https://lendenclub.com/wp-content/uploads/2024/09/FACTSHEET-LenDenClub-Aug-2024.pdf): ₹100 diversification slices, loss of principal metric
  - [What is LenDenClub](https://support.lendenclub.com/support/solutions/articles/1060000154563-what-is-lendenclub-)
  - [Fixed maturity plan launch (ThePrint)](https://theprint.in/ani-press-releases/lendenclub-introduces-a-fixed-maturity-peer-to-peer-investment-plan-offering-expected-returns-of-10-to-12-per-cent-p-a/1060744)
- **[S2]** [Inc42: LenDenClub auto-invest used by 70%+ of lenders](https://inc42.com/?p=167830)
- **[S3]** LenDenClub referral programme: [Refer & Earn](https://www.lendenclub.com/?p=62628) and [referral T&C](https://lendenclub.com/referral-tc)
- **[S4]** [LenDenClub P2P workshop in Kanpur](https://lendenclub.com/?p=57160)
- **[S5]**
  - [LenDenClub on RBI caps](https://www.lendenclub.com/?p=87628)
  - [PressReader / Banking Frontiers on digital onboarding](https://www.pressreader.com/india/banking-froniers/20220710/281754158035539)
- **[S6] Faircent**
  - [FAQs (NACH, reminders, collections)](https://www.faircent.com/node/13)
  - [Lender process (trustee escrow, OTP withdrawals)](https://www.faircent.com/node/140)
  - [Fair practices code](https://qc9.faircent.com/node/452)
  - [Business Standard 2018 on auto-invest](https://www.business-standard.com/amp/article/companies/faircent-uses-automation-to-bring-borrowers-and-lenders-on-same-platform-118010800006_1.html)
- **[S7]** [Faircent affiliate & referral programmes](https://www.faircent.com/affiliates-partners)
- **[S8] Rang De**
  - [Site](https://rangde.in) and [FAQs](https://rangde.in/faqs)
  - [App Store listing (Auto UPI, RBI P2P NBFC)](https://apps.apple.com/us/app/rang-de/id1475769579)
  - [Razorpay Smart Collect case](https://razorpay.com/blog/?p=2838)
  - [Student challenge](https://rangde.in/blog/rang-de-x-tribesforgood-how-a-special-student-challenge-drove-social-impact)
  - [The Logical Indian](https://thelogicalindian.com/?p=84141)
  - [Deccan Herald](https://www.deccanherald.com/archives/small-investments-usher-big-change-2506433)
- **[S9] Kiva**
  - [Auto-lending FAQ](https://www-1.kiva.org/blog/auto-lending-on-kiva-frequently-asked-questions)
  - [Lending teams (SSIR)](https://ssir.org/articles/entry/kiva_introduces_lending_team_feature)
  - [What is social underwriting](https://www-1.kiva.org/blog/what-is-social-underwriting)
  - [Direct loans due diligence (PFP, Trustees)](https://kiva.org/about/due-diligence/direct-loans)
  - [Bonus/referral programme](https://www.kiva.org/bonus/learnmore)
  - [Monthly Good](https://www.kiva.org/lp/support-causes-monthly)
- **[S10] Honeycomb Credit**
  - [How to get paid back](https://www.honeycombcredit.com/amp/how-to-get-paid-back-after-investing-in-a-crowdfunding-campaign)
  - [Crowdfund Insider 2024 (loan structure, liens)](https://www.crowdfundinsider.com/2024/03/222861-honeycomb-credit-is-a-top-reg-cf-issuer-that-can-replace-bank-loans-for-smaller-firms/)
  - [Investor perks guide](https://smallbusiness.honeycombcredit.com/flightplan/investor-perks)
  - [Investor referral page](https://www.honeycombcredit.com/investor-referral-page)
  - [Trustpilot reviews (defaults, communication)](https://au.trustpilot.com/review/honeycombcredit.com?page=3)
  - [YieldTalk review](https://yieldtalk.com/honeycomb-review/)
- **[S11] Republic**
  - [How Republic Note works](https://republic.com/note/how-it-works)
  - [Secondary market](https://republic.com/help/what-is-republic-secondary-market-and-how-does-it-work-2)
  - [Note referral terms](https://republic.com/note/republic-note-referral-program-terms)
  - [Cancellation help](https://republic.co/help/how-can-i-cancel-my-investment-817a1de3-ad54-4651-b6bd-1007f172634a)
  - [Review](https://boringbusinessnerd.com/post/republic-review)
- **[S12] Wefunder**
  - [What a reservation means](https://wefunder.helpjuice.com/reservations/what-does-it-mean-to-%22reserve%22-an-investment)
  - [Testing the waters](https://communityroundup.substack.com/p/testing-the-waters)
  - ["Friends invest first" example](https://7generationgames.com/invest-in-our-wefunder-today-friends-invest-first-ends-6-30)
  - [Mercury community-round learnings](https://mercury.com/blog/community-round-learnings)
  - [Communityround.com launch](https://www.raptorgroup.com/news/wefunder-launches-communityround-com-as-demand-for-turning-fans-into-investors-builds/)
  - [Trustpilot (updates, no secondary market)](https://www.trustpilot.com/review/wefunder.com?page=5)
- **[S13] StartEngine**
  - [Secondary marketplace (Crowdfund Insider 2023)](https://www.crowdfundinsider.com/2023/07/210080-startengine-launches-secondary-marketplace-for-securities-issued-on-its-platform-and-others/)
  - [Secondary learn](https://startengine.com/secondary-learn)
  - [Venture Club](https://invest.startengine.com/venture-club)
  - [Owner's Bonus](https://www.startengine.com/blog/what-is-owners-bonus)
  - [Cancel an investment](https://startengine.zendesk.com/hc/en-us/articles/115002320072-How-do-I-cancel-my-investment)
  - [2026 review](https://angelinvestorsnetwork.com/capital-raising/startengine-review-2026-equity-crowdfunding)
- **[S14] Khatabook**
  - [App features blog](https://khatabook.com/blog/khatabook-app-features)
  - [YourStory product roadmap](https://yourstory.com/2021/08/product-roadmap-fintech-startup-khatabook-10-million-msme-users)
  - [OkCredit comparison](https://okcredit.in/khatabook-alternative)
- **[S15] Meesho**
  - [Inc42 on Vaani voice commerce](https://inc42.com/features/meesho-bets-big-on-voice-commerce-will-india-respond)
  - [Vaani launch](https://startupfeed.in/meesho-launches-vaani-indias-first-vernacular-ai-shopping-assistant-for-250-mn-bharat-users/)
  - [Business Insider (WhatsApp sellers, 12-hour onboarding)](https://www.businessinsider.in/advertising/brands/article/meesho-the-latest-company-to-join-the-unicorn-club-aims-to-build-a-single-ecosystem-to-help-smbs/articleshow/81953840.cms)
  - [Inc42 on resellers](https://inc42.com/startups/meesho-revamps-indias-unorganised-retail-by-empowering-resellers)
  - [YourStory product roadmap (sharing optimisation)](https://yourstory.com/2021/03/product-roadmap-meesho-fashion-social-ecommerce-startupe-ntrepreneurs)
- **[S16] ffreedom / Boss Wallah**
  - [ThePrint press release (languages, courses, mentors)](https://theprint.in/ani-press-releases/ffreedom-app-empowering-1-crore-indians-with-livelihood-education/1347923)
  - [App Store listing (Mentor-Connect)](https://apps.apple.com/in/app/ffreedom-app/id1445018395)
  - [Boss Wallah blog](https://blog.bosswallah.com/?p=6818)
  - [Inc42 acquisition](https://inc42.com/?p=502777)
- **[S17] Shark Tank India**
  - [SonyLIV Season 4 FAQ](https://prd-emss3.sonyliv.com/team_1/user_1/program_146/faq_shark_tank_s4_22012025.html)
  - [Season 6 FAQ](https://origin-staticv2.sonyliv.com/UI_icons/FAQ+final+Shark+Tank+India+Season+6_07.07.pdf)
  - [Velocity registration guide](https://blog.velocity.in/how-to-register-for-shark-tank-india/)
- **[S18] Pitch apps** (PitchConnectUs not found)
  - [PitchConnect concept](https://www.turbostarter.dev/ideas/social/pitchconnect)
  - [Pitch Me App](https://apps.apple.com/es/app/pitch-me-app/id6444131239)
  - [EI Connect](https://apps.apple.com/gb/app/eiconnect/id1594026333)
- **[S19] RBI P2P amendment, 16 Aug 2024**
  - [Moneylife](https://www.moneylife.in/article/rbi-tightens-regulations-for-nbfcp2p-lending-platforms/74936.html)
  - [Medianama](https://www.medianama.com/2024/08/223-rbi-bans-p2p-lending-companies-from-selling-loans-as-investments-in-new-guidelines/)
  - [Vinod Kothari](https://vinodkothari.com/2024/08/survival-at-stake-the-impact-of-rbis-norms-on-p2p-lending-platforms/)
  - [IndiaCorpLaw](https://indiacorplaw.in/2024/10/18/rbis-revised-master-directions-on-peer-to-peer-lending-shift-in-regulatory-policy/)
  - [Exposure limits (TaxGuru)](https://taxguru.in/rbi/p2p-lending-concept-regulations.html)
- **[S20]** [SEBI warning on crowdfunding platforms (Inc42)](https://inc42.com/buzz/sebi-warning-crowdfunding)
- **[S21] UPI one-time mandate** (block in own account, up to ~60 days)
  - [ICICI Bank](https://www.icici.bank.in/personal-banking/blogs/payments/mobile-banking/upi-one-time-mandate)
  - [PayU docs](https://docs.payu.in/docs/upi-one-time-mandate-integration)
  - [Pine Labs (OTM vs Reserve Pay)](https://www.pinelabs.com/docs/online-payments/one-time-mandate)
- **[S22]** [NPCI Hello! UPI voice payments (Business Today)](https://businesstoday.in/technology/news/story/hello-upi-npci-rolls-out-new-voice-enabled-payment-methods-and-more-features-check-details-397313-2023-09-07)
- **[S23]** Low-literacy mobile UX research
  - [Microsoft Research: Designing mobile interfaces for novice and low-literacy users](https://www.microsoft.com/en-us/research/?p=161317)
  - [Medhi et al., CHI 2009](https://microsoft.com/en-us/research/wp-content/uploads/2016/02/medhi_chi2009.pdf)
