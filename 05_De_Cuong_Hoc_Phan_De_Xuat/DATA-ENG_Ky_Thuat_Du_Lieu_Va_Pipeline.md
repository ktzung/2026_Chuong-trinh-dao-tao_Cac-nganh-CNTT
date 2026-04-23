# DATA-ENG: Kỹ thuật dữ liệu & Pipeline (Data Engineering & ETL Pipeline)

**Mã học phần đề xuất:** DATA-ENG  
**Số tín chỉ:** 3 TC (30 tiết lý thuyết + 15 tiết thực hành tích hợp)  
**Học kỳ gợi ý:** Học kỳ 5 (năm 3)  
**Học phần tiên quyết:** Cơ sở dữ liệu (CSE484), Phân tích dữ liệu (CSE131), WEB-A1  
**Áp dụng cho ngành:** HTTT (bắt buộc), TTNT (khuyến nghị mạnh), CNTT (tự chọn)  
**Công cụ bắt buộc:** Python, Apache Airflow, dbt, PostgreSQL, tài khoản GCP/AWS (free tier)

---

## I. Mô tả học phần

Dữ liệu là nhiên liệu của AI. Nhưng dữ liệu thô từ thực tế — lộn xộn, thiếu nhất quán, phân tán ở nhiều nguồn — không thể đưa thẳng vào mô hình AI hay dashboard phân tích. Cần có **Data Engineer** để xây dựng pipeline tự động: thu thập, làm sạch, biến đổi và cung cấp dữ liệu sạch đúng lúc, đúng chỗ.

Học phần này dạy sinh viên xây dựng pipeline dữ liệu từ đầu đến cuối: từ ingestion (thu thập từ nhiều nguồn), transformation (làm sạch và biến đổi), đến loading (đưa vào data warehouse hoặc feature store cho AI). Đây là kỹ năng được tuyển dụng nhiều thứ 7 trên thị trường CNTT Việt Nam Q1/2026 và tăng trưởng 29% YoY.

**Triết lý cốt lõi:** *"Garbage in, garbage out — một mô hình AI tốt trên dữ liệu xấu vẫn cho kết quả xấu."*

---

## II. Chuẩn đầu ra

### Kiến thức
- **CĐR 1:** Giải thích sự khác biệt giữa OLTP (transaction processing) và OLAP (analytical processing), và tại sao cần tách biệt hai hệ thống này.
- **CĐR 2:** Mô tả các kiến trúc data pipeline: ETL (Extract-Transform-Load) vs. ELT (Extract-Load-Transform), batch vs. streaming, Lambda architecture vs. Kappa architecture.
- **CĐR 3:** Phân tích các mô hình thiết kế data warehouse: Star Schema, Snowflake Schema, Data Vault — và khi nào dùng mô hình nào.
- **CĐR 4:** Mô tả các thách thức của data quality: missing values, duplicates, schema drift, late-arriving data — và chiến lược xử lý từng loại.

### Kỹ năng
- **CĐR 5:** Xây dựng pipeline ETL/ELT với Python: kết nối nhiều nguồn dữ liệu (REST API, database, CSV, JSON), transform và load vào data warehouse.
- **CĐR 6:** Thiết kế và triển khai data warehouse schema (Star Schema) trên PostgreSQL hoặc BigQuery.
- **CĐR 7:** Sử dụng dbt (data build tool) để viết transformation logic dưới dạng SQL models có version control và testing.
- **CĐR 8:** Orchestrate pipeline với Apache Airflow: viết DAG, cấu hình dependencies, xử lý failure và retry.
- **CĐR 9:** Thiết lập data quality checks tự động: schema validation, null checks, referential integrity, statistical anomaly detection.
- **CĐR 10:** Xây dựng pipeline cơ bản cho AI/ML: feature engineering, feature store cơ bản, cung cấp dữ liệu cho model training.

### Thái độ
- **CĐR 11:** Tư duy "data as a product": dữ liệu không phải là byproduct — nó là sản phẩm cần được thiết kế, maintain và đảm bảo chất lượng.
- **CĐR 12:** Ý thức về data governance: hiểu tầm quan trọng của data lineage, data catalog, và quyền truy cập dữ liệu.

---

## III. Nội dung theo tuần

