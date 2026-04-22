# BÁO CÁO RÀ SOÁT VÀ ĐÁNH GIÁ CHIẾN LƯỢC CHƯƠNG TRÌNH ĐÀO TẠO CNTT (TẦM NHÌN 2030)

**Thực hiện bởi:** Hội đồng Tư vấn Chiến lược Giáo dục Đại học (Chuyên gia ABET/CDIO, Cựu Dean CS, CTO Big Tech, Chuyên gia AI Disruption).
**Đối tượng đánh giá:** Khung chương trình đào tạo 5 ngành: An ninh mạng (ANM), Công nghệ thông tin (CNTT), Hệ thống thông tin (HTTT), Kỹ thuật phần mềm (KTPM), Trí tuệ nhân tạo (TTNT).

---

## 1. EXECUTIVE SUMMARY (TÓM TẮT TỔNG QUAN)

Thế giới công nghệ đang trải qua đợt "đứt gãy" (disruption) lớn nhất kể từ khi Internet ra đời. Sự trỗi dậy của AI Agent (Devin, GitHub Copilot Workspace, v0) đã "hàng hóa hóa" (commoditize) hoàn toàn kỹ năng viết mã (coding) cấp thấp và trung bình. Kỹ sư phần mềm "thợ gõ code" (Junior Coder) đang mất đi giá trị thị trường. 

Trong bối cảnh đó, chương trình đào tạo hiện tại của nhà trường, mặc dù có cấu trúc học thuật vững chắc và bước đầu đưa AI vào (CSE105), nhưng vẫn mang nặng **"tư duy kỷ nguyên 2010"**: Dạy sinh viên tự viết từng dòng mã, tự xây dựng từng component cơ bản.

**Tuyên ngôn chiến lược:** Chúng ta phải chuyển dịch ngay lập tức mục tiêu đào tạo từ **"Code Generators"** (Người tạo mã) sang **"AI Orchestrators & System Architects"** (Người điều phối AI và Kiến trúc sư hệ thống). Nếu không tái cấu trúc, sinh viên ra trường trong 3-4 năm tới sẽ đối mặt với nguy cơ đào thải ngay từ vạch xuất phát. Báo cáo này phác thảo lộ trình tái thiết kế toàn diện (Deep Redesign) cho giai đoạn 2026-2030.

---

## 2. CURRENT CURRICULUM DIAGNOSIS (CHẨN ĐOÁN HIỆN TRẠNG)

### A. Academic Quality (Chất lượng học thuật)
*   **Điểm mạnh:** Khối kiến thức cốt lõi (Toán rời rạc, CTDL&GT, Kiến trúc máy tính, Hệ điều hành) được thiết kế bài bản, đúng chuẩn ACM/IEEE. Prerequisite structure (Cấu trúc tiên quyết) khá chặt chẽ.
*   **Điểm yếu:** Thiếu sự liên kết giữa lý thuyết và các bài toán phân tán (distributed) hiện đại. Tỷ trọng thời gian dành cho việc "gõ mã cú pháp" quá lớn so với "thiết kế hệ thống".

### B. Industry Relevance (Mức độ phù hợp thị trường)
*   **Hiện tại (2024-2025):** Vẫn đáp ứng được các doanh nghiệp outsource truyền thống.
*   **Tương lai (2026-2030):** Bắt đầu chệch nhịp nghiêm trọng. Thị trường tương lai yêu cầu MLOps, LLM Systems, Cloud-Native Architecture, và Data Engineering. Các kỹ năng CRUD (Create, Read, Update, Delete) cho Web/App đã bị AI tự động hóa 90%.

### C. Missing Competencies (Khoảng trống năng lực)
1.  **AI Engineering (cho ngành non-AI):** KTPM, HTTT thiếu kỹ năng tích hợp API LLM, xây dựng RAG, vector database.
2.  **Cloud & DevOps/MLOps:** Gần như vắng bóng hoặc quá mỏng. Sinh viên không biết triển khai hệ thống lên Cloud tự động.
3.  **Human-AI Collaboration:** Kỹ năng làm việc nhóm với AI Agent (Pair-programming với AI).
4.  **Product Thinking & Entrepreneurship:** Tư duy làm sản phẩm thay vì chỉ nhận spec và code.

