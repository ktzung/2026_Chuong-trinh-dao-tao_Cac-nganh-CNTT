# BÁO CÁO RÀ SOÁT VÀ ĐỀ XUẤT NÂNG CẤP CHƯƠNG TRÌNH ĐÀO TẠO
## Ngành an ninh mạng (ANM) — Tầm nhìn 2026–2030

> **Kính gửi:** Hội đồng Khoa học & Đào tạo Khoa CNTT
> **Người thực hiện:** Tổ Rà soát Chương trình
> **Thời gian:** Tháng 4/2026

---

## I. Tóm tắt đề xuất

An ninh mạng đang bước vào giai đoạn biến đổi chiến lược sâu sắc nhất kể từ khi Internet ra đời. Cuộc chơi thay đổi theo hai hướng đồng thời: **(1) AI trở thành vũ khí tấn công cực mạnh** — hacker dùng LLM để tự động sinh mã độc đa hình (polymorphic malware), dò quét lỗ hổng quy mô lớn, tạo nội dung phishing cực kỳ thuyết phục; **(2) AI trở thành lá chắn không thể thiếu** — các hệ thống SIEM hiện đại, EDR thế hệ mới đều dùng ML để phát hiện bất thường.

Nguy cơ nghiêm trọng nhất của chương trình ANM hiện tại: **đang đào tạo sinh viên phòng thủ thủ công trong khi kẻ tấn công đã vũ khí hóa AI**. Một sinh viên phân tích malware thủ công tốn 3 ngày; một AI Tool tốn 3 phút.

Đề xuất tái định vị ngành ANM thành **"AI-Powered Cybersecurity & AI Systems Defense"** — đào tạo chuyên gia biết *dùng AI để bảo vệ* và *bảo vệ chính các hệ thống AI*.

---

## II. Chẩn đoán chương trình hiện tại

### Điểm mạnh cần bảo tồn
- Nền tảng kỹ thuật vững: Mật mã ứng dụng, Lập trình mạng, Quản trị mạng, Thiết kế mạng.
- Có các môn chuyên sâu thực tế: Phân tích mã độc, Điều tra số, An ninh mạng — cốt lõi của nghề.
- Đánh giá an ninh mạng (CSE495) — môn thực hành Pentest quan trọng, cần nâng cấp sang tự động hóa.

### Điểm yếu nghiêm trọng
1. **Không có AI Security:** Không một môn học nào đề cập đến bảo mật cho hệ thống LLM, chống Prompt Injection, hay Data Poisoning — trong khi đây là mặt trận mới nhất của an ninh mạng.
2. **Phòng thủ thủ công là chính:** Log analysis bằng mắt thường, Malware analysis theo từng bước — AI Agent đã làm điều này nhanh hơn 100 lần.
3. **Không có Cloud Security:** Hầu hết hệ thống doanh nghiệp hiện chạy trên Cloud, nhưng chương trình không có môn Cloud Security chuyên biệt.
4. **Các môn lập trình ứng dụng không đúng chỗ:** Các môn như Lập trình Windows, Java nằm trong track tự chọn của ANM — không liên quan đến nghề.

---

## III. Phân tích rủi ro AI — từng học phần

