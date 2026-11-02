# Tính toán đường ống tưới

Ứng dụng web (1 file `index.html`, không cần cài đặt) giúp chọn **phi (Ø) ống** cho hệ thống **tưới nhỏ giọt** hoặc **tưới béc**, kể cả trên **địa hình có chênh cao**, vườn rộng chia **nhiều khu, nhiều nhánh ống**, và **so sánh phương án bơm**.

## Chức năng
- **Thiết kế 1 khu tưới**: kiểu tưới, số đầu tưới/cây, lưu lượng và áp đầu tưới (thường hoặc bù áp), khoảng cách hàng/cây, số cây/hàng, số hàng, vị trí cấp nước (đầu/giữa), độ dốc dọc hàng và dọc ống nhánh. Ống tưới và ống nhánh cấp 2 được tính từng đầu tưới một (lưu lượng giảm dần, cộng/trừ chênh cao).
- **Mạng ống chính nhiều nhánh**: mỗi đoạn đi từ Bơm hoặc một điểm đã có (Đ1, Đ2…) tới điểm mới, với chiều dài, cao độ và số khu lấy nước. Nhiều đoạn cùng đi từ một điểm là rẽ nhánh.
- **Ống to trước – nhỏ dần, tối ưu chi phí**: quy hoạch động trên cây đường ống + tìm kiếm cục bộ chính xác chọn cách phối cỡ ống **rẻ nhất** thỏa vận tốc, đủ áp mọi khu, áp tối thiểu ở đỉnh đồi, cột áp bơm trong giới hạn; nhánh không to hơn ống phía trước. So sánh với phương án mỗi tuyến đi 1 cỡ.
- **So sánh phương án vận hành**: từ 1 lượt (mở tất cả khu, bơm lớn, ống lớn) đến nhiều lượt (bơm nhỏ, ống nhỏ, tưới lâu hơn). Mỗi phương án tính lại ống, bơm (theo lượt nặng nhất), điện năng từng lượt, thời gian tưới xong 1 vòng; cảnh báo vượt **nguồn nước** hoặc **quá số ngày cho phép**; chọn ★ phương án có tổng chi phí (ống + bơm + điện N năm) thấp nhất. Chia lượt “rải đều các nhánh” (ống nhỏ nhất) hoặc “theo cụm”.
- Lịch tưới từng lượt, cỡ ống từng đoạn, cấp áp PN, mặt cắt dọc theo tuyến và lượt, bảng áp tại từng điểm, gợi ý van xả khí / xả cặn / van điều áp.
- So sánh tổn thất cho phép ↔ tiền ống ↔ bơm ↔ tiền điện.
- **Tính nhanh 1 đoạn**: lưu lượng + chiều dài + chênh cao → Ø ống và áp cần ở đầu đoạn.
- Mẫu có sẵn: cà phê nhỏ giọt, cà phê béc gốc, tiêu nhỏ giọt, sầu riêng béc.
- Danh mục ống: PE mềm/LDPE (16–32), HDPE PE100 PN10 (20–200), PVC-U hệ Bình Minh/Tiền Phong (21–220). Giá ống = khối lượng × đơn giá/kg; giá bơm theo triệu đ/HP (nhập giá đại lý).
- Dữ liệu nhập được lưu trên trình duyệt.

## Cách dùng
Mở `index.html` bằng trình duyệt (máy tính hoặc điện thoại). Có thể đưa lên GitHub Pages hoặc chèn vào website WordPress.

## Công thức chính
- Tổn thất Hazen–Williams `h = 10,67·L·Q^1,852 / (C^1,852·D^4,87)`, cộng tổn thất cục bộ (%).
- Dao động áp cho phép trong khu: 20% áp đầu tưới (đầu thường); với đầu bù áp là khoảng giữa áp tối thiểu và áp tối đa của đầu.
- Lưu lượng thiết kế mỗi đoạn = lưu lượng lớn nhất qua đoạn đó trong các lượt.
- Ràng buộc mạng: `cột áp tại cửa bơm ≤ max(cao độ + áp cần) + tổn thất cho phép (m/100 m × tuyến dài nhất)`.
- Bơm `H = độ sâu hút + lọc + cột áp cửa bơm`, `P = 9,81·Q·H / η`; áp lớn nhất khi đóng van ≈ 1,2 × H.

Kết quả để thiết kế sơ bộ; độ dày thành ống, giá ống và giá bơm là giá trị tham khảo — đối chiếu catalogue và báo giá nhà sản xuất.
