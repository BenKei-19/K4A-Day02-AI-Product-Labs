# 02 — Group Problem Statement (Bản nộp nhóm)

> Làm chung 1 bản, mỗi thành viên copy vào repo cá nhân. Đi theo Phase 3 → 6 trong `01-worksheet.md`. Nhóm chỉ chọn **candidate problem** ở Phase 3, viết Problem Statement sau khi validate + vẽ workflow.

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm (VD: facilitator, workflow, research, writer) |
|-----|-----------|-------------|---------------------------------------------------------------|
| 1   | Nguyễn Quang Huy | 2A202602421 | Team Lead, Writer, Workflow |
| 2   | Trần Văn An | 2A202602422 | Research, Validation |
| 3   | Lê Thị Bích | 2A202602423 | Facilitator, Problem Scoping |
| 4   | Phạm Quang Cường | 2A202602424 | Workflow, Editor |

**Candidate problem nhóm chọn (1 câu):**
BA/PM mất quá nhiều thời gian (3-5h) để viết một bản mô tả yêu cầu sản phẩm (PRD) chi tiết từ meeting notes, dễ bỏ sót các edge cases gây chậm trễ cho dev.

---

## Phase 3 — Group Convergence: từ 9-12 candidates về 1

### 3.1. Trình bày top 3 mỗi người (mỗi candidate 1-2 phút)

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh của nhóm |
|---|---|---|---|---|---|
| 1 | Huy | Viết PRD chi tiết tốn 3-5h/bản | BA/PM | Nghĩ và rà soát edge cases | Đau thật, ai làm BA cũng nản |
| 2 | Huy | Phân tích 50-80 feedback khách hàng | BA/PM | Đọc và phân loại thủ công | Hữu ích nhưng data nhạy cảm |
| 3 | Huy | Tổng hợp meeting notes sau họp | PM/Scrum Master | Nghe lại và gán action items | Dễ làm, nhiều tool có sẵn |
| 4 | An | Code review tốn nhiều thời gian | Senior Dev | Đọc code của junior để tìm lỗi logic | Hơi khó làm bằng AI vì context lớn |
| 5 | An | Sinh test case UAT từ PRD | QA / BA | Viết lặp lại các kịch bản test chuẩn | Khá hay, đầu vào chuẩn xác |
| 6 | An | Dịch tài liệu API nội bộ sang tiếng Anh | Dev | Dịch technical terms | Ít gặp, tần suất thấp |
| 7 | Bích | Trả lời ticket hỗ trợ khách hàng lặp lại | CS Team | Tra cứu chính sách để trả lời | Đã có chatbot rồi |
| 8 | Bích | Tạo báo cáo tiến độ tuần (Weekly report) | PM | Copy paste số liệu từ Jira | Làm bằng tool tự động tốt hơn AI |
| 9 | Bích | Viết Release Notes từ Github PRs | Tech Lead | Rà soát hàng chục PR description | Dễ làm, impact vừa phải |
| 10 | Cường | Tóm tắt tài liệu specs dài của đối tác | Dev / BA | Đọc 100 trang PDF | Thường xuyên cần nhưng dễ dùng ChatGPT thẳng |
| 11 | Cường | Sinh dummy data để test | Tester | Nghĩ ra data hợp lệ | Dùng script Python cũng làm được |
| 12 | Cường | Trích xuất thông tin từ hóa đơn | Kế toán | Nhập tay data hóa đơn | Là bài toán OCR cũ, ít hứng thú |

### 3.2. Gom trúng / cluster (gom 9-12 ý thành 3-4 cụm)

| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| A (Sinh văn bản từ notes) | 1, 3, 5, 9 | Biến thông tin thô (notes, PRs) thành tài liệu chuẩn (PRD, Release Notes, Test case) | Có cấu trúc rõ ràng, LLM làm rất tốt |
| B (Phân loại & Trích xuất) | 2, 7, 12 | Nhận lượng lớn text hỗn độn, cần rút trích insights hoặc metadata | Đòi hỏi xử lý ngôn ngữ tự nhiên tốt |
| C (Công cụ Dev/Test) | 4, 6, 11 | Hỗ trợ coder và tester (code review, dummy data, translation) | Yêu cầu hiểu sâu về kỹ thuật, rủi ro sai sót cao |

### 3.3. Shortlist (giữ 2-3 bài trả lời được 7 câu hỏi worksheet)

