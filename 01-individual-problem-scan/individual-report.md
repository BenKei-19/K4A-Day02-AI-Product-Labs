# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Nguyễn Quang Huy
- Mã học viên: 2A202602421
- Vai trò / bối cảnh (VD: sinh viên năm X, intern PM, ...): Sinh viên năm cuối CMC, đang làm BA / Product Manager
- Công việc hàng tuần (3-5 gạch đầu dòng để soi problem):
  - Thu thập và phân tích yêu cầu từ stakeholders (khách hàng, team dev)
  - Viết tài liệu đặc tả (PRD / User Stories / Wireframe)
  - Quản lý backlog và ưu tiên tính năng trên Jira
  - Họp sync hàng tuần với dev team và báo cáo tiến độ cho quản lý
  - Kiểm tra UAT (User Acceptance Testing) trước khi release

---

## Phase 1 — Scan 5+ problems (tối thiểu 5, khuyến khích 8-10)

**Cách điền:** mỗi dòng = việc gì + ai chịu + đo bằng gì. Cột `Dấu hiệu thật` bắt buộc có số: mất bao lâu (bấm giờ mấy lần), mấy lần/tuần, bao nhiêu người gặp, log/ticket/quote nào.

| # | Lăng kính (Lặp lại / Tốn thời gian / AI có thể tốt hơn / Pain từ người khác) | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật (số + bằng chứng) |
|---|---|---|---|---|
| 1 | Tốn thời gian | Viết PRD (Product Requirements Document) cho mỗi tính năng mới, phải mô tả chi tiết flow, edge case, acceptance criteria | BA / PM | Mất 3-5h cho mỗi PRD, trung bình 2 PRD/tuần, hay bị dev hỏi lại vì thiếu edge case |
| 2 | Lặp lại | Tổng hợp meeting notes sau mỗi buổi họp với stakeholder rồi gửi email recap | BA / PM | Mất 30-45 phút sau mỗi buổi họp, 3-4 buổi/tuần, đôi khi quên ghi action item |
| 3 | Pain từ người khác | Dev team thường xuyên hỏi lại yêu cầu vì User Story viết chưa rõ ràng, gây block sprint | Dev team / BA | 5-7 câu hỏi clarify/tuần trên Slack, mỗi lần mất 15-30 phút qua lại |
| 4 | AI có thể tốt hơn | Phân tích feedback từ khách hàng (email, survey, chat log) để tìm ra pain point chung | PM / BA | Mất 2h/tuần đọc 50-80 feedback, hay bỏ sót pattern vì quá nhiều data |
| 5 | Lặp lại | Cập nhật status report hàng tuần cho quản lý: tổng hợp tiến độ từ Jira, highlight risk, đề xuất next steps | PM / Project Manager | Mất 1h mỗi thứ Sáu, copy-paste số liệu từ Jira sang slide, format lại cho đẹp |
| 6 | Tốn thời gian | So sánh và benchmark tính năng với đối thủ cạnh tranh khi làm competitive analysis | PM | Mất 3-4h mỗi lần cần ra quyết định tính năng mới, phải vào từng app đối thủ screenshot và ghi chú |
| 7 | Lặp lại | Viết test case cho UAT dựa trên acceptance criteria trong User Story | BA / QA | Mất 1-2h cho mỗi feature, format giống nhau nhưng phải viết lại từ đầu mỗi lần |

> Gợi ý tự soi: tuần trước mất nhiều thời gian nhất vào việc gì? Việc gì hay trì hoãn? Người khác hay hỏi lại câu gì? Workflow nào ai cũng biết là chậm?

**AI đã dùng ở Phase 1 (nếu có):**
- Prompt đã hỏi: "Là một BA/PM, liệt kê các công việc lặp đi lặp lại hàng tuần mà tôi hay mất thời gian nhất"
- Ý dùng được: Tổng hợp meeting notes và phân tích customer feedback.
- Ý bỏ vì không phải pain thật: "Quản lý lịch họp" — vì Google Calendar đã giải quyết tốt rồi, không cần LLM.

**Self-check Phase 1:**
- [x] Đã 5+ dòng, mỗi dòng có actor + số đo cụ thể
- [x] Dùng ít nhất 3/4 lăng kính
- [x] Không có dòng chung chung kiểu "mất nhiều thời gian"

---

## Phase 2 — Top 3 Problem Cards

### 2.1. Chọn top 3

Giữ bài nào: actor cụ thể, workflow vẽ được 3-7 bước, bottleneck ở 1 bước, impact đo được. Loại bài quá rộng.

