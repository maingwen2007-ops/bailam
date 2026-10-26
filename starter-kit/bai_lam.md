# BÀI LÀM – THI THỬ HACKATHON 02 (GAMEZONE)

- **Họ tên: Lê Anh Duy** 
- **Lớp: CNTT3** 
- **[Link repository](https://github.com/maingwen2007-ops/bailam)**
- **Hệ điều hành (Windows/macOS): Windows** 

## 4.2. Thao tác CLI

### Các lệnh đã chạy

```powershell
# Ghi lệnh vào đây
pwd
ls -Recurse -Force
mv .\cap_nhat.txt .\docs\
mv .\logo_gamezone.PNG .\media\
rm .\temp_207.tmp -Force
cd .\logs\
ls -Force -Recurse
cd..
```

### Kết quả liệt kê toàn bộ dự án

```text
Directory: C:\game\de-on-tap-game\starter-kit\gamezone-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM            986 game.log

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```powershell
sls "ERROR" .\logs\game.log > .\logs\daily_report.txt
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
logs\game.log:2:2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
```

## 4.4. README.md

> Chấm trực tiếp trên `README.md` ở gốc dự án.

- [x] Heading 1
- [x] Mô tả in đậm + in nghiêng
- [x] Bảng `Thư mục | Nội dung` (≥3 dòng)
- [x] Code block lệnh liệt kê
- [ ] Task list (≥2 việc, ≥1 đã xong)
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report

### Lệnh chạy

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass 
.\auto_report.ps1

```

### Nội dung file logs/auto_report.txt

```text
2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```powershell
(Get-Content .\logs\game.log|sls "ERROR").count
```

### Kết quả đếm

```text
6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```powershell
"=== TONG HOP LOG GAMEZONE ===" > .\logs\tong_hop.txt
sls "WARNING" .\logs\game.log >> .\logs\tong_hop.txt
(sls "ERROR" .\logs\game.log).count >> .\logs\tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG GAMEZONE ===

logs\game.log:19:2025-11-05 08:54:15 [WARNING] May chu qua tai CPU 90%


6
```
## 4.8. Excel

> Chấm trực tiếp trên file `data/giao_dich_thang_11.xlsx`.
