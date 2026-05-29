# 01 - Individual Problem Scan

## Thông tin cá nhân

* Họ và tên: Nguyễn Trọng Tấn
* MSSV: 2A202600901

---

# Phase 1 — Individual Scan

## Bảng scan problem

| # | Lăng kính          | Problem quan sát được                                                                    | Ai đang đau?                                   | Dấu hiệu thật                                      |
| - | ------------------ | ---------------------------------------------------------------------------------------- | ---------------------------------------------- | -------------------------------------------------- |
| 1 | Tốn thời gian      | Người dùng phải mở nhiều file PDF, app bệnh viện và giấy tờ để xem lại lịch sử khám bệnh | Người có bệnh mãn tính, người lớn tuổi         | Mỗi lần khám lại mất khoảng 30-60 phút tổng hợp    |
| 2 | AI có thể tốt hơn  | Người dùng không biết bài tập nào phù hợp với bệnh nền                                   | Người có bệnh xương khớp, tim mạch, tiểu đường | Thường tìm YouTube/Google nhưng không chắc an toàn |
| 3 | AI có thể tốt hơn  | Người dùng khó xây dựng thực đơn phù hợp với tình trạng sức khỏe                         | Người ăn kiêng, tiểu đường, huyết áp           | Dễ ăn sai thực phẩm hoặc thiếu cân bằng dinh dưỡng |
| 4 | Lặp lại            | Người dùng phải nhập lại thông tin thuốc và lịch sử khám khi đổi bệnh viện/app           | Người khám ở nhiều nơi                         | Thông tin phân tán, không đồng bộ                  |
| 5 | Pain từ người khác | Người lớn tuổi khó nhớ lịch uống thuốc và lịch tái khám                                  | Người lớn tuổi, người chăm sóc                 | Hay quên thuốc hoặc tái khám trễ                   |
| 6 | Tốn thời gian      | Người dùng tự đọc kết quả xét nghiệm nhưng không hiểu thuật ngữ                          | Người không có kiến thức y khoa                | Phải tra Google từng chỉ số                        |
| 7 | Lặp lại            | Người dùng ghi chú tình trạng sức khỏe thủ công                                          | Người tập luyện, ăn kiêng                      | Dữ liệu rời rạc, khó theo dõi lâu dài              |
| 8 | Pain từ người khác | Người chăm sóc phải tổng hợp hồ sơ sức khỏe cho người thân                               | Người chăm sóc người lớn tuổi                  | Tốn thời gian khi cần khám gấp                     |

---

# Phase 2 — Top 3 Problem Cards

## Chọn top 3

| Rank | Problem                    | Vì sao chọn                                | Điều còn chưa chắc                |
| ---- | -------------------------- | ------------------------------------------ | --------------------------------- |
| 1    | Chuẩn hóa hồ sơ bệnh án    | Workflow rõ, có pain thật, dễ đo thời gian | Độ chính xác khi OCR tài liệu     |
| 2    | Gợi ý bài tập phù hợp      | AI phù hợp với recommendation              | Rủi ro nếu gợi ý sai              |
| 3    | Chế độ ăn uống cá nhân hóa | Có thể cá nhân hóa theo bệnh nền           | Khó validate dinh dưỡng chính xác |

---

# Problem Card #1 — Chuẩn hóa hồ sơ bệnh án

## Problem 1 câu

Người dùng phải mở nhiều nguồn dữ liệu sức khỏe khác nhau để xem lại lịch sử khám bệnh, gây mất thời gian và dễ bỏ sót thông tin quan trọng.

## Actor

Người có bệnh mãn tính hoặc người thường xuyên khám bệnh tại nhiều cơ sở y tế.

## Thời điểm / bối cảnh

Khi đi tái khám hoặc cần theo dõi lịch sử điều trị.

## Current workflow

1. Mở file PDF kết quả khám bệnh
2. Mở ảnh đơn thuốc cũ
3. Kiểm tra lịch sử khám trên app bệnh viện
4. Ghi chú thủ công thông tin quan trọng
5. So sánh các lần khám để theo dõi thay đổi

