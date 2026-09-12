# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Dương Đức Vương
- Mã học viên: 2A202602944
- Nhóm: Thần giao cách cảm - Zone A
- Candidate problem nhóm chọn: Hỗ trợ phân loại và định tuyến ticket phản ánh cư dân bằng AI, với CSKH review trước khi chuyển đến BQL phù hợp.

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Tôi tự scan 10 problem từ bối cảnh tìm việc, tự học, công việc tự do và việc qua cửa VinUni. | Nhóm có thêm các candidate có actor, tần suất và cách đo cụ thể; bài tắc nghẽn cửa VinUni được dùng để pitch. |
| Pitch Problem Card | Tôi pitch Card #1 về hàng chờ tại cửa VinUni giờ cao điểm, kèm các khung giờ cần đo, metric và phương án non-AI. | Nhóm thấy tôi ưu tiên kiểm tra bottleneck và giải pháp vận hành trước khi dùng AI. |
| Challenge bài của bạn khác | Tôi đặt câu hỏi liệu 200 ticket/ngày và 8 phút/ticket đã có log chưa, và nhắc kiểm tra ticket multi-intent. | Các số liệu được ghi rõ là hypothesis; phạm vi được giới hạn vào pilot và ticket một intent. |
| Gom trùng / cluster | Tôi cùng nhóm gom các bài thành nhóm tổng hợp tri thức, triage/routing và tóm tắt vận hành. | Nhóm nhìn được pattern chung là đọc thông tin không cấu trúc rồi chuyển thành output có cấu trúc. |
| Chọn candidate problem | Tôi tham gia so sánh ticket routing với tổng hợp task và xử lý sự cố pin theo actor, workflow, evidence, impact và khả năng làm trong lab. | Nhóm chọn ticket routing vì có workflow và metric rõ hơn, dù vẫn cần validation thêm. |
| Validation / research | Tôi phụ trách điều phối validation và giữ quan điểm rằng chưa có interview, survey hoặc log ticket thì chưa nên kết luận pain đã được xác minh. | Báo cáo bổ sung phần tín hiệu xác nhận/phản bác, dữ liệu còn thiếu và điều kiện để chuyển sang Go. |
| Workflow nhóm | Tôi rà lại các bước nhận ticket, đọc, phân loại, chọn BQL và chuyển tiếp; chú ý fallback khi AI sai. | Workflow tương lai có Rule kiểm tra input, AI gợi ý, CSKH review và hàng đợi thủ công. |
| Problem Statement | Tôi góp ý tách số liệu ước tính khỏi baseline đã xác minh và làm rõ boundary của AI. | PS v1 có metric median time, accuracy, tỷ lệ sửa, fallback và không tự route khi confidence thấp. |
| Rule / Workflow / Agent | Tôi tham gia phản biện việc dùng Agent cho bài toán triage và đề xuất giữ Rule làm baseline/fallback. | Nhóm chọn Workflow vì luồng cố định, có schema, confidence threshold, human review và audit log. |
| Decision | Tôi đồng thuận với quyết định `Not Yet` vì data/input và baseline chưa đủ, dù workflow và boundary đã rõ. | Nhóm có điều kiện cụ thể trước pilot: ticket ẩn danh, taxonomy, danh bạ BQL và đo baseline. |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Tôi để lại dấu tay rõ nhất ở phần validation và boundary: các số 200 ticket/ngày, 8 phút/ticket và mục tiêu route đúng 92% đều được ghi là giả thuyết cần kiểm chứng. Tôi cũng giúp nhóm giữ quyết định cuối ở mức Not Yet, thay vì vội xem prototype là bằng chứng bài toán đã đúng.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Không dùng; tôi tự scan trước từ trải nghiệm thật. | Tôi tự nhận ra các việc lặp lại và ghi được actor, tần suất, thời gian. | Nếu dùng AI ngay, danh sách có thể rộng nhưng không phải pain tôi từng gặp. | Tôi giữ lại 10 candidate có dấu hiệu cần đo và loại cách mô tả quá chung. |
| Problem Card | Dùng để gợi ý câu hỏi tự phản biện sau khi tự viết card. | Giúp soi baseline, rủi ro và ranh giới quyền ra vào trong card cửa VinUni. | AI có thể nhảy nhanh sang dự báo lưu lượng mà chưa chứng minh bottleneck. | Tôi ưu tiên đo 3-5 ngày và thử giải pháp vận hành trước, không giao quyền ra vào cho AI. |
| Workflow | Dùng để hỗ trợ diễn đạt flow và kiểm tra các nhánh fallback. | Giúp nhìn rõ điểm AI can thiệp giữa Rule kiểm tra input và bước CSKH review. | Một flow đẹp không chứng minh các bước thực tế hay thời gian là đúng. | Tôi giữ human review 100% trong pilot và thêm fallback cho confidence thấp, schema lỗi, multi-intent và timeout. |
| Research | Dùng AI/search để tìm và tóm tắt các hướng text classification, structured output. | Giúp nhóm so sánh Rule, classification và JSON có schema. | JSON hợp lệ không có nghĩa là category hoặc BQL được chọn đúng; nguồn cũng không thay thế dữ liệu ticket thật. | Tôi yêu cầu taxonomy nhỏ, ticket ẩn danh, audit và metric accuracy trước khi Go. |
| Problem Statement | Dùng để phản biện field còn mơ hồ và kiểm tra logic metric/boundary. | Giúp phát hiện sự khác nhau giữa mục tiêu `<= 2 phút` và baseline chưa có log. | AI có thể làm câu chữ chắc chắn hơn mức bằng chứng cho phép. | Tôi đổi cách viết thành hypothesis, thêm cách đo và ghi rõ dữ liệu cần xác minh. |
| Rule / Workflow / Agent | Dùng để so sánh ba mức can thiệp. | Giúp diễn đạt ưu nhược điểm của Rule, Workflow và Agent. | Đề xuất Agent dễ làm bài toán trông hiện đại nhưng vượt phạm vi và khó audit. | Tôi chọn Workflow, giữ Rule làm fallback và loại tự động route ticket confidence thấp. |
| Decision | Dùng để gợi ý câu hỏi challenge, không dùng AI chốt quyết định. | Có thêm góc nhìn về rủi ro route sai và điều kiện rollback. | AI không thể thay nhóm xác nhận quyền truy cập dữ liệu, owner hay mức hậu quả. | Tôi cùng nhóm chọn `Not Yet`, yêu cầu baseline, dữ liệu ẩn danh, taxonomy và interview trước pilot. |

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
Khi nghe top 3 problem của các bạn, tôi học được rằng một bài có impact lớn chưa chắc là bài phù hợp nhất để làm trong lab. Candidate sự cố pin có rủi ro vận hành và phụ thuộc dữ liệu realtime, còn ticket routing có workflow và metric dễ kiểm thử hơn. Tôi cũng nhận ra nhóm rất dễ đi từ pain sang Agent nếu không dừng lại ở bước mô tả workflow. Ban đầu tôi quan tâm đến việc dùng AI dự báo hàng chờ ở cửa VinUni, nhưng sau khi tự challenge, tôi thấy chưa thể biết bottleneck nằm ở tốc độ quẹt thẻ hay cách bố trí làn. Vì vậy tôi đồng ý ưu tiên đo và thử giải pháp vận hành trước. Trong bài toán ticket routing, tôi đóng góp bằng cách yêu cầu tách số liệu ước tính khỏi evidence đã xác minh. Điều khó nhất khi viết Problem Statement là giữ metric đủ cụ thể nhưng không biến mục tiêu thành sự thật đã có. Nhóm đã xử lý điều đó bằng cách ghi baseline 8 phút là hypothesis, thêm cách đo và đặt boundary cho CSKH review. Tôi thấy Workflow phù hợp hơn Agent vì các bước đã biết trước và kết quả AI có thể bị từ chối. Nếu làm lại, tôi sẽ challenge sớm hơn về tiêu chí route đúng, dữ liệu ticket multi-intent và cách lấy quote thật từ CSKH. Bài học lớn nhất của tôi là một quyết định Not Yet vẫn có giá trị nếu nó chỉ rõ dữ liệu và điều kiện cần để tiến tiếp.
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

