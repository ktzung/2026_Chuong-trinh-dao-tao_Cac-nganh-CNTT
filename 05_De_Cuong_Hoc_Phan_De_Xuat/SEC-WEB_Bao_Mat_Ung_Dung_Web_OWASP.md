# SEC-WEB: Bảo mật ứng dụng Web & OWASP (Web Application Security & OWASP)

**Mã học phần đề xuất:** SEC-WEB  
**Số tín chỉ:** 3 TC (30 tiết lý thuyết + 15 tiết thực hành tích hợp)  
**Học kỳ gợi ý:** Học kỳ 4 (năm 2) — thay thế CSE122 cho ngành ANM  
**Học phần tiên quyết:** Mạng máy tính (CSE489), Cơ sở dữ liệu (CSE484), Lập trình hướng đối tượng (CSE116)  
**Áp dụng cho ngành:** ANM (bắt buộc, thay thế CSE122)  
**Công cụ bắt buộc:** Burp Suite Community Edition, OWASP WebGoat, TryHackMe/HackTheBox (free tier), Kali Linux (VM)

---

## I. Mô tả học phần

Web là mặt trận tấn công chủ yếu trong an ninh mạng hiện đại. OWASP Top 10 — danh sách 10 lỗ hổng web nguy hiểm nhất — đều là các lỗ hổng ở tầng ứng dụng web. Một chuyên gia ANM không hiểu web là một chuyên gia ANM không hoàn chỉnh.

Học phần này **không dạy sinh viên ANM xây dựng website** — đó là việc của ngành KTPM. Thay vào đó, học phần dạy sinh viên **tấn công và phòng thủ** trên nền tảng web: tìm lỗ hổng, khai thác chúng trong môi trường lab an toàn, và quan trọng hơn — biết cách vá chúng.

**Triết lý cốt lõi:** *"Để bảo vệ một hệ thống web, bạn phải biết cách tấn công nó trước."*

> **Lưu ý đạo đức và pháp lý:** Toàn bộ thực hành tấn công trong học phần này được thực hiện trên các hệ thống lab được thiết kế để bị tấn công (OWASP WebGoat, DVWA, TryHackMe). Tuyệt đối không áp dụng kỹ thuật tấn công lên hệ thống thực tế khi chưa có sự cho phép bằng văn bản. Vi phạm sẽ bị đình chỉ học phần và xử lý theo quy định nhà trường.

---

## II. Chuẩn đầu ra

### Kiến thức
- **CĐR 1:** Giải thích kiến trúc ứng dụng web từ góc độ bảo mật: HTTP/HTTPS, session management, authentication flow, API endpoints — và điểm yếu tiềm ẩn của từng thành phần.
- **CĐR 2:** Mô tả chi tiết OWASP Top 10 (2021): nguyên nhân gốc rễ, cách khai thác, và biện pháp phòng chống của từng loại lỗ hổng.
- **CĐR 3:** Phân tích sự khác biệt giữa các loại tấn công web: client-side (XSS, CSRF) vs. server-side (SQLi, SSRF, XXE) vs. authentication attacks.
- **CĐR 4:** Mô tả quy trình Bug Bounty và Responsible Disclosure — cách báo cáo lỗ hổng một cách có đạo đức.

### Kỹ năng
- **CĐR 5:** Sử dụng Burp Suite để intercept, modify và replay HTTP requests; thiết lập proxy, sử dụng Repeater, Intruder và Scanner.
- **CĐR 6:** Phát hiện và khai thác (trong môi trường lab) các lỗ hổng OWASP Top 10: SQL Injection, XSS (Reflected/Stored/DOM), CSRF, IDOR, SSRF, XXE, Broken Authentication.
- **CĐR 7:** Thực hiện web application penetration testing theo phương pháp OWASP Testing Guide: reconnaissance → scanning → exploitation → reporting.
- **CĐR 8:** Viết báo cáo lỗ hổng bảo mật chuyên nghiệp: mô tả lỗ hổng, bằng chứng khai thác (PoC), đánh giá mức độ nghiêm trọng (CVSS), và khuyến nghị vá lỗi.
- **CĐR 9:** Sử dụng AI agent để tự động hóa một phần quy trình pentest web: tự động dò quét endpoint, fuzz parameter, phân tích response.

### Thái độ
- **CĐR 10:** Đạo đức nghề nghiệp: hiểu rõ ranh giới giữa ethical hacking (có phép) và tấn công bất hợp pháp; luôn có văn bản ủy quyền trước khi pentest.
- **CĐR 11:** Tư duy attacker: luôn đặt câu hỏi "Nếu tôi là kẻ tấn công, tôi sẽ tấn công điểm nào?" khi thiết kế hoặc review hệ thống.

---

## III. Nội dung theo tuần

### Giai đoạn 1: Nền tảng Web Security (tuần 1–3)

