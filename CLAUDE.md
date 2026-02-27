# Project: Timeless

## Mô tả
Website dịch vụ của Timeless — đơn vị quản lý các **nhóm Facebook thời trang** và cung cấp dịch vụ đăng bài cho các thương hiệu thời trang.

Khách hàng (thương hiệu) trả tiền để Timeless đăng bài vào các nhóm Facebook có số lượng thành viên lớn.

## Tech Stack
- HTML + CSS + JavaScript — **tất cả trong 1 file duy nhất: `index.html`**
- Không cần framework, không cần build

## Cấu trúc thư mục
```
my-project/
├── index.html    ← toàn bộ website (HTML + CSS + JS)
└── docs/
    ├── architecture.md   ← cấu trúc kỹ thuật chi tiết
    ├── conventions.md    ← quy ước thiết kế
    └── tasks.md          ← công việc cần làm
```

## Cách chỉnh sửa nhanh (CONFIG)

### Thêm / sửa nhóm Facebook
Tìm đến dòng ~698 trong `index.html`, mảng `const groups = [...]`:
```js
{
  emoji: '🌸',           // biểu tượng hiển thị (🌸 hoặc 🔴)
  name: 'Tên nhóm',     // tên nhóm Facebook
  members: 'X thành viên',
  link: 'https://facebook.com/groups/...',
  prices: {
    '1 bài / ngày': '550.000₫',
    '2 bài / ngày': '850.000₫',
    '3 bài / ngày': '1.000.000₫'
  }
}
```

### Sửa thông tin thanh toán
Tìm `id="tab-payment"` (~dòng 644)

### Sửa quy định
Tìm `id="tab-info"` (~dòng 508)

### Sửa liên hệ
Tìm `id="tab-contact"` (~dòng 676)

## Quy tắc code
- Viết comment bằng tiếng Việt
- Không tách file — giữ nguyên 1 file HTML duy nhất
