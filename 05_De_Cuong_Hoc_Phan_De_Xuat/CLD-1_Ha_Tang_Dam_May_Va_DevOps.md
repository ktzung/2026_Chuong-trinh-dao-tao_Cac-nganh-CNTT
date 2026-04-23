# CLD-1: Hạ tầng đám mây & DevOps (Cloud Infrastructure & DevOps)

**Mã học phần đề xuất:** CLD-1  
**Số tín chỉ:** 3 TC (30 tiết lý thuyết + 15 tiết thực hành tích hợp)  
**Học kỳ gợi ý:** Học kỳ 5 (năm 3)  
**Học phần tiên quyết:** Mạng máy tính (CSE489), Hệ điều hành (CSE482), WEB-A1  
**Áp dụng cho ngành:** CNTT (bắt buộc), KTPM (bắt buộc), HTTT (khuyến nghị mạnh), TTNT (khuyến nghị)  
**Công cụ bắt buộc:** Docker, GitHub Actions, tài khoản AWS Free Tier hoặc GCP Free Tier, Linux terminal

---

## I. Mô tả học phần

Trong kỷ nguyên AI, mọi ứng dụng đều chạy trên cloud. Kỹ sư phần mềm không biết Docker, không biết CI/CD, không biết deploy lên cloud là kỹ sư chưa hoàn chỉnh — dù code có tốt đến đâu. Học phần này trang bị cho sinh viên toàn bộ kỹ năng vận hành hệ thống hiện đại: từ container hóa, tự động hóa triển khai, đến quản lý hạ tầng dưới dạng mã (Infrastructure as Code).

Đây không phải môn học lý thuyết về cloud. Mọi tiết học đều có thực hành trên hệ thống thật, với tài khoản cloud thật, deploy ứng dụng thật.

**Triết lý cốt lõi:** *"Nếu không thể deploy, bạn chưa thực sự xây dựng được gì."*

---

## II. Chuẩn đầu ra

### Kiến thức
- **CĐR 1:** Giải thích các mô hình dịch vụ cloud (IaaS, PaaS, SaaS, FaaS) và khi nào nên dùng mô hình nào dựa trên yêu cầu kỹ thuật và chi phí.
- **CĐR 2:** Mô tả kiến trúc container: sự khác biệt giữa container và VM, Docker image layers, container networking và storage.
- **CĐR 3:** Giải thích các thành phần của CI/CD pipeline và vai trò của từng bước trong việc đảm bảo chất lượng phần mềm.
- **CĐR 4:** Mô tả khái niệm Infrastructure as Code (IaC) và lợi ích so với quản lý hạ tầng thủ công.
- **CĐR 5:** Phân tích các chiến lược deployment (rolling, blue-green, canary) và trade-off của từng chiến lược.

### Kỹ năng
- **CĐR 6:** Viết Dockerfile tối ưu cho ứng dụng web/API; build và push image lên container registry.
- **CĐR 7:** Thiết kế và triển khai multi-container application với Docker Compose.
- **CĐR 8:** Xây dựng CI/CD pipeline hoàn chỉnh với GitHub Actions: test → build → security scan → deploy.
- **CĐR 9:** Triển khai ứng dụng lên cloud (AWS EC2/ECS hoặc GCP Cloud Run) và cấu hình load balancer, auto-scaling.
- **CĐR 10:** Viết Infrastructure as Code cơ bản với Terraform để tạo và quản lý tài nguyên cloud.
- **CĐR 11:** Thiết lập monitoring và alerting cho ứng dụng production: logs, metrics, uptime alerts.

### Thái độ
- **CĐR 12:** Tư duy "infrastructure as code": không bao giờ cấu hình server thủ công qua giao diện — mọi thứ phải được mã hóa và version control.
- **CĐR 13:** Ý thức bảo mật trong DevOps: không commit secrets, không expose port không cần thiết, luôn scan dependencies.

---

## III. Nội dung theo tuần

### Giai đoạn 1: Linux & Container Foundation (tuần 1–4)

