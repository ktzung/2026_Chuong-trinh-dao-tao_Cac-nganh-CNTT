# BÁO CÁO RÀ SOÁT VÀ ĐỀ XUẤT NÂNG CẤP CHƯƠNG TRÌNH ĐÀO TẠO
## NGÀNH CÔNG NGHỆ THÔNG TIN (CNTT) — Tầm nhìn 2026–2030

> **Kính gửi:** Hội đồng Khoa học & Đào tạo Khoa CNTT
> **Người thực hiện:** Tổ Rà soát Chương trình
> **Thời gian:** Tháng 4/2026

---

## I. TÓM TẮT ĐỀ XUẤT

Ngành CNTT hiện đang rơi vào tình trạng "biết mỗi thứ một ít" — sinh viên ra trường không đủ sâu để làm System Engineer, không đủ kiến thức AI để làm AI Engineer, không đủ kỹ năng Cloud để làm DevOps. Đây là hệ quả của việc chương trình cố gắng bao phủ quá rộng mà không có định vị rõ ràng.

Trong kỷ nguyên AI, ngành CNTT cần tái định vị thành **"Cloud & Intelligent Systems Engineering"** — đào tạo những kỹ sư có thể vận hành, mở rộng và bảo vệ các hệ thống phức tạp mà AI tạo ra. Khi AI viết hàng triệu dòng code mỗi ngày, thế giới cần những kỹ sư biết cách **triển khai, giám sát và tối ưu hóa** các hệ thống đó.

---

## II. CHẨN ĐOÁN CHƯƠNG TRÌNH HIỆN TẠI

### Điểm mạnh cần bảo tồn
- Nền tảng hệ thống vững: Kiến trúc máy tính, HĐH, Mạng máy tính.
- Có các môn học về dữ liệu và AI cơ bản (Phân tích dữ liệu, Trí tuệ nhân tạo).
- Cấu trúc chương trình có nhiều track chuyên sâu linh hoạt.

### Điểm yếu nghiêm trọng
1. **AI chỉ là môn "Nhập môn" duy nhất:** CSE492 (Trí tuệ nhân tạo) ở HK4 chỉ là tổng quan lý thuyết — trong khi thị trường cần AI Engineering.
2. **Không có Cloud/DevOps bắt buộc:** 100% doanh nghiệp CNTT dùng Cloud, nhưng chương trình không có một môn Cloud nào là bắt buộc trong năm 1–3.
3. **Các môn lập trình ứng dụng mang tính thừa:** Lập trình Windows, Java app — AI làm tốt hơn sinh viên.
4. **Phân tán, thiếu trục cốt lõi:** Sinh viên không có một "bản sắc" rõ ràng sau 4 năm.

---

## III. PHÂN TÍCH RỦI RO AI — TỪNG HỌC PHẦN

| Học phần | Mã HP | TC | Rủi ro AI | Quyết định đề xuất |
|----------|-------|----|-----------|-------------------|
| Nhập môn lập trình | CSE111 | 3 | 🟡 Trung bình | Giữ — đổi sang Computational Thinking + Python |
| Lập trình nâng cao | CSE205 | 3 | 🟡 Trung bình | Giữ — chuyển sang Code Review AI output |
| Toán rời rạc | CSE203 | 3 | 🟢 Thấp | Giữ nguyên |
| CTDL & Giải thuật | CSE281 | 3 | 🟢 Thấp | Giữ — thêm bài tập đánh giá thuật toán AI |
| Kiến trúc máy tính | CSE370 | 3 | 🟢 Thấp | Giữ nguyên |
| Cơ sở dữ liệu | CSE484 | 3 | 🟡 Trung bình | Giữ — thêm Vector DB, NoSQL |
| Mạng máy tính | CSE489 | 3 | 🟢 Thấp | Giữ — thêm Software-Defined Networking |
| Lập trình hướng đối tượng | CSE116 | 3 | 🟡 Trung bình | Giữ — gộp với Design Patterns |
| Hệ điều hành | CSE482 | 3 | 🟢 Thấp | Giữ — thêm Linux Kernel, Container internals |
| Phát triển UD Web cơ bản | CSE122 | 3 | 🔴 **Cao** | **Gộp hoặc giảm** — AI làm HTML/CSS trong vài giây |
| Điện toán đám mây | CSE121 | 3 | 🟢 Thấp | Giữ — **nâng thành BẮT BUỘC** ở HK3, không phải HK4 |
| Phân tích dữ liệu | CSE131 | 3 | 🟡 Trung bình | Giữ — tích hợp Python Data Stack (Pandas, SQL) |
| Trí tuệ nhân tạo | CSE492 | 3 | 🟡 Trung bình | **Nâng cấp toàn diện** — tách thành ML Foundations |
| Phân tích & thiết kế HT | CSE123 | 3 | 🟡 Trung bình | Giữ — thêm AI-assisted System Design |
| Công nghệ phần mềm | CSE481 | 3 | 🔴 **Cao** | Cập nhật sang AI-Driven SDLC |
| Tối ưu hóa | CSE414 | 3 | 🟡 Trung bình | Giữ — liên kết với MLOps optimization |
| Học máy | CSE445 | 3 | 🟢 Thấp | Giữ — **nâng thành BẮT BUỘC** |
| Phát triển UD Web nâng cao | CSE124 | 3 | 🟡 Trung bình | Giữ — chuyển hướng sang Cloud-Native Web |
| Thuật toán ứng dụng | CSE426 | 3 | 🟢 Thấp | Giữ nguyên |
| An toàn & bảo mật TT | CSE488 | 3 | 🟢 Thấp | Giữ — thêm Cloud Security |
| Khai phá dữ liệu | CSE404 | 3 | 🟡 Trung bình | Giữ — thêm AI-powered Data Mining |
| XLý ngôn ngữ tự nhiên | CSE458 | 3 | 🟢 Thấp | **Nâng thành bắt buộc** — cốt lõi để hiểu LLM |
| Thị giác máy tính | CSE132 | 3 | 🟢 Thấp | Giữ — tự chọn |
| Phát triển UD hướng dịch vụ | CSE106 | 3 | 🟡 Trung bình | Giữ — chuyển sang API-first & Microservices |
| Kết nối vạn vật | CSE475 | 3 | 🟢 Thấp | Giữ — tự chọn |