**Tuần 1 — Web từ góc nhìn của kẻ tấn công**
- Nội dung: HTTP/HTTPS deep dive: headers, cookies, sessions, CORS. Cách trình duyệt xử lý request. Same-Origin Policy và tại sao nó tồn tại. Burp Suite setup: cài đặt, cấu hình proxy, intercept request đầu tiên.
- Thực hành: Dùng Burp Suite để "mổ xẻ" một ứng dụng web thực tế (WebGoat): xem tất cả request/response, tìm các endpoint ẩn, phân tích cookie và session token.
- Checkpoint: Vẽ sơ đồ kiến trúc của WebGoat từ góc nhìn attacker: liệt kê tất cả endpoint, parameter, và điểm nhập dữ liệu tiềm năng.

**Tuần 2 — OWASP Top 10: tổng quan và phân loại**
- Nội dung: OWASP Top 10 (2021) overview: A01 Broken Access Control, A02 Cryptographic Failures, A03 Injection, A04 Insecure Design, A05 Security Misconfiguration, A06 Vulnerable Components, A07 Auth Failures, A08 Software Integrity Failures, A09 Logging Failures, A10 SSRF. CVSS scoring system.
- Thực hành: Phân tích 3 case study thực tế (breach reports): xác định lỗ hổng OWASP nào đã bị khai thác, thiệt hại gây ra, và cách phòng chống.
- Checkpoint: Cho một ứng dụng web mô tả, sinh viên phải xác định ít nhất 5 lỗ hổng OWASP tiềm năng và giải thích lý do.

**Tuần 3 — Reconnaissance & Information Gathering**
- Nội dung: Passive reconnaissance: OSINT, Google Dorks, Shodan, Wayback Machine. Active reconnaissance: directory enumeration (Gobuster, ffuf), subdomain enumeration, technology fingerprinting (Wappalyzer, WhatWeb). Robots.txt, sitemap.xml, .git exposure.
- Thực hành: Thực hiện full reconnaissance trên một target lab (TryHackMe room). Tìm hidden directories, exposed files, technology stack, và potential attack vectors.
- Checkpoint: Báo cáo reconnaissance: liệt kê tất cả thông tin thu thập được và đánh giá mức độ nguy hiểm của từng thông tin.

---

### Giai đoạn 2: OWASP Top 10 — Tấn công & Phòng thủ (tuần 4–10)

**Tuần 4 — SQL Injection: vua của các lỗ hổng**
- Nội dung: SQL Injection mechanics: tại sao xảy ra, các loại (Classic, Blind, Time-based, Out-of-band). Manual SQLi với Burp Suite. Automated SQLi với sqlmap. Phòng chống: Parameterized queries, Stored procedures, Input validation, WAF.
- Thực hành: Khai thác SQLi trên DVWA (Damn Vulnerable Web Application) — từ basic đến blind SQLi. Sau đó: xem source code của ứng dụng dễ bị tấn công và viết lại đoạn code đó theo cách an toàn.
- Checkpoint: Khai thác thành công SQLi để dump toàn bộ user table. Sau đó fix lỗ hổng và chứng minh attack không còn hoạt động.

**Tuần 5 — Cross-Site Scripting (XSS): tấn công phía client**
- Nội dung: XSS types: Reflected, Stored, DOM-based. XSS payloads: cookie stealing, keylogging, phishing. BeEF framework cơ bản. Content Security Policy (CSP). Output encoding. HttpOnly và Secure cookie flags.
- Thực hành: Khai thác Stored XSS để steal session cookie của admin user (trong lab). Sau đó implement CSP và output encoding để ngăn chặn.
- Checkpoint: Demo: inject XSS payload → steal cookie → hijack session. Sau đó demo: với CSP đúng, payload không còn hoạt động.

**Tuần 6 — Authentication & Session Attacks**
- Nội dung: Broken Authentication: weak passwords, credential stuffing, brute force. Session fixation, session hijacking. JWT vulnerabilities: alg:none, weak secret, algorithm confusion. OAuth2 misconfigurations. Multi-factor authentication bypass.
- Thực hành: Brute force login với Burp Intruder. Khai thác JWT với alg:none vulnerability. Sau đó implement proper authentication: bcrypt, rate limiting, account lockout, secure JWT.
- Checkpoint: Crack một JWT token có weak secret. Sau đó implement JWT với proper signing và expiration.

**Tuần 7 — Broken Access Control & IDOR**
- Nội dung: Insecure Direct Object Reference (IDOR): truy cập tài nguyên của user khác bằng cách thay đổi ID. Horizontal vs. Vertical privilege escalation. Path traversal. Forced browsing. Proper authorization implementation.
- Thực hành: Khai thác IDOR để xem thông tin của tất cả users trong hệ thống lab. Khai thác path traversal để đọc file `/etc/passwd`. Sau đó implement proper authorization checks.
- Checkpoint: Tìm và khai thác ít nhất 3 IDOR vulnerabilities trong một ứng dụng lab. Viết fix cho từng lỗ hổng.

