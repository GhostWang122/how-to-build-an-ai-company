# 03 · Execution System — Cadence, Sheets, Priorities

The execution system answers one question: *how does intent at the top become verified results at the bottom, every day, without the founder reading eleven threads?*

## Daily cadence

| Beat | Artifact | Checked by |
|---|---|---|
| Morning | **Daily work plan** — numbered items, each with an owner and an expected output | CEO, every morning |
| Midday & evening | **Department progress reports** — two sections only: *Progress* / *Blockers* | GM |
| Evening | **Daily work summary** — the morning plan's items, each marked with its result | CEO, every night, against the plan |
| Continuous | **Approval feedback** — the chairman writes decisions inside the sheet (see below); the responsible GM answers every line before the day closes | CEO (closing scan) |

Two rules keep the cadence honest:
- A summary is **measured against the morning plan, item by item**. A summary that tells a new story instead of closing the plan's items is sent back.
- Department work runs **in parallel by default**; a department waiting on another says so in the Blockers section the same day, not at the deadline.

## The master-sheet protocol

All routine reporting and approvals live in one shared operating sheet per project. Chat is not a reporting medium. The protocol, at full granularity:

1. **Fresh-read before write.** Before writing anything, re-read the whole current sheet and locate the target row by its item number — *never* by a remembered row position. (The sheet is re-sorted by humans; a write from a stale layout lands in the wrong row. This has happened; the rule is the scar.)
2. **One dated approval column per day.** Each day, a new column is added at the far right, headed with that date. Yesterday's column is preserved exactly — header and content. Renaming an old column to fake today's is a recorded error.
3. **Decisions live in the sheet.** Anything needing the chairman's decision is written into its row, with the day's approval column in place. He approves (or questions, or rejects) **inside the column**, in his own words.
4. **Answers attach to the question.** The GM writes the handling result directly after the chairman's words, in the same column — a question gets a factual, evidence-backed answer, never a bare "received".
5. **Closing scan.** Before the day closes, every GM scans that day's approval column line by line and answers every line. An unanswered approval line at night is a defect in the *system*, not an oversight.
6. **Read-back after write.** Every write is verified by reading the sheet back. "I wrote it" is not evidence; the read-back is.
7. **Summaries carry the link.** Every summary delivered to the chairman ends with the sheet links. He must always be one click from approving — if he has to ask for the sheet, the summary failed.

## Priority labelling: the four quadrants

Every item in a plan or summary carries one label:

| Label | Definition in this company |
|---|---|
| **Important + Urgent** | Act today: revenue, orders, compliance, a decision, or someone else is blocked |
| **Not important + Urgent** | Due today, but it does not move the company — do it, don't dramatize it |
| **Important + Not urgent** | The compounding work — its time is protected precisely because nothing screams for it |
| **Not important + Not urgent** | Named as such, so it cannot borrow urgency from its neighbours |

- **Important** = directly tied to revenue, orders, policy compliance, a chairman decision, or an external commitment.
- **Urgent** = if nobody acts today, it slips, blocks someone, or expires.
- Presentation order in the CEO's summary: **decisions for the chairman first**, then items grouped by quadrant, each tagged with its project. Missing or obviously wrong labels are returned for correction — and the correction itself is noted, so labelling quality is visible.

## Blocker protocol

> "Don't sit on a blocker. If it's stuck and you don't surface it, I can't know."

- A blocker older than **one day** is escalated as its own item, in this exact shape: **where it is stuck · how long · waiting on whom**.
- A blocker is never buried inside a progress paragraph, and never softened into "in progress".
- Escalating early is rewarded; surfacing a blocker late is itself reported.

## Authority by error rate

Authorization is not a rank privilege; it is a meter:

- Sustained error-free runs **expand** a line's autonomy (more direct replies allowed, fewer pre-approvals). The intended end-state is a system that runs itself on routine work.
- Repeated errors **shrink** it automatically — e.g. in Customer Service, one wrong direct reply suspends the direct-reply authorization until it is re-earned.
- Nobody is punished for a *new* kind of error that becomes a written rule. Repeating a *ruled* error is what costs authority.
