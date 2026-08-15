# List 1 — UK Ltd companies already running Meta ads

Goal: 400–600 rows before day 15. Cost: £0 plus a few dollars to verify emails.

Prospeo / Disco-like / Blitz / Google Maps skills in this repo stay unused until the budget grows. They would blow the $100 cap.

## Who is on the list

Keep a row only if **all** of these are true:

1. UK presence (site, Companies House, or ads delivered to GB)
2. Limited company or LLP (Companies House). **Drop sole traders** — PECR treats them like consumers.
3. 2–50 people (LinkedIn company page or a sane guess from the site)
4. Founder / MD / Head of Marketing / Ecommerce Manager email at the **company domain**
5. At least one **active** Meta ad targeting or visible in the UK (Ad Library)

Drop: agencies, recruiters, large PLC in-house teams, `@gmail.com` / `@hotmail.com`, anyone who already knows you.

## Build it (about 4–6 hours, spread across warmup)

### A. Find advertisers (free)

1. Open [Meta Ad Library](https://www.facebook.com/ads/library) → country **United Kingdom** → category **All ads**.
2. Search product/category terms you can actually help: `skincare`, `protein powder`, `kitchenware`, `kids clothes`, `mattress`, `coffee subscription`, `gym wear`, `vitamin`, `pet food`.
3. For each advertiser with a real shop (not a dropship ghost):
   - Copy Page name, a link to one live ad, and the destination URL.
   - Skip if the only ads are job ads or app-install spam.
4. Optional second source: [Google Ads Transparency Center](https://adstransparency.google.com/) for the same brand names.
5. Optional third source: your own memory of UK Shopify stores in categories you have bought media for.

Stop at ~250 **companies**. You do not need 2,000. Two inboxes cannot send that many safely this month.

### B. Confirm they are a company (free)

For each domain, search [Companies House](https://find-and-update.company-information.service.gov.uk/):

- Active Ltd or LLP → keep. Note company number.
- Dissolved / sole trader / no match → drop.

### C. Find the person (free / cheap)

Order of operations:

1. Website `/about`, `/team`, footer, LinkedIn company “People”.
2. Title match from `client-profile.yaml`. Prefer Founder at <15 people; Head of Marketing / Ecommerce Manager at 15–50.
3. Email pattern from the site or a hunter-style lookup. Typical UK patterns: `first@`, `first.last@`.
4. Verify with MillionVerifier (or similar) **before** Smartlead. Unverified catch-alls bounce and kill a new domain.

If you cannot find a company-domain email, skip the row. Do not guess `info@` for cold personal outreach.

### D. CSV columns (Smartlead + scorecard)

```text
email,first_name,last_name,job_title,company_name,company_domain,company_industry,company_headcount,linkedin_url,ad_example,product_hook
```

- `ad_example`: one-line description of a live ad (“the blue serum UGC on Reels”).
- `product_hook`: what they sell in 3–5 words.

Save as `profiles/datawithejaz/lists/uk-meta-advertisers.csv` (that folder is gitignored). Do not commit emails to git.

## Qualify 50 before you finish the rest

Same idea as `/icp-prompt-builder`:

1. Grade 10 rows yourself: would you take this diagnostic?
2. Common NOs: agency, marketplace seller with no brand, crypto, “too big, they have a media team”.
3. Repeat until two batches of 10 need no changes.
4. Apply that bar to the remaining companies.

## Score before send

```text
/list-quality-scorecard
```

Fix anything the scorecard flags on duplicates, personal emails, and title junk. Do not upload a list with >2–3% likely bounces.

## Volume math

| Stage | Sends |
|---|---|
| Warmup days 1–14 | 0 campaign sends |
| Days 15–21 | ~10/inbox/day × 2 = 20/day ≈ 100 for the week |
| Days 22–28 | ~20/inbox/day ≈ 200 for the week |
| First live month | ~400–500 sends |

A 500-row list is plenty. Quality beats a 25k Prospeo dump you cannot afford and cannot send.
