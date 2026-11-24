# Study Hub v6.3 — Learning Experience Redesign

Bản đầy đủ 61 file ở thư mục gốc. Upload tất cả sau khi giải nén vào GitHub Pages, main / root. Không upload nguyên ZIP. Bản này giữ nguyên dataset 365 LOS/6.803 MCQ của v6.2. `index.html` và `deep.html` dùng giao diện mới; `legacy.html` và `legacy-deep.html` giữ nguyên cách trình bày cũ. `study-index.js` là chỉ mục nhẹ, `study.js` tải dataset theo môn khi cần, `quant-bridge.js` đưa 8 bài HTML Quant vào trình học mới. Không phụ thuộc CDN/backend. Đáp án cũ vẫn dùng key localStorage `cfa26-studyhub:quiz:v1:`; tiến độ đọc/thẻ/lịch sử mới dùng key riêng. Sao lưu tại Cài đặt & dữ liệu. Nội dung cũ là bản nháp học thuật, chưa nghiệm thu toàn diện; các mô phỏng là minh họa, mock ngẫu nhiên không phải đề chính thức.

---

# CFA Level I 2026 Study Hub v6.2 — Static GitHub Pages

Release v6.2: 55 files; LM4 GIPS (5 LOS) and LM5 Ethics Application (2 LOS). 85 theory sections, 18 frameworks, 95 worked cases, 95 English MCQs, 198 flashcards. All 365/365 catalog LOS covered by detailed academic drafts; 6,803 detailed MCQs. This is a coverage milestone, not academic certification. Next: full academic/coverage gap audit, QBank/Mock/prerequisite mapping, legacy generic question quality and actual hosted deployment checks. Update deep-eth.js, app.js, index.html, README.md; earlier data and progress keys retained.

## Historical releases
# CFA Level I 2026 Study Hub v6.1 — Static GitHub Pages

Release v6.1: 55 files; added LM3 Guidance for all 23 sub-standards across three LOS. 112 theory sections, 45 qualitative frameworks, 112 original cases, 112 English MCQs, 269 flashcards. 358/365 detailed draft LOS; 6,708 detailed MCQs. Remaining: LM4 GIPS (5 LOS), LM5 Ethics Application (2 LOS). Update deep-eth.js, app.js, index.html, README.md. Existing content and progress keys preserved. Source-mapped academic draft; not independently certified.

## Historical releases
# CFA Level I 2026 Study Hub v6.0 — Static GitHub Pages

**Release v6.0:** 55 root files. Added Ethics LM1–LM2: 11 LOS, 95 theory sections, 30 qualitative frameworks, 37 original worked cases, 132 English MCQs, 162 flashcards. 355/365 detailed draft LOS; 6,596 English detailed MCQs. 10 Ethics LOS remain; LM3 needs full sub-standard guidance despite 3 LOS. Includes I(E) Competence, V(B) service/cost disclosure, VI(A) Avoid or Disclose Conflicts. New deep-eth.js; update app.js, deep.js, deep.html, index.html, README.md. Existing datasets and progress keys retained. Original learning material, not official or independent certification.

## Historical release notes
# CFA Level I 2026 Study Hub v5.9 — Static GitHub Pages

**Release v5.9:** 54 root files. Added Portfolio Management LM5–LM6: 10 official LOS, 98 theory sections, 30 formulas/frameworks, 30 worked cases (17 numeric), 115 English practice questions, 145 flashcards. Running count: 344/365 detailed draft LOS, 6,464 detailed MCQs; 21 Ethics LOS remain. PM 40/40 draft LOS. From v5.8 replace deep-pm.js, app.js, index.html, README.md. Original questions; numeric supplements not additional LOS. Prior progress keys retained. Not independent academic certification.

## Historical release notes
# CFA Level I 2026 Study Hub v5.8 — Static GitHub Pages

**Release v5.8:** 54 root files. Added Portfolio Management LM3–LM4: 14 official LOS, 94 theory sections, 37 formulas/frameworks, 44 worked cases (30 numerical and 14 conceptual), 124 English practice questions, 161 flashcards. Running project count (carried from v5.7): 334/365 detailed draft LOS, 6,349 detailed MCQs; 31 LOS remain (10 PM + 21 Ethics). New questions are original; worked numerical examples are also available as practice. From v5.7 replace `deep-pm.js`, `app.js`, `index.html`, `README.md`. All old modules and old quiz keys retained. Numeric supplements are not extra LOS. Not a comprehensive independent academic certification.

