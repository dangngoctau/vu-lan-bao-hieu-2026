# Triển khai lên GitHub Pages

Thư mục này chứa bản tĩnh, tự chứa của landing page:

- `index.html` — toàn bộ trang trong một file (không cần build, không cần server).
- `.nojekyll` — tắt xử lý Jekyll của GitHub Pages.

## Cách deploy

1. Tạo repo mới trên GitHub (ví dụ `vulan-nguhanhson-2026`).
2. Đẩy nội dung **bên trong** thư mục `deploy/` lên nhánh `main` (đặt `index.html` ở gốc repo).
   ```bash
   git init
   git add .
   git commit -m "Landing page Vu Lan 2026"
   git branch -M main
   git remote add origin https://github.com/<tài-khoản>/<tên-repo>.git
   git push -u origin main
   ```
3. Vào **Settings → Pages**, mục *Build and deployment*: Source = **Deploy from a branch**, Branch = `main`, thư mục `/ (root)` → Save.
4. Sau 1–2 phút, trang chạy tại `https://<tài-khoản>.github.io/<tên-repo>/`.

## Lưu ý

- Bản đồ dùng tile CARTO/OpenStreetMap qua Internet — máy người xem cần có mạng để hiện bản đồ (phù hợp với kịch bản quét QR tại chỗ).
- Ảnh sơ đồ phân khu và ảnh gallery hiện là ô giữ chỗ; khi có ảnh thật, cập nhật trong file nguồn `Vu Lan Ngu Hanh Son 2026.dc.html` rồi xuất lại bản này.
- Không sửa trực tiếp `index.html` (file đã đóng gói) — sửa file nguồn rồi build lại.
