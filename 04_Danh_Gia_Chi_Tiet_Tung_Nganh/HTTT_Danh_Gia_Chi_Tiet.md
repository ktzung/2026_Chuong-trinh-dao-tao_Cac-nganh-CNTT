# BÁO CÁO RÀ SOÁT VÀ ĐỀ XUẤT NÂNG CẤP CHƯƠNG TRÌNH ĐÀO TẠO
## Ngành hệ thống thông tin (HTTT) — Tầm nhìn 2026–2030

> **Kính gửi:** Hội đồng Khoa học & Đào tạo Khoa CNTT
> **Người thực hiện:** Tổ Rà soát Chương trình
> **Thời gian:** Tháng 4/2026

---

## I. Tóm tắt đề xuất

Ngành Hệ thống Thông tin có lợi thế cạnh tranh độc đáo trong kỷ nguyên AI: **hiểu biết về nghiệp vụ tổ chức**. AI có thể xử lý dữ liệu, nhưng không thể tự hiểu quy trình kinh doanh phức tạp của một doanh nghiệp cụ thể, không thể tự quyết định KPI nào quan trọng hơn, không thể tự giao tiếp với stakeholders để khai thác yêu cầu. Đây chính là "vùng xanh" (safe zone) của HTTT.

Tuy nhiên, chương trình hiện tại vẫn đang đào tạo sinh viên theo hướng **"Quản lý cơ sở dữ liệu truyền thống"** — một kỹ năng đang bị thay thế nhanh chóng bởi AI. Đề xuất tái định vị ngành HTTT thành **"Data & AI-Powered Enterprise Systems"**: đào tạo những chuyên gia kết nối dữ liệu doanh nghiệp với các hệ thống AI thông minh.

---

## II. Chẩn đoán chương trình hiện tại

### Điểm mạnh cần bảo tồn
- Các môn liên quan đến nghiệp vụ: Phân tích & Thiết kế HTTT, Phân tích dữ liệu.
- Môn Khai phá dữ liệu, Hệ thống kinh doanh thông minh — nền tảng tốt, cần nâng cấp.
- Có Hệ thống thông tin thông minh (CSE125) — đây là hướng đi đúng, cần đầu tư thêm.

### Điểm yếu nghiêm trọng
1. **Thiếu Data Engineering:** Không có môn nào dạy xây dựng pipeline dữ liệu quy mô lớn (ETL/ELT, Spark, Airflow).
2. **Business Intelligence cổ điển:** Dạy làm dashboard tĩnh trong khi xu hướng là "Chat with Data" — hỏi báo cáo bằng ngôn ngữ tự nhiên.
3. **Thiếu Cloud cho Dữ liệu:** Snowflake, BigQuery, AWS Redshift đang là chuẩn của doanh nghiệp, nhưng chương trình không đề cập.
4. **Các môn lập trình ứng dụng không cần thiết:** HTTT không nên tập trung vào viết Web app — đó là việc của KTPM.

---

## III. Phân tích rủi ro AI — từng học phần