## Historical release notes
# CFA Level I 2026 Study Hub v5.7 — Static GitHub Pages

**Release v5.7:** 54 root files. Added Portfolio Management LM1–LM2: 16 official LOS, 82 theory sections, 52 formulas/frameworks, 77 worked cases, 143 original English practice questions, 195 flashcards. Running project count: 320/365 detailed draft LOS, 6,225 detailed MCQs; 45 LOS remain (24 PM + 21 Ethics). New questions are original; worked numerical examples are also available as practice. From v5.6 add `deep-pm.js` and replace `app.js`, `deep.js`, `deep.html`, `index.html`, `README.md`. All historical quiz keys retained. Not a comprehensive independent academic certification.

## Historical release notes
# CFA Level I 2026 Study Hub v5.5 — Static GitHub Pages

**Release v5.5, 2026-11-24:** 53 root files, 10 subjects, offline-compatible HTML/JS, no backend. Expanded **Alternative Investments LM1–LM2** (5/22 official LOS): 57 theory sections, 30 formulas/frameworks, 106 original examples, 155 original English MCQs and 193 flashcards. Entire site: **294/365 detailed draft LOS**, **5,864 detailed original English MCQs**. Remainder: 17 Alternatives + 40 Portfolio Management + 21 Ethics = 78 LOS. Status: *source-mapped detailed draft*, **not comprehensive academic certification**.

**Deployment:** Extract 53 files to GitHub Pages root. From exactly v5.3, replace `app.js`, `deep.js`, `deep.html`, `index.html`, `README.md` and ADD `deep-alt.js`. Other 47 files are byte-identical. Retain previous progress JSON backup; question keys are preserved.

**Primary source:** CFAI Level I 2026 Alternative Investments Volume 8 physical PDF pages 11–72; supporting Kaplan 2026 Book 4 pp11–27 and SAPP Alternative Investments slides pp3–23 and pp169–195. The source PDFs and licensed banks are not part of public website.

**Private audit** is packaged separately, and live GitHub Pages storage persistence is not verified in this environment.

---

## Prior checkpoint: v5.3 (retained release history)

# CFA Level I 2026 Study Hub v5.3 — Static GitHub Pages

**Complete website upload:** 52 root files. No database, no server, plain HTML/CSS/JS. Version v5.3 supersedes previous checkpoints. Historical release notes below are retained for traceability.

## GitHub Pages upload
1. Extract all **52 site files** from the website ZIP. Upload them into the root of your current GitHub repository, overwriting same-named files. Do not upload ZIP itself.
2. Ensure `index.html`, `deep.html` and all `.js` files are at repository root. Settings → Pages → Deploy from a branch → main → /(root).
3. Keep the separate private audit ZIP off GitHub. Source CFA Institute/Kaplan/SAPP textbooks, commercial QBank or mock PDF files should not be uploaded to a publicly shared site.

## Current content status (DRAFT, not academically signed off)
- 10 subjects, 93 Learning Modules + 1 prerequisite appendix catalog. Retained inherited general draft content.
- **282/365 LOS detailed drafts:** 38/38 Quantitative Methods, 30/30 Economics, 22/22 Corporate Issuers, 53/53 Financial Statement Analysis, 66/66 Equity, 51/51 Fixed Income, 22/22 Derivatives. Remaining: 22 Alternatives, 40 Portfolio, 21 Ethics. Historical generic lessons also remain in the catalog.
- **5,547 authored detailed English MCQs** (not including 1,278 inherited generic draft MCQs, which still need English-language and academic QA). Teaching and explanations primarily Vietnamese; original English three-choice exam questions.
- Previously authored in the project's FSA phase: **FSA LM6** Analysis of Inventories (3 LOS, 73 sections, 47 frameworks, 52 worked examples, 108 English MCQs, 120 cards); **FSA LM7** Analysis of Long-Term Assets (3 LOS, 60 sections, 26 frameworks, 43 examples, 79 MCQs, 86 cards); **FSA LM8** Topics in Long-Term Liabilities and Equity (3 LOS, 86 sections, 36 frameworks, 69 examples, 105 MCQs, 122 cards); **FSA LM9** Analysis of Income Taxes (4 LOS, 90 sections, 36 frameworks, 90 examples, 138 MCQs, 126 cards); **FSA LM10** Financial Reporting Quality (8 LOS, 108 sections, 35 frameworks, 80 original case examples, 96 MCQs, 143 cards).
- Example URL: `deep.html?module=CFA26-04-10&los=LOS01`. Each detailed page links from the 10-subject catalog.

