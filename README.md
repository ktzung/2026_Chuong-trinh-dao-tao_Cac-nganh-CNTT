# 🎓 Rà soát và đề xuất nâng cấp chương trình đào tạo CNTT (2026–2030)

> **Trường Đại học Thăng Long (TLU) — Khối ngành Công nghệ Thông tin**  
> Tài liệu chiến lược: Tái cấu trúc toàn diện 5 chương trình đào tạo CNTT trong kỷ nguyên AI Agent.

---

## 📌 Tổng quan dự án

Đây là kho tài liệu chiến lược phục vụ công tác **rà soát, đánh giá và đề xuất nâng cấp** chương trình đào tạo đại học (CTĐT) cho **5 ngành thuộc khối CNTT**, nhằm đáp ứng xu hướng thị trường lao động công nghệ giai đoạn **2026–2030** — thời đại AI agent đã "hàng hóa hóa" kỹ năng lập trình cấp thấp và trung bình.

### 🎯 Mục tiêu chiến lược

Chuyển dịch mục tiêu đào tạo từ:

| ❌ Tư duy cũ (kỷ nguyên 2010) | ✅ Tư duy mới (kỷ nguyên AI 2026+) |
|---|---|
| **"Code generator"** — đào tạo thợ gõ mã | **"AI orchestrator & system architect"** — đào tạo kiến trúc sư điều phối AI |
| Học cú pháp ngôn ngữ lập trình | Học system design, cloud, tích hợp AI |
| Viết CRUD API từ đầu | Thiết kế microservices, triển khai CI/CD |
| Bài thi: viết chương trình X | Bài thi: debug, oral defense, live debugging |

---

## 🏫 Các ngành được đánh giá

| Mã ngành | Tên ngành | Mức rủi ro AI | Định hướng mới |
|:---:|---|:---:|---|
| **KTPM** | Kỹ thuật phần mềm | 🔴 Nguy cơ cao nhất | AI-assisted software architecture |
| **CNTT** | Công nghệ thông tin | 🟠 Nguy cơ cao | Cloud & distributed systems |
| **HTTT** | Hệ thống thông tin | 🟡 Nguy cơ trung bình | Data engineering & AI-driven BI |
| **TTNT** | Trí tuệ nhân tạo & khoa học dữ liệu | 🟢 Nguy cơ thấp | LLMOps, MLOps & AI product |
| **ANM** | An ninh mạng | 🟡 Nguy cơ trung bình | AI-powered security & LLM security |

---

## 📁 Cấu trúc repository

```
2026_Chuong-trinh-dao-tao_Cac-nganh-CNTT/
│
├── 📂 01_Khung_CTDT_Hien_Tai/              # Khung CTĐT gốc (theo QĐ3511)
│   ├── ANM.md                               # Khung ngành an ninh mạng
│   ├── CNTT.md                              # Khung ngành công nghệ thông tin
│   ├── HTTT.md                              # Khung ngành hệ thống thông tin
│   ├── KTPM.md                              # Khung ngành kỹ thuật phần mềm
│   ├── TTNT.md                              # Khung ngành trí tuệ nhân tạo
│   └── QD3511_KhungCTDT.2025-...pdf        # Quyết định chính thức khung CTĐT
│
├── 📂 02_Huong_Dan_Va_Bieu_Mau/            # Hướng dẫn và biểu mẫu sử dụng
│   ├── Review_Role.md                       # Bối cảnh và vai trò đánh giá
│   ├── Review_Update.md                     # Hướng dẫn cập nhật rà soát
│   └── Template.md                          # Biểu mẫu đánh giá chuẩn
│
├── 📂 03_Bao_Cao_Ra_Soat_Tong_Hop/        # Báo cáo chiến lược tổng hợp
│   ├── 01_Danh_Gia_Tong_Quan_Ban_Dau.md   # Đánh giá ban đầu & đề xuất chiến lược
│   ├── 02_Ra_Soat_CTDT_Toan_Dien_10_Phases.md  # Rà soát toàn diện theo 10 phases
│   └── 03_De_Xuat_Khung_CTDT_Moi.md       # Blueprint khung CTĐT mới (2026-2030)
│
├── 📂 04_Danh_Gia_Chi_Tiet_Tung_Nganh/    # Đánh giá chi tiết từng ngành
│   ├── ANM_Danh_Gia_Chi_Tiet.md
│   ├── CNTT_Danh_Gia_Chi_Tiet.md
│   ├── HTTT_Danh_Gia_Chi_Tiet.md
│   ├── KTPM_Danh_Gia_Chi_Tiet.md
│   └── TTNT_Danh_Gia_Chi_Tiet.md
│
└── README.md                                # Tài liệu này
```

---

## 📋 Nội dung chi tiết từng thư mục