| Rank | Problem (copy từ bảng scan) | Vì sao chọn (2-3 ý) | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Viết PRD cho mỗi tính năng mới | Tốn thời gian nhất (3-5h), workflow rõ ràng, AI rất giỏi sinh văn bản có cấu trúc | AI có hiểu đúng business context đặc thù của dự án không |
| 2 | Tổng hợp meeting notes sau buổi họp stakeholder | Lặp lại 3-4 lần/tuần, đầu vào là text/audio dễ xử lý, impact rõ ràng | Độ chính xác khi ghi nhận tên người và action item |
| 3 | Phân tích feedback khách hàng để tìm pain point | Data đầu vào lớn (50-80 feedback/tuần), AI phân loại và clustering tốt hơn người | AI có bỏ sót feedback tinh tế (sarcasm, ngữ cảnh văn hóa) không |

### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

#### Problem Card #1 — [AI-Assisted PRD Writer]

```text
Problem 1 câu: BA/PM mất 3-5 tiếng viết một bản PRD chi tiết cho mỗi tính năng mới, trong khi cấu trúc PRD gần như giống nhau mỗi lần.

Actor: BA / Product Manager

Thời điểm / bối cảnh: Đầu mỗi Sprint khi có tính năng mới cần triển khai, phải giao PRD cho dev trước Sprint Planning.

Current workflow 3-7 bước:
1. Họp với stakeholder để hiểu yêu cầu (đã có sẵn meeting notes).
2. Tạo file PRD mới, copy template cũ.
3. Viết mô tả tính năng, user flow, và business logic.
4. Liệt kê edge cases và acceptance criteria.
5. Vẽ wireframe hoặc mockup đơn giản.
6. Gửi cho dev review, nhận feedback, sửa lại 1-2 vòng.

Bottleneck: Bước 3 và 4 — Viết chi tiết flow và liệt kê edge case rất tốn thời gian vì phải tưởng tượng ra mọi tình huống.

Impact: Giảm từ 3-5h xuống còn 1h cho mỗi PRD, giảm số lần dev hỏi lại vì thiếu thông tin.

Success metric: Thời gian viết PRD < 1.5h, số câu hỏi clarify từ dev giảm 50%.

Non-AI alternative: Xây dựng bộ template PRD chi tiết hơn với checklist edge case sẵn.

AI hypothesis: LLM có thể nhận đầu vào là meeting notes + mô tả ngắn về tính năng, sau đó tự sinh ra bản nháp PRD hoàn chỉnh bao gồm user flow, edge cases và acceptance criteria theo đúng template công ty.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #1** (ASCII / Mermaid / ảnh đính kèm):

```text
CURRENT STATE — 240 phút

[1 Họp stakeholder: 30'] → [2 Copy template: 10'] → [3 Viết flow + logic: 90'] → [4 Liệt kê edge case: 60'] → [5 Wireframe: 30'] → [6 Review & sửa: 20']  <-- bottleneck (bước 3,4)

FUTURE STATE — 60 phút

[1 Họp stakeholder: 30'] → [2 AI sinh draft PRD từ notes: 5'] → [3 Human review & bổ sung context: 20'] → [4 Wireframe: 5']  <-- human boundary

Fallback: nếu AI sinh PRD sai logic nghiệp vụ, BA tự sửa lại phần flow và giữ nguyên phần edge case AI đã gợi ý.
```

File đính kèm (nếu vẽ riêng): `01-individual-problem-scan-workflow-card-1.png`

---

#### Problem Card #2 — [Meeting Notes Auto-Summarizer]

```text
Problem 1 câu: Sau mỗi buổi họp stakeholder, BA/PM mất 30-45 phút để tổng hợp lại nội dung, trích xuất action items và gửi email recap cho mọi người.

Actor: BA / Product Manager

Thời điểm / bối cảnh: Ngay sau mỗi buổi họp với stakeholder hoặc dev team (3-4 buổi/tuần).

Current workflow 3-7 bước:
1. Vừa họp vừa gõ note thô trên Google Docs.
2. Kết thúc họp, đọc lại note và bổ sung phần bị sót.
3. Phân loại nội dung: quyết định, thảo luận mở, action items.
4. Gán action item cho đúng người + deadline.
5. Format thành email recap và gửi cho tất cả attendees.

Bottleneck: Bước 2 và 3 — Phải nhớ lại ngữ cảnh cuộc họp để bổ sung note, rồi phân loại nội dung rất tốn não.

Impact: Tiết kiệm 30-45 phút sau mỗi buổi họp (tổng 2-3h/tuần), action items không bị sót.

Success metric: Thời gian ra email recap < 10 phút, tỷ lệ sót action item = 0%.

Non-AI alternative: Cử 1 người chuyên làm thư ký cuộc họp (note-taker).