| Học phần | Mã HP | TC | Rủi ro AI | Quyết định đề xuất |
|----------|-------|----|-----------|-------------------|
| Nhập môn lập trình | CSE111 | 3 | 🟡 Trung bình | Giữ — học Python/C từ đầu (cần biết tầng thấp) |
| Lập trình nâng cao | CSE205 | 3 | 🟡 Trung bình | Giữ — tập trung scripting & exploit development cơ bản |
| Toán rời rạc | CSE203 | 3 | 🟢 Thấp | Giữ — nền tảng cho mật mã học |
| CTDL & Giải thuật | CSE281 | 3 | 🟢 Thấp | Giữ nguyên |
| Kiến trúc máy tính | CSE370 | 3 | 🟢 Thấp | Giữ — thêm CPU/Memory exploitation (Buffer overflow) |
| Cơ sở dữ liệu | CSE484 | 3 | 🟡 Trung bình | Giữ — thêm SQL Injection, DB Security |
| Mạng máy tính | CSE489 | 3 | 🟢 Thấp | Giữ — **nền tảng cốt lõi** của ANM |
| Lập trình hướng đối tượng | CSE116 | 3 | 🟡 Trung bình | Giữ — tập trung Secure Coding từ đây |
| Hệ điều hành | CSE482 | 3 | 🟢 Thấp | Giữ — **rất quan trọng**: process, syscall, privilege escalation |
| Phát triển UD Web cơ bản | CSE122 | 3 | 🔴 **Cao** | **LOẠI BỎ** — thay bằng Web Security & OWASP Top 10 |
| Nhập môn ATBMTT | CSE400 | 3 | 🟢 Thấp | Giữ — **bắt buộc** nhưng cần cập nhật AI threat landscape |
| Điện toán đám mây | CSE121 | 3 | 🟢 Thấp | **Nâng thành BẮT BUỘC** — thêm Cloud Security (IAM, VPC, SIEM) |
| Phân tích dữ liệu | CSE131 | 3 | 🟡 Trung bình | Giữ — tập trung Security Log Analytics |
| Trí tuệ nhân tạo | CSE492 | 3 | 🟡 Trung bình | **Thay bằng** AI for Cybersecurity |
| Phân tích & thiết kế HT | CSE123 | 3 | 🟡 Trung bình | Giữ ở mức nhẹ — tập trung Security Architecture |
| Công nghệ phần mềm | CSE481 | 3 | 🔴 **Cao** | **Thay bằng** DevSecOps |
| Lập trình mạng | CSE401 | 3 | 🟢 Thấp | Giữ — **cốt lõi** cho ANM: raw sockets, packet crafting |
| Mật mã ứng dụng | CSE402 | 3 | 🟢 Thấp | Giữ — thêm Post-Quantum Cryptography |
| Quản trị mạng | CSE421 | 3 | 🟡 Trung bình | Giữ — thêm Network Security Automation |
| **An ninh mạng** | CSE478 | 3 | 🟢 Thấp | Giữ — **bắt buộc, cốt lõi** |
| **Phân tích mã độc** | CSE471 | 3 | 🟢 Thấp | Giữ — **thêm AI-assisted Malware Analysis** |
| Quản lý ATTT | CSE472 | 3 | 🟢 Thấp | Giữ — thêm AI Governance trong bảo mật |
| Lập trình an toàn | CSE473 | 3 | 🟢 Thấp | Giữ — **rất quan trọng**: OWASP, Secure SDLC |
| Thiết kế mạng | CSE420 | 3 | 🟢 Thấp | Giữ — thêm Zero Trust Network Architecture |
| Đánh giá an ninh mạng | CSE495 | 3 | 🟡 Trung bình | **Nâng cấp**: thêm Automated Pentest (AI-assisted) |
| **Điều tra số** | CSE141 | 3 | 🟢 Thấp | Giữ — thêm AI-assisted Forensics |
| Chuyên đề ANM | CSE474 | 2 | 🟡 Trung bình | **Mở rộng** — cập nhật chủ đề AI Security |
| **Lập trình Windows (tự chọn)** | CSE383 | 3 | 🔴 **Cao** | **LOẠI KHỎI DANH SÁCH TỰ CHỌN** — không liên quan |
| **Java ứng dụng (tự chọn)** | CSE114 | 3 | 🔴 **Cao** | **LOẠI KHỎI DANH SÁCH TỰ CHỌN** — không liên quan |

---

## IV. Học phần đề xuất loại bỏ hoặc thay thế — luận giải

### 4.1. Phát triển ứng dụng Web cơ bản (CSE122 — 3 TC) → TÁI ĐỊNH HƯỚNG CHO ANM

**Luận cứ:**
- Web không phải kỹ năng cần loại bỏ khỏi ANM — ngược lại, web là **mặt trận tấn công chủ yếu** trong an ninh mạng thực tế. OWASP Top 10 là tập hợp các lỗ hổng *đều* ở tầng ứng dụng web.
- Vấn đề là **cách dạy cũ sai mục tiêu**: dạy sinh viên ANM *xây dựng* website (HTML form, PHP CRUD) là hoàn toàn không phù hợp. Họ cần dạy *tấn công và phòng thủ* trên nền tảng web.
- Môn học cần được **tái định hướng hoàn toàn nội dung**, không bỏ mà đổi mục tiêu 180 độ.

**Thay thế nội dung:** Học phần **"Bảo mật ứng dụng Web & OWASP"** — dạy Burp Suite, OWASP Testing Guide, khai thác XSS/CSRF/SQLi thực tế, thực hành trên HackTheBox/TryHackMe. Dùng AI agent để tự động hóa dò quét lỗ hổng web.


### 4.2. Công nghệ phần mềm truyền thống (CSE481 — 3 TC) → THAY BẰNG DEVSECOPS

**Luận cứ:**
- SDLC truyền thống (Waterfall, Scrum) không phải kỹ năng cốt lõi của kỹ sư ANM.
- Kỹ năng thực sự cần: Tích hợp bảo mật vào CI/CD pipeline (SAST, DAST), quản lý secrets, container security scanning.
- DevSecOps là một trong những kỹ năng được tuyển dụng nhiều nhất trong lĩnh vực ANM năm 2025-2026 (nguồn: ISC2 Cybersecurity Workforce Study 2025).