### 📂 `01_Khung_CTDT_Hien_Tai/` — Khung hiện tại

Chứa các file mô tả chương trình đào tạo gốc của từng ngành theo **Quyết định 3511**, bao gồm danh sách học phần, số tín chỉ, phân bổ theo học kỳ. Đây là cơ sở để đối chiếu, phân tích và đề xuất cải tiến.

**Điểm nổi bật của CTĐT hiện tại:**
- ✅ Đã có học phần **"Kỹ năng số và khai thác AI" (CSE105)** ngay từ học kỳ 1 — bước đi tiên phong
- ✅ Ngành TTNT đã có **AI tạo sinh & mô hình ngôn ngữ lớn (CSE134)** và **hệ thống tác tử (CSE107)**
- ✅ Cấu trúc học phần linh hoạt, có môn tự chọn theo xu hướng
- ⚠️ Vẫn phân bổ nhiều tín chỉ cho việc dạy cú pháp lập trình cụ thể
- ⚠️ Thiếu nền tảng cloud, DevOps/MLOps ở hầu hết các ngành

---

### 📂 `02_Huong_Dan_Va_Bieu_Mau/` — Hướng dẫn & biểu mẫu

Chứa tài liệu hướng dẫn quy trình rà soát và biểu mẫu đánh giá chuẩn, bao gồm:
- **`Review_Role.md`**: Mô tả bối cảnh và nhiệm vụ của công tác đánh giá CTĐT trong kỷ nguyên AI
- **`Template.md`**: Mẫu đánh giá chi tiết từng học phần (mức rủi ro AI, đề xuất hành động)

---

### 📂 `03_Bao_Cao_Ra_Soat_Tong_Hop/` — Báo cáo chiến lược

Ba tài liệu cốt lõi của toàn bộ dự án:

#### 📄 `01_Danh_Gia_Tong_Quan_Ban_Dau.md`
- Phân tích các vấn đề tồn tại (pain points) của CTĐT hiện tại
- Đề xuất **4 chiến lược tổng thể** (paradigm shift):
  1. Chuyển đầu ra từ "code generation" → "code review & orchestration"
  2. Bình thường hóa và bắt buộc dùng AI IDE (Cursor, GitHub Copilot)
  3. Cải tiến phương pháp đánh giá (debugging, oral exam)
  4. Phổ cập "AI agent" cho mọi chuyên ngành

#### 📄 `02_Ra_Soat_CTDT_Toan_Dien_10_Phases.md`
- Rà soát từng môn học theo mức rủi ro AI (cao/trung bình/thấp)
- Phân tích theo từng ngành với tầm nhìn 2030
- **Lộ trình 3 giai đoạn chuyển đổi** (2025 → 2026 → 2028)
- Đề xuất thiết kế mới: năm 1 → năm 4

#### 📄 `03_De_Xuat_Khung_CTDT_Moi.md`
- **Blueprint thi công** chi tiết cho từng ngành
- Bảng học phần cũ cần loại bỏ/nâng cấp → học phần mới đề xuất
- Luận cứ thuyết phục cho từng thay đổi

---

### 📂 `04_Danh_Gia_Chi_Tiet_Tung_Nganh/` — Đánh giá chi tiết

Báo cáo phân tích sâu cho từng ngành, bao gồm:
- Đánh giá từng học phần theo tiêu chí rủi ro AI
- Đề xuất nội dung học phần thay thế cụ thể
- Định hướng chuẩn đầu ra (learning outcomes) mới

---

## 🔑 Triết lý thiết kế khung CTĐT mới

### Luận điểm cốt lõi

> **1. Sự sụp đổ của kỹ năng lập trình thô**  
> AI hiện tại (Cursor, Devin, GitHub Copilot) đã giải bài toán viết code từ logic thông thường. Dạy sinh viên gõ từng dòng HTML/CSS hay CRUD API là lãng phí 3 năm thanh xuân và tiền bạc của nhà trường.

> **2. Sự lên ngôi của kiến trúc và tích hợp**  
> Kỹ sư CNTT tương lai phải là "kiến trúc sư và tổng thầu": chia nhỏ bài toán phức tạp, giao AI agent làm từng phần, sau đó tích hợp, kiểm thử và triển khai lên cloud.

> **3. Tách biệt nền tảng và ứng dụng**  
> Toán học, giải thuật, cấu trúc dữ liệu, nguyên lý hệ điều hành → **giữ và dạy sâu hơn**. Lập trình Windows, Java web form, CRUD API thủ công → **loại bỏ**, thay bằng DevOps/MLOps.

---

## 🗺️ Khung CTĐT mới theo năm học

