# Thư mục đề cương học phần đề xuất mới

Thư mục này chứa các đề cương chi tiết (syllabus) cho các học phần **mới hoặc được tái cấu trúc** theo khung chương trình đào tạo AI-native giai đoạn 2026–2030.

---

## Danh sách học phần đề xuất

### Nhóm 1: Phát triển ứng dụng Web AI-native (thay thế CSE122 + CSE124)

Thay vì dạy cú pháp HTML/CSS/JS từ đầu, hai học phần mới này tái định hướng hoàn toàn: sinh viên dùng AI agent để tạo giao diện ngay từ đầu, trọng tâm là **kiến trúc hệ thống**, **tích hợp AI** và **triển khai cloud**.

| Mã đề xuất | Tên học phần | Tín chỉ | Học kỳ gợi ý | Áp dụng cho ngành |
|---|---|---|---|---|
| `WEB-A1` | [Phát triển web hiện đại với AI agent](./WEB-A1_Phat_Trien_Web_Hien_Dai_Voi_AI_Agent.md) | 3 | HK3 | KTPM, CNTT, HTTT, TTNT |
| `WEB-A2` | [Tích hợp AI vào ứng dụng web & triển khai cloud](./WEB-A2_Tich_Hop_AI_Va_Trien_Khai_Cloud.md) | 3 | HK4 | KTPM, CNTT, HTTT, TTNT |

> **Lưu ý về ngành ANM:** Hai học phần trên không áp dụng nguyên cho ANM. Ngành ANM sẽ học biến thể riêng tập trung vào **bảo mật ứng dụng web** (Burp Suite, OWASP, penetration testing) — xem đề cương riêng khi có.

### Nhóm 2: Công nghệ phần mềm điều hướng bởi AI (thay thế CSE481)

Tái cấu trúc hoàn toàn môn Công nghệ phần mềm truyền thống: không còn viết SRS bằng tay, vẽ UML trong Visio hay làm Gantt chart trong Excel — thay bằng quy trình SDLC **có AI hỗ trợ ở mọi bước**, từ phân tích yêu cầu đến CI/CD.

| Mã đề xuất | Tên học phần | Tín chỉ | Học kỳ gợi ý | Áp dụng cho ngành |
|---|---|---|---|---|
| `SE-AI` | [Công nghệ phần mềm điều hướng bởi AI](./SE-AI_Cong_Nghe_Phan_Mem_Dieu_Huong_Boi_AI.md) | 3 | HK4 | KTPM (bắt buộc), CNTT (khuyến nghị) |


---

## Nguyên tắc thiết kế chung

Tất cả các đề cương trong thư mục này tuân thủ các nguyên tắc sau:

1. **AI-first workflow:** Sinh viên sử dụng công cụ AI (Cursor, GitHub Copilot, v0.dev) như một phần bắt buộc của quy trình làm việc, không phải tùy chọn.
2. **Không học thuộc cú pháp:** Không có bài kiểm tra yêu cầu viết code từ đầu trong điều kiện không có AI/Internet.
3. **Đánh giá dựa trên tư duy:** Kiểm tra năng lực thông qua oral defense, live debugging và phân tích kiến trúc — không phải sản phẩm cuối.
4. **Bắt buộc nộp prompt log:** Mọi đồ án phải nộp kèm nhật ký tương tác với AI, chấm điểm tư duy prompt.
5. **Kết quả là hệ thống thực:** Đồ án phải được deploy lên cloud thực tế (Vercel, Railway, AWS, GCP), không phải chạy trên localhost.

---

## Cấu trúc đề cương chuẩn

Mỗi đề cương trong thư mục này bao gồm:

1. **Thông tin chung** — mã, tín chỉ, tiên quyết, công cụ bắt buộc
2. **Chuẩn đầu ra** — kiến thức, kỹ năng, thái độ
3. **Nội dung theo tuần** — 15 tuần, cấu trúc 3 giai đoạn (Foundation → Core → Capstone)
4. **Phương pháp đánh giá** — không thi viết, tập trung oral defense và live demo
5. **Tài liệu & công cụ** — ưu tiên tài liệu official, không giáo trình lỗi thời

---

*Cập nhật lần cuối: 04/2026 — Nhóm rà soát CTĐT khoa CNTT, Trường Đại học Thủy lợi.*
