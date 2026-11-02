# Tính toán đường ống tưới

Ứng dụng web (1 file `index.html`, không cần cài đặt) giúp chọn **phi (Ø) ống** cho hệ thống **tưới nhỏ giọt** hoặc **tưới béc**, kể cả trên **địa hình có chênh cao**.

## Chức năng
- **Cả hệ thống**
  - Thiết kế 1 khu tưới: kiểu tưới, số đầu tưới/cây, lưu lượng và áp đầu tưới (thường hoặc bù áp), khoảng cách hàng/cây, số cây/hàng, số hàng, vị trí cấp nước (đầu/giữa), **độ dốc dọc hàng và dọc ống nhánh**.
  - Ống tưới và ống nhánh được tính **từng đầu tưới một** (lưu lượng giảm dần, cộng/trừ chênh cao), cho ra dao động áp thực tế và áp cần tại đầu khu.
  - **Tuyến ống chính nhiều đoạn**: mỗi đoạn có chiều dài, cao độ điểm cuối (so với bơm) và số khu lấy nước. Vận hành: mở cùng lúc hoặc tưới lần lượt.
  - **Ống chính đi to trước, nhỏ dần**: tối ưu (quy hoạch động) để **tổng tiền ống thấp nhất**. Ràng buộc: vận tốc, đủ áp mọi khu, áp tối thiểu ở đỉnh đồi, cột áp bơm không vượt mức cho phép. So sánh với phương án đi 1 cỡ suốt tuyến.
  - Mặt cắt dọc tuyến (cao độ ống và đường áp), bảng áp tại từng điểm, gợi ý van xả khí / xả cặn / van điều áp, **cấp áp PN theo từng đoạn**.
  - So sánh **tổn thất cho phép ↔ tiền ống ↔ tiền điện 10 năm** để chọn phương án kinh tế.
  - Cột áp, công suất bơm, thời gian tưới.
- **Tính nhanh 1 đoạn**: lưu lượng + chiều dài + chênh cao → Ø ống và áp cần ở đầu đoạn.
- Mẫu có sẵn: cà phê nhỏ giọt, cà phê béc gốc, tiêu nhỏ giọt, sầu riêng béc.
- Danh mục ống: PE mềm/LDPE (16–32), HDPE PE100 PN10 (20–200), PVC-U hệ Bình Minh/Tiền Phong (21–220). Giá ống tính theo khối lượng × đơn giá/kg (nhập giá đại lý).
- Dữ liệu nhập được lưu trên trình duyệt.

## Cách dùng
Mở `index.html` bằng trình duyệt (máy tính hoặc điện thoại). Có thể đưa lên GitHub Pages hoặc chèn vào website WordPress.

## Công thức
- Tổn thất Hazen–Williams `h = 10,67·L·Q^1,852 / (C^1,852·D^4,87)`, cộng tổn thất cục bộ (%).
- Dao động áp cho phép trong khu: 20% áp đầu tưới (đầu thường); với đầu bù áp là khoảng giữa áp tối thiểu và áp tối đa của đầu.
- Ống chính: chia tuyến thành đoạn ngắn, duyệt mọi cách phối cỡ ống không tăng dần theo chiều nước chảy, chọn cách rẻ nhất thỏa
  `cột áp tại cửa bơm ≤ max(cao độ + áp cần) + tổn thất cho phép`.
- Bơm `H = độ sâu hút + lọc + cột áp cửa bơm`, `P = 9,81·Q·H / η`; áp lớn nhất khi đóng van ≈ 1,2 × H.

Kết quả để thiết kế sơ bộ; độ dày thành ống và giá là giá trị tham khảo — đối chiếu catalogue và báo giá nhà sản xuất.
