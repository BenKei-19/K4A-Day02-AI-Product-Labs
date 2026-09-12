# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: *(điền tên bạn)*
- Mã học viên: *(điền mã)*
- Nhóm: *(điền tên/số nhóm)*
- Candidate problem nhóm chọn: Tổng hợp Progress Report đồ án nhóm từ nhiều nguồn (Trello/GitHub/chat)

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Scan 8 problems từ trải nghiệm làm nhóm trưởng đồ án + admin CLB + ôn thi, sử dụng cả 4 lăng kính | Nhóm có thêm nhiều candidate ở mảng quản lý nhóm + học tập, đa dạng hơn so với chỉ nhìn từ góc dev |
| Pitch Problem Card | Pitch Card #1 (Progress Report) với workflow 6 bước, metric 70 phút → 22 phút, giải thích bottleneck ở bước tổng hợp + viết nhận xét | Card được đưa vào shortlist vì workflow rõ ràng và có baseline thời gian cụ thể |
| Challenge bài của bạn khác | Hỏi bạn A về card "auto-debug code": "Nếu AI debug sai thì ai phát hiện? Sinh viên mới có đủ trình kiểm tra AI không?" | Bạn A nhận ra card thiếu fallback plan và boundary rõ ràng, sau đó bổ sung thêm field boundary |
| Gom trùng / cluster | Gom 3 bài liên quan đến "tổng hợp thông tin từ nhiều nguồn" (progress report, meeting notes, ôn thi) vào 1 cluster | Nhóm thấy pattern chung: pain nằm ở việc biến dữ liệu rời rạc thành narrative mạch lạc |
| Chọn candidate problem | Đề xuất chọn Progress Report vì có workflow + metric rõ nhất trong cluster, và tất cả nhóm viên đều trải nghiệm qua (không cần domain expert bên ngoài) | Nhóm đồng thuận 3/4 phiếu chọn Progress Report; 1 bạn muốn chọn Ôn thi nhưng chấp nhận vì metric khó đo hơn |
| Validation / research | Hỏi nhanh 2 nhóm trưởng khác trong lớp: "Mỗi tuần bạn mất bao lâu viết báo cáo?" — cả 2 confirm 45-90 phút. Research Notion AI, GitHub Copilot Workspace, Trello Power-Ups | Nhóm xác nhận pain thật; research cho thấy chưa tool nào giải quyết đúng bài toán "gom Trello + GitHub + chat → narrative" |
| Workflow nhóm | Vẽ bản current workflow chi tiết 6 bước với thời gian từng bước, đề xuất future workflow 5 bước | Nhóm dùng workflow tôi vẽ làm base, thêm chi tiết actor/input/output |
| Problem Statement | Viết draft PS v0, đặc biệt phần boundary: "AI không tự nộp report, không bịa số liệu commit/task" | Nhóm giữ nguyên boundary tôi đề xuất, thêm 1 boundary nữa: "không thay nhóm trưởng đánh giá hiệu suất thành viên" |
| Rule / Workflow / Agent | Lập luận rằng Workflow đủ vì các bước tuyến tính rõ ràng, chưa cần Agent vì không cần AI tự lập kế hoạch hay gọi API động | Nhóm chốt chọn Workflow; loại Agent vì scope quá rộng cho lab |
| Decision | Tổng hợp checklist Go/Not Yet/No-Go, điền 6 câu hỏi quyết định | Nhóm chốt Go với scope nhỏ: pilot với data mẫu 2 tuần report gần nhất |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Phần workflow before/after là do tôi vẽ bản đầu tiên và nhóm chỉnh sửa thêm. Phần boundary trong Problem Statement ("AI không tự nộp report, không bịa số liệu") cũng là tôi đề xuất vì tôi từng bị giảng viên hỏi lại số liệu trong report cũ.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Hỏi gợi ý thêm problems sau khi tự scan 5 ý | Gợi ý problem FAQ CLB — đúng pain thật vì tôi là admin Discord | Gợi ý "chatbot tư vấn chọn môn" — quá rộng, không có workflow cụ thể | Bỏ 2 ý quá rộng, chỉ giữ 1 ý có trải nghiệm thật |
| Problem Card | Nhờ AI phản biện Card #1 | Chỉ ra metric "số lần bị hỏi lại" chưa có baseline | AI đề xuất thêm "sentiment analysis cho report" — không cần thiết cho bài toán này | Thêm baseline cụ thể: 1-2 lần bị hỏi lại/report trong 3 tuần gần nhất |
| Workflow | Nhờ AI chuyển mô tả workflow thành dạng cấu trúc rõ ràng hơn | Giúp format nhanh, nhắc thêm cột "human boundary" và "fallback" mà tôi suýt quên | AI gộp bước "tổng hợp" và "viết nhận xét" thành 1 bước | Tách lại vì bottleneck nằm ở "viết nhận xét" chứ không phải "tổng hợp data" |
| Research | Tìm tool/pattern tương tự | Gợi ý Notion AI, Trello Power-Ups, GitHub Actions summary | Có claim "Notion AI giảm 60% thời gian báo cáo" không có nguồn rõ | Chỉ giữ link chính thức, bỏ số liệu không verify được |
| Problem Statement | Nhờ AI phản biện PS v0 | Chỉ ra field "Impact" nên tách rõ impact cho nhóm trưởng vs impact cho giảng viên | AI đề xuất metric "NPS score từ giảng viên" — không thực tế trong bối cảnh đồ án | Giữ metric đơn giản: thời gian + số lần bị hỏi lại |
| Rule / Workflow / Agent | Không dùng | Không dùng vì phần này cần nhóm tự thảo luận và lập luận | — | — |
| Decision | Không dùng | Không dùng vì quyết định Go/Not Yet/No-Go phải từ nhận định thật của nhóm | — | — |

