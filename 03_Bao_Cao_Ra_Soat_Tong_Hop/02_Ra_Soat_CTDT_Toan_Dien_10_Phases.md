# Báo cáo rà soát và đánh giá chiến lược chương trình đào tạo CNTT (tầm nhìn 2030)

**Thực hiện bởi:** Hội đồng tư vấn chiến lược giáo dục đại học (chuyên gia ABET/CDIO, cựu Dean CS, CTO Big Tech, chuyên gia AI disruption).  
**Đối tượng đánh giá:** Khung chương trình đào tạo 5 ngành: an ninh mạng (ANM), công nghệ thông tin (CNTT), hệ thống thông tin (HTTT), kỹ thuật phần mềm (KTPM), trí tuệ nhân tạo (TTNT).

---

## 1. Tóm tắt tổng quan

Thế giới công nghệ đang trải qua đợt "đứt gãy" (disruption) lớn nhất kể từ khi Internet ra đời. Sự trỗi dậy của AI agent (Devin, GitHub Copilot Workspace, v0) đã "hàng hóa hóa" (commoditize) hoàn toàn kỹ năng viết mã (coding) cấp thấp và trung bình. Kỹ sư phần mềm "thợ gõ code" (junior coder) đang mất đi giá trị thị trường.

Trong bối cảnh đó, chương trình đào tạo hiện tại của nhà trường, mặc dù có cấu trúc học thuật vững chắc và bước đầu đưa AI vào (CSE105), nhưng vẫn mang nặng **"tư duy kỷ nguyên 2010"**: dạy sinh viên tự viết từng dòng mã, tự xây dựng từng component cơ bản.

**Tuyên ngôn chiến lược:** Chúng ta phải chuyển dịch ngay lập tức mục tiêu đào tạo từ **"code generators"** (người tạo mã) sang **"AI orchestrators & system architects"** (người điều phối AI và kiến trúc sư hệ thống). Nếu không tái cấu trúc, sinh viên ra trường trong 3-4 năm tới sẽ đối mặt với nguy cơ đào thải ngay từ vạch xuất phát. Báo cáo này phác thảo lộ trình tái thiết kế toàn diện (deep redesign) cho giai đoạn 2026-2030.

---

## 2. Chẩn đoán hiện trạng

### A. Chất lượng học thuật

*   **Điểm mạnh:** Khối kiến thức cốt lõi (Toán rời rạc, CTDL&GT, kiến trúc máy tính, hệ điều hành) được thiết kế bài bản, đúng chuẩn ACM/IEEE. Cấu trúc tiên quyết (prerequisite structure) khá chặt chẽ.
*   **Điểm yếu:** Thiếu sự liên kết giữa lý thuyết và các bài toán phân tán (distributed) hiện đại. Tỷ trọng thời gian dành cho việc "gõ mã cú pháp" quá lớn so với "thiết kế hệ thống".

### B. Mức độ phù hợp thị trường

*   **Hiện tại (2024-2025):** Vẫn đáp ứng được các doanh nghiệp outsource truyền thống.
*   **Tương lai (2026-2030):** Bắt đầu chệch nhịp nghiêm trọng. Thị trường tương lai yêu cầu MLOps, LLM systems, cloud-native architecture, và data engineering. Các kỹ năng CRUD (Create, Read, Update, Delete) cho Web/App đã bị AI tự động hóa 90%.

### C. Khoảng trống năng lực

1.  **AI engineering (cho ngành non-AI):** KTPM, HTTT thiếu kỹ năng tích hợp API LLM, xây dựng RAG, vector database.
2.  **Cloud & DevOps/MLOps:** Gần như vắng bóng hoặc quá mỏng. Sinh viên không biết triển khai hệ thống lên cloud tự động.
3.  **Cộng tác người-AI:** Kỹ năng làm việc nhóm với AI agent (pair-programming với AI).
4.  **Tư duy sản phẩm & khởi nghiệp:** Tư duy làm sản phẩm thay vì chỉ nhận spec và code.

---

## 3. Phân tích từng ngành

### 3.1. Kỹ thuật phần mềm (KTPM)

*   **Tình trạng:** Nguy cơ cao nhất.
*   **Phân tích:** Ngành KTPM hiện tại đang dạy sinh viên làm những việc mà Devin/Copilot làm tốt nhất: viết code ứng dụng, tạo form, CRUD. Các môn như *Phát triển ứng dụng với Java, Lập trình Windows* đã lỗi thời về cả mặt công nghệ lẫn tư duy tiếp cận.
*   **Định hướng:** Chuyển từ "software coding" sang "software architecture & AI integration". Tập trung mạnh vào: microservices, system design, kiểm thử tự động bằng AI, và quản trị dự án có AI hỗ trợ.