| Candidate | Vì sao vào shortlist (2-3 ý) | Rủi ro / điều chưa rõ |
|---|---|---|
| 1 (Viết PRD) | Impact cực lớn (giải phóng BA), quy trình rõ ràng, đầu vào (meeting notes) dễ chuẩn hóa. | Làm sao ép AI viết đúng template và thuật ngữ công ty. |
| 2 (Phân tích feedback) | Giải quyết được bài toán quá tải thông tin, AI cluster tốt hơn người làm tay. | Dữ liệu feedback thường chứa thông tin nhạy cảm của khách. |
| 5 (Sinh test case UAT) | Đầu vào (PRD) rất chuẩn, đầu ra (Test case Excel/Jira) dễ kiểm chứng đúng/sai. | Đôi khi test case cần business logic ngầm định mà PRD ko ghi. |

### 3.4. Score để đồng thuận (chấm 1-5, ép nói rõ vì sao cho 5 / cho 3)

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| 1 (PRD Writer) | 5 | 5 | 5 | 5 | 4 | 5 | 5 | 34 |
| 2 (Feedback) | 4 | 4 | 4 | 4 | 3 | 4 | 5 | 28 |
| 5 (Test Case) | 5 | 4 | 4 | 4 | 4 | 4 | 4 | 29 |

**Candidate nhóm chọn (1 bài duy nhất):**

```text
AI-Assisted PRD Writer (Sinh nháp PRD chi tiết từ Meeting Notes).
```

**Vì sao chọn (4-5 câu):**

```text
Chúng tôi chọn bài toán này vì nó có điểm số cao nhất (34/35) và mọi thành viên đều hiểu rõ nỗi đau của việc phải hì hục gõ PRD hàng giờ đồng hồ. Workflow rất rõ ràng: từ lúc có meeting notes đến lúc ra bản PRD cuối cùng. Impact có thể đo lường ngay lập tức bằng số giờ tiết kiệm được (từ 3-5h xuống còn chưa tới 1h). Bài toán này đủ phức tạp để thiết kế một AI Workflow (RAG, chaining) thay vì chỉ gọi ChatGPT một lần.
```

**Vì sao KHÔNG chọn các candidate còn lại (mỗi bài 2-3 câu):**

```text
- Feedback Analyzer: Đầu vào khá rác và chứa nhiều dữ liệu nhạy cảm (PII), khó kiếm đủ dữ liệu sạch để làm demo trong phạm vi bài Lab.
- Test Case Generator: Dù dễ làm, nhưng impact không chạm trực tiếp đến phần core business như PRD. Nếu PRD sai thì test case AI sinh ra cũng sai theo (Garbage in, Garbage out).
```

**Disagreement (nếu có — ai lo gì, chốt ra sao):**

```text
Bạn An lo lắng rằng AI sinh PRD sẽ bị "ảo giác" bịa thêm tính năng không có thật. Nhóm chốt giải pháp là AI chỉ sinh bản "Draft" (Nháp), và tạo một boundary cứng yêu cầu con người (BA) phải review và duyệt từng section trước khi chốt.
```

---

## Phase 4 — Quick Validation + Research

### 4.1. Quick validation (Ít nhất 1 cách: interview 2-3 người hoặc survey 5-10 người)

| Nguồn | Số người / mẫu | Tín hiệu xác nhận (kèm quote nguyên văn) | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Interview BA | 2 người | "Viết PRD mệt nhất là rà soát edge cases, lỡ sót là dev chửi sấp mặt." | "Anh không tin AI viết được business logic phức tạp." | Đóng khung AI chỉ viết phần khung, edge case chuẩn, còn logic lõi BA phải kiểm tra lại. |
| Interview Dev | 1 người | "Mấy cái PRD dài dòng đọc mệt, anh chỉ cần bảng Acceptance Criteria rõ ràng." | (Không có) | Thêm yêu cầu AI phải sinh bảng Acceptance Criteria thật ngắn gọn, dạng checklist. |

**Insight sau validation (1-2 câu — pain thật nằm ở đâu):**

```text
Pain thật sự không phải là việc "gõ chữ", mà là việc bị "sót trường hợp" (edge cases) và cấu trúc PRD lộn xộn khiến Dev khó đọc.
```

Bằng chứng đính kèm (nếu có): `02-group-problem-statement-interview-notes.md`

### 4.2. Research giải pháp đã có (Ít nhất 2-3 tools/patterns + 1-2 link kiểm chứng)

