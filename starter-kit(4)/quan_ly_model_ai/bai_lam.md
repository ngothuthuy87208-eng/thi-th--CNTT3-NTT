# BÀI LÀM –(CHỦ ĐỀ QUẢN LÝ MODEL AI)

- **Mã đề:**
- **Họ tên:**Ngô Thu thúy
- **Lớp:**CNTT3
- **Link repository:**Githup
- **Hệ điều hành (Windows/macOS):**Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
# 1.pwd
  2.ls -Force
  3.mv .\tai_lieu_ban_giao.txt .\docs
  4.mkdir .\backup
  5.cp .\data\chi_phi_model_thang_11.xlsx .\backup
  6.rm .\model_cache_01.tmp
  7.cd .\logs
   Get-content .\clinic.log
    cd..

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
PS C:\Users\MY LAPTOP\Downloads\starter-kit(4)\quan_ly_model_ai\logs> Get-ChildItem -Recurse -Force


    Directory: C:\Users\MY LAPTOP\Downloads\starter-kit(4)\quan_ly_model_ai\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        11/10/2026   1:41 PM           1234 Inference.log
```

## 4.3. Lọc log vận hành Model AI

### a) Lệnh lọc các dòng ERROR

```shell
# Get-Content logs/inference.log | Select-String "ERROR" > logs/loi_model.txt
Get-Content logs\loi_model.txt -TotalCount 2

```

### 2 dòng đầu tiên trong logs/loi_model.txt

```text
2026-11-01 09:01:12 INFO GET /lich-chieu
2026-11-01 09:04:25 INFO GET /gia-ve

```

### b) Lệnh đếm số dòng WARNING và kết quả

```shell
# Get-Content logs\inference.log | Select-String "WARNING" | Measure-Object

```

```text
Count    : 5
Average  :
Sum      :
Maximum  :
Minimum  :
Property :

```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
# Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\tong_hop.ps1

```

### Nội dung file logs/tong_hop.txt

```text
=== BAO CAO VAN HANH MODEL AI ===
2026-11-10 08:09:18 WARNING POST /v1/embeddings model=LLAMA-2-OLD
2026-11-10 08:16:05 WARNING GET /v1/fine-tune/jobs-legacy
2026-11-10 08:38:29 WARNING GET /images/model-card-v1.png
2026-11-10 09:01:44 WARNING POST /v1/completions model=DAVINCI-002
2026-11-10 09:14:02 WARNING GET /v1/quota/expired-key

Count    : 6
Average  :
Sum      :
Maximum  :
Minimum  :
Property :
```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] README.md: Heading 1, hình ảnh (`![Alt](path)`), mô tả có **in đậm**, _in nghiêng_ và `inline code`, bảng, code block, task list, blockquote
- [x] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [x] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | -------------------------- | --------------------------- | -------------- |
| 1   |                            |                             |                |
| 2   |                            |                             |                |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:**
- **Expected:**
- **Actual:**
- **Log:**

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/chi_phi_model_thang_11.xlsx`, không cần ghi vào đây.
