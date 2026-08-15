# Campaign Plan — Data with Ejaz (paid ads diagnostic)
Generated: 2026-08-15

## Business
Ejaz Ahmed (Data with Ejaz) helps UK brands spend better on Meta and Google. Six years in agency paid media, 85+ brands, plus measurement (GA4) so the ads are not a black box.
Website: https://datawithejaz.com

## ICP
- Titles: Founder, Managing Director, Head of Marketing, Ecommerce Manager, Head of Growth
- Industries: UK retail / ecommerce / consumer (fashion, food, fitness, home, beauty)
- Headcount: 2–50
- Geography: United Kingdom only
- Hard filters: **Ltd or LLP only** (corporate subscriber under PECR). Company email, not Gmail. Already running Meta or Google ads in the UK (campaign 1), or a live store with no ads (campaign 2).
- Excluded: sole traders, agencies pitching *their* clients, in-house media teams at large groups, anyone who asks to be removed, existing/past employers

“People interested in paid ads” is not an ICP. The first list is people **already paying Meta or Google**. They have budget. They can tell in 15 minutes whether you are useful.

## Offer
- Primary CTA: 15-minute diagnostic
- Free hook: three specific notes on where the current ads are leaking spend, delivered on the call or as a short Loom if they cannot meet
- Delivery: their live ads (Meta Ad Library + site). You do not need their Ads Manager login for v1.

## Top 3 campaigns (pick #1 only)

1. **Active UK Meta advertisers** — list from Meta Ad Library (free). Open on a real ad they are running. Offer three notes. Best first campaign: intent is proven, research is free.
2. **New Head of Marketing / Ecommerce Manager** — started in role recently, inherited a messy account. Run this as campaign 2 once #1 has a baseline reply rate.
3. **Store with no ads** — Shopify/WooCommerce UK Ltd, no Ad Library presence. Harder close (no budget yet). Do not start here.

Full angles: see “Campaign ideas” below. Write copy for campaign 1 only.

## Infrastructure readiness
- [ ] SMARTLEAD_API_KEY in `.env`
- [ ] Sending domain bought (not datawithejaz.com)
- [ ] 2 commercial inboxes (Google Workspace or Microsoft 365 Business)
- [ ] SPF / DKIM / DMARC pass (`/email-deliverability-audit`)
- [ ] Inboxes warming 14 days
- [ ] Privacy policy live + UK address in footer
- [ ] Legitimate interests note saved (`uk-lia.md`)
- [ ] Calendly or equivalent 15-min slot
- [x] PROSPEO / Zapmail / Dynadot / Blitz / RapidAPI — **not this month**

See `budget-and-infra.md`.

## Next steps

**This week**
1. Buy domain + 2 commercial mailboxes. Connect Smartlead. Start warmup. Do not send campaigns.
2. Put a privacy page on datawithejaz.com and a real UK address in the signature.
3. Fill `legal.physical_address` in `client-profile.yaml`.
4. Build list #1 (`list-building.md`) to ~400–600 rows while you wait.

**Days 15–21**
5. `/list-quality-scorecard` on the CSV.
6. Load `campaigns/active-advertisers/variants.yaml` via `/smartlead-campaign-upload-public` (DRAFT). Start at 10/day/inbox.
7. Put `/cold-email-weekly-rhythm` on the calendar (Monday audit, Wednesday replies, Friday retro).

**Day 36 (21 days after first send)**
8. `/positive-reply-scoring`. If positive replies are weak, `/experiment-design` changing **one** variable (usually the list slice: fashion vs food, or founder vs ecommerce manager).

---

## Campaign ideas (budget-honest)

Ordered broad → niche. AI personalization here means **you** glancing at Ad Library + homepage, not Clay.

| Campaign | Level | List | Personalization | Value | Overview |
|---|---|---|---|---|---|
| Active Meta advertisers | Focused | UK Ltd, 2–50 people, ads live in Ad Library | Name one live ad or the product it sells | Save wasted spend | Email 1 cites a real ad. Offer three notes in 15 min. |
| Google Ads Transparency | Focused | Same size, ads visible in Google Ads Transparency Center | Name a search/display campaign theme | Same | Use if Meta list is thin. Same copy, swap the signal. |
| Creative Ideas (constrained) | Broad | Any ICP company with a shop | 3 ideas using only Meta, Google, or measurement | Make the next pound work harder | Follow-up only. Ideas must be things you actually do. |
| New marketing lead | Focused | Title change <90 days | Start date / previous company if public | Quick win in a new seat | Campaign 2. |
| Hiring a media buyer | Niche | Companies House / LinkedIn job for “paid social” / “Google Ads” | Quote the job | Fill the gap without a 3-month hire | Small list, high intent. |
| Lookalike of brands you have worked | Focused | UK brands in the same category as a named case (without leaking confidential figures) | “Similar to {public category} work” | Proof | Only if you can name a result that is already public. |
| No-AI billboard | Focused | Same as row 1, static copy | None | 15 min, three notes, no deck | Control variant. |
| Shopify, no ads | Niche | UK Ltd store, zero Ad Library hits | Homepage product | Start paid the unglamorous way | Campaign 3. Skip sole traders. |
| Founder posted about ROAS | Niche | LinkedIn post | Quote the post | Peer reply, not a pitch | Manual, 20–30 people. |
| Agency overflow (later) | Niche | Small UK paid-media agencies | Their client vertical | Extra pair of hands | Not month 1. Different ICP. |

### No-AI campaign
**Three notes, no login.** Why it works: the offer is the email. Subject can be the brand’s product or “your Meta ads”. Body is four sentences. Use this if Ad Library research per row is too slow.

### Front-end offer
The 15-minute diagnostic *is* the front-end. Do not ask them to “book a chemistry call.” Promise they leave with three notes even if you never work together.

---

## Skills to invoke in this repo

```
(you are here) campaign-plan
    → budget-and-infra          # buy domain + 2 inboxes, 14-day warmup
    → list-building             # Ad Library + Companies House, no Prospeo
    → /spam-word-checker        # already applied to copy in this folder
    → /list-quality-scorecard   # before upload
    → /smartlead-campaign-upload-public
    → /cold-email-weekly-rhythm
    → /positive-reply-scoring
```