| Nguồn / tool / case | Link | Họ giải quyết bước nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| ChatPRD | chatprd.ai | Gen full PRD từ prompt ngắn | Dễ dùng, tối ưu riêng cho PM | Không tùy chỉnh được template riêng của công ty | Cần tính năng feed custom template. |
| Notion AI | notion.so | Auto-complete & summarize | Tích hợp sẵn trong workspace | Phải prompt bằng tay mỗi lần, ko có cấu trúc bắt buộc | Cần tạo prompt chain tự động. |
| Jira AI | atlassian.com | Tạo User Story | Gắn liền với task dev | Chỉ viết ngắn gọn, không đủ thành 1 PRD dài | Chia nhỏ PRD thành các User stories. |

**Research takeaway (2-3 câu — nên build gì / không build gì):**

```text
Nhóm KHÔNG build một con chatbot chat qua lại (như Notion AI), mà build một WORKFLOW một chiều (Form input -> Gen PRD Draft -> BA Review). Điểm khác biệt là hệ thống sẽ bắt buộc tuân theo template chuẩn của công ty và có bước tự động nhắc nhở edge cases.
```

---

## Phase 5 — Workflow + Problem Statement

### 5.1. Current workflow bên nhóm

Dán workflow hoặc link file: `02-group-problem-statement-workflow.png`

