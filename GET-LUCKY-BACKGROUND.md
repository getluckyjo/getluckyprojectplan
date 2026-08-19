# Get Lucky Golf Club — Background

**Everything done to date, in one place.**
Compiled 19 August 2026 · Internal · Johannes Le Roux

---

## 0. What this is, and where it comes from

This is a consolidated background record of the Get Lucky Golf Club project — the
business, the commercial relationships, the money, the software, and the investor
story — assembled from four sources:

| Source | What was read |
|---|---|
| **Gmail** (johannes@getluckygolfclub.com) | Shareholder updates, investor correspondence, Indwe/Santam threads, partner negotiations, supplier and accounting threads, Mar 2025 → 19 Aug 2026 |
| **Google Drive** | Investor FAQ, Corient meeting prep, course agreements, use-of-funds workbooks, sales toolkits, trackers |
| **`getluckyjo/getlucky-www`** | 56 commits, May → Aug 2026 — the live public site and lead pipeline |
| **`getluckyjo/investgetlucky`** | 143 commits, Jul → Aug 2026 — the investor pitch site, financial model and dataroom; its `HANDOFF.md` is a 1,452-line decision log |

Where documents disagree — and they do, in several material places — the
disagreement is recorded rather than resolved. Those are collected in
[§11 Open issues](#11-open-issues-contradictions-and-decisions-outstanding).

---

## 1. The company at a glance

| | |
|---|---|
| **Legal name** | Get Lucky Golf Club (Pty) Ltd |
| **Registration** | 2025 / 047585 / 07 |
| **Financial year end** | 28 February |
| **Bank** | Capitec Business (account ending 6210) |
| **Accountants** | Luke Hahn CA(SA), Simplify IT (Pty) Ltd |
| **Founders** | Johannes Le Roux (Founder), Andrew Davenport (Founder) |
| **Contact** | johannes@getluckygolfclub.com · +27 60 961 5091 |

### People

| Person | Role | Notes |
|---|---|---|
| Johannes Le Roux | Founder | Product, story, investor lead, all software |
| Andrew Davenport | Founder | Commercial, partnerships, sales |
| Inus | Shareholder / early team | 10% at seed, subject to reverse-vesting to 5% |
| Michelle Wendy Hewitt | Shareholder | 26% at seed; active on SHA / AFS governance |
| Neil John Hewitt | Shareholder | Surrey Holmes |
| Willem (Willie) Ross | Strategic investor | Via Domino Capital; ex-Carlyle / JP Morgan, Harvard MBA; Bellair Road |
| Gerard Moodley | Head of Partnership | Course acquisition — signed Zimbali, Killarney, Victoria |
| Maxime Davenport | Head of Sales | sales@ — on notice as at Aug 2026 |
| Liezell Brits | Sales | Consultation/notice letter issued 7 Aug 2026 |

### Shareholding (seed, per cap table circulated 29 Jul 2026)

Johannes 30% · Andrew 30% · Michelle 26% · Inus 10% · Willie 5%

Willie Ross's original R1.8m came in and was later split into equity plus a
**R900k loan**; on 30 Jul 2026 he offered to convert that loan back to equity
(reverting to a 10% position) to reduce indebtedness.

### Digital estate

| Property | Purpose |
|---|---|
| `getluckygolf.co.za` | Primary public site (**`getlucky-www`**) |
| `getluckygolfclub.com` | Legacy site |
| `membership.getluckygolfclub.com` | Club-specific membership sign-up (`/join/<slug>`) |
| `simulator.getluckygolfclub.com` | Simulator challenge |
| `investgetlucky.vercel.app` | Investor pitch + dataroom (**`investgetlucky`**) |
| `erniexgetlucky.vercel.app` | The Ernie Els proposal page |
| `get-lucky-golf.vercel.app` | The golfer app (PWA prototype) |
| `golfdaypro.co.za` | Golf day booking marketplace |
| `golfsitepro.co.za` | Free AI-built websites for golf clubs |

Related repos in the same GitHub org: `get-lucky-golf`, `get-lucky-dashboard`,
`getlucky-subscriptions`, `golf-day-pro`, `epic-golf`, `indwe-microsite`,
`fairways-to-heaven`.

---

## 2. The product, as it stands today

The core proposition has been constant since inception and was **explicitly
re-affirmed on 18 August 2026** after a two-week detour (see §7):

> Commercialise the hole-in-one. One insured swing at a par-3, anywhere, for a
> prize that changes a life — sold shot by shot, with the prize underwritten by
> an insurer rather than pooled from players.

### How it is sold

1. **Installed courses (the proven engine).** Camera-verified rigs on the
   signature par-3 at premium courses. Golfer pays at the board / QR form.
   Local stake ladder: **R50 → R25,000 · R100 → R60,000 · R150 → R100,000 ·
   R250 → R200,000 · R500 → R500,000 · R1,000 → R1,000,000.**
2. **Membership.** **R149/month** locally ("Get Lucky Club"); the global plan is
   **$10/month including one insured swing a month at the $10,000 tier.**
3. **The app.** Pick any course and par-3, choose a stake, film the shot, submit
   for verification. USD ladder $1→$500 up to $100→$100,000.
4. **Simulators.** $1 entry / $1,000 insured prize, split 46 / 30 / 24
   (Get Lucky / operator / insurer). No hardware cost to Get Lucky.
5. **Golf days, corporate, charity, schools and tour operators** — bulk vouchers
   and activations, sold through the website.

### Unit economics

Entry splits **66 / 10 / 24** — Get Lucky gross profit / course share /
insurance premium ceded. Membership retains 74.9% after the $2.51 premium ceded
on the single included swing.

### Why the membership allowance is capped at one swing

This is the single most important structural decision in the business and it is
underwriting, not marketing. From the Santam submission
(`GetLucky_Insurance_Model.xlsx`), reproduced independently:

| | |
|---|---|
| Ace probability per attempt | 8 × 10⁻⁵ (1 in 12,500) |
| Weighted average entry | $17.00 |
| Premium per entry | $4.08 (24%) |
| Expected claim per entry | $1.30 |
| **Loss ratio** | **31.9%** |
| Combined ratio | 51.9% |
| Breakeven | aces would need to occur **2.51×** more often than amateur odds |
| Cover | 100%, brokered by Indwe, 20% broker commission |

At **one** included swing a month: expected claim $0.80, premium ceded $2.51 on
a $10 fee. At **four** included swings the ceded premium is $10.03 — the entire
membership fee. An *unlimited* allowance (16 attempts/month at the $10,000 tier)
runs a **533% loss ratio**. That is why "unlimited swings" was withdrawn and must
not come back.

### Regulatory position

Structured as a **skill-based competition, not gambling**: no randomness, no
wagering against odds, no player-pooled prize. Prizes are pre-funded and fully
insured. Peer side-games (skins, dots) ship as a **free** feature — Get Lucky
takes no rake and holds no pot, ever, because a fee is exactly what kills South
Africa's informal-bet exemption (NGA s4) and drew a cease-and-desist against
BetOpenly in Arizona on a 1% commission.

---

## 3. Timeline

### 2025 — acquisition and launch

- **Mar 2025** — Due diligence completed on the acquisition of the only
  meaningful local competitor; rebranded into Get Lucky, consolidating the SA
  market from day one. Knysna club manager comes on board; course listings begin.
- **Jul 2025 → Dec 2025** — First operating half. Monthly revenue climbs from
  **R10,000 in July to R250,000 in December.**
- Camera and installation assets built to roughly **R1.0m**; ~20 permanent
  installations nationwide.
- **Santam / Indwe headline sponsorship signed: R9m over three years** —
  R2.5m (Y1) · R3.0m (Y2) · R3.5m (Y3). Indwe Risk Services (est. 1903,
  Santam-backed) is the broker and headline sponsor; Get Lucky supplies access to
  an affluent golfer audience (average net worth quoted north of R14m) and Indwe
  converts them to advisory clients.
- Shanky's Whip commits **1,800 bottles for 2025 (~R900k sponsorship value)** for
  promo-day activations.

### Early 2026 — the honest re-think

The **17 April 2026 shareholder update** is the pivot point of the whole story.
After 20 premium clubs, 10,000+ rounds of data and 500+ activations, five
structural problems were named openly:

1. Passive entries are rare — golfers walk past the board.
2. Promotions work but are expensive and weather/field dependent.
3. Golf days lock Get Lucky out of its own par-3.
4. Golf days are simultaneously the biggest opportunity — but the conversation
   happens before the event comms go out, and Get Lucky wasn't in it.
5. A digital brand with no digital product is burning money.

Everything built since answers one of those five.

What was launched off the back of it:

- **New website** (later `getlucky-www`) positioning Get Lucky as an integrated
  golf marketing platform.
- **Membership** — 10 club-specific sign-up pages built (Metropolitan, Clovelly,
  Paarl, Boschenmeer, Atlantic Beach, Bellville, Durbanville, Rondebosch,
  Mossel Bay, Goose Valley). Target 800 paid members / ~R1m ARR.
- **The Get Lucky App** — pick course + par-3, choose stake, film, submit.
  Targeted June 2026 launch.
- **Get Lucky Golf Show** — 15-episode celebrity series (Maps Maponyane, Jack
  Parow, Jacques Kallis; hosted by Nich Hamman). **FlySafair** pitched as
  Official Airline Partner, 3 years, ~R1.425m (R95k/episode).
- **Nedbank SA Amateurs** — Official Hole-in-One Challenge Partner. First event
  Wild Coast Sun, 19–22 April 2026; second Sun City, October 2026.
- **Golf Day Pro** — the "Booking.com of golf days". 450+ SA clubs, ~6,750 golf
  days/year, a R2–4bn market. Get Lucky earns ~5% and holds float 30+ days.
  The hole-in-one challenge is an add-on inside the booking flow.
- **Golf Site Pro** — free AI-generated websites for clubs (Port Shepstone,
  Metropolitan, Wanderers live) as distribution infrastructure.
- **Simulator proof-of-concept** — rent-free office space, 50% profit share.

### May → July 2026 — build and commercialise

- **12 May** — `getlucky-www` repo initialised; the live site moves under version
  control. (During the same cleanup pass, iCloud was found to be **corrupting the
  git repositories** — SIGBUS on `.git` files — and all four repos were relocated
  to `~/dev/getlucky/`.)
- **29 Apr** — Zimbali Country Club signed. **27–28 May** — Victoria Golf Course
  agreement negotiated (restraint-of-trade carve-outs for existing golf days).
- **2 Jun** — Draft FY26 Annual Financial Statements issued by Luke Hahn CA(SA).
- **8–18 Jun** — Shareholders' Agreement amended through three rounds of Michelle
  Hewitt's review (dilution, minority protections cl. 9.3/11, 14.3.2, 19.5).
- **26 Jun** — First contact with **Corient** (Paul Weldon) on the Ernie Els
  partnership. **8 Jul** — introduced to Stuart Makin (Cape Town partner).
- **13 Jul** — `investgetlucky` repo created; investor pitch site built.
- **20 Jul** — Corient meeting in Claremont (Johannes, Andrew, Willie).
- **28 Jul** — The hard shareholder update (below).
- **29 Jul** — "Ernie Els is officially in" note to Indwe leadership.

### August 2026 — bridge, pivot, un-pivot, and the Ernie answer

- **3 Aug** — Grapevine (Vine) engaged on WhatsApp requirements via Indwe intro.
- **4 Aug** — **R400,000 bridge loan** signed and funded: R200k each from Willie
  Ross and Michelle Hewitt, no interest, to be repaid from the Indwe invoice.
- **5–7 Aug** — The investor site is rebuilt twice (see §7).
- **6 Aug** — Dataroom NDA gate replaced with notify-on-open via Resend from
  `dataroom@getluckygolfclub.com`.
- **10–12 Aug** — WhatsApp Business API RFQ issued to five vendors (Everlytic,
  Clickatell, Pivotal Data, Cellfind, ReachMax); Cellfind engages first.
- **11 Aug** — Twilio sender profile registered (confirmed 18 Aug).
- **13–17 Aug** — WhatsApp opt-in capture shipped on the live entry forms.
- **13 Aug** — MOVE Golf approached re the PGA Show; meeting held 18 Aug.
- **14 Aug** — **Epic Golf** partnership: first fully digital Hole-in-1 Challenge
  on simulators; Juniper Sky (Roxanne) briefed on campaign creative; Epic Golf
  golf day booked for 16 October (4 bays, ~20–40 players).
- **17 Aug** — Storesmart storage unit 1117 given notice, vacating 31 August.
- **18 Aug** — **The core is re-asserted: the hole-in-one is the business again.**
  Model, site, plan and all seven dataroom PDFs rebuilt.
- **18 Aug** — **Corient reverts on Ernie Els.** See below.
- **19 Aug** — Site-wide password gate shipped on the investor site; handover
  documentation folder circulated to the team.

---

## 4. The Ernie Els partnership — the full arc

This deserves its own section because most of the investor material is built on
it, and its status changed four days ago.

**The proposal.** Ernie Els as **Founding Partner** — name, likeness and network,
for **5% non-diluting equity**. No cash, no directorship, no guarantee, no time
obligation beyond up to two days a year at his election. If he terminates for
Get Lucky's fault he keeps the stake; the licence ends, the shareholding
survives and is transmissible to his estate. Framed as: *"He doesn't endorse this
business. He owns part of it."*

**The route.** Corient — Paul Weldon (introduced 26 Jun) and Stuart Makin
(Cape Town). A parallel channel to Piet Pieters at Ernie Els Group also existed.

**The progression.**

| Date | Event |
|---|---|
| 26 Jun 2026 | One-pagers and valuation model sent to Paul Weldon |
| 2 Jul | Paul to sit with Ernie after the Senior US Open |
| 8 Jul | Introduced to Stuart Makin |
| 20 Jul | Claremont meeting (prep doc in Drive) |
| 28 Jul | Shareholder update: *"Ernie has agreed to come on board as a founding partner"* — awaiting agreements |
| 29 Jul | Johannes to Willie: *"more than a loose expression of interest, but not yet signed"* |
| 29 Jul | Announced to Indwe leadership as officially backing the challenge |
| 13 Aug | Follow-up to Stuart and Paul: holding the allocation, offering to fly to meet Ernie |
| **18 Aug** | **Stuart Makin reverts** |

**The 18 August answer, verbatim in substance:** the proposal was discussed with
Ernie and his Board at some length; *"He loves the concept and immediately saw the
potential link up with insurance companies in particular."* But **due to his full
playing schedule and extensive sponsor commitments he does not feel he can give
the project the attention it deserves at this stage.** He asked to be kept abreast
of progress, with a possible in-person reconvening **when he is back in South
Africa in December**.

**What this means, plainly.** It is a deferral rather than a refusal, but it is
not a commitment. Every investor surface currently describes Ernie as a founding
partner holding 5% non-diluting — the investor site, the business plan, all seven
dataroom PDFs, the Ace Registry naming, `data/model.json`, and the shareholder
communications of 28–29 July. **None of that has been updated.** The 19 August
password gate on `investgetlucky.vercel.app` limits the exposure but does not
resolve it. This is the highest-priority open item in §11.

*Note also flagged in the project record:* the Ernie photography used on the site
carries third-party sponsor branding (EY, SAP, Boeing, Stanley, Srixon, XXIO) and
usage rights were never confirmed.

---

## 5. Commercial relationships

### Sponsors and partners

| Partner | Status | Detail |
|---|---|---|
| **Indwe Risk Services / Santam** | **Contracted** | R9m / 3 years headline sponsorship (R2.5m → R3.0m → R3.5m). Indwe brokers the prize cover; Santam underwrites (Authorised FSP 3416; Indwe is FSP 3425). Weekly "STATUS UPDATE: GLG \| Indwe \| Stratitude" governance call. |
| **Shanky's Whip** | Delivered | 1,800 bottles for 2025, ~R900k value, promo-day activation |
| **Nedbank SA Amateurs** | Delivered | Official Hole-in-One Challenge Partner; Wild Coast Sun Apr 2026, Sun City Oct 2026 |
| **FlySafair** | Verbal, unconfirmed | Get Lucky Golf Show anchor, ~R95k/episode × 15 |
| **Epic Golf** | Active | First fully digital simulator challenge; golf day 16 Oct 2026 |
| **MOVE Golf** | In discussion | Simulator partner for the PGA Show stand |
| **Blu Label Tour** | Agreement drafted | May 2026 |
| **Grapevine (Vine)** | Quoting | WhatsApp journey build, introduced by Indwe |
| **Golfzon and other sim operators** | **Target only — nothing signed** | 7 named target operators; the route was Ernie's relationships |
| **Cloud & Things** | Named technology partner | SA engineering firm, AWS partner, led by the former CTO of Capitec Bank |
| **Juniper Sky (Roxanne)** | Retained | Campaign creative |
| **Pomme Express (Zaida)** | Active | PGA Golf & Lifestyle Show promotion (~23,000 views on early social) |

### Courses

**25 premium courses installed** as at mid-2026. Named in the site and model:
Atlantic Beach · Bellville · Boschenmeer (17th + 23rd) · Centurion · Clovelly ·
Durbanville · East London · Goose Valley · Graceland · Highland Gate · Killarney ·
Metropolitan (9th + 18th) · Mossel Bay · Mount Edgecombe · Paarl · Rondebosch ·
San Lameer · Serengeti · St Francis Links · State Mines · Umhlali · Victoria ·
Wild Coast · Zimbali. Durban Country Club was installing as at July.

**Terms:** exclusive, 2-year auto-renewing, **10% revenue share** on paid entries,
2-year restraint of trade, no upfront cost to the club, Get Lucky covers
installation, insurance, technology and operations. Generally one signature par-3
per club; two live holes at both Metropolitan and Boschenmeer.

### Channels built into the website

Corporate golf days · Charity golf days (with fundraising calculator) ·
School fundraising · Golf tour operators · Golf simulators · Agency ·
Become-a-partner (course acquisition) · Buy-a-swing vouchers · Free entry.

### Pay Before You Play

The margin fix, launched July 2026: instead of stationing a promoter at the hole
all day, the promoter pitches in the pro shop/clubhouse at check-in — while
golfers are waiting and receptive rather than mid-round. **Roughly 60% cost
reduction**, rolling out across 200+ golf days over five months.

---

## 6. The numbers

### Actual trailing twelve months (Jul 2025 → Jul 2026)

| | |
|---|---|
| Turnover | **R4.0m** — R2.5m contracted sponsorship + R1.5m entries |
| Paid entries | **10,000** at a realised average of **R150** |
| Course activations | **800** |
| Members reached | 60,000 |
| Installed courses | 25 |
| Capital invested to date | R3.0m |
| Camera/installation assets | ~R1.0m |
| Aces paid out | 5 |
| **Paid subscribers** | **48** (as at 28 Jul 2026) |

The 48-subscriber figure matters more than its size suggests: it is the single
piece of evidence that eventually forced the August un-pivot, because the model
at the time forecast 100,183 subscribers.

### Promotional-day behaviour

Money-back-if-you-hit-the-green promo days roughly **double entries**, and about
**25% of entrants hit the green** — which validates both the offer and its cost.

### Current forecast (built by `scripts/model.py`, 72-month build from Jan 2027)

> Everything below is **forecast**, not history. Members start at zero in
> January 2027.

| | 2027 | 2029 | 2032 |
|---|---|---|---|
| Revenue | R12.3m | R71.7m | R277.5m |
| Cost | R14.7m | R56.9m | R185.9m |
| EBITDA | −R2.4m | R14.9m | R91.6m |
| EBITDA margin | −19.3% | 20.7% | 33.0% |
| Members (closing) | 3,749 | 22,694 | 75,555 |
| Insured swings | 29,076 | 218,988 | 913,519 |
| **Ace revenue share** | **44.1%** | **70.8%** | **81.6%** |

Build-year cash need **R5.87m** against the R8m round; peak cumulative drawdown
R6.03m in 2027; EBITDA-positive from 2028, cash-positive from 2029.

### Supporting streams in the plan

- **Simulators** — attach rate applied only to South Korea's ~94M annual sim
  rounds: 0.3% (2027) → 1.5% (2029) → 4.0% (2032), giving R2.4m → R12.0m → R32.0m
  to Get Lucky at ~42% EBITDA margin. Nothing signed.
- **Territory sponsorship** — US from 2029 (R2.0m → R4.0m), Europe from 2030
  (R3.0m), Japan from 2031 (R2.0m). Sized deliberately *below* the SA run-rate at
  entry. SA sponsorship held flat at R3.5m after the deal expires in 2028 and is
  never extrapolated.

### The round

**R8.0m for 15% — R45.3m pre / R53.3m post.** Minimum ticket R1m; R1m buys 1.88%.
Valuation milestones at a flat **3.0× revenue** at every forward point:
R53.3m (round) → R215.2m (2029) → R832.5m (2032). Investor multiple 4.04× to
2029, 15.61× to 2032; IRR ~59% on a Q4-2026-in / Dec-2029 basis. Entry multiple
4.33×, so the multiple *compresses*. Multiple sensitivity is published
(2.5× / 3.0× / 3.5× → 3.36× / 4.04× / 4.71×).

**Use of funds:** app & Ace Registry 30% · market entry & brand 25% ·
legal & ops 20% · simulators 15% · 90-day pilot 10%.

---

## 7. `investgetlucky` — the investor site, and how the story moved

143 commits between 13 July and 19 August 2026. `HANDOFF.md` in that repo is the
authoritative decision log; this is the compressed version, because the *sequence*
matters as much as the destination.

**What it is:** a static site (no build step) — `index.html` public pitch,
`dataroom.html` gated documents, `demo.html` a tappable MVP of the app.
The forecast is **built, not typed**: `scripts/model.py` runs the driver model and
writes `data/model.json`; every published figure is then checked by
`scripts/tie-out.py`, which grew from 41 to **103 checks** and fails the build on
any surface still carrying a superseded number.

### The arc, in order

| Date | Move |
|---|---|
| 13–14 Jul | v1 built: 15-section pitch, NDA dataroom, brand restyle, Ernie treatment, app-demo phone. Round: **R4m for 10% at R40m.** Project paused 14 Jul. |
| 4 Aug | **Repriced to R8m for 15%.** Simulator channel modelled in. Then simulators moved from "growth engine" into the **core plan**; territory sponsorship added; in-play upsells added as a fourth stream; independent DCF removed. |
| 4 Aug (later) | Cost base *raised* rather than revenue cut — opex R350k → R450k/month — because the founder chose to fund the plan rather than shrink it. Valuation multiple walked 2.744 → 2.5 → 3.5 → **3.0**, and the IRR travelled 34 → 36 → 40 → 36 → 52 → 44 across a single day. |
| 5 Aug | **Three-reviewer investor-readiness audit.** It found real bugs: the insurance premium was **double-deducted**, SA sponsorship had been **extrapolated to 9× the contracted amount** inside a stream labelled "contracted", rungs 1 and 2 contributed **R0** to a forecast that led the page, and the calculator silently republished a withdrawn price when `model.json` failed to load. All fixed. The model was rebuilt, not patched. |
| 5 Aug | The **capped-allowance** resolution: "unlimited" was the problem, not "subscription". |
| 5 Aug (v3–v6) | Founder review applied — build start moved to Jan 2027, play frequency cut 4 → 2 rounds/month, installed courses modelled as a real line. IRR fell 41.7% → 28.5%. Repriced to hold 40% (16.9% at R47.3m), then the "arrived-at not solved-for" pass removed six reverse-engineering tells, then **reinstated R8m for 15%** and accepted ~34%. |
| **5–6 Aug (v7–v9)** | **The pivot.** Peer-to-peer golf games ("a golf day in your pocket") became the core product, with the ace demoted to *"the jackpot on the slip — the lottery ticket at the till."* Business plan, model, site and dataroom all rebuilt around it. |
| 7 Aug | App requirements master spec written (§0–§26, 34-screen inventory, 15 end-to-end flows) plus the tappable investor demo. |
| **18 Aug (v14)** | **The un-pivot.** *"We have overcomplicated the core goal of the business — to commercialise hole-in-one's globally. We want to own & reward hole in one's."* |
| 19 Aug (v15) | Site-wide password gate. |

### Why the un-pivot was right, on the evidence in the record

1. The proposal **Ernie actually agreed to** (`erniexgetlucky.vercel.app`) is a
   pure global hole-in-one business. No skins anywhere in it.
2. Johannes's own words to Indwe on 29 July: *"the mobile challenge is the
   engine: one shot at a hole-in-one on every Par 3, anywhere in the world, sold
   shot by shot."*
3. Investors kept repeating the same sentence back: a wager on a hole-in-one that
   could be life changing.
4. **48 subscribers against a 100,183 forecast.** The subscription-led plan was
   the least-evidenced part of the business; the ace had taken real money 10,000
   times.

Tie-out now bans the demotion vocabulary outright and **fails the build if the
ace drops below 60% of 2032 revenue** — the drift cannot recur silently.

### What the site says today

Sequence: the moment → the wager → the Global Ace Jackpot → **the Ernie Els Ace
Registry** → proof → the premium engine → Ernie → market → numbers → risk → deal
→ team → FAQ. Hero: **"We own the hole-in-one."**

The **Ace Registry** is the flagship funded pillar: digitise every clubhouse
honours board under Ernie's name and record every ace anywhere, entered or not,
with a live global ace feed in the app. It is positioned as both the acquisition
engine and a data asset no competitor or insurer holds. **No club, union or
federation agreement is signed** — the site says so in three places.

### Published gating milestones

1. Santam written sign-off on the membership's included insured swing
2. Ernie Els counsel sign-off on registry naming and brand use
3. First registry partnerships signed with clubs and unions
4. Geo-gating feature flags from first commit
5. **90-day pilot across the 25 installed courses** measuring swings per member
   per month — the decisive metric, modelled at 1 included swing (55% redeemed)
   plus 0.5 paid swings at maturity

---

## 8. `getlucky-www` — the live site and lead machine

56 commits, 12 May → 17 Aug 2026. This is the operating system of the commercial
business, not a brochure.

**Stack:** Next.js 16 (App Router) · React 19 · TypeScript · Tailwind 4 ·
Resend (email) · PayFast (payments) · Supabase/Postgres · Google Sheets via an
Apps Script webhook · Vercel. Node pinned to 22.x.

**Pages:** home · buy-a-swing · form / form-2 (activation entry) ·
become-a-partner · corporate-golf-days · charity-golf-days · school-fundraising ·
golf-simulators · golf-tours · agency · terms · privacy.

**Twelve form endpoints** feed one pipeline: entry, free-entry, voucher,
membership, partner, corporate, charity, school, simulator, tour, agency,
risk-review.

**Calculators built as sales tools:** golf-day, charity fundraising, tour
revenue, simulator revenue.

### The Indwe lead feed

A documented, authenticated partner API — `GET /api/indwe/leads` with a Bearer
token, optional `since` and `type` filters, no pagination or webhooks by design.
Every lead captured across the website and on-course QR forms is returned as
normalised JSON. Built out over ten commits:

- Partial-result handling when one Apps Script type fails
- Agency leads excluded from the sponsor feed
- Risk-review submission pipeline from the Indwe microsite
- Membership leads folded in, with entry source recorded
- Leads sent **regardless of payment status**
- Every lead **tagged with a qualification tier**
- Address captured on risk-review; quote CTA linked to the Indwe microsite

### Engineering history worth knowing

- **PayFast** — canonical field order (`email_address` before `cell_number`),
  PHP-compatible encoding of `!'()*~`, ITN source-IP validation (fail-open) on top
  of signature and server-side postback, and a **daily health canary** at 06:00 UTC
  with a cross-app aggregate.
- **June cleanup pass** (7 phases): `googleapis` removed (~194MB, unused),
  vulnerabilities 7 → 2, lint fixed (it had been silently broken), orphaned
  components deleted, env-var audit clean with no secret leak, Node pinned.
- **Supabase migration** Phase A (Postgres as durable system-of-record) then
  Phase B (PayFast notify + lead-API reads move to Postgres) — closing the
  "paid and PII data lives in a Google Sheet" risk raised in the cleanup.
- **GA4 + GTM + Google Ads** conversion tracking site-wide
  (AW-18144302506 / G-J5E9QM1F7L / GTM-T7JGF7M2), with a full Google Ads campaign
  build (campaign, ad groups, keywords, negatives, ads, sitelinks) in `docs/`.
- **Full T&Cs and POPIA privacy notice** published 28 May.
- **WhatsApp opt-in** captured on the entry forms (13 Aug), reduced to a single
  consent question that says what the WhatsApp is for (17 Aug).

### Outstanding from the cleanup

Confirm `main` branch protection; detach the unused Vercel KV integration; remove
stale `CRON_SECRET` / `KV_REST_API_*`; fix four surfaced React lint errors; add
security headers (CSP, X-Frame-Options) in `next.config`.

---

## 9. Money and governance

### Funding to date

- **R3.0m** of capital invested across founders, family and Willie Ross
  (originally R1.8m, later split into equity plus a **R900k loan**).
- **R400k bridge loan**, 4 Aug 2026 — R200k each from Willie Ross and Michelle
  Hewitt, no interest, to be repaid from the **R625k Indwe invoice due 1 October**.
- **Capitec overdraft** of R100k was the only external offer, requiring director
  surety. Not taken.

### The 28 July 2026 shareholder update — the honest one

Sent to Willie Ross, Michelle and Neil Hewitt. Headline items:

- Ernie Els agreed as founding partner (awaiting agreements)
- Raise of **R4m at R40m** unlocked by it
- **The capital gap named plainly:** R500,000 of two-month operating costs against
  R100,000 of conservative winter income — a **R400,000** net requirement
- Anti-dilution protection offered to shareholders who bridged (15% total —
  5% Ernie, 10% the raise)
- Salary line: R335k over two months — Commercial Manager R100k, Marketing Manager
  R100k, Operations Manager R60k, Promotions Manager R20k, plus R55k for July
- Everything else moving: Pay Before You Play, the PGA Show, Golf Day Pro,
  FlySafair, and membership at 48 subscribers held back by course-director red tape

### Willie Ross's position (30 July 2026) — treat as a live constraint

1. **Ernie** — "understood and well done on this. Could of course be
   transformational for us."
2. **Salaries** — the opex base must be aligned with *sustainable* income, and
   that alignment is a **precondition to committing further capital**.
3. **Anti-dilution** — support it for Ernie, but do not use it as a lever going
   forward.
4. **Timing of the raise** — *"my preference would be to delay another external
   raise for as long as possible… bootstrap/raise internally until we have proof
   of concept on the global platform and then go to market, perhaps in H1 2027.
   Proof of concept + Ernie will be a powerful catalyst for valuation uplift.
   Think we will all leave a lot on the table if we go to market now."*
5. **The R900k loan** — open to converting it back to a 10% equity position.
6. **Insurance** — wants the cost of moving to **100% cover** quantified so the
   company carries no existential risk.

Point 4 sits directly against the investor site, which is built and priced to go
to market now.

### Accounting and legal

- **FY26 draft AFS** compiled by Luke Hahn CA(SA), issued 2 June, no changes
  requested by 17 July; **independent review agreed** but management accounts need
  updating.
- **Shareholders' Agreement** amended through Michelle Hewitt's reviews
  (dilution, minority protections, cl. 9.3/11, 14.3.2, 19.5).
- Xero reconciled April 2026; Andrew's loan-account and salary entries
  reconciled against the Capitec/ABSA record.
- **SARS Tax Clearance (TCS)** outstanding — a recurring item on the weekly
  GLG/Indwe/Stratitude status list.

### Cost reduction, August 2026

Liezell Brits issued a consultation and notice letter (7 Aug); Maxime Davenport
gave notice on the unit; **handover documentation and trackers were prepared and
shared on 19 August**; the Storesmart storage unit is vacated 31 August.

---

## 10. Live workstreams as at 19 August 2026

| Workstream | Status |
|---|---|
| PGA Golf & Lifestyle Show, 18–21 Sept | Free R50k stand secured in exchange for a simulator with a R25,000 hole-in-one shot for every attendee; simulator partner (MOVE Golf / Epic Golf) doing setup for exposure; ~8,000 attendees |
| Epic Golf digital challenge | First fully digital challenge; creative in final rounds with Juniper Sky; golf day 16 Oct |
| WhatsApp Business API | Twilio sender registered 18 Aug; opt-in live on the forms; five vendor quotes out; Grapevine engaged via Indwe |
| Dawn Heights Annual Golf Day | 28 Aug, Mt Edgecombe — flyer approved, Indwe co-branded |
| Indwe complimentary 12-month membership | Call script delivered 14 Aug |
| Santam global underwriting | Meeting held with Indwe CEO; "Hole in One Query" escalated to Joe Szemerei (Chief Underwriting); awaiting process and treaty limits |
| Golf Day Pro | Live and quoting; corporate pitching underway |
| Membership | 48 paid subscribers; PayFast recurring collections running daily |
| Investor dataroom | Live, password-gated 19 Aug, notify-on-open by email |
| Team handover | Documents and tracker circulated 19 Aug |

---

## 11. Open issues, contradictions and decisions outstanding

Ordered by how much damage they do if left alone.

### Critical

1. **Ernie Els is no longer a commitment, and every investor surface still says he
   is.** The 18 Aug Corient reply defers to December. The investor site, business
   plan, all seven dataroom PDFs, `model.json`, the Ace Registry naming and the
   28–29 July shareholder and Indwe communications all describe him as a founding
   partner holding 5% non-diluting. This needs a decision — restructure the story
   without him, or hold the raise until December — and then a correction to
   shareholders and to Indwe, who were told he was officially in.

2. **The price disagrees across live documents.** `erniexgetlucky.vercel.app`
   prints R40M → R96.8M → R500M; the 28 July shareholder letter says R4M at a R40M
   valuation; the investor site says R8.0m at R53.3m post. Corient, the
   shareholders and Ernie's page all hold different numbers.

3. **The lead investor's stated preference is to delay the raise to H1 2027.**
   Unresolved against a site built and priced to go to market now, and against
   Willie's precondition that the opex base be aligned with sustainable income
   before he commits further capital.

### Material

4. **The insurance submission and the investment plan describe different
   companies.** The Santam submission carries a 200,000-player Ernie Partner
   Network reaching 144,091 registered players and R403m of year-3 entry revenue;
   the investment plan has no partner network and reaches 22,694 members. Both are
   36-month views of the same business. If an insurer and an investor ever compare
   documents, that gap needs an answer.

5. **Cap table wording.** "90% founder ownership" predates Ernie's 5% and the 15%
   round (founder ~76.5% if Ernie holds 5% pre-round). Confirm before any investor
   call.

6. **Figures still disagreeing across surfaces:** 20,000 members (Ernie deck) vs
   60,000 reached (site); "Top 100 courses live" vs 25 installed; 78% gross margin
   (Ernie deck) vs 66% retained.

7. **Documents confirmed available but still not published in the dataroom:**
   cap table, management accounts, the signed Santam agreement, and the written
   legal opinion. Each one closes a named reviewer finding.

8. **The existing hole-in-one legal opinion does not cover peer-to-peer play.**
   Relevant if skins ever move beyond a free, no-fee feature.

9. **Insurance cover level.** Willie Ross asked for the cost of moving to 100%
   cover to remove existential risk. Not yet quantified.

10. **Real traction is absent from the pitch:** golfdaypro.co.za, the FlySafair
    show deal, and the PGA Show launch pad are not in the investor material.

### Housekeeping

11. `SITE_PASSWORD` is not yet set in Vercel on `investgetlucky` — until it is,
    the gate is deterrence against a forwarded link, not access control, and the
    fallback digest is forgeable from the public repo.
12. `GetLucky_Business_Plan.md` and `INVESTOR-REVIEW.md` sit at the repo root and
    are publicly fetchable on the deploy — a one-line `.vercelignore` fix if
    unintended.
13. Ernie photography carries third-party sponsor branding with unconfirmed usage
    rights.
14. `assets/video/golf-day.mp4` is 14.2MB, unverified and uncompressed (no H.264
    decoder in the build container) — confirm playback, generate a poster,
    re-encode before launch.
15. `getlucky-www`: branch protection, Vercel KV detach, stale env vars, four lint
    errors, security headers.
16. The Get Lucky App concept screens are still concepts — real screenshots and a
    walkthrough video remain an asset ask.
17. SARS Tax Clearance certificate outstanding.

---

## 12. The through-line

Three things are worth holding onto from all of the above.

**The product has never actually changed.** From the March 2025 acquisition to the
18 August 2026 re-assertion, the business has been one thing: sell a golfer one
insured swing at a hole-in-one. Everything that felt like a pivot — the
membership, the app, the simulator channel, Golf Day Pro, the peer-to-peer
detour — was an attempt to fix a distribution or margin problem around that
transaction. The two-week experiment that demoted the ace to a jackpot on a bet
slip is the only time the core was genuinely at risk, and the evidence pulled it
back within a fortnight.

**The evidence is lopsided, and honestly so.** 10,000 people have paid for a swing.
48 people have paid for a subscription. Every forecast that leans on subscription
growth is the least-evidenced part of the plan, which is exactly why the 90-day
pilot across the 25 installed courses — measuring swings per member per month —
is the milestone that matters more than any of the valuation arithmetic.

**The discipline built around the numbers is the real asset in the repos.** The
model is generated from drivers rather than typed; 103 automated checks fail the
build if any published surface drifts from it; the double-deducted premium, the
9× sponsorship extrapolation and the silently-republished withdrawn price were all
caught by review rather than by an investor. That machinery is what makes the next
version of the story defensible, whoever the amplifier turns out to be.

---

*Sources: Gmail (johannes@getluckygolfclub.com, Mar 2025 – 19 Aug 2026) ·
Google Drive · `getluckyjo/getlucky-www` @ 2ed8b7b · `getluckyjo/investgetlucky`
@ ce08763 (incl. `HANDOFF.md`, `GetLucky_Business_Plan.md`, `data/model.json`,
`INVESTOR-REVIEW.md`).*
