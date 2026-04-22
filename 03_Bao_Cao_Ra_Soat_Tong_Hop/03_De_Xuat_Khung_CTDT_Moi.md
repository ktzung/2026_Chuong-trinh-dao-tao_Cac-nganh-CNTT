# Báo cáo đề xuất chi tiết khung chương trình và học phần cho từng ngành (tầm nhìn 2026-2030)

**Tài liệu:** Đề xuất cấu trúc CTĐT & danh mục học phần mới  
**Mục tiêu:** Cung cấp "bản thiết kế thi công" (blueprint) cho việc nâng cấp toàn diện 5 ngành CNTT để đáp ứng xu hướng AI agent và sự dịch chuyển của thị trường lao động công nghệ.

---

## 1. Triết lý thiết kế chung

Để thuyết phục Hội đồng Khoa học và Ban giám hiệu, toàn bộ đề xuất dưới đây dựa trên 3 luận điểm cốt lõi:

1.  **Sự sụp đổ của kỹ năng lập trình thô:** AI hiện tại (Cursor, Devin) đã giải bài toán viết code từ logic thông thường. Giữ các học phần tập trung dạy cú pháp ngôn ngữ lập trình cụ thể (Java, C#, Web HTML/CSS) là làm lãng phí 3 năm thanh xuân của sinh viên và tiền bạc của nhà trường.
2.  **Sự lên ngôi của kiến trúc và tích hợp:** Sinh viên CNTT tương lai phải được đào tạo như những "kiến trúc sư" và "tổng thầu": biết chia nhỏ bài toán phức tạp, giao cho AI agent làm từng phần nhỏ, sau đó ghép nối (integrate), kiểm thử (test) và triển khai (deploy) chúng lên nền tảng đám mây.
3.  **Tách biệt cơ sở nền tảng và ứng dụng:** Toán học, giải thuật, cấu trúc dữ liệu, nguyên lý hệ điều hành phải được giữ nguyên và dạy sâu hơn (vì đây là nền tảng máy học không thể tự học). Nhưng các môn ứng dụng (như Lập trình Windows) phải được xóa sổ để thay bằng các môn vận hành/tích hợp (DevOps/MLOps).

---

## 2. Ngành kỹ thuật phần mềm (KTPM)

### Luận điểm chiến lược

Ngành KTPM chịu sự đe dọa trực tiếp nhất từ GenAI. Tư duy đào tạo phải chuyển từ **"software developer"** (người viết ứng dụng) sang **"AI-assisted software architect"** (kiến trúc sư phần mềm dùng AI). Nếu sinh viên KTPM ra trường chỉ biết viết CRUD API bằng Nodejs hay Java, họ sẽ bị đào thải.

### Đề xuất khung học phần mới

| Phân loại | Tên môn học cũ (cần loại bỏ/gộp) | Học phần đề xuất thay thế / bổ sung | Luận cứ thuyết phục (tại sao phải học?) |
| :--- | :--- | :--- | :--- |
| **Gộp & tái định hướng** | - Lập trình Windows (3 TC)<br>- Phát triển UD Java (3 TC)<br>- Phát triển UD Web cơ bản (3 TC) + Web nâng cao (3 TC) | **Gộp thành:** AI-native web & application development (6 TC). | Web vẫn là nền tảng của mobile và vị trí việc làm phổ biến nhất. Không loại bỏ mà **tái định hướng**: dùng AI agent (Cursor, v0.dev) tạo UI; trọng tâm là kiến trúc hệ thống, tích hợp AI vào sản phẩm và deploy lên cloud. Lập trình Windows loại bỏ (lỗi thời); Java chuyển tự chọn. |
| **Nâng cấp** | - Công nghệ phần mềm (3 TC)<br>- Phân tích yêu cầu phần mềm (3 TC) | **AI-driven software engineering** (công nghệ phần mềm điều hướng bởi AI) | Dạy sinh viên dùng AI để tự động hóa: sinh tài liệu SRS, tạo UML diagram, phân tích requirement, tự động hóa test case. |
| **Môn mới** | *(Chưa có)* | **Cloud-native & microservices architecture** (kiến trúc vi dịch vụ và đám mây) | Code do AI sinh ra thường là nguyên khối (monolith). Kỹ sư KTPM cần biết chia tách hệ thống thành các microservices để chịu tải cao trên AWS/GCP. |
| **Môn mới** | *(Chưa có)* | **Xây dựng hệ thống phần mềm tích hợp AI (LLM integration & RAG)** | Đây là kỹ năng hot nhất hiện nay. Kỹ sư phần mềm phải biết cách gọi API của OpenAI, xây dựng vector database, retrieval-augmented generation (RAG) để nhúng AI vào sản phẩm. |

---

## 3. Ngành hệ thống thông tin (HTTT)

### Luận điểm chiến lược

Ngành HTTT đóng vai trò cầu nối giữa kinh doanh (business) và công nghệ. Trong kỷ nguyên mới, "data" (dữ liệu) là nhiên liệu cho AI. HTTT phải chuyển dịch từ **"quản lý cơ sở dữ liệu truyền thống"** sang **"kỹ thuật dữ liệu (data engineering) & tự động hóa nghiệp vụ (business automation)"**.

### Đề xuất khung học phần mới

| Phân loại | Tên môn học cũ (cần loại bỏ/gộp) | Học phần đề xuất thay thế / bổ sung | Luận cứ thuyết phục (tại sao phải học?) |
| :--- | :--- | :--- | :--- |
| **Tái định hướng** | - Phát triển UD Web nâng cao (3 TC)<br>*(Web cơ bản: gộp vào Web nâng cao)* | **AI-native web & data application** (6 TC gộp) | HTTT không cần đào tạo frontend chuyên sâu như KTPM, nhưng web vẫn là phương tiện trình bày dữ liệu chủ yếu. Tái định hướng: dùng AI agent tạo giao diện data dashboard, tích hợp "chat with data", kết nối API nghiệp vụ. Trọng tâm là data visualization và AI-powered BI, không phải cú pháp HTML. |
| **Loại bỏ** | - Lập trình Windows (3 TC) | Không học lập trình ứng dụng desktop ở ngành này. | Kỹ sư HTTT cần hiểu hệ thống dữ liệu, không cần tranh việc viết web/app với ngành KTPM. |
| **Nâng cấp** | - CSDL / Hệ quản trị CSDL<br>- Kho dữ liệu | **Data engineering & cloud data warehouse** (kỹ thuật dữ liệu đám mây) | Dữ liệu hiện đại nằm trên cloud (Snowflake, BigQuery). Sinh viên cần biết xây dựng pipeline dữ liệu (ETL/ELT) tự động để cấp dữ liệu sạch cho các mô hình AI. |
| **Môn mới** | *(Chưa có)* | **Tự động hóa quy trình nghiệp vụ với AI agent** (business automation w/ AI agents) | Các hệ thống ERP, CRM (SAP, Salesforce) hiện đều vận hành qua AI agent. Sinh viên cần biết thiết lập workflow tự động thay vì nhập liệu thủ công. |
| **Môn mới** | - Hệ thống kinh doanh thông minh (cũ) | **Applied AI for business intelligence** (AI ứng dụng trong BI) | Thay vì vẽ dashboard tĩnh (PowerBI), dạy sinh viên làm hệ thống "chat with data" (dùng ngôn ngữ tự nhiên để hỏi báo cáo doanh thu). |

---

## 4. Ngành công nghệ thông tin (CNTT)

### Luận điểm chiến lược

CNTT thường bị coi là ngành "trung dung", biết mỗi thứ một ít. Để tạo thế mạnh cạnh tranh không thể thay thế, CNTT cần định vị lại thành mũi nhọn về **"hạ tầng hệ thống & vận hành" (cloud infrastructure & system operations)**. Khi các lập trình viên dùng AI viết ra hàng triệu dòng code, hệ thống cần kỹ sư CNTT để vận hành và duy trì cho chúng chạy trơn tru, bảo mật và mở rộng được.

### Đề xuất khung học phần mới

| Phân loại | Tên môn học cũ (cần loại bỏ/gộp) | Học phần đề xuất thay thế / bổ sung | Luận cứ thuyết phục (tại sao phải học?) |
| :--- | :--- | :--- | :--- |
| **Tái định hướng** | - Các môn lập trình ứng dụng web đơn lẻ | Gộp thành **AI-native web & systems application** (6 TC). | Web là giao diện của mọi hệ thống cloud. Kỹ sư CNTT cần biết xây dựng web app vận hành trên cloud, không phải gõ HTML. Dùng AI agent tạo UI, trọng tâm là system integration, API gateway, bảo mật và monitoring. |
| **Môn mới** | *(Học phần hệ điều hành/mạng máy tính nâng cao)* | **Distributed systems** (hệ thống phân tán) | Cốt lõi của các hệ thống Big Tech (Google, Facebook). AI không thể cấu trúc một hệ thống phân tán tối ưu nếu không có tư duy của system engineer. |
| **Môn mới** | *(Chưa có)* | **Cloud infrastructure & DevOps** (hạ tầng đám mây & vận hành phát triển) | Thay vì cài cắm server vật lý, kỹ sư CNTT phải viết mã hạ tầng (infrastructure as code — Terraform, Docker, Kubernetes) để tự động hóa triển khai. |
| **Môn mới** | *(Chưa có)* | **MLOps (machine learning operations)** | Đưa các mô hình AI (do ngành TTNT làm ra) vào môi trường thực tế (production) là một bài toán cực khó. Đây là khoảng trống khổng lồ của thị trường. |

---

## 5. Ngành trí tuệ nhân tạo và khoa học dữ liệu (TTNT)

### Luận điểm chiến lược

Ngành TTNT thường rơi vào bẫy "học thuật": dạy sinh viên rất nhiều công thức toán và tự huấn luyện (train) mô hình nhỏ. Thực tế doanh nghiệp 90% không tự train mô hình (vì chi phí hàng triệu USD), mà họ làm **"applied AI" (sản phẩm hóa AI)** bằng cách dùng LLM có sẵn (OpenAI, Gemini, Llama) kết hợp dữ liệu nội bộ.

### Đề xuất khung học phần mới

| Phân loại | Tên môn học cũ (cần loại bỏ/gộp) | Học phần đề xuất thay thế / bổ sung | Luận cứ thuyết phục (tại sao phải học?) |
| :--- | :--- | :--- | :--- |
| **Tái định hướng** | - Học máy (machine learning)<br>- Học sâu (deep learning) | Vẫn giữ nhưng giảm tính hàn lâm (toán), tăng tính ứng dụng (dùng PyTorch/TensorFlow giải quyết bài toán thực). | Nền tảng quan trọng, nhưng không bắt sinh viên code lại thuật toán từ đầu mà dạy cách dùng framework. |
| **Tái định hướng Web** | - Phát triển UD Web cơ bản (CSE122) | **Web app triển khai mô hình AI** (Gradio, Streamlit, FastAPI + React) | Sinh viên TTNT cần biết đưa model AI ra web để demo và production. Không dạy HTML/CSS thuần mà dạy cách build AI-powered web interface bằng AI agent tools và framework chuyên dụng. |
| **Môn mới** | *(Chưa có trọng tâm)* | **LLMOps & fine-tuning foundation models** | Doanh nghiệp khát nhân sự biết fine-tune các mô hình mã nguồn mở (như Llama 3, Mistral) để chạy độc lập (offline) cho bảo mật dữ liệu. |
| **Nâng cấp** | - Hệ thống tác tử thông minh | **Phát triển AI agent & multi-agent systems** (hệ thống đa tác tử) | Tương lai của AI là các agent tự giao tiếp với nhau (ví dụ: CrewAI, AutoGen). Phải dạy sinh viên cách lập trình cho các bot AI làm việc nhóm với nhau. |
| **Môn mới** | *(Chưa có)* | **AI product management & ethics** (phát triển sản phẩm AI & đạo đức) | Không chỉ làm thuật toán, kỹ sư TTNT cần tư duy sản phẩm: đánh giá độ lệch (bias), ảo giác (hallucination), và tính sinh lời của sản phẩm AI. |

---

## 6. Ngành an ninh mạng (ANM)

### Luận điểm chiến lược

Hacker hiện đã dùng AI để sinh mã độc đa hình (polymorphic malware) và tìm lỗ hổng zero-day trong vài phút. An ninh mạng thủ công đã chết. Ngành ANM phải tiến hóa thành **"AI-powered security"** (dùng AI làm khiên) và **"securing AI"** (bảo vệ chính các hệ thống AI).

### Đề xuất khung học phần mới

| Phân loại | Tên môn học cũ (cần loại bỏ/gộp) | Học phần đề xuất thay thế / bổ sung | Luận cứ thuyết phục (tại sao phải học?) |
| :--- | :--- | :--- | :--- |
| **Tái định hướng** | - Đánh giá an ninh mạng<br>- Phân tích mã độc | **Automated penetration testing & threat hunting** (pentest tự động) | Sinh viên không dò lỗi bằng tay nữa, mà viết kịch bản (script) cho AI agent tự động rà quét và khai thác toàn bộ hệ thống. |
| **Tái định hướng Web** | - Phát triển UD Web cơ bản (CSE122) | **Bảo mật ứng dụng Web & OWASP** (web app security) | Web vẫn là mặt trận tấn công chủ yếu. Sinh viên ANM không cần *xây* web mà cần *tấn công và phòng thủ* web. Thay dạy HTML/CSS bằng dạy Burp Suite, OWASP Top 10, XSS, CSRF, SQL Injection trên nền tảng web thực tế. |
| **Môn mới** | *(Chưa có)* | **Applied AI in cybersecurity** (AI ứng dụng trong ANM) | Sử dụng học máy và LLM để phân tích hàng triệu dòng log truy cập (SIEM), phát hiện bất thường (anomaly detection) theo thời gian thực. |
| **Môn mới** | *(Hoàn toàn mới)* | **Bảo mật hệ thống trí tuệ nhân tạo (AI security / LLM security)** | Lỗ hổng mới nhất hiện nay là prompt injection (lừa AI tiết lộ dữ liệu nhạy cảm) và data poisoning (đầu độc dữ liệu huấn luyện). Sinh viên ra trường có kỹ năng này sẽ có lương cực cao. |

---

## Kết luận & đề xuất thực thi

Để hiện thực hóa khung chương trình này, cần một lộ trình **"sandboxing"** (thử nghiệm cục bộ):

1.  **Chấp nhận phá vỡ sự kháng cự:** Việc xóa bỏ các môn dạy cú pháp truyền thống (Java, Windows Form) sẽ gặp phản kháng từ giảng viên thâm niên. Hội đồng khoa học cần ra quyết định cấp khoa về việc "ngưng dạy ngôn ngữ, bắt đầu dạy kiến trúc".
2.  **Khối kiến thức chung cực kỳ quan trọng:** Thống nhất đưa 2 môn: **Cloud computing foundation** và **Applied AI/Prompt engineering** thành môn bắt buộc cho 100% sinh viên cả 5 ngành ngay trong năm thứ 2.
3.  **Hạ tầng thực hành:** Cần liên kết với các đối tác (AWS Academy, Google Cloud Edu, GitHub Education) để sinh viên có tài khoản cloud thật và công cụ AI (Copilot) thật để thực hành các môn mới. Máy tính cấu hình cao tại trường không còn là yếu tố quyết định bằng tài nguyên đám mây.
