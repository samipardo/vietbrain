---
type: system
status: evergreen
created: 2026-06-20
tags:
  - System/Maintenance
---

# 🗄️ Hướng dẫn Dọn dẹp & Bảo trì Bộ não (Brain Review & Cleanup)

Để bộ não thứ hai không thành "bãi rác thông tin", cần quy trình dọn dẹp định kỳ dựa trên mô hình **Phòng tri thức + CODE**.

---

## 📅 Dọn dẹp hàng tuần (Weekly Review) — 15–20 phút, cuối tuần

### 1. Giải phóng Inbox (Inbox Zero)
Đi qua từng mục trong `00_Hộp_thư_đến/`, đưa vào đúng **phòng tri thức**:
- Liên quan dự án → `01_brain_dự_án/<tên dự án>/`.
- Tri thức theo chủ đề → phòng `brain_*` tương ứng, nén thành ghi chú nguyên tử, đặt tên tiếng Việt dễ đọc.
- Hết giá trị → xóa thẳng.
- **Mục tiêu:** `00_Hộp_thư_đến/` trống trong tối đa 7 ngày.

### 2. Dọn thẻ Tag
- Kiểm tra đúng định dạng **CamelCase phân tầng** (`Domain/TaiChinh`, `Type/Framework`).
- Thẻ dưới 3 ghi chú → gộp hoặc xóa.

### 3. Cập nhật trạng thái
- Dự án đã xong / chủ đề không còn quan tâm → chuyển sang `90_Lưu_trữ/`.
- Mỗi phòng giữ **7–15 mục**. Nhiều hơn thì tách phòng con.

---

## 🔄 Ôn tập chu kỳ (Spaced Repetition)

1. **7 ngày (Tuần):** Dọn Inbox, ôn lại Nhật ký `60_Nhật_ký/` theo khung **4F**, nén phát hiện thành note nguyên tử.
2. **30 ngày (Tháng):** Đọc lại note `growing` → cân nhắc nâng lên `permanent`/`evergreen`.
3. **90 ngày (Quý):** Rà soát Bản đồ tri thức `50_Bản_đồ/` — kết nối đã đủ chặt chưa.
4. **180 ngày (Nửa năm):** Lọc bỏ note hết giá trị; chuyển dự án/chủ đề ngừng hoạt động vào `90_Lưu_trữ/`.

---

## 💡 Tài liệu đính kèm thừa
Cài plugin **Janitor** hoặc **Clear Unused Images** để quét `00_Hộp_thư_đến/Attachments/` và xóa hình ảnh không được liên kết.

---

## 🔗 Liên kết
- [[99_Hệ_thống/vault-constitution|📜 Hiến pháp Vault]]
- [[AGENT|🤖 Cẩm nang cho AI Agent]]
- [[50_Bản_đồ/Trang chủ|🎛️ Trang chủ — Master MOC]]
