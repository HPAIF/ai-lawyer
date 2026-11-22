---
name: verify-law
description: Check that a legal act, article, rate, threshold or deadline is current before relying on it — status, edition, pending amendments, drafts and court practice — on the jurisdiction's official sources. Use every time any legal provision is used in advice, a memo, a contract review or a digest, even if a law card says it was verified before.
---

# verify-law

Goal: prove the provision you are about to rely on is the law **today** (or on the date that
matters), and know what is about to change. Run it per act, in the same conversation where you
give the advice. Jurisdiction specifics (which site, how editions and translations work) are in
`${CLAUDE_PLUGIN_ROOT}/jurisdictions/<name>/README.md` — follow them.

## Steps

1. **Locate the act on the Tier 1 consolidated-law source** of the jurisdiction (`sources.md`).
   Use the law card's `url_official`/`official_id` if a card exists in `ai-team/lawyer/laws/`;
   otherwise search by the official-language title (fall back to English). Fetch the page.
   Never use a remembered text.
2. **Read the status**: in force / lost force / partly in force; the date of the edition you are
   reading; the list of amending acts; transitional provisions.
3. **Use the official-language edition.** If you quote a translation, compare edition dates; if
   the translation is older, say so and paraphrase from the official text.
4. **Confirm the exact provision** (article / part / point) still says what you need. Quote or
   paraphrase it with the article number.
5. **Look for changes coming**:
   - amendments adopted but with a later entry-into-force date;
   - bills in parliament for this act;
   - government drafts in public consultation that amend it;
   - if interpretation matters: supreme/cassation court practice and constitutional court
     decisions on the provision.
6. **Record the result**:
   - Card exists → update front-matter `last_verified`, `latest_amendment_seen`,
     `pending_changes`, `status`, and append a row to its "Verification log".
   - No card and the act matters long-term → run `ai-lawyer:add-law`.
7. **Report** in the answer's Verification section: source URL, status seen, edition/amendment
   date, pending changes found (or "none found on <sources checked>"), date checked.

## If you cannot verify
- Site down / blocked / act not found → mark the claim **UNVERIFIED** in bold, say exactly what
  the founder (or a lawyer) should check and where, and lower your confidence to low. If a
  source keeps failing or moved, record a `source` learning.
- Sources conflict (official text vs regulator guidance vs secondary sources) → state the
  conflict; the official text wins on what the law says, regulator guidance shows how it is applied.

## Don'ts
- Don't treat a law-firm article, news item or AI summary as verification.
- Don't skip this because the card was verified recently. The rule is: every use.
