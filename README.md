# Hướng Dẫn Sử Dụng - GitHub Image Uploader

Trình tải ảnh trực tiếp lên kho lưu trữ GitHub (Image Hosting / Image Bed) kèm tự động sinh link CDN jsDelivr siêu nhanh cho Website, Markdown, Blog.

---

## 🚀 1. Cách lấy GitHub Token (Personal Access Token)

1. Truy cập: [GitHub Tokens Settings](https://github.com/settings/tokens)
2. Chọn **Generate new token** -> **Generate new token (classic)**
3. Đặt tên gợi nhớ ở mục **Note** (ví dụ: `image-uploader`)
4. Chọn thời hạn **Expiration** (ví dụ: `No expiration` hoặc `90 days`)
5. Tích chọn quyền:
   - ✅ **`repo`** (Full control of private repositories)
6. Kéo xuống dưới cùng và bấm **Generate token**.
7. **Sao chép mã Token** (dạng `ghp_xxxxxxxxxxxx`) và lưu lại.

---

## 📁 2. Chuẩn bị Repository trên GitHub

1. Tạo một repository mới (hoặc dùng repo có sẵn), ví dụ: `hinh-anh` hoặc `my-cdn-images`.
2. Có thể để chế độ **Public** (để link ảnh có thể xem công khai trên web) hoặc **Private**.
   > **Mẹo**: Nếu để Public, bạn có thể dùng link **jsDelivr CDN** tải ảnh siêu tốc không bị giới hạn băng thông.
3. Đảm bảo repo đã có ít nhất một commit khởi tạo (ví dụ tạo file `README.md`).

---

## ⚙️ 3. Cấu hình trên giao diện Web

Mở file [`index.html`](index.html) bằng bất kỳ trình duyệt nào (Chrome, Edge, Cốc Cốc, Firefox...):

1. Bấm nút **Cấu hình GitHub** ở góc trên bên phải:
   - **GitHub Token (PAT)**: Dán token vừa tạo ở Bước 1.
   - **Repository**: Nhập theo định dạng `username/tên-repo` (ví dụ: `nguyenvana/my-images`).
   - **Branch**: Mặc định là `main`.
   - **Thư mục lưu ảnh**: Mặc định là `images` (hoặc để trống nếu lưu ở thư mục gốc).
2. Bấm nút **"Kiểm tra kết nối Repo"** để xác nhận mọi thông số đã chuẩn.
3. Bấm **"Lưu cấu hình"** (thông tin được lưu an toàn trong trình duyệt của bạn).

---

## 🖼️ 4. Cách tải ảnh lên & lấy link

- **Cách 1 - Kéo thả**: Kéo ảnh trực tiếp vào khung kéo thả.
- **Cách 2 - Chọn file**: Bấm vào khung kéo thả để mở hộp thoại chọn ảnh (hỗ trợ chọn nhiều ảnh cùng lúc).
- **Cách 3 - Dán ảnh (Ctrl + V)**: Chụp màn hình (Windows + Shift + S) rồi nhấn **Ctrl + V** ngay trên trang web.
- Bấm **"Bắt đầu tải lên Git"**.
- Sau khi tải xong, bạn có thể bấm 1 chạm để sao chép:
  - ⚡ **CDN Link**: Link qua jsDelivr CDN tải siêu tốc.
  - 📝 **Markdown**: `![tên-ảnh](link)` dùng cho Github, Notion, Obsidian, v.v.
  - 🌐 **HTML**: Thẻ `<img src="..." />` dùng cho website.
  - 🔗 **Raw Link**: Link raw github.
