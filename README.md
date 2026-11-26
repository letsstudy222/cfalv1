# Study Hub v14.0 — thiết kế lại luồng tự học

**Cài đặt:** giải nén ZIP, upload 67 file vào cùng thư mục gốc GitHub Pages (ghi đè `index.html`, `private-study.js`, README; thêm `study-v14.js`, `study-v14.css`, `study-archive.html`). Sau khi GitHub Pages hoàn thành triển khai, mở `/#home` và refresh mạnh nếu giao diện cũ còn trong cache. Không đưa gói `.json.gz` lên repository công khai. Bản v14 dùng lại gói `CFA_2026_Private_Study_Data_v137.json.gz` và cùng khóa IndexedDB từ v13.8; nếu gói đã lưu đúng trên trình duyệt, tự khôi phục khi mở nội dung gốc. Nếu chưa lưu, chỉ chọn một lần; quyền lưu phụ thuộc trình duyệt.

## Luồng học
- Trang chủ tiếp tục đúng module và phần gần nhất; 10 môn; tiến độ đánh dấu đã học thủ công.
- Môn học → module → 4 tab: Học lý thuyết, Công thức & ví dụ, Tổng kết, Luyện câu hỏi. Lý thuyết là bản tóm lược nhóm kiến thức; chọn ngôn ngữ và đọc nguồn ngay tại phần tương ứng. Liên kết chi tiết cũ vẫn có trong mục đọc tài liệu gốc.
- Luyện câu hỏi: lọc môn/module/nguồn/trạng thái, chọn số câu và thứ tự. Phiên luyện dùng đúng danh sách đã lọc. Đề thi thử: 52 phiên nguồn không trộn năm. Câu gốc tự chấm theo lời giải; chưa có đồng hồ thi hoặc tự chấm toàn bộ. Ôn câu sai/chưa chắc/đã lưu dùng khóa tiến độ nguồn cũ.
- Cài đặt: thư viện gốc, thiết lập học liệu, tìm toàn văn, kiến thức nền, xuất tiến độ v14; giao diện cũ tại `study-archive.html`. Giữ tất cả 64 file cũ (cập nhật 3 file), thêm 3 file mới. Không tạo thêm nội dung học thuật/câu hỏi.

## Kiểm thử
- 399 lượt render Chromium cô lập: 93 × 4 tab + 10 trang môn + 10 trang tổng kết môn + 7 trang chính/tìm kiếm; không có thông báo lỗi render. Thử với gói v13.7 thật: nạp gói, lọc 10 câu Kaplan, chọn A, hiện lời giải, tự chấm sai, ôn lại; 52 phiên Mock; đánh dấu/bỏ đánh dấu module; giao diện 390px không tràn ngang trên trang chủ/bài học. Kiểm tra cú pháp mọi JS, dữ liệu `study-index.js`, `recap-data.js`, `source-bank.js` và toàn bộ JS học liệu cũ nguyên byte. Test DOM bằng script thật, localStorage mô phỏng vì môi trường chặn điều hướng URL/file. Không xác nhận IndexedDB tồn tại qua lần tải lại thật; chưa kiểm thử bản triển khai GitHub. Bản này chỉ sửa trải nghiệm; giới hạn học thuật, 30 câu thiếu lời giải nguồn khớp, ảnh/bảng gốc còn cần PDF giữ nguyên từ v13.7.

---

# v13.8 — Giao diện học tập và lưu học liệu một lần

- Giữ nguyên toàn bộ dữ liệu v13.7 (534 nguồn, gói cá nhân **CFA_2026_Private_Study_Data_v137.json.gz**, cùng SHA-256). Không cần tải lại gói nếu đã có.
- Chọn gói cá nhân một lần; website xác thực và lưu bản nén trong IndexedDB của trình duyệt, tự mở khi quay lại. Không truyền gói lên mạng. Lưu thành công hiển thị “Học liệu đã lưu trên thiết bị”.
- Nếu dùng trình duyệt ẩn danh, thiếu dung lượng, xóa dữ liệu trang, đổi tên miền/thiết bị, có thể cần nạp lại. Tùy chọn xóa gói trong Quản lý học liệu không xóa tiến độ. PDF gốc vẫn là tùy chọn đối chiếu.
- Màn hình Học liệu & luyện đề đưa nút học lên đầu, thu gọn thông tin quản trị PDF và kiểm định. Không thêm nội dung học thuật trong bản sửa giao diện này; các giới hạn v13.7 vẫn còn.

# v13.7 — SAPP Revision Mindmaps và Kaplan QuickSheet

- Cập nhật 64 file website, giữ nguyên tên file. Nạp gói cá nhân `CFA_2026_Private_Study_Data_v137.json.gz` thay v13.6 (SHA-256 `f3ac6bc059b26bf7e1daa0d4544b9bb7b5e612555fee82b132523111ba183ad6`); không upload gói cá nhân lên GitHub công khai.
- Mở lại, đối chiếu SHA-256 và dùng trực tiếp 10 SAPP Revision Mindmaps và Kaplan QuickSheet 2026 (6 trang). Bổ sung 109 nhóm diễn giải song ngữ từ các nhánh Mindmap (86 nhóm ngoài Ethics, 23 tiểu chuẩn Ethics trong LM3), cùng 14 thẻ chọn lọc từ QuickSheet, có mã nguồn/trang. Nhánh Quant M8+9 và FSA M4+5 được giữ gộp như sơ đồ. Đây là nội dung diễn giải ôn tập, không phải câu hỏi mới. Ethics Mindmap không bao phủ 4 module Ethics ngoài LM3. Các công thức/hình nguồn có thể không đọc được từ lớp chữ.
- Bổ sung ảnh PNG nguyên trang cho toàn bộ 10 mindmap và 6 trang QuickSheet, tổng 194 ảnh trong gói cá nhân (thêm 16). Khi mở các nguồn này, trình đọc ưu tiên ảnh gốc, có tùy chọn phóng to và cuộn, văn bản trích xuất nằm trong mục mở rộng. Các ảnh khác giữ nguyên. Không thay đổi bất kỳ đoạn câu hỏi/lời giải nào, không thêm câu tự sáng tác. Bảo toàn 534 tài liệu, 22.712 trang, 14.643 bản ghi định vị; 30 vị trí thiếu lời giải khớp nguồn vẫn giữ nguyên trạng.
- Bản tổng kết môn và module hiển thị nhóm Mindmap tương ứng, thẻ QuickSheet ở tổng kết môn. Không tuyên bố tất cả các nhánh chi tiết đã được dịch từng chữ, không coi mọi cách diễn đạt trong nguồn bổ trợ là chuẩn độc lập. PDF gốc là tài liệu đối chiếu cuối cùng.
- Chưa hoàn thành toàn bộ nội dung song ngữ 44 PDF học liệu: cần tiếp tục đối chiếu SAPP Slides, SchweserNotes, Prerequisite, Wiley historical và các chi tiết CFAI chưa diễn giải. Các bảng biểu ngoài ảnh tích hợp vẫn mở bằng PDF nguyên bản. Không tuyên bố đã nghiệm thu học thuật toàn diện.

- Bổ sung thêm trong cùng v13.7: mở lại và kiểm tra SHA-256 cả 3 PDF Prerequisite Reading 2024. Thêm 22 thẻ song ngữ diễn giải các điểm chính từ trang Summary (Quant 6, Economics 7, FSA 9; phụ lục Quant chưa diễn giải). Nguồn lịch sử được phân biệt với 2026; không xác nhận dịch hết 890 trang. Tổng 145 nhóm/thẻ song ngữ bổ sung (109 + 14 + 22).
- Kiểm thử Chromium cô lập: tổng kết môn, module gộp, 23 Ethics, gói cá nhân và phóng to ảnh Mindmap/QuickSheet, luyện QBank cũ đạt. Kiểm thử website đã triển khai thật chưa thực hiện.

---

# v13.6 — Hoàn tất tách câu Mock và khôi phục trang hình ảnh gốc

## Cách sử dụng
1. Giải nén `CFA_2026_StudyHub_GitHub_v136_64files.zip`, thay 64 file trên GitHub Pages bằng phiên bản mới.
2. Nạp `CFA_2026_Private_Study_Data_v136.json.gz` qua **Tài liệu gốc & bài tập → Thư viện nội dung gốc → Nạp học liệu**. Không upload gói cá nhân lên GitHub công khai. Nếu trình duyệt không hỗ trợ gzip, giải nén thành JSON trên thiết bị rồi nạp. Gói được giữ trong bộ nhớ phiên; tải lại trang phải nạp lại.
3. Đọc câu hỏi tiếng Anh đã tách, mở lời giải nguyên văn, tự chấm. Bấm **Ảnh trang gốc** nếu có để kiểm tra bảng/hình/công thức; ảnh nguyên trang có thể chứa câu lân cận hoặc lời giải. Với các trang khác, mở PDF gốc qua thư mục PDF cục bộ. Trang không có lớp chữ được hiển thị ảnh hoặc thông báo đã kiểm tra trắng.

