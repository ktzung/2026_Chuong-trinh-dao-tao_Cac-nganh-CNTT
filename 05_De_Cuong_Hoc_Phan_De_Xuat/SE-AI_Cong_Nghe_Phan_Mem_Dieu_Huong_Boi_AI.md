# SE-AI: Công nghệ phần mềm điều hướng bởi AI (AI-Driven Software Engineering)

**Mã học phần đề xuất:** SE-AI  
**Số tín chỉ:** 3 TC  
**Học kỳ gợi ý:** Học kỳ 4 (năm 2)  
**Học phần tiên quyết:** WEB-A1, Cấu trúc dữ liệu & giải thuật  
**Áp dụng cho ngành:** KTPM (bắt buộc), CNTT (khuyến nghị)  
**Công cụ bắt buộc:** Cursor IDE, GitHub Copilot, GitHub Projects, Jira (hoặc Linear)

---

## I. Mô tả học phần

Công nghệ phần mềm truyền thống dạy sinh viên Waterfall, Scrum thuần túy, UML vẽ tay và viết tài liệu SRS bằng Word. Tất cả những điều đó vẫn đúng về nguyên lý — nhưng **cách thực thi đã thay đổi hoàn toàn**.

Học phần này dạy sinh viên làm kỹ sư phần mềm trong kỷ nguyên AI: dùng LLM để tự động hóa việc phân tích yêu cầu, sinh tài liệu, tạo test case, review code và quản lý dự án — trong khi vẫn nắm vững các nguyên lý nền tảng (vì AI cần người hiểu nguyên lý để ra lệnh đúng).

Triết lý: **"Kỹ sư phần mềm không còn viết code — họ thiết kế hệ thống và điều phối AI. Nhưng để điều phối AI, họ phải hiểu sâu hơn thế hệ trước."**

---

## II. Chuẩn đầu ra

### Kiến thức
- **CĐR 1:** Giải thích sự khác biệt giữa SDLC truyền thống và AI-augmented SDLC, chỉ ra các bước nào AI có thể tự động hóa và bước nào vẫn cần tư duy người.
- **CĐR 2:** Mô tả các kỹ thuật requirement elicitation với AI: phỏng vấn có hỗ trợ LLM, phân tích tài liệu tự động, trích xuất user story từ văn bản phi cấu trúc.
- **CĐR 3:** Phân tích các mô hình kiến trúc phần mềm (monolith, microservices, event-driven) và khi nào AI hỗ trợ thiết kế tốt hơn.
- **CĐR 4:** Mô tả các phương pháp kiểm thử tự động bằng AI: test case generation, mutation testing, fuzz testing và regression testing.

### Kỹ năng
- **CĐR 5:** Dùng LLM để phân tích yêu cầu từ khách hàng (transcript phỏng vấn, email, tài liệu), trích xuất user story và acceptance criteria có cấu trúc.
- **CĐR 6:** Tạo tài liệu đặc tả (SRS) và sơ đồ kiến trúc (UML, C4 model) bằng AI từ mô tả yêu cầu ngắn gọn.
- **CĐR 7:** Thiết lập CI/CD pipeline tự động gồm: lint, unit test, integration test, security scan và deploy — với AI hỗ trợ viết pipeline script.
- **CĐR 8:** Dùng AI để tự động sinh và chạy test case, phân tích kết quả và đề xuất sửa lỗi.
- **CĐR 9:** Thực hiện code review dựa trên AI: phát hiện code smell, vi phạm SOLID, lỗ hổng bảo mật và vấn đề hiệu năng trong code do người hoặc AI viết ra.

### Thái độ
- **CĐR 10:** Trách nhiệm nghề nghiệp: hiểu rằng AI sinh ra tài liệu và code sai là trách nhiệm của kỹ sư phụ trách, không phải của AI.
- **CĐR 11:** Tư duy hệ thống: luôn xem xét toàn bộ vòng đời phần mềm (SDLC) thay vì chỉ tập trung vào giai đoạn hiện tại.