AI hypothesis: LLM nhận transcript cuộc họp (từ recording hoặc note thô), tự động phân loại thành "Quyết định / Thảo luận mở / Action Items" và format thành email recap sẵn sàng gửi.

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

[1 Họp + gõ note thô: 0'] → [2 Đọc lại + bổ sung: 15'] → [3 Phân loại nội dung: 15'] → [4 Gán action items: 10'] → [5 Format email + gửi: 5']  <-- bottleneck (bước 2,3)

FUTURE STATE — 10 phút

[1 Họp + Auto Record/Note] → [2 AI phân loại + gen email recap: 2'] → [3 Human review + gửi: 8']  <-- human boundary

Fallback: Nếu AI gán sai tên người cho action item, BA tự sửa tên trước khi gửi email.
```

File đính kèm: `01-individual-problem-scan-workflow-card-2.png`

---

#### Problem Card #3 — [Customer Feedback Analyzer]

```text
Problem 1 câu: PM/BA mất 2h/tuần để đọc 50-80 feedback từ nhiều kênh (email, survey, chat) và thường bỏ sót pattern quan trọng vì quá nhiều data.

Actor: Product Manager / BA

Thời điểm / bối cảnh: Cuối mỗi tuần, khi cần tổng hợp insight từ feedback khách hàng để đưa vào Sprint Planning.

Current workflow 3-7 bước:
1. Export feedback từ các kênh (Zendesk, Google Forms, Slack).
2. Đọc từng feedback một, ghi chú keyword.
3. Phân loại thủ công theo chủ đề (UX, Performance, Feature Request, Bug).
4. Đếm tần suất từng chủ đề, xếp hạng ưu tiên.
5. Viết báo cáo insight gửi cho team.

Bottleneck: Bước 2 và 3 — Đọc từng feedback và phân loại thủ công rất chậm, dễ bỏ sót feedback tinh tế.

Impact: Giảm thời gian phân tích từ 2h xuống 20 phút, phát hiện được pattern mà người khó thấy.

Success metric: Thời gian phân tích < 30 phút, phát hiện 100% chủ đề có tần suất > 5 lần.

Non-AI alternative: Dùng Google Sheets + filter thủ công theo keyword.

AI hypothesis: LLM đọc toàn bộ feedback, tự phân loại theo chủ đề, đếm tần suất, highlight sentiment (tích cực/tiêu cực) và sinh báo cáo insight tóm tắt.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #3:**

```text
CURRENT STATE — 120 phút

[1 Export feedback: 10'] → [2 Đọc từng cái: 50'] → [3 Phân loại thủ công: 40'] → [4 Đếm + xếp hạng: 10'] → [5 Viết báo cáo: 10']  <-- bottleneck (bước 2,3)

FUTURE STATE — 20 phút

[1 Export feedback: 10'] → [2 AI phân loại + clustering + sentiment: 3'] → [3 Human review insight: 7']  <-- human boundary

Fallback: Nếu AI phân loại sai chủ đề, PM dùng filter trong sheet để kiểm tra lại nhóm đó.
```

File đính kèm: `01-individual-problem-scan-workflow-card-3.png`

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card tôi muốn pitch nhất:**

```text
Problem Card #1 — AI-Assisted PRD Writer
```

**Vì sao (2-3 câu: workflow gì, số đo gì, impact gì):**

```text
Viết PRD là công việc tốn thời gian nhất của BA/PM mỗi tuần (3-5h/bản, 2 bản/tuần). Đầu vào (meeting notes + mô tả ngắn) hoàn toàn là text có cấu trúc, rất phù hợp để LLM xử lý. Impact trực tiếp: giảm 70% thời gian viết PRD, đồng thời giảm số lần dev phải hỏi lại vì thiếu edge case — giúp Sprint chạy mượt hơn.
```

**Câu hỏi tôi muốn nhóm challenge (1-2 câu hỏi đáng chú ý):**

```text
1. Làm sao để AI hiểu đúng business context đặc thù của dự án mà không cần giải thích lại mỗi lần?
2. Nếu AI sinh ra edge case sai hoặc thiếu, liệu dev có tin tưởng PRD đó không?
```

**AI phản biện Card (nếu có):**
- Điểm yếu AI chỉ ra: AI không có domain knowledge sâu, có thể sinh ra acceptance criteria "đúng format nhưng sai nghiệp vụ". Nếu BA không review kỹ, dev sẽ code sai theo PRD sai.
- Tôi sửa gì: Thêm bước "Domain context injection" — feed cho AI các PRD cũ đã được approve làm few-shot examples, giúp AI học được ngôn ngữ và logic nghiệp vụ riêng của dự án.

### Self-check nộp phần 01
- [x] Có 5+ problems + top 3 Cards đã field
- [x] Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [x] Đã chọn 1 card pitch + câu hỏi challenge
