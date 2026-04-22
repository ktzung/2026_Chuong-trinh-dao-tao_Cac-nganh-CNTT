# Báo cáo đánh giá và đề xuất nâng cấp chương trình đào tạo CNTT trong kỷ nguyên AI

**Kính gửi:** Ban phát triển chương trình đào tạo  
**Chủ đề:** Đánh giá khung CTĐT đại học khối ngành CNTT (2025-2026) và giải pháp tích hợp năng lực AI agent, chuyển đổi phương pháp giảng dạy.

---

## 1. Đánh giá hiện trạng chương trình đào tạo

Qua phân tích 5 khung chương trình (ANM, CNTT, HTTT, KTPM, TTNT), dưới góc độ của một chuyên gia công nghệ và đào tạo trong kỷ nguyên AI, tôi có các nhận định sau:

### Điểm sáng

*   Đã đưa học phần **"Kỹ năng số và khai thác AI" (CSE105)** vào ngay học kỳ 1. Đây là bước đi rất tiên phong và đúng đắn.
*   Cấu trúc ngành linh hoạt, các môn học bắt kịp xu hướng cơ bản (điện toán đám mây, phân tích dữ liệu...).
*   Ngành TTNT đã có các môn cốt lõi về **AI tạo sinh và mô hình ngôn ngữ lớn (CSE134)**, **hệ thống tác tử thông minh (CSE107)**.

### Vấn đề tồn tại cốt lõi

*   **Tư duy đào tạo vẫn là "tạo ra thợ viết code" thay vì "kỹ sư kiến trúc":** Khung CTĐT vẫn phân bổ thời lượng lớn cho việc học cú pháp, ngôn ngữ lập trình cụ thể. Với sức mạnh của GenAI (Cursor, GitHub Copilot, Devin), AI đã làm xuất sắc việc này. Nếu vẫn dạy sinh viên tự viết từng dòng HTML/CSS hay API, sinh viên sẽ thấy nhàm chán, đối phó và lạm dụng AI.
*   **Thiếu kỹ năng "AI agentic" cho khối ngành ngoài AI:** Các ngành CNTT, KTPM, HTTT, ANM coi "AI tạo sinh" và "hệ thống tác tử" là môn *tự chọn*. Trong khi đó, thị trường hiện tại yêu cầu kỹ sư phần mềm hay an ninh mạng **bắt buộc** phải biết dùng AI agent để tự động hóa quy trình.
*   **Rủi ro từ phương pháp đánh giá:** Nếu cách kiểm tra vẫn là "viết chương trình giải bài toán X", sinh viên sẽ copy paste từ ChatGPT. Bằng cấp sẽ không còn phản ánh đúng năng lực.

---

## 2. Đề xuất chiến lược tổng thể

Để giải quyết bài toán sinh viên lạm dụng AI và đáp ứng tiêu chí tuyển dụng của doanh nghiệp (ưu tiên ứng viên có kỹ năng AI agent), tôi đề xuất 4 chiến lược tổng thể:

### 2.1. Chuyển dịch chuẩn đầu ra: từ "code generation" sang "code review & orchestration"

*   Sinh viên không cần phải thuộc cú pháp. Kỹ năng quan trọng nhất hiện nay là: **prompt engineering (viết yêu cầu rõ ràng), system design (thiết kế kiến trúc hệ thống), code review (đọc hiểu và kiểm duyệt mã AI sinh ra), và security auditing (kiểm tra lỗ hổng do AI tạo ra)**.

### 2.2. Bình thường hóa và bắt buộc sử dụng IDE có AI

*   Thay vì "cấm" sinh viên dùng AI, hãy **bắt buộc** sinh viên sử dụng các công cụ như Cursor, GitHub Copilot Workspace, v.v. từ học kỳ 3 trở đi.
*   **Yêu cầu nộp nhật ký prompt:** Trong các đồ án, sinh viên nộp mã nguồn kèm theo nhật ký các prompt đã dùng để tương tác với AI. Điểm số đánh giá dựa trên tư duy chia nhỏ vấn đề để ra lệnh cho AI, chứ không chỉ đánh giá sản phẩm cuối.

### 2.3. Cải tiến phương pháp đánh giá

*   Chuyển đổi bài thi từ "viết ứng dụng X" thành:
    *   **Debugging & refactoring:** Giảng viên cung cấp một đoạn code / hệ thống chạy sai hoặc chưa tối ưu (do AI tạo ra), yêu cầu sinh viên tìm lỗi, giải thích và sửa.
    *   **Phỏng vấn / vấn đáp:** Hỏi trực tiếp sinh viên về kiến trúc, lý do chọn thuật toán này mà không phải thuật toán khác để chống việc sinh viên nhờ AI làm toàn bộ mà không hiểu cốt lõi.

### 2.4. Phổ cập "AI agent" cho mọi chuyên ngành

*   Đưa khái niệm tích hợp AI (API integration, RAG, agents) vào làm tiêu chuẩn bắt buộc cho các đồ án môn học của tất cả các chuyên ngành, không chỉ riêng ngành TTNT.

---

## 3. Đề xuất cải tiến chi tiết từng nhóm môn học

### 3.1. Nhóm môn lập trình cơ sở (nhập môn lập trình, lập trình nâng cao, CTDL & giải thuật)

*   **Nhập môn lập trình (HK1):** Dạy thuần túy tư duy logic (computational thinking), hiểu cách máy tính hoạt động. Có thể cấm AI ở giai đoạn này để rèn luyện tư duy nền tảng.
*   **Lập trình nâng cao & CTDL (HK3):** Cho phép dùng AI. Bài tập tập trung vào: "Yêu cầu AI sinh ra 3 giải thuật khác nhau, sinh viên phân tích độ phức tạp thời gian/không gian (Big O) của từng giải thuật và chọn giải thuật tối ưu nhất". Tập trung dạy kỹ năng viết test case tự động.

