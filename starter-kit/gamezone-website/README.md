# Quản lý hệ thống web game GameZone
## 1. Bối cảnh
 Bạn là quản trị viên của web game **GameZone**. Máy chủ vừa ghi nhận nhiều sự cố trong **Game.log** và bạn *cần sắp xếp lại dữ liệu, lọc lỗi, viết tài liệu, viết script báo cáo và thống kê giao dịch vật phẩm trong Excel*.
## 2. Bảng
| Thư mục | Nội dung |
| --- | ---|
| `data` | chứa file excel giao_dich_thang_11.xlsx |
| `logs` | Chứa nhật kí báo cáo lỗi hàng ngày |
| `docs` | Các thông tin cập nhật mới |

```powershell
Get-ChildItem gamezone-website
```
> Tuyệt đối không upload file `.env`
