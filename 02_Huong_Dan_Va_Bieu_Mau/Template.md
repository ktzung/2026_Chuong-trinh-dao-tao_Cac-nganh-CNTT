# PHẦN I: ĐÁNH GIÁ TỔNG THỂ

Khung CTĐT K62 của 3 ngành **CNTT / HTTT / KTPM** trong file đính kèm phản ánh khá đúng tư duy đào tạo giai đoạn **2018–2020**: tập trung mạnh vào lập trình truyền thống, hạ tầng cơ bản, phát triển phần mềm cổ điển [1]. Các học phần hiện diện rõ gồm: Nhập môn lập trình, Lập trình nâng cao, OOP, Cấu trúc dữ liệu & giải thuật, Cơ sở dữ liệu, Công nghệ phần mềm, Java/Web/Windows Programming, Mạng máy tính, Hệ điều hành, Trí tuệ nhân tạo (chỉ mức nhập môn), Đồ án/Thực tập tốt nghiệp [1]. Một số học phần tự chọn như Deep Learning, IR, Cloud, Big Data... nhưng nằm ở cuối chương trình và chưa phải lõi bắt buộc [1].

## I. Chẩn đoán chiến lược: Vì sao CTĐT hiện tại bắt đầu lỗi thời?

**1. Chương trình đang đào tạo cho thị trường lao động của 2015–2020**
Mô hình hiện tại giả định: học lập trình → thành junior developer → viết CRUD/web/app → đi làm [2]. 
Nhưng AI đã phá vỡ chuỗi này [2]. Hiện nay: GitHub Copilot, Cursor, Claude Code, Devin, OpenAI Codex Agent, Windsurf, AutoGen, LangGraph, OpenHands đang thay thế mạnh phần: viết boilerplate code, CRUD API, unit test cơ bản, debugging cơ bản, frontend scaffolding, SQL query đơn giản [2]. 
=> phần việc vốn dành cho sinh viên mới ra trường đang bị AI ăn mòn cực mạnh [2].

## II. Thay đổi lớn từ phía doanh nghiệp tuyển dụng
Doanh nghiệp hiện tuyển [3]:
- **Không còn hỏi:** Biết Java không? Biết CRUD không? Biết PHP không? [3]
- **Họ đang hỏi:** Có biết dùng AI coding assistant không? Có biết prompt engineering không? Có biết orchestration multi-agent không? Có biết MLOps không? Có biết cloud deployment không? Có biết data pipeline không? Có biết security/privacy AI systems không? Có thể làm việc cùng AI agent không? [3]

## III. Điểm yếu lớn nhất của CTĐT hiện tại

**1. Quá nhiều môn “implementation-heavy nhưng low-value”**
Ví dụ: Windows Programming, Java Programming, Web Development kiểu cũ, Application Development theo framework cũ, một số môn thiên syntax hơn tư duy [3, 4].
Vấn đề: AI viết nhanh hơn sinh viên [4]. Nếu vẫn giữ cách dạy: "làm website bán hàng" => sinh viên copy ChatGPT [4].

**2. AI chỉ xuất hiện như môn phụ**
Trong CTĐT hiện tại: Artificial Intelligence, Deep Learning (tự chọn) => quá yếu [4]. Trong tương lai AI phải là năng lực nền tảng như lập trình [4].

**3. Thiếu AI Engineering**
Không có môn: LLM engineering, RAG, AI Agents, Vector DB, AI Product Design, Prompt engineering, Model deployment [4, 5].

**4. Thiếu Data-centric thinking**
Thiếu: Data engineering, Feature engineering, Data governance, Data product [5].

**5. Thiếu Cloud-native engineering**
Cloud hiện tại chỉ là tự chọn [5]. Trong khi doanh nghiệp cần: Docker, Kubernetes, CI/CD, AWS/GCP/Azure, DevOps [5].

**6. Thiếu Human-AI Collaboration**
Sinh viên không được dạy: cách làm việc với AI, cách đánh giá output AI, cách kiểm chứng hallucination, cách giám sát agent [5].

## IV. Tư duy đào tạo mới cần chuyển sang
Từ đào tạo coder sang đào tạo AI-native problem solver [5].

## V. Kiến trúc chương trình mới đề xuất
**Tầng 1: Foundations (giữ lại nhưng tinh gọn)**
- Giữ: Programming Fundamentals, Data Structures, Algorithms, Database, OS, Networks, Software Engineering, Probability/Statistics [6].
- Loại bỏ trùng lặp: Windows Programming, các môn framework lỗi thời, các môn quá syntax-driven [6].

## VI. Thêm khối AI Core bắt buộc
- **Year 1–2 - AI Literacy for Engineers:** Prompt engineering, AI ethics, AI limitations, Human-AI collaboration [6].
- **Applied Machine Learning:** supervised learning, unsupervised learning, evaluation [6].
- **Deep Learning Foundations:** CNN, Transformer, LLM basics [7].
- **Data Engineering:** ETL, pipelines, Spark, streaming [7].

## VII. Thêm AI Engineering Layer
- **LLM Engineering:** fine-tuning, RAG, embeddings, vector DB [7].
- **AI Agent Systems:** LangChain, LangGraph, AutoGen, multi-agent systems [7].
- **MLOps:** deployment, monitoring, model drift [7].
- **AI Product Engineering:** ship AI products [7].

## VIII. Cloud & Systems Layer
Bắt buộc: Docker, Kubernetes, Cloud Architecture, Distributed Systems, Microservices [7].

## IX. Security Layer
Thêm: AI Security, Adversarial attacks, Model privacy, Federated learning, Secure deployment [7, 8].

## X. Chuyển đồ án từ “viết app” sang “build product”
- Hiện tại: xây website quản lý thư viện [8].
- Đề xuất: Option 1 (AI startup product), Option 2 (Vertical AI SaaS), Option 3 (Autonomous agent), Option 4 (AI for agriculture/water/resource - rất phù hợp định hướng Thủy Lợi) [8].

## XI. Đề xuất sửa theo từng môn hiện tại
**1. Nhập môn lập trình:** Sửa thành "Programming in the Age of AI". Thêm: Copilot usage, code review AI, debugging AI-generated code [8].
**2. Lập trình nâng cao:** Đổi thành: Software Engineering with AI Pair Programming [8].
**3. Java Programming:** Khuyến nghị bỏ bắt buộc. Chuyển thành: Backend Engineering (dạy: API, distributed systems, deployment) [9].
**4. Windows Programming:** Khuyến nghị loại bỏ. Rất lỗi thời [9].
**5. Web Development:** Đổi thành: Full-stack + AI-assisted development [9].
**6. Database:** Thêm: NoSQL, Vector DB, data pipelines [9].
**7. Artificial Intelligence:** Hiện quá nhập môn. Phải chia thành: ML, DL, LLM, AI Engineering [9].
**8. Software Engineering:** Thêm: AI-assisted SDLC, autonomous testing, AI project management [9].
**9. Information System Analysis Design:** Thêm: product thinking, platform thinking, AI workflow design [9, 10].
**10. Graduation Thesis:** Khuyến khích: startup product, publishable research, enterprise AI solution [10].

## XII. Đề xuất riêng cho từng ngành
- **CNTT:** Tập trung AI systems, cloud, distributed computing, security [10].
- **KTPM:** Tập trung AI-native software engineering, DevOps, product engineering [10].
- **HTTT:** Tập trung data engineering, analytics, enterprise AI systems, business intelligence [10].

## XIII. Cải tổ phương pháp đánh giá
Phải chuyển sang: Live coding interview, Oral defense, Build in class, AI audit log submission [10, 11]. Sinh viên phải nộp: prompt history, AI usage log, reasoning log [11].

## XIV. Mô hình đào tạo mới đề xuất
- Year 1: Computing + AI literacy [11].
- Year 2: Core CS + Data + ML [11].
- Year 3: AI Engineering + Cloud + Product [11].
- Year 4: Specialization + Startup/Research [11].

## XV. Các môn mới nên bổ sung ngay
Prompt Engineering, LLM Engineering, AI Agents, Cloud Native Development, MLOps, Data Engineering, AI Product Management, Cybersecurity for AI, Human-AI Collaboration, Responsible AI [11, 12].

## XVI. Nếu không thay đổi sẽ xảy ra điều gì?
5 năm tới: sinh viên khó cạnh tranh, doanh nghiệp bỏ qua sinh viên truyền thống, chương trình mất sức hút tuyển sinh, giảng viên dạy theo cách cũ bị đào thải [12].

## XVII. Kết luận chiến lược
Trường không nên đào tạo: “người viết code” mà phải đào tạo: “AI-native engineer”, cao hơn nữa: “problem solver + system architect + AI collaborator” [12]. Người thắng trong 5 năm tới không phải người code nhanh nhất. Mà là người: hiểu hệ thống, biết dùng AI, biết kiểm soát AI, biết tạo sản phẩm, biết giải quyết bài toán thật [12, 13].

**Đề xuất hành động ngay trong 12 tháng:** [13]
- Giai đoạn 1: Rà soát toàn bộ môn lỗi thời
- Giai đoạn 2: Thiết kế lại CLO/PLO theo AI era
- Giai đoạn 3: Pilot 5 môn mới
- Giai đoạn 4: Thay đổi cách đánh giá
- Giai đoạn 5: Liên kết doanh nghiệp AI

**Kết luận mạnh mẽ nhất:** AI không làm ngành CNTT chết. AI đang giết chết **chương trình đào tạo CNTT lỗi thời**. Và đây chính là thời điểm phải tái thiết chương trình từ gốc [13].

---

# PHẦN 2: Đề xuất chương trình đào tạo chi tiết cho ngành Hệ thống thông tin (HTTT)

Theo hướng **AI-native, data-centric, enterprise-oriented**, được xây trên nền khung hiện tại của chương trình K62 [13]. Trong khung hiện hành, ngành HTTT đã có nhiều học phần nền quan trọng... Tuy nhiên, phần AI, dữ liệu hiện đại, cloud, product và enterprise systems vẫn chưa trở thành trục lõi xuyên suốt [13].

## 1. Định vị lại ngành HTTT
Ngành HTTT không nên tiếp tục được hiểu hẹp là: học cơ sở dữ liệu + phân tích thiết kế + làm phần mềm quản lý [14]. Trong bối cảnh mới, HTTT phải được định vị là ngành đào tạo: **kiến trúc sư hệ thống số cho tổ chức**, có năng lực kết nối **nghiệp vụ – dữ liệu – quy trình – nền tảng số – AI – ra quyết định** [14].

## 2. Chuẩn đầu ra đề xuất cho ngành HTTT
**2.1. Kiến thức:** Nắm được 6 lớp tri thức gồm nền tảng CNTT, nền tảng HTTT, dữ liệu, AI ứng dụng, triển khai hệ thống, quản trị và an toàn [15, 16].
**2.2. Kỹ năng:** Khảo sát, phân tích, thiết kế quy trình, xây hệ thống có AI, làm dashboard, triển khai cloud, sử dụng AI đúng cách... [16].
**2.3. Năng lực nghề nghiệp:** Business Analyst, Data Analyst, Product Analyst, AI-enabled Information System Developer, Junior Solution Architect, ERP/CRM/Workflow Consultant, Data & Process Engineer [17].

## 3. Quan điểm thiết kế chương trình mới
1. Giữ nền tảng, nhưng không dạy theo kiểu cũ [17].
2. HTTT phải lấy bài toán tổ chức làm trung tâm [18].
3. Dữ liệu và AI phải là trục bắt buộc [18].
4. Cloud và tích hợp phải là năng lực cốt lõi [18].
5. Đánh giá phải chống lệ thuộc AI [18].

## 4. Cấu trúc chương trình đề xuất
Khối A (Giáo dục đại cương), Khối B (Nền tảng CNTT – Toán – Dữ liệu), Khối C (Nền tảng HTTT và phân tích nghiệp vụ), Khối D (Data – Analytics – AI for Information Systems), Khối E (Enterprise Systems – Cloud – Security – Product), Khối F (Dự án tích hợp – Thực tập – Đồ án) [19, 20].

## 5. Đề xuất chương trình chi tiết theo học kỳ
- **Năm 1:** Nền tảng số và tư duy hệ thống (Nhấn mạnh môn Nhập môn Hệ thống thông tin) [20].
- **Năm 2:** Cốt lõi CNTT + Cốt lõi HTTT (Thêm môn Phân tích nghiệp vụ và mô hình hóa quy trình, Trực quan hóa dữ liệu cơ bản) [21, 22].
- **Năm 3:** Data – AI – Enterprise Systems (Kho dữ liệu và BI, ML cho HTTT, Tích hợp hệ thống và API, Cloud cho HTTT, ERP/CRM...) [22, 23].
- **Năm 4:** AI-native Information Systems + chuyên sâu + dự án (LLM và AI Agent cho HTTT, Chuyển đổi số, Pháp lý và đạo đức AI) [24].

## 6. Danh mục học phần lõi mới nên bổ sung
Nhập môn HTTT trong kỷ nguyên AI, Phân tích nghiệp vụ và mô hình hóa quy trình, Trực quan hóa dữ liệu cơ bản, Kho dữ liệu và BI, Quản trị dữ liệu và chất lượng dữ liệu, Machine Learning cho HTTT, Tích hợp hệ thống và API, Điện toán đám mây cho HTTT, ERP/CRM, LLM và AI Agent cho HTTT, Chuyển đổi số và kiến trúc doanh nghiệp, Pháp lý/đạo đức và quản trị AI/dữ liệu [24-27].

## 7. Các học phần nên điều chỉnh từ chương trình hiện tại
Cơ sở dữ liệu (thêm NoSQL, Vector DB), Phân tích & thiết kế HTTT (thêm BPMN, service design), Công nghệ web (chuyển sang xây portal/dashboard/internal app), Khai phá dữ liệu (Analytics & Data Mining), An toàn thông tin, Công nghệ đa phương tiện, Phát triển ứng dụng di động (thành low-code/no-code), Quản trị mạng [28-30].

## 8. Nhóm học phần tự chọn chuyên sâu
Track 1 (Business Intelligence & Data Analytics), Track 2 (AI for Enterprise Systems), Track 3 (Digital Transformation & Product), Track 4 (Platform, Cloud & Security) [30, 31].

## 9. Đề xuất phương pháp giảng dạy mới
Dạy theo studio/project, Tích hợp AI có kiểm soát, Oral defense bắt buộc, Dạy bằng case study [31, 32].

## 10. Đề xuất mô hình đánh giá
20% kiểm tra nền tảng, 25% lab/mini project, 20% báo cáo phân tích, 20% demo sản phẩm, 15% vấn đáp phản biện [33]. Không nên thi viết 100% [33].

## 11. Đề xuất đồ án tốt nghiệp cho ngành HTTT
Yêu cầu 5 thành phần: bài toán tổ chức, phân tích quy trình, thiết kế dữ liệu, triển khai thực nghiệm, đánh giá KPI [33, 34].

## 12. Lộ trình triển khai thực tế cho khoa/trường
Giai đoạn 1 (Rà soát CTĐT), Giai đoạn 2 (Viết lại CLO/PLO), Giai đoạn 3 (Thí điểm 4 học phần mới), Giai đoạn 4 (Bồi dưỡng giảng viên), Giai đoạn 5 (Liên kết doanh nghiệp) [35, 36].

## 13. Kết luận
**HTTT nên được tái định vị thành ngành đào tạo “kiến trúc sư hệ thống số và dữ liệu cho tổ chức trong thời đại AI”.** [36]

---

# PHẦN 3: Đề xuất chương trình đào tạo chi tiết cho ngành Công nghệ thông tin (CNTT)

Dựa trên khung hiện tại trong file đính kèm, AI hiện mới xuất hiện rời rạc thay vì trở thành năng lực lõi bắt buộc xuyên suốt chương trình [37].

## I. Tái định vị ngành CNTT
Ngành CNTT phải tái định vị thành: **AI-native Computer Science & Intelligent Systems Engineering** [38]. Sinh viên CNTT tương lai phải trở thành: system thinker, AI collaborator, platform engineer, infrastructure-aware developer, intelligent system builder, product innovator [38].

## II. Chuẩn đầu ra mới cho ngành CNTT
1. Computer Science Foundations [39]
2. AI-native Development [39]
3. AI/ML Systems [39]
4. Cloud & Infrastructure [39]
5. Security & Reliability [40]
6. Product & Innovation [40]

## III. Cấu trúc CTĐT mới
- **Khối A:** General Education [40]
- **Khối B:** Mathematical & Computational Foundations (Học kỳ 1-2, thêm môn mới Computational Thinking) [40, 41]

## IV. Core Computer Science Layer
Học kỳ 3-4: Thuật toán nâng cao, Kiến trúc máy tính, HĐH, CSDL, Mạng, Software Engineering, Web Systems, Mobile & Cross-platform, API Engineering, System Design Fundamentals [41]. Bỏ các môn quá thiên syntax [41, 42].

## V. AI Core Layer (BẮT BUỘC)
- **Học kỳ 5:** Machine Learning Foundations, Data Engineering, Applied Statistics for AI, Database at Scale [42].
- **Học kỳ 6:** Deep Learning, NLP, Computer Vision, MLOps Foundations [42].
- **Học kỳ 7:** Large Language Models, RAG, AI Agents & Multi-Agent Systems, Responsible AI [42].

## VI. Systems & Infrastructure Layer
Học kỳ 6-7: Cloud Computing, Distributed Systems, DevOps & CI/CD, Containerization, Observability Engineering [42, 43].

## VII. Security Layer
Học kỳ 7: Cybersecurity Foundations, Secure Software Engineering, Privacy Engineering [43].

## VIII. Product Engineering Layer
Học kỳ 7: Product Management for Engineers, Startup Engineering, Human-AI Interaction [43].

## IX. Capstone Layer
Học kỳ 8: Internship, Capstone Project / Thesis [43].

## X. Các học phần cần giữ nguyên nhưng nâng cấp
Cơ sở dữ liệu (thêm NoSQL, vector DB), Mạng máy tính (thêm cloud/edge networking), Công nghệ phần mềm (thêm AI-assisted SDLC), Trí tuệ nhân tạo (Tách thành ML, DL, LMM systems) [43, 44].

## XI. Các môn nên loại bỏ hoặc giảm trọng số
Windows Programming (loại), Java (tự chọn), các môn framework-specific [44].

## XII. Các specialization tracks
Track 1 (AI Systems), Track 2 (Cloud & Distributed Systems), Track 3 (Cybersecurity), Track 4 (Data Systems), Track 5 (Robotics/IoT) [44, 45].

## XIII. Đổi mới phương pháp giảng dạy
Không giao bài kiểu viết website quản lý, thay bằng build production system, deploy thật, benchmark thật, optimize thật [45].

## XIV. Đổi mới đánh giá
Live coding, system design interview, oral defense, AI usage audit, deployment review [45].

## XV. Capstone mới
AI SaaS product, autonomous agent, cloud platform, publishable research, startup prototype [45, 46].

## XVI. Các nghề đầu ra
AI Engineer, Platform Engineer, ML Engineer, Cloud Engineer, Data Engineer... [46].

## XVII. Tại sao CNTT phải thay đổi mạnh hơn HTTT?
Vì CNTT đang bị AI disruption mạnh nhất ở tầng coding [46]. Nếu không thay đổi: sinh viên học 4 năm để cạnh tranh với AI => thất bại [46].

## XVIII. Tầm nhìn mới
Ngành CNTT không nên đào tạo coder mà phải đào tạo: **builders of intelligent systems** [46]. Đây mới là chương trình đủ sức cạnh tranh đến giai đoạn 2030–2035 [46].