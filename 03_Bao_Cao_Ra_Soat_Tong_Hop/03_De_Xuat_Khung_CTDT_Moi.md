# BÁO CÁO ĐỀ XUẤT CHI TIẾT KHUNG CHƯƠNG TRÌNH VÀ HỌC PHẦN CHO TỪNG NGÀNH (TẦM NHÌN 2026-2030)

**Tài liệu:** Đề xuất Cấu trúc CTĐT & Danh mục học phần mới
**Mục tiêu:** Cung cấp "Bản thiết kế thi công" (Blueprint) cho việc nâng cấp toàn diện 5 ngành CNTT để đáp ứng xu hướng AI Agent và Sự dịch chuyển của thị trường lao động công nghệ.

---

## 1. TRIẾT LÝ THIẾT KẾ CHUNG (DESIGN PHILOSOPHY)

Để thuyết phục Hội đồng Khoa học và Ban giám hiệu, toàn bộ đề xuất dưới đây dựa trên 3 luận điểm cốt lõi (Core Arguments):
1.  **Sự sụp đổ của kỹ năng lập trình thô (The Fall of Raw Coding):** AI hiện tại (Cursor, Devin) đã giải bài toán viết code từ logic thông thường. Giữ các học phần tập trung dạy cú pháp (syntax) ngôn ngữ lập trình cụ thể (Java, C#, Web HTML/CSS) là làm lãng phí 3 năm thanh xuân của sinh viên và tiền bạc của nhà trường.
2.  **Sự lên ngôi của Kiến trúc và Tích hợp (The Rise of Architecture & Integration):** Sinh viên CNTT tương lai phải được đào tạo như những "Kiến trúc sư" và "Tổng thầu": Biết chia nhỏ bài toán phức tạp, giao cho AI agent làm từng phần nhỏ, sau đó ghép nối (integrate), kiểm thử (test) và triển khai (deploy) chúng lên nền tảng Đám mây.
3.  **Tách biệt Cơ sở nền tảng và Ứng dụng:** Toán học, Giải thuật, Cấu trúc dữ liệu, Nguyên lý Hệ điều hành phải được giữ nguyên và dạy sâu hơn (vì đây là nền tảng máy học không thể tự học). Nhưng các môn ứng dụng (như Lập trình Windows) phải được xóa sổ để thay bằng các môn Vận hành/Tích hợp (DevOps/MLOps).

---

## 2. NGÀNH KỸ THUẬT PHẦN MỀM (KTPM - SOFTWARE ENGINEERING)

### Luận điểm chiến lược
Ngành KTPM chịu sự đe dọa trực tiếp nhất từ GenAI. Tư duy đào tạo phải chuyển từ **"Software Developer"** (Người viết ứng dụng) sang **"AI-Assisted Software Architect"** (Kiến trúc sư phần mềm dùng AI). Nếu sinh viên KTPM ra trường chỉ biết viết CRUD API bằng Nodejs hay Java, họ sẽ bị đào thải.

### Đề xuất Khung Học phần Mới

| Phân loại | Tên môn học cũ (Cần loại bỏ/Gộp) | Học phần Đề xuất thay thế / Bổ sung | Luận cứ thuyết phục (Tại sao phải học?) |
| :--- | :--- | :--- | :--- |
| **Bỏ/Gộp** | - Lập trình Windows (3 TC)<br>- Phát triển UD Java (3 TC)<br>- Phát triển UD Web cơ bản (3 TC) | **Gộp thành:** Lập trình Ứng dụng & API cơ bản (3 TC). | Dùng AI để sinh mã, chỉ cần 1 môn duy nhất để SV hiểu cách các component giao tiếp (Frontend gọi Backend qua API). |
| **Nâng cấp** | - Công nghệ phần mềm (3 TC)<br>- Phân tích yêu cầu PM (3 TC) | **AI-Driven Software Engineering** (CNPM điều hướng bởi AI) | Dạy SV dùng AI để tự động hóa: sinh tài liệu SRS, tạo UML diagrams, phân tích requirement, tự động hóa Test case. |
| **Môn Mới** | *(Chưa có)* | **Cloud-Native & Microservices Architecture** (Kiến trúc Vi dịch vụ và Đám mây) | Code do AI sinh ra thường là nguyên khối (Monolith). Kỹ sư KTPM cần biết chia tách hệ thống thành các Microservices để chịu tải cao trên AWS/GCP. |
| **Môn Mới** | *(Chưa có)* | **Xây dựng hệ thống phần mềm tích hợp AI (LLM Integration & RAG)** | Đây là kỹ năng hot nhất hiện nay. Kỹ sư phần mềm phải biết cách gọi API của OpenAI, xây dựng Vector Database, Retrieval-Augmented Generation (RAG) để nhúng AI vào sản phẩm. |

---

## 3. NGÀNH HỆ THỐNG THÔNG TIN (HTTT - INFORMATION SYSTEMS)

### Luận điểm chiến lược
Ngành HTTT đóng vai trò cầu nối giữa Kinh doanh (Business) và Công nghệ. Trong kỷ nguyên mới, "Data" (Dữ liệu) là nhiên liệu cho AI. HTTT phải chuyển dịch từ **"Quản lý cơ sở dữ liệu truyền thống"** sang **"Kỹ thuật Dữ liệu (Data Engineering) & Tự động hóa nghiệp vụ (Business Automation)"**.

### Đề xuất Khung Học phần Mới

| Phân loại | Tên môn học cũ (Cần loại bỏ/Gộp) | Học phần Đề xuất thay thế / Bổ sung | Luận cứ thuyết phục (Tại sao phải học?) |
| :--- | :--- | :--- | :--- |
| **Loại bỏ** | - Phát triển UD Web nâng cao (3 TC)<br>- Lập trình Windows (3 TC) | Không học lập trình ứng dụng sâu ở ngành này. | Kỹ sư HTTT cần hiểu hệ thống dữ liệu, không cần tranh việc viết web/app với ngành KTPM. |
| **Nâng cấp** | - CSDL / Hệ quản trị CSDL<br>- Kho dữ liệu | **Data Engineering & Cloud Data Warehouse** (Kỹ thuật Dữ liệu Đám mây) | Dữ liệu hiện đại nằm trên Cloud (Snowflake, BigQuery). SV cần biết xây dựng pipeline dữ liệu (ETL/ELT) tự động để cấp dữ liệu sạch cho các mô hình AI. |
| **Môn Mới** | *(Chưa có)* | **Tự động hóa Quy trình Nghiệp vụ với AI Agent** (Business Automation w/ AI Agents) | Các hệ thống ERP, CRM (SAP, Salesforce) hiện đều vận hành qua AI Agent. SV cần biết thiết lập workflow tự động thay vì nhập liệu thủ công. |
| **Môn Mới** | - Hệ thống kinh doanh thông minh (Cũ) | **Applied AI for Business Intelligence** (AI ứng dụng trong BI) | Thay vì vẽ dashboard tĩnh (PowerBI), dạy SV làm hệ thống "Chat with Data" (Dùng ngôn ngữ tự nhiên để hỏi báo cáo doanh thu). |

---

## 4. NGÀNH CÔNG NGHỆ THÔNG TIN (CNTT - INFORMATION TECHNOLOGY)

### Luận điểm chiến lược
CNTT thường bị coi là ngành "trung dung", biết mỗi thứ một ít. Để tạo thế mạnh cạnh tranh không thể thay thế, CNTT cần định vị lại thành mũi nhọn về **"Hạ tầng Hệ thống & Vận hành" (Cloud Infrastructure & System Operations)**. Khi các lập trình viên dùng AI viết ra hàng triệu dòng code, hệ thống cần kỹ sư CNTT để vận hành và duy trì cho chúng chạy trơn tru, bảo mật và mở rộng được.

### Đề xuất Khung Học phần Mới

| Phân loại | Tên môn học cũ (Cần loại bỏ/Gộp) | Học phần Đề xuất thay thế / Bổ sung | Luận cứ thuyết phục (Tại sao phải học?) |
| :--- | :--- | :--- | :--- |
| **Bỏ/Gộp** | - Các môn lập trình ứng dụng lẻ tẻ. | Loại bỏ bớt số tín chỉ lập trình ứng dụng cụ thể. | Dành dư địa (tín chỉ) để học sâu về kiến trúc máy tính, hệ thống phân tán. |
| **Môn Mới** | *(Học phần Hệ điều hành/Mạng máy tính nâng cao)* | **Distributed Systems** (Hệ thống phân tán) | Cốt lõi của các hệ thống Big Tech (Google, Facebook). AI không thể cấu trúc một hệ thống phân tán tối ưu nếu không có tư duy của System Engineer. |
| **Môn Mới** | *(Chưa có)* | **Cloud Infrastructure & DevOps** (Hạ tầng Đám mây & Vận hành PT) | Thay vì cài cắm server vật lý, kỹ sư CNTT phải viết mã hạ tầng (Infrastructure as Code - Terraform, Docker, Kubernetes) để tự động hóa triển khai. |
| **Môn Mới** | *(Chưa có)* | **MLOps (Machine Learning Operations)** | Đưa các mô hình AI (do ngành TTNT làm ra) vào môi trường thực tế (production) là một bài toán cực khó. Đây là khoảng trống khổng lồ của thị trường. |

---

## 5. NGÀNH TRÍ TUỆ NHÂN TẠO VÀ KHOA HỌC DỮ LIỆU (TTNT - AI & DATA SCIENCE)

### Luận điểm chiến lược
Ngành TTNT thường rơi vào bẫy "Học thuật": Dạy sinh viên rất nhiều công thức toán và tự huấn luyện (train) mô hình nhỏ. Thực tế doanh nghiệp 90% không tự train mô hình (vì chi phí hàng triệu USD), mà họ làm **"Applied AI" (Sản phẩm hóa AI)** bằng cách dùng LLM có sẵn (OpenAI, Gemini, Llama) kết hợp dữ liệu nội bộ.

### Đề xuất Khung Học phần Mới

| Phân loại | Tên môn học cũ (Cần loại bỏ/Gộp) | Học phần Đề xuất thay thế / Bổ sung | Luận cứ thuyết phục (Tại sao phải học?) |
| :--- | :--- | :--- | :--- |
| **Nâng cấp** | - Học máy (Machine Learning)<br>- Học sâu (Deep Learning) | Vẫn giữ nhưng giảm tính hàn lâm (toán), tăng tính ứng dụng (dùng PyTorch/TensorFlow giải quyết bài toán thực). | Nền tảng quan trọng, nhưng không bắt SV code lại thuật toán từ đầu (từ con số 0) mà dạy cách dùng framework. |
| **Môn Mới** | *(Chưa có trọng tâm)* | **LLMOps & Fine-tuning Foundation Models** | Doanh nghiệp khát nhân sự biết Fine-tune các mô hình mã nguồn mở (như Llama 3, Mistral) để chạy độc lập (offline) cho bảo mật dữ liệu. |
| **Nâng cấp** | - Hệ thống tác tử thông minh | **Phát triển AI Agent & Multi-Agent Systems** (Hệ thống đa tác tử) | Tương lai của AI là các Agent tự giao tiếp với nhau (vd: CrewAI, AutoGen). Phải dạy SV cách lập trình cho các bot AI làm việc nhóm với nhau. |
| **Môn Mới** | *(Chưa có)* | **AI Product Management & Ethics** (Phát triển SP AI & Đạo đức) | Không chỉ làm thuật toán, kỹ sư TTNT cần tư duy sản phẩm: Đánh giá độ lệch (bias), ảo giác (hallucination), và tính sinh lời của sản phẩm AI. |

---

## 6. NGÀNH AN NINH MẠNG (ANM - CYBERSECURITY)

### Luận điểm chiến lược
Hacker hiện đã dùng AI để sinh mã độc đa hình (polymorphic malware) và tìm lỗ hổng zero-day trong vài phút. An ninh mạng thủ công đã chết. Ngành ANM phải tiến hóa thành **"AI-Powered Security"** (Dùng AI làm khiên) và **"Securing AI"** (Bảo vệ chính các hệ thống AI).

### Đề xuất Khung Học phần Mới

| Phân loại | Tên môn học cũ (Cần loại bỏ/Gộp) | Học phần Đề xuất thay thế / Bổ sung | Luận cứ thuyết phục (Tại sao phải học?) |
| :--- | :--- | :--- | :--- |
| **Nâng cấp** | - Đánh giá an ninh mạng<br>- Phân tích mã độc | **Automated Penetration Testing & Threat Hunting** (Pentest Tự động) | Sinh viên không dò lỗi bằng tay nữa, mà viết kịch bản (script) cho AI Agent tự động rà quét và khai thác toàn bộ hệ thống. |
| **Môn Mới** | *(Chưa có)* | **Applied AI in Cybersecurity** (AI ứng dụng trong ANM) | Sử dụng Học máy và LLM để phân tích hàng triệu dòng Log truy cập (SIEM), phát hiện bất thường (Anomaly Detection) theo thời gian thực. |
| **Môn Mới** | *(Hoàn toàn Mới)* | **Bảo mật Hệ thống Trí tuệ Nhân tạo (AI Security / LLM Security)** | Lỗ hổng mới nhất hiện nay là Prompt Injection (lừa AI tiết lộ dữ liệu nhạy cảm) và Data Poisoning (đầu độc dữ liệu huấn luyện). Sinh viên ra trường có kỹ năng này sẽ có lương cực cao. |

---

## KẾT LUẬN & ĐỀ XUẤT THỰC THI

Để hiện thực hóa Khung chương trình này, cần một lộ trình **"Sandboxing"** (Thử nghiệm cục bộ):
1.  **Chấp nhận phá vỡ sự kháng cự:** Việc xóa bỏ các môn dạy cú pháp truyền thống (Java, Windows Form) sẽ gặp phản kháng từ giảng viên thâm niên. Hội đồng khoa học cần ra quyết định cấp khoa về việc "Ngưng dạy ngôn ngữ, bắt đầu dạy kiến trúc".
2.  **Khối kiến thức chung cực kỳ quan trọng:** Thống nhất đưa 2 môn: **Cloud Computing Foundation** và **Applied AI/Prompt Engineering** thành môn bắt buộc cho 100% sinh viên cả 5 ngành ngay trong Năm thứ 2.
3.  **Hạ tầng thực hành:** Cần liên kết với các đối tác (AWS Academy, Google Cloud Edu, GitHub Education) để sinh viên có tài khoản Cloud thật và công cụ AI (Copilot) thật để thực hành các môn mới. Máy tính cấu hình cao tại trường không còn là yếu tố quyết định bằng tài nguyên Đám mây.
