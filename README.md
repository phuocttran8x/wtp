# Waterpoint Tracking - GitHub Pages

## Files
- `index.html`: trang public cho cư dân xem
- `admin.html`: trang quản trị riêng, có mật khẩu
- `data.json`: dữ liệu timeline
- `files/`: thư mục lưu PDF nếu có

## Cấu hình bắt buộc
Mở cả `index.html` và `admin.html`, tìm:

```js
const CONFIG = { owner: 'YOUR_GITHUB_USERNAME', repo: 'YOUR_REPO_NAME', branch: 'main', dataPath: 'data.json' };
```

Ví dụ repo URL:

```text
https://github.com/phuoctran/waterpoint-tracking
```

Sửa thành:

```js
const CONFIG = { owner: 'phuoctran', repo: 'waterpoint-tracking', branch: 'main', dataPath: 'data.json' };
```

## GitHub Pages
Settings → Pages → Deploy from a branch → `main` → `/root`

## Admin
Truy cập:

```text
/admin.html
```

Mật khẩu admin:

```text
wxfA9F6UEO1gZQcX
```

Sau khi đăng nhập admin, nhập GitHub fine-grained token có quyền:

```text
Contents: Read and Write
```

## Dark mode
Có nút 🌙 / ☀️ trên cả trang public và admin. Trạng thái được lưu trong trình duyệt.


## Hiển thị timeline
- Mục mới nhất luôn mở full nội dung.
- Các mục cũ mặc định thu gọn, chỉ hiện tiêu đề và ngày.
- Người xem bấm `Xem chi tiết` để mở nội dung cũ, bấm `Thu gọn` để đóng lại.
