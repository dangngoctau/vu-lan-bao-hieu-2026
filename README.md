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

## Ảnh xem trước khi chia sẻ (Facebook, Zalo)

Thẻ `og:*` trong `index.html` dùng địa chỉ tuyệt đối `https://lehoivulanbaohieu-nhs-danang.vn`. **Nếu deploy sang tên miền khác, phải sửa lại tất cả địa chỉ này**, nếu không Facebook/Zalo sẽ không lấy được ảnh.

Ảnh xem trước: `img/og-share.jpg` (1200×630, 114 KB) — dựng từ `og-card.dc.html`.

Sau khi deploy, xoá cache của mạng xã hội (nếu không, chúng vẫn hiện bản trắng cũ):

- Facebook: developers.facebook.com/tools/debug → dán link → **Scrape Again**
- Zalo: developers.zalo.me/tools/debug-open-graph → dán link → **Cập nhật lại**

## Lưu ý

- Phải giữ đủ cả 4 mục: `index.html`, `support.js`, `image-slot.js`, `img/`. Thiếu một file thì trang sẽ trắng.
- Bản đồ dùng tile CARTO/OpenStreetMap và phông chữ Google — máy người xem cần có mạng.
- Muốn cập nhật nội dung: sửa file nguồn `Vu Lan Ngu Hanh Son 2026.dc.html` rồi xuất lại thư mục này.