**Tuần 1 — Linux cho kỹ sư cloud: những gì thực sự cần biết**
- Nội dung: Linux filesystem hierarchy. Các lệnh thiết yếu: file management, process management, networking (curl, netstat, ss), text processing (grep, awk, sed). Shell scripting cơ bản. SSH và key-based authentication. Systemd và service management.
- Thực hành: Kết nối SSH vào một Linux VM (AWS EC2 free tier hoặc GCP Compute Engine). Thực hiện 20 tác vụ quản trị hệ thống: cài đặt package, cấu hình firewall, xem log, quản lý process.
- Checkpoint: Viết shell script tự động hóa việc cài đặt và cấu hình một web server (Nginx) từ đầu.

**Tuần 2 — Docker: container hóa ứng dụng**
- Nội dung: Container vs. VM — tại sao container thắng. Docker architecture: daemon, client, registry. Dockerfile instructions: FROM, RUN, COPY, WORKDIR, EXPOSE, CMD, ENTRYPOINT. Image layers và caching. Multi-stage builds.
- Thực hành: Container hóa một ứng dụng web (từ WEB-A1 hoặc WEB-A2). Tối ưu Dockerfile: giảm image size, tăng build speed bằng layer caching. Push lên Docker Hub hoặc GitHub Container Registry.
- Checkpoint: Image size phải <200MB cho Node.js app hoặc <300MB cho Python app. Build time phải <60 giây khi không có thay đổi (cache hit).

**Tuần 3 — Docker Compose: multi-container applications**
- Nội dung: Docker Compose file structure. Service dependencies (depends_on, healthcheck). Networking giữa containers. Volume management. Environment variables và secrets management (không hardcode!). Override files cho dev/prod.
- Thực hành: Xây dựng stack hoàn chỉnh với Docker Compose: frontend + backend API + PostgreSQL + Redis cache + Nginx reverse proxy. Toàn bộ stack khởi động bằng một lệnh `docker compose up`.
- Checkpoint: Xóa toàn bộ containers và volumes, chạy lại từ đầu — ứng dụng phải hoạt động hoàn toàn trong <2 phút.

**Tuần 4 — Container Security: những gì AI thường bỏ qua**
- Nội dung: Common container security mistakes: running as root, exposing unnecessary ports, secrets in environment variables, outdated base images. Docker security best practices. Container image scanning với Trivy. Secrets management với Docker secrets hoặc environment files.
- Thực hành: Audit Dockerfile từ tuần 2 — tìm tất cả vấn đề bảo mật. Chạy Trivy scan, fix tất cả critical và high vulnerabilities. Implement proper secrets management.
- Checkpoint: Trivy scan phải trả về 0 critical vulnerabilities. Container không được chạy với root user.

---

### Giai đoạn 2: CI/CD Pipeline (tuần 5–8)

**Tuần 5 — GitHub Actions: tự động hóa mọi thứ**
- Nội dung: GitHub Actions concepts: workflows, jobs, steps, runners. YAML syntax. Triggers: push, pull_request, schedule, manual. Secrets và environment variables trong Actions. Marketplace actions.
- Thực hành: Xây dựng workflow đầu tiên: mỗi khi push code → tự động chạy linting (ESLint/Flake8) và unit tests → báo cáo kết quả trên PR.
- Checkpoint: Tạo PR với code có lỗi lint — workflow phải fail và block merge. Fix lỗi — workflow phải pass.

**Tuần 6 — CI Pipeline hoàn chỉnh: test, build, scan**
- Nội dung: Testing pyramid trong CI: unit → integration → E2E. Test parallelization. Docker build trong CI. Security scanning: Snyk hoặc Trivy trong pipeline. SAST với SonarCloud (free tier). Dependency vulnerability scanning.
- Thực hành: Xây dựng CI pipeline đầy đủ: lint → unit test → integration test → Docker build → Trivy scan → SonarCloud analysis. Pipeline phải chạy trong <5 phút.
- Checkpoint: Giới thiệu một dependency có known vulnerability — pipeline phải detect và fail.