### 3.2. Công nghệ thông tin (CNTT)

*   **Tình trạng:** Nguy cơ cao.
*   **Phân tích:** Mang tính hàn lâm rộng nhưng thiếu mũi nhọn. Sinh viên dễ bị kẹt ở mức "biết mỗi thứ một ít" nhưng không đủ sâu để làm system engineer, cũng không đủ giỏi AI để làm AI engineer.
*   **Định hướng:** Biến ngành này thành ngành **"cloud & distributed systems"**. Đẩy mạnh cloud computing, IoT architecture, và AI deployment.

### 3.3. Hệ thống thông tin (HTTT)

*   **Tình trạng:** Nguy cơ trung bình.
*   **Phân tích:** HTTT có lợi thế vì gắn với business logic (nghiệp vụ). AI khó thay thế người hiểu nghiệp vụ. Tuy nhiên, các công cụ business intelligence truyền thống đang bị AI thay thế bởi "chat with data".
*   **Định hướng:** Dịch chuyển sang **data engineering & AI-driven business intelligence**. Tập trung vào data warehouse, phân tích chuỗi thời gian, và tự động hóa quy trình nghiệp vụ bằng AI agent.

### 3.4. Trí tuệ nhân tạo và khoa học dữ liệu (TTNT)

*   **Tình trạng:** Nguy cơ thấp, nhưng cần nâng cấp.
*   **Phân tích:** Đã có các môn rất tốt như AI tạo sinh, tác tử thông minh. Tuy nhiên, dường như đang dạy "AI research" nhiều hơn "AI engineering".
*   **Định hướng:** Cần bổ sung MLOps, LLMOps, tối ưu hóa mô hình lớn (quantization, fine-tuning), và system design cho machine learning (thiết kế hệ thống ML lớn).

### 3.5. An ninh mạng (ANM)

*   **Tình trạng:** Nguy cơ trung bình.
*   **Phân tích:** AI có thể tự động dò quét lỗ hổng và viết mã độc. Nếu dạy ANM theo cách thủ công, sinh viên sẽ không đọ lại AI.
*   **Định hướng:** Tập trung vào **AI security** (bảo vệ các hệ thống LLM khỏi prompt injection, data poisoning), và sử dụng **AI trong phòng thủ** (automated threat hunting, log analysis bằng LLM).

---

## 4. Rà soát từng môn học

| Môn học | Vai trò hiện tại | Rủi ro AI | Đề xuất & hành động | Phiên bản mới |
| :--- | :--- | :---: | :--- | :--- |
| **Nhập môn lập trình** | Dạy cú pháp, logic cơ bản | Trung bình | **Giữ nguyên nhưng thay đổi cách dạy.** Cấm AI ở 4 tuần đầu để luyện tư duy logic. Sau đó cho phép dùng IDE AI. | Cấu trúc dữ liệu & tư duy máy tính (computational thinking). |
| **Phát triển UD Web cơ bản** | Dạy HTML/CSS/JS, PHP/Node | Cao | **Tái định hướng — không loại bỏ.** Web vẫn là nền tảng của mobile và là vị trí việc làm phổ biến nhất thị trường. Thay đổi **cách dạy**: dùng AI agent tạo UI; tập trung kiến trúc hệ thống và tích hợp AI vào sản phẩm. | Gộp Web cơ bản + Web nâng cao thành: **AI-native web & application development** (6 TC). |
| **Lập trình Windows** | Dạy WinForm/WPF | Cao | **Loại bỏ hoàn toàn.** Công nghệ lỗi thời, không có giá trị kiến trúc cao. | Thay thế bằng: **Cloud computing & DevOps cơ bản**. |
| **Phát triển UD với Java** | Dạy OOP Java ứng dụng | Cao | **Chuyển thành tự chọn hoặc gộp.** | Thay thế bằng: **Microservices & distributed application development**. |
| **Cấu trúc dữ liệu & giải thuật** | Nền tảng CS | Thấp | **Giữ nguyên.** Đây là cốt lõi để sinh viên có thể đánh giá code do AI sinh ra có tối ưu O(n) hay không. | Dạy cách prompt AI sinh ra nhiều thuật toán và yêu cầu sinh viên đánh giá hiệu năng (reviewing). |
| **Công nghệ phần mềm** | Quy trình phát triển phần mềm | Cao | **Cập nhật toàn diện.** Các phương pháp Agile cũ cần được nâng cấp với AI tools. | **AI-driven software engineering** (dùng AI sinh SRS, sinh test case, quản lý CI/CD). |
| **CSDL / Hệ quản trị CSDL** | Dạy SQL, thiết kế ERD | Trung bình | **Cập nhật.** Dạy cách dùng LLM để sinh SQL từ text (Text-to-SQL), tối ưu query tự động. | **Modern database systems & data engineering**. |
| **Mạng máy tính / HĐH** | Nền tảng hệ thống | Thấp | **Giữ nguyên, tăng độ khó.** Đây là nơi AI còn yếu. Cần dạy sinh viên hiểu sâu tầng thấp của hệ thống. | Tích hợp system design, Linux kernel, cloud infrastructure. |
| **AI tạo sinh & LLMs** | Chuyên ngành TTNT | Thấp | **Mở rộng.** Bắt buộc cho toàn bộ sinh viên khối ngành CNTT/KTPM, không chỉ riêng AI. | **Applied generative AI & LLM engineering**. |

