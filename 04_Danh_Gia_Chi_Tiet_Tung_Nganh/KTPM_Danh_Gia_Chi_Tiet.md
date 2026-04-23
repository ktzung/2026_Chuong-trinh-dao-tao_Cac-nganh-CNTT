# BÁO CÁO RÀ SOÁT VÀ ĐỀ XUẤT NÂNG CẤP CHƯƠNG TRÌNH ĐÀO TẠO
## Ngành kỹ thuật phần mềm (KTPM) — Tầm nhìn 2026–2030

> **Kính gửi:** Hội đồng Khoa học & Đào tạo Khoa CNTT
> **Người thực hiện:** Tổ Rà soát Chương trình
> **Thời gian:** Tháng 4/2026

---

## I. Tóm tắt đề xuất

Ngành Kỹ thuật Phần mềm đứng trước nguy cơ đào thải lớn nhất. Các công cụ như GitHub Copilot, Cursor, Devin đã "hàng hóa hóa" kỹ năng viết code thông thường. Chương trình hiện tại đang đào tạo "Junior Developer" — một vị trí đang co hẹp nhanh. Báo cáo đề xuất tái cơ cấu sang đào tạo **"AI-Assisted Software Architect"**: kỹ sư thiết kế, tích hợp và triển khai hệ thống trong môi trường AI-first.

---

## II. Chẩn đoán chương trình hiện tại

### Điểm mạnh cần bảo tồn
- Nền tảng CS vững (Thuật toán, CTDL, HĐH, Mạng) — AI không thay thế được tư duy hệ thống tầng thấp.
- Có Design Patterns, Kiểm thử phần mềm — nền tảng quan trọng cần giữ và nâng cấp.

### Điểm yếu nghiêm trọng
1. **Quá nặng kỹ năng gõ mã:** Lập trình Windows, Java, Web cơ bản — AI làm được toàn bộ.
2. **Thiếu hoàn toàn tầng AI Engineering:** Không có môn nào dạy tích hợp LLM, RAG, AI Agent.
3. **DevOps/Cloud ở mức tối thiểu:** 100% doanh nghiệp dùng Cloud nhưng chương trình gần như bỏ qua.
4. **Đánh giá lỗi thời:** Bài "viết app quản lý X bằng Java" — ChatGPT hoàn thành trong 2 phút.

---

## III. Phân tích rủi ro AI — từng học phần

| Học phần | Mã HP | TC | Rủi ro AI | Quyết định đề xuất |
|----------|-------|----|-----------|-------------------|
| Nhập môn lập trình | CSE111 | 3 | 🟡 Trung bình | Giữ — đổi phương pháp dạy (Computational Thinking) |
| Lập trình nâng cao | CSE205 | 3 | 🟡 Trung bình | Giữ — chuyển sang Code Review AI output |
| Lập trình hướng đối tượng | CSE116 | 3 | 🟡 Trung bình | Giữ — tích hợp thêm Design Patterns sâu |
| Cấu trúc dữ liệu & GT | CSE281 | 3 | 🟢 Thấp | Giữ nguyên, thêm bài tập đánh giá thuật toán AI |
| Mạng máy tính | CSE489 | 3 | 🟢 Thấp | Giữ nguyên |
| Hệ điều hành | CSE482 | 3 | 🟢 Thấp | Giữ nguyên |
| Kiến trúc máy tính | CSE370 | 3 | 🟢 Thấp | Giữ nguyên |
| Cơ sở dữ liệu | CSE484 | 3 | 🟡 Trung bình | Giữ — thêm Vector DB, NoSQL |
| **Lập trình Windows** | CSE383 | 3 | 🔴 **Cao** | **LOẠI BỎ** — thay bằng Cloud Systems |
| **Phát triển UD với Java** | CSE114 | 3 | 🔴 **Cao** | **Chuyển sang tự chọn** — thay bằng Backend Engineering |
| **Phát triển UD Web cơ bản** | CSE122 | 3 | 🟡 **Trung bình** | **Tái định hướng** — không loại bỏ. Gộp với Web nâng cao → **AI-native web & application development** (6 TC); trọng tâm kiến trúc, bảo mật và tích hợp AI vào sản phẩm |
| Phát triển UD Web nâng cao | CSE124 | 3 | 🟡 Trung bình | Giữ — nâng cấp sang Cloud-Native Architecture |
| Mẫu thiết kế phần mềm | CSE119 | 3 | 🟢 Thấp | Giữ — mở rộng sang Microservices patterns |
| Kiểm thử & ĐBCL PM | CSE462 | 3 | 🟡 Trung bình | Giữ — thêm AI Test Generation, Mutation Testing |
| Công nghệ phần mềm | CSE481 | 3 | 🔴 **Cao** | Cập nhật toàn diện sang AI-Driven SDLC |
| Lập trình đồng thời & PH | CSE115 | 3 | 🟢 Thấp | Giữ nguyên |
| Phát triển UD Di động | CSE112 | 3 | 🟡 Trung bình | Giữ — chuyển sang Flutter/RN + AI-assisted |
| Phát triển dự án PM | CSE412 | 3 | 🟢 Thấp | Giữ — thêm AI Project Management tools |

