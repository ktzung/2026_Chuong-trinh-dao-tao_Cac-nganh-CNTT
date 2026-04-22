# WEB-A1: Phát triển web hiện đại với AI agent

**Mã học phần đề xuất:** WEB-A1  
**Số tín chỉ:** 3 TC (30 tiết lý thuyết + 15 tiết thực hành tích hợp)  
**Học kỳ gợi ý:** Học kỳ 3 (năm 2)  
**Học phần tiên quyết:** Nhập môn lập trình, Lập trình hướng đối tượng  
**Học phần song hành / tiếp theo:** WEB-A2 (Tích hợp AI vào ứng dụng web & triển khai cloud)  
**Áp dụng cho ngành:** KTPM, CNTT, HTTT, TTNT  
**Công cụ bắt buộc:** Cursor IDE (hoặc VS Code + GitHub Copilot), Node.js / Python, Git/GitHub

---

## I. Mô tả học phần

Phát triển web vẫn là một trong những kỹ năng cốt lõi và phổ biến nhất trong ngành CNTT — nền tảng của ứng dụng di động, hệ thống doanh nghiệp và giao diện người dùng của mọi dịch vụ số. Học phần này **không bỏ qua kiến thức nền tảng web**, nhưng thay đổi hoàn toàn **phương pháp truyền đạt**.

**Sự khác biệt cốt lõi so với cách dạy truyền thống:**

| Cách dạy cũ | Cách tiếp cận mới |
|---|---|
| Ghi nhớ toàn bộ cú pháp HTML/CSS/JS | Hiểu *tại sao* mỗi thành phần tồn tại — đọc và sửa code nhanh |
| Tự gõ từng dòng từ đầu | Dùng AI sinh code — sau đó **bắt buộc đọc, hiểu và giải thích** |
| Học theo trình tự tuyến tính (tag → CSS → JS) | Học theo dự án thực tế từ tuần đầu — kiến thức nền được "fill in" khi cần |
| Thuộc cú pháp là mục tiêu | Thiết kế kiến trúc và tích hợp hệ thống là mục tiêu |

Triết lý cốt lõi: **"Không cần thuộc cú pháp nhưng phải hiểu sâu những gì AI viết ra — vì người điều khiển AI dốt hơn AI là mối nguy hiểm thực sự."**

---

## II. Chuẩn đầu ra

### Kiến thức
- **CĐR 1:** Giải thích cấu trúc và vai trò của HTML (cấu trúc), CSS (trình bày), JavaScript (hành vi) trong một trang web — không cần thuộc lòng nhưng phải đọc hiểu code một cách tự tin.
- **CĐR 2:** Giải thích kiến trúc client-server, HTTP/HTTPS, REST API — tại sao chúng hoạt động như vậy (nguyên lý), không chỉ cách dùng.
- **CĐR 3:** Mô tả các lớp của một ứng dụng web hiện đại: frontend, backend, database, authentication layer, API gateway.
- **CĐR 4:** Phân tích điểm mạnh/yếu của các kiến trúc web phổ biến (MVC, microservices, serverless) trong các bối cảnh khác nhau.

### Kỹ năng
- **CĐR 5:** Đọc hiểu và sửa code HTML/CSS/JS do AI tạo ra — xác định lỗi, giải thích từng đoạn code và điều chỉnh theo yêu cầu.
- **CĐR 6:** Sử dụng AI agent (Cursor, v0.dev, GitHub Copilot) để sinh giao diện và logic ứng dụng từ mô tả yêu cầu.
- **CĐR 7:** Thiết kế và triển khai REST API với xác thực (JWT/OAuth2), phân quyền và xử lý lỗi chuẩn — dùng AI sinh code, tự kiểm tra và vá lỗi.
- **CĐR 8:** Thực hiện code review cơ bản: xác định các vấn đề tiềm ẩn về bảo mật (OWASP Top 10 cơ bản) và hiệu năng trong code do AI hoặc người khác viết.
- **CĐR 9:** Viết prompt kỹ thuật hiệu quả để hướng dẫn AI tạo code chất lượng — biết đặt đúng ngữ cảnh, ràng buộc và định dạng đầu ra.

### Thái độ
- **CĐR 10:** Hình thành tư duy "hiểu trước, code sau" — không chấp nhận code chạy được mà không hiểu tại sao nó chạy.
- **CĐR 11:** Thái độ phản biện với code do AI sinh ra: không coi code AI là code đúng cho đến khi tự kiểm chứng được.

