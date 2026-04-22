# 🎓 Rà Soát & Đề Xuất Nâng Cấp Chương Trình Đào Tạo CNTT (2026–2030)

> **Trường Đại học Thủy lợi (TLU) — Khối ngành Công nghệ Thông tin**  
> Tài liệu chiến lược: Tái cấu trúc toàn diện 5 chương trình đào tạo CNTT trong kỷ nguyên AI Agent.

---

## 📌 Tổng Quan Dự Án

Đây là kho tài liệu chiến lược phục vụ công tác **rà soát, đánh giá và đề xuất nâng cấp** chương trình đào tạo đại học (CTĐT) cho **5 ngành thuộc khối CNTT**, nhằm đáp ứng xu hướng thị trường lao động công nghệ giai đoạn **2026–2030** — thời đại AI Agent đã "hàng hóa hóa" kỹ năng lập trình cấp thấp và trung bình.

### 🎯 Mục Tiêu Chiến Lược

Chuyển dịch mục tiêu đào tạo từ:

| ❌ Tư duy cũ (Kỷ nguyên 2010) | ✅ Tư duy mới (Kỷ nguyên AI 2026+) |
|---|---|
| **"Code Generator"** — Đào tạo thợ gõ mã | **"AI Orchestrator & System Architect"** — Đào tạo kiến trúc sư điều phối AI |
| Học cú pháp ngôn ngữ lập trình | Học System Design, Cloud, AI Integration |
| Viết CRUD API từ đầu | Thiết kế Microservices, triển khai CI/CD |
| Bài thi: Viết chương trình X | Bài thi: Debug, Oral Defense, Live Debugging |

---

## 🏫 Các Ngành Được Đánh Giá

| Mã ngành | Tên ngành | Mức Rủi ro AI | Định hướng Mới |
|:---:|---|:---:|---|
| **KTPM** | Kỹ thuật Phần mềm | 🔴 Nguy cơ Cao nhất | AI-Assisted Software Architecture |
| **CNTT** | Công nghệ Thông tin | 🟠 Nguy cơ Cao | Cloud & Distributed Systems |
| **HTTT** | Hệ thống Thông tin | 🟡 Nguy cơ Trung bình | Data Engineering & AI-driven BI |
| **TTNT** | Trí tuệ Nhân tạo & KHDT | 🟢 Nguy cơ Thấp | LLMOps, MLOps & AI Product |
| **ANM** | An ninh Mạng | 🟡 Nguy cơ Trung bình | AI-Powered Security & LLM Security |

---

## 📁 Cấu Trúc Repository

```
2026_Chuong-trinh-dao-tao_Cac-nganh-CNTT/
│
├── 📂 01_Khung_CTDT_Hien_Tai/          # Khung CTĐT gốc (theo QĐ3511)
│   ├── ANM.md                           # Khung ngành An ninh Mạng
│   ├── CNTT.md                          # Khung ngành Công nghệ Thông tin
│   ├── HTTT.md                          # Khung ngành Hệ thống Thông tin
│   ├── KTPM.md                          # Khung ngành Kỹ thuật Phần mềm
│   ├── TTNT.md                          # Khung ngành Trí tuệ Nhân tạo
│   └── QD3511_KhungCTDT.2025-...pdf    # Quyết định chính thức khung CTĐT
│
├── 📂 02_Huong_Dan_Va_Bieu_Mau/        # Hướng dẫn và biểu mẫu sử dụng
│   ├── Review_Role.md                   # Bối cảnh và vai trò đánh giá
│   ├── Review_Update.md                 # Hướng dẫn cập nhật rà soát
│   └── Template.md                      # Biểu mẫu đánh giá chuẩn
│
├── 📂 03_Bao_Cao_Ra_Soat_Tong_Hop/    # Báo cáo chiến lược tổng hợp
│   ├── 01_Danh_Gia_Tong_Quan_Ban_Dau.md   # Đánh giá ban đầu & đề xuất chiến lược
│   ├── 02_Ra_Soat_CTDT_Toan_Dien_10_Phases.md # Rà soát toàn diện theo 10 phases
│   └── 03_De_Xuat_Khung_CTDT_Moi.md   # Blueprint khung CTĐT mới (2026-2030)
│
├── 📂 04_Danh_Gia_Chi_Tiet_Tung_Nganh/ # Đánh giá chi tiết từng ngành
│   ├── ANM_Danh_Gia_Chi_Tiet.md
│   ├── CNTT_Danh_Gia_Chi_Tiet.md
│   ├── HTTT_Danh_Gia_Chi_Tiet.md
│   ├── KTPM_Danh_Gia_Chi_Tiet.md
│   └── TTNT_Danh_Gia_Chi_Tiet.md
│
└── README.md                            # Tài liệu này
```

---

## 📋 Nội Dung Chi Tiết Từng Thư Mục

### 📂 `01_Khung_CTDT_Hien_Tai/` — Khung Hiện Tại

