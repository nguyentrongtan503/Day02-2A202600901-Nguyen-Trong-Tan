
| Cluster | Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---:|---|---|---|
| Sales / email outreach | 1 | Soạn nháp email cá nhân hóa cho sản phẩm mới hoặc chương trình mới | Workflow rõ, sales mất nhiều thời gian viết/chỉnh email, có metric tốt như thời gian chuẩn bị email và tỷ lệ phản hồi | Dữ liệu khách hàng có đủ để cá nhân hóa tốt hay không |
| Sales / email outreach | 2 | Gợi ý câu trả lời cho email khách hàng | Pain thật, email khách hỏi lặp lại nhiều, AI có thể giúp đọc email và tạo nháp trả lời nhanh | AI có được truy cập nguồn thông tin đáng tin cậy như bảng giá, tồn kho, FAQ và chính sách không |
| Sales / email outreach | 3 | Phân nhóm khách hàng và gợi ý nội dung phù hợp | Impact rộng, giúp email liên quan hơn thay vì gửi một nội dung chung cho toàn bộ danh sách | Dữ liệu khách hàng có sạch và đủ thuộc tính để phân nhóm chính xác hay không |
| Interview / learning support | 1 | Phân tích JD và gap kỹ năng | Actor rõ, workflow rõ, bottleneck cụ thể, metric đo được, dễ validate | Pain có đủ phổ biến ngoài nhóm fresher không? |
| Interview / learning support | 2 | Ôn phỏng vấn không có feedback | AI có thể hỗ trợ tốt, pain rõ, workflow đơn giản | Chất lượng câu trả lời "đủ tốt" khó đo |
| Internal knowledge / onboarding | 1 | Onboarding documentation rời rạc và thiếu hướng dẫn cụ thể cho dev/engineer khiến new hire tốn nhiều thời gian cho setup và hỏi mentor lặp lại | Workflow rõ, tốn nhiều thời gian, ảnh hưởng TFMC | Có nên cho AI đọc internal docs/org chart? Privacy limits? |
| Internal knowledge / onboarding | 2 | Khi nhận task, người thực hiện phải tìm context từ nhiều Slack/thread và tài liệu, mất thời gian ghép bối cảnh và dễ làm sai yêu cầu | Thông tin phân tán, gây rework và delay | Chất lượng tóm tắt AI đo thế nào? Ai verify? |
| Internal knowledge / onboarding | 3 | Khi cần biết ai chịu trách nhiệm một tác vụ hay tài nguyên, team thường bị chuyển tiếp nhiều lần, delay assign và execution | Nhiều người bị ảnh hưởng, gây chuyển tiếp và delay | Data access & owner registry governance? |
| Vendor / supplier workflow | 1 | Theo dõi phản hồi từ nhà cung cấp | Workflow rõ, lặp lại, dễ đo bằng thời gian và số vendor đã phản hồi | Cần biết team hiện dùng Gmail, Sheet hay CRM |
| Vendor / supplier workflow | 2 | Tìm kiếm thông tin nhà cung cấp | Tốn thời gian, xảy ra trước mỗi dự án | Chất lượng nguồn tìm kiếm có thể khó kiểm soát |
| Vendor / supplier workflow | 3 | So sánh báo giá vendor | Có impact cao cho quyết định kinh doanh | Format báo giá khác nhau, khó chuẩn hóa |


# Cluster và candidate examples

| Cluster | Candidate examples | Pattern chung |
|---|---|---|
| Sales / email outreach | Soạn nháp email cá nhân hóa cho sản phẩm mới, gợi ý câu trả lời cho email khách hàng, phân nhóm khách hàng và gợi ý nội dung phù hợp | Dùng dữ liệu khách hàng và thông tin sản phẩm để tạo email/nội dung phù hợp hơn, giảm thời gian viết và chỉnh sửa thủ công |
| Interview / learning support | Phân tích JD và gap kỹ năng, ôn phỏng vấn không có feedback | Đọc yêu cầu hoặc câu trả lời rồi chỉ ra thiếu sót, gap kỹ năng và gợi ý cách cải thiện |
| Internal knowledge / onboarding | Onboarding documentation rời rạc, tìm context từ Slack/thread/tài liệu, tìm người chịu trách nhiệm hoặc tài nguyên liên quan | Tìm và tổng hợp thông tin phân tán để người dùng hiểu đúng context, giảm hỏi lại mentor/team |
| Vendor / supplier workflow | Theo dõi phản hồi từ nhà cung cấp, tìm kiếm thông tin nhà cung cấp, so sánh báo giá vendor | Thu thập, chuẩn hóa và theo dõi thông tin vendor để tránh bỏ sót phản hồi, giảm thời gian tìm kiếm và follow-up |



# Shortlist và score

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Vendor / supplier workflow | 5 | 5 | 5 | 4 | 5 | 5 | 5 | 34 |
| Sales / email outreach | 4 | 3 | 3 | 4 | 4 | 3 | 4 | 25 |
| Internal knowledge / onboarding | 4 | 3 | 4 | 4 | 3 | 4 | 4 | 26 |