---

## III. Nội dung theo tuần

### Giai đoạn 1: Nền tảng web & cách web hoạt động (tuần 1–3)

> **Triết lý giai đoạn này:** Sinh viên học nền tảng HTML/CSS/JS KHÔNG bằng cách ghi nhớ cú pháp, mà bằng cách **đọc code AI sinh ra**, giải thích từng phần, và **tự tay sửa** theo yêu cầu thay đổi. Cách tiếp cận: *"AI viết bản nháp đầu tiên — bạn là người review và cải thiện."*

**Tuần 1 — Web hoạt động như thế nào: từ trình duyệt đến server**
- Nội dung lý thuyết: DNS, HTTP/HTTPS, request-response cycle, browser rendering pipeline. Vai trò của HTML (cấu trúc nội dung), CSS (trình bày và bố cục), JavaScript (hành vi và tương tác động).
- Thực hành: Dùng DevTools để "mổ xẻ" một website thực tế — xem Network tab, Elements tab, Console tab. Đặt câu hỏi: *"Dữ liệu đến từ đâu? Bao nhiêu file được tải? File nào làm trang chậm?"*
- Bài tập tự đọc: Giảng viên cung cấp một trang HTML/CSS hoàn chỉnh (30 dòng HTML + 50 dòng CSS). Sinh viên đọc, giải thích từng phần và thay đổi 5 điểm theo yêu cầu cụ thể. **Không cần viết mới từ đầu — cần hiểu và sửa.**
- Checkpoint: Vẽ sơ đồ kiến trúc của một website thực tế từ góc nhìn network traffic và giải thích vai trò của HTML/CSS/JS trong sơ đồ đó.

**Tuần 2 — HTML & CSS: cấu trúc và trình bày**
- Nội dung lý thuyết: Semantic HTML (header, nav, main, footer, article, section — tại sao dùng đúng tag quan trọng hơn dùng div cho mọi thứ). Box model. Flexbox và Grid (nguyên lý, không thuộc cú pháp).
- Thực hành: Dùng AI (v0.dev hoặc Cursor) để tạo giao diện một trang web từ mô tả bằng tiếng Việt. Sau đó: (1) đọc toàn bộ code AI tạo ra, (2) giải thích mục đích của từng section, (3) thực hiện 3 thay đổi thiết kế theo yêu cầu của giảng viên **bằng cách sửa trực tiếp vào code**.
- Checkpoint: Trình bày trước lớp: *"AI dùng Flexbox hay Grid ở đây? Tại sao lại chọn như vậy? Nếu muốn layout 3 cột thì cần sửa gì?"*

**Tuần 3 — JavaScript: hành vi và tương tác**
- Nội dung lý thuyết: DOM manipulation. Event handling. Fetch API — cách frontend giao tiếp với backend. Async/await (khái niệm, không thuộc cú pháp chi tiết). JSON.
- Thực hành: Dùng AI để sinh một trang web có form nhập liệu, validation và gọi API thực tế. Đọc JavaScript AI viết ra, giải thích luồng xử lý: *"Khi user bấm nút → chuyện gì xảy ra theo thứ tự?"* Sau đó thêm một validation rule mới vào form.
- Checkpoint: Live coding ngắn (10 phút, có AI, có tài liệu): giảng viên yêu cầu thêm tính năng nhỏ vào trang web từ tuần 2. Sinh viên phải hoàn thành bằng cách prompt AI và chỉnh sửa code.

---

### Giai đoạn 2: Kiến trúc hệ thống & API (tuần 4–7)

> **Triết lý giai đoạn này:** Từ "biết web là gì" đến "biết web hoạt động như thế nào ở tầng hệ thống". Đây là phần kiến thức AI chưa thể thay thế — tư duy kiến trúc đòi hỏi hiểu biết ngữ cảnh nghiệp vụ.

**Tuần 4 — Thiết kế API: hợp đồng giữa frontend và backend**
- Nội dung: REST principles (resource, stateless, HTTP verbs, status codes). Request/response format (JSON). So sánh REST vs GraphQL. OpenAPI/Swagger.
- Thực hành: Thiết kế API spec cho một hệ thống quản lý đơn hàng — viết bằng OpenAPI trước khi code. Sau đó dùng AI sinh backend từ spec đó.
- Checkpoint: Peer review API spec của nhóm khác: *"Endpoint này có đúng HTTP verb không? Status code 200 hay 201? Naming convention nhất quán chưa?"*