Chứa các file mô tả chương trình đào tạo gốc của từng ngành theo **Quyết định 3511**, bao gồm danh sách học phần, số tín chỉ, phân bổ theo học kỳ. Đây là cơ sở để đối chiếu, phân tích và đề xuất cải tiến.

**Điểm nổi bật của CTĐT hiện tại:**
- ✅ Đã có học phần **"Kỹ năng số và Khai thác AI" (CSE105)** ngay từ Học kỳ 1 — bước đi tiên phong
- ✅ Ngành TTNT đã có **AI Tạo sinh & Mô hình ngôn ngữ lớn (CSE134)** và **Hệ thống Tác tử (CSE107)**
- ✅ Cấu trúc học phần linh hoạt, có môn tự chọn theo xu hướng
- ⚠️ Vẫn phân bổ nhiều tín chỉ cho việc dạy cú pháp lập trình cụ thể
- ⚠️ Thiếu nền tảng Cloud, DevOps/MLOps ở hầu hết các ngành

---

### 📂 `02_Huong_Dan_Va_Bieu_Mau/` — Hướng Dẫn & Biểu Mẫu

Chứa tài liệu hướng dẫn quy trình rà soát và biểu mẫu đánh giá chuẩn, bao gồm:
- **`Review_Role.md`**: Mô tả bối cảnh và nhiệm vụ của công tác đánh giá CTĐT trong kỷ nguyên AI
- **`Template.md`**: Mẫu đánh giá chi tiết từng học phần (AI Risk Level, đề xuất hành động)

---

### 📂 `03_Bao_Cao_Ra_Soat_Tong_Hop/` — Báo Cáo Chiến Lược

Ba tài liệu cốt lõi của toàn bộ dự án:

#### 📄 `01_Danh_Gia_Tong_Quan_Ban_Dau.md`
- Phân tích pain points của CTĐT hiện tại
- Đề xuất **4 chiến lược tổng thể** (Paradigm Shift):
  1. Chuyển đầu ra từ "Code Generation" → "Code Review & Orchestration"
  2. Bình thường hóa & bắt buộc dùng AI IDE (Cursor, GitHub Copilot)
  3. Cải tiến phương pháp đánh giá (Debugging, Oral Exam)
  4. Phổ cập "AI Agent" cho mọi chuyên ngành

#### 📄 `02_Ra_Soat_CTDT_Toan_Dien_10_Phases.md`
- Rà soát từng môn học theo mức rủi ro AI (High/Medium/Low)
- Phân tích theo từng ngành với tầm nhìn 2030
- **Lộ trình 3 giai đoạn chuyển đổi** (2025 → 2026 → 2028)
- Đề xuất thiết kế mới: YEAR 1 → YEAR 4

#### 📄 `03_De_Xuat_Khung_CTDT_Moi.md`
- **"Blueprint" thi công** chi tiết cho từng ngành
- Bảng học phần cũ cần loại bỏ/nâng cấp → học phần mới đề xuất
- Luận cứ thuyết phục cho từng thay đổi

---

### 📂 `04_Danh_Gia_Chi_Tiet_Tung_Nganh/` — Đánh Giá Chi Tiết

Báo cáo phân tích sâu cho từng ngành, bao gồm:
- Đánh giá từng học phần theo tiêu chí AI Risk
- Đề xuất nội dung học phần thay thế cụ thể
- Định hướng chuẩn đầu ra (Learning Outcomes) mới

---

## 🔑 Triết Lý Thiết Kế Khung CTĐT Mới

### Luận điểm cốt lõi (Core Arguments)

> **1. Sự sụp đổ của kỹ năng lập trình thô (The Fall of Raw Coding)**  
> AI hiện tại (Cursor, Devin, GitHub Copilot) đã giải bài toán viết code từ logic thông thường. Dạy sinh viên gõ từng dòng HTML/CSS hay CRUD API là lãng phí 3 năm thanh xuân và tiền bạc nhà trường.

> **2. Sự lên ngôi của Kiến trúc và Tích hợp (The Rise of Architecture & Integration)**  
> Kỹ sư CNTT tương lai phải là "Kiến trúc sư & Tổng thầu": Chia nhỏ bài toán phức tạp, giao AI Agent làm từng phần, sau đó tích hợp (integrate), kiểm thử và triển khai lên Cloud.

> **3. Tách biệt Nền tảng và Ứng dụng**  
> Toán học, Giải thuật, CTDL, Nguyên lý HĐH → **Giữ và dạy sâu hơn**. Lập trình Windows, Java Web Form, CRUD API thủ công → **Loại bỏ**, thay bằng DevOps/MLOps.

---

## 🗺️ Khung CTĐT Mới Theo Năm Học

