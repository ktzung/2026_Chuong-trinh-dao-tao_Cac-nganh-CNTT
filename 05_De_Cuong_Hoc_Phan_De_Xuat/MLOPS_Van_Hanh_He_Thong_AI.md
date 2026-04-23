# MLOPS: Vận hành hệ thống AI & MLOps (AI System Deployment & MLOps)

**Mã học phần đề xuất:** MLOPS  
**Số tín chỉ:** 3 TC (30 tiết lý thuyết + 15 tiết thực hành tích hợp)  
**Học kỳ gợi ý:** Học kỳ 6 (năm 3)  
**Học phần tiên quyết:** WEB-A2, Machine Learning Foundations (hoặc CSE445)  
**Áp dụng cho ngành:** TTNT (bắt buộc), CNTT (bắt buộc), KTPM (khuyến nghị mạnh)  
**Công cụ bắt buộc:** Python, Docker, GitHub Actions, MLflow, tài khoản AWS/GCP (free tier)

---

## I. Mô tả học phần

Khoảng cách lớn nhất giữa sinh viên AI Việt Nam và kỹ sư AI tại doanh nghiệp không phải là kiến thức về thuật toán — mà là khả năng **đưa mô hình AI từ notebook Jupyter ra môi trường production thực tế**. Một mô hình đạt 95% accuracy trong lab nhưng không thể deploy, không có monitoring, không có CI/CD thì không có giá trị kinh doanh.

Học phần này lấp đầy khoảng trống đó. Sinh viên sẽ học cách vận hành toàn bộ vòng đời của một hệ thống AI: từ experiment tracking, model versioning, đến containerization, deployment, monitoring và tự động hóa pipeline.

**Triết lý cốt lõi:** *"Một mô hình AI chưa được deploy là một mô hình chưa tồn tại."*

---

## II. Chuẩn đầu ra

### Kiến thức
- **CĐR 1:** Giải thích sự khác biệt giữa ML Research và ML Engineering — tại sao một mô hình tốt trong notebook có thể thất bại trong production.
- **CĐR 2:** Mô tả các thành phần của một ML pipeline hoàn chỉnh: data ingestion → feature engineering → training → evaluation → deployment → monitoring → retraining.
- **CĐR 3:** Phân tích các chiến lược deployment: batch inference, real-time inference, A/B testing, canary deployment, shadow mode.
- **CĐR 4:** Mô tả các vấn đề đặc thù của hệ thống AI trong production: data drift, concept drift, model degradation, và cách phát hiện sớm.

### Kỹ năng
- **CĐR 5:** Thiết lập experiment tracking với MLflow: log parameters, metrics, artifacts; so sánh và chọn model tốt nhất.
- **CĐR 6:** Container hóa ML model với Docker; viết Dockerfile tối ưu cho Python ML stack.
- **CĐR 7:** Xây dựng REST API serving ML model với FastAPI; xử lý batch và real-time request.
- **CĐR 8:** Thiết lập CI/CD pipeline cho ML: tự động test, build, deploy khi có model mới hoặc code thay đổi.
- **CĐR 9:** Thiết lập monitoring cho hệ thống AI: theo dõi latency, throughput, prediction distribution, data drift alert.
- **CĐR 10:** Triển khai model lên cloud (AWS SageMaker, GCP Vertex AI, hoặc Kubernetes) và cấu hình auto-scaling.

### Thái độ
- **CĐR 11:** Tư duy "production-first": luôn thiết kế model và pipeline với khả năng deploy và maintain trong tâm trí.
- **CĐR 12:** Trách nhiệm với hệ thống AI đang chạy: hiểu rằng model degradation không được phát hiện có thể gây hại thực tế cho người dùng.

---

## III. Nội dung theo tuần

### Giai đoạn 1: Nền tảng MLOps & Experiment Management (tuần 1–4)

**Tuần 1 — Từ Notebook đến Production: khoảng cách và cách vượt qua**
- Nội dung: Tại sao 87% ML project không bao giờ ra production (Gartner). Technical debt trong ML. Sự khác biệt giữa ML Research, ML Engineering và MLOps. Giới thiệu MLOps maturity model (Level 0 → Level 3).
- Thực hành: Nhận một notebook Jupyter "hoạt động tốt" — phân tích tất cả lý do tại sao nó không thể deploy trực tiếp (hardcoded paths, no error handling, no versioning, no monitoring).
- Checkpoint: Viết báo cáo 1 trang: "5 vấn đề của notebook này và cách khắc phục từng vấn đề."