---

## III. Nội dung theo tuần

### Giai đoạn 1: AI-Augmented Requirements & Design (tuần 1–5)

**Tuần 1 — SDLC trong kỷ nguyên AI: cái gì thay đổi, cái gì không**
- Nội dung: Review nhanh SDLC (Agile/Scrum) — sinh viên tự đọc trước. Phân tích từng bước: Requirements → Design → Implementation → Testing → Deployment → Maintenance và AI có thể tự động hóa bao nhiêu % mỗi bước.
- Thực hành: Nghiên cứu case study — GitHub đã dùng Copilot để tăng tốc độ delivery của chính họ như thế nào. Rút ra 5 bài học thực tiễn.
- Checkpoint: Vẽ sơ đồ SDLC mới có annotation AI vs Human ở từng bước.

**Tuần 2 — Requirement Elicitation với AI: từ phỏng vấn đến user story**
- Nội dung: Kỹ thuật phỏng vấn khách hàng. Dùng LLM để phân tích transcript cuộc họp, email và tài liệu mơ hồ. Trích xuất functional requirements và non-functional requirements tự động. Phát hiện mâu thuẫn trong requirements.
- Thực hành: Giảng viên đóng vai khách hàng mô tả một hệ thống cần xây dựng (mơ hồ, thiếu chi tiết, có mâu thuẫn). Sinh viên phỏng vấn, ghi lại transcript, dùng LLM để phân tích và trích xuất requirements có cấu trúc.
- Checkpoint: So sánh requirements do sinh viên tự phân tích vs do LLM phân tích. Điểm khác biệt và thiếu sót.

**Tuần 3 — User Story, Acceptance Criteria và Backlog với AI**
- Nội dung: Chuẩn viết user story (As a... I want... So that...). Gherkin syntax cho acceptance criteria (Given-When-Then). Dùng AI để sinh user story từ requirements, ước lượng story point và sắp xếp backlog.
- Thực hành: Từ requirements tuần 2, dùng AI sinh toàn bộ product backlog. Import vào GitHub Projects hoặc Jira. Refinement session — phát hiện và sửa các story không đủ tiêu chuẩn INVEST.
- Checkpoint: Backlog phải có ≥ 20 user story, có acceptance criteria Gherkin, có priority và story point.

**Tuần 4 — AI-assisted System Design & Architecture**
- Nội dung: C4 model (Context → Container → Component → Code). Dùng AI để sinh sơ đồ kiến trúc từ requirements. Architecture Decision Record (ADR). Phân tích trade-off tự động.
- Thực hành: Từ product backlog tuần 3, dùng AI để đề xuất kiến trúc hệ thống. Sinh C4 diagram, ERD và sequence diagram. Viết ADR cho 3 quyết định kiến trúc quan trọng nhất.
- Checkpoint: Thuyết trình kiến trúc 10 phút. Hội đồng hỏi: *"Tại sao chọn kiến trúc này? Điểm yếu là gì?"*

**Tuần 5 — SRS & Technical Documentation với AI**
- Nội dung: Cấu trúc tài liệu SRS (IEEE 830 chuẩn). Dùng LLM để sinh SRS từ requirements và kiến trúc. API documentation (OpenAPI/Swagger). README engineering.
- Thực hành: Sinh toàn bộ SRS cho hệ thống đang thiết kế bằng AI. Review chéo: nhóm A review SRS của nhóm B và chỉ ra điểm chưa đạt chuẩn.
- Checkpoint: SRS phải đủ chi tiết để nhóm khác có thể implement mà không cần hỏi thêm.

---

### Giai đoạn 2: AI-Augmented Testing & Quality (tuần 6–10)

**Tuần 6 — Kiểm thử phần mềm trong kỷ nguyên AI**
- Nội dung: Testing pyramid (unit → integration → E2E). Khi nào dùng loại test nào. Test-Driven Development (TDD) với AI. Property-based testing. Dùng AI để sinh test case từ acceptance criteria.
- Thực hành: Từ acceptance criteria Gherkin tuần 3, dùng AI để sinh toàn bộ unit test suite. Mục tiêu: ≥ 50 test case cho 1 module.
- Checkpoint: Chạy test suite. Coverage phải ≥ 80%.