**Tuần 8 — Server-Side Attacks: SSRF, XXE, Command Injection**
- Nội dung: Server-Side Request Forgery (SSRF): tấn công internal services qua server. XML External Entity (XXE): đọc file hệ thống qua XML parser. Command Injection: thực thi lệnh hệ thống qua input. OS Command Injection vs. Code Injection.
- Thực hành: Khai thác SSRF để truy cập AWS metadata endpoint (169.254.169.254) trong môi trường lab. Khai thác XXE để đọc `/etc/passwd`. Sau đó implement input validation và disable external entity processing.
- Checkpoint: Demo SSRF attack chain: SSRF → access internal service → extract sensitive data. Sau đó demo fix.

**Tuần 9 — Security Misconfiguration & Vulnerable Components**
- Nội dung: Common misconfigurations: default credentials, exposed admin panels, verbose error messages, directory listing, unnecessary services. Dependency scanning: npm audit, pip-audit, OWASP Dependency-Check. CVE database và NVD. Software composition analysis (SCA).
- Thực hành: Audit một ứng dụng web cho security misconfigurations. Chạy dependency scan — tìm và update tất cả vulnerable dependencies. Tìm exposed admin panel và default credentials.
- Checkpoint: Báo cáo: liệt kê tất cả misconfiguration tìm được, CVSS score của từng lỗ hổng, và remediation steps.

**Tuần 10 — AI-Assisted Web Penetration Testing**
- Nội dung: Dùng AI để tăng tốc pentest: tự động generate payloads, phân tích response patterns, tìm hidden parameters. LLM để phân tích source code tìm lỗ hổng. Tự động hóa reconnaissance với Python scripts + AI. Giới hạn của AI trong pentest (false positives, context understanding).
- Thực hành: Viết Python script dùng LLM API để tự động phân tích HTTP responses và đề xuất potential vulnerabilities. So sánh kết quả với manual testing.
- Checkpoint: Script phải tìm được ít nhất 3 trong 5 lỗ hổng được cài sẵn trong target lab.

---

### Giai đoạn 3: Pentest Methodology & Reporting (tuần 11–13)

**Tuần 11 — Web Application Pentest Methodology**
- Nội dung: OWASP Testing Guide (OTG) methodology. Pentest phases: Planning → Reconnaissance → Scanning → Exploitation → Post-exploitation → Reporting. Scope definition và Rules of Engagement. Evidence collection (screenshots, request/response logs).
- Thực hành: Thực hiện full pentest theo OTG methodology trên một ứng dụng lab mới (chưa từng thấy). Ghi lại toàn bộ quá trình theo chuẩn.
- Checkpoint: Pentest report draft: phải có ít nhất 5 findings với evidence đầy đủ.

**Tuần 12 — Viết báo cáo pentest chuyên nghiệp**
- Nội dung: Cấu trúc báo cáo pentest: Executive Summary, Technical Findings, Risk Rating, Remediation Recommendations. CVSS scoring. Proof of Concept (PoC) documentation. Responsible Disclosure process. Bug Bounty platforms: HackerOne, Bugcrowd.
- Thực hành: Hoàn thiện báo cáo pentest từ tuần 11. Peer review: nhóm A review báo cáo của nhóm B — đánh giá tính rõ ràng, đầy đủ và chuyên nghiệp.
- Checkpoint: Báo cáo phải đủ chất lượng để gửi cho một doanh nghiệp thực tế — không phải báo cáo học thuật.

**Tuần 13 — CTF Practice & Competitive Security**
- Nội dung: Capture The Flag (CTF) format. Web security CTF challenges. CTF platforms: HackTheBox, TryHackMe, PicoCTF. Writeup culture — tại sao viết writeup quan trọng cho career.
- Thực hành: Giải ít nhất 3 web security CTF challenges trên TryHackMe hoặc HackTheBox. Viết writeup chi tiết cho 1 challenge.
- Checkpoint: Nộp flag + writeup. Writeup phải giải thích rõ ràng từng bước tấn công.

---

### Giai đoạn 4: Đồ án & bảo vệ (tuần 14–15)

**Tuần 14–15 — Đồ án: Full Web Application Pentest**

Yêu cầu: Thực hiện pentest toàn diện trên một ứng dụng web lab được cung cấp (chưa từng thấy trước đó). Nộp báo cáo pentest chuyên nghiệp.

**Tiêu chí đánh giá báo cáo:**
- Số lượng và chất lượng findings (không phải nhiều là tốt — phải có evidence)
- Độ chính xác của CVSS scoring
- Chất lượng PoC (reproducible, clear steps)
- Chất lượng remediation recommendations (cụ thể, khả thi)
- Tính chuyên nghiệp của báo cáo

