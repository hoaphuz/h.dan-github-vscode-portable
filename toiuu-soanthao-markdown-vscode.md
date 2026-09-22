# Tối ưu trình soạn thảo Markdown trên VScode

Soạn các tài liệu thông tin, hướng dẫn trên GitHub đa số sẽ làm việc với định dạng markdown nên cần phải tối ưu chút để soạn thảo dễ dàng hơn

Nhập `>Preferences: Open Workspace Settings (JSON)` vào ô tìm kiếm nếu muốn áp dụng cho toàn bộ VScode

hoặc nhập `>Preferences: Open Workspace Settings (JSON)` nếu muốn áp dụng cho dự án hiện tại thôi

Dán cụm cấu hình sau vào trong cặp dấu ngoặc nhọn { ... } của tệp settings.json

```
  // Tự động cập nhật đường dẫn Markdown khi đổi tên hoặc di chuyển file/thư mục
  "markdown.updateLinksOnFileMove.enabled": "always",

  // Bật tính năng sao chép file khi kéo thả hoặc dán từ clipboard ngoài
  "markdown.editor.drop.copyIntoWorkspace": "mediaFiles",
  "markdown.editor.filePaste.copyIntoWorkspace": "mediaFiles",

  // Chỉ định thư mục lưu ảnh: ./assets cùng cấp với file Markdown đang mở
  "markdown.copyFiles.destination": {
    "**/*": "./assets/${fileName}"
  },

  // Tùy chọn: Tự động ghi đè file nếu bị trùng tên thay vì báo lỗi
  "markdown.copyFiles.overwriteBehavior": "nameIncrementally"
```