| Học phần | Mã HP | TC | Rủi ro AI | Quyết định đề xuất |
|----------|-------|----|-----------|-------------------|
| Nhập môn lập trình | CSE111 | 3 | 🟡 Trung bình | Giữ — tập trung vào Python cho phân tích dữ liệu |
| Lập trình nâng cao | CSE205 | 3 | 🟡 Trung bình | Giữ — hướng sang scripting & automation |
| CTDL & Giải thuật | CSE281 | 3 | 🟢 Thấp | Giữ nguyên |
| Kiến trúc máy tính | CSE370 | 3 | 🟢 Thấp | Giữ nguyên |
| Cơ sở dữ liệu | CSE484 | 3 | 🟡 Trung bình | Giữ — thêm Vector DB, Data Modeling nâng cao |
| Mạng máy tính | CSE489 | 3 | 🟢 Thấp | Giữ nguyên |
| Lập trình hướng đối tượng | CSE116 | 3 | 🟡 Trung bình | Giữ ở mức nhẹ — HTTT không cần OOP sâu |
| Hệ điều hành | CSE482 | 3 | 🟢 Thấp | Giữ nguyên |
| Phát triển UD Web cơ bản | CSE122 | 3 | 🔴 **Cao** | **Cân nhắc loại bỏ** — HTTT không cần làm Web frontend |
| Điện toán đám mây | CSE121 | 3 | 🟢 Thấp | **Nâng thành BẮT BUỘC** ở HK3; thêm Cloud Data services |
| Phân tích dữ liệu | CSE131 | 3 | 🟡 Trung bình | Giữ — nâng cấp sang Python Data Stack hoàn chỉnh |
| Trí tuệ nhân tạo | CSE492 | 3 | 🟡 Trung bình | **Nâng cấp** sang AI for Business Applications |
| Phân tích & thiết kế HT | CSE123 | 3 | 🟡 Trung bình | Giữ — thêm AI-assisted process mapping |
| Công nghệ phần mềm | CSE481 | 3 | 🔴 **Cao** | Cập nhật sang AI-Driven Project Management |
| Hệ quản trị CSDL | CSE486 | 3 | 🟡 Trung bình | Giữ — thêm Cloud Database (RDS, BigQuery) |
| Khai phá dữ liệu | CSE404 | 3 | 🟡 Trung bình | Giữ — tích hợp AI-powered analytics |
| HTTT thông minh | CSE125 | 3 | 🟢 Thấp | **Mở rộng** — quan trọng, cần đầu tư thêm |
| Quản lý dự án CNTT | CSE392 | 3 | 🟡 Trung bình | Giữ — thêm AI PM tools |
| Hệ thống kinh doanh thông minh | CSE411 | 3 | 🟡 Trung bình | **Nâng cấp** sang Conversational BI & Generative BI |
| Tính toán mềm | CSE452 | 3 | 🟡 Trung bình | Chuyển sang tự chọn nếu cần giải phóng TC |
| Thiết kế HT hiệu năng cao | CSE129 | 3 | 🟢 Thấp | Giữ — rất quan trọng, AI không thay thế được |
| Quản trị HTTT | CSE405 | 3 | 🟢 Thấp | Giữ — thêm AI Governance framework |
| Học sâu & ứng dụng | CSE429 | 3 | 🟢 Thấp | Giữ — tự chọn, khuyến nghị mạnh |
| Phân tích chuỗi thời gian | CSE399 | 3 | 🟢 Thấp | Giữ — rất có giá trị cho HTTT |
| AI tạo sinh & LLMs | CSE134 | 3 | 🟢 Thấp | **Nâng thành bắt buộc** cho track AI |
| Kho dữ liệu | CSE127 | 3 | 🟢 Thấp | Giữ — **nâng thành bắt buộc**, thêm Cloud DW |

---

## IV. Học phần đề xuất loại bỏ hoặc gộp

### 4.1. Phát triển ứng dụng Web cơ bản (CSE122 — 3 TC) → TÁI ĐỊNH HƯỚNG CHO HTTT

**Luận cứ:**
- Web không phải kỹ năng lỗi thời — đây vẫn là phương tiện chủ yếu để trình bày và tương tác với dữ liệu. Dashboard phân tích, báo cáo tương tác, hệ thống ERP/CRM đều chạy trên web.
- Vấn đề là **cách dạy**: ngành HTTT không cần học HTML/CSS thuần 45 tiết. Dùng AI agent (v0.dev, Cursor) để tạo UI trong vài giây, rồi tập trung vào phần HTTT thực sự cần: kết nối API nghiệp vụ, data visualization, tích hợp "chat with data".
- Sinh viên HTTT cần **biết web ở tầng tích hợp**, không phải tầng giao diện.

**Thay thế:** Gộp Web cơ bản + Web nâng cao thành **AI-native web & data application** (6 TC) — tập trung data dashboard (Streamlit, Grafana), REST API tới ERP/CRM, AI-powered BI ("hỏi báo cáo bằng ngôn ngữ tự nhiên"), không phải cú pháp HTML.


### 4.2. Tính toán mềm (CSE452 — 3 TC) → ĐỀ XUẤT CHUYỂN TỰ CHỌN

**Luận cứ:**
- Logic mờ (Fuzzy Logic) và mạng nơ-ron tính toán mềm đã bị supersede bởi Deep Learning hiện đại.
- Kiến thức này có tính lịch sử nhưng không còn là kỹ năng cốt lõi của thị trường.
- Giải phóng 3 TC để bổ sung **"LLM Engineering cho Doanh nghiệp"**.