---

## IV. HỌC PHẦN ĐỀ XUẤT LOẠI BỎ HOẶC GỘP

### 4.1. Phát triển ứng dụng Web cơ bản (CSE122 — 3 TC) → GỘP/GIẢM

**Luận cứ:** HTML/CSS/JS cơ bản có thể học trong 2 tuần với AI. v0.dev tạo toàn bộ UI từ text trong vài giây. 45 tiết dạy nội dung này là lãng phí trực tiếp tài nguyên đào tạo ngành CNTT — vốn cần đi sâu vào hệ thống và cơ sở hạ tầng.

**Thay thế:** Phân bổ TC này vào **DevOps & Cloud Fundamentals**.

### 4.2. Trí tuệ nhân tạo (CSE492) ở dạng "Nhập môn" → NÂNG CẤP TRIỆT ĐỂ

**Luận cứ:** Một môn AI nhập môn 3 TC ở HK4 không đủ trang bị cho sinh viên trong kỷ nguyên AI. Cần tách thành: (1) Machine Learning Foundations, (2) AI Engineering & LLM Application — tối thiểu 6 TC bắt buộc.

---

## V. ĐỀ XUẤT CHƯƠNG TRÌNH ĐÀO TẠO MỚI (THAM KHẢO — 140 TC)

### KHỐI I: GIÁO DỤC ĐẠI CƯƠNG (37 TC — GIỮ NGUYÊN)

*(Giữ nguyên cấu trúc hiện tại. Riêng CSE105 "Kỹ năng số & Khai thác AI" cần nâng cao nội dung Prompt Engineering từ mức "biết dùng" lên mức "hiểu giới hạn và kiểm chứng AI".)*

---

### KHỐI II: NỀN TẢNG KHOA HỌC MÁY TÍNH (27 TC)

| TT | Học phần | TC | HK | Ghi chú thay đổi |
|----|----------|----|----|-----------------|
| 1 | Nhập môn lập trình & Tư duy máy tính | 3 | 1 | Python + Computational Thinking; cấm AI 4 tuần đầu |
| 2 | Toán rời rạc | 3 | 2 | Giữ nguyên |
| 3 | CTDL & Giải thuật | 3 | 2 | Thêm bài tập: Đánh giá thuật toán do AI sinh ra |
| 4 | Lập trình nâng cao & OOP | 3 | 2 | Gộp CSE205 + CSE116; học qua Code Review |
| 5 | Kiến trúc máy tính & Hệ điều hành | 3 | 2 | Gộp — thêm Container internals, Virtualization |
| 6 | Cơ sở dữ liệu & Hệ quản trị CSDL | 3 | 3 | SQL + NoSQL + Vector DB |
| 7 | Mạng máy tính & Hạ tầng Cloud | 3 | 3 | Tích hợp Cloud Networking (VPC, CDN, Load Balancer) |
| 8 | Phân tích & Thiết kế hệ thống | 3 | 4 | Thêm AI-assisted System Design |
| 9 | Xác suất thống kê ứng dụng ML | 3 | 3 | Tăng bài tập Python Statistics |

---

### KHỐI III: LÕI CNTT & AI ENGINEERING (27 TC)