## Kiểm định và giới hạn
- Toàn bộ 534 PDF, 22.712 vị trí trang và 45.794.364 ký tự lớp chữ v13.5 được giữ nguyên. Không thêm câu tự sáng tác. 14.643 bản ghi định vị và các nội dung học song ngữ đã có được giữ nguyên.
- Đã sửa 44 đoạn đề và 55 đoạn lời giải Mock còn đọc ở chế độ nguyên trang bằng cách đối chiếu tiêu đề/số câu, ngữ cảnh nguồn và ranh giới văn bản. Kết quả: 7.020/7.020 vị trí câu Mock tách riêng; 7.014/7.020 vị trí lời giải có đoạn tách. QBank vẫn 4.627/4.627 đề và 4.603/4.627 lời giải. Đây là số vị trí nguồn, không phải số câu độc lập sau khi loại trùng. Tách đoạn không bảo đảm khôi phục hoàn hảo bảng/hình/công thức.
- 144 trang có lớp chữ rỗng: 66 trang raster trắng hoàn toàn; 78 trang có nội dung hình ảnh/đồ họa được khôi phục bằng ảnh nguyên trang. Tổng 178 ảnh PNG nguyên trang từ PDF gốc (144 dpi), gồm 78 trang rỗng lớp chữ và 100 trang liên quan Mock cần kiểm tra trực quan. Đã mở lại và kiểm tra SHA-256 94 PDF ở lượt kiểm tra ảnh. Không OCR. Các hình/bảng ở trang khác vẫn phải đối chiếu PDF nguyên bản cục bộ.
- 24 lời giải Bonus Monetary Policy không có trong file đáp án (SRC-0343 chỉ có câu 25). Rà soát lại các nguồn khác không tìm được bản trùng nguyên văn để thay thế đáng tin cậy. 6 lời giải Mock không khớp như v13.4. 30 vị trí chưa có lời giải nguồn khớp, không suy diễn.
- Gói dữ liệu cá nhân SHA-256: `ea4e5f7e4f791d23c27b2e431ebaca312a8e75e97c887cfff6fb4daf8be8da05` (44.339.848 byte). Không chứa nội dung mới ngoài tài liệu người dùng cung cấp. Gói website không chứa bản sao nguyên văn của PDF nguồn.
- Chromium DOM kiểm thử cô lập: nạp gói, luyện QBank, lọc nguồn, liên kết recap, đoạn Mock đã sửa, giải mã ảnh nguyên trang, hiển thị trang chỉ có ảnh và trang trắng đều đạt. Kiểm thử không tương đương triển khai GitHub Pages thật; không xác nhận giao diện mọi thiết bị.
- **Chưa hoàn thành tuyệt đối yêu cầu học song ngữ toàn bộ nguồn:** nguyên văn có thể đọc/tìm theo nguồn, nhưng chưa dịch đầy đủ mọi nội dung lý thuyết, lời giải, bảng biểu và chưa nghiệm thu học thuật từng dòng. Ảnh nguyên trang chỉ có cho 178 trang trong gói; PDF gốc vẫn cần thiết cho các trang còn lại có nội dung trực quan. Không tạo thêm học liệu ngoài nguồn.

---

# v13.5 — Học trực tiếp từ nguyên văn nguồn (private study companion)

## Cách sử dụng
1. Giải nén `CFA_2026_StudyHub_GitHub_v135_64files.zip` và thay thế các file website cũ trên GitHub Pages bằng 64 file của bản này.
2. Giữ riêng `CFA_2026_Private_Study_Data_v135.json.gz` trên thiết bị. **Không upload gói học liệu cá nhân lên GitHub công khai.**
3. Trên website mở **Tài liệu gốc & bài tập → Thư viện nội dung gốc → Nạp học liệu** rồi chọn file `.json.gz` (nếu trình duyệt không hỗ trợ DecompressionStream, giải nén thành `.json` rồi chọn file JSON). Dữ liệu chỉ nạp trong bộ nhớ phiên, không gửi lên máy chủ. Tải lại trang thì cần chọn lại.
4. Chọn **Luyện câu này tại web** để đọc đề tiếng Anh, chọn A/B/C, mở lời giải nguồn và tự chấm, lưu câu để ôn. Dữ liệu lựa chọn và tự chấm lưu cục bộ khi trình duyệt cho phép. Không tự suy diễn đáp án khi nguồn không ghi rõ.
5. Để xem đồ thị, bảng, công thức, trang scan hoặc bố cục chính xác: giải nén các PDF gốc vào một thư mục cha, dùng **Chọn cả thư mục đã giải nén** hoặc chọn PDF đúng nguồn khi trình đọc yêu cầu; mở PDF nguyên bản tại trang đã định vị. Native PDF viewer phụ thuộc trình duyệt, có nút mở tab riêng.

## Phạm vi thực hiện
- Reopened and SHA-256-verified all 534 original PDFs against the existing catalog in this pass. Extracted every physical page's text layer using pdftotext -layout: **22,712 page positions**, 22,568 nonempty extracted text pages, 144 empty text pages, 45,794,364 extracted characters; 10,607 pages in 44 theory/revision documents. No OCR, no invented text or questions. Source files preserve their original language, order, publisher wording and source date.
- Private gzip package SHA-256: `893095561c5118232d1b8bb37629b93137b8fdd93b53880d3a84dae75ec77eac`. File is separate from the public website ZIP. Every text page is linked by source ID and physical page. Full-text search across all sources; results capped at 150 pages per query. Source text may include running headers, footers, OCR defects already in source, soft hyphens or misordered columns. Original PDF is authoritative for figures, tables, math layout and typographic answer markers.
- Exact-number anchored question text segments: 4,627/4,627 unique QBank question positions, 4,603/4,627 matched solution segments; 6,976/7,020 Mock question positions and 6,959/7,020 Mock solution positions. 44 Mock questions and 55 of the 7,014 matched Mock solutions remain full-page reading rather than isolated question text. Counts are positions in supplied files, not deduplicated academic questions. Segment boundaries follow actual numbered/publisher headings and reviewed page locators; not independently audited line by line. All remaining curriculum/exercise locators open source page text. Page-context mode may show neighboring questions or solutions on the same page; not a clean exam simulation.
- Correction of v13.3–13.4: `SRC-0283:3` (Kaplan Statistical Measures) **has** its original solution in `SRC-0273` PDF p.1–2. A typesetting line interrupts Question #3 heading, but publisher Question ID 1572756 and explanation match. QBank matched solutions now 4,603; remaining 24 missing solutions in Bonus Monetary Policy. Six Mock mismatches remain (see v13.4). Total 30 unresolved source solutions, no invented answers.
- All prior bilingual recap and lesson content retained, as well as 14,643 item IDs and 93 module outlines. Original source reader is not a full Vietnamese translation of all 22,712 pages. No automatic correctness inference or academic acceptance claimed. Existing authored content retains its existing labels.
- Technical fixes: moved v13.4 page-jump/filter handler inside study.js closure; added local-only reading/quiz dialog with text search, page controls, native PDF attachment and manual self-grading. Chromium actual DOM integration tests (assets injected in isolated browser, no network) passed package import, recovered QBank question and solution, source-filter, recap reader, source search, page reading and self-grade. Environment blocks direct URL navigation, so public deployment and actual mobile/browser PDF rendering not verified. No deployment performed.
- Completion boundary: all source text layers are now accessible in the website via private package, with original PDFs accessible locally for missing visual content. Full bilingual integration of all details, perfect table/figure reflow, all Mock question isolation, and academic line-by-line validation are **not yet complete**. No outside learning content created.

---

# v13.4 — Complete source-file inventory and Mock question navigation

- Reopened all 146 PDFs outside the two Question Bank archives in this pass; each SHA-256 matches its source record. Combined with the 388 PDFs reopened in v13.3: 534/534 file-level scans. Actual page counts for the reopened sources include blank separator pages; source text-layer presence is not academic validation.
- Mock collection: all 102 exam/solution PDFs (including 6 in bonus RAR) accounted for in 52 sessions. The remaining 5 PDFs in the Mock archive are Wiley 2020 study guides, classified as theory in the reading index. 7,020/7,020 question positions located; 7,014/7,020 aligned with solutions. Historical exams may duplicate questions or use superseded syllabi. Source matching used question number and normalized initial stem or publisher Question ID, ordered anchors, and manual review of exceptional layouts. Some previous matches retained; no claim of independent solution validation.
- Manual corrections: FinQuiz AM printed 38 twice (sequence position 28 retained with printedNumber 38); FinQuiz PM questions 55–58 map to solution numbers 57–60. The 6 unresolved mock answers: SRC-0025 #32,59,60 (different stems/number shift); SRC-0086 #105 (most vs least likely); SRC-0115 #18 and SRC-0112 #18 (least vs most correct). No substitute answers created. Existing 25 QBank missing solutions retained.
- Added 2,223 source question locators; 14,643 total locator records (not a unique-question count). 194/194 QBank question PDFs remain indexed, 4,627 question positions and 4,602 matched answers. No original question prose/answer prose or source PDFs republished.
- Added reading index for 44 theory/revision documents, with 3,156 source bookmark/title-slide/navigation entries; 93/93 SAPP modules mapped to actual title slides and page ranges, plus 10/10 single-page revision mindmaps. SAPP Alternative Investments has nonsequential module order; Ethics module-list printed numbers differ from actual title-slide positions; use actual PDF title slide pages. Native bookmarks are source metadata, not independent verification of all headings. Historical prerequisite and Wiley study guides marked as such. The PDF navigator supports any physical page (including tables, diagrams, and blank separator pages), direct per-file question filtering and module-level slide/mindmap links. Source files stay on the learner's device; choose the extracted directory. Page-jump input retains requested page during selection.
- Verification: all 63 original file names retained; no duplicate item IDs; all 14,643 item source and answer references resolve, all non-null page locations within physical page count; all JS passed node --check. Desktop Chromium navigation smoke attempt blocked by environment (ERR_BLOCKED_BY_ADMINISTRATOR at local server); no browser pass claimed.
- Completion boundary: all PDF files accounted for and accessible through the local PDF navigation, and all identified QBank and Mock question positions located. **Not full integration or academic acceptance**: no full transcription of question, answer, figure, or table content; still need detailed bilingual content reconciliation from 44 theory/revision PDFs and original lesson text. 31 question positions across QBank/Mock have missing or mismatching source solutions. No newly authored learning content or questions. Next: prioritize detailed source-to-website theory, formula, example and table reconciliation; no additional original content.

---

# v13.3 — Source bank coverage pass

