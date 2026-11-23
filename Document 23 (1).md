Bước 1: Phân tích lỗi (Tác hại khi khai báo biến số lộn xộn)

Việc trộn lẫn hai cú pháp `[language]` và `{audience}` gây trở ngại lớn trong quy trình thiết kế prompt và tự động hóa vì các lý do sau:

**Khó tự động hóa bằng script hoặc template engine:** Khi chạy hàng loạt qua code, regex, hoặc các công cụ tự động hóa, hệ thống thường quy ước một cú pháp cố định (ví dụ chỉ tìm `{{bien}}` hoặc `[BIEN]`). Khai báo không thống nhất khiến trình thay thế bỏ sót biến, để lộ ký tự lạ hoặc báo lỗi cú pháp.

**Dễ nhầm lẫn giữa "biến cần thay thế" và "văn bản bình thường":** Ngoặc vuông `[...]` đôi khi được dùng để ghi chú hướng dẫn cho người đọc, còn ngoặc nhọn `{...}` đôi khi xuất hiện trong văn bản mẫu, code hoặc cấu trúc dữ liệu. Không quy ước rõ ràng khiến người soạn hoặc người dùng sau dễ điền nhầm hoặc quên thay giá trị.

**Thiếu tính chuẩn hóa và khó bảo trì:** Dùng lẫn lộn ngôn ngữ (tiếng Anh lẫn tiếng Việt), viết hoa/thường không nhất quán khiến bộ Prompt Library khó đọc, khó kiểm soát khi mở rộng thêm nhiều biến số hoặc chia sẻ cho người khác dùng chung.

Bước 2: Prompt mẫu đã đồng bộ biến số

Plaintext

`Hãy viết một bài chia sẻ về Quản trị Prompt & System Instructions bằng ngôn ngữ [NGÔN_NGỮ]. Dành cho đối tượng [ĐỐI_TƯỢNG].` 

Kết quả chạy thử sau khi điền dữ liệu thực tế

**Giá trị thay thế:** `[NGÔN_NGỮ]` = `Tiếng Việt`, `[ĐỐI_TƯỢNG]` = `sinh viên năm nhất ngành Công nghệ Thông tin mới bắt đầu học về AI`

**Prompt đã điền dữ liệu:** *"Hãy viết một bài chia sẻ về Quản trị Prompt & System Instructions bằng ngôn ngữ Tiếng Việt. Dành cho đối tượng sinh viên năm nhất ngành Công nghệ Thông tin mới bắt đầu học về AI."*

**Kết quả phản hồi:**

**Quản trị Prompt & System Instructions: Bắt đầu từ đâu cho người mới?**

Nếu bạn mới làm quen với AI, hẳn có lúc bạn thấy AI trả lời lan man, sai trọng tâm hoặc thiếu nhất quán giữa các lần hỏi. Trong thực tế làm việc với AI, hai khái niệm giúp bạn kiểm soát điều này tốt hơn là **Quản trị Prompt (Prompt Management)** và **System Instructions**.

**Prompt là gì và tại sao cần quản trị?** Prompt là lời hướng dẫn bạn đưa cho AI. Khi mới học, nhiều người viết prompt ngẫu hứng rồi tự hỏi sao lần thì hay, lần thì dở. Quản trị prompt nghĩa là bạn biết cách viết câu lệnh rõ ràng, có bối cảnh, có yêu cầu đầu ra cụ thể và lưu lại những mẫu hiệu quả để dùng lại khi cần—giống như việc bạn lưu lại các đoạn code mẫu hoặc ghi chú học tập có cấu trúc thay vì gõ lại từ đầu.

**System Instructions đóng vai trò gì?** Nếu prompt thông thường giống như câu hỏi hoặc yêu cầu cho từng tình huống cụ thể, thì **System Instructions** giống như "bộ quy tắc nền" thiết lập sẵn cho AI ngay từ đầu. Ở đó, bạn có thể định hình vai trò (ví dụ: giải thích dễ hiểu cho người mới), giọng văn, phạm vi trả lời hoặc các quy tắc bắt buộc để AI giữ sự ổn định trong suốt quá trình làm việc.

**Người mới bắt đầu nên luyện tập thế nào?**

**Đừng viết câu lệnh quá mơ hồ:** Thay vì chỉ nói *"Giải thích về AI"*, hãy nêu rõ mục đích và mức độ chi tiết bạn cần.

**Tách bạch quy tắc chung và yêu cầu riêng:** Đưa các nguyên tắc lặp lại vào phần hướng dẫn chung, giữ phần câu hỏi cho từng bài tập cụ thể.

**Thử, quan sát và sửa dần:** Mỗi lần AI trả lời chưa sát ý, hãy xem mình thiếu thông tin hay thiếu ràng buộc ở chỗ nào rồi chỉnh lại prompt.

Làm chủ cách viết và quản lý prompt ngay từ sớm sẽ giúp bạn học nhanh hơn, làm việc với AI chủ động hơn và tránh phụ thuộc vào những câu trả lời mang tính may rủi.