## Grounding and validation
- Primary: CFA Institute Curriculum Level I 2026 Volume4 FSA pp185–203, pp221–242, pp253–283, pp289–317, pp323–392 (physical PDF). Cross-checked topic anchors in Kaplan SchweserNotes 2026 Book2 Readings32–36 and SAPP FSA Slides 2026 Modules6–10.
- Numerical QA: **571/571** numerically generated cases reconstructed independently from the English problem stems and matched stored answer values (FSA LM6–7: 189, LM8: 138, LM9: 180, LM10: 64). This checks arithmetic only, **not** independent textbook-level adjudication of all concepts and distractors.
- English question format checked for new modules; no literal overlap between solved examples and graded question stems. All 37 public JavaScript files passed `node --check`.
- Chromium DOM harness passed all **15/15** Module6–10 desktop/mobile pages and catalog links; 390-pixel mobile pages had no horizontal overflow in the tested flows. Sandbox blocked direct local-URL navigation, so live GitHub Pages URL has **not** been tested.
- Progress stored on the local browser/device (`localStorage`) and can be exported/imported; no automatic cloud sync.

## Outstanding before academic completion
- Independent **line-by-line** Curriculum cross-check and answer-key signoff for all drafted LOS, including conceptual MCQ distractors and rare edge cases.
- Full 534-source-PDF coverage audit not completed: scope verification so far covers selected relevant page ranges.
- 1,278 inherited generic MCQs need English migration/verification; 170 older Quant questions still need full independent answer audit.

## v3.5 additions (FSA draft coverage milestone)
- New: Financial Statement Analysis LM11 **Financial Analysis Techniques** (6 LOS) and LM12 **Introduction to Financial Statement Modeling** (5 LOS); **143/365** project LOS now have detailed study drafts, including **53/53 FSA**.
- Two new module objects were appended to the existing `deep-fsa.js` file; route links in `app.js`. The complete website still has 50 root files. No backend or paid infrastructure is needed.
- New original material: 159 explanation sections, 92 formulas/analytical frameworks, 61 worked examples, 187 original English MCQs, 170 recall cards. This content is deliberately *not* a reproduction of any commercial PDF or question bank.
- Primary source: 2026 CFA Institute Level I Financial Statement Analysis Volume 4, Learning Module 11 and 12; Kaplan 2026 Book 2 Readings 37–38 and SAPP FSA Slides 2026 modules 11–12 used for topic cross-checks only.
- **No academic certification yet.** Source alignment and checked computations do not imply line-by-line validation of the full Curriculum, conceptual distractors, accounting alternatives or future standards updates.
- Known legacy gaps: 1,278 inherited general MCQs still need English/academic QA; original 170 Quant detailed questions need independent complete answer review; complete PDF-source audit still pending.
- Progress stored via browser `localStorage`; export/import via the detailed lesson page.

## v3.6 Equity Investments LM1
- Added 12 source-mapped LOS for Market Organization and Structure; 36 original English MCQs, original Vietnamese learning notes, 12 sets of flashcards, and worked margin examples. This is a **study draft**, not certified exhaustive Curriculum coverage.
- Source inspected: CFAI 2026 Equity Investments Volume 5 LM1, physical PDF pp13–90; outcomes at physical p13. More detailed page-by-page and distractor audits are outstanding.
- Site contains 50 root files; `deep-equity.js` hosts Equity detailed module records.

## v3.7 Equity LM2
- Added 11 draft LOS for Security Market Indexes with calculation and conceptual coverage; detailed draft total 166/365 and English detailed questions 3,296.
- CFAI 2026 Equity Volume5 LM2 verified official outcomes at physical PDF p91, chapter content pp92–130. Source checks do not yet equal exhaustive academic audit.

