# WEB-A2: Tích hợp AI vào ứng dụng web & triển khai cloud

**Mã học phần đề xuất:** WEB-A2  
**Số tín chỉ:** 3 TC (30 tiết lý thuyết + 15 tiết thực hành tích hợp)  
**Học kỳ gợi ý:** Học kỳ 4 (năm 2)  
**Học phần tiên quyết:** WEB-A1 (Phát triển web hiện đại với AI agent)  
**Áp dụng cho ngành:** KTPM, CNTT, HTTT, TTNT  
**Công cụ bắt buộc:** Cursor IDE, Python/Node.js, Docker, tài khoản AWS/GCP (free tier)

---

## I. Mô tả học phần

Nếu WEB-A1 dạy sinh viên xây dựng ứng dụng web có chất lượng kiến trúc tốt, WEB-A2 dạy sinh viên **nhúng trí tuệ nhân tạo vào trái tim của ứng dụng đó** và **đưa toàn bộ hệ thống lên cloud trong môi trường production thực tế**.

Đây là học phần nơi ranh giới giữa "web developer" và "AI engineer" biến mất. Mọi sinh viên kết thúc học phần này đều có thể xây dựng và vận hành một ứng dụng web có tính năng AI thật sự — không phải demo lab, mà là hệ thống có thể chịu tải người dùng thực.

Triết lý cốt lõi: **"Bất kỳ ứng dụng web nào ra đời sau 2025 mà không có tính năng AI đều đã lỗi thời trước khi ra mắt."**

---

## II. Chuẩn đầu ra

### Kiến thức
- **CĐR 1:** Giải thích kiến trúc của một hệ thống RAG (Retrieval-Augmented Generation): embedding model, vector database, reranker, LLM và cách chúng phối hợp để trả lời câu hỏi dựa trên dữ liệu riêng.
- **CĐR 2:** Mô tả các mô hình tích hợp LLM vào ứng dụng: function calling, tool use, structured output, streaming response.
- **CĐR 3:** Phân tích chi phí vận hành hệ thống AI trên cloud: token cost, compute cost, latency trade-off và chiến lược tối ưu.
- **CĐR 4:** Mô tả các rủi ro bảo mật đặc thù của ứng dụng AI: prompt injection, jailbreak, data leakage qua LLM, và các biện pháp phòng chống.

### Kỹ năng
- **CĐR 5:** Xây dựng pipeline RAG hoàn chỉnh: thu thập tài liệu → chunking → embedding → lưu vào vector database → truy vấn semantic → tích hợp vào API → giao diện chat.
- **CĐR 6:** Tích hợp LLM API (OpenAI, Anthropic, Gemini hoặc mô hình mã nguồn mở qua Ollama) vào ứng dụng web, bao gồm streaming, error handling và fallback strategy.
- **CĐR 7:** Triển khai ứng dụng lên cloud (AWS/GCP/Azure hoặc PaaS như Railway/Fly.io) với Docker, thiết lập CI/CD pipeline tự động (GitHub Actions).
- **CĐR 8:** Thiết lập monitoring và observability cho ứng dụng AI: theo dõi latency, token usage, error rate và chất lượng phản hồi của LLM.
- **CĐR 9:** Thực hiện prompt injection testing và các biện pháp bảo vệ hệ thống AI khỏi bị lạm dụng.

### Thái độ
- **CĐR 10:** Tư duy sản phẩm: luôn đặt câu hỏi "Tính năng AI này có thực sự giúp ích người dùng không?" trước khi xây dựng.
- **CĐR 11:** Trách nhiệm với AI: hiểu rằng mọi hệ thống AI đưa ra phản hồi sai đều có thể gây hại thực tế — phải có cơ chế kiểm tra và fallback.

---

## III. Nội dung theo tuần

### Giai đoạn 1: Tích hợp LLM vào ứng dụng web (tuần 1–5)

**Tuần 1 — LLM API: cách gọi và tại sao phải hiểu cách tính tiền**
- Nội dung: OpenAI API / Gemini API / Anthropic API — cấu trúc request, response, streaming. Token là gì. Cách tính chi phí. Rate limiting và retry strategy.
- Thực hành: Tích hợp LLM API vào backend đã xây từ WEB-A1. Xây dựng endpoint `/api/chat` trả về streaming response.
- Checkpoint: Tính chi phí ước tính nếu 1.000 user/ngày mỗi người hỏi 10 câu. Đề xuất chiến lược caching để giảm chi phí.

**Tuần 2 — Structured output & function calling: LLM như một bộ não có kỷ luật**
- Nội dung: Tại sao plain text output từ LLM không đủ cho production. JSON mode, structured output (Pydantic/Zod). Function calling — cách LLM quyết định gọi công cụ nào.
- Thực hành: Xây dựng chatbot có thể gọi API thời tiết, tra cứu database sản phẩm và đặt lịch hẹn — tất cả thông qua function calling.
- Checkpoint: Demo live — giảng viên chat với chatbot và kiểm tra xem LLM có gọi đúng function không.

**Tuần 3 — RAG phần 1: Embedding và Vector Database**
- Nội dung: Embedding là gì (vector representation của văn bản). Cosine similarity. Các vector database phổ biến: Chroma, Qdrant, Pinecone. Chunking strategy — tại sao chunk size quan trọng.
- Thực hành: Nhập 50 trang tài liệu (PDF hoặc web page) vào vector database. Thực hiện semantic search và so sánh kết quả với keyword search thông thường.
- Checkpoint: Giải thích trước lớp: *"Tại sao tìm kiếm từ khóa 'xe ô tô' lại không tìm thấy đoạn văn nói về 'phương tiện di chuyển 4 bánh'? Và RAG giải quyết điều này như thế nào?"*

**Tuần 4 — RAG phần 2: Pipeline hoàn chỉnh và tối ưu hóa**
- Nội dung: Reranking. Hybrid search (keyword + semantic). Context window management. Hallucination mitigation. Grounding — cách bắt LLM trả lời chỉ dựa trên tài liệu cung cấp.
- Thực hành: Xây dựng hệ thống Q&A dựa trên tài liệu nội bộ (ví dụ: quy định của trường, giáo trình, FAQ). Đánh giá chất lượng câu trả lời bằng cách so sánh với ground truth.
- Checkpoint: "Red team mini" — cố tình đặt câu hỏi bẫy để LLM bịa câu trả lời (hallucinate), ghi lại kết quả và đề xuất cách phòng chống.

**Tuần 5 — AI agent trong ứng dụng web: orchestration đơn giản**
- Nội dung: Khái niệm AI agent trong ứng dụng thực tế (không phải lý thuyết hàn lâm). LangChain / LlamaIndex cơ bản. Multi-step reasoning — khi nào LLM cần nhiều bước để trả lời.
- Thực hành: Xây dựng "research assistant" agent: nhận câu hỏi → tìm kiếm web → đọc trang web → tổng hợp → trả lời với trích dẫn nguồn.
- Checkpoint: Agent phải hoạt động với ít nhất 3 loại câu hỏi khác nhau và trả lời chính xác > 70%.

---

### Giai đoạn 2: Triển khai cloud & vận hành production (tuần 6–10)

**Tuần 6 — Docker và container hóa ứng dụng AI**
- Nội dung: Dockerfile cho ứng dụng Python/Node.js. Docker Compose cho multi-service app. Xử lý secrets trong container (không bao giờ hardcode API key).
- Thực hành: Container hóa toàn bộ stack: frontend + backend + vector database + LLM proxy. Chạy với một lệnh `docker compose up`.
- Checkpoint: Xóa toàn bộ file local, pull lại từ GitHub, chạy lại từ đầu — mọi thứ phải hoạt động.

**Tuần 7 — CI/CD: tự động hóa quy trình triển khai**
- Nội dung: GitHub Actions pipeline: test → build → deploy. Staging vs production environment. Feature flags. Rollback strategy.
- Thực hành: Thiết lập pipeline tự động: mỗi khi push code lên `main`, ứng dụng tự động được test và deploy lên cloud.
- Checkpoint: Giới thiệu bug vào code, merge vào main. CI phải bắt lỗi và ngăn deploy thất bại.

**Tuần 8 — Cloud deployment: từ PaaS đến IaaS**
- Nội dung: So sánh các lựa chọn: Railway, Render, Fly.io (dễ) vs AWS EC2, GCP Cloud Run (nhiều quyền kiểm soát hơn). Load balancer. Auto-scaling cơ bản.
- Thực hành: Deploy ứng dụng lên ít nhất 2 nền tảng khác nhau. Đo latency và chi phí của mỗi nền tảng.
- Checkpoint: URL production phải trả lời trong < 2 giây cho 95% request.

**Tuần 9 — Monitoring & Observability cho ứng dụng AI**
- Nội dung: Logging (structured logs). Metrics (Prometheus/Grafana hoặc cloud-native). Tracing (OpenTelemetry). Alerting. Đặc thù của AI systems: token usage, LLM latency, response quality metrics.
- Thực hành: Thiết lập dashboard monitoring cho ứng dụng: theo dõi số request, latency, token cost và lỗi theo thời gian thực.
- Checkpoint: Giảng viên gây ra tình huống lỗi (kill một service). Sinh viên phải phát hiện ra sự cố qua dashboard trong vòng 5 phút.

**Tuần 10 — Bảo mật ứng dụng AI: prompt injection và LLM-specific risks**
- Nội dung: Prompt injection attack — cách hacker thao túng LLM thông qua user input. Indirect prompt injection. Data leakage qua LLM. Jailbreak. Các biện pháp phòng chống: input validation, output filtering, system prompt hardening.
- Thực hành: "AI Red Team exercise" — nhóm A cố gắng tấn công ứng dụng AI của nhóm B qua prompt injection. Nhóm B vá lỗi.
- Checkpoint: Mỗi nhóm nộp báo cáo: các lỗ hổng đã tìm được và cách khắc phục.

---

### Giai đoạn 3: Đồ án capstone (tuần 11–15)

**Tuần 11 — Định hướng đồ án theo ngành**

Sinh viên chọn đề tài theo ngành, phải đáp ứng 3 tiêu chí bắt buộc:
1. **Deployed trên cloud** — có URL thực tế, không phải localhost.
2. **Ít nhất 1 tính năng AI** — tích hợp LLM hoặc ML model thực thụ, không phải chỉ gọi API đơn giản.
3. **Có monitoring** — dashboard theo dõi hoạt động hệ thống.

**Gợi ý đề tài theo ngành:**

*KTPM:* Hệ thống hỗ trợ lập trình viên: chatbot trả lời câu hỏi về codebase nội bộ (RAG trên tài liệu kỹ thuật), tích hợp GitHub, tự động review PR bằng LLM.

*CNTT:* Hệ thống giám sát hạ tầng thông minh: thu thập log → phân tích bằng LLM → phát hiện bất thường → gửi alert với giải thích nguyên nhân bằng ngôn ngữ tự nhiên.

*HTTT:* Dashboard phân tích dữ liệu doanh nghiệp với "chat with data": người dùng hỏi bằng tiếng Việt, hệ thống tự sinh SQL, truy vấn database và trình bày kết quả qua chart.

*TTNT:* Web app triển khai model machine learning tự huấn luyện: upload dataset → train model qua giao diện web → deploy model → API endpoint phục vụ dự đoán → monitoring độ chính xác theo thời gian.

**Tuần 12–13 — Sprint phát triển đồ án**
- Giảng viên đóng vai "product owner", review tiến độ hàng tuần.
- Sinh viên phải nộp daily log (ghi lại prompt đã dùng, quyết định kỹ thuật và lý do, vấn đề gặp phải).

**Tuần 14–15 — Demo và oral defense**

Format bảo vệ (20 phút/sinh viên):
- **3 phút:** Giới thiệu vấn đề và giải pháp (không đọc slide).
- **7 phút:** Live demo — mở URL production, thao tác thực tế trước hội đồng.
- **10 phút:** Trả lời câu hỏi kỹ thuật chuyên sâu.

Câu hỏi mẫu:
> *"Hệ thống RAG của em có vấn đề gì về latency khi tài liệu tăng lên 10.000 trang? Em sẽ giải quyết thế nào?"*  
> *"Nếu OpenAI tăng giá API gấp 10 lần, em có phương án thay thế không?"*  
> *"Một người dùng cố tình prompt injection vào chatbot của em — em đã bảo vệ hệ thống thế nào?"*  
> *"Chi phí vận hành hệ thống của em mỗi tháng là bao nhiêu? Em có thể tối ưu thêm không?"*

---

## IV. Phương pháp đánh giá

| Thành phần | Trọng số | Mô tả |
|---|---|---|
| Checkpoint hàng tuần (tuần 1–10) | 20% | 10 checkpoint, mỗi cái 2 điểm |
| Bài tập giữa kỳ — AI Red Team | 15% | Tìm và báo cáo lỗ hổng prompt injection, kèm bản vá |
| Đồ án — demo live | 25% | Hệ thống phải chạy được, có AI thực sự, có monitoring |
| Đồ án — nhật ký phát triển | 10% | Prompt log, decision log, ghi lại quá trình tư duy |
| Oral defense | 30% | Trả lời câu hỏi về kiến trúc AI, chi phí, bảo mật và khả năng mở rộng |

> **Tiêu chí fail tự động (điểm 0 đồ án):**
> - Ứng dụng không truy cập được qua URL (không deploy thực sự).
> - Không có tính năng AI thật sự (gọi API đơn giản không phải AI-native).
> - Sinh viên không giải thích được kiến trúc của hệ thống của mình trong oral defense.

---

## V. Tài liệu & công cụ bắt buộc

### LLM APIs (chọn ít nhất một)
- **OpenAI API** — GPT-4o, text-embedding-3-small
- **Google Gemini API** — miễn phí cho sinh viên qua Google Cloud Education
- **Anthropic Claude API** — Claude 3.5 Sonnet
- **Ollama (local)** — Llama 3, Mistral — miễn phí, chạy offline

### Vector Databases
- **ChromaDB** — đơn giản nhất, chạy local
- **Qdrant** — có cloud free tier
- **pgvector** — nếu đã dùng PostgreSQL

### Frameworks
- **LangChain / LlamaIndex** — cho RAG pipeline
- **FastAPI** — backend Python
- **Next.js** — frontend (dùng AI để tạo, không code tay)

### Cloud Platforms (cần tài khoản free tier)
- AWS Free Tier (12 tháng đầu miễn phí)
- Google Cloud Free Tier ($300 credit cho sinh viên)
- Railway.app (có free tier cho sinh viên)

### Tài liệu bắt buộc đọc trước kỳ học
- [OpenAI Cookbook](https://cookbook.openai.com) — các pattern tích hợp LLM thực tế
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [12-Factor App](https://12factor.net) — nguyên tắc vận hành ứng dụng cloud-native

---

## VI. Phân biệt ứng dụng theo ngành

| Ngành | Trọng tâm đặc thù trong WEB-A2 |
|---|---|
| **KTPM** | RAG trên codebase nội bộ, AI-assisted code review, tích hợp với GitHub workflow |
| **CNTT** | AI trong monitoring & operations: log analysis, anomaly detection, automated alerting |
| **HTTT** | "Chat with data" — Text-to-SQL, data visualization thông minh, business intelligence tự động |
| **TTNT** | ML model serving qua API, A/B testing giữa các model, model performance monitoring |

---

## VII. Mối liên hệ với các học phần khác

```
WEB-A1 ──────────────────────────── WEB-A2
(Kiến trúc & AI agent cơ bản)       (LLM integration & Cloud ops)
         ↕                                    ↕
   Cloud Computing              MLOps & AI System Deployment
   (CSE121 nâng cấp)           (Học phần mới, năm 3)
```

Sinh viên hoàn thành cả WEB-A1 và WEB-A2 sẽ có đủ nền tảng để học các học phần chuyên sâu năm 3: **MLOps**, **Distributed Systems**, **AI Security** và **Advanced Data Engineering**.

---

*Học phần WEB-A2 — Khoa CNTT, Trường Đại học Thủy lợi. Phiên bản 1.0 — Tháng 4/2026.*