```
YEAR 1 — TƯ DUY NỀN TẢNG & AI LITERACY
├── Toán học cho KHMT (Đại số, Xác suất)
├── Tư duy máy tính & Nhập môn thuật toán (thực hành tay, không AI)
├── Kỹ năng số & Prompt Engineering chuyên sâu
└── Kiến trúc máy tính & Hệ điều hành

YEAR 2 — AI-ASSISTED ENGINEERING
├── CTDL & Giải thuật nâng cao (trọng tâm: Code Review thuật toán AI viết)
├── Thiết kế CSDL & Data Engineering
├── Mạng máy tính & Bảo mật nền tảng
└── Applied AI Engineering (API OpenAI/Anthropic, RAG cơ bản)

YEAR 3 — CLOUD, DISTRIBUTED SYSTEMS & ORCHESTRATION
├── Kiến trúc phần mềm (Software Architecture & Microservices)
├── Cloud Computing & MLOps/DevOps
├── Phát triển hệ thống AI Agent (BẮT BUỘC chung)
└── Các môn chuyên ngành sâu (Security, Data, IoT...)

YEAR 4 — INDUSTRY CAPSTONE & PRODUCT
├── Tư duy Sản phẩm (Product Thinking) & Khởi nghiệp
└── Đồ án tốt nghiệp: Bắt buộc tích hợp AI — Chấm điểm dựa trên
    System Architecture và Prompt/Agent Logs
```

---

## 📊 Lộ Trình Thực Thi

| Giai đoạn | Mục tiêu | Hành động cụ thể |
|---|---|---|
| **2025** | Thiết lập Baseline | Áp dụng Oral Defense cho Đồ án; Thay Lập trình Windows → Cloud/AI cơ bản; Cấp GitHub Copilot cho GV |
| **2026** | Chuyển đổi Phương pháp | Áp dụng Live Debugging & Prompt Log; KTPM/CNTT học LLM/Tác tử như môn bắt buộc |
| **2028** | Full Transformation | Xóa hoàn toàn môn dạy cú pháp; 100% CTĐT định hướng System Architecture & AI Engineering |

---

## 🔬 Phương Pháp Đánh Giá Mới (Assessment Redesign)

Nhằm **vô hiệu hóa gian lận AI** và biến AI thành công cụ hợp pháp trong đào tạo:

| Phương pháp | Mô tả |
|---|---|
| **AI Usage Policy** | Cho phép dùng AI (Copilot, Cursor) trong 80% bài thi thực hành |
| **Prompt Logs** | Sinh viên nộp bài kèm lịch sử trò chuyện/prompt với AI — chấm điểm kỹ năng ra lệnh cho máy |
| **Oral Defense** | GV hỏi trực tiếp về kiến trúc, lý do chọn giải thuật — người chép code AI rớt ngay |
| **Live Debugging** | Bài thi giữa kỳ: Project do AI sinh ra có cài sẵn bug, SV tìm & vá trong 60 phút |

---

## 🏢 Yêu Cầu Hạ Tầng

| Hạng mục | Trạng thái hiện tại | Đề xuất |
|---|---|---|
| GitHub Copilot | Chưa có | Cấp miễn phí 100% SV/GV qua GitHub Education |
| Cloud Credits | Chưa có | AWS Educate, Azure for Students, Google Cloud Edu |
| API LLM | Chưa có | Budget cho OpenAI/Anthropic API phục vụ môn thực hành |
| GPU/Lab AI | Thiếu | Ưu tiên Cloud (không cần GPU vật lý cao cấp) |

---

## 📎 Tài Liệu Tham Chiếu Gốc

- **Quyết định 3511**: Khung CTĐT năm 2025 — nhóm ngành CNTT (xem [`01_Khung_CTDT_Hien_Tai/QD3511_KhungCTDT.2025-Nhom nganh CNTT.pdf`](./01_Khung_CTDT_Hien_Tai/QD3511_KhungCTDT.2025-Nhom%20nganh%20CNTT.pdf))
- **Chuẩn ACM/IEEE** cho chương trình đào tạo Khoa học Máy tính
- **Báo cáo thị trường**: Xu hướng tuyển dụng AI Agent 2024-2026

---

## ✍️ Thông Tin Tài Liệu

| Thuộc tính | Nội dung |
|---|---|
| **Đơn vị** | Trường Đại học Thủy lợi (TLU) |
| **Phạm vi** | 5 ngành CNTT: ANM, CNTT, HTTT, KTPM, TTNT |
| **Phiên bản** | 1.0 — Tháng 4/2026 |
| **Mục tiêu áp dụng** | Khóa tuyển sinh 2026 trở đi |
| **Tầm nhìn** | 2026–2030 |

---

> 💡 **Kết luận chiến lược:**  
> Đây không chỉ là sự nâng cấp — đây là vấn đề **sinh tồn** của chất lượng đào tạo và giá trị văn bằng khối ngành CNTT trong thập kỷ tới. Cần một cuộc "đại phẫu thuật", không phải sửa đổi nhỏ giọt.
