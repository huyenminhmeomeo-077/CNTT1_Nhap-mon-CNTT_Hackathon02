# BÀI LÀM – HACKATHON 02

- **Mã đề:** 05
- **Họ tên:Đặng Minh Huyền**
- **Lớp:CNTT1**
- **Link repository:https://github.com/huyenminhmeomeo-077/CNTT1_Nhap-mon-CNTT_Hackathon02**
- **Hệ điều hành (Windows/macOS):MacOs**

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
# Ghi lần lượt các lệnh đã chạy, mỗi lệnh một dòng
pwd 
ls -a 
mv quy_dinh_thue.txt docs/
mkdir backup 
cp data/don_thue_thang_5.xlsx backup/
rm .tmp
cd ./logs
ls -a
cd ..
ls -aR
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
(Dán kết quả vào đây – xoá dòng này)
.			.env			data			logs
..			backup			docs			temp_505.tmp
.DS_Store		bai_lam 07.38.22.md	evidence		web

./backup:
.			..			don_thue_thang_5.xlsx

./data:
.			..			.~don_thue_thang_5.xlsx	don_thue_thang_5.xlsx

./docs:
.			..			quy_dinh_thue.txt

./evidence:
.	..

./logs:
.		..		loi_500.txt	rental.log	tong_hop.txt

./web:
.		..		app.js		images		index.html	style.css

./web/images:
.		..		logo-campgo.png


## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500

```shell
# Ghi lệnh vào đây (xoá dòng này)
grep "ERROR" logs/rental.log > logs/loi_500.txt 
head -2 logs/loi_500.txt

```

### 2 dòng đầu tiên trong logs/loi_500.txt

```text
(Dán kết quả vào đây – xoá dòng này)
2026-11-11 08:27:45 ERROR POST /v1/chat/completions rental=CLAUDE-35
2026-11-11 08:31:12 ERROR POST /v1/audio/transcriptions rental=WHISPER-V3

```

### b) Lệnh đếm số dòng status=404 và kết quả

```shell
# Ghi lệnh vào đây (xoá dòng này)
cat logs/rental.log | grep "WARNING" | wc -1 
```

```text
(Dán kết quả đếm vào đây – xoá dòng này)
wc: illegal option -- 1
usage: wc [-Lclmw] [file ...]

```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
# Ghi lệnh vào đây (xoá dòng này)
chomd +x tong_hop.txt
bash tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```text
(Dán nội dung file vào đây – xoá dòng này)
# Script: tong_hop.txt
# Tac gia: Dang Minh Huyen
# Ngay tao: 2026-11-11
echo "Dang tao bao cao..."
echo "=== BAO CAO SU CO WEBSITE ===" > logs/tong_hop.txt
cat logs/rental.log | grep "WARNING" >> logs/tong_hop.txt
cat logs/rental.log | grep "ERROR" | wc -l >> logs/tong_hop.txt
echo "Hoan thanh!"
```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [x] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [x] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 |  |  |  |
| 2 |  |  |  |

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

> Phần Excel được chấm trực tiếp trên file `data/don_thue_thang_5.xlsx`, không cần ghi vào đây.
