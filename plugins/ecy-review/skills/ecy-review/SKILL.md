---
name: ecy-review
description: "Audit completed AI-generated work for ECY before it is used, sent, published, or treated as complete. Use explicitly for review of research, listings, product specs and manuals, business communication, marketing copy, localization, spreadsheets, presentations, images, agent or coding deliverables, and commercial analysis. This is a review-first workflow, not a general writing or rewriting skill."
---

# ECY Review

Audit the real artifact against the original task and available evidence. Make the workflow feel simple to the user: infer the review route and depth instead of presenting a checklist menu.

## Non-negotiable rules

- Review first. Do not rewrite, polish, regenerate, or silently fix the artifact during the audit.
- If the user asks to review and revise in one request, complete the review and stop after the issue list. Revise only after the user explicitly confirms the next step.
- Never claim verification from plausibility, internal consistency, or the author's summary. Verification requires independent evidence.
- Use `UNABLE TO VERIFY` when the needed source, calculation, file, runtime result, or visual evidence is unavailable.
- Point to the exact location of every issue: sentence, table row, cell, slide, page, image region, file, or runtime step.
- Prefer deterministic checks when possible: recalculation, source comparison, file existence, diff, test, build, runtime, render, logs, or exported-file inspection.
- Review the actual artifact. For agent work, do not treat the agent's completion summary as evidence.
- Do not make final commercial commitments, brand decisions, risk acceptance, or external approvals for the user.

## Start without a menu

1. Identify the artifact type from the content, attachment, file extension, and current conversation.
2. Recover the original brief and acceptance criteria from the conversation. Do not ask the user to paste information that is already visible.
3. Choose the review depth automatically:
   - `Quick` when the user asks for a fast check or the artifact is low-risk and internal.
   - `Standard` by default.
   - `Deep` for external publication, product facts, price or terms, financial/data conclusions, instructions that affect real product use, important research, or completion claims by code/automation/agents.
4. Read exactly the relevant reference file listed below. Do not load unrelated domain references.
5. Run the audit and return only actionable problems and material unknowns by default.

Do not ask the user to choose an artifact category, checklist, or depth unless their explicit choice is necessary. If the artifact itself is missing, ask for it. If the brief is missing, infer the likely criteria and label them as assumptions. Ask one concise question only when a high-risk decision cannot be reviewed meaningfully without the missing criterion. Missing sources do not block the first review; mark dependent checks `UNABLE TO VERIFY`.

## Route to one reference

- Research, market or competitor analysis; ecommerce, Amazon or listing content; product specifications, manuals, FAQs: read [references/research-commerce-product.md](references/research-commerce-product.md).
- External email, proposals and business communication; marketing, social or brand copy; translation and localization: read [references/communication-marketing-localization.md](references/communication-marketing-localization.md).
- Spreadsheets, CSV, Excel or quantitative summaries; presentations, documents and reports; images and visual designs: read [references/data-presentation-visual.md](references/data-presentation-visual.md).
- Coding, automation or agent completion claims: read [references/agent-completion.md](references/agent-completion.md).
- Sales, channel, forecast, pricing, unit economics or commercial recommendations: read [references/commercial-analysis.md](references/commercial-analysis.md).
- Anything else: read [references/universal-review.md](references/universal-review.md).

For a mixed artifact, select the reference for the decision-critical risk. Read a second reference only if the artifact contains another independently material domain, such as a commercial recommendation built from a spreadsheet.

## Status and severity

Use these statuses:

- `FAIL`: a concrete problem is present.
- `UNABLE TO VERIFY`: the answer depends on evidence that was not independently checked.
- `PASS`: checked with sufficient evidence and no problem found.
- `NOT APPLICABLE`: the check does not apply.

Default output includes only `FAIL` and decision-relevant `UNABLE TO VERIFY`. Provide the full PASS record only when the user requests it.

Use these severities:

- `High`: may cause an incorrect decision, external commitment, product or financial error, unusable deliverable, or false completion claim.
- `Medium`: may mislead, omit a material condition, or substantially reduce delivery quality.
- `Low`: minor wording, presentation, or consistency issue that does not change the underlying decision.

## Output contract

Match the user's language. Keep the result compact and prioritize High, then Medium.

```markdown
审查结论：暂不建议交付 / 可交付但有待确认项 / 未发现阻断问题

| Severity | Status | Exact location | Issue | Evidence / reason | Next verification |
| --- | --- | --- | --- | --- | --- |

最值得人工确认：
1. ...

本次审查边界：
- 未检查或无法看到的内容
```

Apply these verdicts conservatively:

- `暂不建议交付`: at least one unresolved High `FAIL`.
- `可交付但有待确认项`: no High `FAIL`, but a decision-relevant unknown or Medium issue remains.
- `未发现阻断问题`: no blocking issue found in the inspected scope. This is not a claim that the artifact is universally correct.

If no problem is found, say what was actually inspected and what was not. Do not manufacture issues to appear thorough.

## Next-turn behavior

After the review, the user can ask to:

- verify selected issues using new evidence;
- revise only confirmed issues;
- run a focused final check after revision.

During revision, preserve correct content, do not introduce new claims, and recheck affected numbers, terms, links, charts, cross-references, and final file usability.