- Bảo toàn toàn bộ nội dung v13.2 (93 module/365 LOS/10 môn); không tạo câu hỏi mới, không chép PDF lên GitHub.
- Đã mở lại và kiểm tra SHA-256 465/534 PDF, gồm toàn bộ 388 PDF Question Bank và 77 PDF thuộc archive Mock. Quét lớp chữ và số trang; không phải kiểm định từng lời giải.
- Kaplan QBank: 101/101 file đề, 2.693 câu, 2.692 cặp đề–lời giải định vị được bằng số câu và Question ID. SRC-0283 câu 3 không thấy trong SRC-0273.
- Bonus QBank: 93/93 file đề, 1.934 câu, 1.910 cặp định vị bằng số câu và phần đầu đề tiếng Anh. SRC-0351 câu 1–24 không có trong SRC-0343 (file chỉ chứa câu 25). Không sáng tác lời giải thay thế.
- Mock lịch sử: 34 cặp file đề–lời giải, 4.797 định vị, 4.769 có trang lời giải đã ghép. 28 định vị chưa ghép chắc chắn lời giải; 63 câu chưa định vị trong 21 session CFAI/FinQuiz đã quét. Các đề cũ không được coi là khớp chương trình 2026.
- Tổng bản ghi định vị: 12.420 (thêm 6.935, có thể có nội dung trùng nguồn); không đồng nghĩa số câu hỏi độc lập hoặc câu hỏi tương tác.
- Giao diện Tài liệu gốc: chọn cả thư mục PDF đã giải nén (trình duyệt hỗ trợ webkitdirectory), tìm bằng ID nguồn; trạng thái thiếu lời giải hiển thị riêng; file đã quét có số trang. PDF nguyên bản vẫn mở cục bộ, không tải lên GitHub. Tính năng chọn thư mục phụ thuộc trình duyệt; nếu không hỗ trợ, dùng nút chọn nhiều PDF.
- Chưa hoàn thành: 30 PDF trong nhóm Mock chưa quét lại (gồm 6 PDF RAR và 24 PDF ZIP); chưa đối chiếu toàn bộ mock và 39 PDF học liệu lý thuyết/giáo trình trong các archive khác. Quét văn bản không thay thế rà bảng biểu/hình, nội dung học thuật và kiểm thử trình duyệt. 25 câu QBank thiếu lời giải ở nguồn đi kèm cần file bổ sung nếu muốn đáp án gốc. Các bản ghi cũ và module recap không bị xóa.
- Checkpoint: tiếp tục mock còn thiếu, xác minh câu chưa ghép; hoàn thiện đối chiếu nội dung học liệu lý thuyết từ mọi nguồn.

---

# v13.2 — 93/93 CFAI section-level mapping (2026-11-26)

- Original V10 SHA-256 matches catalog. Ethics PDF pp17–301. Counts (LM, bilingual groups, examples, exhibits, distinct end-practice, in-text MCQ, named application cases): [(1, 9, 6, 4, 12, 15, 0), (2, 9, 0, 0, 10, 0, 0), (3, 52, 210, 3, 39, 0, 0), (4, 5, 0, 0, 11, 0, 0), (5, 8, 0, 0, 0, 37, 37)]. Checked all 210 LM3 example headings and Comment locations; 37 named LM5 case and Analysis pages; added 15 LM1 in-text question locators. No authored questions. Revised I(E), V(B), VI(A) emphasized.
- Technical fix: source example panel supports both historical start/end and newer page/title schema; Ethics substandard and Comment location displayed, named case index added. No live browser test yet.
- All 93 module-level source maps now present; 93/93 Module Reviews, 365/365 legacy LOS Reviews and 10/10 Master Reviews retained. 5485 locator records (not unique questions; historical aliases intentionally retained). 72 unique Ethics end-practice questions in two old ID sets, counted once in audit. Exhaustive academic acceptance 0/93: not a claim that all curriculum content has been digitized or independently validated.
- This turn completed Derivatives LM4–10, Alternative Investments LM1–7, Portfolio Management LM1–6, and Ethics LM1–5. Next: reconcile all legacy lesson content and actual source coverage, then secondary notes/slides/mindmaps/prerequisites and question/mock collections; verify every source/answer pair and browser behavior. No full source PDF or question text redistributed.
- 63 flat files. Upload the contents of this latest ZIP to GitHub Pages; do not merge multiple old versions.

# v13.2 PM — CFAI Portfolio Management LM1–6 (2026-11-26)

- Original V9 SHA-256 matches catalog. PDF pp13–300. Counts (LM, bilingual groups, examples, exhibits, distinct end-practice items, inline MCQ, other inline): [(1, 12, 8, 26, 30, 0, 25), (2, 11, 11, 13, 41, 0, 24), (3, 9, 0, 22, 15, 1, 0), (4, 12, 12, 16, 19, 11, 6), (5, 13, 16, 2, 15, 12, 2), (6, 11, 5, 1, 19, 19, 3)]. Existing example cards retained; in-text exercises indexed only if identifiable with solution. Historical data remain historical. Source notes: p109 M² reporting, p196 IPS mismatch, p239 Exhibit reference, p288 covariance notation.
- Two pre-existing ID sets for the 139 PM end-practice items share identical question/answer pages. Retained to preserve links; distinct end-practice count 139, not 278. Total locator records 5470 are not a unique-question count. No authored questions.
- Totals 93/93 Module Reviews, 365/365 legacy LOS Reviews, 10/10 Master Reviews; section-level mapping 88/93, PM 6/6. Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full digitization, detailed legacy content review, secondary sources and browser testing pending. Next: Ethics LM1.

# v13.2 extended — CFAI Alternative Investments LM1–7 (2026-11-26)

- Original CFAI V8 SHA-256 matches catalog. All seven modules (PDF pp11–220). Counts (LM, bilingual groups, numbered examples, Exhibit locators, end-practice locators checked, inline MCQ, other inline, existing inline checked, new inline): [(1, 12, 6, 11, 8, 9, 10, 19, 0), (2, 10, 7, 2, 7, 9, 22, 22, 9), (3, 10, 4, 7, 9, 6, 12, 18, 0), (4, 11, 4, 11, 13, 17, 7, 24, 0), (5, 9, 1, 10, 9, 8, 10, 18, 0), (6, 11, 4, 8, 7, 14, 3, 17, 0), (7, 12, 7, 11, 12, 14, 9, 23, 0)]. Existing example cards retained. Nine numbered example exercises in LM2 indexed; no newly authored questions. Source notes: p56 HWM equation, p94 correlation range, p158 fee arithmetic, historical cases and digital product/regulatory descriptions.
- Totals: 93/93 Module Reviews, 365/365 legacy LOS Reviews, 10/10 Master Reviews, 5367 source locators; section-level mapping 82/93 (Derivatives 10/10; Alternative Investments 7/7). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Portfolio Management LM1.

# v13.2 — CFAI Derivatives LM4–10 section-level coverage (2026-11-26)

- Original CFAI V7 SHA-256 matches catalog. All seven remaining modules (PDF pp85–246). Counts (LM, bilingual groups, numbered examples, Exhibit locators, end-practice locators checked, inline MCQ, other inline, existing inline checked, new inline): [(4, 8, 8, 10, 0, 4, 10, 9, 5), (5, 9, 8, 9, 6, 3, 11, 10, 4), (6, 7, 5, 6, 4, 3, 11, 10, 4), (7, 7, 4, 4, 6, 3, 11, 10, 4), (8, 8, 4, 9, 9, 3, 15, 12, 6), (9, 6, 4, 9, 6, 3, 9, 12, 0), (10, 7, 2, 3, 4, 5, 10, 15, 0)]. Existing example cards retained. LM4 missing Question Set A #5 added; original inline count corrected from 9 to 10. Added missing self-assessment locators; preserved prior IDs. Source notes: p121 FX position sign, p144 MTM signs, p169 settlement timing, p190 broad put bound, p219 credit premium interpretation, p234 rate typo. No newly authored questions or scenarios.
- Totals: 93/93 Module Reviews, 365/365 legacy LOS Reviews, 10/10 Master Reviews, 5358 source locators; section-level mapping 75/93 (Derivatives 10/10). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Alternative Investments LM1.

# v13.1 — CFAI Derivatives LM1–3 section-level coverage (2026-11-26)

- Original CFAI V7 SHA-256 matches catalog. LM1 pp11–30; LM2 pp31–60; LM3 pp61–84 (blank separator pages included). Counts (LM, bilingual groups, numbered examples, Exhibit locators, additional example cards, end-practice locators checked, inline MCQ, other inline): [(1, 10, 0, 7, 2, 5, 4, 15), (2, 11, 5, 13, 2, 4, 4, 20), (3, 10, 6, 4, 1, 4, 2, 14)]. Source notes: historical lithium specifications, compressed futures margin illustration, p79 initial cash outlay wording versus required futures margin. No newly authored questions or scenarios.
- Totals: 93/93 Module Reviews, 365/365 legacy LOS Reviews, 10/10 Master Reviews, 5335 source locators; section-level mapping 68/93 (Derivatives 3/10). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Derivatives LM4 Arbitrage, Replication, and the Cost of Carry.

# v13.0 — CFAI Fixed Income LM16–19 section-level coverage (2026-11-26)

- Original CFAI V6 SHA-256 matches catalog. LM16 pp421–452; LM17 pp453–474; LM18 pp475–506; LM19 pp507–546 (blank separator pages included). Counts (LM, bilingual groups, numbered examples, Exhibit locators, additional example cards, end-practice locators checked, inline MCQ, other inline): [(16, 12, 7, 6, 3, 9, 7, 12), (17, 8, 2, 9, 1, 8, 6, 6), (18, 10, 6, 9, 1, 12, 13, 15), (19, 12, 5, 8, 2, 13, 16, 8)]. Source notes: retained Bowstream margin, CLT maturity illustration, CFP currency, Al-Shims average and CMBS coupon discrepancies; added warehouse mixed currency note pp534–535. Unnumbered examples retained as examples, not fabricated questions. No newly authored questions or scenarios.
- Totals: 93/93 Module Reviews, 365/365 legacy LOS Reviews, 10/10 Master Reviews, 5276 source locators; section-level mapping 65/93 (FI 19/19). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Derivatives LM1.

# v12.9 — CFAI Fixed Income LM13–15 section-level coverage (2026-11-26)

- Original CFAI V6 SHA-256 matches catalog. LM13 pp331–354; LM14 pp355–392; LM15 pp393–420 (blank separator pages included). Counts (LM, bilingual groups, numbered examples, Exhibit locators, additional example cards, end-practice locators checked, inline MCQ, other inline): [(13, 10, 4, 7, 3, 8, 4, 20), (14, 12, 8, 11, 2, 6, 14, 8), (15, 10, 13, 7, 2, 6, 10, 4)]. Source notes: negative price-change sign p333; empirical model wording p350; retained existing notes on repricing, portfolio typo, VIVU spread wording, Romania bid/offer and GDP growth formula. Unnumbered examples retained as examples, not fabricated questions. No newly authored questions or scenarios.
- Totals: 93/93 Module Reviews, 365/365 legacy LOS Reviews, 10/10 Master Reviews, 5193 source locators; section-level mapping 61/93 (FI 15/19). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Fixed Income LM16 Credit Analysis for Corporate Issuers.

# v12.8 — CFAI Fixed Income LM10–12 section-level coverage (2026-11-26)