```
Năm 1 — Tư duy nền tảng & AI literacy
├── Toán học cho khoa học máy tính (đại số, xác suất)
├── Tư duy máy tính & nhập môn thuật toán (thực hành tay, không AI)
├── Kỹ năng số & prompt engineering chuyên sâu
└── Kiến trúc máy tính & hệ điều hành

Năm 2 — Kỹ thuật với hỗ trợ AI
├── Cấu trúc dữ liệu & giải thuật nâng cao (trọng tâm: đánh giá code do AI viết)
├── Thiết kế cơ sở dữ liệu & data engineering
├── Mạng máy tính & bảo mật nền tảng
└── Applied AI engineering (API OpenAI/Anthropic, RAG cơ bản)

Năm 3 — Cloud, hệ thống phân tán & điều phối
├── Kiến trúc phần mềm (software architecture & microservices)
├── Cloud computing & MLOps/DevOps
├── Phát triển hệ thống AI agent (bắt buộc chung)
└── Các môn chuyên ngành sâu (bảo mật, dữ liệu, IoT...)

Năm 4 — Đồ án thực tế & tư duy sản phẩm
├── Tư duy sản phẩm (product thinking) & khởi nghiệp
└── Đồ án tốt nghiệp: bắt buộc tích hợp AI — chấm điểm dựa trên
    kiến trúc hệ thống và nhật ký prompt/agent
```

---

## 📊 Lộ trình thực thi

| Giai đoạn | Mục tiêu | Hành động cụ thể |
|---|---|---|
| **2025** | Thiết lập điểm khởi đầu | Áp dụng oral defense cho đồ án; thay lập trình Windows → cloud/AI cơ bản; cấp GitHub Copilot cho giảng viên |
| **2026** | Chuyển đổi phương pháp | Áp dụng live debugging & prompt log; KTPM/CNTT học LLM/tác tử như môn bắt buộc |
| **2028** | Chuyển đổi toàn diện | Xóa hoàn toàn môn dạy cú pháp; 100% CTĐT định hướng kiến trúc hệ thống & kỹ thuật AI |

---

## 🔬 Phương pháp đánh giá mới

Nhằm **vô hiệu hóa gian lận AI** và biến AI thành công cụ hợp pháp trong đào tạo:

| Phương pháp | Mô tả |
|---|---|
| **Chính sách sử dụng AI** | Cho phép dùng AI (Copilot, Cursor) trong 80% bài thi thực hành |
| **Nộp nhật ký prompt** | Sinh viên nộp bài kèm lịch sử trò chuyện với AI — chấm điểm kỹ năng ra lệnh cho máy |
| **Vấn đáp kiến trúc** | Giảng viên hỏi trực tiếp về kiến trúc, lý do chọn giải thuật — người chép code AI rớt ngay |
| **Debug trực tiếp** | Bài thi giữa kỳ: project do AI sinh ra có cài sẵn lỗi, sinh viên tìm và vá trong 60 phút |

---

## 🏢 Yêu cầu hạ tầng

| Hạng mục | Trạng thái hiện tại | Đề xuất |
|---|---|---|
| GitHub Copilot | Chưa có | Cấp miễn phí 100% sinh viên/giảng viên qua GitHub Education |
| Cloud credits | Chưa có | AWS Educate, Azure for Students, Google Cloud Edu |
| API LLM | Chưa có | Cấp ngân sách API OpenAI/Anthropic phục vụ môn thực hành |
| GPU/lab AI | Thiếu | Ưu tiên cloud (không cần GPU vật lý cao cấp) |

---

## 📎 Tài liệu tham chiếu gốc

- **Quyết định 3511**: Khung CTĐT năm 2025 — nhóm ngành CNTT (xem [`01_Khung_CTDT_Hien_Tai/QD3511_KhungCTDT.2025-Nhom nganh CNTT.pdf`](./01_Khung_CTDT_Hien_Tai/QD3511_KhungCTDT.2025-Nhom%20nganh%20CNTT.pdf))
- **Chuẩn ACM/IEEE** cho chương trình đào tạo khoa học máy tính
- **Báo cáo thị trường**: xu hướng tuyển dụng AI agent 2024–2026

---

## ✍️ Thông tin tài liệu

| Thuộc tính | Nội dung |
|---|---|
| **Đơn vị** | Trường Đại học Thủy lợi (TLU) |
| **Phạm vi** | 5 ngành CNTT: ANM, CNTT, HTTT, KTPM, TTNT |
| **Phiên bản** | 1.0 — tháng 4/2026 |
| **Mục tiêu áp dụng** | Khóa tuyển sinh 2026 trở đi |
| **Tầm nhìn** | 2026–2030 |

---

> 💡 **Kết luận chiến lược:**  
> Đây không chỉ là sự nâng cấp — đây là vấn đề **sinh tồn** của chất lượng đào tạo và giá trị văn bằng khối ngành CNTT trong thập kỷ tới. Cần một cuộc "đại phẫu thuật", không phải sửa đổi nhỏ giọt.
