# KQuiz Landing Page

Landing page tĩnh cho KQuiz, tối ưu để deploy trực tiếp lên GitHub Pages từ root repo.

## Có gì trong repo này

- Giao diện landing page sáng, gọn, ít chữ và bám theo ảnh hero riêng cho desktop/mobile
- Nút tải thật cho Android APK: `KquizV1.0.4.apk`
- File phát hành kỹ thuật bổ sung: `KquizV1.0.4.aab`
- Google Play, App Store và Web App đang để `Coming soon`
- Không cần build step, không cần framework, không cần backend

## Cấu trúc chính

- `index.html`: landing page chính
- `styles.css`: giao diện và responsive cho desktop, tablet, mobile
- `script.js`: hiệu ứng reveal nhẹ khi cuộn
- `assets/hero/logo-k.jpg`: logo KQuiz
- `assets/hero/hero-desktop.png`: ảnh minh họa hero cho desktop
- `assets/hero/hero-mobile.png`: ảnh minh họa hero cho mobile
- `downloads/KquizV1.0.4.apk`: file APK tải trực tiếp
- `downloads/KquizV1.0.4.aab`: file AAB phát hành kỹ thuật
- `.nojekyll`: giúp GitHub Pages chạy static thuần

## Cập nhật bản phát hành bằng Git Bash

Khi có bản mới:

1. Thay file trong thư mục `downloads/`
2. Cập nhật version và tên file trong `index.html`
3. Nếu cần, sửa lại mô tả trong `README.md`
4. Push lại repo

Ví dụ:

```bash
git add .
git commit -m "Update landing page to v1.0.4"
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

- Thêm link Google Play khi store sẵn sàng
- Thêm link App Store khi có bản iOS
- Thêm link bản web khi web app hoàn thiện
- Thêm release notes ngắn cho từng phiên bản nếu muốn
- Nếu muốn repo nhẹ hơn, có thể chuyển APK/AAB sang GitHub Releases rồi đổi lại nút tải
