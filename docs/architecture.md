# Architecture: Timeless

## Tổng quan
Single-page app, 1 file HTML duy nhất (~542KB). CSS và JS đều nhúng inline.

## Tabs (điều hướng)
| Tab | ID HTML | Nội dung |
|-----|---------|----------|
| Hệ thống nhóm | `#tab-groups` | Danh sách nhóm Facebook + giá |
| Quy định | `#tab-info` | Quy định & lưu ý |
| Thanh toán | `#tab-payment` | Thông tin chuyển khoản |
| Liên hệ | `#tab-contact` | Thông tin liên hệ |

## Cấu trúc JS chính
```
const groups = [...]       // ~dòng 698  — DỮ LIỆU NHÓM (chỉnh ở đây)
renderGroups(data)         // ~dòng 785  — render card nhóm ra DOM
filterGroups(query)        // ~dòng 863  — lọc nhóm theo tìm kiếm
showTab(tab, el)           // ~dòng 869  — chuyển tab
copySTK()                  // ~dòng 876  — copy số tài khoản
Sakura canvas animation    // ~dòng 807  — hiệu ứng hoa rơi
```

## Cấu trúc data 1 nhóm
```js
{
  emoji: '🌸' | '🔴',   // màu nhóm
  name: string,
  members: string,        // vd: '200.000 thành viên'
  link: string,           // URL Facebook group
  prices: {
    '1 bài / ngày': string,
    '2 bài / ngày': string,
    '3 bài / ngày': string
  }
}
```

## Màu sắc (CSS variables ~dòng 8)
```css
--rose: #c8a0a0
--rose-deep: #9b6b6b
--rose-light: #f5eded
--rose-bg: #faf5f5
--gold: #b8976a
--muted: #7a6a6a
--dark: #2a1f1f
```

## Responsive
Breakpoint tại 600px (~dòng 453)