**Nhóm chọn: Vendor / supplier workflow.**

## Vì sao chọn

- Workflow rõ nhất: tìm vendor → lấy contact → ghi sheet → gửi email → chờ phản hồi → check inbox → cập nhật trạng thái → follow-up.
- Có actor rõ: người phụ trách tìm nhà cung cấp, sales/admin/operation hoặc PM.
- Pain dễ thấy: thông tin vendor nằm rải rác, dễ quên check email, dễ bỏ sót vendor chưa phản hồi.
- Impact đo được tốt: giảm thời gian tìm kiếm, giảm số vendor bị bỏ sót, tăng tỷ lệ follow-up đúng hạn.
- Có thể làm trong lab: dùng Google Sheet/email mẫu/mock inbox là có thể demo được.
- Dễ vẽ before/after: trước làm thủ công, sau có AI hỗ trợ tìm, tổng hợp, nhắc follow-up và cập nhật trạng thái.

## Vì sao không chọn các bài khác

- **Sales / email outreach:** impact tốt nhưng dễ bị giống bài viết email thông thường, cần dữ liệu khách hàng đủ sạch để cá nhân hóa tốt.
- **Internal knowledge / onboarding:** bài toán thực tế nhưng data access phức tạp, dễ trượt sang hệ thống search/RAG lớn, khó làm gọn trong lab.
- **Interview / learning support:** dễ demo nhưng pain và impact trong bối cảnh lab có thể không mạnh bằng vendor workflow.

---

## Bước 4.1 — Quick validation

**Problem kiểm chứng:** Theo dõi phản hồi nhà cung cấp sau khi gửi email — check inbox, cập nhật status, dễ sót rep / quên follow-up.

### Option A — Quick interviews

Hỏi **2 người** (Operations âm nhạc; bạn làm event liên hệ venue/AV).

| Người | Đau nhất | Thời gian | Muốn thay đổi |
|---|---|---|---|
| A | Check inbox + cập nhật Sheet | ~ 30 phút/ngày (~20 vendor) | Biết ngay ai đã rep, ai cần nhắc |
| B | Search inbox theo tên vendor | ~20–30 phút/ngày lúc cao điểm | Bảng status luôn đúng, đỡ bị hỏi lại |



**Insight:** Pain chủ yếu **sau khi đã gửi email** — cần status rõ (replied / follow-up), không ôm cả tìm vendor hay so sánh báo giá.

---

## Bước 4.2 — Research giải pháp đã có

Tìm ít nhất:

- 2–3 existing solutions/tools/patterns.
- 1–2 nguồn tham khảo có hyperlink.
- Nhận xét: họ xử lý bước nào trong workflow, chưa xử lý bước nào.
- Bài học kéo về bài toán nhóm mình.

| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Gmail + Google Sheets (Rule) | https://support.google.com/mail/answer/6579 · https://support.google.com/docs/answer/9060445 | Gửi email, label/lọc thread; Sheet lưu vendor + cột status | Miễn phí, lab demo dễ, team quen tool | Không tự match reply ↔ vendor; vẫn check inbox + update tay | Dùng làm nền Rule: template email + cột status cố định |
| Streak CRM (Gmail) | https://www.streak.com/ | Pipeline theo vendor/deal trong Gmail; theo dõi thread, stage (sent / replied) | Gắn sát inbox, ít đổi thói quen email | Học pipeline mới; khó tóm tắt nội dung báo giá tự động | Pattern Workflow: status gắn thread, không cần Agent |
| HubSpot CRM (free) | https://www.hubspot.com/products/crm | Log email, contact/deal, task nhắc follow-up | Timeline rõ, nhắc việc, scale khi nhiều vendor | Setup nặng hơn Sheet; AI/gợi ý status phụ thuộc gói | Nếu công ty đã có CRM thì không build lại từ đầu |

**Research takeaway:**

```text
Không cần build Agent tự gửi email / tự chọn vendor. Hướng hợp lý: Workflow trên nền Sheet + Gmail — AI/workflow chỉ gợi ý vendor nào đã rep và status, người Operations review trước khi follow-up.
```

---

## Workflow before/after

**File nhóm nộp kèm:** `02-group-problem-statement-workflow.md`

**Nội dung workflow** (phần theo dõi phản hồi sau khi đã gửi email — ~20 vendor/dự án):

```text
CURRENT STATE — 6 bước, 30 phút/ngày

[1 Mở Google Sheet danh sách vendor: 2']
→ [2 Mở inbox, search từng vendor/email thread: 10']
→ [3 Đọc email phản hồi nếu có: 8']
→ [4 Cập nhật status trong Sheet: replied / not replied / follow-up needed: 5']  <-- bottleneck
→ [5 Ghi chú ngắn nội dung phản hồi: 3']
→ [6 Đánh dấu vendor cần follow-up: 2']

FUTURE STATE — 5 bước, 10 phút/ngày

[1 Workflow quét inbox theo danh sách vendor trong Sheet: 2']     -- Workflow
→ [2 Tự match email phản hồi với vendor: 2']                    -- Workflow
→ [3 AI tóm tắt phản hồi + gợi ý status: 3']                    -- Workflow / AI
→ [4 Operations review và xác nhận status trên Sheet: 3']         -- Human boundary
→ [5 Gửi follow-up / cập nhật manager (nếu cần): theo quyết định người]  -- Human

Fallback:
AI match sai hoặc gợi ý status sai → Operations mở email gốc, cập nhật Sheet thủ công; tắt gợi ý AI cho vendor đó.

Bottleneck mới:
Operations review + xác nhận status. Bottleneck chấp nhận được vì là điểm kiểm soát — tránh sót rep và gửi follow-up nhầm.
```

