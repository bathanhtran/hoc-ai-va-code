# Học AI & Code — 6 app HTML

Sáu app nhỏ, mỗi app chỉ là **1 file HTML duy nhất**
(HTML + CSS + JavaScript, chú thích tiếng Việt). Không cần cài đặt, không cần
máy chủ: tải file về, nhấp đúp mở bằng trình duyệt là chạy. Bốn app đầu làm
trong ngày 2026-10-24, hai app sau thêm ngày 2026-10-25. Lưu ý: app Thời
Tiết cần mạng vì gọi API Open-Meteo, các app còn lại chạy được cả khi tắt mạng.

## Danh sách app

| App | File | Dùng để làm gì |
| --- | --- | --- |
| Prompt Builder 4 phần (v2) | `prompt-builder/prompt-builder.html` | Nhập Vai trò / Nhiệm vụ / Ngữ cảnh / Định dạng rồi ghép thành prompt hoàn chỉnh; có kho yêu cầu theo 6 mục đích, chọn giọng văn, độ dài và 5 quy tắc chất lượng tự thêm. |
| Bot Quét Bảo Vệ Code | `secret-scanner/secret-scanner.html` | Quét code ngay trong trình duyệt (không gửi code đi đâu), tìm API key, token, mật khẩu viết thẳng trong code. Kết quả che mờ key, chỉ giữ 6 ký tự đầu + 4 ký tự cuối. |
| Flashcard Học AI | `flashcard/flashcard-hoc-ai.html` | 10 thẻ thuật ngữ AI bằng tiếng Việt dễ hiểu, lật thẻ, đánh dấu Đã thuộc / Chưa thuộc, xáo trộn, lọc thẻ chưa thuộc, tự thêm thẻ. Tiến độ lưu bằng localStorage trên máy của bạn. |
| Quản Lý Chi Tiêu (v2) | `quan-ly-chi-tieu/quan-ly-chi-tieu.html` | Nhập thu / chi theo ngày và danh mục, tự tính tổng thu / tổng chi / số dư theo tháng, biểu đồ chi theo danh mục, hạn mức ngân sách (xanh / vàng / đỏ), sửa giao dịch, tìm kiếm, so sánh với tháng trước, Xuất / Nhập file JSON. |
| App Thời Tiết | `thoi-tiet/thoi-tiet.html` | Gõ tên thành phố → xem nhiệt độ hiện tại, cảm giác thực, độ ẩm, gió và dự báo 7 ngày qua API Open-Meteo miễn phí (cần mạng, không cần key). |
| Trading Bot Demo | `trading-bot-demo/trading-bot-demo.html` | Mô phỏng bot giao dịch bằng tiền ảo: tín hiệu EMA theo 7 khung giờ, cắt lỗ / chốt lời chỉnh được, tạm dừng / đặt lại demo — học cách bot vận hành, không giao dịch thật, không có ô nhập API key. |

## Cách chạy

1. Mở thư mục của app muốn dùng.
2. Nhấp đúp file `.html` để mở bằng Chrome / Edge / Firefox.

Hoặc chạy trực tiếp trên web (repo đã bật GitHub Pages): mở link `https://bathanhtran.github.io/hoc-ai-va-code/<thư-mục>/<file>.html` tương ứng với từng app trong bảng trên.

## Mang dữ liệu sang máy khác

Dữ liệu lưu bằng localStorage chỉ nằm trên trình duyệt của từng máy, không đi
theo file HTML. Với app Quản Lý Chi Tiêu, dùng nút **Xuất file** để tải file
JSON backup, sang máy khác bấm **Nhập file** là khôi phục được.

## Lưu ý về app Bot Quét

Đoạn code mẫu "đầy lỗi" trong app chứa các key **giả**, được ghi chú rõ ràng
trong code là key bịa ra để thử bot — không dùng được ở đâu cả. Đừng bao giờ
dán key thật của bạn vào code rồi đăng lên GitHub: việc đầu tiên khi key thật
đã lộ là thu hồi key đó và tạo key mới.