---

## IV. Các học phần đề xuất loại bỏ — luận giải

### 4.1. Lập trình Windows (CSE383 — 3 TC) → LOẠI BỎ KHỎI BẮT BUỘC

**Luận cứ:**
- Thị trường tuyển dụng WinForms/WPF chiếm **dưới 3%** tổng tin tuyển dụng CNTT Việt Nam (itviec Q1/2026).
- Microsoft đã chính thức đẩy sang .NET MAUI và Blazor — chính hãng đã bỏ WinForms.
- GitHub Copilot tạo hoàn chỉnh giao diện WinForms CRUD trong **dưới 5 phút**.
- **3 tín chỉ** (45 tiết) dạy công nghệ lỗi thời là lãng phí tài nguyên đào tạo.

**Phương án thay thế:** Phân bổ 3 TC này vào học phần **"Cloud Systems & Infrastructure"** (Docker, K8s, AWS cơ bản).

### 4.2. Phát triển ứng dụng với Java (CSE114 — 3 TC) → CHUYỂN TỰ CHỌN

**Luận cứ:**
- Việc ràng buộc sinh viên vào Java cụ thể không còn phù hợp khi thị trường dùng Python, Go, Node.js, Rust cho backend.
- Giá trị cần học là **Backend Architecture** (API design, auth, database optimization), không phải ngôn ngữ Java.
- AI viết Java boilerplate tốt hơn sinh viên năm 3.

**Phương án thay thế:** Học phần **"Backend Engineering & API Design"** — language-agnostic, dạy RESTful, GraphQL, authentication, database optimization.

### 4.3. Phát triển ứng dụng Web cơ bản (CSE122 — 3 TC) → TÁI ĐỊNH HƯỚNG, KHÔNG LOẠI BỎ

**Luận cứ:**
- Web không phải kỹ năng lỗi thời — đây vẫn là nền tảng của ứng dụng di động (PWA, React Native, WebView), ứng dụng doanh nghiệp và là vị trí việc làm phổ biến nhất trên thị trường.
- Vấn đề không phải là "bỏ web" mà là **bỏ cách dạy cũ**: 45 tiết ghi nhớ HTML/CSS/JS thuần là lãng phí — AI agent (v0.dev, Cursor) tạo toàn bộ UI trong vài giây.
- **Giải pháp:** Gộp Web cơ bản + Web nâng cao thành một môn 6 TC theo hướng AI-native: sinh viên dùng AI agent tạo UI, trọng tâm là kiến trúc hệ thống, bảo mật, tích hợp AI vào sản phẩm và deploy lên cloud.

**Phương án thay thế:** Gộp thành **"AI-native web & application development"** (6 TC) — 1 tuần nhập môn kiến trúc web, phần còn lại dạy API gateway, load balancing, bảo mật OWASP, tích hợp LLM vào ứng dụng, deploy CI/CD. Mọi đồ án **bắt buộc tích hợp AI** (chatbot RAG, gợi ý thông minh, hoặc AI-powered feature).

---

## V. Đề xuất chương trình đào tạo mới (phiên bản tham khảo)

> *Tổng tín chỉ được duy trì 140 TC. Đây là đề xuất thảo luận, chưa thay thế quy trình thẩm định chính thức.*