**Tuần 5 — Database: từ thiết kế đến thực thi**
- Nội dung: Thiết kế schema database (SQL và NoSQL), khi nào dùng loại nào. ORM là gì. Lỗi N+1 query — tại sao AI thường mắc phải.
- Thực hành: Dùng AI sinh schema và migration scripts. Giảng viên trình bày bug N+1 trong code AI vừa tạo — sinh viên tự tìm và sửa.
- Checkpoint: Giải thích trước lớp tại sao code AI tạo ra chậm và cách sửa.

**Tuần 6 — Xác thực & phân quyền**
- Nội dung: Session vs JWT vs OAuth2. Tại sao lưu mật khẩu plain text là thảm họa. RBAC. OWASP A01–A03.
- Thực hành: Dùng AI implement hệ thống đăng nhập JWT hoàn chỉnh. Sau đó tìm lỗ hổng bảo mật trong code AI tạo ra.
- Checkpoint: "Bug bounty mini" — nhóm A tìm lỗi trong code của nhóm B.

**Tuần 7 — Kiến trúc ứng dụng: chọn đúng pattern**
- Nội dung: Monolithic vs microservices. API Gateway. Khi nào nên dùng cái nào. Trade-off giữa độ phức tạp và khả năng mở rộng.
- Thực hành: Dùng AI sinh boilerplate cho kiến trúc microservices 2–3 service. Đọc và giải thích cấu trúc thư mục, luồng giao tiếp giữa các service.
- Checkpoint: Thuyết trình 5 phút: *"Hệ thống của chúng em sẽ bị sập ở đâu nếu có 10.000 user cùng lúc?"*

---

### Giai đoạn 3: Xây dựng full-stack với AI agent (tuần 8–11)

> **Triết lý giai đoạn này:** Sinh viên đã có nền tảng đủ để làm việc hiệu quả với AI. Mục tiêu là xây dựng sản phẩm thực, không phải bài tập học thuật.

**Tuần 8 — Kỹ thuật prompt cho lập trình web**
- Nội dung: Cấu trúc prompt kỹ thuật: Context → Task → Constraints → Format. Lỗi prompt phổ biến. Chain-of-thought prompting.
- Thực hành: So sánh kết quả prompt tệ vs prompt tốt cho cùng yêu cầu. Xây dựng "prompt library" cá nhân.
- Checkpoint: Nộp 5 prompt kỹ thuật có giải thích lý do thiết kế như vậy.

**Tuần 9 — Xây dựng frontend với AI agent**
- Nội dung: Quy trình làm việc với v0.dev, Cursor Composer. Component-driven design. Responsive design.
- Thực hành: Từ mô tả yêu cầu → AI tạo UI → **sinh viên đọc toàn bộ code, giải thích từng component, sửa ít nhất 3 điểm theo yêu cầu mới** → demo.
- *Lưu ý phương pháp:* Sinh viên được dùng AI tạo code nhưng **phải có khả năng giải thích mọi dòng code trong sản phẩm của mình**. Không giải thích được = không đạt checkpoint.
- Checkpoint: Demo UI — giảng viên chỉ vào bất kỳ element nào và hỏi: *"Em giải thích đoạn CSS này làm gì?"*

**Tuần 10 — Xây dựng backend & tích hợp full-stack**
- Nội dung: Dùng AI tạo backend API hoàn chỉnh. CORS. Environment variables. Kết nối frontend + backend + database.
- Thực hành: Build full-stack application — UI + API + database + authentication. Phải chạy được trên máy local.
- Checkpoint: Demo full-stack — giảng viên thao tác trực tiếp, hỏi về bất kỳ phần nào.

**Tuần 11 — Code review & kiểm thử**
- Nội dung: Đọc code AI tạo ra một cách phê phán. Các pattern nguy hiểm: XSS, SQL injection, secrets trong code. Dùng AI sinh test case.
- Thực hành: Bài kiểm tra giữa kỳ — giảng viên cung cấp 3 đoạn code AI (có cài lỗi). Sinh viên tìm, giải thích và sửa từng lỗi (mở tài liệu, mở AI).
- Checkpoint: Giữa kỳ — phân tích code, chỉ ra tất cả vấn đề bảo mật và hiệu năng.

---

### Giai đoạn 4: Triển khai & bảo vệ (tuần 12–15)

