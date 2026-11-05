# Dong Hui - Thông Báo Hiện Trường (Web / Vercel)

Bản web được chuyển từ dự án Android Studio v1.7. Không cần Android Studio để chạy.

## Chức năng giữ nguyên
- 3 mẫu: tiến độ, chất lượng, an toàn.
- Giao diện và nội dung song ngữ / đa ngôn ngữ.
- Upload logo công ty và nhiều ảnh đính kèm.
- Lưu công trình, nhà thầu, mã hợp đồng và bản nháp trên thiết bị bằng localStorage.
- Xuất PNG nhiều trang, PDF A4 nhiều trang, Word `.doc`.
- Dịch tự động nếu người dùng nhập Google Cloud Translation API key.
- Có thể cài lên màn hình chính dưới dạng PWA.

## Deploy bằng GitHub + Vercel
1. Tạo repository mới trên GitHub.
2. Upload toàn bộ file trong thư mục này vào **gốc repository**.
3. Mở Vercel > Add New > Project > Import Git Repository.
4. Framework Preset: `Other`.
5. Build Command: để trống.
6. Output Directory: để trống hoặc `.`.
7. Bấm Deploy.

Vercel sẽ phục vụ trực tiếp `index.html`.

## Lưu ý
- Dữ liệu localStorage chỉ lưu trên từng trình duyệt/thiết bị; chưa đồng bộ cloud giữa điện thoại và máy tính.
- Google Translation API key chạy ở phía trình duyệt nên không nên dùng key production không giới hạn. Nếu phát hành rộng, nên chuyển dịch qua API backend/Vercel Function.
- `html2canvas` hiện tải từ CDN. Sau lần tải thành công, phần giao diện PWA cốt lõi vẫn có cache; chức năng xuất ảnh/PDF có thể cần Internet nếu thư viện chưa được browser cache.
- Word hiện là HTML `.doc`, đúng với bản Android gốc, không phải `.docx`.


## v2.3.1
- Cập nhật căn cứ biên bản vi phạm an toàn: “Tài liệu bàn giao quy định an toàn, cam kết an toàn”.
