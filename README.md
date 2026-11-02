# Tính toán đường ống tưới

Ứng dụng web (1 file `index.html`, không cần cài đặt) giúp chọn **phi (Ø) ống** cho hệ thống **tưới nhỏ giọt** hoặc **tưới béc**:

- **Cả hệ thống**: nhập kiểu tưới, số đầu tưới/cây, lưu lượng đầu tưới, khoảng cách hàng/cây, số cây/hàng, số hàng/khu, số khu → tính Ø **ống tưới**, **ống nhánh (cấp 2)**, **ống chính**, cột áp và công suất **bơm**, thời gian tưới mỗi khu.
- **Tính nhanh 1 đoạn**: nhập lưu lượng + chiều dài → Ø ống phù hợp.
- Mẫu có sẵn: cà phê nhỏ giọt, cà phê béc gốc, tiêu nhỏ giọt, sầu riêng béc.
- Danh mục ống: PE mềm/LDPE (16–32), HDPE PE100 PN10 (20–200), PVC-U hệ Bình Minh/Tiền Phong (21–220).

## Cách dùng
Mở `index.html` bằng trình duyệt (máy tính hoặc điện thoại). Có thể đưa lên GitHub Pages hoặc chèn vào website WordPress.

## Công thức
- Ø trong tối thiểu theo vận tốc: `D = √(4Q / πv)`, v ≤ 1,5 m/s.
- Tổn thất áp Hazen–Williams `h = 10,67·L·Q^1,852 / (C^1,852·D^4,87)` × hệ số Christiansen F (ống nhiều cửa ra).
- Dao động áp cho phép trong khu: 20% áp đầu tưới (đầu thường), 45% (đầu bù áp).
- Công suất bơm `P = 9,81·Q·H / η`.

Kết quả để thiết kế sơ bộ; độ dày thành ống là giá trị điển hình — đối chiếu catalogue nhà sản xuất.
