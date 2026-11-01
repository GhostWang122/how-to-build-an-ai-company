# 06 · Templates — Reporting at Working Granularity

Copy-paste templates. The fields are the point: a report that skips a field is incomplete, however good its prose.

## Daily work plan (GM → CEO)

```text
# Daily Plan — <Project> — <YYYY-MM-DD>
Quadrant key: IU = Important+Urgent · NU = Not Important+Urgent
              IN = Important+Not Urgent · NN = Not Important+Not Urgent

| # | Item | Quadrant | Owner | Expected output today | Depends on |
|---|------|----------|-------|----------------------|------------|
| 12 | <one-line task> | IU | Tech | <artifact: link / screenshot / measurement> | — |
```

Rules: items keep their numbers across days until closed; "expected output" names an **artifact**, not an activity ("verify X and attach the 390px screenshot", not "work on X").

## Daily work summary (GM → CEO)

```text
# Daily Summary — <Project> — <YYYY-MM-DD>
## Closed today
- #12 [IU] <item> — Result: <one line>. Evidence: <link/measurement>.
## Still open
- #9 [IN] <item> — Age: 3d. Next step: <…> by <when>.
## Blockers (own section, always — even if empty: write "none")
- #15 — Stuck at: <where>. For: <how long>. Waiting on: <whom>.
## Tomorrow's first moves
- <…>
Sheet: <link>
```

## CEO summary (CEO → Chairman)

```text
## Decisions needed (always on top — or "none today")
1. <Decision> — Recommendation: <…>. If it waits: <consequence>.
## Important + Urgent
- [<Project>] <item> — <result / status>.
## Not Important + Urgent
- …
## Important + Not Urgent
- …
## Not Important + Not Urgent
- …
Sheets: <Astro link> · <Project-2 link>   ← links are mandatory, every time
```

## Escalation (anyone → Chairman)

```text
Needs your decision: <one line>
Facts (checked): <evidence, with sources>
Options: A … / B … — Recommendation: <A/B, and why>
If it waits: <what slips, what expires>
```

## Blocker report (standalone, never inside a progress update)

```text
BLOCKED — #<item> <name>
Stuck at: <the exact step / person / system>
Since: <date> (<n> days)
Waiting on: <whom — and what exactly they need to do>
Impact if it waits another day: <…>
What I have already tried: <…>
```

## Dispatch (GM → Department)

```text
#<item> — <task name>
Spec: <what to build/change, precisely>
Acceptance: <the exact checks the result will face — paste from 05-quality-gates.md where relevant>
Deadline: <date/time>
If blocked: report today, in the Blockers section — do not wait for the deadline.
Deliver: <artifact> + evidence, referencing #<item>.
```

## QA finding

```text
[Severity P0/P1/P2] <page/surface> — <defect in one line>
Evidence: <screenshot / measurement / raw HTML excerpt>
Expected (settled rule): <the rule or approved mock it violates>
Found: <date/time> · Status: OPEN → DISPATCHED (#<item>) → FIXED → RE-VERIFIED <date>
```
A finding is closed by QA's re-verification entry — never by the fixer.

## Approval-column answer (GM, in the master sheet)

```text
<Chairman's words, quoted>
→ Handled: <what was done, item #>. Evidence: <…>. Status: closed / waiting on <…> because <…>.
```
A question is answered with facts and evidence. "Received" / "Noted" alone is a failed answer.