### Khối I: Giáo dục đại cương (37 TC — giữ nguyên)

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 1–6 | Các môn Lý luận chính trị, Pháp luật | 13 | 2–7 |
| 7 | Kỹ năng mềm & Tinh thần khởi nghiệp | 3 | 1 |
| 8–11 | Toán Giải tích, Xác suất TK, Đại số TT | 12 | 1–4 |
| 12 | **Kỹ năng số & Prompt Engineering** | 3 | 1 |
| 13–14 | Tiếng Anh 1, 2 | 6 | 2–3 |

---

### Khối II: Nền tảng khoa học máy tính (24 TC)

| TT | Học phần | TC | HK | Ghi chú thay đổi |
|----|----------|----|----|-----------------|
| 15 | Tư duy máy tính & Nhập môn lập trình | 3 | 1 | Dạy Computational Thinking + Python; **cấm AI 4 tuần đầu** |
| 16 | Cấu trúc dữ liệu & Giải thuật | 3 | 2 | Giữ; thêm bài tập: đánh giá O(n) của code AI sinh ra |
| 17 | Lập trình hướng đối tượng & Design Patterns | 3 | 2 | Gộp CSE116 + CSE119 |
| 18 | Cơ sở dữ liệu hiện đại | 3 | 3 | SQL + NoSQL + Vector DB (Chroma, Pinecone) |
| 19 | Kiến trúc máy tính & Hệ điều hành | 3 | 2 | Giữ nguyên |
| 20 | Mạng máy tính & Bảo mật cơ bản | 3 | 3 | Thêm Cloud Networking |
| 21 | Toán rời rạc | 3 | 2 | Giữ nguyên |
| 22 | Xác suất thống kê ứng dụng | 3 | 3 | Tăng bài tập ứng dụng ML |

---

### Khối III: Lõi kỹ thuật phần mềm (27 TC)

| TT | Học phần | TC | HK | Ghi chú thay đổi |
|----|----------|----|----|-----------------|
| 23 | AI-Driven Software Engineering | 3 | 4 | **Môn mới:** Agile+AI, sinh SRS/UML bằng LLM, CI/CD cơ bản |
| 24 | Kiến trúc phần mềm & Microservices | 3 | 4 | Mở rộng từ Design Patterns lên Cloud Architecture |
| 25 | Kiểm thử PM & Đảm bảo chất lượng | 3 | 4 | Thêm AI Test Gen, Mutation Testing, Security Testing |
| 26 | Lập trình đồng thời & Phân tán | 3 | 5 | Giữ; thêm Distributed Systems patterns |
| 27 | Tương tác người-máy & UX for AI | 3 | 5 | Thêm Human-AI Interaction Design |
| 28 | Kiến trúc & Phát triển Web Hiện đại | 3 | 4 | Gộp Web cơ bản + nâng cao; thiên về Architecture |
| 29 | Phát triển ứng dụng di động | 3 | 5 | Flutter/RN + AI-assisted rapid development |
| 30 | Phân tích yêu cầu phần mềm | 3 | 5 | Thêm LLM-assisted requirements extraction |
| 31 | Quản lý & Phát triển dự án PM | 3 | 6 | Thêm AI Project Management (Jira AI, Linear AI) |

---

### Khối IV: AI engineering & cloud (15 TC — hoàn toàn mới)

| TT | Học phần | TC | HK | Mô tả |
|----|----------|----|----|-------|
| 32 | **LLM Engineering & Ứng dụng** | 3 | 5 | RAG, Vector DB, API LLM, Prompt Engineering nâng cao |
| 33 | **AI Agent Systems** | 3 | 6 | LangChain, LangGraph, AutoGen, Tool Calling, Multi-agent |
| 34 | **Cloud Systems & Infrastructure** | 3 | 5 | Docker, Kubernetes, AWS/GCP, Terraform cơ bản |
| 35 | **DevOps & CI/CD Pipeline** | 3 | 6 | GitHub Actions, Monitoring (Grafana), Deployment strategies |
| 36 | **Phát triển với AI Pair Programmer** | 3 | 4 | Thực hành build Production App với Cursor/Copilot |

---

### Khối V: Tự chọn chuyên sâu (9 TC — chọn 1 track)

