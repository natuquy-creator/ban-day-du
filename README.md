# VATM – Gói triển khai

## Thành phần
- `index.html`: ứng dụng HTML, giữ nguyên luồng xử lý hiện có; bổ sung nút tải mẫu Excel nhập nhanh.
- `VATM_MauNhapLieu_HoSoXuatCanh.xlsx`: mẫu nhập dữ liệu với sheet `MauNhapLieu` và `HuongDan`.
- `firebase.json`: cấu hình Firebase Hosting cơ bản.
- `.gitignore`: loại trừ tệp cấu hình cục bộ và dữ liệu tạm.

## Dùng mẫu Excel
1. Mở ứng dụng, chọn **Tải mẫu Excel** hoặc dùng file mẫu đi kèm ZIP.
2. Nhập dữ liệu vào sheet `MauNhapLieu`, giữ nguyên hàng tiêu đề.
3. Hai cột bắt buộc: **Họ và Tên**, **Số thẻ Đảng**.
4. Đăng nhập đúng tài khoản, chọn **Import Excel**, chọn file đã điền và kiểm tra thông báo kết quả.
5. Nên sao lưu dữ liệu trước khi nhập hàng loạt. Quyền User/Admin vẫn theo logic hiện có.

## Đưa lên GitHub
Giải nén ZIP, tạo repository hoặc mở repository hiện tại, chép các tệp trong thư mục này vào thư mục gốc, commit và push. Không đưa mật khẩu, khóa riêng hoặc tệp `.env` lên repository.

## Firebase Hosting
Cài Firebase CLI, đăng nhập và chọn đúng Firebase project của bạn:

```bash
npm install -g firebase-tools
firebase login
firebase use --add
firebase deploy --only hosting
```

Cấu hình Firebase project cụ thể không được nhúng vì cần dùng project ID thuộc tài khoản của bạn. Nếu ứng dụng đang dùng Firebase Authentication/Firestore, hãy giữ nguyên cấu hình dự án và quy tắc bảo mật hiện tại; không công khai thông tin bí mật.
