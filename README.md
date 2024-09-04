# mysql002

## 1. KhachHang
### Columns:
MaKH (Primary Key)
TaiKhoan
MatKhau
Email
DiaChi
DienThoai
GioiTinh
NgaySinh
HoTen
## 2. DonHang
### Columns:
MaDonHang (Primary Key)
NgayGiao
NgayDat
TinhTrangGH
DaThanhToan
MaKH (Foreign Key referencing KhachHang.MaKH)
## 3. Sach
### Columns:
MaSach (Primary Key)
TenSach
GiaBan
AnhBia
MoTa
NgayCapNhat
SoLuongTon
MaChuDe (Foreign Key referencing ChuDe.MaChuDe)
MaNSX (Foreign Key referencing NhaXuatBan.MaNSX)
## 4. ChuDe
### Columns:
MaChuDe (Primary Key)
TenChuDe
## 5. NhaXuatBan
### Columns:
MaNSX (Primary Key)
TenNSX
DienThoai
DiaChi 
## 6. TacGia
### Columns:
MaTacGia (Primary Key)
TenTacGia
DienThoai
TieuSu
DiaChi
## 7. Sach_TacGia
### Columns:
MaSach (Foreign Key referencing Sach.MaSach)
MaTacGia (Foreign Key referencing TacGia.MaTacGia)
VaiTro
ViTri
Composite Primary Key:
MaSach, MaTacGia
## 8. DonHang_Sach
### Columns:
MaDonHang (Foreign Key referencing DonHang.MaDonHang)
MaSach (Foreign Key referencing Sach.MaSach)
SoLuong (Quantity)
DonGia (Unit Price)
Composite Primary Key:
MaDonHang, MaSach

## Relationships:
One-to-Many between KhachHang and DonHang
Many-to-Many between Sach and TacGia through TacGia_Sach.
Many-to-Many between DonHang and Sach through DonHang_Sach.
One-to-Many between NhaXuatBan and Sach.
One-to-Many between ChuDe and Sach.
