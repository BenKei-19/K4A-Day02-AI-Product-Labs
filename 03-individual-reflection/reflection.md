# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Nguyễn Quang Huy
- Mã học viên: 2A202602421
- Nhóm: Nhóm 5 người (cùng Khánh, Hiếu, Hải, Giáp)
- Candidate problem nhóm chọn: Học viên trong nhóm/lớp K4A bị thất thoát thông tin liên quan trực tiếp đến cá nhân mình (deadline, phân công) do thông tin trôi trên Discord và Zoom.

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Tự scan 7 problems từ góc độ của một BA/PM/Sinh viên năm cuối (PRD, meeting notes, feedback). | Mang đến đa dạng góc nhìn cho nhóm khi gom nhóm (clustering). |
| Pitch Problem Card | Pitch ý tưởng "AI-Assisted PRD Writer" trong 2 phút. | Bị nhóm challenge là hơi đặc thù ngành, không phải ai cũng gặp. |
| Challenge bài của bạn khác | Đặt câu hỏi cho bài "Code review" của An/Hiếu về việc context window của AI có đủ đọc hết codebase không. | Giúp nhóm nhận ra rủi ro kỹ thuật và loại bỏ bài toán Code review. |
| Gom trúng / cluster | Đề xuất gom các bài toán về tóm tắt (Zoom, Discord, Meeting notes) vào một cluster chung. | Nhóm hình thành được nhóm "Text Generation & Summarization". |
| Chọn candidate problem | Đồng ý nhượng bộ bài PRD của mình để chọn bài Discord/Zoom của Hải vì tính phổ quát. | Giúp nhóm chốt được bài toán nhanh chóng, không bị kẹt ở bước vote. |
| Validation / research | **Chủ trì phần Research**: Tìm hiểu 3 tool (Fireflies.ai, Discord Summarizer Bot, Notion AI) và check link nguồn. | Chỉ ra rằng các tool có sẵn thường quá thừa tính năng hoặc giá cao, giúp nhóm tự tin thiết kế giải pháp nội bộ. |
| Workflow nhóm | Góp ý thêm bước "Human in the loop" (người dùng tự review tóm tắt trước khi forward) vào quy trình. | Tránh rủi ro AI tóm tắt sai làm hỏng việc của cả lớp. |
| Problem Statement | Viết nháp phần Boundary (giới hạn AI làm gì và không làm gì). | Giúp PS thực tế hơn, không bị sa đà vào việc xây dựng AGI. |
| Rule / Workflow / Agent | Tranh luận bảo vệ phương án Workflow (Prompt chaining) thay vì dùng Agent tự động. | Nhóm quyết định không dùng Agent vì rủi ro mất kiểm soát khi gửi tin nhắn nhầm. |
| Decision | Cùng nhóm biểu quyết Go và vạch ra luồng Pilot nhỏ chạy tay bằng ChatGPT. | Có plan hành động cụ thể để test giả thuyết ngay trong tuần tới. |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Phần tôi đóng góp đậm nét nhất là bảng 4.2 Research các giải pháp đã có trên thị trường. Tôi đã trực tiếp search, đọc docs của các Discord Bot và rút ra takeaway quan trọng: "Cần build Workflow một chiều, không build Agent tự nhắn tin" để tránh rủi ro spam group lớp.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Gợi ý các pain point thường gặp của nghề BA/PM. | Đưa ra được khung sườn (viết PRD, feedback) rất chuẩn xác. | Đề xuất quản lý lịch họp (rất vô lý vì Google Calendar đã làm tốt). | Gạch bỏ ý tưởng quản lý lịch, tự thêm pain point về UAT test case. |
| Problem Card | Không dùng | Tự viết dựa trên kinh nghiệm thật. | | |
| Workflow | Gợi ý các bước chẻ nhỏ trong quy trình tóm tắt Zoom. | Tách được bước "Transcript" và "Diarization" (nhận diện giọng nói) rất kỹ thuật. | Bỏ quên bước human review. | Bổ sung cứng bước Human Boundary vào trước khi gửi đi. |
| Research | Hỏi Perplexity/ChatGPT tìm các tool tóm tắt Discord. | Tiết kiệm 30 phút lướt Google, lấy được danh sách tool nhanh. | AI hay đưa ra các tool đã ngừng hoạt động hoặc quá đắt. | Phải tự bấm vào từng link AI đưa để kiểm chứng giá cả và API. |
| Problem Statement | Nhờ AI gọt dũa lại v0 cho súc tích. | Rút ngắn được các câu văn lủng củng. | Xóa mất một vài context cụ thể của lớp K4A. | Thêm lại keyword "lớp K4A" và "Discord/Zoom" để sát thực tế. |
| Rule/Workflow/Agent| Dùng AI để so sánh nhanh ưu nhược điểm của Agent vs Workflow. | Phân tích rủi ro rất hệ thống. | AI hay thiên vị Agent vì nghe "ngầu" hơn. | Tôi phản bác AI và kiên quyết chọn Workflow vì bối cảnh lớp học cần an toàn. |
| Decision | Không dùng | Tự quyết định dựa trên mức độ rủi ro. | | |

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
Qua buổi thực hành hôm nay, điều tôi cảm thấy giá trị nhất là sự chuyển biến trong tư duy khi làm việc nhóm. Ban đầu, tôi khá tự tin với Problem Card "AI-Assisted PRD Writer" của mình và quyết tâm bảo vệ nó vì tính ứng dụng rất cao cho dân BA/PM. Tuy nhiên, khi nghe các bạn trình bày top 3 problems, đặc biệt là ý tưởng của Hải về việc "thất thoát thông tin deadline trên Discord và Zoom của lớp K4A", tôi đã thay đổi ý kiến hoàn toàn. Tôi nhận ra một Problem tốt không phải là cái nghe "ngầu" nhất về mặt kỹ thuật, mà là cái giải quyết đúng nỗi đau (pain point) chung mà ai trong nhóm cũng đang phải chịu đựng hàng ngày. 

Trong quá trình làm nhóm, nhóm tôi cũng từng rơi vào "bẫy solution-first" khi một bạn đề xuất làm hẳn một con Agent tự động nhảy vào các thread Discord trả lời học viên. Nhờ phần Research do tôi đảm nhiệm, tôi đã chứng minh được rằng việc thả rông Agent có thể gây spam hoặc trả lời sai lệch thông báo quan trọng của giảng viên. Từ đó, tôi in đậm dấu tay của mình vào bài bằng cách chốt cứng Boundary: "AI chỉ sinh bản tóm tắt nháp (Draft), bắt buộc phải có một lớp trưởng/facilitator đọc lại trước khi chốt gửi lên channel chung". Điều khó nhất khi viết Problem Statement chính là việc kìm hãm sự hưng phấn của nhóm lại để vạch ra Boundary này, đảm bảo dự án khả thi trong nguồn lực giới hạn.
```

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1)
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [x] [15đ] Nhóm có workflow trước/sau
- [x] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ
- [x] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [x] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI
