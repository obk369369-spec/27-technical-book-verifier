# TOOL027 Canonical Master

## Identity
- TOOL: TOOL027
- Name: 기술도서 CSV 검증 도구
- Canonical runtime: `index.html`
- Public runtime: https://obk369369-spec.github.io/27-technical-book-verifier/
- Status: COMPLETE / REMOTE_VERIFIED
- Completed at: 2026-08-30 KST

## Verified operating scope
- CSV upload and header mapping
- Publisher inference from the input filename
- Internal category/keyword classification
- X/WARN/duplicate gates
- Automatic persistence and state restore
- Table/card observer views and copy outputs

This completion verifies the operational CSV pipeline. It does not claim external bibliographic truth verification for synthetic input.

## FIRST_VALIDATION
- Scope: the previously unverified public runtime connection and the changed persistence connection only
- Input: one synthetic, non-personal CSV row
- Upload result: DB 1 / X 0 / WARN 0 / DUP 0
- Persistence result: automatic write success
- Restore read-back: RESTORED / PERSIST:ok / DB 1
- Pages deployment run: https://github.com/obk369369-spec/27-technical-book-verifier/actions/runs/33314021811
- Pages run status: SUCCESS
- Runtime fix commit: 9e311dc
- Validation attempts on changed scope: 1

## Asset classification
- CANONICAL_NORMAL: `index.html`
- HOLD_UNKNOWN: `index (가장 기본 버전).html`, `index(그나마 검색 가능 버전).html`, `index_4단계 버전.html`
- SHELL_OR_STALE: none promoted by this work
- Deletion: not authorized; no file was deleted

## Reuse
- EXISTING_COMMON_REUSE: branch-based GitHub Pages deployment
- New reusable component created by this work: none
- Known waiting TOOL unlocked: none

## Reopen gate
TOOL027_REOPEN = REAL_USE_NEW_FAILURE_ONLY
RETEST_UNCHANGED_SCOPE = FORBIDDEN