## Before/after impact

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| **Tổng thời gian** | 30 phút/ngày | Dưới 10 phút/ngày | Target chính |
| **Số bước** | 6 | 5 | Không chỉ giảm bước, mà giảm effort ở bước check inbox + cập nhật status |
| **Bước thủ công** | 6/6 | 2/5 | Operations vẫn review và follow-up |
| **Bottleneck chính** | Check inbox + cập nhật status | Review/xác nhận status | Human boundary |
| **Risk mới** | Không có AI nhận diện sai | Có risk match email/status sai | Cần review email gốc trước khi chốt Sheet |

---

## Bước 5.3 — Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Nhân viên Operations hoặc Project Coordinator phụ trách liên hệ nhà cung cấp (công ty âm nhạc, event, sản xuất). |
| **Workflow** | Lập danh sách vendor trên Google Sheet → gửi email yêu cầu báo giá/hợp tác → mỗi ngày check Gmail → cập nhật status từng vendor → follow-up nếu chưa phản hồi → báo manager tiến độ. |
| **Bottleneck** | Bước check inbox và cập nhật status thủ công: phải search từng email thread, match với đúng vendor trong Sheet, dễ sót phản hồi hoặc cập nhật chậm. |
| **Impact** | Khoảng **30 phút/ngày** khi theo dõi ~20 vendor; chậm chọn nhà cung cấp; manager/teammate hay hỏi lại “bên nào rep rồi”; dễ quên follow-up sau 2–3 ngày. |
| **Success Metric** | Giảm thời gian theo dõi phản hồi từ 30 phút/ngày xuống **dưới 10 phút/ngày**; **không bỏ sót** vendor đã phản hồi; 100% vendor có status rõ: `sent` / `replied` / `follow-up needed` / `rejected`. |
| **Boundary** | Không tự chọn vendor cuối cùng thay người; không tự gửi email follow-up nếu chưa được duyệt; chỉ dùng email/Sheet đã có quyền truy cập; mọi status chốt phải do Operations xác nhận. |

---

## Problem Statement v1

| Field | Nội dung |
|---|---|
| Actor | Nhân viên Operations/Project Coordinator trong công ty âm nhạc. |
| Workflow | Tìm vendor → ghi thông tin → gửi email yêu cầu → chờ phản hồi → check inbox → cập nhật status → follow-up nếu cần. |
| Bottleneck | Check email thủ công và cập nhật trạng thái từng vendor mất thời gian, dễ sót phản hồi. |
| Impact | Chậm quá trình chọn nhà cung cấp, dễ quên follow-up, manager phải hỏi lại trạng thái nhiều lần. |
| Success Metric | Giảm thời gian check/update vendor xuống dưới 10 phút/ngày; không bỏ sót vendor đã phản hồi; status vendor rõ ràng. |
| Boundary | AI không tự chọn vendor cuối cùng, không tự gửi follow-up nếu chưa được duyệt, không tự bịa thông tin nhà cung cấp. |
| AI intervention point | Sau khi email được gửi và bắt đầu có phản hồi từ vendor. |
| Mức chọn | Workflow: email template + check reply + update status + human review. |
| Rủi ro & người thật kiểm tra | Risk: nhận diện nhầm email, tóm tắt sai nội dung báo giá, update nhầm trạng thái. Người kiểm tra: nhân viên Operations review email gốc trước khi xác nhận. |

## Final decision

**Decision:**  
Go với scope nhỏ.

**Pilot nhỏ nhất:**

- Dùng danh sách 10 nhà cung cấp.
- Gửi email bằng template cố định.
- Theo dõi phản hồi trong 3–5 ngày.
- AI/workflow chỉ làm 2 việc:
  1. Kiểm tra vendor nào đã phản hồi.
  2. Gợi ý status: replied / not replied / follow-up needed.
- Nhân viên review lại trước khi cập nhật bản cuối.

**Exit / rollback:**

- Nếu AI nhận diện sai phản hồi quá 2 lần trong 1 tuần, quay lại check thủ công.
- Nếu workflow làm rối hơn Google Sheet, chỉ giữ email template + Sheet status.
- Nếu có rủi ro gửi nhầm email, không cho AI tự gửi email follow-up.

**Decision rationale:**  
Problem rõ, workflow rõ, có bottleneck thật.  
Không cần build agent lớn ngay.  
Workflow đơn giản là đủ: gửi email theo template, theo dõi phản hồi, cập nhật trạng thái, người thật kiểm tra.