**Tuần 7 — Mutation Testing & AI-powered QA**
- Nội dung: Mutation testing là gì và tại sao coverage cao không có nghĩa là test tốt. Dùng AI để phân tích kết quả mutation testing và đề xuất test mạnh hơn. Fuzz testing cơ bản.
- Thực hành: Chạy mutation testing trên test suite tuần 6. AI phân tích các "surviving mutant" và đề xuất test mới để kill chúng.
- Checkpoint: Mutation score phải ≥ 60% sau khi cải thiện.

**Tuần 8 — Code Review với AI: từ checker đến mentor**
- Nội dung: Quy trình code review chuyên nghiệp. Dùng AI để review code: phát hiện code smell (SOLID violations, DRY, SRP), lỗ hổng bảo mật (OWASP), vấn đề hiệu năng. Pull Request workflow.
- Thực hành: Mỗi nhóm nộp 200 dòng code để nhóm khác review — vừa dùng AI vừa review thủ công. So sánh kết quả. Giảng viên chấm quality của review, không phải quality của code.
- Checkpoint: Mỗi sinh viên viết ít nhất 5 comment review có chiều sâu (không chỉ "đổi tên biến này") trong PR của nhóm khác.

**Tuần 9 — CI/CD Pipeline: tự động hóa toàn bộ quy trình**
- Nội dung: GitHub Actions workflow. Pipeline stages: lint → test → security scan → build → deploy. Dùng AI để sinh pipeline script. Notification và alerting khi pipeline fail.
- Thực hành: Thiết lập CI/CD pipeline hoàn chỉnh cho dự án nhóm. Mỗi PR phải pass toàn bộ pipeline trước khi merge.
- Checkpoint: Giảng viên cố tình push code có bug → pipeline phải bắt được và block merge.

**Tuần 10 — DevSecOps: bảo mật tích hợp vào pipeline**
- Nội dung: Shift-left security. SAST (Static Application Security Testing). DAST (Dynamic). Dependency scanning. Secret scanning (không commit API key). Software Bill of Materials (SBOM).
- Thực hành: Tích hợp công cụ bảo mật vào CI pipeline: Snyk hoặc Trivy cho dependency scan, GitHub Secret Scanning, SonarQube cơ bản.
- Checkpoint: Pipeline phải chặn deploy nếu có critical vulnerability hoặc secret bị lộ.

---

### Giai đoạn 3: Quản lý dự án AI & Đồ án (tuần 11–15)

**Tuần 11 — AI-augmented Project Management**
- Nội dung: Agile với AI: dùng LLM để viết sprint report tự động, phân tích velocity, phát hiện risk sớm. AI trong retrospective. Công cụ: GitHub Projects + Copilot, Linear AI.
- Thực hành: Mô phỏng 1 sprint 2 tuần rút gọn (trong 3 tiết). Sprint planning → daily standup (5 phút, dùng AI tóm tắt) → sprint review → retrospective với AI phân tích.
- Checkpoint: Sprint report được tạo tự động bằng AI từ commit history và closed issues.

**Tuần 12–13 — Đồ án nhóm: Mini Product Development**

Yêu cầu: Mỗi nhóm 3–4 người xây dựng một sản phẩm phần mềm nhỏ hoàn chỉnh theo đúng quy trình đã học, có sử dụng AI ở mọi bước SDLC. Phải nộp đầy đủ artifacts:

| Artifact | Tuần nộp |
|---|---|
| Product backlog (≥ 20 stories, AI-generated + reviewed) | Tuần 12 |
| SRS document (AI-generated + reviewed) | Tuần 12 |
| Architecture diagram (C4 + ADR) | Tuần 12 |
| Test suite (AI-generated, coverage ≥ 80%) | Tuần 13 |
| CI/CD pipeline (chạy được) | Tuần 13 |
| Prompt log (toàn bộ AI interaction) | Tuần 13 |