### Giai đoạn 1: Nền tảng Data Engineering (tuần 1–4)

**Tuần 1 — Tại sao Data Engineering tồn tại: từ Excel đến Data Platform**
- Nội dung: Hành trình của dữ liệu trong doanh nghiệp: từ transaction systems (ERP, CRM, app logs) đến analytics. Tại sao không thể query trực tiếp production database cho analytics. Data Engineer vs. Data Analyst vs. Data Scientist — ai làm gì. Modern Data Stack overview.
- Thực hành: Phân tích một case study thực tế: một công ty e-commerce có 5 nguồn dữ liệu khác nhau (MySQL orders, MongoDB products, Kafka events, Google Analytics, Salesforce CRM). Vẽ sơ đồ kiến trúc data platform phù hợp.
- Checkpoint: Giải thích tại sao không thể dùng một câu SQL JOIN để lấy dữ liệu từ 5 nguồn trên và trả lời trong <1 giây.

**Tuần 2 — Python cho Data Engineering**
- Nội dung: Python data engineering stack: pandas (data manipulation), SQLAlchemy (database connection), requests (API calls), pydantic (data validation), pyarrow (columnar data). File formats: CSV, JSON, Parquet, Avro — khi nào dùng gì. Xử lý dữ liệu lớn hơn RAM với chunking.
- Thực hành: Viết Python script kết nối đến 3 nguồn dữ liệu khác nhau (REST API, PostgreSQL, CSV file), extract dữ liệu, validate schema với Pydantic, và load vào một database tổng hợp.
- Checkpoint: Script phải xử lý được file CSV 1GB mà không bị OOM (out of memory) — dùng chunking.

**Tuần 3 — Data Warehouse Design: Star Schema & Dimensional Modeling**
- Nội dung: OLAP vs. OLTP. Dimensional modeling: Facts và Dimensions. Star Schema vs. Snowflake Schema. Slowly Changing Dimensions (SCD Type 1, 2, 3). Surrogate keys. Date dimension — tại sao mọi data warehouse đều có.
- Thực hành: Thiết kế Star Schema cho một hệ thống bán hàng: fact_orders, dim_customer, dim_product, dim_date, dim_location. Implement trên PostgreSQL. Load sample data và viết 5 analytical queries.
- Checkpoint: Các analytical queries phải chạy trong <1 giây trên 1 triệu rows — cần proper indexing.

**Tuần 4 — dbt: SQL Transformation với Software Engineering Practices**
- Nội dung: dbt (data build tool) là gì và tại sao nó thay đổi cách viết transformation. dbt models: staging → intermediate → marts. dbt tests: not_null, unique, accepted_values, relationships. dbt documentation tự động. dbt lineage graph.
- Thực hành: Chuyển toàn bộ transformation logic từ tuần 3 sang dbt models. Viết dbt tests cho mọi model. Generate documentation và lineage graph.
- Checkpoint: `dbt test` phải pass 100%. Lineage graph phải hiển thị rõ ràng data flow từ raw → staging → marts.

---

### Giai đoạn 2: Pipeline Orchestration & Data Quality (tuần 5–9)

**Tuần 5 — Apache Airflow: Orchestrating Data Pipelines**
- Nội dung: Airflow concepts: DAG, Task, Operator, Sensor, Hook. DAG design principles: idempotency, atomicity. Scheduling: cron expressions. XCom cho task communication. Airflow UI: monitoring, triggering, debugging.
- Thực hành: Viết Airflow DAG orchestrate toàn bộ pipeline từ tuần 2–4: extract từ 3 nguồn → transform với dbt → load vào data warehouse. DAG chạy tự động mỗi ngày lúc 2 giờ sáng.
- Checkpoint: DAG phải xử lý được failure: nếu một task fail, Airflow phải retry 3 lần và gửi alert email.

**Tuần 6 — Data Quality & Testing**
- Nội dung: Data quality dimensions: Completeness, Accuracy, Consistency, Timeliness, Uniqueness. Great Expectations framework. Schema validation. Statistical anomaly detection (Z-score, IQR). Data contracts. Alerting khi data quality drop.
- Thực hành: Implement data quality checks với Great Expectations cho pipeline từ tuần 5. Cố tình inject bad data — hệ thống phải detect và block pipeline.
- Checkpoint: Inject 5 loại data quality issues khác nhau — hệ thống phải detect ít nhất 4/5.