---

## 3. PER-PROGRAM ANALYSIS (PHÂN TÍCH TỪNG NGÀNH)

### 3.1. Kỹ thuật phần mềm (KTPM)
*   **Tình trạng:** NGUY CƠ CAO NHẤT (Highest Risk).
*   **Phân tích:** Ngành KTPM hiện tại đang dạy sinh viên làm những việc mà Devin/Copilot làm tốt nhất: Viết code ứng dụng, tạo form, CRUD. Các môn như *Phát triển ứng dụng với Java, Lập trình Windows* đã lỗi thời về cả mặt công nghệ lẫn tư duy tiếp cận.
*   **Định hướng:** Chuyển từ "Software Coding" sang "Software Architecture & AI Integration". Tập trung mạnh vào: Microservices, System Design, Kiểm thử tự động bằng AI, và Quản trị dự án có AI hỗ trợ.

### 3.2. Công nghệ thông tin (CNTT)
*   **Tình trạng:** NGUY CƠ CAO (High Risk).
*   **Phân tích:** Mang tính hàn lâm rộng nhưng thiếu mũi nhọn. Sinh viên dễ bị kẹt ở mức "biết mỗi thứ một ít" nhưng không đủ sâu để làm System Engineer, cũng không đủ giỏi AI để làm AI Engineer.
*   **Định hướng:** Biến ngành này thành ngành **"Cloud & Distributed Systems"**. Đẩy mạnh Cloud Computing, IoT Architecture, và AI Deployment.

### 3.3. Hệ thống thông tin (HTTT)
*   **Tình trạng:** NGUY CƠ TRUNG BÌNH (Medium Risk).
*   **Phân tích:** HTTT có lợi thế vì gắn với Business Logic (Nghiệp vụ). AI khó thay thế người hiểu nghiệp vụ. Tuy nhiên, các công cụ Business Intelligence truyền thống đang bị AI thay thế bởi "Chat with Data".
*   **Định hướng:** Dịch chuyển sang **Data Engineering & AI-driven Business Intelligence**. Tập trung vào Data Warehouse, Phân tích chuỗi thời gian, và tự động hóa quy trình nghiệp vụ bằng AI Agent.

### 3.4. Trí tuệ nhân tạo và Khoa học dữ liệu (TTNT)
*   **Tình trạng:** NGUY CƠ THẤP (Low Risk), nhưng CẦN NÂNG CẤP.
*   **Phân tích:** Đã có các môn rất tốt như AI Tạo sinh, Tác tử thông minh. Tuy nhiên, dường như đang dạy "AI Research" nhiều hơn "AI Engineering". 
*   **Định hướng:** Cần bổ sung MLOps, LLMOps, Tối ưu hóa mô hình lớn (Quantization, Fine-tuning), và System Design cho Machine Learning (Thiết kế hệ thống ML lớn).

### 3.5. An ninh mạng (ANM)
*   **Tình trạng:** NGUY CƠ TRUNG BÌNH (Medium Risk).
*   **Phân tích:** AI có thể tự động dò quét lỗ hổng và viết mã độc. Nếu dạy ANM theo cách thủ công, sinh viên sẽ không đọ lại AI.
*   **Định hướng:** Tập trung vào **AI Security** (Bảo vệ các hệ thống LLM khỏi Prompt Injection, Data Poisoning), và sử dụng **AI trong phòng thủ** (Automated Threat Hunting, Log Analysis bằng LLM).

---

## 4. COURSE-BY-COURSE AUDIT (RÀ SOÁT TỪNG MÔN HỌC)

