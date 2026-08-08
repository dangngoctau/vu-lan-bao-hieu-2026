# Vu Lan Báo Hiếu 2026 — NHS

Trang thông tin đại lễ Vu Lan Báo Hiếu 2026, xuất bản bằng GitHub Pages.

## Nội dung cần cập nhật

Toàn bộ trang nằm trong một tệp duy nhất: `index.html`. Các chỗ trong ngoặc vuông `[...]`
là nội dung tạm, cần thay bằng thông tin thật:

| Mục | Vị trí trong `index.html` | Ghi chú |
|---|---|---|
| Địa chỉ đầy đủ | phần `#thong-tin`, thẻ **Địa điểm** | |
| Tên người phụ trách | phần `#lien-he` | |
| Số điện thoại | phần `#lien-he` | cập nhật cả `href="tel:..."` |
| Email | phần `#lien-he` | cập nhật cả `href="mailto:..."` |
| Liên kết ghi danh | phần `#lien-he` | ví dụ Google Form |

Cần kiểm tra lại (đang để giá trị dự kiến):

- **Ngày tổ chức** — hiện đặt là Chủ Nhật 30/08/2026 (nhằm 18 tháng Bảy năm Bính Ngọ).
  Rằm tháng Bảy 2026 rơi vào Thứ Năm 27/08/2026.
- **Giờ giấc và chương trình** — phần `#chuong-trinh`.
- **Tên đạo tràng "NHS"** — xuất hiện ở tiêu đề, phần đầu trang và chân trang.

## Xem thử tại máy

```sh
open index.html
```

Hoặc chạy một máy chủ tĩnh:

```sh
python3 -m http.server 8000
```

rồi mở http://localhost:8000

## Xuất bản

Mỗi lần đẩy lên nhánh `main`, GitHub Pages sẽ tự động cập nhật trang.

```sh
git add -A
git commit -m "Cập nhật thông tin đại lễ"
git push
```