**Tuần 7 — Incremental Loading & Change Data Capture**
- Nội dung: Full load vs. Incremental load — tại sao không thể full load mỗi ngày khi data lớn. Watermark-based incremental loading. Change Data Capture (CDC) với Debezium. Upsert patterns. Handling late-arriving data.
- Thực hành: Chuyển pipeline từ full load sang incremental load. Implement CDC từ PostgreSQL source database. Xử lý trường hợp record bị update và delete.
- Checkpoint: Pipeline incremental phải chạy nhanh hơn 10x so với full load trên cùng dataset.

**Tuần 8 — Cloud Data Warehouse: BigQuery / Snowflake**
- Nội dung: Cloud DW vs. on-premise: tại sao cloud DW thắng. BigQuery architecture: columnar storage, serverless, separation of compute and storage. Snowflake: virtual warehouses, time travel, data sharing. Cost model: pay-per-query vs. pay-per-compute. Partitioning và clustering để tối ưu chi phí.
- Thực hành: Migrate data warehouse từ PostgreSQL lên BigQuery (hoặc Snowflake free trial). Tối ưu queries bằng partitioning và clustering. So sánh chi phí query trước và sau tối ưu.
- Checkpoint: Tính chi phí query cho 1TB data scan. Sau khi partition, chi phí phải giảm ít nhất 80%.

**Tuần 9 — Real-time Data Processing cơ bản**
- Nội dung: Batch vs. Streaming — khi nào cần real-time. Apache Kafka cơ bản: topics, producers, consumers, consumer groups. Kafka Connect cho data ingestion. Stream processing với Kafka Streams hoặc Flink cơ bản. Lambda architecture.
- Thực hành: Thiết lập Kafka pipeline: simulate real-time events (user clicks, orders) → Kafka topic → consumer → real-time aggregation → dashboard.
- Checkpoint: Pipeline phải xử lý 1.000 events/giây với latency <100ms.

---

### Giai đoạn 3: Data Engineering cho AI/ML (tuần 10–12)

**Tuần 10 — Feature Engineering & Feature Store**
- Nội dung: Feature engineering là gì và tại sao quan trọng. Feature types: numerical, categorical, temporal, text, embedding. Feature Store concept: tại sao Uber, Airbnb xây dựng Feature Store. Feast (open-source Feature Store) cơ bản. Online vs. Offline feature serving.
- Thực hành: Xây dựng feature pipeline cho một ML use case (ví dụ: churn prediction): extract raw data → engineer features → store trong Feast → serve cho model training và inference.
- Checkpoint: Feature pipeline phải tạo ra ít nhất 20 features từ raw data. Features phải có documentation và lineage.

**Tuần 11 — Data Pipeline cho LLM Applications**
- Nội dung: RAG data pipeline: document ingestion → chunking → embedding → vector database. Chunking strategies: fixed-size, semantic, recursive. Embedding models: OpenAI, Sentence Transformers. Vector database ingestion pipeline. Incremental update cho vector database.
- Thực hành: Xây dựng automated pipeline: crawl tài liệu từ web → chunk → embed → load vào Qdrant vector database. Pipeline tự động cập nhật khi có tài liệu mới.
- Checkpoint: Pipeline phải xử lý 100 tài liệu PDF trong <5 phút. Semantic search phải trả về kết quả liên quan cho 90% test queries.

**Tuần 12 — Data Governance & Lineage**
- Nội dung: Data governance là gì và tại sao quan trọng (GDPR, data privacy). Data catalog: Apache Atlas, DataHub. Data lineage: biết dữ liệu đến từ đâu và đi đến đâu. Data access control. PII (Personally Identifiable Information) detection và masking.
- Thực hành: Thiết lập DataHub cho data platform đã xây dựng. Document tất cả datasets, owners, và lineage. Implement PII masking cho một dataset có thông tin cá nhân.
- Checkpoint: DataHub phải hiển thị lineage đầy đủ từ raw source đến final mart. PII fields phải được mask trước khi đưa vào analytics layer.

---

### Giai đoạn 4: Đồ án capstone (tuần 13–15)