**Format bảo vệ (20 phút/sinh viên):**
- 5 phút: Trình bày Executive Summary (không đọc slide).
- 5 phút: Demo live một finding quan trọng nhất.
- 10 phút: Trả lời câu hỏi kỹ thuật.

Câu hỏi mẫu:
> *"Em tìm được SQLi ở endpoint này. Nếu database là PostgreSQL thay vì MySQL, payload của em có thay đổi không?"*  
> *"CVSS score của lỗ hổng này là 8.1. Em giải thích tại sao không phải 9.0 hay 7.0?"*  
> *"Nếu developer fix lỗ hổng bằng cách blacklist ký tự `'`, em có bypass được không?"*  
> *"Em đã dùng AI để hỗ trợ pentest như thế nào? AI đã sai ở đâu?"*

---

## IV. Phương pháp đánh giá

| Thành phần | Trọng số | Mô tả |
|---|---|---|
| Checkpoint hàng tuần (tuần 1–13) | 25% | 13 checkpoint, rubric rõ ràng |
| CTF challenges (tuần 13) | 15% | Số flag + chất lượng writeup |
| Đồ án — báo cáo pentest | 35% | Chất lượng findings, evidence, remediation |
| Oral defense | 25% | Giải thích kỹ thuật, trả lời câu hỏi về attack và defense |

> **Nguyên tắc đánh giá:** Điểm không dựa trên số lượng lỗ hổng tìm được mà dựa trên **chất lượng phân tích và báo cáo**. Một finding được mô tả rõ ràng, có PoC đầy đủ và remediation cụ thể tốt hơn 5 finding mơ hồ.

---

## V. Tài liệu & công cụ

### Tài liệu bắt buộc đọc
- [OWASP Top 10 (2021)](https://owasp.org/www-project-top-ten/) — đọc toàn bộ trước tuần 2
- [OWASP Testing Guide v4.2](https://owasp.org/www-project-web-security-testing-guide/) — tham khảo trong suốt học phần
- [PortSwigger Web Security Academy](https://portswigger.net/web-security) — miễn phí, lab thực hành tốt nhất

### Công cụ bắt buộc
- Burp Suite Community Edition (miễn phí)
- OWASP WebGoat (lab ứng dụng dễ bị tấn công)
- DVWA (Damn Vulnerable Web Application)
- Kali Linux (VM — có sẵn tất cả công cụ pentest)
- sqlmap (SQL injection automation)
- Gobuster / ffuf (directory enumeration)

### Nền tảng thực hành (miễn phí)
- [TryHackMe](https://tryhackme.com) — học theo lộ trình, có hướng dẫn
- [HackTheBox](https://hackthebox.com) — thực hành nâng cao
- [PortSwigger Web Security Academy](https://portswigger.net/web-security) — lab web security tốt nhất

---

## VI. Mapping với chứng chỉ nghề nghiệp quốc tế

| Chứng chỉ | Học phần chuẩn bị | Ghi chú |
|-----------|-------------------|---------|
| **CompTIA Security+** | SEC-WEB + An ninh mạng (CSE478) | Nền tảng bắt buộc cho mọi chuyên gia ANM |
| **CEH (Certified Ethical Hacker)** | SEC-WEB + Đánh giá ANM (CSE495) | Chứng chỉ pentest phổ biến nhất |
| **OSCP (Offensive Security Certified Professional)** | SEC-WEB + toàn bộ track Red Team | Chứng chỉ pentest uy tín nhất, yêu cầu cao |
| **eWPT (Web Application Penetration Tester)** | SEC-WEB | Chứng chỉ chuyên về web pentest |

> **Khuyến nghị:** Sinh viên ANM nên đặt mục tiêu đạt CompTIA Security+ trước khi tốt nghiệp và CEH trong vòng 1 năm sau tốt nghiệp.

---

## VII. So sánh với CSE122 (Phát triển ứng dụng Web cơ bản)

| Nội dung | CSE122 (cũ — cho ANM) | SEC-WEB (mới — cho ANM) |
|---|---|---|
| Mục tiêu | Xây dựng website | Tấn công và phòng thủ web |
| Công cụ | VS Code, HTML/CSS/JS | Burp Suite, Kali Linux, sqlmap |
| Thực hành | Làm form đăng ký | Khai thác SQLi, XSS, IDOR |
| Đầu ra | Website CRUD | Báo cáo pentest chuyên nghiệp |
| Liên quan đến ANM | Thấp | Rất cao — đây là core skill |

---

*Học phần SEC-WEB — Khoa CNTT, Trường Đại học Thủy lợi. Phiên bản 1.0 — Tháng 4/2026.*
