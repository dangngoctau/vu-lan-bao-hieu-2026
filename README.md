# Triển khai lên GitHub Pages

Thư mục này là bản tĩnh nhiều file của landing page (tải nhanh, ảnh hiện dần).

- `index.html` — trang chính
- `support.js`, `image-slot.js` — mã chạy trang
- `img/` — ảnh
- `.nojekyll` — tắt xử lý Jekyll của GitHub Pages

## Cách deploy

Đẩy toàn bộ nội dung **bên trong** thư mục `deploy/` lên nhánh `main`, giữ nguyên cấu trúc thư mục (`index.html` ở gốc repo, `img/` là thư mục con).

```bash
git init
git add .
git commit -m "Landing page Vu Lan 2026"
git branch -M main
git remote add origin https://github.com/<tài-khoản>/<tên-repo>.git
git push -u origin main
```

Vào **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main`, thư mục `/ (root)` → Save.

## Lưu ý

- Phải giữ đủ cả 4 mục: `index.html`, `support.js`, `image-slot.js`, `img/`. Thiếu một file thì trang sẽ trắng.
- Bản đồ dùng tile CARTO/OpenStreetMap và phông chữ Google — máy người xem cần có mạng.
- Muốn cập nhật nội dung: sửa file nguồn `Vu Lan Ngu Hanh Son 2026.dc.html` rồi xuất lại thư mục này.
