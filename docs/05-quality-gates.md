# 05 · Quality Gates — The Granularity Standard, as Checklists

Every gate below was created by a real failure in this company, and is written at the granularity the failure taught us. A gate is a checklist with a pass condition — not an aspiration. Work that has not passed its gate is not "done", whoever measured it.

## Gate 1 — Canonical URL only
- [ ] Acceptance measured on the canonical URL, **no query parameters**
- [ ] Measured **more than once**, at an interval (cache copies converge at different speeds per page)
- [ ] Measurements cross-checked against an independent QA measurement of the same points
- [ ] If copies have not converged: report *"installed + converging + which pages are already new"* — never "fully live"
- [ ] A stuck single-page cache is purged with the targeted per-page purge, not a global purge

## Gate 2 — Intent placement, not just coordinates
Coordinates prove a thing is where *you* put it. They do not prove it is where it was *approved* to be.
- [ ] Coordinate check against the specification
- [ ] **Semantic placement check against the approved mock** ("in the white band below the header" ≠ "floating over the hero card" — both can share a y-coordinate)
- [ ] Structure check: the surrounding card/body structure is itself intact (a decoration that breaks the card it decorates is a fail)
- [ ] For homepage-class changes: the chairman sees the fixed preview and approves **before** the switch — no schedule pressure overrides this

## Gate 3 — Mobile-first
- [ ] ~390px viewport rendering checked and evidenced (screenshot or measurement)
- [ ] Desktop checked second, not first
- [ ] No mobile evidence → no acceptance, full stop

## Gate 4 — Anonymous visitor state
- [ ] Raw anonymous HTML inspected for visitor-facing changes
- [ ] Logged-in view checked *in addition*, never *instead* (logged-in views have hidden broken visitor states in this system before)

## Gate 5 — Plugin / code release (three machine checks + live verify)
Before install:
- [ ] **Diff** — line-by-line diff against the last known-good version; every change describable in one sentence
- [ ] **Quote audit** — machine check that quotes balance on every line
- [ ] **Byte checks** — no stray escape bytes, no redaction markers, balanced brackets (judged by byte count in code, never by eyeballing a terminal — escaped display lies)
- [ ] Syntax check for extracted inline scripts (e.g. `node --check`)
- [ ] Long code ships as an installable package (plugin zip), not pasted into a snippet tool
- [ ] The last known-good version is kept, ready to restore

After install:
- [ ] Homepage, admin, and checkout verified **within minutes**
- [ ] Any anomaly → immediate rollback by deactivating the package at the hosting level, then diagnose — never debug a fatal on the live site

## Gate 6 — Publishing (content)
A content piece may publish without per-piece founder review **only when every box is ticked**; one empty box returns it to the review gate:
- [ ] Approved presentation assets (sales cards) in place, chosen by page intent
- [ ] SEO plugin score in the green band
- [ ] Structured data in the editor-safe wrapped format — *and* the editor panel itself opened on at least one piece per batch to prove it renders (public output can be perfect while the editor crashes)
- [ ] Cover present, placed in the same session (a missing cover is produced on the spot, never left as a bare title card on listing pages)
- [ ] Listing / archive presentation checked — not only the article page
- [ ] Mobile rendering evidence attached

## Gate 7 — Numbers and claims
- [ ] Every figure in a department report carries its source; unsourced figures are returned, not debated
- [ ] A conclusion in a strategy paper names the evidence it rests on, or is labelled *to be verified*
- [ ] Speed/performance acceptance is measured on the full loading waterfall over a realistic route — never on server response time alone
- [ ] A file edited by one tool is verified by a second, independent renderer/tool before delivery

## Gate 8 — Customer-facing authorization (tiered)
Customer Service works in tiers, because "be helpful" is not an authorization:
- [ ] **Tier A (direct reply):** a short whitelist of factual policy questions, answered with the *exact settled wording* — no rewriting, no combining, nothing outside the list; every direct reply reported the same day
- [ ] **Tier B (draft only):** everything else is drafted and approved before sending
- [ ] **Always approve-first, no exceptions:** refunds, complaints, damage, individual orders, discount asks, individual service cases
- [ ] Unknown stock/product facts are never answered with a flat "no": the settled pattern is *confirm first, then follow up through the customer's chosen channel* — except facts read live from the store system, which are stated as-is
- [ ] One wrong Tier-A reply suspends Tier A automatically (see error-rate authority, `03-execution-system.md`)