## v3.8 update — Equity Investments LM3 through LM8
- 43 new source-outcome-mapped detailed LOS drafts (total detailed draft coverage: 209/365); 215 theory sections, 102 analytical frameworks/formulas, 43 original applications, 129 original English MCQs, 215 flashcards.
- The new Equity total is 66/66 official Equity LOS. All question stems and choices are English; explanations are Vietnamese/English; academic editorial signoff for detailed 2026 full-chapter fidelity is still PENDING.
- Static hosting unchanged: 50 root files (only deep-equity.js, app.js and README.md changed). No copyrighted curriculum, Kaplan, question-bank or mock PDFs included.

## v3.9 source-first Fixed Income LM1–LM3
- Newly integrated dedicated `deep-fi.js`; **7 official 2026 FI LOS** in the first three learning modules. Added **82 bilingual theory sections, 37 formula/framework records, 21 original worked cases, 70 original English 3-choice MCQs, and 72 flashcards**. Prior general Fixed Income material and all prior subjects remain.
- Program accounting: **216/365 detailed draft LOS** and **3,698 detailed English MCQs** (excluding **1,278** previously inherited generic Qs still requiring QA). Source comparison anchored to CFA Institute 2026 FI Volume 6 physical pp13–32, 33–63, and 65–87, with Kaplan 2026 SchweserNotes Book3 Readings47–49 and SAPP FI slides Modules1–3 as secondary topic checks.
- This is **not a certification of complete book-by-book equivalence**. Targeted official learning-outcome and subject comparison performed; comprehensive paragraph-level audit of all relevant passages, editorial adjudication of every distractor and browser-hosted GitHub acceptance testing remain outstanding. All examples/MCQs are original; no copyrighted QBank, Mock, publisher PDFs or user-supplied documents are distributed in this website ZIP.
- Website now has **51 flat root files** (new `deep-fi.js`; updated `app.js`, `deep.js`, `deep.html`, and `README.md`). The audit and builder ZIP must be kept separate from public website.


## v4.0 source-first FI LM4–LM5 — 2026-11-23
- Deep FI extended in **same `deep-fi.js`** from modules 1–3 to **modules 1–5**: new **5 official LOS** (3 in Corporate Issuers funding/repo/IG-vs-HY, 2 in Government Issuers), **62 theory sections, 28 formula/framework entries, 21 worked examples, 67 original English 3-choice MCQs, 90 bilingual flashcards**.
- Aggregated **221/365 detailed draft LOS** and **3,562 original detailed English MCQs**; excludes 1,278 inherited generic questions needing English/academic QA.
- Primary source: CFA Institute 2026 Fixed Income Volume 6 physical PDF pp89–136, secondary context from Kaplan Book3 pp37–52 and SAPP FI slides pp134–195. These PDFs and publisher questions are not redistributed.
- 5 new LOS deep links integrated into `app.js`; website remains **51 flat root files**, <100 GitHub uploads. Only `deep-fi.js`, `app.js`, `README.md` changed versus v3.9.
- Content remains **academic drafts**, not certified full-source equivalence; complete line-by-line and conceptual answer audits and live hosted GitHub test still outstanding.


## v4.1 source-first Fixed Income LM6 — 2026-11-23
- Added CFAI 2026 Fixed Income LM06 **Fixed-Income Bond Valuation: Prices and Yields** with 3 official LOS, source-aligned independent Vietnamese instruction and original English-choice MCQs, detailed numerical examples and flashcards.
- Main topics: on-coupon and between-coupon DCF pricing; periodic YTM and IRR; accrued interest actual/actual and 30/360; clean versus full; price–yield–coupon–maturity effects; constant-yield pull to par; matrix pricing of illiquid/new bonds from comparable yields and benchmark spreads.
- Official source: CFA Institute 2026 FI Volume 6 pp137–166; secondary: Kaplan SchweserNotes Book3 Reading52 PDF pp52–61; SAPP FI slides module6 PDF pp197–229; original source PDF pages and publisher question bank are NOT redistributed.
- Detailed draft progress **224/365 LOS**, Fixed Income **15/51**; **3,628** authored detailed English MCQs (inherited 1,278 generic questions excluded).
- Only `deep-fi.js`, `app.js`, and `README.md` updated; retains 51 flat site files. Material is a carefully source-aligned study draft, not certified complete line-by-line academic equivalence.