---

## V. Đề xuất chương trình đào tạo mới (tham khảo — 140 TC)

### Khối I: Giáo dục đại cương (37 TC — giữ nguyên)

*(Bao gồm tất cả các môn Lý luận chính trị, Toán, Tiếng Anh, Giáo dục quốc phòng. Riêng CSE105 cần tăng nội dung AI Literacy từ "dùng AI cơ bản" lên "hiểu hallucination, kiểm chứng, và đạo đức AI".)*

---

### Khối II: Nền tảng CNTT & dữ liệu (27 TC)

| TT | Học phần | TC | HK | Ghi chú thay đổi |
|----|----------|----|----|-----------------|
| 1 | Lập trình Python cho Phân tích dữ liệu | 3 | 1 | Thay CSE111 — học Python ngay từ đầu với ứng dụng Data |
| 2 | CTDL & Giải thuật | 3 | 2 | Giữ nguyên |
| 3 | Cơ sở dữ liệu & Thiết kế dữ liệu | 3 | 2 | SQL + Relational Design + NoSQL cơ bản |
| 4 | Mạng máy tính & Hạ tầng | 3 | 2 | Giữ — thêm API protocols (REST, GraphQL) |
| 5 | Kiến trúc máy tính & HĐH | 3 | 2 | Giữ nguyên |
| 6 | Lập trình hướng đối tượng (nhẹ) | 3 | 3 | Chỉ dạy OOP cơ bản, tập trung Python OOP |
| 7 | Phân tích & Thiết kế HTTT | 3 | 3 | Thêm BPMN 2.0, Service Design, AI-assisted mapping |
| 8 | Toán rời rạc | 3 | 2 | Giữ nguyên |
| 9 | Xác suất thống kê ứng dụng | 3 | 3 | Liên kết chặt với Data Analysis |

---

### Khối III: Lõi hệ thống thông tin & AI (30 TC)

| TT | Học phần | TC | HK | Ghi chú thay đổi |
|----|----------|----|----|-----------------|
| 10 | **Phân tích dữ liệu & Python Data Stack** | 3 | 3 | Nâng cấp CSE131: Pandas, NumPy, SQL, Visualization |
| 11 | **Cloud Computing & Cloud Data Services** | 3 | 3 | **BẮT BUỘC TỪ HK3** — AWS S3, RDS, BigQuery, Azure Data |
| 12 | **Data Engineering & ETL Pipeline** | 3 | 4 | **Môn mới** — Airflow, dbt, Spark cơ bản, data pipeline |
| 13 | **Kho dữ liệu & Data Warehouse Hiện đại** | 3 | 4 | Snowflake, BigQuery, Dimensional Modeling |
| 14 | **Học máy ứng dụng cho HTTT** | 3 | 4 | Supervised/Unsupervised learning, sklearn, model evaluation |
| 15 | **AI Engineering cho Doanh nghiệp** | 3 | 5 | **Môn mới** — RAG, API LLM, "Chat with Data", xây Chatbot nội bộ |
| 16 | Hệ thống kinh doanh thông minh (nâng cấp) | 3 | 5 | Generative BI, NLP-powered dashboards, Power BI + Copilot |
| 17 | Hệ quản trị CSDL & Cloud Database | 3 | 4 | Thêm Cloud DB: RDS, MongoDB Atlas, Redis |
| 18 | Khai phá dữ liệu & AI Analytics | 3 | 5 | Tích hợp AutoML, AI-powered clustering |
| 19 | Thiết kế HTTT hiệu năng nâng cao | 3 | 6 | Giữ — rất quan trọng cho hệ thống lớn |

---

### Khối IV: Hệ thống doanh nghiệp & chuyên ngành (15 TC, chọn 1 track)

**Track A — AI & Advanced Analytics:**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 20 | Phân tích chuỗi thời gian | 3 | 6 |
| 21 | AI tạo sinh & LLMs cho Doanh nghiệp | 3 | 6 |
| 22 | LLM Agent cho Tự động hóa Quy trình | 3 | 6 |
| 23 | Kho dữ liệu Vector & Semantic Search | 3 | 7 |
| 24 | Quản trị Dữ liệu & AI Governance | 3 | 7 |