**Tuần 13 — Hoàn thiện đồ án**

Yêu cầu: Xây dựng một data platform hoàn chỉnh cho một use case thực tế (tự chọn hoặc từ danh sách gợi ý):

**Gợi ý use case:**
- E-commerce analytics: pipeline từ orders/products/users → data warehouse → dashboard + AI recommendation
- Social media analytics: pipeline từ API → real-time processing → sentiment analysis → dashboard
- IoT data platform: pipeline từ sensor data → time-series database → anomaly detection → alert

**Checklist bắt buộc:**
- [ ] Ít nhất 2 nguồn dữ liệu khác nhau
- [ ] ETL/ELT pipeline tự động (Airflow DAG)
- [ ] Data transformation với dbt (≥5 models)
- [ ] Data quality checks (Great Expectations)
- [ ] Data warehouse trên cloud (BigQuery hoặc Snowflake free tier)
- [ ] Ít nhất 1 use case AI/ML sử dụng dữ liệu từ pipeline
- [ ] Documentation và lineage

**Tuần 14–15 — Demo & Data Architecture Defense**

Format bảo vệ (20 phút/sinh viên):
- 5 phút: Demo pipeline đang chạy (Airflow UI, dbt docs, data warehouse).
- 5 phút: Demo use case AI/ML sử dụng dữ liệu từ pipeline.
- 10 phút: Trả lời câu hỏi kỹ thuật.

Câu hỏi mẫu:
> *"Nếu nguồn dữ liệu thay đổi schema (thêm cột mới, đổi tên cột), pipeline của em xử lý thế nào?"*  
> *"Chi phí BigQuery của em mỗi tháng là bao nhiêu? Nếu data tăng 100x, chi phí tăng bao nhiêu?"*  
> *"Nếu Airflow DAG fail lúc 3 giờ sáng, em có biết không? Hệ thống của em có tự recover không?"*  
> *"Data lineage của em có thể trả lời câu hỏi: 'Cột revenue trong dashboard đến từ bảng nào trong source database?' không?"*

---

## IV. Phương pháp đánh giá

| Thành phần | Trọng số | Mô tả |
|---|---|---|
| Checkpoint hàng tuần (tuần 1–12) | 30% | 12 checkpoint, rubric rõ ràng |
| Bài kiểm tra giữa kỳ (tuần 7) | 20% | Thiết kế data pipeline cho một use case cho trước — mở tài liệu, mở AI |
| Đồ án — data platform | 30% | Đánh giá theo checklist bắt buộc |
| Data architecture defense | 20% | Trả lời câu hỏi về thiết kế, chi phí, failure handling |

---

## V. Tài liệu & công cụ

### Tài liệu bắt buộc đọc
- [Fundamentals of Data Engineering (O'Reilly)](https://www.oreilly.com/library/view/fundamentals-of-data/9781098108298/) — sách nền tảng tốt nhất
- [dbt Documentation](https://docs.getdbt.com) — tham khảo trong suốt học phần
- [Apache Airflow Documentation](https://airflow.apache.org/docs/)
- [The Data Engineering Cookbook](https://github.com/andkret/Cookbook) — miễn phí trên GitHub

### Công cụ bắt buộc
- Python 3.12+ với: pandas, SQLAlchemy, pydantic, great_expectations
- Apache Airflow (Docker Compose setup)
- dbt Core (miễn phí)
- PostgreSQL (local development)
- BigQuery (GCP free tier) hoặc Snowflake (30-day free trial)
- Kafka (Docker Compose)
- Feast (Feature Store)

---

## VI. So sánh với chương trình hiện tại

| Nội dung | Chương trình cũ (HTTT) | DATA-ENG (mới) |
|---|---|---|
| Pipeline dữ liệu | Không có | Airflow DAG tự động |
| Transformation | SQL thủ công | dbt với testing và documentation |
| Data quality | Không có | Great Expectations tự động |
| Cloud DW | Không có | BigQuery/Snowflake thực tế |
| AI/ML data prep | Không có | Feature Store, RAG pipeline |
| Đánh giá | Báo cáo PDF | Live demo data platform |

---

*Học phần DATA-ENG — Khoa CNTT, Trường Đại học Thủy lợi. Phiên bản 1.0 — Tháng 4/2026.*