- Original CFAI V6 SHA-256 matches catalog. LM10 pp249–276; LM11 pp277–306; LM12 pp307–330. Counts (LM, bilingual groups, numbered examples, Exhibit locators, additional example cards, end-practice locators checked, inline MCQ, other inline): [(10, 10, 5, 4, 3, 8, 14, 12), (11, 10, 2, 6, 1, 7, 12, 10), (12, 11, 2, 7, 2, 9, 7, 19)]. Source notes: zero-coupon duration wording p253; PRICE yield input p321. Example 1 LM12 shared worked discussion retained as an example. No newly authored questions or scenarios.
- Totals: 93/93 Module Reviews, 365/365 legacy LOS Reviews, 10/10 Master Reviews, 5133 source locators; section-level mapping 58/93 (FI 12/19). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Fixed Income LM13 Curve-Based and Empirical Fixed-Income Risk Measures.

# v12.7 — CFAI Fixed Income LM7–9 section-level coverage (2026-11-26)

- Original CFAI V6 SHA-256 matches catalog. LM7 pp167–196; LM8 pp197–220; LM9 pp221–248. Counts (LM, bilingual groups, numbered examples, Exhibit locators, additional example cards, end-practice locators checked, inline MCQ, other inline): [(7, 13, 9, 8, 4, 5, 7, 13), (8, 10, 4, 3, 3, 7, 8, 10), (9, 10, 4, 9, 4, 9, 0, 29)]. Source notes: negative YTM sign, G-spread units, call option adjustment and call price, money-market day basis and FRN reset wording, forward equation and printed factors. No newly authored questions or scenarios.
- Totals: 93/93 Module Reviews, 365/365 legacy LOS Reviews, 10/10 Master Reviews, 5059 source locators; section-level mapping 55/93 (FI 9/19). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Fixed Income LM10 Interest Rate Risk and Return.

# v12.6 — CFAI Fixed Income LM4–6 section-level coverage (2026-11-26)

- Original CFAI V6 SHA-256 matches catalog. LM4 pp89–116; LM5 pp117–136; LM6 pp137–166. Counts (LM, bilingual groups, numbered examples, Exhibit locators, selected example cards, end-practice locators checked, inline MCQ, other inline): [(4, 14, 0, 10, 3, 6, 18, 6), (5, 10, 0, 2, 2, 6, 10, 6), (6, 12, 7, 11, 5, 7, 8, 11)]. Source notes: repo party inconsistency p91; matrix average and spreadsheet frequency discrepancies pp160–161. No newly authored questions or scenarios.
- Totals: 93/93 Module Reviews, 365/365 legacy LOS Reviews, 10/10 Master Reviews, 4992 source locators; section-level mapping 52/93 (FI 6/19). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Fixed Income LM7 Yield and Yield Spread Measures for Fixed-Rate Bonds.

# v12.5 — CFAI Fixed Income LM1–3 section-level coverage (2026-11-26)

- Original CFAI V6 SHA-256 matches catalog. LM1 pp13–32; LM2 pp33–64; LM3 pp65–88 (64 and 88 are blank separators). Counts (LM, bilingual groups, numbered examples, Exhibit locators, selected additional example cards, end-practice locators checked, inline MCQ, other inline): [(1, 13, 0, 10, 4, 5, 4, 12), (2, 15, 3, 12, 4, 5, 11, 10), (3, 12, 4, 6, 3, 5, 15, 5)]. Source notes: p14 coupon arithmetic, p45 rounded CPI, LM2 combined source outcomes, p87 BBB− boundary; existing spread-tier overlap and working-capital answer notes retained. Numbered narrative examples are not invented questions. Historical case data retained; no newly authored questions.
- Totals: 93/93 Module Reviews, 365/365 legacy LOS Reviews (not guaranteed one-to-one source LOS), 10/10 Master Reviews, 4933 source locators; section-level mapping 49/93 (Quant 11/11, Econ 8/8, CI 7/7, FSA 12/12, Equity 8/8, FI 3/19). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Fixed Income LM4 Fixed-Income Markets for Corporate Issuers.

# v12.4 — CFAI Equity LM7–8 section-level coverage (2026-11-26)

- Original CFAI V5 SHA-256 matches catalog. LM7 pp295–344; LM8 pp345–398. Counts (LM, bilingual groups, numbered examples, Exhibit locators, selected supplementary example cards, end-practice locators checked, inline MCQ, other inline): [(7, 20, 4, 21, 6, 8, 23, 17), (8, 23, 21, 12, 9, 36, 8, 24)]. Includes self-assessment, Question Sets, Knowledge Check and numbered example subquestions. Example 16 worked calculation is indexed as example, not a separate question. Historical data retained; no new questions or scenarios. Source notes: rounded segment growth, percentage-point margin change, conditional retraction valuation, Cameco debt assumption.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4876 source locators; section-level mapping 46/93 (Quant 11/11, Econ 8/8, CI 7/7, FSA 12/12, Equity 8/8). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Fixed Income LM1 Fixed-Income Instrument Features.

# v12.3 — CFAI Equity LM5–6 section-level coverage (2026-11-26)

- Original CFAI V5 SHA-256 matches catalog. LM5 pp207–254; LM6 pp255–294. Counts (LM, bilingual groups, numbered examples, Exhibit locators, selected supplementary example cards, end-practice locators checked, inline MCQ, other inline): [(5, 17, 3, 6, 8, 6, 27, 4), (6, 16, 0, 6, 6, 8, 17, 12)]. Includes self-assessment and Question Sets; numbered Example 1 and 2 discussions not treated as invented questions. Source notes retain decimal separator, DFL rounding, ICB acronym and supplier/customer wording discrepancy. Historical company and fictional case data retained; no new questions or scenarios.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4804 source locators; section-level mapping 44/93 (Quant 11/11, Econ 8/8, CI 7/7, FSA 12/12, Equity 6/8). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Equity LM7 Company Analysis: Forecasting and LM8 Equity Valuation: Concepts and Basic Tools.

# v12.2 — CFAI Equity LM3–4 section-level coverage (2026-11-26)

- Original CFAI V5 SHA-256 matches catalog. LM3 pp133–168; LM4 pp169–206. Counts (LM, bilingual groups, numbered examples, Exhibit locators, selected example cards, end-practice locators checked, inline MCQ, written inline): [(3, 18, 6, 4, 4, 26, 6, 3), (4, 18, 0, 20, 8, 24, 0, 0)]. Source notes: Example 1 is discussion not a standalone question; Tesla historical case; Level II ADR narrative/table discrepancy; Maker/Marker name discrepancy. No newly authored questions or scenarios.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4744 source locators; section-level mapping 42/93 (Quant 11/11, Econ 8/8, CI 7/7, FSA 12/12, Equity 4/8). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Equity LM5 Company Analysis: Past and Present.

# v12.1 — CFAI Equity LM1–2 section-level coverage (2026-11-26)

- Original CFAI V5 SHA-256 matches catalog. LM1 pp13–90; LM2 pp91–132. Counts (LM, bilingual groups, numbered examples, Exhibit locators, selected example cards, end-practice locators checked, written/calculation inline): [(1, 26, 30, 2, 7, 37, 51), (2, 17, 0, 11, 6, 34, 0)]. Source notes: IOC terminology; divisor precision and rounded credit shares; historical index composition. No newly authored questions or scenarios.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4735 source locators; section-level mapping 40/93 (Quant 11/11, Econ 8/8, CI 7/7, FSA 12/12, Equity 2/8). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Equity LM3 Market Efficiency.

# v12.0 — CFAI FSA LM10–12 section-level coverage (2026-11-26)

- Original CFAI V4 SHA-256 matches catalog. LM10 pp323–392; LM11 pp393–458; LM12 pp459–516. Counts (LM, bilingual groups, numbered examples, Exhibit locators, additional selected example cards, end-practice locators checked, inline MCQ, other inline): [(10, 21, 6, 26, 6, 27, 0, 18), (11, 18, 16, 36, 5, 17, 5, 12), (12, 18, 10, 34, 5, 21, 5, 13)]. Source notes: PACCAR segment and profit measure distinction; Exhibit 31 rounding; modeling forecasts retained in original historical periods and rounded values distinguished from exact calculations. Numbered exercises with verified solution-page locators only; unnumbered cases indexed by example, not invented question IDs. No newly authored questions or scenarios.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4684 source locators; section-level mapping 38/93 (Quant 11/11, Econ 8/8, CI 7/7, FSA 12/12). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: Equity Investments LM1 Market Organization and Structure.

# v11.9 — CFAI FSA LM8–9 section-level coverage (2026-11-26)

- Original CFAI V4 SHA-256 matches catalog. LM8 pp253–288; LM9 pp289–322. Counts (LM, bilingual groups, numbered examples, Exhibit locators, additional example cards, end-practice locators checked, inline MCQ, other inline): [(8, 14, 6, 9, 8, 15, 2, 11), (9, 12, 6, 25, 10, 8, 25, 8)]. Source notes: Proton year reference and preexisting principal typo, Walmart cash-tax proxy and period label, rounding in country B deferral. Historical examples and curriculum accounting conventions; no invented questions or examples.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4631 source locators; section-level mapping 35/93 (Quant 11/11, Econ 8/8, CI 7/7, FSA 9/12). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: FSA LM10 Financial Reporting Quality.

# v11.8 — CFAI FSA LM6–7 section-level coverage (2026-11-26)

- Original CFAI V4 SHA-256 matches catalog. LM6 pp185–220; LM7 pp221–252. Counts (LM, bilingual groups, numbered examples, Exhibit locators, additional example cards, end-practice locators checked, inline MCQ, other inline): [(6, 12, 4, 6, 8, 37, 0, 13), (7, 14, 6, 6, 6, 23, 1, 15)]. Source notes: Volvo allowance movement assumption, Ferrari IPO arithmetic, Exhibit 6 reference and Verizon currency typo. No invented questions or examples.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4585 source locators; section-level mapping 33/93 (Quant 11/11, Econ 8/8, CI 7/7, FSA 7/12). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: FSA LM8 Topics in Long-Term Liabilities and Equity.

# v11.7 — CFAI FSA LM4–5 section-level coverage (2026-11-26)

- Original CFAI V4 SHA-256 matches catalog. LM4 pp135–166; LM5 pp167–184. Counts (LM, bilingual groups, numbered examples, Exhibit locators, selected additional example cards, end-practice locators checked, inline MCQ, other inline): [(4, 16, 8, 34, 10, 11, 11, 0), (5, 12, 3, 11, 3, 4, 0, 8)]. Example 2 LM5 item 1 introduces data, not a standalone question. Source notes: Mountain date typo; Acme financing subtotal discrepancy; common-size denominator; LOS mapping. No invented questions or examples.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4556 source locators; section-level mapping 31/93 (Quant 11/11, Econ 8/8, CI 7/7, FSA 5/12). Exhaustive academic acceptance 0/93.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full question/table digitization, old detailed lesson verification, secondary sources, browser/live testing pending. Next: FSA LM6 Analysis of Inventories.

