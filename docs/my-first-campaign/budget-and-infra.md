# $100/month stack — UK, no warmed inboxes

The full GrowthEngineX path in the README (~$360 month 1, 20 domains, 40 Zapmail inboxes) does not fit this budget. Use a **micro-stack**: two real inboxes, one sequencer, free lists.

## What the student ID is for (and what it is not)

**Use it for**

- GitHub Student Pack: Copilot, Codespaces, and a Namecheap `.me` or Name.com `.live` / `.studio` domain as a **booking/landing page**, not as the From domain.
- Student Notion / Canva / similar, to write up the three diagnostic notes.
- Azure credits if you later host a tiny booking page.

**Do not use it for sending**

- Do not send commercial outreach from a university `@*.ac.uk` address. It looks unprofessional and usually breaks the university acceptable-use policy.
- Do not put cold outreach on Microsoft 365 Education or Google Workspace for Education. Those licences are for study. Commercial bulk sending gets the tenant shut down, and deliverability on education domains is poor anyway.
- Do not use a free `.me` / `.live` / `.dev` student domain as the sending domain. Recipients and filters treat those as throwaway.

Buy a normal commercial mailbox product. That is the $18–25/month that actually protects the campaign.

## Monthly budget (stay at or under $100)

| Item | What it does | Target cost |
|---|---|---|
| 1 sending domain (`.co.uk` or `.com`) | Separate from datawithejaz.com | ~$12–20 **once** (month 1) |
| 2 × Google Workspace Business Starter **or** Microsoft 365 Business Basic | Real inboxes on that domain | ~$20–25/mo incl. VAT |
| Smartlead Base | Warmup + sequences + unibox | $39/mo (or ~$32.50 billed yearly) |
| Email verification (MillionVerifier or similar pay-as-you-go) | Stop bounces burning the new domain | ~$5–8 for the first 500–1,000 |
| List building | Meta Ad Library + Companies House + website/LinkedIn | **$0** |
| **Month 1 total** | Domain + mailboxes + Smartlead + verify | **~$80–95** |
| **Month 2+** | Mailboxes + Smartlead + a little verification | **~$65–75** |

That leaves a small buffer. Do not add Zapmail, Prospeo, Blitz, RapidAPI, or Instantly until a campaign has booked at least a couple of diagnostics.

If Smartlead’s trial is still 14 days with no card, use the trial for warmup weeks 1–2, then pay Base only when you are ready to send.

## Why two inboxes, not twenty

At this volume you will send about **20 emails per inbox per day** after warmup. Two inboxes × 20 × ~12 sending days in the first live month ≈ **480 emails**. That is enough if the list is “UK Ltd already running Meta ads,” and it is the volume a new domain can survive.

## Domain and DNS (do this once)

1. Buy a domain that looks like a person, not a tool. Examples of the *shape* (pick one you can actually register): `helloejaz.co.uk`, `ejazahmed.co.uk`, `with-ejaz.co.uk`. **Never send from `datawithejaz.com`.** A burned primary domain costs you the website, not just a mailbox.
2. Create two Google Workspace or Microsoft 365 users, e.g. `ejaz@` and a second first-name style inbox. Real names, not `info@` or `outreach@`.
3. Set SPF, DKIM, DMARC before connecting Smartlead. Use `/email-deliverability-audit` → `check-domain-auth.ts` once DNS has propagated.
4. Put a one-line physical UK address and a privacy-policy link in the Smartlead signature. `/smartlead-inbox-manager` can set signatures in bulk.

## Warmup (you cannot skip this)

You have no warm inboxes. Plan on **14 days of warmup with zero campaign sends**.

Connect both inboxes to Smartlead, turn warmup on, and leave it. Typical new-domain ramp:

| Days | Campaign sends per inbox per day |
|---|---|
| 1–14 | 0 (warmup only) |
| 15–21 | 10 |
| 22–28 | 15–20 |
| 29+ | cap at 20–25 |

If you send 50/day from a two-day-old domain, the domain dies and the $12 you saved on patience is gone.

## What this repo can do at this budget

**Use (free, no extra APIs)**

- `/cold-email-kickoff` artefacts already drafted in this folder
- `/campaign-copywriting` + `/spam-word-checker` when you iterate copy
- `/list-quality-scorecard` on your CSV before upload
- `/smartlead-inbox-manager` once keys exist
- `/email-deliverability-audit` after DNS
- `/cold-email-weekly-rhythm` on a calendar
- `/positive-reply-scoring` after week 3 of sending
- `/experiment-design` before campaign 2

**Skip until you have revenue from this**

- `/zapmail-domain-setup-public` (Dynadot + Zapmail ~$60/mo inboxes alone)
- `/prospeo-full-export`, `/disco-like`, `/blitz-list-builder`, `/google-maps-list-builder`, `/competitor-engagers`
- `/auto-research-public` (needs Prospeo + MillionVerifier + 20 warmed inboxes)

When you *do* have Smartlead connected, `/smartlead-campaign-upload-public` can take `campaigns/active-advertisers/variants.yaml` from this folder. Upload stays DRAFT. You hit Start in the UI.

## Parallel channel that costs $0

While inboxes warm, run the same ICP on LinkedIn from your personal profile. Connection note, then the same three-notes offer. That is not in this skills pack, but at $100/month it will likely book as many diagnostics as email in month 1.
