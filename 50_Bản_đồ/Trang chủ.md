---
type: moc
status: evergreen
created: 2026-06-20
tags:
  - MOC/Master
---

# 🎛️ Trang Chủ — Master MOC

_Điểm điều hướng tối cao của Bộ não thứ hai. Chỉ liên kết xuống Sub-MOC và các Phòng tri thức._

---

> [!info] 🚀 Truy Cập Nhanh
> - **Chỉ dẫn AI**: [[AGENT|🤖 Cẩm nang cho AI Agent]]
> - **Hiến pháp Vault**: [[99_Hệ_thống/vault-constitution|📜 Hiến pháp Vault]]
> - **Dọn dẹp & ôn tập**: [[99_Hệ_thống/Review & Cleanup|🗄️ Review & Cleanup]]
> - **Cài đặt OpenClaw**: [[99_Hệ_thống/Hướng dẫn Cài đặt OpenClaw|🤖 Hướng dẫn]]

---

## 🧠 Các Phòng Tri Thức (brain_*)

| Phòng | Nội dung | Bản đồ |
|---|---|---|
| 💼 `01_brain_dự_án` | Dự án đang làm/đã làm | [[50_Bản_đồ/Bản đồ Dự án\|🗺️ Bản đồ Dự án]] |
| ✍️ `02_brain_content` | Nội dung đã viết | [[50_Bản_đồ/Bản đồ Content\|✍️ Bản đồ Content]] |
| 💻 `03_brain_công_nghệ` | Lập trình, kỹ thuật, AI | [[03_brain_công_nghệ/Mục lục Công nghệ\|💻]] |
| 🦞 `04_brain_open_source` | Repo hay, mã nguồn mở | [[04_brain_open_source/Mục lục Open Source\|🦞]] |
| 💰 `05_brain_tài_chính` | Tài chính, đầu tư | [[05_brain_tài_chính/Mục lục Tài chính\|💰]] |
| 🏠 `06_brain_bất_động_sản` | Bất động sản | [[06_brain_bất_động_sản/Mục lục Bất động sản\|🏠]] |
| 📈 `07_brain_kinh_doanh` | Kinh doanh, marketing | [[07_brain_kinh_doanh/Mục lục Kinh doanh\|📈]] |
| 🌱 `08_brain_phát_triển_bản_thân` | Kỹ năng, tư duy, hồ sơ | [[08_brain_phát_triển_bản_thân/Mục lục Phát triển bản thân\|🌱]] |
| 🎓 `09_brain_bài_học` | Bài học đúc kết | [[09_brain_bài_học/Mục lục Bài học\|🎓]] |

---

## ⚙️ Khung vận hành
`00_Hộp_thư_đến` (thu thập) · `50_Bản_đồ` (điều hướng) · `60_Nhật_ký` (nhật ký 4F) · `90_Lưu_trữ` (lưu trữ) · `99_Hệ_thống` (hạ tầng)

---

## 💼 Dự án đang làm (Dataview — cần plugin Dataview)

> [!abstract] Các dự án trong `01_brain_dự_án/`
> ```dataview
> LIST
> FROM "01_brain_dự_án"
> WHERE file.folder != "01_brain_dự_án"
> ```

---

## ✍️ Hoạt động gần đây (Dataview)

> [!note] Nội dung & nhật ký mới cập nhật
> ```dataview
> TABLE file.mtime AS "Cập nhật lúc", status AS "Trạng thái"
> FROM "02_brain_content" OR "60_Nhật_ký"
> SORT file.mtime DESC
> LIMIT 5
> ```