| Track | Học phần | TC | HK |
|-------|----------|----|----|
| **A — Enterprise Architecture** | Kiến trúc doanh nghiệp, ERP Integration, SOA | 9 | 6–7 |
| **B — AI Product Engineering** | AI Product Management, Responsible AI, UX for AI | 9 | 6–7 |
| **C — Security Engineering** | Secure Coding, DevSecOps, Pentest cơ bản | 9 | 6–7 |

---

### Khối VI: Thực tập & đồ án (14 TC)

| TT | Học phần | TC | HK | Yêu cầu mới |
|----|----------|----|----|------------|
| 37 | Thực tập doanh nghiệp | 4 | 8 | Nộp báo cáo AI Usage Log |
| 38 | Đồ án tốt nghiệp | 10 | 8 | Bắt buộc: System Architecture Diagram + Proof of AI Integration + Oral Defense |

---

## VI. Đổi mới phương pháp đánh giá

| Phương pháp cũ | Vấn đề | Phương pháp mới đề xuất |
|----------------|--------|------------------------|
| Thi viết code trên giấy | Không thực tế | **Live Debugging:** Debug hệ thống lỗi trong 45 phút có laptop |
| Bài tập lớn nộp cuối kỳ | AI làm toàn bộ | **Oral Defense bắt buộc:** Bảo vệ kiến trúc 15 phút trước GV |
| Chấm code chạy được | AI đều làm được | **Chấm Prompt Log + Reasoning:** Sinh viên nộp lịch sử prompt + giải thích |
| Thi trắc nghiệm lý thuyết | Dễ gian lận | **System Design Interview:** Thiết kế kiến trúc 60 phút, không Internet |

---

## VII. Kết luận và kiến nghị

Kỹ thuật Phần mềm trong kỷ nguyên AI không mất đi bản sắc — nhưng **công cụ đã thay đổi hoàn toàn**. Giống như kỹ sư xây dựng hiện đại không tự đúc gạch nhưng phải thành thạo BIM, kỹ sư phần mềm không cần tự gõ từng dòng HTML nhưng phải thành thạo **System Architecture và AI Orchestration**.

**Kiến nghị cụ thể:**
1. Loại bỏ **Lập trình Windows (CSE383)** khỏi danh sách bắt buộc.
2. Gộp **Web cơ bản + Web nâng cao** thành một môn Architecture.
3. Bổ sung **5 học phần mới** thuộc nhóm AI Engineering & Cloud (15 TC).
4. Bắt buộc **Oral Defense** cho tất cả học phần có đồ án.
5. Thí điểm trong năm học **2026–2027** tại 1–2 lớp trước khi áp dụng đại trà.

---
*Tài liệu tham khảo: IEEE-CS 2023 Computing Curricula; CMU CS Course Catalog 2024; Stanford CS AI Track; VietnamWorks IT Hiring Report Q1/2026; Stack Overflow Developer Survey 2025.*

---

## IX. Bảng phân bổ tín chỉ theo học kỳ — Khung CTĐT mới đề xuất (KTPM)

> *Tổng: 140 TC. Bảng này để kiểm tra tính khả thi về tải học kỳ (không vượt 21 TC/HK).*

