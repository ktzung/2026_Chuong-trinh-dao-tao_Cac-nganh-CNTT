# BÁO CÁO ĐÁNH GIÁ VÀ ĐỀ XUẤT NÂNG CẤP CHƯƠNG TRÌNH ĐÀO TẠO CNTT TRONG KỶ NGUYÊN AI

**Kính gửi:** Ban phát triển Chương trình đào tạo 
**Chủ đề:** Đánh giá khung CTĐT đại học khối ngành CNTT (2025-2026) và giải pháp tích hợp năng lực AI Agent, chuyển đổi phương pháp giảng dạy.

---

## 1. ĐÁNH GIÁ HIỆN TRẠNG CHƯƠNG TRÌNH ĐÀO TẠO
Qua phân tích 5 khung chương trình (ANM, CNTT, HTTT, KTPM, TTNT), dưới góc độ của một chuyên gia công nghệ và đào tạo trong kỷ nguyên AI, tôi có các nhận định sau:

### Điểm sáng:
*   Đã đưa học phần **"Kỹ năng số và Khai thác AI" (CSE105)** vào ngay Học kỳ 1. Đây là bước đi rất tiên phong và đúng đắn.
*   Cấu trúc ngành linh hoạt, các môn học bắt kịp xu hướng cơ bản (Điện toán đám mây, Phân tích dữ liệu...).
*   Ngành TTNT đã có các môn cốt lõi về **AI tạo sinh và Mô hình ngôn ngữ lớn (CSE134)**, **Hệ thống tác tử thông minh (CSE107)**.

### Vấn đề tồn tại cốt lõi (Pain points):
*   **Tư duy đào tạo vẫn là "Tạo ra thợ viết code" (Coder) thay vì "Kỹ sư kiến trúc" (System Architect):** Khung CTĐT vẫn phân bổ thời lượng lớn cho việc học cú pháp, ngôn ngữ lập trình cụ thể. Với sức mạnh của GenAI (Cursor, GitHub Copilot, Devin), AI đã làm xuất sắc việc này. Nếu vẫn dạy sinh viên tự viết từng dòng HTML/CSS hay API, sinh viên sẽ thấy nhàm chán, đối phó và lạm dụng AI.
*   **Thiếu kỹ năng "AI Agentic" cho khối ngành ngoài AI:** Các ngành CNTT, KTPM, HTTT, ANM coi "AI tạo sinh" và "Hệ thống tác tử" là môn *tự chọn*. Trong khi đó, thị trường hiện tại yêu cầu kỹ sư phần mềm hay an ninh mạng **bắt buộc** phải biết dùng AI Agent để tự động hóa quy trình.
*   **Rủi ro từ phương pháp đánh giá:** Nếu cách kiểm tra vẫn là "Viết chương trình giải bài toán X", sinh viên sẽ copy paste từ ChatGPT. Bằng cấp sẽ không còn phản ánh đúng năng lực.

---

## 2. ĐỀ XUẤT CHIẾN LƯỢC TỔNG THỂ (PARADIGM SHIFT)

Để giải quyết bài toán sinh viên lạm dụng AI và đáp ứng tiêu chí tuyển dụng của doanh nghiệp (ưu tiên ứng viên có kỹ năng AI Agent), tôi đề xuất 4 chiến lược tổng thể:

### 2.1. Chuyển dịch chuẩn đầu ra: Từ "Code Generation" sang "Code Review & Orchestration"
*   Sinh viên không cần phải thuộc cú pháp. Kỹ năng quan trọng nhất hiện nay là: **Prompt Engineering (viết yêu cầu rõ ràng), System Design (thiết kế kiến trúc hệ thống), Code Review (đọc hiểu và kiểm duyệt mã AI sinh ra), và Security Auditing (kiểm tra lỗ hổng do AI tạo ra)**.

### 2.2. Bình thường hóa và bắt buộc sử dụng IDE có AI
*   Thay vì "cấm" sinh viên dùng AI, hãy **bắt buộc** sinh viên sử dụng các công cụ như Cursor, GitHub Copilot Workspace, v.v. từ Học kỳ 3 trở đi. 
*   **Yêu cầu nộp "Prompt Log":** Trong các đồ án, sinh viên nộp mã nguồn kèm theo nhật ký các Prompt đã dùng để tương tác với AI. Điểm số đánh giá dựa trên tư duy chia nhỏ vấn đề (decomposition) để ra lệnh cho AI, chứ không chỉ đánh giá sản phẩm cuối.

### 2.3. Cải tiến phương pháp Đánh giá (Assessment)
*   Chuyển đổi bài thi từ "Viết ứng dụng X" thành: 
    *   **"Debugging & Refactoring":** Giảng viên cung cấp một đoạn code / hệ thống chạy sai hoặc chưa tối ưu (do AI tạo ra), yêu cầu SV tìm lỗi, giải thích và sửa.
    *   **Phỏng vấn / Vấn đáp (Oral Exam):** Hỏi trực tiếp sinh viên về kiến trúc, lý do chọn thuật toán này mà không phải thuật toán khác để chống việc sinh viên nhờ AI làm toàn bộ mà không hiểu cốt lõi.

### 2.4. Phổ cập "AI Agent" cho mọi chuyên ngành
*   Đưa khái niệm tích hợp AI (API integration, RAG, Agents) vào làm tiêu chuẩn bắt buộc cho các đồ án môn học của tất cả các chuyên ngành, không chỉ riêng ngành TTNT.

---