**Tuần 2 — Experiment Tracking với MLflow**
- Nội dung: Tại sao cần experiment tracking (reproducibility, comparison). MLflow architecture: Tracking, Projects, Models, Registry. Log parameters, metrics, artifacts. Model versioning và staging (Staging → Production → Archived).
- Thực hành: Chuyển một training script thông thường sang MLflow-tracked experiment. Chạy 5 experiment với hyperparameter khác nhau, so sánh trên MLflow UI, chọn model tốt nhất và promote lên Production stage.
- Checkpoint: MLflow UI phải hiển thị đầy đủ 5 runs với metrics, parameters và artifacts. Giải thích lý do chọn model.

**Tuần 3 — Data Versioning & Feature Store cơ bản**
- Nội dung: Data versioning với DVC (Data Version Control). Tại sao version data quan trọng không kém version code. Feature Store concept — tại sao các công ty lớn (Uber, Airbnb) xây dựng Feature Store. Feast cơ bản.
- Thực hành: Thiết lập DVC cho một dataset. Thay đổi data preprocessing, tạo version mới, so sánh model performance giữa 2 data versions.
- Checkpoint: Chứng minh có thể reproduce kết quả training từ 2 tuần trước chỉ bằng `dvc checkout` + `mlflow run`.

**Tuần 4 — Model Packaging & Serving API**
- Nội dung: Các format lưu model: pickle, ONNX, TorchScript, SavedModel. Tại sao ONNX quan trọng (interoperability). Xây dựng REST API với FastAPI: request validation (Pydantic), async handling, batch prediction endpoint.
- Thực hành: Đóng gói model từ tuần 2 thành FastAPI service. Viết endpoint `/predict` (single) và `/predict/batch`. Thêm input validation và error handling. Test với Postman.
- Checkpoint: API phải xử lý được: (1) input hợp lệ, (2) input thiếu field, (3) input sai kiểu dữ liệu — mỗi trường hợp trả về response phù hợp.

---

### Giai đoạn 2: Containerization & CI/CD cho ML (tuần 5–9)

**Tuần 5 — Docker cho ML: từ "chạy trên máy tôi" đến "chạy ở mọi nơi"**
- Nội dung: Docker review nhanh (sinh viên đã học ở WEB-A2). Dockerfile tối ưu cho Python ML: multi-stage build, layer caching, minimize image size. Docker Compose cho ML stack (API + database + monitoring).
- Thực hành: Container hóa FastAPI service từ tuần 4. Tối ưu image size từ >2GB xuống <500MB bằng multi-stage build và base image phù hợp.
- Checkpoint: `docker run` phải khởi động service trong <10 giây. Image size phải <600MB.

**Tuần 6 — CI/CD Pipeline cho ML với GitHub Actions**
- Nội dung: CI/CD cho ML khác gì CI/CD cho web app thông thường (data testing, model testing, performance regression). GitHub Actions workflow cho ML: data validation → unit test → model training → model evaluation → deploy nếu performance đạt ngưỡng.
- Thực hành: Thiết lập GitHub Actions pipeline: mỗi khi push code mới, pipeline tự động chạy data tests, train model, so sánh với model hiện tại trong production — chỉ deploy nếu model mới tốt hơn ít nhất 1%.
- Checkpoint: Giới thiệu một thay đổi làm model tệ hơn — pipeline phải block deployment tự động.

**Tuần 7 — Deployment Strategies: từ Big Bang đến Canary**
- Nội dung: Blue-Green deployment. Canary deployment (5% → 20% → 100% traffic). Shadow mode (chạy model mới song song, không ảnh hưởng user). A/B testing cho ML models. Feature flags.
- Thực hành: Triển khai 2 phiên bản model (v1 và v2) với Nginx load balancer. Cấu hình 10% traffic đến v2 (canary). Theo dõi metrics của cả 2 phiên bản.
- Checkpoint: Demo live: thay đổi tỷ lệ traffic từ 10% lên 50% mà không có downtime.

