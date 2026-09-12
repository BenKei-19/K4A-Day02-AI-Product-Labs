# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Nguyễn Quang Huy
- Mã học viên: 2A202602421
- Vai trò / bối cảnh (VD: sinh viên năm X, intern PM, ...): Sinh viên năm cuối CMC
- Công việc hàng tuần (3-5 gạch đầu dòng để soi problem):
  - Review Code (Pull Requests) cho team
  - Viết unit tests cho các tính năng mới
  - Tham gia họp Weekly Sync và Sprint Planning
  - Soạn thảo Release Notes cuối mỗi Sprint

---

## Phase 1 — Scan 5+ problems (tối thiểu 5, khuyến khích 8-10)

**Cách điền:** mỗi dòng = việc gì + ai chịu + đo bằng gì. Cột `Dấu hiệu thật` bắt buộc có số: mất bao lâu (bấm giờ mấy lần), mấy lần/tuần, bao nhiêu người gặp, log/ticket/quote nào.

| # | Lăng kính (Lặp lại / Tốn thời gian / AI có thể tốt hơn / Pain từ người khác) | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật (số + bằng chứng) |
|---|---|---|---|---|
| 1 | Lặp lại | Viết boilerplate unit tests cho các API endpoints cơ bản | Dev team | Mất 2-3h/tuần cho mỗi dev, ticket ghi nhận thiếu test coverage thường xuyên xuất hiện |
| 2 | Tốn thời gian | Tổng hợp Release Notes từ 20-30 PRs cuối mỗi Sprint | Tech Lead / PM | Mất 1.5h mỗi cuối Sprint, hay bị sót các fix nhỏ, team 5 người chờ đợi để deploy |
| 3 | Lặp lại | Giải thích lại các logic cũ trong codebase cho Fresher mới vào | Senior Dev / Tech Lead | Mất 3h/tuần, lặp lại cùng câu hỏi 3-4 lần/tháng trên Slack |
| 4 | AI có thể tốt hơn | Format và kiểm tra lỗi cú pháp các file JSON/YAML config nhiều môi trường | DevOps / Dev | Mất 1h/tuần, lỗi typo YAML gây fail CI pipeline (3 lần/tháng) |
| 5 | Tốn thời gian | Tóm tắt 60 phút họp Weekly Sync thành các Action Items phân công rõ ràng | Tech Lead / Scrum Master | Mất 30-45 phút sau mỗi cuộc họp, 2 lần/tuần, đôi khi quên tag tên người phụ trách |

> Gợi ý tự soi: tuần trước mất nhiều thời gian nhất vào việc gì? Việc gì hay trì hoãn? Người khác hay hỏi lại câu gì? Workflow nào ai cũng biết là chậm?

**AI đã dùng ở Phase 1 (nếu có):**
- Prompt đã hỏi: "Đóng vai một Tech Lead, liệt kê 5 công việc lặp đi lặp lại nhiều nhất gây lãng phí thời gian của team development"
- Ý dùng được: Tổng hợp Release Notes và Viết boilerplate code.
- Ý bỏ vì không phải pain thật: Theo dõi bug trên JIRA (đã có tool tự động khá tốt, không cần LLM).

**Self-check Phase 1:**
- [x] Đã 5+ dòng, mỗi dòng có actor + số đo cụ thể
- [x] Dùng ít nhất 3/4 lăng kính
- [x] Không có dòng chung chung kiểu "mất nhiều thời gian"

---

## Phase 2 — Top 3 Problem Cards

### 2.1. Chọn top 3

| Rank | Problem (copy từ bảng scan) | Vì sao chọn (2-3 ý) | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Tổng hợp Release Notes từ 20-30 PRs cuối mỗi Sprint | Impact rõ ràng, quy trình gom data từ Github dễ làm API, tiết kiệm 1.5h | Format đầu ra của AI có chuẩn markdown công ty không |
| 2 | Tóm tắt 60 phút họp Weekly Sync thành Action Items | Đau đầu mỗi tuần, data đầu vào là audio transcript dễ có sẵn | Độ chính xác khi nhận diện giọng nói (speaker diarization) |
| 3 | Viết boilerplate unit tests cho các API endpoints cơ bản | Dev rất ghét viết test, AI gen code rất tốt, tăng coverage | AI có hiểu hết mock/stub nội bộ của codebase không |

### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

#### Problem Card #1 — [Auto Release Notes Generator]

```text
Problem 1 câu: Mất quá nhiều thời gian duyệt lại hàng chục PRs để viết Changelog/Release Notes mỗi khi release.

Actor: Tech Lead / Product Manager

Thời điểm / bối cảnh: Cuối Sprint (mỗi 2 tuần), trước khi merge code lên production.

Current workflow 3-7 bước:
1. Mở danh sách các PRs đã merge trong Sprint.
2. Đọc tiêu đề và description của từng PR.
3. Phân loại PR (Feature, Bugfix, Tech Debt).
4. Viết lại nội dung bằng ngôn ngữ dễ hiểu cho người dùng cuối.
5. Review và paste vào kênh Slack thông báo release.

Bottleneck: Bước 2 và 4 (Đọc hiểu code/PR và dịch sang ngôn ngữ con người).

Impact: Giảm 1.5 tiếng làm việc nhàm chán xuống còn 10 phút, tránh bỏ sót thay đổi.

Success metric: Thời gian hoàn thành Release Notes < 15 phút, tỷ lệ phải sửa tay < 20% số dòng.

Non-AI alternative: Bắt buộc mọi Dev phải tự viết 1 dòng Release Note chuẩn khi tạo PR.

AI hypothesis: LLM có thể đọc metadata (Title, Description, File changes) từ Github API của các PRs và tự động phân loại, tóm tắt nội dung chính.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #1** (ASCII / Mermaid / ảnh đính kèm):

```text
CURRENT STATE — 90 phút

