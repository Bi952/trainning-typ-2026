# Hướng dẫn nộp bài

## Bước 1: Fork repo
- Fork repo này về tài khoản GitHub cá nhân

## Bước 2: Làm bài
- Mỗi tuần tạo **branch mới** từ `main` (đặt tên: `week-1`, `week-2`,...)
- Thêm bài làm vào folder tương ứng (code, tài liệu, ảnh demo,...)

### Ví dụ minh họa

**Tuần 1:** Tạo branch `week-1` từ `main`, thêm bài làm vào folder `week-1/`

```
repo (branch: week-1)
├── README.md              ← có sẵn từ main
├── SUBMISSION.md           ← có sẵn từ main
├── week-1/
│   ├── README.md           ← đề bài (có sẵn từ main)
│   ├── ly-thuyet.md        ←  bài làm của bạn
│   ├── queries.sql         ←  bài làm của bạn
│   └── screenshots/        ←  bài làm của bạn
├── week-2/
│   └── README.md           ← đề bài (có sẵn, KHÔNG ĐỘNG VÀO)
├── week-3/
│   └── README.md
├── ...
```

→ Tạo PR. Mentor review diff sẽ **chỉ thấy các file trong `week-1/`** mà bạn thêm vào.

---

**Tuần 2:** Tạo branch `week-2` từ `main` (KHÔNG phải từ branch `week-1`), thêm bài làm vào folder `week-2/`

```
repo (branch: week-2)
├── README.md
├── SUBMISSION.md
├── week-1/
│   └── README.md           ← đề bài (KHÔNG có bài tuần 1 ở đây)
├── week-2/
│   ├── README.md           ← đề bài (có sẵn từ main)
│   ├── ly-thuyet.md        ←  bài làm của bạn
│   └── src/                ←  bài làm của bạn
│       ├── controllers/
│       ├── models/
│       └── ...
├── week-3/
│   └── README.md
├── ...
```

→ Tạo PR. Mentor review diff sẽ **chỉ thấy các file trong `week-2/`** mà bạn thêm vào.

---

> **Quan trọng:** Mỗi tuần tạo branch mới **từ `main`**, không tạo từ branch tuần trước. Như vậy mỗi PR chỉ chứa diff của đúng tuần đó, mentor review gọn hơn.

## Bước 3: Tạo Pull Request
- Tạo PR từ branch về **repo gốc** (không phải fork của bạn)
- Tiêu đề PR theo format:

```
[Week X] Họ và tên
```

Ví dụ:
```
[Week 1] Trịnh Quang Lâm
[Week 2] Trịnh Quang Lâm
```

- Gắn **label** tương ứng: `week-1`, `week-2`, `week-3`, `week-4`, `week-5`, `project`

## Bước 4: Review
- Mentor sẽ review trên PR và comment feedback
- Sửa bài theo feedback → push thêm commit vào cùng branch → PR tự cập nhật