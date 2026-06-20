---
type: system
status: evergreen
created: 2026-06-20
tags:
  - System/Constitution
---

# 📜 Hiến Pháp Vault (Vault Constitution)

*Tài liệu này quy định tiêu chuẩn về cấu trúc, cách đặt tên, thuộc tính ghi chú và vòng đời thông tin, để Bộ não thứ hai luôn nhất quán, sạch sẽ và tối ưu. Vault dùng mô hình **Hybrid**: các **Phòng Tri Thức** (`brain_*`) tổ chức theo chủ đề cuộc sống + bộ khung vận hành (Hộp thư, Bản đồ, Nhật ký, Lưu trữ, Hệ thống). Kết hợp **Zettelkasten** (ghi chú nguyên tử), **MOC** (bản đồ tri thức) và quy trình **CODE**.*

---

## 📂 1. Cấu trúc thư mục

Vault chia 2 lớp: **Phòng tri thức** (chứa nội dung theo chủ đề) và **Khung vận hành** (dòng chảy thông tin).

### 🧠 Phòng Tri Thức (`brain_*`) — chứa nội dung theo chủ đề
| Thư mục | Chứa gì |
|---|---|
| **`01_brain_dự_án/`** | Các dự án bạn đang làm/đã làm (mỗi dự án 1 thư mục con). |
| **`02_brain_content/`** | Nội dung bạn viết: `0_Nháp/`, `1_Đã_đăng/`. |
| **`03_brain_công_nghệ/`** | Kiến thức lập trình, kỹ thuật, AI, công cụ. |
| **`04_brain_open_source/`** | Repo hay, dự án mã nguồn mở đáng học. |
| **`05_brain_tài_chính/`** | Tài chính, đầu tư, quản lý tiền. |
| **`06_brain_bất_động_sản/`** | Kiến thức bất động sản. |
| **`07_brain_kinh_doanh/`** | Kinh doanh, khởi nghiệp, marketing, bán hàng. |
| **`08_brain_phát_triển_bản_thân/`** | Kỹ năng, tư duy, giao tiếp, hồ sơ cá nhân. |
| **`09_brain_bài_học/`** | Bài học hay đúc kết từ trải nghiệm, sách, người khác. |

> 💡 **Tùy biến thoải mái:** Xóa phòng bạn không cần, đổi tên, hoặc thêm phòng mới khi có chủ đề mới trong đời (ví dụ `10_brain_sức_khỏe/`, `11_brain_du_lịch/`). Khi một phòng vượt **15 note**, tách phòng con (ví dụ `05_brain_tài_chính/Cổ phiếu/`).

### ⚙️ Khung Vận Hành — dòng chảy thông tin
| Thư mục | Vai trò |
|---|---|
| **`00_Hộp_thư_đến/`** | **Capture** — cửa vào duy nhất cho mọi thông tin mới. Dọn sạch (Inbox Zero) trong **7 ngày**. Chứa `Attachments/`. |
| **`50_Bản_đồ/`** | **MOC** — bản đồ điều hướng. `Trang chủ.md` là Home; các `Bản đồ *.md` là Sub-MOC. |
| **`60_Nhật_ký/`** | **Calendar** — nhật ký hàng ngày (khung 4F). |
| **`90_Lưu_trữ/`** | **Archive** — dự án xong / chủ đề ngừng quan tâm / tri thức hết giá trị. |
| **`99_Hệ_thống/`** | **Meta** — Hiến pháp, `Templates/`, hướng dẫn. |

---

## 🧱 2. Ghi chú nguyên tử (Atomic Notes — Zettelkasten)

Mỗi ghi chú tri thức chỉ chứa **một ý tưởng duy nhất**, đọc hiểu cốt lõi trong **10 giây**, và nằm trong phòng `brain_*` đúng chủ đề. Mỗi ghi chú thuộc 1 trong 5 loại:

1. **`concept` (Khái niệm)** — Định nghĩa cốt lõi của một kiến thức.
2. **`framework` (Mô hình/Quy trình)** — Mô hình có các bước cụ thể.
3. **`insight` (Bài học)** — Phát hiện đúc rút từ trải nghiệm thực tế.
4. **`perspective` (Góc nhìn)** — Quan điểm, phản biện, triết lý cá nhân.
5. **`technique` (Kỹ thuật/Cách làm)** — Thủ thuật, lệnh code copy-dùng-ngay.

---

## 🏷️ 3. Quy tắc đặt tên & thuộc tính

### Đặt tên tệp — **TIẾNG VIỆT, dễ đọc**
- Tên file viết **tiếng Việt có dấu, Title Case, cách bằng khoảng trắng** — nhìn tên là hiểu nội dung. Ví dụ: `Cách tối ưu chỉ số P_E khi định giá.md`.
- **Ngoại lệ giữ nguyên tên gốc**: tên **dự án** và **bài content đã đăng** (đặt theo ngày `YYYY-MM-DD-...`).
- Phân loại đã thể hiện qua **thư mục (phòng)** + **frontmatter**, nên KHÔNG cần nhồi mã phân loại vào tên file.

### Thuộc tính bắt buộc (YAML Frontmatter)
```yaml
---
type: concept        # concept | framework | insight | perspective | technique
status: seed         # seed | growing | permanent | evergreen
domain: tài-chính    # chủ đề/phòng chứa note
created: YYYY-MM-DD
tags:
  - Domain/TaiChinh
  - Type/Concept
---
```

---

## ⛓️ 4. Kết nối & Quản lý thẻ (Tag)

- **Mật độ liên kết:** Mỗi ghi chú phải có **tối thiểu 3 liên kết** (`[[Tên Note]]`). Tri thức không liên kết là "tri thức chết".
- **Quy tắc 7–15:** Mỗi phòng nên chứa **7–15 mục**. Vượt quá thì tách phòng con.
- **Thẻ (Tag):** Tối đa **5 thẻ**/ghi chú, định dạng **CamelCase phân tầng** (`Domain/TaiChinh`, `Type/Framework`). Gộp/xóa thẻ có dưới 3 ghi chú.

---

## 🔄 5. Vòng đời trạng thái ghi chú (Status Lifecycle)

`seed (Hạt mầm) ➔ growing (Đang lớn) ➔ permanent (Vĩnh cửu) ➔ evergreen (Thường xanh)`

- 🌱 **`seed`** — Ý tưởng thô mới chép, chưa kiểm chứng.
- 🌿 **`growing`** — Đang bổ sung thông tin, ví dụ, liên kết.
- 🧱 **`permanent`** — Đã xác minh đúng đắn, viết chỉn chu.
- 🌲 **`evergreen`** — Tri thức cốt lõi bền vững, tái sử dụng cực cao.

---

## 🚀 6. Quy trình vận hành CODE (PKM Pipeline)

**CODE** = Capture → Organize → Distill → Express:

1. **Capture (Thu thập)** — Ghi ngay mọi thông tin thô vào `00_Hộp_thư_đến/`.
2. **Organize (Sắp xếp)** — Định kỳ dọn Inbox: đưa từng mục vào đúng **phòng tri thức**.
3. **Distill (Chưng cất)** — Viết Nhật ký theo khung **4F (Facts – Feelings – Findings – Future)**, rồi nén bài học thành ghi chú nguyên tử.
4. **Connect (Kết nối)** — Gắn ghi chú vào MOC `50_Bản_đồ/` và tạo ≥3 liên kết chéo.
5. **Express & Review** — Dùng tri thức tạo đầu ra. Ôn tập ngắt quãng: **7 ➔ 30 ➔ 90 ➔ 180 ngày**.

---

## 🔗 Liên kết hệ thống
- [[AGENT|🤖 Cẩm nang cho AI Agent]]
- [[99_Hệ_thống/Review & Cleanup|🗄️ Quy trình Dọn dẹp & Bảo trì]]
- [[50_Bản_đồ/Trang chủ|🎛️ Trang chủ — Master MOC]]
