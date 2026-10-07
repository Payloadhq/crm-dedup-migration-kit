# CRM Dedup & Migration Cleanup Kit

*Offline duplicate detection and dry-run merge planning for CRM CSV exports. A commercial product by Payload.*

> **This repo contains documentation and sample data.** The full kit ($149, one-time) ships when you buy; it is not open source. Buy links are below.

Your CRM is full of duplicates. Same contact three times with different emails. Companies split across two records. You're migrating to a new system and the thought of importing that mess keeps you up at night.

Manual cleanup doesn't scale. Most dedup tools either want your API keys, want your data in their cloud, or make you pay per record.

## Who it's for

Operations people, founders, and admins cleaning a messy CRM before (or during) a migration — anyone with a contact or company CSV export who wants duplicates found and a safe, reviewable merge plan.

## What it does

The kit reads a contact or company CSV exported from your CRM (HubSpot and Salesforce formats detected automatically), finds duplicate records with normalized + fuzzy matching, and produces a reviewable dry-run merge plan plus import-ready CSVs.

**What it never does:** it never connects to the internet, never asks for API keys, and never touches your live CRM. It only reads the file you give it and writes new files. Your original export is never modified.

### Workflow

1. **Import** — run your CRM export CSV, or try a sample file instantly. Format is auto-detected from headers.
2. **Review** — duplicate clusters listed with confidence tiers:
   - `AUTO` — exact email, phone, or domain match. Pre-selected for merging.
   - `REVIEW` — close fuzzy match (score 80–94). Merge only if you approve.
3. **Dry-run plan** — preview exactly what would merge: the surviving record, absorbed records, and every field decision with its source. Nothing is written yet.
4. **Export** — download the merge plan, import-ready CSVs, and a change log.

## Sample data

This repo's `samples/` folder contains anonymized sample CSVs in HubSpot and Salesforce formats so you can see the expected input structure:

- `hubspot_contacts_sample.csv`
- `hubspot_companies_sample.csv`
- `salesforce_contacts_sample.csv`

## What you receive

The full kit ($149, one-time) includes:

- Ready-to-run app (no Python needed) + Python source
- Local web UI for review and merge planning
- 54 automated tests
- Import-ready CSV export + change log

## What it does NOT include

- It does not connect to your CRM, use API keys, or modify your live data. Everything happens on files you supply.
- It does not auto-merge without your review. `AUTO` matches are pre-selected; `REVIEW` matches merge only with your approval; nothing is written until you export.
- It does not perform the migration into your new system. It produces import-ready CSVs and a change log; you import them.

## Buy

**$149 one-time. Yours forever. No subscriptions, no per-record fees.**

**Buy:** [Gumroad](https://payloadtools.gumroad.com/l/crm-dedup-migration-kit) · [Whop](https://whop.com/payload-f126/products/crm-dedup-migration-cleanup-kit/)

7-day refund if the product is materially not as described or cannot be made functional after reasonable support.

## Support and updates

- Support: kylers.partners@gmail.com
- Telegram: https://t.me/payloadtool
- Patreon: https://patreon.com/PayloadTools

Sold and supported by Payload. Small software that earns its keep.

---

**Payload** — Developer infrastructure for x402, agent payments, and programmable revenue..
Developer portal: https://payloadhq.github.io/ ·
All products: https://payloadtools.gumroad.com/ ·
Contact: kylers.partners@gmail.com