### 3.2. Nhóm môn phát triển ứng dụng (Web, Mobile, Java, Windows)

*(Phát triển ứng dụng Web cơ bản/nâng cao, PTUD di động, Java...)*

> **Lưu ý quan trọng:** Phát triển web không phải là kỹ năng lỗi thời. Đây vẫn là nền tảng của ứng dụng di động (PWA, React Native, WebView), các hệ thống enterprise, và là vị trí việc làm phổ biến nhất trên thị trường. Vấn đề không phải là **bỏ web**, mà là **thay đổi hoàn toàn cách dạy**.

*   **Cách dạy mới — AI-native web development:**
    *   **Không dạy ghi nhớ cú pháp** HTML/CSS/JS — AI agent (v0.dev, Cursor, GitHub Copilot) giải quyết việc này trong vài giây. Sinh viên sử dụng AI agent để tạo toàn bộ UI người dùng ngay từ buổi học đầu tiên.
    *   **Dạy kiến trúc và tư duy tích hợp:** Phân chia module, thiết kế API, luồng xác thực (authentication), bảo mật web (OWASP), triển khai CI/CD.
    *   **Trung tâm là tích hợp AI vào sản phẩm:** Mọi đồ án web phải tích hợp ít nhất một tính năng AI (chatbot, gợi ý thông minh, RAG search, personalization bằng LLM).
    *   **Giảng viên đóng vai trò "product manager":** Giao yêu cầu thực tế (user story), sinh viên dụng AI agent triển khai, sau đó cả lớp review kiến trúc, bảo mật và hiệu năng của hệ thống AI đã tạo ra.
*   **Đầu ra cần đạt:** Sinh viên biết xây dựng một ứng dụng web hoàn chỉnh có tích hợp AI, deploy lên cloud và có thể giải thích toàn bộ kiến trúc trước hội đồng — không cần thuộc cú pháp, nhưng phải hiểu sâu hệ thống.

### 3.3. Nhóm môn kỹ thuật phần mềm & phân tích hệ thống

*(Công nghệ phần mềm, phân tích thiết kế hệ thống, quản lý dự án CNTT...)*

*   **Cách dạy mới:** Cập nhật phương pháp "AI-driven development".
*   **Trọng tâm:** Dùng LLM để tự động hóa việc trích xuất yêu cầu từ khách hàng (requirement elicitation), sinh UML diagram tự động, viết tài liệu đặc tả (SRS) bằng AI. Đưa công cụ AI vào quy trình Agile/Scrum để quản lý task.
*   **Kiểm thử phần mềm:** Dạy sinh viên cách dùng AI để tự động sinh ra hàng ngàn unit test case và mutation testing.

### 3.4. Nhóm môn trí tuệ nhân tạo & dữ liệu (dành cho tất cả các ngành)

*   **Đề xuất:** Nâng cấp học phần **"AI tạo sinh và mô hình ngôn ngữ lớn (CSE134)"** hoặc **"Hệ thống tác tử thông minh (CSE107)"** thành học phần **bắt buộc** hoặc tối thiểu là khuyến nghị mạnh cho khối KTPM và CNTT.
*   Kỹ sư phần mềm tương lai nếu không biết cách xây dựng RAG (Retrieval-Augmented Generation) hoặc function calling cho LLM thì sẽ mất lợi thế cạnh tranh rất lớn.

### 3.5. Nhóm môn an ninh mạng & quản trị hệ thống

*(An ninh mạng, mật mã ứng dụng, quản trị mạng...)*

*   **Cách dạy mới:** Tích hợp AI vào quá trình tấn công và phòng thủ.
*   **Trọng tâm:** Dùng LLM để phân tích log hệ thống, phát hiện bất thường (anomaly detection). Đặc biệt, thêm chương trình giảng dạy về **AI security** (bảo mật cho các mô hình AI) như: chống prompt injection, data poisoning. Sinh viên phải biết dùng AI agent để tự động hóa các kịch bản pentest.

### 3.6. Môn "Kỹ năng số và khai thác AI" (CSE105 - HK1)

*   **Đề xuất:** Cần vượt ra khỏi mức "dùng ChatGPT để hỏi đáp". Cần dạy sinh viên:
    1.  Cấu trúc của một prompt chuẩn kỹ thuật (Context - Task - Constraints - Format).
    2.  Nhận thức về hallucination (ảo giác của AI) và cách kiểm chứng thông tin (fact-checking).
    3.  Đạo đức AI và ranh giới giữa việc dùng AI để học (learning) và gian lận (cheating).
    4.  Sử dụng các công cụ Copilot trong ứng dụng văn phòng và tìm kiếm học thuật.

---

**Kết luận:**  
Chương trình đào tạo hiện tại có cấu trúc rất tốt. Việc điều chỉnh không nhất thiết phải thay đổi tên môn học hay mã môn, mà chủ yếu là **cuộc cách mạng về nội dung giảng dạy (syllabus)** và **phương pháp kiểm tra đánh giá** bên trong mỗi môn học. Bằng cách trang bị tư duy "orchestrator" (người điều phối AI) thay vì "coder", nhà trường sẽ tạo ra một thế hệ sinh viên miễn nhiễm với sự đào thải của AI, đáp ứng đúng "cơn khát" nhân sự AI agent của thị trường.