# v11.6 — CFAI FSA LM1–3 section-level coverage (2026-11-26)

- Original CFAI V4 SHA-256 matches catalog. LM1 PDF pp15–48, LM2 pp49–102, LM3 pp103–134. Counts (LM, bilingual groups, numbered examples, Exhibit locators, added source example cards, end-practice locators checked, inline MCQ, other inline): [(1, 16, 0, 6, 3, 16, 1, 0), (2, 21, 15, 20, 8, 14, 6, 20), (3, 13, 1, 13, 5, 15, 1, 6)]. Skipped uncertain locator mappings: []. Inline entries are source locators, not digitized questions. Historical examples, not contemporary accounting or company updates. Source notes preserve discrepancies.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4537 source locators; section-level mapping 29/93 (Quant 11/11, Econ 8/8, CI 7/7, FSA 3/12). Exhaustive academic acceptance 0/93. No newly invented questions or cases.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full table/figure and question digitization, old detailed lesson verification, Kaplan/SAPP/other sources, browser and live GitHub Pages testing remain pending. Next: FSA LM4 Analyzing Statements of Cash Flows I.

# v11.5 — CFAI Corporate Issuers LM4–7 section-level coverage (2026-11-26)

- CFAI V3 original SHA-256 matches catalog. LM4 pp105–142, LM5 pp143–180, LM6 pp181–219, LM7 pp221–250. Counts (LM, bilingual groups, numbered examples, Exhibit locators, added example cards, end practice checked, inline MCQ, other inline): [(4, 15, 5, 13, 3, 5, 17, 17), (5, 13, 9, 5, 5, 5, 8, 23), (6, 11, 5, 7, 5, 5, 17, 21), (7, 12, 7, 7, 5, 5, 6, 10)]. Inline records are locators only; other formats include unclassified choice, written, matching, true/false and fill-in. Skipped uncertain numbered mappings: [].
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4503 source locators; section-level mapping 26/93 (Quant 11/11, Econ 8/8, CI 7/7). Exhaustive academic acceptance 0/93. Source notes retained. No newly authored questions or examples. Historical company cases not current claims.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Full tables, examples, question digitization, detailed draft audit, Kaplan/SAPP/other sources, browser and live GitHub Pages testing pending. Next: Financial Statement Analysis LM1.

# v11.4 — CFAI Corporate Issuers LM1–3 section-level coverage (2026-11-26)

- Original CFAI V3 SHA-256 matched catalog; LM1 pp11–44, LM2 pp45–73, LM3 pp75–103. Counts (LM, bilingual groups, numbered examples, Exhibit locators, added source example cards, end practice, inline MCQ, other inline): [(1, 14, 9, 16, 6, 5, 6, 19), (2, 11, 2, 7, 4, 5, 10, 19), (3, 14, 1, 2, 4, 5, 16, 13)]. Includes self-assessment, Knowledge Checks, Question Sets and numbered example exercises. Other inline includes written/calculation, two-option, matching, fill-in, true/false and multiple-select. All question records are page locators, not transcribed prompts. Existing 15 end-practice locators checked for question and solution headings; written formats identified.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4384 source locators. Section-level mapping 22/93 (Quant 11/11, Econ 8/8, CI 3/7); exhaustive academic acceptance 0/93. Historical cases not current claims; traditional direct listing treated as source model. No invented questions or cases.
- Changed recap-data.js, source-bank.js, README.md only. No full digitization, exhaustive academic acceptance or live browser/GitHub Pages test; Kaplan, SAPP, other sources and detailed drafts remain pending. Next: CI LM4 Working Capital and Liquidity; then LM5–7.

# v11.3 — CFAI Economics LM5–8 section-level coverage (2026-11-26)

- Original CFAI V2 SHA-256 matched source catalog. LM5 pp149–201; LM6 pp203–221; LM7 pp223–259; LM8 pp261–276. Counts (LM, bilingual groups, numbered examples, exhibits, additional selected example cards, end practice, inline MCQ, other inline): [(5, 20, 14, 15, 8, 10, 8, 20), (6, 10, 3, 3, 1, 8, 2, 17), (7, 13, 5, 6, 2, 4, 23, 3), (8, 7, 2, 1, 5, 7, 12, 0)]. Inline other includes written, true/false, fill-in, matching and multiple-select; all are source locators only, not transcribed prompts or options. Historical cases are not current facts. Existing source notes retained; no authored questions or invented examples.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4301 source locators. CFAI section-level mapping 19/93 (Quant 11/11, Economics 8/8); exhaustive academic acceptance 0/93. Existing detailed drafts, full example/table/question coverage and secondary sources not fully validated; no browser or hosted deployment verification. Next: Corporate Issuers LM1, then remaining modules; source-first only.
- Changed recap-data.js, source-bank.js, study.js (inline label only), README.md. 63 flat files.

# v11.2 — CFAI Economics LM3–4 section-level coverage (2026-11-26)

- CFAI V2 original PDF SHA-256 matched. Fiscal Policy pp87–112: 18 bilingual groups, 2 numbered examples, 10 Exhibit locators, 4 supplementary source example cards and 18 inline MCQ locators. Monetary Policy pp113–148: 20 bilingual groups, 3 numbered examples, 7 Exhibit locators, 6 supplementary source example cards and 23 inline MCQ locators. Existing 13 end-practice locators checked against numbered questions and solutions. No newly authored questions or scenarios.
- Source notes: p110 fiscal answer conflicts with p107 actual-versus-structural balance distinction; p95–96 budget neutrality distinguished from p105 output effects. Historical monetary policy and IMF study results are not current policy or universal coefficients.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4,216 source locators; section-level mapping 15/93 (Quant 11/11, Econ 4/8); exhaustive academic acceptance 0/93. Selected source paraphrases and locators only; full question/table digitization, secondary sources, older detailed drafts and browser/live GitHub Pages verification remain pending.
- Changed recap-data.js, source-bank.js, README.md only; 63 flat files. Next: Economics LM5 Introduction to Geopolitics and LM6 International Trade. Source-first only.

# v11.1 — CFAI Economics LM1–2 section-level coverage (2026-11-26)

- CFAI 2026 V2 original PDF SHA-256 matched source catalog. LM1 PDF pp11–56: 19 bilingual section groups, 4 numbered examples, 20 Exhibit locators, 6 additional selected source example cards, 2 formula cards, 16 inline MCQ and 7 written subpart locators. LM2 PDF pp57–86: 17 groups, 2 numbered examples, 14 Exhibit locators, 7 example cards, 1 formula card, 19 inline MCQ locators. Verified 28 existing end-practice locators by question/solution heading. No invented questions or scenarios.
- Source notes: shutdown equality, Nash versus zero profit, HHI top-N convention; LM2 p57/68–81 LOS c names external trade and housing but detailed external trade coverage is not present in a standalone section; housing discussed via credit and permits. Further source crosswalk required. Corrected LM2 business-cycle Question Set page 64 to 65.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4,175 source locators. Section-level mapping 13/93 (Quant 11/11, Economics 2/8), exhaustive academic acceptance 0/93. Selected examples and locators only; full digitization, secondary sources, old detailed drafts and browser/live GitHub Pages tests still pending.
- Changed recap-data.js, source-bank.js, README.md; 63 flat files. Next: Economics LM3 Fiscal Policy, then LM4 Monetary Policy. Source-first only.

# v11.0 — CFAI Quantitative Methods LM10–11 section-level coverage (2026-11-26)

- Original CFAI 2026 V1 SHA-256 matched. LM10 PDF pp271–333 (p334 blank): 22 bilingual section groups, 2 numbered example and 45 Exhibit locators, 10 additional source example cards, 3 formula cards, 29 inline written question locators. LM11 pp335–348: 17 groups, 3 Exhibit locators, 3 source illustration cards, no numbered examples or inline questions. Checked 41 end-practice question and solution heading locators; corrected 0 page mappings. No new invented questions or examples.
- Existing source notes retained; LM10 p308/p310 mismatched cross-reference labels noted. LM11 programming languages and database topics included; not an external coding course.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4,133 source locators. CFAI section-level mapping 11/93 (Quant 11/11); exhaustive academic acceptance 0/93. Appendix pp349–358 already listed separately, not counted as assessed module. Full digitization, secondary sources, detailed draft audit and browser/GitHub Pages tests remain pending.
- Changed recap-data.js, source-bank.js, README.md; 63 flat files. Next: Economics LM1, then remaining modules, source-first only.

# v10.9 — CFAI Quantitative Methods LM7–9 section-level coverage (2026-11-26)

- Continues v10.8 with supplied original CFAI 2026 V1 (catalog SHA-256 matched). LM7 PDF pp201–221 (p222 blank): 14 bilingual section groups, 4 example and 6 Exhibit locators, 4 additional example cards, 2 formula cards. LM8 pp223–249 (p250 blank): 14 groups, 3 example and 13 Exhibit locators, 6 example cards and 1 formula card. LM9 pp251–270: 12 groups, 4 example and 12 Exhibit locators, 6 example cards and 1 formula card. Checked 27 existing end-practice locators by matching numbered question and answer on the stored pages. Added 25 inline Question Set locators (9 MCQ, 16 written/multi-part). No invented questions or scenarios; references require the local source PDF.
- Source notes: LM7 p202 overview variance/SE and p208 empirical MAE differences; LM8 p232 existing left-tail note retained, p240 Q4 reversal and inconsistent statistic documented (correct decision fail to reject); LM9 p261 tied-rank shortcut differs from Pearson correlation of average ranks (−0.20921 vs source −0.20417), same approximate test decision; small-sample approximation limitation. Numerical notes explicitly distinguished from publisher content.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4,104 source locators. Section-level mapping 9/93 (Quant 9/11); exhaustive academic acceptance 0/93. Existing draft lesson content not certified; full example/table/question digitization and secondary sources still pending. No browser or live GitHub Pages test in this release.
- Changed recap-data.js, source-bank.js and README.md only; 63 flat files. Next: Quant LM10 Simple Linear Regression, LM11 Introduction to Big Data Techniques. Continue source-first, no additional authored practice.