**Tuần 8 — Cloud Deployment: AWS SageMaker / GCP Vertex AI**
- Nội dung: Managed ML platforms vs. self-managed. AWS SageMaker: Training Jobs, Model Registry, Endpoints. GCP Vertex AI: Custom Training, Model Registry, Prediction. Chi phí và khi nào nên dùng managed vs. self-managed.
- Thực hành: Deploy model lên AWS SageMaker Endpoint (hoặc GCP Vertex AI Endpoint). Gọi endpoint từ Python client. Cấu hình auto-scaling dựa trên số request.
- Checkpoint: Endpoint phải trả lời trong <500ms cho 95% request. Tính chi phí vận hành ước tính cho 1.000 request/ngày.

**Tuần 9 — Kubernetes cho ML: khi cần scale lớn**
- Nội dung: Kubernetes review (sinh viên đã học ở Cloud/DevOps). Kubernetes cho ML: resource requests/limits cho GPU workload. Horizontal Pod Autoscaler. Helm charts cho ML services. KServe (Kubernetes-native model serving).
- Thực hành: Deploy ML service lên Kubernetes cluster (minikube local hoặc GKE free tier). Cấu hình HPA để tự động scale khi CPU > 70%.
- Checkpoint: Chạy load test (100 concurrent requests) — Kubernetes phải tự động scale từ 1 pod lên 3 pods.

---

### Giai đoạn 3: Monitoring, Observability & Retraining (tuần 10–13)

**Tuần 10 — Monitoring hệ thống AI: không chỉ là uptime**
- Nội dung: Sự khác biệt giữa monitoring hệ thống thông thường và monitoring AI: cần theo dõi cả system metrics (latency, throughput) lẫn model metrics (prediction distribution, confidence scores). Prometheus + Grafana cho ML. Evidently AI cho model monitoring.
- Thực hành: Thiết lập dashboard Grafana theo dõi: request rate, latency (p50/p95/p99), error rate, prediction distribution theo thời gian.
- Checkpoint: Dashboard phải hiển thị real-time metrics. Giảng viên gây ra spike traffic — dashboard phải phản ánh trong vòng 30 giây.

**Tuần 11 — Data Drift & Concept Drift Detection**
- Nội dung: Data drift là gì (phân phối input thay đổi). Concept drift là gì (mối quan hệ input-output thay đổi). Các phương pháp phát hiện: statistical tests (KS test, PSI), monitoring prediction distribution. Evidently AI reports.
- Thực hành: Mô phỏng data drift bằng cách thay đổi phân phối input data. Thiết lập alert tự động khi drift score vượt ngưỡng.
- Checkpoint: Hệ thống phải tự động gửi alert (email hoặc Slack) khi phát hiện drift — không cần can thiệp thủ công.

**Tuần 12 — Automated Retraining Pipeline**
- Nội dung: Khi nào nên retrain model (scheduled vs. triggered). Continuous Training pipeline. Human-in-the-loop: khi nào cần người review trước khi deploy model mới. Champion-Challenger pattern.
- Thực hành: Xây dựng pipeline tự động: khi drift alert được kích hoạt → tự động trigger retraining job → so sánh model mới với model hiện tại → nếu tốt hơn, tự động deploy (hoặc gửi notification để người review).
- Checkpoint: Demo end-to-end: inject drifted data → alert → retrain → deploy mới — toàn bộ tự động trong <30 phút.

**Tuần 13 — LLMOps: MLOps cho Large Language Models**
- Nội dung: LLMOps khác MLOps truyền thống như thế nào. Prompt versioning và management. Evaluation cho LLM (không có ground truth rõ ràng). Fine-tuning pipeline (LoRA/QLoRA). Cost monitoring cho LLM API calls. LangSmith / Langfuse cho LLM observability.
- Thực hành: Thiết lập LLM observability với Langfuse: log tất cả LLM calls, theo dõi latency, token usage và cost. Tạo evaluation dataset và chạy automated evaluation.
- Checkpoint: Dashboard Langfuse phải hiển thị: tổng token usage, chi phí ước tính, latency distribution, và tỷ lệ response đạt chất lượng.

