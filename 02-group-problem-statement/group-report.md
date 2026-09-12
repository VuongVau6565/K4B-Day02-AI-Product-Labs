# 02 - Group Problem Statement (Bản nộp nhóm)

> Bản tổng hợp từ `individual-report.md` và `indiviual_report2.md`. `individual-report3.md` hiện đang rỗng, vì vậy các candidate cá nhân của ba thành viên bổ sung chưa được điền giả.

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
|---|---|---|---|
| 1 | Dương Đức Vương | 2A202602944 | Facilitator, validation |
| 2 | Nguyễn Đức Anh Quân | 2A202602405 | Workflow, research |
| 3 | Đỗ Hoàng Quân | 2A202603016 | Domain, AI prototype |
| 4 | Nguyễn Ngọc Linh | 2A202602480 | Research, validation |
| 5 | Lê Thị Trâm Anh | 2A202602846 | Writer, documentation |

**Phân công bổ sung:** Dương Đức Vương phụ trách điều phối và validation; Nguyễn Ngọc Linh phụ trách research và thu thập dữ liệu; Lê Thị Trâm Anh phụ trách viết và chuẩn hóa báo cáo.

**Candidate problem nhóm chọn (1 câu):**

Nhân viên vận hành phải đọc, phân loại và chuyển tiếp thông tin không có cấu trúc từ nhiều nguồn; một workflow AI có human review có thể tạo bản tóm tắt/JSON để giảm thời gian xử lý mà vẫn giữ quyền quyết định cho người phụ trách.

---

## Phase 3 - Group Convergence

### 3.1. Top candidates từ các báo cáo đã nhận

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh của nhóm |
|---|---|---|---|---|---|
| 1 | Nguyễn Đức Anh Quân | Tổng hợp task/deadline từ Discord, Zalo, Google Docs | Leader và thành viên nhóm | Đọc, đối chiếu và gom thông tin từ nhiều kênh | Workflow rõ, nhưng cần giới hạn phạm vi nguồn |
| 2 | Nguyễn Đức Anh Quân | Tìm lại tài liệu, quyết định và file cũ trước deadline | Cả nhóm | Search và xác định đúng phiên bản | Pain lặp lại, cần kho dữ liệu có quyền truy cập |
| 3 | Lê Thị Trâm Anh | Viết báo cáo/README từ nhiều nguồn rời rạc | Người viết báo cáo | Đọc, tóm tắt, tạo draft và sửa format | AI phù hợp ở bước outline/draft, không nên tự viết toàn bộ |
| 4 | Dương Đức Vương | Xử lý sự cố pin xe Xanh SM và điều phối xe sạc/cứu hộ | Dispatcher và tài xế | Đối chiếu GPS, trạm sạc, % pin và soạn hướng dẫn | Impact lớn, nhưng rủi ro vận hành và dữ liệu realtime cao |
| 5 | Đỗ Hoàng Quân | Phân loại và định tuyến ticket cư dân Vinhomes | CSKH và cư dân | Đọc ticket không cấu trúc, chọn danh mục và BQL | Workflow rõ, lặp lại cao, đo được tốt |
| 6 | Nguyễn Ngọc Linh | Chẩn đoán sơ bộ lỗi xe VinFast từ mô tả tiếng Việt | Kỹ thuật viên và khách hàng | Hỏi lại triệu chứng và tra cứu tài liệu | AI hiểu ngôn ngữ tự nhiên, nhưng risk sai chẩn đoán cao |
| 7 | Nguyễn Ngọc Linh | Tổng hợp lý do khách hủy cuốc từ ghi âm và ghi chú | BA/Ops | Nghe mẫu và tìm pattern thủ công | Có thể mở rộng nhưng cần dữ liệu ghi âm |
| 8 | Lê Thị Trâm Anh | Trích xuất release notes từ commit/PR | Kỹ sư, QA và Ops | Hiểu commit viết tắt và chuyển thành nội dung để test | Phạm vi nhỏ, dễ làm prototype |


### 3.2. Gom trùng / cluster

| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| A - Tổng hợp tri thức nhóm | 1, 2, 3 | Thông tin rời rạc, người dùng phải đọc và chuyển thành bản có cấu trúc | Phù hợp workflow AI có review |
| B - Triage và routing vận hành | 4, 5, 6 | Đầu vào tự nhiên/nhiều hệ thống, cần phân loại và chọn hành động tiếp theo | Cần boundary và fallback chặt |
| C - Tóm tắt vận hành | 7, 8 | Chuyển ghi âm, commit hoặc log thành summary cho người khác xử lý | Dễ prototype nếu có dữ liệu mẫu |
| D | 9 | Chưa có thông tin | Chờ bổ sung report 3 |