## Bottleneck

Thông tin bị phân tán ở nhiều nơi, khó tổng hợp và dễ bỏ sót dữ liệu quan trọng.

## Impact

Người dùng mất khoảng 45-60 phút để tổng hợp thông tin trước mỗi lần khám lại.

## Success metric

Giảm thời gian tổng hợp hồ sơ từ khoảng 60 phút xuống dưới 15 phút.

## Non-AI alternative

Người dùng tự lưu thông tin vào Excel hoặc ghi chú thủ công.

## AI hypothesis

AI OCR và NLP tự động trích xuất thông tin từ hồ sơ bệnh án, đơn thuốc và lịch sử khám bệnh để tạo dashboard tổng hợp.

## Quick gut

* [ ] No AI / process fix
* [ ] Rule
* [x] Workflow
* [ ] Agent
* [ ] Chưa biết

---

## Draft current workflow

```text
CURRENT STATE — 60 phút

[Mở PDF bệnh án]
→ [Mở ảnh đơn thuốc]
→ [Đăng nhập app bệnh viện]
→ [Đọc và ghi chú thủ công]
→ [So sánh các lần khám]
→ [Tổng hợp thông tin]
```

## Draft future workflow

```text
FUTURE STATE — 15 phút

[Upload hồ sơ]
→ [AI OCR trích xuất dữ liệu]
→ [AI chuẩn hóa thông tin]
→ [Dashboard tổng hợp]
→ [Người dùng kiểm tra lại]

Fallback:
Nếu OCR sai hoặc thiếu dữ liệu, người dùng chỉnh sửa thủ công.
```

---

# Problem Card #2 — Gợi ý bài tập phù hợp

## Problem 1 câu

Người dùng có bệnh nền không biết bài tập nào phù hợp và an toàn với tình trạng sức khỏe của mình.

## Actor

Người có bệnh xương khớp, tim mạch hoặc tiểu đường.

## Current workflow

1. Tìm bài tập trên Google hoặc YouTube
2. Đọc bình luận hoặc review
3. Tự chọn bài tập
4. Thử tập luyện
5. Dừng tập nếu thấy không phù hợp

## Bottleneck

Không có hướng dẫn cá nhân hóa theo bệnh nền.

## Success metric

Giảm thời gian tìm bài tập từ khoảng 30 phút xuống dưới 10 phút.

## AI hypothesis

AI đề xuất bài tập theo hồ sơ sức khỏe và mức độ vận động phù hợp.

## Quick gut

* [ ] Rule
* [x] Workflow
* [ ] Agent

---

# Problem Card #3 — Chế độ ăn uống cá nhân hóa

## Problem 1 câu

Người dùng khó xây dựng thực đơn phù hợp với tình trạng sức khỏe và bệnh nền của mình.

## Actor

Người ăn kiêng, tiểu đường hoặc huyết áp cao.

## Current workflow

1. Tra cứu thực phẩm trên Google
2. Tự xây dựng thực đơn
3. Kiểm tra lượng dinh dưỡng
4. Điều chỉnh thủ công

## Bottleneck

Thông tin dinh dưỡng rời rạc và khó cá nhân hóa.

## Success metric

Giảm thời gian lên thực đơn từ khoảng 45 phút xuống dưới 20 phút.

## AI hypothesis

AI gợi ý thực đơn và danh sách thực phẩm phù hợp với hồ sơ sức khỏe.

## Quick gut

* [ ] Rule
* [x] Workflow
* [ ] Agent

---

# Card muốn pitch nhất

Chuẩn hóa hồ sơ bệnh án.

## Vì sao

Đây là bài toán có workflow rõ nhất, có thể đo được thời gian trước/sau và AI phù hợp để hỗ trợ OCR, chuẩn hóa dữ liệu và tổng hợp thông tin.

## Câu hỏi muốn nhóm challenge

* Mức độ chính xác của OCR có đủ dùng không?
* Có cần AI Agent hay chỉ cần Workflow?
* Boundary an toàn cho dữ liệu sức khỏe là gì?
