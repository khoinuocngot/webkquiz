# KQuiz Landing Page

Landing page tĩnh cho KQuiz, tối ưu để deploy trực tiếp lên GitHub Pages từ root repo.

## Có gì trong repo này

- Giao diện landing page mới theo hướng `premium, ít chữ, nhiều hình`
- Hero riêng cho desktop và mobile
- Nút tải thật cho Android APK: `KquizV1.0.3.apk`
- Google Play, App Store và Web App đang để `Coming soon`
- Không cần build step, không cần framework, không cần backend

## Cấu trúc chính

- `index.html`: landing page chính
- `styles.css`: giao diện và responsive cho desktop, tablet, mobile
- `script.js`: hiệu ứng reveal nhẹ khi cuộn
- `assets/hero/logo-k.jpg`: logo KQuiz
- `assets/hero/hero-desktop.png`: ảnh minh họa hero cho desktop
- `assets/hero/hero-mobile.png`: ảnh minh họa hero cho mobile
- `downloads/KquizV1.0.3.apk`: file APK tải trực tiếp
- `.nojekyll`: giúp GitHub Pages chạy static thuần

## Cập nhật APK bằng Git Bash

Khi có bản APK mới:

1. Thay file trong thư mục `downloads/`
2. Cập nhật version và tên file trong `index.html`
3. Nếu cần, sửa lại mô tả trong `README.md`
4. Push lại repo

Ví dụ:

```bash
git add .
git commit -m "Update landing page to APK v1.0.3"
git push origin main
```

## Cập nhật ảnh giao diện

Nếu muốn đổi lại ảnh minh họa:

1. Thay `assets/hero/hero-desktop.png`
2. Thay `assets/hero/hero-mobile.png`
3. Nếu muốn đổi logo, thay `assets/hero/logo-k.jpg`
4. Push lại repo

## Bật GitHub Pages

1. Vào repo `webkquiz` trên GitHub
2. Mở `Settings`
3. Chọn `Pages`
4. Ở mục `Build and deployment`, chọn:
   - `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
5. Save

Sau đó GitHub Pages sẽ xuất bản trang từ root repo.

## Gợi ý nâng cấp về sau

- Thay mockup hiện tại bằng ảnh app thật khi cần
- Thêm link Google Play khi store sẵn sàng
- Thêm link App Store khi có bản iOS
- Thêm link bản web khi web app hoàn thiện
- Nếu muốn repo nhẹ hơn, có thể chuyển APK sang GitHub Releases rồi đổi lại nút tải