> Nếu phase nào không dùng AI, ghi `Không dùng` và vì sao tự làm.

---

## 3. Reflection câu hỏi mở

Chọn 3-4 câu trong 6 câu dưới để viết thành đoạn 8-12 câu (không trả lời bullet 1 dòng):
- Tôi học được gì khi nghe top 3 problems của các bạn khác?
- Nhóm có lúc nào bị solution-first, đòi làm Agent cho ngầu không?
- Tôi có thay đổi ý kiến sau khi bị challenge không, vì sao đổi?
- Tôi đóng góp gì thật sự vào artifact cuối, phần nào có dấu tay của tôi?
- Điều khó nhất khi viết Problem Statement là gì, metric hay boundary?
- Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

**Reflection:**

```text
Khi nghe top 3 problems của các bạn khác, tôi nhận ra rằng mình hay bị "ngồi trong bong bóng" — chỉ nhìn problem từ góc nhóm trưởng mà quên nhìn từ góc người review code hay người dùng sản phẩm. Có bạn trong nhóm đưa ra problem về việc debug code mất cả buổi chiều, tôi ban đầu nghĩ đó là pain cá nhân, nhưng khi bạn ấy chỉ ra rằng 4/5 thành viên đều gặp và có log chat hỏi nhau thì tôi thấy mình đã đánh giá thấp problem đó.

Nhóm tôi có lúc bị solution-first khi một bạn đề xuất ngay "dùng Agent auto gửi report cho giảng viên". Lúc đó tôi challenge lại: "Agent tự gửi mà sai số liệu thì sao? Giảng viên hỏi lại ai chịu?" — câu hỏi đó giúp nhóm dừng lại và quay về vẽ workflow trước. Cuối cùng nhóm chọn Workflow thay vì Agent, và tôi thấy quyết định đó đúng vì workflow tuyến tính, chưa cần AI tự lập kế hoạch.

Tôi cũng thay đổi ý kiến ở phần metric. Ban đầu tôi chỉ đặt metric "giảm thời gian", nhưng khi bạn B challenge "giảm thời gian mà report tệ hơn thì có ý nghĩa gì?", tôi thêm metric phụ "không tăng số lần giảng viên yêu cầu bổ sung". Đó là lần tôi thấy rõ nhất giá trị của việc bị challenge — nó không phải để phủ nhận mà để làm bài chặt chẽ hơn.

Điều khó nhất khi viết Problem Statement là boundary. Viết actor, workflow, metric thì dựa vào trải nghiệm thật, nhưng boundary phải tưởng tượng ra "nếu AI làm quá thì sao" — một thứ mình chưa trải qua. Tôi mất 10 phút mới nghĩ ra "AI không tự nộp report" vì ban đầu tôi thấy đó là chuyện đương nhiên, nhưng khi viết ra mới thấy nếu không ghi rõ thì scope dễ bị trượt.

Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở phần validation: nhóm chỉ hỏi 2 người, con số quá nhỏ để confirm pain. Tôi nên đề xuất làm survey nhanh trên Discord lớp với 15-20 người để có baseline tin cậy hơn trước khi chốt Go.
```

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1)
- [ ] Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [ ] [15đ] Nhóm có workflow trước/sau
- [ ] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ
- [ ] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [ ] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI
