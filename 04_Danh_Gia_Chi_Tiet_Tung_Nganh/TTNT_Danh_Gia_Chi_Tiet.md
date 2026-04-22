# BÁO CÁO RÀ SOÁT VÀ ĐỀ XUẤT NÂNG CẤP CHƯƠNG TRÌNH ĐÀO TẠO
## NGÀNH TRÍ TUỆ NHÂN TẠO VÀ KHOA HỌC DỮ LIỆU (TTNT) — Tầm nhìn 2026–2030

> **Kính gửi:** Hội đồng Khoa học & Đào tạo Khoa CNTT
> **Người thực hiện:** Tổ Rà soát Chương trình
> **Thời gian:** Tháng 4/2026

---

## I. TÓM TẮT ĐỀ XUẤT

Ngành TTNT hiện mang nặng tư duy **"AI Research"**: dạy sinh viên tự xây dựng thuật toán từ con số 0, tự huấn luyện mô hình từ đầu bằng toán học, nghiên cứu lý thuyết hàn lâm sâu. Đây là hướng đào tạo phù hợp với mục tiêu **tạo ra nhà khoa học AI** — nhưng không phù hợp với nhu cầu thực tế của 95% doanh nghiệp Việt Nam.

Thực tế hiện nay: OpenAI, Google DeepMind, Meta FAIR đã giải quyết bài toán Foundation Models. Không một công ty Việt Nam nào có tài nguyên tự train một mô hình LLM từ đầu. Điều họ cần là **AI Engineers** — những người biết cách lấy một LLM sẵn có (GPT-4o, Claude, Llama 3), tinh chỉnh nó, nhúng nó vào sản phẩm, triển khai và vận hành nó trong môi trường Production.

Đề xuất tái định vị TTNT thành **"Applied AI Engineering & Data Science"**: giữ nền tảng toán học vững nhưng tập trung năng lượng vào **sản phẩm hóa AI**, **LLMOps**, và **hệ thống AI tự trị (Agentic AI)**.

---

## II. CHẨN ĐOÁN CHƯƠNG TRÌNH HIỆN TẠI

### Điểm mạnh cần bảo tồn
- Nền tảng toán học mạnh (Xác suất, Đại số TT, Giải tích) — thiết yếu cho AI Engineer.
- Có các môn thực sự tiên tiến: AI Tạo sinh & LLMs (CSE134), Hệ thống tác tử (CSE107), RL (CSE470) — **đây là điểm sáng nhất của toàn bộ 5 ngành**.
- Có Đồ án chuyên ngành (CSE398) — cần đổi mới yêu cầu để phản ánh thực tiễn.

### Điểm yếu nghiêm trọng
1. **Thiếu MLOps/LLMOps hoàn toàn:** Biết train model nhưng không biết deploy — giống như kỹ sư biết thiết kế xe nhưng không biết đăng kiểm và đưa ra đường.
2. **Không có Data Engineering:** Pipeline dữ liệu là xương sống của mọi hệ thống AI thực tế.
3. **Fine-tuning Foundation Models thiếu vắng:** Kỹ năng hot nhất thị trường (LoRA, QLoRA fine-tuning Llama/Mistral) chưa có trong chương trình.
4. **Thiếu Product Thinking:** Sinh viên không được học cách biến một model AI thành sản phẩm sinh lời.
5. **Đồ án vẫn mang tính nghiên cứu:** Đề tài kiểu "Nghiên cứu thuật toán X" không phản ánh kỹ năng công nghiệp.

---

## III. PHÂN TÍCH RỦI RO AI — TỪNG HỌC PHẦN

| Học phần | Mã HP | TC | Rủi ro AI | Quyết định đề xuất |
|----------|-------|----|-----------|-------------------|
| Nhập môn lập trình | CSE111 | 3 | 🟡 Trung bình | Giữ — học Python ngay, không C/C++ |
| Lập trình nâng cao | CSE205 | 3 | 🟡 Trung bình | Giữ — tập trung Python advanced (iterators, async, type hints) |
| Toán rời rạc | CSE203 | 3 | 🟢 Thấp | Giữ nguyên |
| CTDL & Giải thuật | CSE281 | 3 | 🟢 Thấp | Giữ — thêm Graph algorithms cho AI |
| Kiến trúc máy tính | CSE370 | 3 | 🟡 Trung bình | Giữ — thêm GPU Architecture, CUDA cơ bản |
| Cơ sở dữ liệu | CSE484 | 3 | 🟡 Trung bình | Giữ — thêm Vector Database |
| Mạng máy tính | CSE489 | 3 | 🟡 Trung bình | Giảm xuống 2 TC hoặc gộp — TTNT không cần quá sâu |
| Lập trình hướng đối tượng | CSE116 | 3 | 🟡 Trung bình | Giữ — học qua Python OOP |
| Hệ điều hành | CSE482 | 3 | 🟢 Thấp | Giữ ở mức nhẹ — chú trọng Linux & CLI |
| Phát triển UD Web cơ bản | CSE122 | 3 | 🔴 **Cao** | **LOẠI BỎ** — không liên quan đến định hướng ngành |
| Điện toán đám mây | CSE121 | 3 | 🟢 Thấp | **Nâng thành BẮT BUỘC** — Cloud là môi trường deploy AI |
| Phân tích dữ liệu | CSE131 | 3 | 🟡 Trung bình | Giữ — tăng cường Python Data Stack |
| Trí tuệ nhân tạo | CSE492 | 3 | 🟡 Trung bình | **Thay bằng** AI Foundations toàn diện hơn |
| Phân tích & thiết kế HT | CSE123 | 3 | 🟡 Trung bình | Giảm TC — TTNT cần ít hơn về phân tích hệ thống truyền thống |
| Công nghệ phần mềm | CSE481 | 3 | 🔴 **Cao** | **Gộp với Thiết kế hệ thống ML** — không cần toàn bộ SDLC cổ điển |
| Trực quan hóa dữ liệu | CSE396 | 3 | 🟡 Trung bình | Giữ — rất quan trọng để giao tiếp với stakeholders |
| Học máy | CSE445 | 3 | 🟢 Thấp | Giữ — tăng độ sâu, thêm Bayesian ML |
| Xử lý ảnh | CSE456 | 3 | 🟢 Thấp | Giữ — nâng cấp sang Vision Transformer |
| Chuyên đề TTNT | CSE433 | 2 | 🟡 Trung bình | **Mở rộng thành 3 TC** — cập nhật chủ đề AI tạo sinh |
| Học sâu & ứng dụng | CSE429 | 3 | 🟢 Thấp | Giữ — thêm Transformer Architecture sâu |
| Phân tích chuỗi thời gian | CSE399 | 3 | 🟢 Thấp | Giữ — thêm Temporal Fusion Transformer |
| Phân tích dữ liệu lớn | CSE406 | 3 | 🟢 Thấp | Giữ — thêm Distributed ML (Spark MLlib) |
| Thị giác máy tính | CSE132 | 3 | 🟢 Thấp | Giữ — thêm Vision Language Models |
| Học tăng cường | CSE470 | 3 | 🟢 Thấp | Giữ — **rất chiến lược** cho AI Agent |
| Xử lý âm thanh & tiếng nói | CSE457 | 3 | 🟢 Thấp | Giữ — thêm Speech LLM (Whisper, TTS) |
| Xử lý ngôn ngữ tự nhiên | CSE458 | 3 | 🟢 Thấp | Giữ — thêm LLM internals |
| Thiết kế hệ thống học máy | CSE135 | 3 | 🟢 Thấp | Giữ — **rất quan trọng** cho ML Engineering |
| Đồ án môn học | CSE398 | 3 | 🟡 Trung bình | **Đổi yêu cầu** — phải build AI product thực tế |
| **Hệ thống tác tử thông minh** | CSE107 | 3 | 🟢 Thấp | **MỞ RỘNG THÀNH BẮT BUỘC** — cực kỳ quan trọng |
| **AI tạo sinh & LLMs** | CSE134 | 3 | 🟢 Thấp | **NÂNG THÀNH BẮT BUỘC** — đây là tương lai |

---

## IV. HỌC PHẦN ĐỀ XUẤT LOẠI BỎ — LUẬN GIẢI

### 4.1. Phát triển ứng dụng Web cơ bản (CSE122 — 3 TC) → LOẠI BỎ HOÀN TOÀN

**Luận cứ:**
- Ngành TTNT không nên dành 45 tiết dạy HTML/CSS/JS. Đây là kỹ năng của KTPM.
- Sinh viên TTNT khi cần build UI có thể dùng Streamlit, Gradio, hoặc FastAPI + AI-generated frontend — các công cụ chuyên biệt cho Data Scientists/ML Engineers.
- 3 tín chỉ này được phân bổ lại cho **"MLOps & AI System Deployment"** — kỹ năng cực kỳ thiếu hụt trên thị trường.

### 4.2. Công nghệ phần mềm (CSE481 — 3 TC toàn bộ) → GỘP VÀO MÔN KHÁC

**Luận cứ:**
- Vòng đời phát triển phần mềm cổ điển (Waterfall, Scrum đơn thuần) không phải trọng tâm của ngành AI.
- ML Engineer cần biết phiên bản dành cho AI: Experiment Tracking, Model Versioning (MLflow, DVC), Model Registry — không phải Gantt Chart và Burndown.
- Gộp nội dung quan trọng của CNPM vào môn **"Thiết kế Hệ thống Học máy"** vốn đã có.

---

## V. ĐỀ XUẤT CHƯƠNG TRÌNH ĐÀO TẠO MỚI (THAM KHẢO — 140 TC)

### KHỐI I: GIÁO DỤC ĐẠI CƯƠNG (37 TC — GIỮ NGUYÊN)

*(Toán học, Tiếng Anh, Lý luận chính trị giữ nguyên. Đặc biệt: Xác suất Thống kê và Đại số Tuyến tính phải được dạy với ứng dụng trực tiếp vào ML — không thuần lý thuyết.)*

---

### KHỐI II: NỀN TẢNG KHOA HỌC MÁY TÍNH & DỮ LIỆU (24 TC)

| TT | Học phần | TC | HK | Ghi chú thay đổi |
|----|----------|----|----|-----------------|
| 1 | Lập trình Python chuyên sâu | 3 | 1 | Python từ HK1, học Python idioms, async, type hints |
| 2 | CTDL & Giải thuật (cho AI) | 3 | 2 | Thêm Graph algorithms, Hash Maps ứng dụng trong ML |
| 3 | Cơ sở dữ liệu & Vector Database | 3 | 2 | SQL + MongoDB + Pinecone/Chroma — chuẩn bị cho RAG |
| 4 | Kiến trúc máy tính & GPU Programming | 3 | 2 | Thêm GPU Architecture, CUDA cơ bản, Cloud GPU |
| 5 | Xác suất thống kê ứng dụng ML | 3 | 2 | Bayesian, Hypothesis Testing, Statistical ML |
| 6 | Đại số tuyến tính ứng dụng AI | 3 | 3 | Liên kết trực tiếp: SVD, PCA, Matrix Factorization trong ML |
| 7 | Trực quan hóa dữ liệu | 3 | 3 | Matplotlib, Plotly, Tableau, Storytelling with Data |
| 8 | Linux & Cloud Computing cho AI | 3 | 3 | Linux CLI, Docker, Cloud GPU (GCP Colab Pro, AWS Sagemaker) |

---

### KHỐI III: LÕI MACHINE LEARNING & AI ENGINEERING (27 TC — BẮT BUỘC)

| TT | Học phần | TC | HK | Ghi chú thay đổi |
|----|----------|----|----|-----------------|
| 9 | Machine Learning Foundations | 3 | 3 | Supervised/Unsupervised, Ensemble, Evaluation, Bias-Variance |
| 10 | Deep Learning & Neural Architecture | 3 | 4 | CNN, RNN, Attention, Transformer — với PyTorch |
| 11 | Xử lý ngôn ngữ tự nhiên | 3 | 4 | Từ Tokenization → BERT → LLM overview |
| 12 | Thị giác máy tính | 3 | 4 | Object Detection, Segmentation, Vision Transformer |
| 13 | **LLM Engineering & Generative AI** | 3 | 5 | **BẮT BUỘC** — RAG, Fine-tuning (LoRA/QLoRA), Evaluation |
| 14 | **Hệ thống tác tử thông minh** | 3 | 5 | **BẮT BUỘC** — LangGraph, AutoGen, Tool calling, Memory |
| 15 | Thiết kế hệ thống học máy | 3 | 5 | ML System Design: Scale, Latency, Data freshness, A/B Testing |
| 16 | **MLOps & AI System Deployment** | 3 | 6 | **Môn mới BẮT BUỘC** — MLflow, BentoML, K8s, Monitoring |
| 17 | Phân tích dữ liệu lớn | 3 | 5 | Spark, Distributed ML, Delta Lake |

---

### KHỐI IV: CHUYÊN SÂU — TỰ CHỌN (15 TC, chọn 1 track)

**Track A — Agentic AI & LLMs:**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 18 | Học tăng cường & ứng dụng | 3 | 6 |
| 19 | Multi-Modal AI Systems | 3 | 6 |
| 20 | AI Safety & Alignment | 3 | 6 |
| 21 | LLMOps & Foundation Model Serving | 3 | 7 |
| 22 | AI Product Engineering | 3 | 7 |

**Track B — Data Science & Analytics:**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 18 | Phân tích chuỗi thời gian | 3 | 6 |
| 19 | Hệ khuyến nghị | 3 | 6 |
| 20 | Khai phá dữ liệu nâng cao | 3 | 6 |
| 21 | Kho dữ liệu & Data Engineering | 3 | 7 |
| 22 | Quản trị dữ liệu & AI Governance | 3 | 7 |

**Track C — Perception & Robotics:**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 18 | Xử lý âm thanh & tiếng nói | 3 | 6 |
| 19 | Điều tra số & Forensics AI | 3 | 6 |
| 20 | Robotics & Embodied AI | 3 | 6 |
| 21 | Edge AI & IoT Intelligence | 3 | 7 |
| 22 | Đồ án Nghiên cứu / Kaggle Competition | 3 | 7 |

---

### KHỐI V: THỰC TẬP & ĐỒ ÁN (14 TC)

| TT | Học phần | TC | HK | Yêu cầu mới |
|----|----------|----|----|------------|
| 23 | Thực tập doanh nghiệp | 4 | 8 | SV phải làm việc trong môi trường ML/AI thực tế; báo cáo experiment results |
| 24 | Đồ án tốt nghiệp | 10 | 8 | Bắt buộc: AI Product (hoặc Kaggle top 20% / bài báo conference) + System Design + Deployment Demo + Oral Defense |

---

## VI. ĐỔI MỚI PHƯƠNG PHÁP ĐÁNH GIÁ

| Loại môn | Phương pháp kiểm tra mới |
|----------|------------------------|
| Môn ML/DL | Nộp Jupyter Notebook với experiment results thật + giải thích quyết định mô hình |
| Môn AI Engineering | Demo product chạy thật (Chatbot RAG, Agent) + Oral Defense về kiến trúc hệ thống |
| Môn MLOps | Nộp deployment pipeline chạy trên Cloud miễn phí; GV đánh giá monitoring setup |
| Đồ án | Hội đồng 3 người gồm GV + đại diện doanh nghiệp; chấm theo: Innovation + Impact + Engineering Quality |

---

## VII. ĐỊNH HƯỚNG NGHỀ NGHIỆP ĐẦU RA (2030)

| Vị trí | Kỹ năng cốt lõi từ CTĐT mới |
|--------|-----------------------------|
| AI Engineer / ML Engineer | LLM Integration, RAG, MLOps, Cloud Deployment |
| LLMOps Engineer | Model serving, Monitoring, Fine-tuning pipelines |
| AI Product Engineer | Biến model thành SaaS, Product thinking |
| Data Scientist | Advanced analytics, Time Series, Recommendation |
| Research Engineer | Fine-tuning, Alignment, Multi-modal AI |

---

## VIII. KẾT LUẬN VÀ KIẾN NGHỊ

Ngành TTNT đang có vị thế tốt nhất trong tất cả 5 ngành — vì AI đang ngày càng cần những người **hiểu AI từ bên trong**. Nhưng cần sự dịch chuyển mạnh từ "nghiên cứu" sang "kỹ thuật": không chỉ biết train model, mà phải biết deploy, monitor, và scale.

**Kiến nghị cụ thể:**
1. **Loại bỏ** Phát triển ứng dụng Web cơ bản (CSE122) và Công nghệ phần mềm (CSE481) truyền thống.
2. **Nâng thành bắt buộc:** AI tạo sinh & LLMs (CSE134), Hệ thống tác tử thông minh (CSE107).
3. **Bổ sung môn mới bắt buộc:** MLOps & AI System Deployment (LLMOps, model monitoring).
4. **Đổi yêu cầu đồ án:** Bắt buộc phải có AI Product hoặc bài báo khoa học — không chấp nhận đồ án "nghiên cứu thuật toán X" thuần lý thuyết.
5. Học **Python từ HK1** thay vì C/C++ — Python là ngôn ngữ đặc thù của ngành AI.

---
*Tài liệu tham khảo: Stanford CS229/CS224N/CS231N Course Materials; fast.ai Practical Deep Learning; Hugging Face Course; MLOps Community Best Practices 2025; AI Engineer Foundation Roadmap 2025.*