---

### Giai đoạn 4: Đồ án capstone (tuần 14–15)

**Tuần 14–15 — Đồ án: End-to-End MLOps Pipeline**

Yêu cầu: Mỗi sinh viên (hoặc nhóm 2 người) xây dựng một hệ thống ML hoàn chỉnh với đầy đủ MLOps practices:

**Checklist bắt buộc:**
- [ ] Model được track bằng MLflow (≥3 experiments)
- [ ] Code và data được version control (Git + DVC)
- [ ] Model được serve qua REST API (FastAPI)
- [ ] Toàn bộ stack được container hóa (Docker Compose)
- [ ] CI/CD pipeline tự động (GitHub Actions)
- [ ] Deployed lên cloud (ít nhất PaaS như Railway hoặc Render)
- [ ] Monitoring dashboard (Grafana hoặc tương đương)
- [ ] Drift detection được thiết lập

**Format bảo vệ (20 phút/sinh viên):**
- 5 phút: Demo live hệ thống đang chạy trên cloud.
- 5 phút: Mở CI/CD pipeline, chỉ vào monitoring dashboard.
- 10 phút: Trả lời câu hỏi kỹ thuật.

**Câu hỏi mẫu:**
> *"Model của em đang chạy trên production. Hôm nay data drift alert được kích hoạt. Em sẽ làm gì trong 30 phút tiếp theo?"*  
> *"Chi phí vận hành hệ thống của em mỗi tháng là bao nhiêu? Nếu traffic tăng 10x, chi phí tăng bao nhiêu?"*  
> *"Nếu model mới sau retraining tệ hơn model cũ, hệ thống của em xử lý thế nào?"*

---

## IV. Phương pháp đánh giá

| Thành phần | Trọng số | Mô tả |
|---|---|---|
| Checkpoint hàng tuần (tuần 1–13) | 30% | 13 checkpoint, rubric rõ ràng |
| Bài kiểm tra giữa kỳ (tuần 7) | 20% | Thiết kế deployment strategy cho một hệ thống cho trước — mở tài liệu, mở AI |
| Đồ án — hệ thống hoàn chỉnh | 30% | Đánh giá theo checklist bắt buộc |
| Oral defense | 20% | Trả lời câu hỏi về kiến trúc, chi phí, incident response |

> **Tiêu chí fail tự động:** Hệ thống không có monitoring, hoặc không deployed thực tế, hoặc sinh viên không giải thích được bất kỳ thành phần nào trong pipeline.

---

## V. Tài liệu & công cụ

### Tài liệu bắt buộc đọc
- [Made With ML — MLOps Course](https://madewithml.com) — khóa học MLOps thực tế nhất hiện nay
- [Full Stack Deep Learning](https://fullstackdeeplearning.com) — từ training đến production
- [MLOps Community Best Practices 2025](https://mlops.community)
- [Evidently AI Documentation](https://docs.evidentlyai.com) — data drift monitoring

### Công cụ bắt buộc
- MLflow (experiment tracking)
- DVC (data versioning)
- FastAPI (model serving)
- Docker + Docker Compose
- GitHub Actions (CI/CD)
- Prometheus + Grafana (monitoring)
- Evidently AI (drift detection)
- Langfuse (LLM observability — tuần 13)

### Cloud platforms (free tier)
- AWS Free Tier: SageMaker Studio Lab (miễn phí)
- GCP: Vertex AI Workbench ($300 credit)
- Railway.app: deploy FastAPI service miễn phí

---

## VI. So sánh với chương trình hiện tại

| Nội dung | Chương trình cũ | MLOPS (mới) |
|---|---|---|
| Deployment | Không có | CI/CD pipeline tự động, cloud deployment |
| Model versioning | Không có | MLflow + DVC |
| Monitoring | Không có | Prometheus + Grafana + drift detection |
| Serving | Không có | FastAPI + Docker + Kubernetes |
| LLMOps | Không có | Langfuse, prompt versioning, cost monitoring |

---

*Học phần MLOPS — Khoa CNTT, Trường Đại học Thủy lợi. Phiên bản 1.0 — Tháng 4/2026.*