**Tuần 7 — CD Pipeline: tự động deploy**
- Nội dung: Continuous Delivery vs. Continuous Deployment. Environment strategy: dev → staging → production. Deployment gates và approval workflows. Rollback strategy. Deployment notifications (Slack, email).
- Thực hành: Mở rộng CI pipeline thành CD: sau khi CI pass → tự động deploy lên staging → chạy smoke test → nếu pass, deploy lên production (hoặc chờ manual approval).
- Checkpoint: Push code mới → trong vòng 10 phút, ứng dụng phải được deploy lên staging tự động và URL staging phải hoạt động.

**Tuần 8 — GitOps & Infrastructure as Code cơ bản**
- Nội dung: GitOps principles: infrastructure state được lưu trong Git, mọi thay đổi qua Pull Request. Terraform basics: providers, resources, variables, outputs, state. Terraform cho AWS/GCP: tạo EC2/VM, security groups, S3 bucket.
- Thực hành: Viết Terraform code để tạo toàn bộ infrastructure cho ứng dụng: VM, networking, security groups, storage. Destroy và recreate toàn bộ infrastructure bằng một lệnh.
- Checkpoint: `terraform destroy` → `terraform apply` → ứng dụng phải hoạt động trở lại trong <5 phút, không cần can thiệp thủ công.

---

### Giai đoạn 3: Cloud Deployment & Operations (tuần 9–12)

**Tuần 9 — Cloud Fundamentals: AWS hoặc GCP**
- Nội dung: Cloud service categories. Compute: EC2/GCE, ECS/Cloud Run, Lambda/Cloud Functions. Storage: S3/GCS, RDS/Cloud SQL. Networking: VPC, subnets, security groups, load balancers. IAM: users, roles, policies — principle of least privilege.
- Thực hành: Deploy ứng dụng từ tuần 3 lên cloud: EC2 (hoặc GCE) + RDS (hoặc Cloud SQL) + Application Load Balancer. Cấu hình IAM role cho EC2 để access S3 mà không cần hardcode credentials.
- Checkpoint: URL production phải truy cập được từ Internet. Không có AWS credentials nào được hardcode trong code hoặc environment variables của EC2.

**Tuần 10 — Managed Container Services: ECS / Cloud Run**
- Nội dung: Tại sao managed container services tốt hơn tự quản lý Docker trên VM. AWS ECS (Fargate) hoặc GCP Cloud Run: serverless containers. Auto-scaling dựa trên CPU/memory/request count. Cost optimization.
- Thực hành: Migrate ứng dụng từ EC2 sang ECS Fargate hoặc Cloud Run. Cấu hình auto-scaling: scale từ 1 instance lên 5 khi CPU > 70%.
- Checkpoint: Chạy load test (Artillery hoặc k6) — hệ thống phải tự động scale và duy trì response time <500ms.

**Tuần 11 — Monitoring & Observability**
- Nội dung: The three pillars of observability: Logs, Metrics, Traces. CloudWatch (AWS) hoặc Cloud Monitoring (GCP). Structured logging. Custom metrics. Alerting policies. Uptime checks. Cost monitoring — tránh bill shock.
- Thực hành: Thiết lập monitoring hoàn chỉnh: dashboard theo dõi CPU, memory, request rate, error rate, latency. Cấu hình alert: gửi email khi error rate > 5% hoặc latency p95 > 1 giây.
- Checkpoint: Giảng viên gây ra lỗi (kill một service) — sinh viên phải phát hiện qua monitoring trong <3 phút và xác định nguyên nhân.

**Tuần 12 — Cost Optimization & FinOps cơ bản**
- Nội dung: Tại sao cloud bill có thể gây sốc. Các nguyên nhân phổ biến: forgotten resources, over-provisioning, data transfer costs. AWS Cost Explorer / GCP Cost Management. Reserved instances vs. Spot instances. Right-sizing.
- Thực hành: Audit tài khoản cloud của nhóm — tìm tất cả tài nguyên đang chạy không cần thiết. Tính chi phí thực tế của ứng dụng đang deploy. Đề xuất ít nhất 3 cách giảm chi phí.
- Checkpoint: Báo cáo chi phí: chi phí hiện tại, chi phí sau tối ưu, và lý do từng thay đổi.

---

### Giai đoạn 4: Đồ án & bảo vệ (tuần 13–15)

**Tuần 13 — Hoàn thiện đồ án**

