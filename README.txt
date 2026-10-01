VATM - Gói triển khai GitHub Pages

Cách đưa lên GitHub:
1. Giải nén gói ZIP.
2. Tạo repository GitHub mới (hoặc mở repository muốn triển khai).
3. Tải index.html và README.txt ở thư mục này lên thư mục gốc (root) của repository.
4. Vào Settings > Pages.
5. Chọn Deploy from a branch, chọn nhánh main và thư mục /(root), rồi Save.
6. Chờ GitHub Pages triển khai và mở đường dẫn Pages được cung cấp.

Lưu ý:
- index.html đã được cập nhật Firebase config cho dự án vatm-ban-goc.
- Cần cấu hình Firebase Realtime Database Rules an toàn trước khi dùng dữ liệu thật.
- Không bật quyền đọc/ghi công khai cho dữ liệu cá nhân.
- ZIP không chứa thông tin bí mật phía máy chủ; Firebase Web API key là cấu hình client, nhưng quyền truy cập phải được bảo vệ bằng Authentication và Database Rules.
- Nên sao lưu dữ liệu hiện có trước khi chuyển hệ thống.
