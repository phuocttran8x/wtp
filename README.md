# Waterpoint Tracking GitHub Pages

## File trong bộ này
- `index.html`: website chính
- `data.json`: dữ liệu timeline
- `files/`: thư mục để upload PDF nếu có

## Cấu hình bắt buộc
Mở `index.html`, tìm:

```js
const CONFIG={owner:'YOUR_GITHUB_USERNAME',repo:'YOUR_REPO_NAME',branch:'main',dataPath:'data.json'};
```

Ví dụ repo URL là:

```text
https://github.com/phuoctran/waterpoint-tracking
```

thì sửa thành:

```js
const CONFIG={owner:'phuoctran',repo:'waterpoint-tracking',branch:'main',dataPath:'data.json'};
```

## Upload lên GitHub
1. Tạo repo mới trên GitHub.
2. Upload toàn bộ file:
   - `index.html`
   - `data.json`
   - thư mục `files/`
3. Vào Settings → Pages.
4. Source: Deploy from a branch.
5. Branch: `main`, folder: `/root`.

## Cách vào admin
Mở website, nhấn:

```text
Ctrl + Alt + A
```

Nhập GitHub fine-grained token có quyền:
- Repository access: repo này
- Permissions → Contents: Read and Write

## Cách cập nhật
1. Vào admin.
2. Thêm/sửa/xóa timeline.
3. Bấm `Commit data.json lên GitHub`.
4. Người xem refresh trang sẽ thấy dữ liệu mới.