## v4.2 Fixed Income LM7 source-first
Added official LM7 2 LOS: compounding-yield conversions and fixed-bond yield/spread measures with original English MCQs, complete explanations, formula assumptions, worked examples and flashcards. References and QA summary are in private audit package; do not deploy the audit package. Draft pending independent academic review.

## v4.3 — Fixed Income LM8–LM9 (23 Nov 2026)

- Added 5 CFAI 2026 official LOS in Fixed Income LM8 and LM9 with 165 original English multiple-choice questions.
- Site deep-draft progress 231/365 LOS; FI 22/51; detailed English MCQs 3,863; flat 51-file GitHub Pages deployment.
- Primary sources: CFAI 2026 Fixed Income Vol 6 pp197–248; Kaplan SchweserNotes Book 3 Readings 54–55; SAPP FI Slides Modules 8–9. Original explanations and questions only; publisher text excluded.
- Academic limitations: source-mapped detailed draft, not exhaustively audited against every licensed example or mock. Live GitHub deployment and hosted localStorage not verified.

## v4.4 — Fixed Income LM10–LM11 (23 Nov 2026)
- Added 5 official outcomes (LM10 3, LM11 2), 162 new original English MCQs; full-site detailed academic-draft coverage 236/365; FI 27/51; 4,025 detailed original English MCQs.
- Official CFA Institute 2026 FI Volume6 physical pp249–306; secondary Kaplan Book3 Readings56–57, SAPP FI modules10–11. Publisher questions/text not distributed.
- Static 51-file GitHub Pages website; existing records retained; not academic-certification or live-hosting tested.

## v4.5 — Fixed Income LM12–LM13 (23 Nov 2026)
- Added all 7 official CFAI 2026 outcomes: LM12 (3) and LM13 (4), with 160 new original English 3-option MCQs, 112 solved examples, 69 theory sections, 49 formula/assumption notes and 258 flashcards.
- Site now has 243/365 detailed academic-draft LOS; 34/51 FI LOS; 4,185 detailed original English MCQs. Entire deploy remains 51 flat files for GitHub Pages.
- Source mapping: CFA Institute FI Volume 6 physical PDF pp307–354, Kaplan SchweserNotes Book 3 Readings 58–59, SAPP Fixed Income Modules 12–13. New work is original educational content, not copied publisher questions or textbooks.
- Checks: structure and independent numeric testing and limited Chromium desktop/mobile regression; not a line-by-line academic certification or a test on a live GitHub Pages URL.


## v4.6 — Fixed Income LM14–LM15 (24 November 2026)
- Source-first bilingual lessons: official CFAI FI 2026 LM14 (3 LOS: credit risk, ratings, spread factors) and LM15 (1 LOS: government issuers). Independent English questions and VI explanation, examples, formulas and flashcards.
- New detailed draft coverage: **4 LOS**; overall **247/365**, FI **38/51**. Detailed authored MCQs: **4,398**. Under 100 files: 51 flat files.
- CFAI FI 2026 PDF physical pp355–417, Kaplan 2026 Book3 Reading 60–61, SAPP FI Module 14–15. Material newly authored, NOT publisher QBank/exercises.
- Academic QA is selective. Hosted Github Pages and cross-device sync not verified. No backend; progress remains browser-local.


## v4.7 — Fixed Income LM16–LM17 (24 November 2026)
- Detailed bilingual draft expanded by 5 official LOS (FI 43/51, program 252/365). Original English MCQ +177; total 4,575.
- Sources: CFAI FI 2026 Volume 6 PDF physical pp421–474, Kaplan 2026 Book3 Readings 62–63, SAPP FI 2026 Slides Modules 16–17. No publisher text or question-bank reproductions.
- Ratios and ABS cash waterfalls use explicitly stated simplifying assumptions. Numeric calculations independently checked in audit. Non-numeric academic fact check is selective; live GitHub Pages site untested.


## v4.8 — FI LM18–LM19 (24 November 2026)
- Added 8 official LOS-draft lessons: FI 51/51, program 260/365, +220 original English 3-choice MCQs (total 4,795).
- Main source CFAI 2026 FI V6 physical PDF pp475–545, Kaplan Book 3 Readings 64–65, SAPP FI Modules 18–19. All teaching/MCQs newly authored; copyrighted source PDFs not redistributed.
- Asset/loan math is conditional on simplifying assumptions; see QA and original source mapping. Academic conceptual audit of every entry and live GitHub Pages deployment not yet verified.