**Tuần 12 — Triển khai lên cloud**
- Nội dung: Docker cơ bản. Vercel/Railway/Render. Environment variables trên production. Không commit secrets.
- Thực hành: Deploy ứng dụng từ tuần 10 lên cloud. URL phải truy cập được từ Internet.
- Checkpoint: Link production phải hoạt động khi demo cuối kỳ.

**Tuần 13 — Hoàn thiện đồ án**
- Yêu cầu: Ứng dụng web full-stack, deployed trên cloud, có ít nhất 1 tính năng AI-powered.
- Nộp kèm: Nhật ký prompt (toàn bộ AI interaction trong quá trình xây dựng).

**Tuần 14–15 — Oral defense**

Format (15 phút/sinh viên):
- **5 phút:** Demo live ứng dụng.
- **10 phút:** Trả lời câu hỏi — giảng viên chọn ngẫu nhiên bất kỳ phần nào trong code và hỏi.

Câu hỏi mẫu:
> *"Em giải thích đoạn useEffect này làm gì? Tại sao có dependency array ở đây?"*  
> *"JWT của em expire sau bao lâu? Nếu token bị đánh cắp, em có cơ chế revoke không?"*  
> *"Database của em có bị SQL injection qua ORM không? Em kiểm tra thế nào?"*  
> *"Em đã prompt AI như thế nào để tạo component X? Tại sao không dùng cách Y?"*

---

## IV. Phương pháp đánh giá

| Thành phần | Trọng số | Mô tả |
|---|---|---|
| Checkpoint hàng tuần (tuần 1–12) | 25% | Rubric rõ ràng — tập trung vào khả năng giải thích, không phải sản phẩm |
| Bài kiểm tra giữa kỳ (tuần 11) | 20% | Code review — mở AI, mở tài liệu, tìm lỗi và giải thích |
| Đồ án — sản phẩm | 25% | Kiến trúc, tính năng, code quality, deployment |
| Đồ án — nhật ký prompt | 10% | Chất lượng AI interaction; thể hiện tư duy phân tích |
| Oral defense | 20% | Giải thích code, kiến trúc và quyết định thiết kế |

> **Nguyên tắc đánh giá xuyên suốt:** Sinh viên được dùng AI trong mọi hình thức đánh giá. Điểm số phản ánh **khả năng hiểu và giải thích**, không phải khả năng viết code từ đầu. Sinh viên không giải thích được code trong sản phẩm của mình sẽ không qua được oral defense.

---

## V. Chính sách về AI

| Hoạt động | Chính sách |
|---|---|
| Dùng AI sinh code | ✅ Được phép và khuyến khích |
| Dùng AI trong bài kiểm tra | ✅ Được phép — đây là kỹ năng cần có |
| Dùng AI khi oral defense | ✅ Được phép — nhưng phải giải thích câu trả lời AI đưa ra |
| Nộp code mà không hiểu gì | ❌ Phát hiện qua oral defense — dẫn đến điểm 0 phần defense |
| Không đọc code AI tạo ra | ❌ Vi phạm triết lý học phần — phản ánh qua checkpoint |

---

## VI. Tài liệu & công cụ

### Tài liệu tham khảo chính
- [MDN Web Docs](https://developer.mozilla.org) — nguồn tham khảo HTML/CSS/JS chuẩn nhất, luôn cập nhật
- [javascript.info](https://javascript.info) — giải thích JavaScript từ nguyên lý, không từ cú pháp
- [OWASP Top 10](https://owasp.org/www-project-top-ten/) — bắt buộc đọc trước tuần 6
- [The Twelve-Factor App](https://12factor.net) — nguyên tắc ứng dụng cloud-native

### Công cụ bắt buộc
- Cursor IDE / VS Code + GitHub Copilot
- Git & GitHub (GitHub Student Developer Pack)
- Node.js LTS hoặc Python 3.12+
- Docker Desktop
- Postman hoặc Thunder Client

---

## VII. Định hướng đồ án theo ngành

| Ngành | Trọng tâm đồ án WEB-A1 |
|---|---|
| **KTPM** | Full-stack app có authentication, unit test cơ bản, CI/CD |
| **CNTT** | Web app vận hành trên cloud, có monitoring log cơ bản |
| **HTTT** | Dashboard kết nối database doanh nghiệp, có data visualization |
| **TTNT** | Web interface demo mô hình AI (text classification, Q&A đơn giản) |

---

*Học phần WEB-A1 — Khoa CNTT, Trường Đại học Thủy lợi. Phiên bản 2.0 (cập nhật) — Tháng 4/2026.*
