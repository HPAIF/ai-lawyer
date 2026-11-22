# Jurisdiction pack — Republic of Armenia (RA)

Load this before any legal work for an Armenian company. Also covers EAEU law where it applies,
and foreign law (e.g. EU GDPR) only when the company deals with that market.

## Language
- Answer in the founder's chosen language (default English). Give the **Armenian name** of an
  act or body in brackets the first time, e.g. Tax Code (Հարկային օրենսգիրք).
- The **Armenian text is the only authoritative one.** English/Russian versions on ARLIS are
  translations and are often older.

## How to verify a provision in Armenia (used by `verify-law`)
1. **ARLIS** (https://www.arlis.am) is the consolidated-law source. Search by Armenian title
   first; act pages are `arlis.am/hy/acts/<id>` (Armenian) and `arlis.am/en/acts/<id>`. Store the
   id as `official_id` and the Armenian URL as `url_official` in law cards.
2. On the act page read the status block: in force / lost force / partly in force; the edition
   date; the list of amending acts; transitional provisions ("see Article N").
3. Open the Armenian edition. If you quote the English/Russian one, compare edition dates and say
   if the translation is older.
4. Coming changes: **parliament.am** (bills, readings, adopted laws not yet published) and
   **e-draft.am** (government drafts in public discussion, at least 15 days, with comment
   deadlines). Search both by the act's Armenian title.
5. Practice: **datalex.am** (use the non-`www` host) for court acts — Court of Cassation
   positions on interpreting a norm guide lower courts in similar facts; **concourt.am** for
   Constitutional Court decisions declaring provisions (un)constitutional.
6. Regulator positions: src.am (tax, cash registers, e-invoicing), pdpa.am (personal data),
   cba.am (payments), competition.am, hightech.gov.am — Tier 2, show how the law is applied.

## Local mandatory checks for contracts (used by `contract-review`)
- Civil Code (Քաղաքացիական օրենսգիրք): form requirements, penalties, liability limits,
  unilateral termination, limitation periods.
- Language requirements for contracts with Armenian parties (verify current rule).
- Law on Protection of Personal Data — processing, consent, transfers abroad, notifications.
- Cash register (ՀԴՄ / e-HDM) duties if the product issues receipts.
- Law on Cybersecurity duties if the customer is in a vital sector / critical information
  infrastructure operator.
- Tax: VAT, withholding for foreign counterparties (→ accountant).
- Disputes: Armenian courts by default; arbitration only if agreed.

## Monitoring guide (used by `legal-watch`)
- parliament.am — bills on watchlist topics (tax, IT/high-tech, cash registers, personal data,
  cybersecurity, electronic documents, labour, competition, the company's sector).
- e-draft.am — drafts in discussion on those topics (note the comment deadline).
- arlis.am — new acts; new editions of acts with law cards.
- Regulators: src.am, pdpa.am, hightech.gov.am, e-gov.am / gov.am (government decisions),
  cba.am (only if a payments module), competition.am (if pricing features or concentrated market).
- Search keywords (leads only): "Armenia law IT companies", "Armenia personal data law draft",
  ՀԴՄ փոփոխություն · Հարկային օրենսգիրք փոփոխություն · անձնական տվյալներ օրենք նախագիծ ·
  ՏՏ ոլորտ օրենք.

## Known access issues (update via learnings → `improve`)
- moj.am blocks automated requests (403, 2026-11) — use a browser or gov.am news.
- mineconomy.am did not answer automated requests (2026-11) — retry.

## Files in this pack
- `sources.md` — official source registry with tiers.
- `watchlist.md` — baseline topics for an Armenian IT / SaaS company; copied into
  `ai-team/lawyer/watchlist.md` by `setup`, then it evolves per company.
- `permissions.json` — WebFetch allow-list for these sources; `setup` offers to merge it into the
  project's `.claude/settings.json`.