**Thay thế:** Học phần **"DevSecOps & Secure Software Supply Chain"** — GitHub Advanced Security, SonarQube, Trivy, Software Bill of Materials (SBOM).

### 4.3. Lập trình Windows (CSE383) & Java ứng dụng (CSE114) trong Track tự chọn → LOẠI KHỎI ANM

**Luận cứ:**
- Không có mối liên hệ logic nào giữa việc học WinForms/Java CRUD với kỹ năng bảo mật.
- Slot tự chọn quý giá của ngành ANM nên dành cho: AI Security, Malware Reverse Engineering nâng cao, Cloud Security, Red Team Operations.

---

## V. Đề xuất chương trình đào tạo mới (tham khảo — 140 TC)

### Khối I: Giáo dục đại cương (37 TC — giữ nguyên)

*(Giữ nguyên cấu trúc. Đặc biệt, Toán rời rạc có giá trị nền tảng cao cho Mật mã học — nên liên kết bài tập rõ ràng hơn.)*

---

### Khối II: Nền tảng kỹ thuật (27 TC)

| TT | Học phần | TC | HK | Ghi chú thay đổi |
|----|----------|----|----|-----------------|
| 1 | Lập trình Python & C cho ANM | 3 | 1 | Python: scripting, automation; C: hiểu memory, exploit |
| 2 | Toán rời rạc | 3 | 2 | Liên kết trực tiếp bài tập với mật mã học |
| 3 | CTDL & Giải thuật | 3 | 2 | Giữ nguyên |
| 4 | Kiến trúc máy tính & Lập trình hệ thống | 3 | 2 | Thêm: x86 Assembly cơ bản, Buffer Overflow, Memory Corruption |
| 5 | Cơ sở dữ liệu & Database Security | 3 | 3 | SQL + SQL Injection + Parameterized Queries |
| 6 | Mạng máy tính & Phân tích giao thức | 3 | 2 | Wireshark, Packet Capture, Protocol Analysis |
| 7 | Hệ điều hành & Bảo mật hệ thống | 3 | 3 | Linux privilege escalation, Windows permissions, Syscall hooking |
| 8 | Lập trình mạng | 3 | 3 | Raw sockets, Packet crafting (Scapy), Network tool development |
| 9 | Lập trình hướng đối tượng & Secure Coding | 3 | 3 | OOP + Secure Coding practices ngay từ đầu |

---

### Khối III: Lõi an ninh mạng (30 TC — bắt buộc)

| TT | Học phần | TC | HK | Ghi chú thay đổi |
|----|----------|----|----|-----------------|
| 10 | Nhập môn AT&BMTT & AI Threat Landscape | 3 | 3 | Cập nhật: AI-powered threats, Deepfake, AI social engineering |
| 11 | Mật mã ứng dụng & Post-Quantum Crypto | 3 | 4 | Thêm: NIST PQC algorithms (CRYSTALS-Kyber, CRYSTALS-Dilithium) |
| 12 | Bảo mật ứng dụng Web & OWASP | 3 | 4 | Thay CSE122: Burp Suite, OWASP Top 10, Bug Bounty methodology |
| 13 | An ninh mạng & Zero Trust Architecture | 3 | 5 | Nâng cấp CSE478: Zero Trust, SASE, Microsegmentation |
| 14 | Phân tích mã độc & AI-Assisted Reverse Engineering | 3 | 5 | Thêm: Ghidra, AI-assisted code analysis, Sandbox automation |
| 15 | Quản lý ATTT & Frameworks | 3 | 5 | Thêm: NIST CSF 2.0, ISO 27001, AI Governance |
| 16 | Lập trình an toàn & DevSecOps | 3 | 5 | Kết hợp CSE473 + DevSecOps: SAST/DAST, CI/CD Security |
| 17 | **AI ứng dụng trong An ninh mạng** | 3 | 6 | **Môn mới BẮT BUỘC** — ML cho Log Analysis, Anomaly Detection, SIEM AI |
| 18 | Thiết kế mạng & Cloud Security | 3 | 6 | Gộp CSE420 + Cloud: Zero Trust Network, AWS/Azure Security |
| 19 | Đánh giá AN toàn mạng & Automated Pentest | 3 | 6 | Nâng cấp CSE495: thêm Metasploit automation, AI Pentest tools |

---

### Khối IV: Chuyên sâu — tự chọn (15 TC, chọn 1 track)

