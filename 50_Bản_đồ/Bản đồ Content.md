---
type: moc
status: evergreen
created: 2026-06-20
tags:
  - MOC/Content
---

# 🗺️ Sub-MOC: Content

_Bản đồ điều hướng nội dung bạn viết. Quy trình: ý tưởng → `0_Nháp/` → đăng → chuyển sang `1_Đã_đăng/`._

---

## 🏠 Trang điều hành
- [[02_brain_content/Trang điều hành Content|✍️ Trang điều hành Content]]

## 📝 Nháp đang viết (Dataview)
```dataview
LIST
FROM "02_brain_content/0_Nháp"
SORT file.mtime DESC
```

## ✅ Bài đã đăng (Dataview)
```dataview
TABLE file.ctime AS "Ngày tạo"
FROM "02_brain_content/1_Đã_đăng"
SORT file.name DESC
```

---

## 🔗 Liên kết
- [[50_Bản_đồ/Trang chủ|🎛️ Trang chủ]]
- [[50_Bản_đồ/Bản đồ Dự án|🗺️ Bản đồ Dự án]]