| Môn học | Vai trò hiện tại | Trạng thái AI Risk | Đề xuất & Hành động | Phiên bản Mới (New Version) |
| :--- | :--- | :---: | :--- | :--- |
| **Nhập môn lập trình** | Dạy cú pháp, logic cơ bản | **Medium** | **Giữ nguyên nhưng thay đổi cách dạy.** Cấm AI ở 4 tuần đầu để luyện tư duy logic. Sau đó cho phép dùng IDE AI. | Cấu trúc dữ liệu & Tư duy máy tính (Computational Thinking). |
| **Phát triển UD Web cơ bản** | Dạy HTML/CSS/JS, PHP/Node | **High** | **Gộp & Giảm tín chỉ / Loại bỏ.** AI tạo frontend trong vài giây. Môn này không còn xứng đáng 3 tín chỉ cốt lõi. | Gộp vào Web Nâng cao thành môn: **Cloud-Native Web Architecture**. |
| **Lập trình Windows** | Dạy WinForm/WPF | **High** | **Loại bỏ hoàn toàn.** Công nghệ lỗi thời, không có giá trị kiến trúc cao. | Thay thế bằng: **Cloud Computing & DevOps cơ bản**. |
| **Phát triển UD với Java** | Dạy OOP Java ứng dụng | **High** | **Chuyển thành tự chọn hoặc Gộp.** | Thay thế bằng: **Microservices & Distributed Application Development**. |
| **Cấu trúc Dữ liệu & Giải thuật** | Nền tảng CS | **Low** | **Giữ nguyên.** Đây là cốt lõi để sinh viên có thể đánh giá code do AI sinh ra có tối ưu O(n) hay không. | Dạy cách Prompt AI sinh ra nhiều thuật toán và yêu cầu SV đánh giá hiệu năng (Reviewing). |
| **Công nghệ phần mềm** | Quy trình phát triển PM | **High** | **Cập nhật toàn diện.** Các phương pháp Agile cũ cần được nâng cấp với AI tools. | **AI-Driven Software Engineering** (Dùng AI sinh SRS, sinh Test case, quản lý CI/CD). |
| **CSDL / Hệ quản trị CSDL** | Dạy SQL, thiết kế ERD | **Medium** | **Cập nhật.** Dạy cách dùng LLM để sinh SQL từ Text (Text-to-SQL), Tối ưu query tự động. | **Modern Database Systems & Data Engineering**. |
| **Mạng máy tính / HĐH** | Nền tảng hệ thống | **Low** | **Giữ nguyên, tăng độ khó.** Đây là nơi AI còn yếu. Cần dạy sinh viên hiểu sâu tầng thấp của hệ thống. | Tích hợp System Design, Linux Kernel, Cloud Infrastructure. |
| **AI Tạo sinh & LLMs** | Chuyên ngành TTNT | **Low** | **Mở rộng.** Bắt buộc cho toàn bộ sinh viên khối ngành CNTT/KTPM, không chỉ riêng AI. | **Applied Generative AI & LLM Engineering**. |

---

## 5. FUTURE RISKS (CÁC RỦI RO TƯƠNG LAI)

1.  **Sự tuyệt chủng của Junior Developer:** Trong 3 năm tới, Big Tech và cả các cty outsource sẽ không tuyển "thực tập sinh viết code". Họ tuyển "Junior AI Operator" – người có khả năng vận hành agent để sinh ra mã tương đương Mid-Senior dev.
2.  **Khoảng cách cơ sở hạ tầng (Infrastructure Gap):** Đào tạo AI/Cloud cần GPU và Cloud credits. Nếu trường chỉ dùng phòng máy tính PC cục bộ, sinh viên sẽ không có trải nghiệm thực tế.
3.  **Khủng hoảng đạo đức học thuật:** Không thể cấm sinh viên dùng AI. Nếu tiếp tục dùng các bài tập truyền thống, 100% sinh viên sẽ qua môn với điểm A bằng cách dùng ChatGPT, dẫn đến lạm phát điểm và mất uy tín bằng cấp.