# v10.8 — CFAI Quantitative Methods LM4–6 section-level coverage (2026-11-26)

- Continues v10.7, original CFAI 2026 V1 SHA-256 matched source catalog. LM4 PDF pp139–158: 11 bilingual section groups, 4 numbered examples and 5 Exhibit locators, 8 additional source example/illustration cards and 2 formula cards. LM5 pp159–182: 14 groups, 3 numbered examples and 11 Exhibit locators, 10 additional source example/illustration cards and 4 formula cards. LM6 pp183–200: 13 groups, 2 numbered examples and 7 Exhibit locators, 5 additional source example/illustration cards and 3 formula cards. All seven existing end-practice locators checked against question/solution pages. Added 21 inline Question Set locators (15 MCQ + 6 written/multi-part question groups); no invented practice or scenarios. Written groups count as one source record each, not number of subparts. Example cards are selected paraphrases, not full digitization of publisher examples.
- Source notes: LM4 p147 answer lettering misalignment and p153 diffuse-prior statement broader than given likelihoods; LM5 p173 Exhibit 10 repeated column II and tied lowest SD, p178 threshold rounding. Existing LM6 wording note retained. The coverage panel now distinguishes written/multi-part groups from MCQs. Original source files remain local, not included in public site ZIP.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4,079 source locators. CFAI section-level mapping 6/93 (Quant 6/11); exhaustive academic acceptance 0/93. Older authored detailed drafts, full tables/examples, secondary sources and question bank/mock coverage still pending.
- QA: verified prior modules and source records unchanged except append-only additions to LM4–6 and new locators; unique IDs, valid LOS/source references, source heading/page alignment, selected numerical checks, all JavaScript syntax passed. Attempted local Chromium browser regression, but navigation blocked by environment policy (ERR_BLOCKED_BY_ADMINISTRATOR); no successful live/browser UI test claimed. No live GitHub Pages deployment test.
- Changed recap-data.js, source-bank.js, study.js, README.md only; 63 flat files. Next: Quant LM7 Estimation and Inference, then LM8 Hypothesis Testing and remaining Quant modules. Source-first only.

# v10.7 — CFAI Quantitative Methods LM2–3 section-level coverage (2026-11-26)

- Continued v10.6 using original CFAI 2026 V1 from supplied ZIP, SHA-256 matched source catalog. LM2 PDF pp53–94: 18 bilingual section groups, 15 numbered examples indexed (11 additional source-example cards), 16 Exhibit headings, 5 additional formula cards, 12 existing end-practice links checked. LM3 PDF pp95–138: 16 bilingual section groups, 7 numbered examples indexed, 29 Exhibit headings, 7 additional example/illustration cards, 4 formulas, 9 existing end-practice links checked. Added 21 inline Question Set MCQ locators (9+3+4+5); p117 item 3 introduces Exhibit 15 and is not a separate MCQ. No invented questions or examples. Exhibit index excludes separately numbered Practice Problems exhibits. Example indices locate the source; they do not certify every subpart.
- Coverage panel now uses actual module example and exhibit counts; LM2 legacy section links are pointers only, LM3 uses LOS links without a claimed detailed crosswalk. Existing authored drafts preserved and not certified. Existing LM2 notes on terminal-value notation and put position retained. No publisher PDF, prompt or options included. Original practice requires local source PDF.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4,058 source locators. CFAI section-level source coverage 3/93, exhaustive academic acceptance 0/93. Secondary sources, full examples/tables/question digitization, old draft audit, and live hosted GitHub Pages testing remain outstanding.
- Changed recap-data.js, source-bank.js, study.js, README.md; 63 files. Next: Quant LM4 Probability Trees and Conditional Expectations, followed by remaining Quant modules. Source-first only.

# v10.6 — CFAI Quantitative Methods LM1 section-level source audit (2026-11-26)

- Continued v10.5, only supplied CFAI 2026 V1 original PDF pp11–52 (SHA-256 matched catalog). 18 bilingual source-based section groups, 15 numbered example heading locators, 17 exhibit locators, 13 additional worked-example/illustration recap cards (including additional parts of Ex.14), 6 formula cards. All 15 numbered examples now have at least one recap card; this is not full reproduction of all subparts/tables. 7 additional inline MCQ locators (Question Set 2, Ex.13 1, Ex.15 4) separated from the existing 13 end-of-module questions. No new authored MCQs or invented example scenarios.
- Updated Review page references for HPR and gross/net, clarified log returns and spreadsheet input conventions. Existing note on p24 mean identity retained. Added section-level coverage panel to LM1 Review with local PDF links; old lesson data and question IDs untouched.
- Totals: 93/93 Module Reviews, 365/365 LOS Reviews, 10/10 Master Reviews, 4,037 source question locators, 534 catalog records. Section-level audit started 1/93; exhaustive academic acceptance remains 0/93. Existing authored drafts have not been audited line by line. No live GitHub Pages test; secondary-source completeness and full case/table/question digitization remain pending.
- Changed recap-data.js, source-bank.js, study.js, README.md only. 63 flat files. Next: CFAI Quant LM2 Time Value of Money in Finance, then remaining Quant modules; return to unresolved LM1 detailed draft and secondary-source audit before any final sign-off. Source-first only.

# v10.5 — Ethics Review and Master Review (2026-11-26)

- Adds five selective CFAI 2026 Ethics Module Reviews (21 LOS) and Ethics Master Review. Source CFAI V10 PDF pp17–301, SHA-256 matched. Includes 23 substandard guidance/procedure cards, 210 numbered application heading locators (NOT full case summaries), selected source cases, GIPS concepts, 72 matched end-practice question/solution locators (12/10/39/11; LM5 uses inline cases). Also matched all 37 LM5 named cases to their Analysis headings. No new authored questions or invented cases.
- Review totals 93/93 modules, 365/365 LOS, 10/10 masters, 4,030 source locators; 0/93 exhaustive academic acceptance. Counts are format coverage only. Existing authored drafts preserved, not re-certified. LM3 example cards are page pointers, not full coverage. LM5 selected examples only. Kaplan, SAPP, bonus QBank, inline cases, supplementary referenced standards and exhaustive source mapping remain incomplete.
- Next: source gap analysis, starting with CFAI curriculum and existing review/lesson data; distinguish locators from actual content; no additional invented material. No live GitHub Pages validation.
- Changed recap-data.js, source-bank.js, study.js (labels) and README.md only; 63 files.

# v10.4 — Portfolio Management LM3–6 + Master Review (2026-11-26)

- Continues cumulative v10.3: adds CFAI 2026 Portfolio Management LM3–6 Review (24 LOS), 21 formula/relationship cards, 32 selected source example cards, 30 comparisons, 22 exam traps, 52 glossary cards and four module maps. Adds Portfolio Management Master Review synthesized from the six existing source-based reviews (64 formula/relationship cards across six modules; 139 mapped CFAI end practice problems). No new authored MCQs or invented example scenarios.
- Primary source: CFAI Volume 9 physical PDF pp131–168, 169–212, 213–247, 249–299; original PDF is not redistributed. Added 68 end-practice locators (15/19/15/19). These are links to local PDF pages, not reproduced question text. Source SHA-256 matched catalog. Secondary Kaplan/SAPP and bonus question banks still pending detailed mapping; examples and tables are selective, including some numbered examples not yet represented. Inline questions and knowledge checks not counted. Source discrepancy notes retained for LM4 rounding and LM6 hedge example.
- Cumulative review progress: 88/93 modules, 344/365 LOS, 9/10 Subject Master Reviews, 3,921 source locators. Detailed learning drafts retained, full academic acceptance remains 0/93. Do not interpret the review count as exhaustive coverage. No new content outside supplied sources. Historical data from the reading is not current market data.
- Changes: recap-data.js, source-bank.js, study.js (neutral calculator reference link label only), README.md. All 63 flat website files preserved. Next checkpoint: Ethics LM1–5 and Ethics Master Review; then exhaustive source gap analysis. No live hosted website validation in this release.

# v10.3 · Source-first Portfolio Management LM1–2 (2026-11-26)

- Continues v10.2 without removing existing content, changing study IDs or adding invented academic questions/examples. Adds LM1 and LM2 Module Reviews: 16 LOS, 43 formula/relationship cards, 25 source example/case cards, 21 comparisons, 19 traps, 31 glossary entries and 2 source-based process diagrams. Selected paraphrases, not exhaustive academic coverage.
- CFAI 2026 Volume 9 physical PDF pp13–70 and 71–129; selected Kaplan Book 4 Reading 83–84, SAPP PM slide example pp19–20 and revision mindmap reference. All eight and eleven numbered CFAI examples are represented by selected cards; further subparts, tables, slide cases, Kaplan quizzes and other question banks remain to be checked. CFAI LM1 p39 and p56 source discrepancies/rounding are flagged in review notes.
- Added 71 CFAI end-of-module question/solution locators (30 + 41). They are page pointers to original English questions/solutions, not digitized MCQs or independently audited answers. Publisher PDFs stay local.
- Progress: 84/93 Module Reviews; 320/365 LOS in review format; 8/10 Subject Master Reviews; 3,853 source locators; 534 source catalog entries; 0/93 exhaustive academic acceptance. PM 2/6 Module Reviews, 16/40 LOS. Existing learning drafts retained (not endorsed as fully verified).
- Next: Portfolio Management LM3 — Portfolio Management: An Overview, then LM4–6 and PM Master Review; Ethics thereafter. Source-first only until user approves any other expansion.
- QA: JS syntax, module/LOS alignment, matched question/solution numbering, unique locator IDs, old records preserved, source IDs valid. No live GitHub Pages browser regression or exhaustive academic audit performed. Only README.md, recap-data.js, source-bank.js changed. 63 flat files.

# v10.2 · Source-first Alternative Investments LM5–7 + Master Review

10 LOS, 20 formula/relationship cards, 29 source cases, 33 glossary, 25 comparisons, 21 traps, 3 visuals, 86 new locators (28 Practice Problems, 39 Question Sets, 19 opening Self-Assessment). Alternative Investments master: 7 modules, 22 LOS, 51 formula/relationship cards, 65 end-of-module practice locators. Overall 82/93 module reviews, 304/365 LOS, 8/10 masters, 3782 source locators, 534 PDF records, 0/93 exhaustive acceptance. No newly invented examples/questions. CFAI pp129–220; selected Kaplan R80–82, SAPP and mindmap.

