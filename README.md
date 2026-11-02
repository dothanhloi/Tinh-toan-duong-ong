# Tính toán đường ống tưới

Ứng dụng web (1 file `index.html`, không cần cài đặt) giúp chọn **phi (Ø) ống** cho hệ thống **tưới nhỏ giọt** hoặc **tưới béc** cho vườn **nhiều khu khác nhau**, mạng ống **nhiều nhánh**, địa hình **có chênh cao**, và **so sánh phương án bơm**.

## Chức năng
- **Mạng ống chính & nhánh**: mỗi đoạn đi từ Bơm hoặc một điểm đã có (Đ1, Đ2…) tới điểm mới, với chiều dài và cao độ. Nhiều đoạn cùng đi từ một điểm là rẽ nhánh.
- **Nhu cầu nước cây trồng**: bảng tra 17 loại cây phổ biến ở Việt Nam (cà phê vối, cà phê chè, hồ tiêu, sầu riêng, bơ, mắc ca, điều, xoài, cây có múi, nhãn/vải, chôm chôm, mít, chuối, thanh long, chanh dây, ca cao, ổi) với Kc, khoảng cách, tán, lít/cây/ngày, m³/ha/ngày, đầu tưới gợi ý, số ngày giữ ẩm tối đa và lưu ý canh tác. Nhu cầu = ETo (theo vùng: Tây Nguyên, Lâm Đồng, Đông Nam Bộ, Nam Trung Bộ, ĐBSCL, miền Bắc…) × Kc × Kr (độ che phủ tán, nên cây non cần ít hơn) × diện tích cây ÷ hiệu suất tưới × mức tưới. Lượng nước mỗi lần = nhu cầu ngày × chu kỳ; kiểm tra đất giữ ẩm đủ cho chu kỳ (theo loại đất, độ sâu rễ, phần diện tích được làm ướt) và đầu tưới làm ướt đủ diện tích.
- **Các khu tưới khác nhau**: mỗi khu có tên, điểm nối, số khu giống nhau (SL) và thông số riêng: cây trồng (mẫu cà phê / tiêu / sầu riêng), kiểu tưới (nhỏ giọt / béc), số đầu/cây, lưu lượng và áp đầu tưới (thường hoặc bù áp), khoảng cách hàng/cây, số cây/hàng, số hàng, vị trí cấp nước, độ dốc dọc hàng và dọc ống nhánh, vật liệu ống tưới / ống nhánh, lượng nước mỗi gốc. Sửa, nhân bản, xóa khu ngay trong bảng.
- Mỗi khu được thiết kế riêng: ống tưới và ống nhánh cấp 2 tính từng đầu tưới một (lưu lượng giảm dần, cộng/trừ chênh cao) → lưu lượng khu, áp cần tại điểm nối, thời gian tưới.
- **Ống to trước – nhỏ dần, tối ưu chi phí**: quy hoạch động trên cây đường ống + tìm kiếm cục bộ chính xác chọn cách phối cỡ ống **rẻ nhất** thỏa vận tốc, đủ áp cho từng khu trong lượt của nó, áp tối thiểu ở đỉnh đồi, cột áp bơm trong giới hạn; nhánh không to hơn ống phía trước. So sánh với phương án mỗi tuyến đi 1 cỡ.
- **So sánh phương án vận hành**: từ 1 lượt (mở tất cả khu, bơm lớn) đến từng khu một (bơm nhỏ), chia lượt tự động (rải đều các nhánh / theo cụm) hoặc **tự xếp lượt** cho từng khu. Mỗi phương án tính ống, bơm (theo lượt nặng nhất), điện năng theo thể tích nước × cột áp từng lượt, thời gian tưới xong 1 vòng (mỗi lượt dài bằng khu lâu nhất); cảnh báo vượt **nguồn nước** hoặc **quá số ngày cho phép**; ★ phương án có tổng chi phí (ống + bơm + điện N năm) thấp nhất.
- Lịch tưới từng lượt, cỡ ống từng đoạn, cấp áp PN, mặt cắt dọc theo tuyến và lượt, bảng áp tại từng điểm, gợi ý van xả khí / xả cặn / van điều áp.
- So sánh tổn thất cho phép ↔ tiền ống ↔ bơm ↔ tiền điện.
- **Tính nhanh 1 đoạn**: lưu lượng + chiều dài + chênh cao → Ø ống và áp cần ở đầu đoạn.
- Danh mục ống: PE mềm/LDPE (16–32), HDPE PE100 PN10 (20–200), PVC-U hệ Bình Minh/Tiền Phong (21–220). Giá ống = khối lượng × đơn giá/kg; giá bơm theo triệu đ/HP (nhập giá đại lý).
- Dữ liệu nhập được lưu trên trình duyệt (dữ liệu từ bản trước được tự chuyển sang danh sách khu).

## Cách dùng
Mở `index.html` bằng trình duyệt (máy tính hoặc điện thoại). Có thể đưa lên GitHub Pages hoặc chèn vào website WordPress.
Hướng dẫn chi tiết từng bước: xem [HUONG_DAN.md](HUONG_DAN.md). Trong app có mục “Hướng dẫn nhanh” ở đầu khung nhập liệu và nút “Làm lại từ ví dụ mẫu”.

## Công thức chính
- Tổn thất Hazen–Williams `h = 10,67·L·Q^1,852 / (C^1,852·D^4,87)`, cộng tổn thất cục bộ (%).
- Dao động áp cho phép trong khu: 20% áp đầu tưới (đầu thường); với đầu bù áp là khoảng giữa áp tối thiểu và áp tối đa của đầu.
- Lưu lượng thiết kế mỗi đoạn = lưu lượng lớn nhất qua đoạn đó trong các lượt.
- Ràng buộc mạng: `cột áp tại cửa bơm ≤ max(cao độ + áp cần) + tổn thất cho phép (m/100 m × tuyến dài nhất)`.
- Bơm `H = độ sâu hút + lọc + cột áp cửa bơm`, `P = 9,81·Q·H / η`; điện năng mỗi lượt `= 9,81·V·H / (3600·η·0,85)` kWh; áp lớn nhất khi đóng van ≈ 1,2 × H.

Kết quả để thiết kế sơ bộ; độ dày thành ống, giá ống và giá bơm là giá trị tham khảo — đối chiếu catalogue và báo giá nhà sản xuất.