```text
[1 Họp lấy yêu cầu: 30' - BA] → [2 Lập dàn ý & flow: 60' - BA] → [3 Viết chi tiết + Edge cases: 120' - BA] → [4 Review nội bộ: 30' - PM/Dev]
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú (handoff? bottleneck?) |
|---|---|---|---|---|---|
| 1 | BA | Context dự án | Meeting notes thô | 30 phút | Thu thập ý kiến |
| 2 | BA | Notes | Dàn ý PRD | 60 phút | Đòi hỏi sắp xếp logic |
| 3 | BA | Dàn ý | Full PRD Draft | 120 phút | BOTTLENECK. Tư duy vét cạn edge cases rất mệt |
| 4 | Dev | PRD Draft | Feedback | 30 phút | Handoff sang team khác |

**Bottleneck chính (2-3 câu):**

```text
Bước 3 là bottleneck. Việc phải viết thành văn bản hoàn chỉnh và tưởng tượng ra mọi edge case (tài khoản hết hạn, lỗi mạng, nhập sai...) tiêu tốn rất nhiều năng lượng, dễ sai sót và phụ thuộc hoàn toàn vào kinh nghiệm của BA.
```

### 5.2. Future workflow bên nhóm

```text
[1 Họp lấy yêu cầu: 30' - BA] → [2 AI gen Dàn ý + Flow: 2' - Máy] → [3 AI gen chi tiết + Edge case: 3' - Máy] → [4 BA Review & Edit: 25' - Human boundary] → [5 Dev Review: 30']

Fallback: Nếu AI gen sai template hoặc bị "ảo giác", BA từ chối bản draft và quay về gõ tay từ meeting notes.
```

**Before/after impact:**

| Metric | Trước | Sau kỳ vọng | Cách đo |
|---|---:|---:|---|
| Tổng thời gian BA làm | 210 phút | 60 phút | Bấm giờ từ lúc họp xong đến lúc gửi dev |
| Số bước thao tác tay | 4 | 2 | Đếm số chặng BA trực tiếp viết |
| Tỷ lệ sót edge cases | Cao (2-3 bug/sprint) | Thấp (0-1 bug) | Số lượng câu hỏi clarify từ QA/Dev |
| Bottleneck chính | Viết chi tiết (120') | Chờ AI gen (5') | Bấm giờ |
| Risk mới | BA lười đọc lại | Có thể sót lỗi logic AI bịa ra | Track số lượng edit của BA trên draft |

### 5.3. Problem Statement v0 (mỗi field 2-3 câu)

| Field | Nội dung |
|---|---|
| **Actor** | Business Analysts (BA) và Product Managers (PM), những người phải viết PRD hàng tuần. |
| **Workflow** | Sau khi họp lấy yêu cầu, BA phải tự viết dàn ý, liệt kê edge cases, viết thành tài liệu chi tiết và gửi cho Dev review. |
| **Bottleneck** | Bước viết tài liệu chi tiết và vét cạn edge cases cực kỳ tốn thời gian (120 phút) và não bộ. |
| **Impact** | Rút ngắn thời gian làm tài liệu từ 3-4 tiếng xuống còn dưới 1 tiếng, giúp BA tập trung vào nghiên cứu người dùng thay vì gõ chữ. |
| **Success Metric** | Giảm 70% thời gian tạo PRD nháp, tỷ lệ Dev chấp nhận PRD ở lần review đầu tiên > 80%. |
| **Boundary** | AI chỉ tạo bản NHÁP (Draft). BA bắt buộc phải là người đọc duyệt, chỉnh sửa cuối cùng và chịu trách nhiệm về nội dung. |

**Câu hỏi AI phản biện v0 (nếu có):**
- Field nào mơ hồ: "Tỷ lệ Dev chấp nhận PRD ở lần review đầu tiên > 80%" khá khó đo lường định lượng trong ngắn hạn.
- Tôi sửa gì: Đổi success metric thành "Số câu hỏi clarify từ Dev giảm đi 50% trong quá trình grooming".

---

## Phase 6 — Rule / Workflow / Agent + Decision

### 6.0. Ma trận độ phù hợp (suy nghĩ nhanh, không thay quyết định cuối)

- Độ mơ hồ: [ ] Thấp (có đúng/sai rõ) / [x] Cao (nhiều cách trả lời vẫn OK) — Vì sao: Không có 1 bản PRD "hoàn hảo" duy nhất, văn phong và format có thể du di.
- Độ phức tạp: [ ] Thấp (1-2 bước) / [x] Cao (3+ bước/nguồn, phụ thuộc nhau) — Vì sao: Cần gen dàn ý trước, sau đó từ dàn ý mới gen chi tiết, rồi check lại với template.

**Bài toán nhóm nằm ở Ô nào:**

```text
Ô C: Độ mơ hồ cao + Độ phức tạp cao (Cần AI Workflow với nhiều prompt nối tiếp nhau).
```

**Vì sao (2-3 câu):**

```text
Do đầu ra dài (1 PRD có thể vài trang), nếu dùng 1 prompt duy nhất AI sẽ bị quên context hoặc sinh nội dung nông. Cần bẻ nhỏ thành quy trình nhiều bước (chaining) để kiểm soát chất lượng từng phần.
```

### 6.1. So sánh Rule / Workflow / Agent (so trên cùng 1 bài)

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? (Dùng cho bước nào?) |
|---|---|---|---|---|
| **Rule** | Dùng template Word/Confluence bắt điền tay. | Đã áp dụng nhưng BA vẫn lười điền chi tiết. | Mất thời gian, không giải quyết được bottleneck. | Không |
| **Workflow** | Nối nhiều prompt: Prompt 1 (Lọc ý) -> Prompt 2 (Gen flow) -> Prompt 3 (Gen edge case). | Đủ kiểm soát chất lượng từng module của PRD. | Nếu prompt 1 sai, các bước sau sẽ sai dây chuyền. | CÓ (Làm core) |
| **Agent** | Cho AI tự tạo file, tự tra cứu Jira, tự email cho Dev. | Vượt quá nhu cầu, không đáng để đầu tư. | Mất kiểm soát, AI có thể gửi mail PRD sai tùm lum. | Không |

**5 câu hỏi chốt (trả lời câu đầy đủ):**
1. Rule có giải được 70-80% case không? Không, rule chỉ tạo template rỗng, vẫn tốn công gõ chữ.
2. Các bước có đi thẳng một đường không hay phải rẽ nhánh? Có thể đi thẳng (Pipeline: Lọc -> Gen Dàn Ý -> Gen Chi Tiết).
3. Có thật sự cần Agent tự lập kế hoạch + gọi tool không? Không, input và output đã hoàn toàn xác định, không cần AI tự suy luận quy trình.
4. Nếu AI sai, ai phát hiện đầu tiên và sửa trong bao lâu? BA là người đọc bản nháp đầu tiên, có thể phát hiện lỗi logic ngay lập tức và tự gõ tay sửa trong 5-10 phút.
5. Có hạ được từ Agent → Workflow → Rule không? Hạ từ Agent xuống Workflow là vừa đẹp để cân bằng giữa tự động hóa và kiểm soát.

**Mức chọn:**

```text
[Workflow]
```

**Vì sao chọn (3-4 câu):**

```text
Bài toán đòi hỏi khả năng xử lý ngôn ngữ sáng tạo (loại bỏ Rule). Tuy nhiên quy trình viết PRD lại rất tuyến tính, các bước có thể định nghĩa tĩnh bằng prompt chain (loại bỏ Agent). Workflow là mức độ hoàn hảo để đảm bảo AI sinh văn bản chất lượng cao mà không bị mất kiểm soát hệ thống.
```

**Vì sao không chọn mức đơn giản hơn (2-3 câu):**

```text
Không chọn Rule vì rule/code cứng không thể tóm tắt meeting notes hay "hiểu" được ngữ cảnh để tự nghĩ ra các edge cases (người không có quyền hệ thống, lỗi network, v.v.).
```

### 6.2. Problem Statement v1 (v0 sửa chút hơn + 3 field cuối)

| Field | Nội dung |
|---|---|
| **Actor** | Business Analysts (BA) và Product Managers (PM) |
| **Workflow** | [Họp lấy yêu cầu] → [AI phân tách ý] → [AI Gen Draft PRD & Edge cases] → [BA Review/Edit] → [Dev] |
| **Bottleneck** | Việc phải tưởng tượng và viết vét cạn các edge cases, acceptance criteria tiêu tốn 120 phút. |
| **Impact** | Giảm tổng thời gian làm PRD từ 3.5 tiếng xuống 1 tiếng. |
| **Success Metric** | Số lượng câu hỏi clarify từ Dev giảm 50%, thời gian viết draft < 5 phút. |
| **Boundary** (làm / không làm) | AI CHỈ sinh bản nháp (text). KHÔNG tự động gửi cho dev, KHÔNG vẽ UI/UX thay designer. BA chịu hoàn toàn trách nhiệm. |
| **AI intervention point** | Can thiệp sau khi họp xong (có notes thô), và trước khi đưa cho dev review. |
| **Mức chọn** (Rule/Workflow/Agent) | **Workflow**. Chaining 3 prompt nối tiếp nhau để tạo từng phần của PRD để đảm bảo cấu trúc chặt chẽ. |
| **Rủi ro & người kiểm tra** | Rủi ro lớn nhất: AI bị "ảo giác" bịa ra logic sai nghiệp vụ. Người kiểm tra: BA bắt buộc phải đọc lại 100% bản nháp trước khi submit nội bộ. |

### 6.3. Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú (câu đầy đủ) |
|---|---|---|
| Actor + workflow rõ chưa? | Yes | BA là người dùng cuối, workflow đã vẽ cụ thể. |
| Baseline + metric đo được chưa? | Yes | Baseline là 210 phút/PRD, đo bằng đồng hồ bấm giờ. |
| Data/input đủ dùng chưa? | Yes | Meeting notes thô là text, có thể tạo giả dễ dàng. |
| AI sai, hậu quả chấp nhận được không? | Yes | Hậu quả thấp vì BA luôn duyệt lại ở bước Human Boundary. |
| Có người review/owner không? | Yes | BA là owner tuyệt đối của văn bản. |
| Có cách non-AI đơn giản hơn không? | No | Đã thử template chuẩn hóa nhưng BA vẫn lười điền. |

**Decision:**

```text
[Go]
```

**Lý do (3-4 câu dựa trên bằng chứng):**

```text
Bài toán đã thoả mãn đủ 6 tiêu chí kiểm định. Nhu cầu là có thật (BA tốn thời gian gõ chữ), dữ liệu đầu vào đã sẵn sàng (text notes), và thiết kế hệ thống đảm bảo an toàn tuyệt đối nhờ bước Human-in-the-loop (BA review). Việc sử dụng AI Workflow (Prompt Chaining) hoàn toàn khả thi về mặt kỹ thuật trong thời gian Lab.
```

**Nếu Go — pilot nhỏ nhất (data nào, chạy tay ra sao, đo 3 số nào):**

```text
Pilot:
1. Dữ liệu: Lấy 3 meeting notes thô của 3 tính năng nhỏ (Login, Reset Password, User Profile).
2. Chạy tay: Dùng Claude/ChatGPT chạy tay 3 prompt nối tiếp (Extract -> Gen Flow -> Gen Edge Case) để xem kết quả đầu ra.
3. Đo: Thời gian gen xong, Số lượng edge case hợp lý AI tìm được, Tỉ lệ text phải sửa lại bằng tay.
```

---

### Self-check nộp phần 02 (nhóm)
- [x] Có nhật ký hội tụ 9-12 → 1 (cluster + shortlist + score)
- [x] Có validation (quote thật) + research (link kiểm chứng)
- [x] Có workflow trước/sau đủ thời gian, handoff, bottleneck, boundary, fallback
- [x] Có PS v0 → v1, metric có trước/sau + cách đo, boundary có làm/không làm
- [x] Có so sánh Rule/Workflow/Agent + Decision Go/Not Yet/No-Go có lý do
