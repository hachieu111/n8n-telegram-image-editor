# 🤖 Hệ Thống Chỉnh Sửa Ảnh Tự Động (n8n + Telegram + Stability AI)

**Đồ án giữa kỳ - Môn: PYTHON**
- **Sinh viên thực hiện:** Hoàng Hạc Hiếu
- **Mã sinh viên:** 123000831

## 🎯 Mục tiêu dự án
Xây dựng một quy trình tự động hóa (Workflow) trên nền tảng n8n với chức năng:
1. Nhận yêu cầu (bao gồm Hình ảnh gốc + Lệnh chỉnh sửa/Caption) từ người dùng qua **Telegram Bot**.
2. Xử lý làm sạch tên file để tránh lỗi hệ thống.
3. Gửi dữ liệu qua API của **Stability AI (Stable Image Ultra)** để chỉnh sửa ảnh theo công nghệ Diffusion.
4. Tự động lưu trữ kết quả đầu ra vào thư mục **Google Drive** với định dạng tên chuẩn hóa.
5. Gửi thông báo hoàn thành kèm tên file về lại cho người dùng.

## 🛠️ Công nghệ sử dụng
- **n8n:** Nền tảng Workflow Automation (Core).
- **Telegram API:** Nhận/Gửi tin nhắn & file (UI).
- **Stability AI (Ultra v2beta):** Image-to-Image Generation (AI Engine).
- **Google Drive API:** Cloud Storage.
- **JavaScript:** Regex làm sạch dữ liệu.

## 📂 Cấu trúc Repository
- `workflow_bai_giua_ky.json`: File chứa toàn bộ mã nguồn của các Node trên n8n.
- `README.md`: Tài liệu hướng dẫn này.

## 🚀 Hướng dẫn cài đặt (Dành cho Giảng viên test)
1. Tải file `workflow_bai_giua_ky.json`.
2. Trong giao diện n8n mới, bấm *Import from File* hoặc Copy nội dung file dán thẳng vào màn hình n8n.
3. Cấp quyền (Credentials) cho 3 dịch vụ: Telegram, Google Drive và Stability AI API.
4. Kích hoạt Workflow và gửi tin nhắn qua bot Telegram.
