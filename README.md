
# KTTV Huế — Auto Upload Bản tin

Tự động đăng nhập và upload file PDF lên cổng: http://222.255.11.117:8888/UploadFile.aspx (Huế).

## Secrets cần thiết (Settings → Secrets → Actions):
- USERNAME = THUE
- PASSWORD = Hue2024@
- PORTAL_URL = http://222.255.11.117:8888/Login.aspx
- UPLOAD_URL = http://222.255.11.117:8888/UploadFile.aspx

## Sử dụng
- Đặt file PDF bản tin vào thư mục `bantin/`. Script sẽ chọn file mới nhất.
- Workflow chạy tự động 04:30 ICT hằng ngày, hoặc có thể Run workflow thủ công.
- Artifact: `after_upload.png` và `uploader.log` để kiểm tra.

## Cấu trúc
```
.github/workflows/upload.yml
tools/playwright_uploader.py
bantin/README.txt
.gitignore
README.md
```