[1 Lọc PRs: 10'] -> [2 Đọc hiểu từng PR: 40'] -> [3 Viết tóm tắt: 30'] -> [4 Gửi Slack: 10']  <-- bottleneck (bước 2,3)

FUTURE STATE — 15 phút

[1 AI fetch PRs + Gen Draft: 5'] -> [2 Human review & edit: 10'] -> [3 Gửi Slack]  <-- human boundary

Fallback: nếu AI phân loại sai, người dùng tự kéo thả thẻ tính năng vào đúng mục trong bảng nháp.
```

---

#### Problem Card #2 — [Meeting Action Item Extractor]

```text
Problem 1 câu: Mất nhiều thời gian nghe lại/nhớ lại nội dung họp để giao task và tóm tắt biên bản.

Actor: Scrum Master / Tech Lead

Thời điểm / bối cảnh: Ngay sau cuộc họp Weekly Sync 60 phút.

Current workflow 3-7 bước:
1. Vừa họp vừa gõ note thô.
2. Cuộc họp kết thúc, ngồi lọc lại note.
3. Tìm xem ai hứa làm gì để tạo Action Items.
4. Gửi email/Slack cho team chốt lại.

Bottleneck: Bước 2 và 3 (Rất tốn não để nhớ lại context và không bị sót người).

Impact: Tiết kiệm 45 phút sau mỗi cuộc họp, action items rõ ràng không cãi nhau.

Success metric: Tỷ lệ sót Action Item = 0, thời gian ra biên bản < 10 phút.

Non-AI alternative: Cử 1 người chuyên làm thư ký cuộc họp.

AI hypothesis: LLM nhận audio transcript, trích xuất chính xác các câu lệnh "Ai - Làm gì - Bao giờ xong" và format thành Todo list.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #2:**

```text
CURRENT STATE — 45 phút

[1 Họp + Note thô] -> [2 Lọc note: 20'] -> [3 Gán task: 15'] -> [4 Gửi Slack: 10']  <-- bottleneck

FUTURE STATE — 10 phút

[1 Họp + Auto Record] -> [2 AI Gen Transcript & Tasks: 2'] -> [3 Human review: 8']  <-- human boundary

Fallback: Nếu AI sai tên người, manual tag lại tên trên Slack.
```

---

#### Problem Card #3 — [Boilerplate Unit Test Generator]

```text
Problem 1 câu: Tốn thời gian viết các bài test lặp đi lặp lại cho các API CRUD cơ bản.

Actor: Software Engineer

Thời điểm / bối cảnh: Khi hoàn thành logic code, cần viết test để đạt đủ coverage merge code.

Current workflow 3-7 bước:
1. Tạo file test mới.
2. Import thư viện và mock data.
3. Setup các case (Success, Failed, Not Found).
4. Assert kết quả trả về.
5. Chạy test và debug.

Bottleneck: Bước 2 và 3 (Copy-paste và sửa tham số rất tẻ nhạt).

Impact: Giảm 2-3h/tuần, coverage code tăng nhanh giúp hệ thống ổn định hơn.

Success metric: Tỷ lệ code sinh ra chạy pass ngay lập tức > 70%.

Non-AI alternative: Tạo sẵn các file template (snippets) trong IDE.

AI hypothesis: LLM có thể đọc file source code của API, hiểu context, và sinh ra file Unit Test đầy đủ các edge cases cơ bản.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #3:**

```text
CURRENT STATE — 180 phút (nhiều files)

[1 Viết logic] -> [2 Copy template test: 20'] -> [3 Viết 5 cases: 100'] -> [4 Debug: 60']  <-- bottleneck

FUTURE STATE — 60 phút

[1 Viết logic] -> [2 AI Gen Test file: 5'] -> [3 Human review & Debug: 55']  <-- human boundary

Fallback: Nếu code AI fail chạy không lên, Dev tự xóa đi và dùng template snippet.
```

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card tôi muốn pitch nhất:**

```text
Problem Card #1 — Auto Release Notes Generator
```

**Vì sao (2-3 câu: workflow gì, số đo gì, impact gì):**

```text
Workflow gom nhóm và dịch PR technical sang Release Note kinh doanh là một pain point có thật ở mọi team tech. Đầu vào (Github PRs) cực kỳ chuẩn chỉnh bằng text, dễ tích hợp AI mà không cần lo xử lý audio hay context phức tạp. Impact là tiết kiệm được ngay 1.5 tiếng lao động tẻ nhạt mỗi 2 tuần, giải phóng Tech Lead.
```

**Câu hỏi tôi muốn nhóm challenge (1-2 câu hỏi đáng chú ý):**

```text
1. Làm sao để AI hiểu được những ticket quá vắn tắt (Dev chỉ ghi "Fix bug")?
2. AI có thể sinh ra giọng điệu hóm hỉnh theo đúng văn hóa công ty không?
```

**AI phản biện Card (nếu có):**
- Điểm yếu AI chỉ ra: AI phụ thuộc hoàn toàn vào chất lượng mô tả PR của Dev. Nếu Dev lười viết mô tả, AI sẽ "nhai rác, nhả rác".
- Tôi sửa gì: Đưa "Non-AI alternative" thành quy trình bắt buộc: Thiết lập PR Template bắt buộc Dev phải điền mục `Summary` trước khi merge, để đảm bảo AI có đủ data.

### Self-check nộp phần 01
- [x] Có 5+ problems + top 3 Cards đã field
- [x] Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [x] Đã chọn 1 card pitch + câu hỏi challenge
