# 04 · Task Lifecycle — One Item's Full Journey

This is the granularity at which a single task is run. The example is generic; the steps are not.

## The eight steps

### 1. Intent
A task is born in one of three ways: the chairman decides it; it falls inside the values floor and the CEO opens it; or a department proposes it and the GM accepts it into the plan. However it is born, it gets **a number, an owner, and a written expected output** before any work starts. An unnumbered task does not exist.

### 2. Framing (CEO, when cross-department)
The CEO states: scope, what evidence the result must carry, which GM owns it, and which settled rules apply. Framing is written, not implied — most execution failures in this system traced back to framing that lived in someone's head.

### 3. Dispatch (GM)
The GM writes the item into the master sheet and tasks the department with:
- the item number (used in every later reference — "see #24" beats a paragraph of context);
- the spec, including the acceptance criteria the result will be checked against;
- the deadline, and what to do if blocked (report same day, in the Blockers section).

### 4. Execution (Department)
The department works inside its mandate. Execution rules:
- conclusions carry their evidence (a measurement, a screenshot, a source) — "I checked" without the artifact is not a result;
- a boundary hit (the task needs another department's territory) is handed back to the GM for re-dispatch, never absorbed silently;
- mid-task discoveries that change the spec are reported up before they are acted on.

### 5. First-line acceptance (GM)
The GM checks the delivered result **against the dispatch spec, item by item** — not against a general impression. Three outcomes only: accepted, accepted with noted defects (which become new numbered items), or returned with the specific failing checks named.

### 6. Independent re-verification (QA, for site-facing work)
For anything a visitor can see or a customer can touch, QA re-verifies on the live surface with its own checklist (see `05-quality-gates.md`). The department's own verification does not count toward this step. A finding re-opens the item at step 4, with the finding attached.

### 7. Summary (CEO)
The closed item enters the CEO's summary with: its four-quadrant label, the one-line result, and the sheet link. Open items enter with their age and their blocker line, if any. Nothing is summarized from memory — the sheet is read first.

### 8. Chairman feedback loop
The chairman's approvals, questions and corrections are written in the sheet's dated column. Each becomes either a closure or a new numbered item at step 3. **The loop is only closed when his words have a written answer under them** — see the closing scan in `03-execution-system.md`.

## Handoff rules (the seams, where systems actually fail)

| Seam | Rule |
|---|---|
| Chairman → CEO | Given in any channel; the CEO routes it to the owning GM and files it — feedback never stays only in the channel where it was spoken |
| CEO → GM | Written framing; the GM repeats back scope + deadline in the plan before executing (a silent nod is not a confirmation) |
| GM → Department | Numbered dispatch with acceptance criteria attached |
| Department → GM | Result + evidence artifact, referencing the item number |
| GM → QA | "Ready for re-verification" is an explicit signal, with the live URL — QA never guesses what changed |
| Anyone → Anyone | If the content changes after an approval, the new version is shown again before it ships. Approval covers exactly what was shown |

## Anti-patterns this lifecycle exists to kill

- **"Done" declared by the doer** — acceptance is granted by the next layer up, re-verified independently for live surfaces.
- **Progress theatre** — activity reported instead of the plan's items closed.
- **The buried blocker** — bad news travelling slower than good news.
- **The stale-layout write** — acting on a remembered state of a shared artifact instead of a fresh read.
- **The silent scope change** — the delivered thing quietly differing from the approved thing.
