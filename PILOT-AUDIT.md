# CFA Study Hub 15.0 Pilot — Audit, Design System & Rates and Returns

**Scope:** one pilot learning module only, CFA26-01-01. Base: v14.2 (67 files). Do not roll this design out to the remaining 92 modules until academic review and user approval. This report distinguishes functionality, source coverage, and learning effectiveness; it does not certify completion of the CFA project.

## 1. Audit findings and evidence

| Area | Finding from v14.2 | Pilot remedy / pending |
|---|---|---|
| Live website | Public HTML returned only the JS startup shell when retrieved; browser policy blocked navigation to live and test URLs. The rendered deployed version could not be verified. | Local Chromium injection used exact artifact CSS/JS; final deployment verification remains open. |
| Information architecture | `study-v14.js` uses hash routes and shared Subjects, Library, Question Bank, Mock Exams, Review and Settings navigation. Lesson, Formula, Review and Practice overlap; `lecture` groups existing audit rows and maps some cards by page. | Replace only LM1 Lesson with a continuous, concept-first pilot; direct links to original practice, Library, source pages and old lesson retained. Global menu migration pending. |
| Language | `pair()` in old renderer puts VI and EN text in parallel; language options are both, VI and EN. | Pilot defaults to English, short Vietnamese support, expandable existing VI summaries; English Only and Full Vietnamese mode. Existing settings outside pilot unchanged. Full mode expands available explanations, not a full literal translation of every source. |
| Content organization | LM1 contains 18 source audit rows, 21 formula cards, 20 worked-example cards, 15 numbered source examples and 17 exhibit locators. These are not equivalent to a full source transcript or complete academic acceptance. | Explicit topic placements, 8 blocks under all 5 LOS, integrated formulas, conditions, selected step solutions and concept recognition. All old rows/cards retained. |
| Source and library | `source-bank.js` indexes 534 PDFs and locators; `private-study.js` uses local JSON/gzip, IndexedDB and original-PDF inputs. Source data and practice depend on optional private materials; the integrated lesson does not need them. | Integrated pilot content and source-adapted knowledge checks work without upload; references open the existing source reader, whose original-material access still depends on user-owned sources. No public original PDFs added. |
| Search | Existing global search matches modules/LOS titles and documents, not arbitrary concept/formula text. | Pilot search indexes titles, concepts, recognition cues and formulas. Results jump to the relevant learning block. Global concept indexing remains pending. |
| Progress / review | Old module completion is manual; original-question review uses saved/self-graded records. | Separate pilot state stores visited blocks, latest graded checks, saved checks and language. Review by LOS uses actual submitted answers; no Mastered claim. Does not overwrite old keys. Full spaced repetition, flashcards and global analytics remain pending. |
| Code / performance | Main page eagerly loads recap and source-bank JS. Legacy files remain in distribution. | Three new scoped files; no backend/external dependency. Full lazy loading and legacy code audit deferred until approval. |

