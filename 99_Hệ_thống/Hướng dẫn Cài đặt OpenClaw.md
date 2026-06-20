---
type: system
status: evergreen
created: 2026-06-20
tags:
  - System/Setup
  - OpenClaw
---

# 🤖 Hướng dẫn kết nối OpenClaw (AI Agent always-on)

_Biến vault thành Bộ não thứ hai **tự vận hành**: một AI Agent (OpenClaw) chạy nền, tự dọn dẹp/ôn tập theo lịch và nhắn tin hỏi ý kiến bạn qua Zalo/Telegram. Đây là điểm khác biệt lớn nhất của bộ khung này so với template chỉ-Obsidian._

> ⚠️ Bước này **tùy chọn**. Không có OpenClaw, vault vẫn dùng tốt 100% như một second brain Obsidian thường.

---

## 1. Mount vault vào container OpenClaw
Trong `docker-compose.yml` của OpenClaw, thêm vault vào volumes (đổi đường dẫn theo máy bạn):
```yaml
volumes:
  - "D:\\vietbrain:/mnt/secondbrain"
```
Trong container, vault nằm tại `/mnt/secondbrain`.

## 2. Điền thông tin vào AGENT.md
Mở [[AGENT|AGENT.md]] ở thư mục gốc, thay mọi chỗ `<...>`: tên agent, tên bạn, Zalo/Telegram ID, danh sách dự án/lĩnh vực.

## 3. Tạo Cron Job tự bảo trì
Tạo các cron job để agent tự quét vault và **gửi đề xuất qua Zalo trước khi làm** (không bao giờ tự xóa file). Ví dụ message cho từng job:

| Tần suất | Lịch (cron) | Nội dung message |
|---|---|---|
| **Tuần** | `0 9 * * 0` | "Quét `/mnt/secondbrain` theo `99_Hệ_thống/Review & Cleanup.md`. Liệt kê file Inbox cần xử lý, tag cần gộp/xóa, dự án cần lưu trữ, file đính kèm thừa. Gửi đề xuất qua Zalo, chờ duyệt." |
| **Tháng** | `30 9 1 * *` | "Quét các note `status: growing` tại `/mnt/secondbrain`, đề xuất note nào nên nâng lên `permanent`/`evergreen`. Hỏi ý kiến qua Zalo." |
| **Quý** | `0 10 1 */3 *` | "Rà soát Bản đồ tri thức `/mnt/secondbrain/50_Bản_đồ/`, đề xuất cải thiện liên kết. Báo cáo qua Zalo." |
| **Nửa năm** | `30 10 1 */6 *` | "Đề xuất chuyển dự án/chủ đề ngừng hoạt động từ `01_brain_dự_án/` sang `90_Lưu_trữ/`. Hỏi ý kiến qua Zalo trước khi thực hiện." |

> 🔒 **Nguyên tắc an toàn:** Agent luôn liệt kê đề xuất và chờ bạn duyệt qua tin nhắn. TUYỆT ĐỐI không tự xóa/di chuyển file.

## 4. (Nâng cao) Quy tắc giao tiếp
Tùy chỉnh phần "Quy tắc Giao tiếp" trong AGENT.md để agent nói chuyện đúng chất bạn.

---

## 🔗 Liên kết
- [[AGENT|🤖 Cẩm nang cho AI Agent]]
- [[99_Hệ_thống/Review & Cleanup|🗄️ Quy trình Dọn dẹp]]
- Cài đặt OpenClaw: tham khảo repo/tài liệu chính thức của OpenClaw (`create-openclaw-bot`).