### 3.3. Shortlist

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
|---|---|---|
| Phân loại và định tuyến ticket cư dân Vinhomes | 200 ticket/ngày theo báo cáo; workflow 4 bước; metric thời gian và accuracy rõ | Chưa có tập ticket đã ẩn danh; ticket multi-intent chưa rõ |
| Tổng hợp task/deadline nhiều kênh | Lặp lại 2-3 lần/tuần; pain ảnh hưởng cả nhóm; có human review tự nhiên | Quyền truy cập Discord/Zalo/Docs và nguồn sự thật chưa rõ |
| Xử lý sự cố pin nguy cấp cho Xanh SM | 80-100 vụ/ngày; bottleneck 15 phút; impact doanh thu lớn | Ranh giới an toàn, API realtime và trách nhiệm khi sai cao |

### 3.4. Score để đồng thuận

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Phân loại/routing ticket cư dân | 5 | 5 | 4 | 5 | 4 | 5 | 3 | 31 |
| Tổng hợp task/deadline nhiều kênh | 5 | 5 | 4 | 4 | 3 | 4 | 4 | 29 |
| Xử lý sự cố pin nguy cấp | 5 | 5 | 4 | 5 | 2 | 3 | 3 | 27 |

**Candidate nhóm chọn:**

```text
Hỗ trợ phân loại và định tuyến ticket phản ánh cư dân bằng AI, với CSKH review trước khi chuyển đến BQL phù hợp.
```

**Vì sao chọn:**

```text
Candidate có actor, đầu vào, workflow và đầu ra rõ ràng: CSKH nhận ticket, đọc nội dung, phân loại, chọn BQL và chuyển tiếp. Báo cáo cá nhân ước tính khoảng 200 ticket/ngày/khu đô thị và 8 phút/ticket, nên có thể đo baseline bằng thời gian xử lý, accuracy và tỷ lệ route đúng. AI phù hợp để trích xuất entity và tạo JSON, trong khi CSKH vẫn giữ quyền review. Phạm vi prototype có thể giới hạn vào một số danh mục và một khu đô thị.
```

**Vì sao không chọn candidate còn lại:**

```text
Tổng hợp task/deadline từ nhiều kênh có pain rõ nhưng phụ thuộc nhiều nền tảng và quyền truy cập, trong khi nhóm chưa có dữ liệu lịch sử để kiểm chứng. Xử lý sự cố pin có impact lớn nhưng sai sót có thể gây tổn thất vận hành và cần API realtime, vượt quá phạm vi lab hiện tại. Các candidate viết báo cáo, tìm file và release notes dễ prototype nhưng impact nhỏ hơn và chưa được cả nhóm ưu tiên.
```

**Disagreement:**

```text
Nguyễn Đức Anh Quân ưu tiên bài toán tổng hợp task vì gần với workflow học tập; Đỗ Hoàng Quân ưu tiên ticket routing vì có volume và metric rõ hơn. Dương Đức Vương, Nguyễn Ngọc Linh và Lê Thị Trâm Anh tham gia validation, research và chuẩn hóa báo cáo. Nhóm tạm chốt ticket routing theo điểm số và khả năng kiểm thử, nhưng phải xác nhận lại bằng validation và bổ sung các báo cáo cá nhân còn thiếu trước khi Go.
```

---

## Phase 4 - Quick Validation + Research

### 4.1. Quick validation

Chưa có interview/survey độc lập trong ba file đầu vào. Các con số dưới đây là quan sát/ước tính từ cá nhân, không phải quote đã xác minh.

| Nguồn | Số người/mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Báo cáo của Đỗ Hoàng Quân | 1 người quan sát, ước tính 200 ticket/ngày | 8 phút/ticket; CSKH đọc và chọn BQL thủ công | Chưa có log/ticket mẫu | Giữ candidate dạng hypothesis, giới hạn vào ticket một intent |
| Báo cáo của Nguyễn Đức Anh Quân | 1 nhóm học tập, 4 người | Xác nhận pain chung là thông tin rời rạc và cần checklist | Không trực tiếp validate ticket cư dân | Dùng để so sánh, không dùng làm bằng chứng domain Vinhomes |
| Interview/survey người dùng | Chưa thực hiện | Chưa có quote nguyên văn | Chưa có | Cần phỏng vấn 2-3 CSKH/dispatcher hoặc dùng tập ticket ẩn danh |