**Tuần 14–15 — Demo & Process Defense**

Format bảo vệ (25 phút/nhóm):
- **5 phút:** Demo sản phẩm live (phải deployed, không phải localhost).
- **5 phút:** Demo quy trình — mở pipeline, chỉ vào test results, chỉ vào coverage report.
- **15 phút:** Hỏi từng thành viên về các quyết định trong quá trình phát triển.

Câu hỏi mẫu:
> *"SRS của nhóm thiếu non-functional requirements về performance. Nếu hệ thống cần chịu 10.000 concurrent users, nhóm sẽ thêm gì vào kiến trúc?"*  
> *"Test suite của nhóm có 82% coverage nhưng mutation score chỉ 45%. Điều đó có nghĩa là gì?"*  
> *"CI pipeline của nhóm mất 8 phút để chạy. Nhóm sẽ tối ưu thế nào để giảm xuống dưới 3 phút?"*  
> *"Nhóm đã dùng AI để làm gì? Bước nào AI làm tệ nhất và tại sao?"*

---

## IV. Phương pháp đánh giá

| Thành phần | Trọng số | Mô tả |
|---|---|---|
| Checkpoint hàng tuần (tuần 1–11) | 25% | 11 checkpoint, có rubric rõ ràng |
| Kiểm tra giữa kỳ (tuần 8) | 15% | Code review exercise — đánh giá chất lượng review |
| Đồ án — artifacts | 30% | SRS, backlog, architecture, test suite, CI/CD |
| Đồ án — prompt log | 10% | Chất lượng AI interaction trong cả dự án |
| Process defense | 20% | Giải thích quyết định quy trình, không phải code |

> **Điều cần lưu ý:** Điểm đồ án **không** dựa trên sản phẩm đẹp hay nhiều tính năng. Điểm dựa trên **chất lượng quy trình**: requirements có đủ không, test có nghiêm túc không, pipeline có chạy không, team có retrospect thực sự không.

---

## V. Tài liệu tham khảo

### Bắt buộc đọc
- [GitHub Engineering Blog](https://github.blog/engineering/) — thực tế áp dụng AI trong SE tại GitHub
- [OWASP DevSecOps Guideline](https://owasp.org/www-project-devsecops-guideline/)
- [C4 Model](https://c4model.com) — kiến trúc hệ thống dạng sơ đồ
- [Conventional Commits](https://www.conventionalcommits.org) — chuẩn commit message

### Công cụ bắt buộc dùng trong học phần
- GitHub + GitHub Actions + GitHub Projects
- Cursor IDE / GitHub Copilot
- SonarQube Cloud (free tier) hoặc Snyk (miễn phí cho sinh viên)
- PlantUML hoặc Mermaid (vẽ diagram trong Markdown)
- Postman (API testing)

---

## VI. So sánh với CSE481 (Công nghệ phần mềm cũ)

| Nội dung | CSE481 (cũ) | SE-AI (mới) |
|---|---|---|
| Yêu cầu phần mềm | Viết SRS thủ công theo mẫu | LLM trích xuất từ phỏng vấn, AI sinh SRS |
| Thiết kế | Vẽ UML bằng tay (Visio, draw.io) | AI sinh C4 diagram từ mô tả, ADR tự động |
| Kiểm thử | Viết test case thủ công | AI sinh test suite, mutation testing tự động |
| Triển khai | Zip và upload FTP | CI/CD pipeline tự động với GitHub Actions |
| Quản lý dự án | Gantt chart trong Excel | AI-assisted sprint planning và reporting |
| Đánh giá | Nộp tài liệu + sản phẩm demo | Process defense + artifact quality + prompt log |

---

*Học phần SE-AI — Khoa CNTT, Trường Đại học Thủy lợi. Phiên bản 1.0 — Tháng 4/2026.*
