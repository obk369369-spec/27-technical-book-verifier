# TOOL027 Canonical Master

## Identity
- TOOL: TOOL027
- Name: 기술도서 CSV 검증 도구
- Historical conversation names: `27번 공학 도서 안내`, `27번 공학도서 안내 도구`, `공학도서 안내서 자동 생성 도구`
- Canonical runtime: `index.html`
- Public runtime: https://obk369369-spec.github.io/27-technical-book-verifier/
- Status: COMPLETE / REMOTE_VERIFIED
- Completed at: 2026-08-30 KST
- Global operating rules: `obk369369-spec/20-operational-manual-viewer/WIC_GLOBAL_OPERATING_RULES.md`

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

## Historical catch-up — recovered user rules
The 278-file historical catch-up recovered the following durable TOOL027 rules. These do not override newer verified runtime behavior; they constrain future TOOL027 changes and real-use output.

### Input/source integrity
- Source metadata may arrive as Excel, CSV, PDF, text, email body, publisher metadata, or pasted lists.
- Original source files are evidence and must not be silently altered or replaced.
- Source-grounded fields must not be invented. Missing Pages/ISBN/date/link or other unsupported values remain blank rather than being filled with placeholder or guessed data.
- Publisher identification may be inferred from the source filename only when that mapping is explicitly supported by the actual input/source convention.

### Deduplication and ordering
- Duplicate priority: ISBN equality first; English title + publication year second when ISBN is unavailable.
- Historical customer-guide flow used newest publication date first, then higher list price for equal dates. Apply only when the active task is that customer-guide output and the source supports the required values.

### Category handling
- Historical rule forbids semantic guessing for classification when running the strict customer-guide flow.
- Classification must use observable title/subject/keyword values and the active keyword table/rules; unsupported expansion/recommendation is not accepted as source-derived classification.

### Customer-guide output integrity
- Historical fixed guide block: English title + Korean title, publisher / pages / ISBN / list price, publication date / supply price, and verified detail link.
- Edition markers such as `1ed`, `2nd`, `edition` are removed from the customer-facing title block when the active output rule calls for it.
- Korean title must not be left as a placeholder where the active guide output requires a translation; unsupported source fields still remain blank.
- Search-result URLs are not accepted as product-detail links. Uncertain links remain blank.
- Historical guide flow used an ANCHOR/source-reference concept tying output to source file, sheet, and row. Future guide export must preserve equivalent traceability when source rows are available.

### PASS/X and shell-risk prevention
- PASS/X is a system-side validation gate, not work delegated to the user.
- A row/output must fail or stop when unsupported ISBN/publisher/date/price/placeholders are generated, source traceability is lost, or required validation evidence is missing.
- Historical forbidden fake/placeholder values include `0`, `TBD`, example data presented as real data, fake ISBN, and fake price.
- User role remains observer/reviewer; repeated manual comparison or repeated PASS/X checking must not be required.

### Historical vs current implementation
- Historical records include Word-only output and later a transition toward UI-based PASS/X automation. These are historical workflow stages, not proof that every Word-export feature is implemented in the current runtime.
- The current verified product status remains `COMPLETE / REMOTE_VERIFIED` for the verified CSV pipeline above.
- Any future Word/customer-guide export feature is NEW/changed scope and requires its own FIRST_VALIDATION once; it must not cause retesting of unchanged verified CSV/runtime scope.

## Historical source set used for catch-up
- `27번 공학 도서 안내.doc`
- `27번 공학 도서 안내(1).doc`
- `27번 공학 도서 안내(2).doc`
- `27번 공학도서 안내 도구.doc`
- `27번 공학도서 안내 도구(1).doc`
- `27번 공학도서 안내 도구(2).doc`
- related TOOL027 fixed-instruction capture(s), where not superseded by newer explicit user direction

## Catch-up state
- Historical numbered-chat canonicalization: COMPLETE
- Existing product/runtime COMPLETE state preserved without unchanged-scope retest.
- No new repository created; existing canonical repository reused.

## Reopen gate
TOOL027_REOPEN = REAL_USE_NEW_FAILURE_ONLY
RETEST_UNCHANGED_SCOPE = FORBIDDEN