# v10.1 · Source-first Alternative Investments LM1–4

12 LOS, 31 formula/relationship cards, 48 source cases, 42 glossary, 31 comparisons, 27 traps, 4 visuals, 120 new locators (37 Practice Problems, 52 Question Sets, 25 opening Self-Assessment, 6 Knowledge Checks). Overall 79/93 module reviews, 294/365 LOS, 7/10 masters, 3696 source locators, 534 PDF records, 0/93 exhaustive acceptance. No newly invented examples/questions. CFAI pp11–128; selected Kaplan Reading 76–79, SAPP and mindmap.

# v10.0 · Source-first Derivatives LM9–10 + Subject Master Review

4 LOS, 28 formula/relationship cards, 22 source cases, 15 glossary, 12 comparisons, 12 traps, 2 visuals, 37 new locators (10 Practice Problems, 19 Question Sets, 8 opening Self-Assessment). Derivatives: 10/10 module reviews, 22 LOS, 106 formula cards, 98 source cases, 48 end-of-module Practice Problems, 70 inline Question Sets, 8 Kaplan QBank, 8 opening Self-Assessment. Overall 75/93 module reviews, 282/365 LOS, 7/10 masters, 3576 source locators, 534 PDF records, 0/93 exhaustive acceptance. No newly invented examples/questions. CFAI pp205–246; Kaplan Reading 74–75; selected SAPP and mindmap.

# v9.9 · Source-first Derivatives LM5–8

9 LOS, 46 formula/relationship cards, 40 source examples, 30 glossary, 29 comparisons, 25 traps, 4 visuals, 67 new locators (25 CFAI Practice Problems, 42 in-text Question Set questions). No newly invented questions or cases. Overall 73/93 Module Reviews, 278/365 LOS, 6/10 Subject Master Reviews, 3,539 locators, 534 PDF catalog, 0/93 exhaustive source acceptance. CFAI pp107–204; Kaplan pp192–213, selected SAPP pp131–248 and mindmap. Source-specific inconsistencies are marked separately.

# v9.8 · Source-first Derivatives LM1–4

9 LOS, 32 formula/relationship cards, 36 source cases, 34 glossary, 26 comparisons, 21 traps, 4 visuals, 30 new locators (13 CFAI Practice Problems, 9 in-text Question Set questions, 8 Kaplan Reading 69 QBank). No newly invented questions or cases. Overall 69/93 Module Reviews, 269/365 LOS, 6/10 Subject Master Reviews, 3,472 locators, 534 PDF catalog, 0/93 exhaustive source acceptance. CFAI pp11–106; Kaplan pp163–191; SAPP and mindmap structural cross-check; selected Kaplan QBank. LM4 has no separate end-of-module Practice Problems.

# v9.7 · Source-first Fixed Income LM17–19 + Subject Master Review

10 LOS, 22 formula/relationship cards, 27 source examples/cases, 23 glossary entries, 18 comparisons, 16 traps, three visuals, 33 new CFAI practice locators. Fixed Income: 19/19 reviews, 51 LOS, 152 master formula/relationship cards, 38 comparison cards, 57 traps, 141 CFAI practice locators. Overall: 65/93 Module Reviews, 260/365 LOS, 6/10 Subject Master Reviews, 3442 locators, 534 catalog records, 0/93 exhaustive source acceptance. No newly invented questions or academic examples. CFAI physical pp453–546, selected Kaplan Reading 63–65.

# v9.6 · Source-first Fixed Income LM13–16

11 LOS, 34 formula/relationship cards, 38 source examples/cases, 27 glossary entries, 24 comparisons, 21 traps, four visuals. 29 new CFAI practice locators. 62/93 Module Reviews, 250/365 LOS, 5/10 Subject Master Reviews, 3409 source locators, 534 catalog records, 0/93 exhaustive source acceptance. No newly authored questions/examples. CFAI physical pp331–452, selected Kaplan Reading 59–62.

# v9.5 · Source-first Fixed Income LM9–12

11 LOS, 36 formula/relationship cards, 33 source examples, 24 glossary entries, 23 comparisons, 22 traps, four visuals. 33 new CFAI practice locators. 58/93 Module Reviews, 239/365 LOS, 5/10 Subject Master Reviews, 3380 source locators, 534 catalog records, 0/93 exhaustive source acceptance. No newly authored questions/examples. CFAI physical pp221–330, selected Kaplan Reading 55–58 and SAPP convexity example.

# v9.4 · Source-first Fixed Income LM5–8

v9.4: Fixed Income LM5–8, 9 LOS, 37 formula/relationship cards, 31 source examples, 28 glossary entries, 22 comparisons, 19 traps, 4 visuals. Added 25 CFAI practice locators; 54/93 module reviews, 228/365 LOS, 5/10 subject reviews, 3347 source locators, 0/93 exhaustive acceptance. No newly authored academic questions/examples.

# v9.3 · Source-first Fixed Income

v9.3: Fixed Income LM1–4, 10 LOS, 23 formula/relationship cards, 22 source examples, 26 glossary entries, 20 comparisons, 16 traps, 4 visuals. Added 21 CFAI practice locators; 50/93 module reviews, 219/365 LOS, 5/10 subject reviews, 3322 source locators, 0/93 exhaustive acceptance. No newly authored academic questions/examples.

# v9.2 — Full cumulative website / Website tích lũy

Equity LM5–8: 28 LOS, 52 formula/relationship cards, 30 source examples/cases, 30 glossary entries, 23 comparisons, 22 traps, 4 source visuals. 58 prior CFAI locators rechecked; no new questions. Equity master: 8 modules, 66 LOS, 78 formula/relationship cards, 35 comparisons, 34 traps, 179 practice locators. Overall 46/93 module recaps, 209/365 LOS, 5/10 subject masters, 0/93 exhaustive acceptance, 3,301 source locators, 534 PDF catalog entries. 63 files. Source-first, no new academic examples/questions. Selected CFAI/Kaplan/SAPP/Mindmap material, not exhaustive source extraction.

# v9.1 — Full cumulative website / Website tích lũy

Equity LM1–4: 38 LOS, 26 formula/relationship cards, 24 source examples, 30 glossary entries, 23 comparisons, 24 traps, 4 visuals. 121 prior CFAI locators rechecked; no duplicate or invented questions. 42/93 Module Reviews, 181/365 LOS, 4/10 Subject Master Reviews, 0/93 full source acceptance. 3301 locators, 534 PDF records, 63 files. Source-based summaries, not full extraction; Equity Master Review pending LM5–8.

# v9.0 — Full cumulative website / Website tích lũy

Source-first FSA LM9–12 (23 LOS): 87 formula/relationship cards, 29 source examples, 27 glossary entries, 21 comparisons, 23 traps, 4 source visuals; 73 existing CFAI practice locators rechecked, no duplicates. FSA Master Review: 12 modules, 53 LOS, 121 selected formula/relationship cards, 20 comparisons, 36 traps, 208 CFAI Practice Problems locators. 38/93 module reviews, 143/365 LOS reviewed in recap format, 4/10 subject master reviews, 0/93 final acceptance. 3301 locators, 534 catalog PDFs, 63 website files. No invented questions/examples; source PDFs local.

# v8.9 — Full cumulative website / Website tích lũy

Source-first FSA LM5–8 (11 LOS): 57 formula/relationship cards, 30 source examples, 26 glossary entries, 21 comparisons, 21 traps, 4 visuals. 79 existing CFAI practice locators rechecked, no duplicates. 34/93 module reviews, 120/365 LOS reviewed in recap format, 3/10 subject master reviews, 0/93 final acceptance. 3301 locators, 534 catalog PDFs, 63 files. No invented questions/examples. Original PDFs remain local.

# v8.8 — Full cumulative website / Website tích lũy

Source-first: FSA LM1–4 (19 LOS), 36 formula/relationship cards, 25 source examples/cases, 24 glossary entries, 4 visuals, 56 existing CFAI practice locators rechecked (no duplicates added). 30/93 module reviews, 109/365 LOS in reviews, 3/10 subject master reviews, 0/93 final acceptance. 3,301 source locators, 534 PDF catalog entries, 63 root files. No invented questions or examples. Original PDFs remain local.

# v8.7 — Full cumulative website / Website tích lũy

Source-first: Corporate Issuers LM5–7 (10 LOS), 20 formula/relationship cards, 19 source examples/cases, 19 glossary entries, 3 visuals, 15 CFAI practice locators; Corporate Issuers Master Review (7 modules, 44 formula/relationship cards, 9 comparisons, 27 traps). 26/93 module reviews, 90/365 LOS in reviews, 3/10 subject master reviews, 0/93 final acceptance. 3,301 source locators, 534 PDF catalog entries, 63 root files. No invented questions or examples. Original PDFs remain local.

# v8.6 — Full cumulative website / Website tích lũy

Source-first: Corporate Issuers LM1–4 (12 LOS), 24 formula/relationship cards, 20 source examples/cases, 25 glossary entries, 4 visuals, 20 CFAI practice locators. 23/93 module reviews, 80/365 LOS in reviews, 2/10 subject master reviews, 0/93 final acceptance. 3,286 source locators, 534 PDF catalog entries, 63 root files. No invented questions or examples. Original PDFs remain local.

# v8.5 — Full cumulative website / Website tích lũy

Source-first: Economics LM5–8 (14 LOS), 24 formula/relationship cards, 21 source examples/cases, 27 glossary entries, 4 source visuals, 29 CFAI practice locators. Economics Master Review covers all 8 modules with 47 formula/relationship cards, 10 comparison groups, 24 traps, 70 CFAI practice locators. 19/93 module summaries, 68/365 LOS in recaps, 2/10 subject master reviews, 0/93 final acceptance. 3,266 source locators, 534 PDF catalog entries, 63 root files. No invented questions or examples. Original PDFs remain local.

# v8.4 — Full cumulative website / Website tích lũy

Source-first: Economics LM1–4 source-based module summaries (16 LOS), 23 formula/relationship cards, 17 source examples/cases, 22 glossary entries, 4 source visuals, 41 CFAI practice locators. 15/93 module summaries, 54/365 LOS in recaps, 1/10 subject master reviews, 0/93 final acceptance. 3,237 source locators, 534 PDF catalog entries, 63 root files. No invented MCQ/examples. Full ZIP only; all previous content retained. Original PDFs remain local. Economics master review pending LM5–8.

# v8.3 — Full cumulative website / Website tích lũy

