# Get Lucky — Project Plan & Operations

## What this project is

This repo runs, manages and **automates the operating Get Lucky Golf Club
business**. It is not an investor project.

As of 19 August 2026 the company is **two founders** — Johannes (product, money,
systems) and Andrew (Indwe, partnerships, golf days) — plus contractors. The
Activations, Promotions and Operations department closes **4 September 2026**.
Everything built here should reduce the work two people have to do by hand.

## The operating reality (read before proposing anything)

- **Indwe/Santam sponsorship is ~93% of revenue** (~R208k/month contracted).
  Renewing it for 2027 is close to an existential question.
- **Digital entry revenue is ~R7.3k/month** (157 paid entries, R29,200, May–Aug).
- **Membership is 48 subscribers.**
- The R1.5m of trailing entry revenue was **promoter-driven**, and promoters are
  gone. Replacing that with a digital channel is the whole Q4 job.

Do not plan against the investor model's forecasts. Plan against these numbers.

## Documents

| File | What it is |
|---|---|
| `GET-LUCKY-BACKGROUND.md` | Full history: company, commercial, financial, technical. Reference. |
| `FOUNDERS-RESET-Q4-2026.md` | Current operating plan — founder split, KPIs, Q4 focus, automation backlog. **Start here.** |

## Related repositories

| Repo | Role |
|---|---|
| `getluckyjo/getlucky-www` | **The live business.** getluckygolf.co.za — entry forms, PayFast, the Indwe lead API. Most automation work lands here. |
| `getluckyjo/investgetlucky` | Investor pitch site. **Reference only** — describes a raise that is parked and a partner who deferred. Do not update without being asked. |
| `getluckyjo/golf-day-pro` | Golf day booking marketplace |
| `getluckyjo/getlucky-subscriptions` | Membership sign-up (`membership.getluckygolfclub.com`) |

## Working rules

- **Cash and time are the constraints.** Prefer the change that takes hours over
  the one that takes weeks, unless the weeks-long one is the app.
- **Check the real data before asserting.** Gmail, Drive, PayFast notifications
  and the Get Lucky Form Submissions sheet are the source of truth on what is
  actually happening — not any deck or model.
- **Write decisions down.** One line, in the relevant doc, with the date.
- **Don't reintroduce the investment framing** into operating work.

## Stack

Next.js 16 · React 19 · TypeScript · Tailwind 4 · Supabase/Postgres · PayFast ·
Resend · Google Sheets (Apps Script) · Twilio WhatsApp · Vercel · Xero
