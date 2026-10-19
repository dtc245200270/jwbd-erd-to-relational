# Bài tập: Chuyển đổi ERD sang mô hình quan hệ

## Bước 1: Xác định các thực thể
- PHIEUXUAT (SoPX, NgayXuat)
- VATTU (MaVTU, TenVTU)
- PHIEUNHAP (SoPN, NgayNhap)
- DONDH (SoDH, NgayDH)
- NHACC (MaNCC, TenNCC, DiaChi, SDT)

## Bước 2: Xác định các mối quan hệ
- N - N giữa PHIEUXUAT và VATTU -> Bảng CHITIET_PHIEUXUAT (SoPX, MaVTU, DGXuat, SLXuat)
- N - N giữa PHIEUNHAP và VATTU -> Bảng CHITIET_PHIEUNHAP (SoPN, MaVTU, DGNhap, SLNhap)
- N - N giữa DONDH và VATTU -> Bảng CHITIET_DONDH (SoDH, MaVTU)
- 1 - N giữa NHACC và DONDH -> Thêm MaNCC vào DONDH

## Bước 3: Thuộc tính đa trị
- NHACC có thuộc tính đa trị SDT -> Bảng NHACC_SDT (MaNCC, SDT)

## Bước 4: Danh sách các bảng quan hệ
1. PHIEUXUAT (SoPX, NgayXuat)
2. VATTU (MaVTU, TenVTU)
3. PHIEUNHAP (SoPN, NgayNhap)
4. NHACC (MaNCC, TenNCC, DiaChi)
5. NHACC_SDT (MaNCC, SDT)
6. DONDH (SoDH, NgayDH, MaNCC)
7. CHITIET_PHIEUXUAT (SoPX, MaVTU, DGXuat, SLXuat)
8. CHITIET_PHIEUNHAP (SoPN, MaVTU, DGNhap, SLNhap)
9. CHITIET_DONDH (SoDH, MaVTU)