**Insight sau validation:**

```text
Chưa đủ bằng chứng để kết luận pain 200 ticket/ngày là đại diện cho mọi khu đô thị. Pain cần kiểm chứng là thời gian đọc và route ticket không có cấu trúc; prototype chỉ nên xử lý một số danh mục có quy tắc rõ và luôn để CSKH review.
```

### 4.2. Research giải pháp đã có

| Nguồn/tool/case | Link | Họ giải quyết bước nào? | Điểm mạnh | Khoảng trống/rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Microsoft Power Automate - AI Builder text classification | [Microsoft Learn](https://learn.microsoft.com/en-us/ai-builder/text-classification-overview) | Phân loại text theo nhãn | Tích hợp workflow và human review | Phụ thuộc dữ liệu huấn luyện, multi-intent khó | Bắt đầu bằng classification có nhãn |
| Azure AI Language - custom text classification | [Microsoft Learn](https://learn.microsoft.com/en-us/azure/ai-services/language-service/custom-text-classification/overview) | Gắn nhãn danh mục cho văn bản | Có custom category và API | Cần tập dữ liệu ẩn danh, theo dõi drift | Định nghĩa taxonomy nhỏ và metric F1/accuracy |
| Structured outputs với Azure OpenAI | [Microsoft Learn](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/structured-outputs) | Trích xuất entity, mức độ khẩn và BQL | JSON dễ kết nối workflow | JSON hợp lệ không đồng nghĩa thông tin đúng | Validate schema, confidence và bước review |

**Research takeaway:**

```text
Nên build workflow nhỏ: nhận ticket -> trích xuất trường có cấu trúc -> gợi ý danh mục/BQL -> CSKH review -> chuyển tiếp. Không nên build agent tự lập kế hoạch, không nên tự động chuyển ticket khi confidence thấp, và không nên đưa ra cam kết SLA khi chưa có dữ liệu thực.
```

---

## Phase 5 - Workflow + Problem Statement

### 5.1. Current workflow

```text
[1 Nhận ticket: 1'] -> [2 Đọc và hiểu nội dung: 4'] -> [3 Chọn danh mục/BQL: 2'] -> [4 Gửi xác nhận và chuyển ticket: 1']
```

| Bước | Actor | Input | Output | Thời gian/tần suất | Ghi chú |
|---|---|---|---|---|---|
| 1 | CSKH | Ticket, ảnh, thông tin căn hộ | Ticket được mở | 1 phút, hằng ngày | Nguồn từ App Resident/CRM |
| 2 | CSKH | Mô tả tự nhiên, ảnh đính kèm | Hiểu sơ bộ về vấn đề | 4 phút | Bottleneck; nội dung không cấu trúc |
| 3 | CSKH | Nội dung đã đọc, danh bạ BQL | Danh mục và nơi nhận | 2 phút | Có thể nhầm với ticket multi-intent |
| 4 | CSKH/BQL | Ticket đã phân loại | Ticket được route | 1 phút | Handoff sang BQL |

**Bottleneck chính:**

```text
CSKH phải đọc và diễn giải lại văn bản tự nhiên trước khi chọn danh mục và BQL. Nếu thiếu thông tin hoặc ticket có nhiều ý, việc route sai làm tăng thời gian phản hồi; AI chỉ nên gợi ý và đánh dấu độ tin cậy, không tự động quyết định mọi trường hợp.
```

### 5.2. Future workflow

```text
[1 Nhận ticket - hệ thống] -> [2 Rule kiểm tra trường bắt buộc] -> [3 AI trích xuất JSON và gợi ý danh mục/BQL] -> [4 CSKH review, sửa nếu cần - boundary] -> [5 Hệ thống chuyển ticket]

Fallback: confidence < 0.85, schema lỗi, ticket multi-intent hoặc AI timeout thì đưa vào hàng đợi xử lý thủ công; không tự động route.
```

**Before/after impact:**

| Metric | Trước | Sau kỳ vọng | Cách đo |
|---|---:|---:|---|
| Thời gian xử lý ticket | 8 phút | <= 2 phút | Timestamp nhận đến route |
| Số bước thủ công | 4 | 1-2 | Đếm thao tác của CSKH |
| Accuracy route | Chưa có baseline | >= 92% | So sánh với nhãn đúng do reviewer |
| Ticket bị trả về/sửa route | Chưa có baseline | Giảm 30% | Log route và correction |
| Risk mới | Không áp dụng | AI route sai | Audit mẫu và fallback |

### 5.3. Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Nhân viên CSKH Ban Quản lý, người tiếp nhận và route ticket cư dân. |
| **Workflow** | Nhận ticket, đọc nội dung/ảnh, phân loại, chọn BQL và chuyển tiếp. |
| **Bottleneck** | Đọc văn bản không cấu trúc và đối chiếu danh mục/BQL thủ công. |
| **Impact** | Ước tính 8 phút/ticket, chậm phản hồi và có nguy cơ route sai. |
| **Success Metric** | Giảm xử lý xuống <= 2 phút và route đúng >= 92% trong tập pilot. |
| **Boundary** | Chỉ xử lý triage; không tự trả lời cam kết, không tự quyết định xử lý sự cố, không tự route khi confidence thấp. |

**Câu hỏi AI phản biện v0:**
- Field mơ hồ: số liệu 200 ticket/ngày và 8 phút/ticket chưa có log gốc; taxonomy và tiêu chí route đúng chưa chốt.
- Tôi sửa gì: đánh dấu các số liệu là hypothesis, thêm confidence threshold, human review và fallback.

---

## Phase 6 - Rule / Workflow / Agent + Decision

### 6.0. Ma trận độ phù hợp

- Độ mơ hồ: **[x] Cao** - ticket tiếng Việt có thể có nhiều ý, ảnh đính kèm và thiếu trường.
- Độ phức tạp: **[x] Cao** - nhiều bước, kết hợp extraction, classification, routing và review.

**Bài toán nhóm nằm ở ô:**

```text
Cao mơ hồ / Cao phức tạp, nhưng chỉ trong phạm vi triage ticket; không mở rộng thành agent tự xử lý sự cố.
```

### 6.1. So sánh Rule / Workflow / Agent

| Mức | Phương án | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| Rule | Keyword, danh mục, danh bạ BQL và required fields | Ticket có mẫu cấu trúc, từ vựng ổn định | Bỏ sót cách diễn đạt tự nhiên, multi-intent | Dùng làm validation và fallback |
| Workflow | Extraction/classification -> confidence -> CSKH review -> route | Đa số ticket có thể triage theo luồng cố định | Sai nhãn hoặc JSON lỗi | **Chọn cho pilot** |
| Agent | Tự lập kế hoạch, gọi nhiều tool, tự xử lý ticket | Quy trình đã có dữ liệu và governance mạnh | Khó audit, route sai, vượt boundary | Không chọn |

**5 câu hỏi chốt:**
1. Rule xử lý được ticket có keyword rõ, nhưng chưa chắc đạt 70-80% khi văn bản tự nhiên và multi-intent nhiều.
2. Các bước chính đi theo luồng thẳng, có nhánh fallback khi confidence thấp.
3. Không cần Agent tự lập kế hoạch; workflow có schema và human review là đủ.
4. CSKH phát hiện sai trong bước review, mục tiêu không quá 20 giây/ticket trong pilot.
5. Có thể hạ xuống Rule cho danh mục có từ khóa và dùng workflow cho phần còn lại.

**Mức chọn:**

```text
Workflow
```

**Vì sao chọn:**

```text
Workflow tách phần AI gợi ý khỏi quyết định route cuối. Schema, confidence threshold và audit log làm cho kết quả có thể kiểm tra. Nó phù hợp hơn Agent vì các bước, người review và fallback đã biết trước.
```

**Vì sao không chọn mức đơn giản hơn:**

```text
Rule chỉ phù hợp với ticket có mẫu cấu trúc và từ khóa ổn định, trong khi đầu vào là mô tả tự nhiên. Tuy nhiên nhóm vẫn giữ Rule cho required fields, keyword và fallback; AI chỉ xử lý phần Rule không bao phủ.
```

### 6.2. Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | CSKH Ban Quản lý, review gợi ý trước khi route ticket cư dân. |
| **Workflow** | CRM nhận ticket; Rule kiểm tra input; model trích xuất entity và gợi ý category/BQL; CSKH review; hệ thống route. |
| **Bottleneck** | 4-6 phút đọc và diễn giải nội dung không cấu trúc, sau đó tra danh mục và BQL. |
| **Impact** | Hypothesis: baseline 8 phút/ticket; mục tiêu pilot <= 2 phút, route đúng >= 92%. Cần log để xác minh. |
| **Success Metric** | Median time/ticket, accuracy route, tỷ lệ sửa gợi ý, tỷ lệ fallback và ticket bị trả về. |
| **Boundary** | Làm triage và gợi ý route. Không tự trả lời khách, không tự phân công kỹ thuật viên, không tự động xử lý ticket confidence thấp. |
| **AI intervention point** | Sau Rule kiểm tra input và trước bước CSKH chọn danh mục/BQL. |
| **Mức chọn** | Workflow, vì luồng cố định và cần kết hợp AI với human review. |
| **Rủi ro & người thật kiểm tra** | Route sai hoặc bỏ sót mức độ khẩn; CSKH review 100% pilot, Ops audit mẫu hằng ngày và có fallback thủ công. |

### 6.3. Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
|---|---|---|
| Actor + workflow rõ chưa? | Yes | Actor và 5 bước đã được giới hạn. |
| Baseline + metric đo được chưa? | Not Yet | Có ước tính 8 phút và 200 ticket/ngày nhưng chưa có log gốc. |
| Data/input đủ dùng chưa? | Not Yet | Cần tập ticket ẩn danh, taxonomy và danh bạ BQL. |
| AI sai, hậu quả chấp nhận được không? | Yes, có điều kiện | Chỉ gợi ý, CSKH duyệt, confidence thấp thì fallback. |
| Có người review/owner không? | Yes | CSKH review; Ops quản lý taxonomy và audit. |
| Có cách non-AI đơn giản hơn không? | Yes | Rule/required fields là baseline và fallback. |

**Decision:**

```text
Not Yet
```

**Lý do:**

```text
Workflow có actor, bottleneck và metric dự kiến rõ, và có boundary an toàn cho human review. Tuy nhiên hai số liệu chính mới là ước tính từ báo cáo cá nhân, chưa có interview, survey hay log ticket để xác minh. Nhóm chỉ nên chuyển sang Go sau khi lấy dữ liệu ẩn danh, chốt taxonomy và đo baseline trên tập mẫu.
```

**Nếu Go - pilot nhỏ nhất:**

```text
Lấy 100-200 ticket đã ẩn danh của một khu đô thị, chỉ chọn 5 danh mục và một danh bạ BQL. Chạy song song cách cũ và workflow mới, không tự động route; đo 3 số: median time/ticket, accuracy route và tỷ lệ CSKH sửa gợi ý.
```

**Nếu Not Yet - cần validate gì trước:**

```text
Phỏng vấn 2-3 CSKH/dispatcher do Dương Đức Vương và Nguyễn Ngọc Linh phụ trách; thu thập ticket mẫu đã ẩn danh; xác nhận baseline 8 phút, volume và tiêu chí route đúng; Lê Thị Trâm Anh tổng hợp kết quả vào báo cáo; bổ sung các báo cáo cá nhân còn thiếu.
```

**Nếu No-Go - làm gì thay AI:**

```text
Dùng form có trường bắt buộc, taxonomy nhỏ, keyword rules và danh bạ BQL duy nhất; theo dõi route sai bằng audit hằng ngày.
```

**Exit / rollback:**

```text
Tắt AI và quay về Rule + CSKH thủ công nếu accuracy route dưới 92% trong hai đợt audit liên tiếp, tỷ lệ sửa gợi ý vượt 20%, có ticket khẩn bị route sai, schema lỗi lặp lại, hoặc AI timeout vượt ngưỡng đã đặt.
```

---

### Self-check nộp phần 02

- [x] Có nhật ký hội tụ từ các báo cáo đã nhận, cluster, shortlist và score.
- [ ] Có validation với quote thật; chưa có trong input, cần bổ sung trước khi Go.
- [x] Có workflow trước/sau, thời gian, handoff, bottleneck, boundary và fallback.
- [x] Có PS v0 -> v1, metric trước/sau và cách đo.
- [x] Có so sánh Rule/Workflow/Agent và Decision Not Yet có lý do.
- [ ] Đã bổ sung candidate cá nhân từ `individual-report3.md`; file hiện đang rỗng.