## 3. ĐỀ XUẤT CẢI TIẾN CHI TIẾT TỪNG NHÓM MÔN HỌC

Dựa trên danh sách các học phần hiện có, dưới đây là cách tái cấu trúc nội dung và phương pháp dạy học để "AI-proof" (chống lại sự đào thải của AI) cho chương trình:

### 3.1. Nhóm môn Lập trình cơ sở (Nhập môn LT, LT Nâng cao, CTDL & Giải thuật)
*   **Nhập môn Lập trình (HK1):** Dạy thuần túy tư duy logic (Computational Thinking), hiểu cách máy tính hoạt động. Có thể cấm AI ở giai đoạn này để rèn luyện tư duy nền tảng.
*   **Lập trình nâng cao & CTDL (HK3):** Cho phép dùng AI. Bài tập tập trung vào việc: "Yêu cầu AI sinh ra 3 giải thuật khác nhau, sinh viên phân tích độ phức tạp thời gian/không gian (Big O) của từng giải thuật và chọn giải thuật tối ưu nhất". Tập trung dạy kỹ năng viết Test Case tự động.

### 3.2. Nhóm môn Phát triển ứng dụng (Web, Mobile, Java, Windows)
*(Phát triển ứng dụng Web cơ bản/nâng cao, PTUD Di động, Java...)*
*   **Cách dạy mới:** Không dạy cách tạo form HTML hay viết CRUD API bằng tay (AI tạo trong 10 giây). Giảng viên đóng vai trò là "Project Manager", sinh viên là "Tech Lead" sử dụng "Lập trình viên AI". 
*   **Trọng tâm:** Dạy cách phân chia module, kết nối API, phân quyền (Authentication), bảo mật web (OWASP), triển khai CI/CD và tối ưu hóa hiệu năng cơ sở dữ liệu.
*   **Bài tập:** Sinh viên dùng AI Agent (ví dụ: v0.dev, Cursor) để gen ra toàn bộ UI/UX. Thời gian trên lớp dùng để tích hợp logic nghiệp vụ phức tạp và review code.

### 3.3. Nhóm môn Kỹ thuật phần mềm & Phân tích hệ thống
*(CNPM, Phân tích thiết kế hệ thống, Quản lý dự án CNTT...)*
*   **Cách dạy mới:** Cập nhật phương pháp "AI-Driven Development". 
*   **Trọng tâm:** Dùng LLM để tự động hóa việc trích xuất yêu cầu từ khách hàng (Requirement Elicitation), sinh UML Diagram tự động, viết tài liệu đặc tả (SRS) bằng AI. Đưa công cụ AI vào quy trình Agile/Scrum để quản lý task.
*   **Kiểm thử phần mềm:** Dạy sinh viên cách dùng AI để tự động sinh ra hàng ngàn unit test case và mutation testing.

### 3.4. Nhóm môn Trí tuệ nhân tạo & Dữ liệu
*(Dành cho tất cả các ngành)*
*   **Đề xuất:** Nâng cấp học phần **"AI tạo sinh và Mô hình ngôn ngữ lớn (CSE134)"** hoặc **"Hệ thống tác tử thông minh (CSE107)"** thành học phần **Bắt buộc** hoặc tối thiểu là Khuyến nghị mạnh (Strongly Recommended) cho khối KTPM và CNTT.
*   Kỹ sư phần mềm tương lai nếu không biết cách xây dựng RAG (Retrieval-Augmented Generation) hoặc Function Calling cho LLM thì sẽ mất lợi thế cạnh tranh rất lớn.

### 3.5. Nhóm môn An ninh mạng & Quản trị hệ thống
*(An ninh mạng, Mật mã ứng dụng, Quản trị mạng...)*
*   **Cách dạy mới:** Tích hợp AI vào quá trình tấn công và phòng thủ.
*   **Trọng tâm:** Dùng LLM để phân tích log hệ thống, phát hiện bất thường (Anomaly Detection). Đặc biệt, thêm chương trình giảng dạy về **AI Security** (Bảo mật cho các mô hình AI) như: chống Prompt Injection, Data Poisoning. Sinh viên phải biết dùng AI Agent để tự động hóa các kịch bản Pentest.

### 3.6. Môn "Kỹ năng số và Khai thác AI" (CSE105 - HK1)
*   **Đề xuất:** Cần vượt ra khỏi mức "Dùng ChatGPT để hỏi đáp". Cần dạy sinh viên:
    1.  Cấu trúc của một Prompt chuẩn kỹ thuật (Context - Task - Constraints - Format).
    2.  Nhận thức về Hallucination (ảo giác của AI) và cách kiểm chứng thông tin (Fact-checking).
    3.  Đạo đức AI và ranh giới giữa việc dùng AI để học (Learning) vs Gian lận (Cheating).
    4.  Sử dụng các công cụ Copilot trong ứng dụng văn phòng và tìm kiếm học thuật.

---
**KẾT LUẬN:** 
Chương trình đào tạo hiện tại có cấu trúc rất tốt. Việc điều chỉnh không nhất thiết phải thay đổi tên môn học hay mã môn, mà chủ yếu là **Cuộc cách mạng về Nội dung giảng dạy (Syllabus)** và **Phương pháp kiểm tra đánh giá** bên trong mỗi môn học. Bằng cách trang bị tư duy "Orchestrator" (người điều phối AI) thay vì "Coder", nhà trường sẽ tạo ra một thế hệ sinh viên miễn nhiễm với sự đào thải của AI, đáp ứng đúng "cơn khát" nhân sự AI Agent của thị trường.