---

## 6. PROPOSED NEW CURRICULUM (THIẾT KẾ CTĐT MỚI CHO 2030)

Dưới đây là khung kiến trúc mới áp dụng chung cho khối ngành KTPM/CNTT (ngành AI có thể chuyên sâu hơn ở Năm 3-4):

*   **YEAR 1: TƯ DUY NỀN TẢNG VÀ AI LITERACY**
    *   Toán học cho Khoa học máy tính (Đại số, Xác suất).
    *   Tư duy máy tính & Nhập môn thuật toán (C/C++ / Python) - *Thực hành code tay, không AI*.
    *   Kỹ năng số & Prompt Engineering chuyên sâu.
    *   Kiến trúc máy tính & Hệ điều hành.
*   **YEAR 2: AI-ASSISTED ENGINEERING (BẮT ĐẦU DÙNG AI IDE)**
    *   Cấu trúc dữ liệu & Giải thuật nâng cao (Bài tập trọng tâm: Code Review thuật toán AI viết).
    *   Thiết kế CSDL & Data Engineering.
    *   Mạng máy tính & Bảo mật nền tảng.
    *   **Applied AI Engineering:** Dạy cách dùng API của OpenAI/Anthropic, xây dựng RAG cơ bản.
*   **YEAR 3: CLOUD, DISTRIBUTED SYSTEMS & ORCHESTRATION**
    *   Kiến trúc phần mềm (Software Architecture & Microservices).
    *   Cloud Computing & MLOps/DevOps.
    *   **Phát triển hệ thống AI Agent (Bắt buộc chung).**
    *   *Các môn chuyên ngành sâu (Security, Data, Games, IoT...)*
*   **YEAR 4: INDUSTRY CAPSTONE & PRODUCT**
    *   Tư duy Sản phẩm (Product Thinking) & Khởi nghiệp.
    *   Đồ án tốt nghiệp: **Bắt buộc phải là một hệ thống/ứng dụng có sử dụng/tích hợp AI** để giải quyết bài toán doanh nghiệp. Chấm điểm dựa trên System Architecture và Prompt/Agent Logs.

---

## 7. TRANSITION PLAN & TEACHING/ASSESSMENT REDESIGN (KẾ HOẠCH CHUYỂN ĐỔI)

### 7.1. Chuyển đổi Mô hình giảng dạy (Teaching Model)
*   **Từ bỏ "Code-along":** GV không chiếu slide rồi code mẫu từng dòng trên bảng. 
*   **Áp dụng "Studio Learning" & "Project-based":** Lớp học biến thành "Phòng họp kỹ thuật". Giảng viên giao bài toán, sinh viên dùng AI sinh ra code, sau đó toàn lớp cùng tranh luận (review) về kiến trúc, bảo mật và hiệu năng của đoạn code đó.

### 7.2. Tái thiết kế Kiểm tra Đánh giá (Assessment Redesign)
Nhằm vô hiệu hóa việc "gian lận" bằng AI và biến AI thành công cụ hợp pháp:
1.  **Chính sách sử dụng AI (AI Usage Policy):** Cho phép dùng AI (Copilot, Cursor) trong 80% các bài thi thực hành. 
2.  **Prompt Logs & AI Auditing:** Khi nộp bài (Assignment), sinh viên phải nộp kèm file log ghi lại toàn bộ lịch sử trò chuyện/prompt với AI. Chấm điểm kỹ năng ra lệnh cho máy.
3.  **Oral Defense (Thi Vấn đáp / Bảo vệ kiến trúc):** Đây là **công cụ cốt lõi**. Giảng viên không chấm điểm đoạn code chạy được (vì AI làm được). Giảng viên mở source code, chỉ vào 1 hàm phức tạp và hỏi: *"Tại sao em thiết kế như thế này? Nếu 1 triệu user truy cập đồng thời, hàm này sẽ sập ở đâu?"*. Người chỉ chép code của AI sẽ rớt ngay lập tức.
4.  **Live Debugging:** Bài thi giữa kỳ là đưa cho sinh viên một project có sẵn (do AI sinh ra có cài cắm bug), yêu cầu sinh viên tìm và vá lỗi bảo mật/hiệu năng trong 60 phút.