**Track B — Enterprise Systems & Transformation:**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 20 | ERP, CRM & Hệ thống doanh nghiệp | 3 | 6 |
| 21 | Tích hợp hệ thống & API Middleware | 3 | 6 |
| 22 | Chuyển đổi số & Kiến trúc doanh nghiệp | 3 | 6 |
| 23 | Quản lý dự án CNTT | 3 | 7 |
| 24 | Pháp lý, Đạo đức & An toàn dữ liệu | 3 | 7 |

**Track C — Cloud & Data Platform:**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 20 | Điện toán đám mây nâng cao | 3 | 6 |
| 21 | Real-time Data Processing (Kafka, Flink) | 3 | 6 |
| 22 | An toàn & Bảo mật hệ thống dữ liệu | 3 | 6 |
| 23 | Blockchain ứng dụng trong HTTT | 3 | 7 |
| 24 | Kết nối vạn vật & Edge Data Systems | 3 | 7 |

---

### Khối V: Thực tập & đồ án (14 TC)

| TT | Học phần | TC | HK | Yêu cầu mới |
|----|----------|----|----|------------|
| 25 | Thực tập doanh nghiệp | 4 | 8 | Báo cáo: SV phải giải thích đã dùng AI/data tools gì trong công việc |
| 26 | Đồ án tốt nghiệp | 10 | 8 | Bắt buộc: Giải quyết bài toán nghiệp vụ thực tế + hệ thống dữ liệu + AI integration + Oral Defense |

---

## VI. Đổi mới phương pháp đánh giá

| Loại môn | Phương pháp kiểm tra mới |
|----------|------------------------|
| Môn phân tích & thiết kế | Case study từ doanh nghiệp thực + Oral Defense giải thích quyết định thiết kế |
| Môn Data Engineering | Nộp pipeline chạy thật trên Cloud (miễn phí tier) thay vì báo cáo PDF |
| Môn AI Engineering | Demo live Chatbot hoặc RAG system; GV hỏi sâu về kiến trúc |
| Đồ án | 5 tiêu chí chấm: Bài toán nghiệp vụ + Thiết kế dữ liệu + Triển khai + Đo KPI + Oral Defense |

---

## VII. Định hướng nghề nghiệp đầu ra (2030)

| Vị trí | Kỹ năng cốt lõi |
|--------|-----------------|
| Business Analyst (AI-augmented) | Phân tích yêu cầu + LLM-assisted documentation |
| Data Analyst / Data Engineer | Python + SQL + Cloud DW + ETL |
| AI-powered BI Developer | Generative BI, "Chat with Data" tools |
| Solution Architect (Information Systems) | Cloud + Data Architecture + Enterprise Integration |
| Digital Transformation Consultant | AI strategy + Business Process Redesign |

---

## VIII. Kết luận và kiến nghị

HTTT là ngành có **"vùng an toàn" cao nhất trong kỷ nguyên AI** — vì AI không thể tự hiểu nghiệp vụ tổ chức. Nhưng điều đó không có nghĩa là chương trình có thể đứng yên. Sinh viên HTTT cần được trang bị để **làm việc cùng AI, cung cấp ngữ cảnh nghiệp vụ cho AI**, và biến dữ liệu tổ chức thành tài sản số.

**Kiến nghị cụ thể:**
1. **Loại bỏ** Phát triển ứng dụng Web cơ bản (CSE122) khỏi chương trình HTTT.
2. **Chuyển tự chọn** Tính toán mềm (CSE452); thay bằng LLM Engineering cho Doanh nghiệp.
3. **Nâng thành bắt buộc:** Điện toán đám mây (HK3), Kho dữ liệu, Học máy ứng dụng.
4. **Bổ sung 2 môn mới bắt buộc:** Data Engineering & ETL Pipeline; AI Engineering cho Doanh nghiệp.
5. **Cải cách đồ án:** Bắt buộc phải giải quyết bài toán nghiệp vụ thực tế, có triển khai hệ thống thật.

---
*Tài liệu tham khảo: ASIS&T IS Curriculum Guidelines 2024; NUS Information Systems Major; MIT Sloan Data & Decisions Track; Gartner Data & Analytics Trends 2025.*