Source-first, no new invented questions. Quantitative Methods LM1–11 module summaries (38 LOS) plus subject master review: 79 selected formula/relationship cards, 11 method comparisons, 23 traps, 11 module practice links and session checklist. 41 new CFAI question/solution locators; 3,196 total, 534 PDF catalog entries, 93 modules, 365 LOS, 63 root files. Academic acceptance 0/93. Prior learning datasets and IDs unchanged. Use full ZIP only; no previous patch needed. Original PDFs remain local.

# v8.2 — Quantitative Methods review LM6–9

Source-first: QM LM6–9 recaps (11 LOS, 29 formula/relationship cards, 21 source-example summaries, 24 glossary entries, 31 CFAI question/solution locators, 4 source-derived figures). No new invented questions/examples. CFAI PDF p.232 left-tailed variance test error explicitly annotated, p.187 lognormal prose and p.208 sampling comparison caveats recorded. Spearman rank ties condition explicitly identified as mathematical clarification. QM 9/11; module recaps 9/93, subject preview 1/10, final subject reviews 0/10, academic acceptance 0/93. 3,155 locators; 534 catalog entries; 63 root files.

# v8.1 — Quantitative Methods review LM1–5

Source-first: new recaps QM LM2–5 (13 LOS, 44 formula/relationship cards, 29 source-example summaries, 24 new CFAI question/solution page locators, 4 source-derived visuals). Glossary on all five recaps; revision checklist per LOS, session-only. All old deep content retained. No new invented questions/examples. Subject QM remains overview preview; 5/93 module recaps, 1/10 subject previews, 0/10 final subject reviews, 0/93 academic acceptance. 3,124 source locators, 534 catalog entries. 63 root files.

# v8.0 — Module Review & Subject Key Review (source-first)

Design reference: supplied Analyst Guide CFA Level I 2027 QM LM1, 30 pages; layout only, not syllabus. CFA 2026 remains authoritative. New recap navigation at end of every module and subject, with explicit pending status when source-based recap not yet written. Pilot: QM LM1, 5 LOS, 15 formula/relationship cards, 7 worked examples summarized from actual CFAI PDF, 5 relations, 8 traps, calculator source pointer, and 13 original practice question/solution locators. Subject QM: preview only, 11 module concept cards and 8 selected formula cards. No additional self-authored questions or invented examples. All prior academic datasets and progress keys preserved. 3,100 source locators total, 534 PDF catalog records. 63 root files. Recap pilot 1/93, subject preview 1/10; final academic acceptance still 0/93. Source PDFs stay on learner device. Do not upload private audit.

# v7.9 — Source-first / Ưu tiên tài liệu gốc

User direction supersedes prior self-authored expansion: do not add invented questions, examples, concepts, formulas, flashcards or simulations. Use the supplied materials only; distinguish source navigation, source-grounded paraphrase/translation, and existing self-authored drafts. All prior materials and progress keys retained as optional supplements, not certified. 534 original PDF records (all nine supplied archives), 93/93 CFAI and 93/93 Kaplan module outlines from actual PDF bookmarks; 2,231 subheading bookmarks. 3,087 source question/answer locators, including 265 new FSA LM10–12 locators. 137 Kaplan question IDs matched and 63 Bonus stems paired; 65 CFAI numbered problem/solution pairs. Locators are not copies of questions and do not certify answers. Original PDFs remain local and must be selected by the learner. Prior academic expansion checkpoint 28/93 modules and 161/365 LOS; no increment for metadata; final acceptance 0/93. Source semantic completeness is still unestablished. 62 root files. Export progress before upload. See audit for limitations.

# v7.8 — FSA LM8–LM9 targeted expansion

Two modules / seven LOS; 28 original bilingual concepts, English MCQs and flashcards; 124 original-PDF locators. Preserve source colors and separate banks. Export progress before updating. Targeted review is not final academic acceptance.

# v7.7 — FSA LM6–LM7 targeted expansion

Two modules / six LOS; 24 original bilingual concepts, English MCQs and flashcards; 150 original-PDF locators. Preserve source colors and separate banks. Export progress before updating. Targeted review is not final academic acceptance.

# v7.6 — FSA LM4–LM5 targeted expansion

Two modules / six LOS; 18 original bilingual concepts, English MCQs and flashcards; 103 new original-PDF locators. Preserve source colors and the separate banks. Export progress before updating. Targeted review is not final academic acceptance.

# v7.5 — FSA LM1–LM3 targeted expansion

Three modules / fifteen LOS, 30 original bilingual concepts, 30 original English MCQs and cards, 308 original-PDF locators. Original content is marked with existing color labels; source locators are not verified answers. Export progress before updating. This is not final academic acceptance.

# v7.4 — Ethics Standards I–VII and Ethics Application targeted expansion

19/93 modules, 127/365 LOS targeted first pass; Ethics 5/5 (21/21 LOS), PM 6/6, Equity 8/8. 7,201 original MCQs and 2,137 question/solution PDF locators (not unique question content). 62 files. Final academic acceptance 0/93. Provisional source mapping and independent validation pending. Existing origin labels, two banks and old answer positions retained.

# v7.3 — Ethics LM1, LM2 and LM4 targeted expansion

17/93 modules, 122/365 LOS targeted first pass; Ethics 3/5 (16/21 LOS), PM 6/6, Equity 8/8. 7,168 original MCQs; 1,560 PDF question/answer locators. 62 files. Origin labels and old answer positions retained. Ethics LM3 and LM5 pending first-pass academic expansion; 18 mixed LM5 source items indexed but not fully reviewed. Final academic acceptance 0/93.

# v7.2 — PM LM5–LM6 targeted expansion

14/93 modules, 106/365 LOS targeted first pass; PM 6/6, 40/40 LOS; Equity 8/8. 7,143 original MCQs; 1,413 PDF question/answer locators. 62 files. Origin labels and old question positions retained. Final academic acceptance 0/93.

# v7.1 — PM LM3–LM4 targeted expansion

12/93 modules, 96/365 LOS targeted first pass; PM 4/6, 30/40 LOS. 7,111 original MCQs; 1,322 original PDF question/answer locators. 62 files. Amber/green/blue/gray origin labels retained, not verification. Prior question positions unchanged. No final academic acceptance.

# v7.0 — Portfolio Management LM1–LM2 + origin labels

Original Study Hub content: amber + explicit label (not independently certified). Original-source PDF locators: green. Blue label indicates an explicit topic anchor, not verification. Archived HTML fragments: gray pending origin review. Language selector now available on all LOS (untranslated sections retain a Vietnamese fallback).

10/93 modules and 82/365 LOS targeted expansion, 0/93 final acceptance. 7,083 original MCQ, 1,196 question locators, 62 website files. Previous content and question positions retained.

# v6.9 — Equity LM7–8 targeted expansion

- 18 LOS; 30 bilingual concepts/cards, 47 original English MCQs, 15 formula cards, 4 examples, 3 visual maps and a two-stage DDM lab.
- 865 source PDF question/solution locators (+294), separate from self-authored questions. Original PDFs not distributed. No claim of final answer verification.
- Targeted 8/93 modules, 66/365 LOS; Equity 8/8 targeted; final acceptance 0/93. Language selection now enabled for all 8 Equity modules; legacy untranslated content retains fallback.
- Upload 62 files or 5-file patch only from v6.8. Backup progress before updating.

# v6.8 — Equity LM5 & LM6 targeted expansion

- 10 LOS (Company Analysis: Past and Present; Industry and Competitive Analysis), 29 new bilingual concepts/cards, 35 new original English MCQs, 8 formula/analysis cards, 5 examples and 4 visual maps.
- Source-separated practice preserved: 571 original PDF question/solution locators (+123), 496 exercise-related PDF catalog entries. Original documents remain local, not included in website. Source locators do not certify answers.
- Targeted expansion progress: 6/93 modules, 48/365 LOS; Equity 6/8 modules, 48/66 LOS; final acceptance 0/93. All prior LOS and MCQ keys retained. Old English translations, full source-answer adjudication, mock and legacy reconciliation remain open.
- Upload 62 root files, or the 5-file patch if and only if repository is exactly v6.7. Backup progress. No backend/build required.

# v6.7 — Source-separated practice, collapsible sidebar, Equity LM4

- Two distinct practice areas: original Study Hub MCQs (unvalidated draft) and actual source PDF locators (not copied publisher content). Source library has 448 question/solution locators with physical PDF pages, plus 496 exercise-related PDFs indexed by filename. PDF bytes remain local; select original files in the browser. SHA-256 comparison where Web Crypto is available, otherwise explicitly labeled filename/size fallback. No source PDF scoring or automatic academic certification.
- Sidebar toggle on desktop and mobile. Desktop preference persists; mobile opens as a dismissible overlay. Existing answer IDs and storage format retained.
- Equity LM4: 8 LOS expanded, 24 new original English MCQs with bilingual feedback and 16 bilingual concepts/cards. 79 new original-document locators. Academic review remains partial. Progress: 4/93 modules and 38/365 LOS targeted expansion, 0 final acceptances.
- Static site: upload 62 root files; no backend or build. Backup progress first. Do not upload private audit.

# v6.6 — Equity LM3 Market Efficiency

7 LOS expanded; 29 original English MCQs, 19 new bilingual concepts/cards, 5 examples, 2 formula entries, 3 visual summaries and Event Study Lab. 35 pre-existing concept/card translations, 21 pre-existing MCQ explanations and 7 old example explanations added in English. All older fields and IDs retained. Targeted source review only, not final acceptance. Progress: 3/93 modules and 30/365 LOS received targeted expansion; 0 final academic acceptances. Backup progress before upload.

# v6.5 — Equity LM1 residual review and LM2 index expansion

55 new original MCQs, 26 bilingual concepts/cards, 13 worked examples and index weighting lab. LM2 existing sections, questions and cards retain order; English explanations added. Targeted review, not complete academic acceptance. See private QA. No storage-key changes.

# v6.4 — Equity LM1 targeted expansion

- 12 LOS expanded; 58 original English MCQs appended; 35 bilingual concepts and flashcards, 12 worked examples, 3 formula entries. Source audit remains in progress. Language selector applies to newly authored material; old Vietnamese material falls back without pretending it is translated.
- Order book lab in LM1 LOS 7/8/10. Retains all original question positions and storage keys. Back up progress before replacing files.
- Static GitHub Pages, no build. Upload the 61 root files, not the private audit ZIP.

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