Design references consulted: CFA Institute Learning Ecosystem (https://www.cfainstitute.org/programs/cfa-program/learning-ecosystem), CFA Institute practice feedback (https://www.cfainstitute.org/programs/cfa-program/candidate-resources/mock-exam-and-practice-questions), Khan Academy mastery learning (https://support.khanacademy.org/hc/en-us/articles/115002552631-What-are-Course-and-Unit-Mastery). Used only general product principles, not content outside the supplied curriculum.

## 2. Design system (pilot implementation)

- English-first. Support mode: one concise Vietnamese explanation per block; expand additional explanations when requested. English Only hides VI; Full Vietnamese expands available explanations. Six term definitions are clickable.
- Single continuous lesson; collapsible contents, block and source deep links, Focus Mode, light/dark tokens, keyboard controls, responsive layout. No mandatory Next click.
- Essential layer: objective, purpose, key concept, math and conditions, selected visual and worked example. Detailed layer: expandable solution, Vietnamese explanation, secondary source note. Source layer: source button and PDF page/coverage map.
- Reusable renderers: concept, formula (native MathML), worked example, timeline, comparison table, line chart, simulation, knowledge check, explanation and review. Formula conditions stay visible. Native MathML requires a modern compatible browser; no external CDN.
- Provenance labels distinguish source summaries, source-adapted checks and teaching simulations. No new exam-bank questions beyond the source scope; 13 local pilot checks are reworded from the 13 CFAI practice questions and are kept separate from original bank items.

## 3. Prototype coverage

Primary source reopened from supplied archive: `2026_CFA_L1V1_Quant_ONLINE.pdf`, SRC-0122, physical PDF pp. 11–52. SHA-256 `e294b2466b4112bc9e42d99c708458822b75d7f302e2f4a84f1a6e37b08ca702` matches catalog. LOS wording from p.11; topic audit from pp.11–45; checks and solutions from pp.46–52. Preserve existing 18 topic groups, 21 formula cards, 20 example cards (representing 15 numbered examples and additional illustrations; some multi-part examples are summaries), 8 traps and 17 exhibit locators. This is card-level coverage, not a cell/paragraph-level content acceptance.

| Block | LOS | Topics | Primary PDF pages | Checks |
|---|---|---|---|---|
| Interest rates and time value of money | a | 0–2 | 11–15 | 1,2 |
| Holding-period and linked returns | b | 3 | 16–19 | linked to next block |
| Choosing the right mean | b | 4–7 | 17–27 | 3,4,5 |
| Money-weighted vs time-weighted return | c | 8–10 | 27–36 | 6,7 |
| Compounding frequency and present value | d | 11 | 36–38 | linked to next block |
| Annualized and continuously compounded returns | d | 12–13 | 38–41 | 8,9 |
| Gross, net, after-tax and real returns | e | 14–16 | 41–45 | 11 |
| Leveraged return and risk premium | e | 17 | 44–45 | 10,12,13 |

Secondary source checks: reopened SchweserNotes Book 1 pp.14–28 (SRC-0134), SAPP Quant Slides pp.4–33 (SRC-0018), SAPP Quant Mindmap p.1 (SRC-0010); all three SHA-256 matched existing records. Topic-level comparison, not exhaustive secondary-source review. Added Kaplan approximation/purchasing power example (p.25) and SAPP multiplicative return and leverage convention (p.25) as linked detailed source notes. SAPP defers part of LOS d into Module 2, so further cross-module checks are required before declaring coverage complete. Source p.24 printed arithmetic×harmonic=geometric² is not valid for arbitrary positive sample size; the existing note flags it; use HM≤GM≤AM for positive inputs. Source Q2 explicitly selects liquidity among the available three choices; default risk is not an offered choice. Original source is preserved.

Interactive models: PV vs discount rate (source Example 11), HPR annualization (Example 12), debt/equity return (source p.44). Default numerical checks: CAD2,748,163.67, 24.55%, and 9.29%, respectively. Values changed by the learner are simulations; not new source questions. Formula renderer uses 21 retained MathML cards plus one additional secondary-source formula in a detail panel.

## 4. Files changed

- Modified `index.html` (load the pilot's data and renderer with versioned assets, set EN document language), `study-v14.js` (LM1 route, search result, review link, Continue route), `README.md`.
- Added `prototype-rates-data.js` (objectives, 8-block map, 13 adapted source checks and formula conditions), `prototype-rates.js` (renderer and local state), `prototype-rates.css` (scoped design), this report.
- All original recap, catalog, source-bank, private-study and other legacy data files remain byte-identical to v14.2. Old LM1 remains available at `#module/CFA26-01-01/learn/legacy` and other 92 modules use the original renderer. No change to v13.7 private package or its storage key. Pilot key: `cfa26-rates-prototype:v1`.

## 5. Actual tests and limitations

- Chromium isolated test with `page.set_content` and exact local CSS/JS; test localStorage substitute. Counted all 8 blocks, 18 topic groups, 21 formula cards (+1 secondary MathML), 20 example cards, 13 checks, 3 simulations. Tested language switching and inline VI, TOC, source default numerical values and changed PV and leverage settings, correct/incorrect grading and 50% review on two attempts, saving and marking a block, state write and route navigation, concept search, focus toggle, fallback old LM1, LM2 render, 534-document Library, review link and mobile width 390px. No page errors observed on completed smoke run. Browser navigation to an HTTPS origin returned ERR_BLOCKED_BY_ADMINISTRATOR; actual reload/persistence on GitHub Pages and real IndexedDB restore were not verified. Private original source dialog is existing code; source pack not required for integrated learning; actual pack restore was not retested here. A longer test with reload failed/timed out, not counted as pass. Screenshots from completed local browser tests, not mockups.
- Node syntax checks, static asset references, unchanged baseline data hashes and flat ZIP integrity. No real deployment made.
- Source data card retention 18/18, 21/21, 20/20; 5/5 LOS represented; 13/13 source practice items adapted and linked. 1/93 modules use prototype. These counts do not measure completeness of all original material or effectiveness of learning. No defensible overall academic completion percentage.

## 6. Stage gate

| Stage | Status | Remaining |
|---|---|---|
| Audit | Partial — suitable to build scoped pilot | Full live deployment and exhaustive legacy-code audit |
| Design System | Pilot implemented | User evaluation, subject-specific variants later |
| Prototype | Implemented | Detailed source acceptance, full VI explanation depth, full worked-example subparts and exhibit cells |
| Verification | Technical smoke PASS; overall NOT ACCEPTED | Live storage/deployment, tablet/browser breadth, full academic source comparison and user confirmation |
| Rollout | NOT STARTED | Wait for explicit user approval; do not replicate to the remaining 92 modules |

## 7. Review instructions

Upload the whole ZIP contents to your GitHub Pages root (71 flat files) or extract and open with a static web server. Navigate Subjects → Quantitative Methods → Rates and Returns, or append `#module/CFA26-01-01/learn/0` to the website URL after deployment. Integrated pilot needs no import. Use the existing v13.7 personal study package only to view original copyrighted materials or original question bank; no re-download necessary. To compare the old layout, use Source references → Previous full lesson. Retain original project files and user storage. Evaluate the actual prototype before any expansion.