---

## 8. BUDGET & FACULTY IMPLICATIONS (TÀI CHÍNH & GIẢNG VIÊN)

### Nâng cấp Giảng viên (Faculty Transformation)
*   **Sự thật mất lòng:** Nhiều giảng viên dạy lập trình lâu năm đang sở hữu bộ kỹ năng cũ kỹ hơn cả sinh viên (do sinh viên cập nhật AI quá nhanh).
*   **Roadmap:** Yêu cầu toàn bộ giảng viên dạy môn cơ sở/chuyên ngành phải trải qua khóa đào tạo "AI-Assisted Teaching" (Sử dụng Cursor, GitHub Copilot) và có chứng chỉ Cloud cơ bản (AWS/GCP/Azure).

### Ngân sách (Budget)
*   Chuyển một phần ngân sách từ việc mua sắm máy tính/phòng lab truyền thống sang:
    1.  Cấp tài khoản **GitHub Copilot Education** (Miễn phí) cho 100% sinh viên/GV.
    2.  Mua **Cloud Credits** (AWS Educate, Azure for Students) để sinh viên thực hành DevOps/Cloud.
    3.  Ngân sách sử dụng **API LLM** (OpenAI, Anthropic) phục vụ các môn học thực hành AI.

---

## 9. STRATEGIC IMPLEMENTATION ROADMAP (LỘ TRÌNH THỰC THI CHIẾN LƯỢC)

| Giai đoạn | Mục tiêu | Hành động cụ thể (Quick Wins & Long-term) |
| :--- | :--- | :--- |
| **Năm 1 (2025)** | **Thiết lập Base-line** | Áp dụng quy chế thi Vấn đáp (Oral Defense) ở các môn Đồ án. Thay thế 1-2 môn lỗi thời (VD: Lập trình Windows) bằng môn Cloud/AI cơ bản. Cấp Copilot cho GV. |
| **Năm 2 (2026)** | **Chuyển đổi Phương pháp**| Áp dụng "Live Debugging" và nộp "Prompt Log". Ngành KTPM và CNTT chính thức học "Hệ thống Tác tử / LLM" như môn bắt buộc. |
| **Năm 3 (2028)** | **Full Transformation** | Xóa bỏ hoàn toàn các môn dạy cú pháp truyền thống. CTĐT 100% chuyển sang định hướng System Architecture & AI Engineering. Giảng viên trở thành Mentor/Reviewer. |

---

## 10. KẾT LUẬN CHIẾN LƯỢC (STRATEGIC CONCLUSION)

Đại học không thể chạy đua với các nền tảng tự học online (Coursera, Bootcamps) trong việc đào tạo "thợ gõ mã". Sứ mệnh của trường đại học công nghệ trong kỷ nguyên AI là tạo ra những **Nhà lãnh đạo Kỹ thuật (Technical Leaders)**, những người hiểu sâu sắc các nguyên lý nền tảng của Khoa học máy tính (Toán, Cấu trúc dữ liệu, Kiến trúc hệ thống) để có thể "quản lý" và "phát hiện lỗi" của lực lượng Lập trình viên AI.

Chương trình đào tạo hiện tại cần một cuộc **"đại phẫu thuật"** (không chỉ là sửa đổi nhỏ giọt). Cắt bỏ những kỹ năng AI có thể làm trong 10 giây (CRUD, UI syntax), đầu tư mạnh mẽ vào System Design, Cloud, Security và Agentic AI Workflow. Đây không chỉ là sự nâng cấp, đây là vấn đề **sinh tồn** của chất lượng đào tạo và giá trị văn bằng khối ngành CNTT trong thập kỷ tới.