## Update v4.9 — Derivatives LM1–LM2
- Added `deep-der.js` with original bilingual detailed drafts for 5 official CFAI 2026 LOS from Derivatives Volume 7.
- `deep.html`, `deep.js`, `app.js`, and `index.html` updated to load and navigate these pages; original public lessons otherwise unchanged.
- Source details, numerical checks and limitations in private QA handoff. No publisher PDF or QBank copied into public website.
- Updated detailed-draft coverage: 265/365 (the 260 prior plus Derivatives LM1–LM2).


## Update v5.0 — Derivatives LM3–LM4
- Extended existing `deep-der.js` with 4 official LOS from LM3 Derivative Benefits/Risks/Uses and LM4 Arbitrage/Replication/Cost of Carry, preserving the LM1–LM2 data.
- Added 66 theory sections, 22 formula and assumptions notes, 60 original solved exercises, 126 authored English three-choice MCQs and 148 flashcards.
- `app.js`, `index.html`, `deep.js`, `README.md`, `deep-der.js` are the only modified assets. No new root files (52 total).
- Progress summary 269/365 detailed draft LOS; 5,051 authored English MCQs; outstanding 96 (Derivatives 13, Alternatives 22, Portfolio 40, Ethics 21).
- Source-grounded but not fully signed-off academic draft. Note corrected equation: continuously compounded forward price is `S0*exp(rT)` (not `S0*r*T`).


## Update v5.1 — Derivatives LM5–LM6
- Detailed four CFAI 2026 official LOS from LM5 (forward mark-to-market, term structures, FRA) and LM6 (futures pricing and settlement, forward–futures differences).
- Original bilingual content: 65 theory sections, 40 formula/conditions notes, 105 solved examples, 170 authored English MCQs and 210 flashcards; not copied from source QBank.
- Added to existing `deep-der.js` without modifying older Derivatives LM1–LM4. Only `deep-der.js`, `app.js`, `index.html`, `README.md` changed; root file count stays 52.
- 273/365 detailed draft LOS, 5,221 authored detailed English MCQs, 71 LOS still to expand (Derivatives 9, Alternatives 22, Portfolio 40, Ethics 21).
- See private audit for coverage/source crosswalk and independent checks. Original draft is not academically signed-off.


## Update v5.2 (2026-11-24)

- Derivatives LM7 and LM8: 5 official 2026 CFAI LOS, original bilingual detailed draft, English practice questions.
- Added 63 theory sections, 45 formula notes, 96 solved examples, 161 MCQs, 154 cards.
- Site coverage: 278/365 LOS detailed draft; 5,382 authored English detailed MCQs. Derivatives 18/22.
- Prior v5.1 modules preserved exactly within `deep-der.js`; unchanged progress key `cfa26-studyhub:quiz:v1:`.
- QA debt: hosted GitHub Pages test and full independent academic peer review of conceptual questions not done.


## v5.3 (2026-11-24) — Derivatives complete detailed drafts
Added LM9–LM10: 4 LOS, 165 original English MCQ, 117 solved examples. CFAI source pages and assumptions logged in private handoff. Coverage now 282/365 detailed draft, Derivatives 22/22, 5,547 English detailed MCQs. Prior progress keys and all earlier deep modules retained.


## v5.5 — Alternative Investments LM3–LM4
- New modules: 7 LOS, 76 theory blocks, 37 formula/frameworks, 139 original worked cases and 162 original English MCQs.
- Updated deep-alt.js, app.js, index.html and README.md; no other root files need change.
- Unchanged local quiz storage keys; export backup before replacing site.


## v5.6 — Alternative Investments LM5–LM7 (2026-11-24)
- Added 10 official LOS to deep-alt.js; 22/22 Alternative Investments detailed academic drafts. Added 218 original English MCQ and additional solved examples / flashcards.
- Overall detailed draft status: 304/365 LOS; 6,082 detailed English MCQs. Remaining 61 LOS: Portfolio Management 40; Ethics 21.
- Do not upload source CFAI, Kaplan, SAPP PDFs or the private audit ZIP to public GitHub. All figures in examples use simplified stated assumptions; academic re-audit pending.