| TT | Học phần | TC | HK1 | HK2 | HK3 | HK4 | HK5 | HK6 | HK7 | HK8 |
|:--:|----------|:--:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **I** | **GIÁO DỤC ĐẠI CƯƠNG** | **37** | | | | | | | | |
| 1 | Kỹ năng số & Prompt Engineering (CSE105) | 3 | 3 | | | | | | | |
| 2 | Kỹ năng mềm & Tinh thần khởi nghiệp (SSE111) | 3 | 3 | | | | | | | |
| 3 | Giải tích hàm một biến (MATH111) | 3 | 3 | | | | | | | |
| 4 | Tiếng Anh 1 (ENG213) | 3 | | 3 | | | | | | |
| 5 | Triết học Mác–Lênin (MLP121) | 3 | | 3 | | | | | | |
| 6 | Giải tích hàm nhiều biến (MATH122) | 3 | | 3 | | | | | | |
| 7 | Tiếng Anh 2 (ENG224) | 3 | | | 3 | | | | | |
| 8 | Xác suất thống kê (MATH254) | 3 | | | 3 | | | | | |
| 9 | Đại số tuyến tính (MATH233) | 3 | | | | 3 | | | | |
| 10 | Kinh tế chính trị Mác–Lênin (MLPE222) | 2 | | | | 2 | | | | |
| 11 | Pháp luật đại cương (GEL111) | 2 | | | | | 2 | | | |
| 12 | Chủ nghĩa xã hội khoa học (SCSO232) | 2 | | | | | 2 | | | |
| 13 | Lịch sử Đảng CSVN (HCPV343) | 2 | | | | | | 2 | | |
| 14 | Tư tưởng Hồ Chí Minh (HCMT354) | 2 | | | | | | | 2 | |
| | GDQP (165t*), GDTC (3TC*) | * | | * | * | * | | | | |
| **II** | **GIÁO DỤC CHUYÊN NGHIỆP** | **103** | | | | | | | | |
| **II.1** | **Nền tảng khoa học máy tính** | **24** | | | | | | | | |
| 15 | Tư duy máy tính & Nhập môn lập trình | 3 | 3 | | | | | | | |
| 16 | Cấu trúc dữ liệu & Giải thuật | 3 | | 3 | | | | | | |
| 17 | Lập trình hướng đối tượng & Design Patterns | 3 | | 3 | | | | | | |
| 18 | Kiến trúc máy tính & Hệ điều hành | 3 | | 3 | | | | | | |
| 19 | Mạng máy tính & Bảo mật cơ bản | 3 | | | 3 | | | | | |
| 20 | Cơ sở dữ liệu hiện đại | 3 | | | 3 | | | | | |
| 21 | Toán rời rạc | 3 | | 3 | | | | | | |
| 22 | Xác suất thống kê ứng dụng | 3 | | | 3 | | | | | |
| **II.2** | **Lõi kỹ thuật phần mềm** | **27** | | | | | | | | |
| 23 | WEB-A1: Phát triển web hiện đại với AI agent | 3 | | | 3 | | | | | |
| 24 | WEB-A2: Tích hợp AI vào ứng dụng web & cloud | 3 | | | | 3 | | | | |
| 25 | SE-AI: Công nghệ phần mềm điều hướng bởi AI | 3 | | | | 3 | | | | |
| 26 | Kiến trúc phần mềm & Microservices | 3 | | | | 3 | | | | |
| 27 | Kiểm thử PM & Đảm bảo chất lượng | 3 | | | | | 3 | | | |
| 28 | Lập trình đồng thời & Phân tán | 3 | | | | | 3 | | | |
| 29 | Tương tác người-máy & UX for AI | 3 | | | | | 3 | | | |
| 30 | Phát triển ứng dụng di động | 3 | | | | | | 3 | | |
| 31 | Phân tích yêu cầu phần mềm | 3 | | | | | | 3 | | |
| **II.3** | **AI Engineering & Cloud** | **15** | | | | | | | | |
| 32 | LLM Engineering & Ứng dụng | 3 | | | | | 3 | | | |
| 33 | CLD-1: Hạ tầng đám mây & DevOps | 3 | | | | | 3 | | | |
| 34 | AI Agent Systems | 3 | | | | | | 3 | | |
| 35 | DevOps & CI/CD Pipeline | 3 | | | | | | 3 | | |
| 36 | Phát triển với AI Pair Programmer | 3 | | | | 3 | | | | |
| **II.4** | **Tự chọn chuyên sâu** | **9** | | | | | | | | |
| 37–39 | Tự chọn (1 trong 3 track) | 9 | | | | | | | 9 | |
| **II.5** | **Thực tập & Đồ án** | **14** | | | | | | | | | |
| 40 | Thực tập tốt nghiệp | 4 | | | | | | | | 4 |
| 41 | Đồ án tốt nghiệp | 10 | | | | | | | | 10 |
| | **Tổng cộng** | **140** | **12** | **18** | **18** | **18** | **18** | **17** | **15** | **14** |

> **Kiểm tra tải:** Tối đa 18 TC/HK (HK2–HK5) — nằm trong giới hạn cho phép. HK1 nhẹ hơn để sinh viên năm nhất thích nghi.