---

## 5. Các rủi ro tương lai

1.  **Sự tuyệt chủng của junior developer:** Trong 3 năm tới, Big Tech và cả các công ty outsource sẽ không tuyển "thực tập sinh viết code". Họ tuyển "junior AI operator" — người có khả năng vận hành agent để sinh ra mã tương đương mid-senior dev.
2.  **Khoảng cách cơ sở hạ tầng:** Đào tạo AI/Cloud cần GPU và cloud credits. Nếu trường chỉ dùng phòng máy tính PC cục bộ, sinh viên sẽ không có trải nghiệm thực tế.
3.  **Khủng hoảng đạo đức học thuật:** Không thể cấm sinh viên dùng AI. Nếu tiếp tục dùng các bài tập truyền thống, 100% sinh viên sẽ qua môn với điểm A bằng cách dùng ChatGPT, dẫn đến lạm phát điểm và mất uy tín bằng cấp.

---

## 6. Thiết kế CTĐT mới cho 2030

Dưới đây là khung kiến trúc mới áp dụng chung cho khối ngành KTPM/CNTT (ngành AI có thể chuyên sâu hơn ở năm 3-4):

*   **Năm 1: Tư duy nền tảng và AI literacy**
    *   Toán học cho khoa học máy tính (đại số, xác suất).
    *   Tư duy máy tính & nhập môn thuật toán (C/C++ / Python) — *thực hành code tay, không AI*.
    *   Kỹ năng số & prompt engineering chuyên sâu.
    *   Kiến trúc máy tính & hệ điều hành.
*   **Năm 2: Kỹ thuật với hỗ trợ AI (bắt đầu dùng AI IDE)**
    *   Cấu trúc dữ liệu & giải thuật nâng cao (bài tập trọng tâm: code review thuật toán AI viết).
    *   Thiết kế CSDL & data engineering.
    *   Mạng máy tính & bảo mật nền tảng.
    *   **Applied AI engineering:** dạy cách dùng API của OpenAI/Anthropic, xây dựng RAG cơ bản.
*   **Năm 3: Cloud, hệ thống phân tán & điều phối**
    *   Kiến trúc phần mềm (software architecture & microservices).
    *   Cloud computing & MLOps/DevOps.
    *   **Phát triển hệ thống AI agent (bắt buộc chung).**
    *   *Các môn chuyên ngành sâu (security, data, games, IoT...)*
*   **Năm 4: Đồ án thực tế & tư duy sản phẩm**
    *   Tư duy sản phẩm (product thinking) & khởi nghiệp.
    *   Đồ án tốt nghiệp: **bắt buộc phải là một hệ thống/ứng dụng có sử dụng/tích hợp AI** để giải quyết bài toán doanh nghiệp. Chấm điểm dựa trên system architecture và prompt/agent logs.

---

## 7. Kế hoạch chuyển đổi

### 7.1. Chuyển đổi mô hình giảng dạy

*   **Từ bỏ "code-along":** Giảng viên không chiếu slide rồi code mẫu từng dòng trên bảng.
*   **Áp dụng "studio learning" & "project-based":** Lớp học biến thành "phòng họp kỹ thuật". Giảng viên giao bài toán, sinh viên dùng AI sinh ra code, sau đó toàn lớp cùng tranh luận (review) về kiến trúc, bảo mật và hiệu năng của đoạn code đó.

### 7.2. Tái thiết kế kiểm tra đánh giá

Nhằm vô hiệu hóa việc "gian lận" bằng AI và biến AI thành công cụ hợp pháp:

1.  **Chính sách sử dụng AI:** Cho phép dùng AI (Copilot, Cursor) trong 80% các bài thi thực hành.
2.  **Nhật ký prompt & AI auditing:** Khi nộp bài, sinh viên phải nộp kèm file log ghi lại toàn bộ lịch sử trò chuyện/prompt với AI. Chấm điểm kỹ năng ra lệnh cho máy.
3.  **Vấn đáp / bảo vệ kiến trúc:** Đây là **công cụ cốt lõi**. Giảng viên không chấm điểm đoạn code chạy được (vì AI làm được). Giảng viên mở source code, chỉ vào 1 hàm phức tạp và hỏi: *"Tại sao em thiết kế như thế này? Nếu 1 triệu user truy cập đồng thời, hàm này sẽ sập ở đâu?"*. Người chỉ chép code của AI sẽ rớt ngay lập tức.
4.  **Debug trực tiếp:** Bài thi giữa kỳ là đưa cho sinh viên một project có sẵn (do AI sinh ra có cài cắm bug), yêu cầu sinh viên tìm và vá lỗi bảo mật/hiệu năng trong 60 phút.

---

## 8. Tài chính & giảng viên

### Nâng cấp giảng viên

*   **Thực tế cần thẳng thắn:** Nhiều giảng viên dạy lập trình lâu năm đang sở hữu bộ kỹ năng cũ kỹ hơn cả sinh viên (do sinh viên cập nhật AI quá nhanh).
*   **Lộ trình:** Yêu cầu toàn bộ giảng viên dạy môn cơ sở/chuyên ngành phải trải qua khóa đào tạo "AI-assisted teaching" (sử dụng Cursor, GitHub Copilot) và có chứng chỉ cloud cơ bản (AWS/GCP/Azure).

### Ngân sách

*   Chuyển một phần ngân sách từ việc mua sắm máy tính/phòng lab truyền thống sang:
    1.  Cấp tài khoản **GitHub Copilot Education** (miễn phí) cho 100% sinh viên/giảng viên.
    2.  Mua **cloud credits** (AWS Educate, Azure for Students) để sinh viên thực hành DevOps/Cloud.
    3.  Ngân sách sử dụng **API LLM** (OpenAI, Anthropic) phục vụ các môn học thực hành AI.

---

## 9. Lộ trình thực thi chiến lược

| Giai đoạn | Mục tiêu | Hành động cụ thể |
| :--- | :--- | :--- |
| **Năm 1 (2025)** | **Thiết lập điểm khởi đầu** | Áp dụng quy chế thi vấn đáp ở các môn đồ án. Thay thế 1-2 môn lỗi thời (ví dụ: Lập trình Windows) bằng môn Cloud/AI cơ bản. Cấp Copilot cho giảng viên. |
| **Năm 2 (2026)** | **Chuyển đổi phương pháp** | Áp dụng "live debugging" và nộp nhật ký prompt. Ngành KTPM và CNTT chính thức học "hệ thống tác tử / LLM" như môn bắt buộc. |
| **Năm 3 (2028)** | **Chuyển đổi toàn diện** | Giảm tỷ trọng và tái định hướng mục tiêu các môn dạy cú pháp: năm 1 giữ nguyên phương pháp để rèn tư duy thuật toán; năm 2–3 chuyển sang AI-assisted (sinh viên dùng AI, trọng tâm là review và kiến trúc); năm 4 hoàn toàn AI-native. CTĐT chuyển mạnh sang system architecture & AI engineering. Giảng viên trở thành mentor/reviewer. |

---

## 10. Kết luận chiến lược

Đại học không thể chạy đua với các nền tảng tự học online (Coursera, Bootcamps) trong việc đào tạo "thợ gõ mã". Sứ mệnh của trường đại học công nghệ trong kỷ nguyên AI là tạo ra những **nhà lãnh đạo kỹ thuật (technical leaders)**, những người hiểu sâu sắc các nguyên lý nền tảng của khoa học máy tính (toán, cấu trúc dữ liệu, kiến trúc hệ thống) để có thể "quản lý" và "phát hiện lỗi" của lực lượng lập trình viên AI.

Chương trình đào tạo hiện tại cần một cuộc **"đại phẫu thuật"** (không chỉ là sửa đổi nhỏ giọt). Cắt bỏ những kỹ năng AI có thể làm trong 10 giây (CRUD, UI syntax), đầu tư mạnh mẽ vào system design, cloud, security và agentic AI workflow. Đây không chỉ là sự nâng cấp, đây là vấn đề **sinh tồn** của chất lượng đào tạo và giá trị văn bằng khối ngành CNTT trong thập kỷ tới.
