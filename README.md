# KQuiz Landing Page

Landing page tĩnh cho KQuiz, tối ưu để deploy trực tiếp lên GitHub Pages từ root repo.

## Repo này có gì

- Landing page sáng theo phong cách pastel xanh dương chủ đạo
- Nút tải thật cho Android APK: `KquizV1.0.2.apk`
- 3 nền tảng còn lại đang để `Coming soon`
- Không cần build step, không cần framework, không cần backend

## Cấu trúc

- `index.html`: landing page chính
- `styles.css`: giao diện và responsive cho desktop + mobile
- `script.js`: hiệu ứng reveal nhẹ khi cuộn
- `assets/`: icon và favicon
- `downloads/`: file APK để người dùng tải trực tiếp
- `.nojekyll`: giúp GitHub Pages deploy đúng dạng static thuần

## Cập nhật APK bằng Git Bash

Khi có bản APK mới:

1. Thay file trong thư mục `downloads/`
2. Cập nhật version trong `index.html`
3. Push lại repo

Ví dụ:

```bash
git add .
git commit -m "Update landing page to APK v1.0.2"
git push origin main
```

## Bật GitHub Pages

1. Vào repo `webkquiz` trên GitHub
2. Mở `Settings`
3. Chọn `Pages`
4. Ở mục `Build and deployment`, chọn:
   - `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
5. Save

Sau đó GitHub Pages sẽ xuất bản landing page từ root repo.

## Gợi ý cập nhật về sau

- Khi có CH Play: thay card `Coming soon` bằng link thật
- Khi có App Store: thay card `Coming soon` bằng link thật
- Khi có bản web: thay card `Coming soon` bằng URL web app
- Nếu sau này muốn repo nhẹ hơn, có thể chuyển APK sang GitHub Releases rồi đổi lại nút tải