Yêu cầu đồ án: Triển khai một ứng dụng web (từ WEB-A1/WEB-A2 hoặc đồ án mới) với đầy đủ DevOps practices:

**Checklist bắt buộc:**
- [ ] Dockerfile tối ưu (multi-stage, non-root user, <300MB)
- [ ] Docker Compose cho local development
- [ ] CI/CD pipeline hoàn chỉnh (GitHub Actions)
- [ ] Security scanning trong pipeline (Trivy hoặc Snyk)
- [ ] Deployed lên cloud (không phải localhost)
- [ ] Infrastructure as Code (Terraform hoặc tương đương)
- [ ] Monitoring dashboard với ít nhất 4 metrics
- [ ] Alerting được cấu hình

**Tuần 14–15 — Demo & Infrastructure Defense**

Format bảo vệ (20 phút/sinh viên):
- **5 phút:** Demo ứng dụng đang chạy trên cloud (mở URL thật).
- **5 phút:** Mở GitHub Actions, chỉ vào pipeline đang chạy; mở monitoring dashboard.
- **10 phút:** Trả lời câu hỏi kỹ thuật.

Câu hỏi mẫu:
> *"Nếu production server bị down lúc 2 giờ sáng, hệ thống monitoring của em có tự động alert không? Em sẽ nhận alert qua kênh nào?"*  
> *"Terraform state file của em đang lưu ở đâu? Nếu lưu local và máy tính hỏng, em có thể recover infrastructure không?"*  
> *"Chi phí cloud của em tháng này là bao nhiêu? Nếu traffic tăng 100x, chi phí tăng bao nhiêu?"*  
> *"Em có thể deploy phiên bản mới mà không có downtime không? Hãy demo."*

---

## IV. Phương pháp đánh giá

| Thành phần | Trọng số | Mô tả |
|---|---|---|
| Checkpoint hàng tuần (tuần 1–12) | 30% | 12 checkpoint, rubric rõ ràng |
| Bài kiểm tra giữa kỳ (tuần 8) | 20% | Viết Terraform code và GitHub Actions workflow cho một hệ thống cho trước — mở tài liệu, mở AI |
| Đồ án — hệ thống hoàn chỉnh | 30% | Đánh giá theo checklist bắt buộc |
| Infrastructure defense | 20% | Trả lời câu hỏi về kiến trúc, chi phí, incident response |

> **Tiêu chí fail tự động:** Ứng dụng không deployed thực tế trên cloud, hoặc không có CI/CD pipeline, hoặc sinh viên không giải thích được bất kỳ thành phần infrastructure nào.

---

## V. Tài liệu & công cụ

### Tài liệu bắt buộc đọc
- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/) — 5 pillars của kiến trúc cloud tốt
- [The Twelve-Factor App](https://12factor.net) — nguyên tắc ứng dụng cloud-native
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Terraform Getting Started](https://developer.hashicorp.com/terraform/tutorials)

### Công cụ bắt buộc
- Docker Desktop
- GitHub + GitHub Actions
- Terraform CLI
- AWS CLI hoặc gcloud CLI
- Trivy (container security scanning)
- Artillery hoặc k6 (load testing)

### Tài khoản cloud (miễn phí)
- AWS Free Tier (12 tháng, EC2 t2.micro, RDS db.t3.micro)
- GCP Free Tier ($300 credit cho sinh viên mới)
- GitHub Student Developer Pack (bao gồm nhiều cloud credits)

---

## VI. So sánh với chương trình hiện tại

| Nội dung | Chương trình cũ (CSE121) | CLD-1 (mới) |
|---|---|---|
| Phạm vi | Lý thuyết cloud + demo | Thực hành end-to-end trên cloud thật |
| CI/CD | Không có | GitHub Actions pipeline hoàn chỉnh |
| Infrastructure as Code | Không có | Terraform cơ bản |
| Security | Không có | Container scanning, IAM, secrets management |
| Monitoring | Không có | CloudWatch/GCP Monitoring + alerting |
| Đánh giá | Bài tập lý thuyết | Infrastructure defense + live demo |

---

*Học phần CLD-1 — Khoa CNTT, Trường Đại học Thủy lợi. Phiên bản 1.0 — Tháng 4/2026.*