| TT | Học phần | TC | HK | Ghi chú thay đổi |
|----|----------|----|----|-----------------|
| 10 | **Điện toán đám mây & DevOps** | 3 | 3 | **BẮT BUỘC TỪ HK3** — Docker, K8s, AWS/GCP cơ bản |
| 11 | **Machine Learning Foundations** | 3 | 4 | Tách từ CSE492 — Supervised/Unsupervised, evaluation |
| 12 | **AI Engineering & LLM Application** | 3 | 5 | **Môn mới BẮT BUỘC** — RAG, API LLM, Prompt Engineering nâng cao |
| 13 | **AI Agent & Workflow Automation** | 3 | 6 | **Môn mới** — LangChain, AutoGen, Multi-agent orchestration |
| 14 | Phân tích dữ liệu & Data Engineering | 3 | 4 | Python stack + ETL pipeline cơ bản |
| 15 | Kiến trúc phần mềm & Microservices | 3 | 4 | API-first, Event-driven, Domain-driven design |
| 16 | An toàn & Bảo mật hệ thống | 3 | 5 | Thêm Cloud Security, OWASP, DevSecOps cơ bản |
| 17 | **Hệ thống phân tán** | 3 | 5 | **Môn mới BẮT BUỘC** — Distributed computing, CAP theorem, Kafka |
| 18 | Công nghệ phần mềm (AI-Driven) | 3 | 4 | Cập nhật AI-SDLC: sinh tài liệu, test tự động |

---

### KHỐI IV: CHUYÊN NGÀNH — TỰ CHỌN (15 TC, chọn 1 track)

**Track A — AI Systems & MLOps:**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 19 | Deep Learning & Neural Architecture | 3 | 6 |
| 20 | MLOps & Model Deployment | 3 | 6 |
| 21 | Xử lý ngôn ngữ tự nhiên | 3 | 6 |
| 22 | Thị giác máy tính | 3 | 7 |
| 23 | AI tạo sinh & Mô hình ngôn ngữ lớn | 3 | 7 |

**Track B — Cloud & Infrastructure:**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 19 | Hạ tầng dưới dạng mã (Terraform/Ansible) | 3 | 6 |
| 20 | Giám sát & Quan sát hệ thống (SRE) | 3 | 6 |
| 21 | Kiến trúc Serverless & Edge Computing | 3 | 6 |
| 22 | Kết nối vạn vật & Edge AI | 3 | 7 |
| 23 | Thiết kế hệ thống hiệu năng cao | 3 | 7 |

**Track C — Cybersecurity:**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 19 | Nhập môn An toàn bảo mật TT | 3 | 6 |
| 20 | AI Security & LLM Security | 3 | 6 |
| 21 | An ninh mạng ứng dụng | 3 | 6 |
| 22 | Điều tra số | 3 | 7 |
| 23 | Quản lý an toàn thông tin | 3 | 7 |

---

### KHỐI V: THỰC TẬP & ĐỒ ÁN (14 TC)

| TT | Học phần | TC | HK | Yêu cầu mới |
|----|----------|----|----|------------|
| 24 | Thực tập doanh nghiệp | 4 | 8 | Báo cáo AI Usage — SV dùng AI như thế nào trong công việc thực tế |
| 25 | Đồ án tốt nghiệp | 10 | 8 | Phải gồm: Kiến trúc hệ thống + Deployment thực tế + Oral Defense 30 phút |

---

## VI. ĐỔI MỚI PHƯƠNG PHÁP ĐÁNH GIÁ

| Học phần loại | Phương pháp kiểm tra mới |
|---------------|------------------------|
| Môn nền tảng (Thuật toán, Mạng, HĐH) | Kết hợp: bài thi lý thuyết (40%) + Lab thực hành có đánh giá (60%) |
| Môn kỹ thuật (DevOps, Cloud, AI Engineering) | Nộp project thật + Oral Defense (GV hỏi về kiến trúc, lý do quyết định) |
| Môn đồ án | Bắt buộc Oral Defense + nộp Prompt Log (lịch sử giao tiếp với AI) |
| Tất cả các môn | **Cấm thi viết code trên giấy** — không thực tế và không đo được năng lực thật |

---

## VII. ĐỊNH HƯỚNG NGHỀ NGHIỆP ĐẦU RA (2030)

| Vị trí | Kỹ năng cốt lõi được đào tạo |
|--------|------------------------------|
| Platform Engineer | Cloud, Kubernetes, CI/CD, IaC |
| AI Engineer | LLM Integration, RAG, AI Agent |
| Cloud Solutions Architect | Cloud Design Patterns, Multi-cloud |
| Data Engineer | ETL, Spark, Data Pipeline |
| Site Reliability Engineer | Monitoring, Observability, SLA |

---

## VIII. KẾT LUẬN VÀ KIẾN NGHỊ

Trong kỷ nguyên AI, ngành CNTT không nên đào tạo coder — mà phải đào tạo **"Builders of Intelligent Infrastructure"**: những người biết dựng lên và vận hành nền tảng mà cả doanh nghiệp lẫn AI Agent hoạt động trên đó.

**Kiến nghị cụ thể:**
1. Nâng **Điện toán đám mây (CSE121)** lên HK3 và thành **học phần bắt buộc**.
2. **Tách CSE492 (AI)** thành 2 môn: ML Foundations (HK4) + AI Engineering & LLM (HK5).
3. Bổ sung **Hệ thống phân tán** như môn bắt buộc.
4. Bổ sung **AI Agent & Workflow Automation** như môn bắt buộc HK6.
5. Áp dụng **Oral Defense** bắt buộc cho tất cả học phần đồ án.

---
*Tài liệu tham khảo: CMU CS Course Catalog 2024; NUS Computing Curriculum 2025; AWS Educate Program; VietnamWorks IT Hiring Report Q1/2026.*
