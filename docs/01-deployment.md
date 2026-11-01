# 01 · Deployment — How This Architecture Was Built

The architecture was not designed on a whiteboard and installed in a day. It was deployed in layers, each layer added when the previous one showed a specific failure mode. This document records the sequence, because the sequence is the lesson: **deploy management capacity exactly one step ahead of execution volume.**

## Deployment principles

1. **Values before volume.** The seven values were written and settled before execution scaled. Later, they became the *authorization floor*: any daily action that sits inside the values and settled policies can run without asking. Without a written floor, every decision climbs to the founder and the system chokes.
2. **One reporting line per node.** Every department and agent reports to exactly one manager. The moment a node has two bosses, it has none.
3. **Layers compress upward, expand downward.** A department's raw output (screenshots, logs, drafts) is compressed by the GM into verified items; the CEO compresses further into decisions and results. Downward, a one-line intent from the chairman expands into numbered, owned, deadline-bound items.
4. **Independence where verification matters.** Whoever checks the work must not report to whoever produced it. (QA reports to the CEO, not to the GM whose departments it inspects.)
5. **Every rule is written the day it is learned.** The handbook is not documentation *about* the system; it *is* the system. An unwritten rule does not exist.

## The steps

### Step 0 — Founder-direct (the failure mode that started it all)
The founder initially directed every working session himself. It worked at three sessions and collapsed at ten: context fragmented, the same question was answered differently in different threads, and nobody could say what the whole company was doing today. *Lesson: the founder's attention is the scarcest resource in the system; architecture is how you stop spending it on routing.*

### Step 1 — Appoint a General Manager
One session was appointed GM with a specific charter:
- coordinate all departments, chase delivery, perform first-line acceptance;
- when the founder urges speed, the GM's job is to **compress deadlines and supervise harder — never to do the department's work personally** (a GM who executes becomes a bottleneck with a title);
- the GM is accountable for the project's targets, not for any single deliverable.

### Step 2 — Charter the departments
Six departments were created, each with a written mandate in three parts:
- **Owns** — the decisions and surfaces that are theirs;
- **Does not own** — the adjacent territory that must be handed off (e.g. SEO places settled policy text on pages but may not rewrite the policy; Technology ships code but makes no content decisions);
- **Standing rules** — the department's own hard rules (e.g. Social publishes nothing without an approved set: design + copy + time approved together).

A mandate that only lists responsibilities, without the "does not own" column, failed in practice: departments absorbed neighbouring work and blurred accountability within a week.

### Step 3 — Add second seats (execution capacity without a shadow chain)
Busy lines received a second seat with a counter-intuitive reporting line: **the second seat reports to the GM, not to the department manager.**
- The manager keeps judgment work (standards, wording, acceptance criteria).
- The second seat keeps throughput work (watching an inbox, forwarding, first-pass execution inside a tight authorization).
- Because both report to the GM, a conflict between them is resolved by the GM — the manager cannot quietly task the second seat off-charter.

### Step 4 — Insert the CEO layer
A second project started, with its own GM. Two GMs reporting directly to the founder recreated the Step-0 problem one level up. A CEO layer was inserted:
- GMs report only to the CEO;
- the CEO filters: routine results are summarized, only **decisions, blockers and the founder's own assignments** reach him, as standalone items, never buried in a long report;
- feedback the founder gives in any channel is routed by the CEO to the owning GM — it does not stay in the channel where it happened to be said.

### Step 5 — Independent QA with a fast lane
A site QA inspector was created, reporting to the CEO, running a daily inspection across a fixed checklist (transaction flow, key pages, mobile rendering, price/policy consistency, dead links, new features in place, content freshness). Two mechanics matter:
- findings go **to the CEO**, who grades them; the GM dispatches fixes; QA **re-verifies** to close — the fixer never closes their own finding;
- a P0 defect uses the fast lane: straight to the CEO immediately, in parallel to the GM, not queued behind the daily report.

### Step 6 — Special lines, explicitly attached
Work that fits no department (a new product line, a sourcing hunt, a domain where the founder wants to decide personally) is opened as a *special line*: named, owned by a GM, with its decision rights written down (e.g. "the chairman decides on this line directly; progress still flows through the GM"). A special line that is not attached to a GM drifts within days.

### Step 7 — Naming, tagging, and channel discipline
- Every staff session is renamed with a company prefix (`Astro · …`). In a multi-company setup, an agent belongs to exactly one company tag; people are never borrowed across companies by chat message — cross-company coordination happens GM→CEO→GM.
- Channels are given jobs: a hotline channel carries only decisions/blockers/founder reminders; routine reporting lives in the shared operating sheets; chat fragments are not a reporting medium.

## What each layer costs — and why it is worth it

| Layer | Cost | What it buys |
|---|---|---|
| GM | One extra hop for every instruction | The founder stops routing; departments get chased daily |
| CEO | Summaries can lose detail | The founder reads one page, not eleven threads; detail is one click away in the sheet |
| QA independence | Duplicate verification effort | Findings actually close; self-graded homework disappears |
| Written mandates | Up-front writing time | Boundary disputes end in one look-up instead of one argument |
