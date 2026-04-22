Vibe Coding đã chết? Sự chuyển dịch sang “Agentic Engineering” trong kỷ nguyên AI

Một năm trước, Andrej Karpathy đưa ra một thuật ngữ khiến cộng đồng lập trình xôn xao: Vibe Coding
Ông mô tả nó rất đơn giản:
“Một kiểu lập trình nơi bạn gần như quên rằng code tồn tại, và chỉ nói cho AI biết mình muốn gì.”
Ngay lập tức, internet bùng nổ.
Video ở khắp nơi:
“Build SaaS in a weekend”
“No-code with AI”
“Just prompt it”
Các công cụ như ChatGPT, Claude hay GitHub Copilot, Cursor,v.v khiến việc viết phần mềm trở nên cực kỳ dễ dàng.
Một founder có thể build MVP.
Một marketer có thể tạo landing page.
Một designer có thể thử nghiệm ý tưởng sản phẩm.
Ý tưởng → sản phẩm chỉ trong vài giờ.
Đó là điều chưa từng xảy ra trong lịch sử phần mềm.
Nhưng sau khoảng một năm, nhiều người bắt đầu nhận ra một vấn đề.
AI giúp bạn viết code cực nhanh. Nhưng nó không giúp bạn hiểu code đó.
Vì sao Vibe Coding lại hấp dẫn?
Câu trả lời rất đơn giản:
Tốc độ.
Nếu trước đây bạn cần:
vài tuần để build prototype
vài tháng để build sản phẩm
thì giờ đây bạn có thể:
tạo UI
viết API
kết nối database
deploy app
chỉ bằng prompt.
Ví dụ:
“Tạo một ứng dụng flashcard học từ vựng với React và lưu dữ liệu vào database.”
AI sẽ tạo ra gần như toàn bộ hệ thống.
Bạn chỉ việc chạy nó.
Và trong vài tuần đầu tiên, mọi thứ hoạt động rất tốt.
Rồi đến tháng thứ ba
Ban đầu bạn chỉ sửa một bug nhỏ.
Sau đó một feature khác đột nhiên bị hỏng.
Bạn nhờ AI sửa tiếp.
Rồi một chỗ khác lại phát sinh lỗi.
Cảm giác giống như cứ sửa xong một lỗi thì chỗ khác lại xuất hiện lỗi mới.
Hệ thống dần trở thành một vòng lặp sửa lỗi không hồi kết.
Bạn không còn phát triển sản phẩm nữa.
Bạn chỉ đang đuổi theo bug.
Điều này xảy ra rất thường xuyên với những dự án được build hoàn toàn bằng Vibe Coding.
Có ba lý do chính dẫn đến việc này
1. Context Collapse
AI rất mạnh.
Nhưng nó không nhìn thấy toàn bộ codebase của bạn cùng lúc.
Nó chỉ thấy phần code bạn paste vào prompt.
Sau vài tháng:
nhiều feature mới
nhiều bug fix
nhiều refactor
AI dần mất dấu các quyết định trước đó.
Kết quả:
Code mới bắt đầu mâu thuẫn với code cũ.
2. Không có System Design
Trong Vibe Coding, AI thường tự quyết định:
thư viện nào được dùng
cách tổ chức code
cách lưu dữ liệu
Trong ngắn hạn, điều này rất tiện.
Nhưng sau vài tháng, codebase trở thành:
nhiều pattern khác nhau
nhiều cách xử lý dữ liệu khác nhau
nhiều logic khó hiểu
Không ai thực sự biết hệ thống hoạt động thế nào.
3. Cognitive Debt
Chúng ta quen với khái niệm Tech Debt.
Nhưng thời AI có thêm một thứ gọi là:
Cognitive Debt
Đó là chi phí trí óc để hiểu code do AI tạo ra.
Ví dụ:
Bạn mở một file.
AI đã viết 600 dòng code.
Bạn chỉ muốn sửa một bug nhỏ.
Nhưng để sửa bug đó, bạn phải:
đọc toàn bộ logic
hiểu cách AI tổ chức code
lần lại các quyết định cũ
AI viết code nhanh hơn bạn.
Nhưng bạn vẫn là người phải hiểu nó.
Next step: Agentic Engineering!!!!
Sau làn sóng Vibe Coding, nhiều developer bắt đầu chuyển sang một cách tiếp cận khác: Agentic Engineering
Sự khác biệt rất đơn giản.
Vibe Coding: AI quyết định cách build hệ thống.
Agentic Engineering: Bạn quyết định hệ thống. AI giúp bạn thực hiện.
Workflow của Agentic Engineering
Những người dùng AI hiệu quả thường làm 4 bước.
1. Viết rõ yêu cầu trước
Ví dụ:
tính năng này làm gì
dữ liệu được lưu ở đâu
trường hợp lỗi xử lý như thế nào
Chỉ vài gạch đầu dòng cũng đủ.
2. Chia task nhỏ
Thay vì:
“Build authentication system”
Hãy nói:
“Tạo API reset password với token hết hạn sau 15 phút.”
Task nhỏ → AI ít sai hơn.
3. Review code AI viết
Không cần đọc từng dòng.
Nhưng bạn nên hiểu:
logic chính là gì
data flow như thế nào
4. Test trước khi deploy
Kiểm tra:
đăng ký
đăng nhập
thanh toán
lưu dữ liệu
AI giúp viết code.
Nhưng testing vẫn là trách nhiệm của bạn.
Vai trò của developer đang thay đổi
Trước đây:
Developer = người viết code.
Bây giờ:
Developer = người thiết kế hệ thống + điều khiển AI.
AI không thay thế developer.
Nó thay thế developer không biết mình đang xây gì.
Kết luận
Vibe Coding không sai.
Nó là cách nhanh nhất để:
build prototype
thử ý tưởng
tạo MVP
Nhưng nếu bạn muốn sản phẩm:
có người dùng thật
chạy ổn định
tồn tại nhiều năm
thì bạn cần bước tiếp theo.
Agentic Engineering
Nơi AI vẫn viết phần lớn code.
Nhưng bạn vẫn là người kiểm soát hệ thống.
AI giúp bạn build phần mềm nhanh hơn.
Nhưng hiểu hệ thống vẫn là trách nhiệm của bạn.