**Track A — AI security & LLM defense (hoàn toàn mới):**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 20 | **Bảo mật Hệ thống AI & LLM Security** | 3 | 6 |
| 21 | **Prompt Injection & Adversarial AI Attacks** | 3 | 6 |
| 22 | **AI-Powered Threat Intelligence** | 3 | 7 |
| 23 | Quản trị mạng & Tự động hóa bảo mật | 3 | 7 |
| 24 | Chuyên đề AN ninh mạng (AI era) | 3 | 7 |

**Track B — Red team & offensive security:**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 20 | Red team operations | 3 | 6 |
| 21 | Kỹ thuật liên mạng & exploitation nâng cao | 3 | 6 |
| 22 | Social engineering & human layer security | 3 | 7 |
| 23 | Kết nối vạn vật & IoT security | 3 | 7 |
| 24 | Chuỗi khối & blockchain security | 3 | 7 |

**Track C — Blue team & forensics:**

| TT | Học phần | TC | HK |
|----|----------|----|----|
| 20 | Điều tra số & Digital Forensics nâng cao | 3 | 6 |
| 21 | Incident Response & Threat Hunting | 3 | 6 |
| 22 | Security Operations Center (SOC) | 3 | 7 |
| 23 | Mã hóa dữ liệu & Privacy Engineering | 3 | 7 |
| 24 | Phân tích dữ liệu mạng & Network Intelligence | 3 | 7 |

---

### Khối V: Thực tập & đồ án (14 TC)

| TT | Học phần | TC | HK | Yêu cầu mới |
|----|----------|----|----|------------|
| 25 | Thực tập doanh nghiệp | 4 | 8 | Thực tập tại: SOC, CERT, Security firm, hoặc Red Team nội bộ |
| 26 | Đồ án tốt nghiệp | 10 | 8 | Bắt buộc chọn 1 trong: CTF writeup (độc đáo) / Security tool mới / Vulnerability discovery / AI Security research + Oral Defense |

---

## VI. Đổi mới phương pháp đánh giá

| Loại môn | Phương pháp kiểm tra mới |
|----------|------------------------|
| Môn tấn công (Pentest, Exploit) | CTF-based assessment: Sinh viên giải challenge trong thời gian giới hạn trên Cyber Range |
| Môn phòng thủ (SIEM, Forensics) | Cung cấp dataset log thật (ẩn danh), SV phải phát hiện tấn công và viết incident report |
| Môn AI Security | Demo tấn công Prompt Injection + giải pháp phòng thủ |
| Đồ án | Hội đồng gồm GV + Security expert doanh nghiệp; chấm theo Impact + Novelty + Technical depth |

---

## VII. Định hướng nghề nghiệp đầu ra (2030)

| Vị trí | Kỹ năng cốt lõi từ CTĐT mới |
|--------|-----------------------------|
| AI Security Engineer | Bảo vệ hệ thống LLM, chống Prompt Injection |
| SOC Analyst (AI-augmented) | SIEM + AI Anomaly Detection + Threat Hunting |
| Penetration Tester | Automated Pentest + Manual exploitation |
| DevSecOps Engineer | CI/CD Security, Container security |
| Cloud Security Engineer | AWS/Azure/GCP Security, IAM, Zero Trust |

---

## VIII. Kết luận và kiến nghị

An ninh mạng đang bước vào giai đoạn **"AI vs AI"** — kẻ tấn công dùng AI để tìm lỗ hổng, người bảo vệ phải dùng AI để phát hiện. Sinh viên ANM không được đào tạo AI là một thiếu sót nghiêm trọng trong năm 2026.

Đặc biệt, **bảo mật cho các hệ thống AI (AI Security / LLM Security)** là một lĩnh vực cực kỳ mới mẻ, khát nhân lực và trả lương rất cao — đây là cơ hội chiến lược đặc biệt mà chương trình ANM có thể đi đầu tại Việt Nam nếu hành động ngay.

**Kiến nghị cụ thể:**
1. **Loại bỏ** Phát triển ứng dụng Web cơ bản (CSE122) và thay bằng **Web Application Security & OWASP**.
2. **Thay CSE481** bằng **DevSecOps & Secure Supply Chain**.
3. **Loại khỏi track tự chọn ANM:** Lập trình Windows (CSE383), Java ứng dụng (CSE114).
4. **Bổ sung bắt buộc:** AI ứng dụng trong An ninh mạng (Môn mới).
5. **Bổ sung 1 track tự chọn hoàn toàn mới:** AI Security & LLM Defense.
6. **Áp dụng CTF-based assessment** cho các môn thực hành tấn công/phòng thủ.

---
*Tài liệu tham khảo: NIST Cybersecurity Framework 2.0; OWASP Top 10 2025; ISC2 Cybersecurity Workforce Study 2025; MITRE ATT&CK Framework v15; CISA AI Cybersecurity Collaboration Playbook 2024.*
