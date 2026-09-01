# Coding, automation and agent completion review

The completion statement is a claim. Verify the artifact, not the statement.

## Evidence hierarchy

Prefer evidence in this order when applicable:

1. Actual file or deployed artifact exists at the expected path or URL.
2. Diff or exact file content matches the brief and avoids unrelated changes.
3. Relevant tests, build, lint, or validation were actually executed and their raw results are available.
4. The application or automation was run with representative inputs.
5. Browser, output file, screenshot, console, network, and logs show the real end state.
6. Acceptance criteria can be mapped one by one to the evidence above.

Plans, pseudocode, generated screenshots without provenance, and phrases such as “implemented”, “should work”, or “ready” are not completion evidence.

## Audit procedure

- Recover each acceptance criterion from the brief.
- Identify the exact artifact path, output file, page, commit, diff, job, or runtime state expected for it.
- Inspect whether the target exists and was actually changed.
- Check the diff for wrong-file edits, unrelated changes, hard-coded values, leaked configuration, or changed behavior outside scope.
- Confirm the exact test/build/runtime command was run, not merely suggested. Preserve failures and warnings.
- Open or exercise the output using realistic inputs when authorized and safe.
- Inspect browser console, network errors, logs, file-open/import results, and downstream compatibility when relevant.
- Test decision-relevant edge cases: empty, duplicate, extreme, malformed, permission denied, network failure, rerun/idempotency, and partial failure.
- Record anything not actually executed as `UNABLE TO VERIFY`.

For agent-completion reviews, use this mapping:

| Acceptance criterion | Expected artifact/evidence | Observed evidence | Status | Gap / next verification |
| --- | --- | --- | --- | --- |

Then state one verdict:

- `完成且已有证据`
- `部分完成`
- `尚未证明完成`

Do not change files while performing the initial completion audit. Do not run destructive, production, deployment, paid, or externally mutating operations merely to obtain evidence unless the user has authorized them.

## Human judgment boundary

People decide deployment timing, rollback readiness, permission scope, user impact, and residual risk. For important automation, recommend a separate person execute the real workflow once.
