# Hướng dẫn sử dụng app Tính ống tưới

App giúp thiết kế sơ bộ hệ thống **tưới nhỏ giọt / tưới béc** cho vườn có nhiều khu, nhiều nhánh ống, địa hình dốc. App tính:

- lượng nước mỗi cây cần;
- phi ống tưới, ống nhánh, ống chính (đi to trước, nhỏ dần);
- bơm cần bao nhiêu HP;
- nên tưới mấy lượt cho rẻ nhất.

---

## 1. Mở app

- Mở file `index.html` bằng Chrome, Cốc Cốc, Edge hoặc Safari, trên máy tính hay điện thoại đều được. Không cần cài đặt, không cần mạng.
- Mọi thứ bạn nhập được **tự lưu trên trình duyệt** của máy đó. Lần sau mở lại vẫn còn.
- Muốn xóa hết để bắt đầu lại: bấm **“↺ Làm lại từ ví dụ mẫu”** ở cuối khung nhập liệu.

Màn hình có 2 phần:

| Phần | Vị trí | Nội dung |
|---|---|---|
| Nhập liệu | Bên trái (điện thoại: phía trên) | 5 bước nhập, đánh số 1–5 |
| Kết quả | Bên phải (điện thoại: phía dưới) | Tự tính lại ngay mỗi khi bạn sửa một ô |

Có 2 chế độ ở trên cùng:

- **Cả hệ thống**: thiết kế toàn bộ vườn.
- **Tính nhanh 1 đoạn**: chọn phi cho một đoạn ống riêng lẻ (xem mục 8).

---

## 2. Bước 1 – Mạng ống chính & các nhánh

Mỗi dòng là **một đoạn ống**:

| Cột | Ý nghĩa |
|---|---|
| **Điểm** | Tên điểm cuối của đoạn: Đ1, Đ2… (app tự đặt) |
| **Đi từ** | Đoạn bắt đầu từ đâu: **Bơm** hoặc một điểm đã có |
| **Dài (m)** | Chiều dài đoạn ống |
| **Cao độ (m)** | Độ cao điểm cuối **so với chỗ đặt bơm**: cao hơn bơm ghi số dương, thấp hơn ghi số âm |
| **Khu nối vào** | Các khu lấy nước tại điểm này (app tự hiện) |

- **Rẽ nhánh**: cho nhiều đoạn cùng “Đi từ” một điểm. Ví dụ Đ2 và Đ4 cùng đi từ Đ1 là 2 nhánh tách ra ở Đ1.
- **Thêm đoạn**: bấm “+ Thêm đoạn”. **Xóa**: bấm ×. Các nhánh và khu nối ở điểm bị xóa sẽ tự chuyển về điểm phía trước.
- **Mẹo**: đặt điểm ở chỗ có khu lấy nước, ở đỉnh đồi và chỗ trũng, để app tính đúng áp và gợi ý van xả khí, van xả cặn.
- **Đo cao độ**: dùng GPS trên điện thoại, Google Earth, hoặc ống nước thăng bằng.

Ví dụ mẫu:

```
Bơm ─150 m─ Đ1 (+4 m) ─200 m─ Đ2 (+14 m) ─150 m─ Đ3 (+8 m)
              └──────220 m──────── Đ4 (−3 m)
```

---

## 3. Bước 2 – Các khu tưới

Mỗi dòng là **một khu tưới**, tức phần vườn mở bằng một van:

| Cột / nút | Ý nghĩa |
|---|---|
| **Tên khu** | Đặt tên dễ nhớ: “Cà phê lô A”, “Sầu riêng sau nhà”… |
| **Nối vào** | Điểm trên mạng ống mà khu lấy nước (chỗ đặt van khu). Có thể chọn “Bơm” nếu khu ở sát bơm |
| **SL** | Số khu giống hệt nhau nối cùng điểm đó (thường là 1) |
| **Lượt** | Chỉ hiện khi chọn “Tự xếp lượt” ở bước 5 |
| ✎ | Mở khu ra sửa chi tiết |
| ⧉ | Nhân bản khu, tiện khi các khu gần giống nhau |
| × | Xóa khu |

---

## 4. Bước 3 – Sửa chi tiết từng khu (khung viền xanh “Đang sửa”)

1. **Cây trồng**: chọn 1 trong 17 loại (cà phê vối, cà phê chè, hồ tiêu, sầu riêng, bơ, mắc ca, điều, xoài, cam/quýt/bưởi, nhãn/vải, chôm chôm, mít, chuối, thanh long, chanh dây, ca cao, ổi). App **điền sẵn** khoảng cách trồng, đường kính tán, kiểu và số đầu tưới. Sau đó **sửa lại theo vườn thật**. Cây không có trong danh sách thì chọn “Cây khác” và tự nhập lượng nước.
2. **Đường kính tán hiện tại**: cây non tán nhỏ thì nhập nhỏ. App sẽ tính ít nước hơn.
3. **Lượng nước mỗi lần tưới**:
   - **Theo nhu cầu cây** (nên dùng): app tự tính.
   - **Tự nhập**: nhập lít/gốc/lần theo kinh nghiệm. App vẫn báo nếu lượng này thiếu so với nhu cầu.
4. **Kiểu tưới & đầu tưới**:
   - nhỏ giọt hay béc;
   - số đầu tưới mỗi cây;
   - lưu lượng một đầu (lít/giờ);
   - áp làm việc (m cột nước; 1 bar ≈ 10 m);
   - đầu tưới có bù áp không. Nếu có, nhập áp tối đa của đầu theo thông số nhà sản xuất.
5. **Bố trí & độ dốc**:
   - khoảng cách hàng, khoảng cách cây, số cây mỗi hàng, số hàng trong khu;
   - ống nhánh cấp vào **giữa hàng** hay **đầu hàng**;
   - ống chính nối vào giữa hay đầu ống nhánh;
   - **độ dốc dọc hàng** và **dọc ống nhánh** (%): + là lên dốc, − là xuống dốc theo chiều nước chảy. 5% nghĩa là 100 m chênh 5 m;
   - vật liệu ống tưới và ống nhánh cấp 2.

> Khi khu nằm trên dốc, nên cấp nước từ **đầu cao** chạy xuống. Cấp ở giữa thì một nửa lên dốc, một nửa xuống dốc, nên áp chênh gấp đôi.

---

## 5. Bước 4 – Nhu cầu nước tưới (mục 3 trong app)

| Ô | Cách nhập |
|---|---|
| **Vùng khí hậu** | Chọn vùng; app tự điền ETo (lượng nước bốc hơi chuẩn lúc cao điểm mùa khô). Có số liệu trạm khí tượng gần vườn thì nhập tay ô ETo |
| **Loại đất** | Đất đỏ bazan, xám/cát pha, cát, phù sa/thịt, sét. Đất càng giữ nước kém thì càng phải tưới dày |
| **Chu kỳ tưới** | Bao nhiêu ngày tưới lại một lần. **Cả vườn phải tưới xong 1 vòng trong chu kỳ này** |
| **Mức tưới (%)** | 100% = đủ nhu cầu. Vườn có tủ gốc có thể để 65–70% |
| **Số ngày cần tưới/năm** | Số ngày mùa khô phải tưới, dùng để tính tiền điện |

---

## 6. Bước 5 – Phương án vận hành (mục 4 trong app)

| Ô | Cách nhập |
|---|---|
| **Nguồn nước tối đa (m³/giờ)** | Giếng hoặc hồ bơm được bao nhiêu. Để trống nếu không giới hạn |
| **Số giờ bơm tối đa/ngày** | Ví dụ 20 giờ (chừa thời gian nghỉ máy, cắt điện) |
| **Chia khu vào các lượt** | **Tự động rải đều các nhánh** (nên dùng, ống nhỏ nhất); **Theo cụm** (tưới hết khu gần nhau rồi mới sang cụm khác); **Tự xếp lượt** (nhập số lượt cho từng khu ở cột “Lượt”) |
| **Phương án xem chi tiết** | Để “★ Tự chọn phương án kinh tế nhất”, hoặc chọn số lượt muốn xem |

---

## 7. Bước 6 – Bơm & chi phí (mục 5 trong app)

- **Độ sâu hút**: từ mặt nước giếng hoặc hồ lên tới bơm (m).
- **Tổn thất bộ lọc + châm phân**: thường 3–7 m.
- **Hiệu suất bơm**: thường 55–70%.
- **Giá bơm + tủ điện (triệu đ/HP)**, **giá điện (đ/kWh)**, **số năm để so sánh**.
- **Vật liệu ống chính** và **giá ống theo kg** (PVC, HDPE, PE mềm): nhập giá đại lý để so sánh tiền sát thực tế.

**Tiêu chí thiết kế (nâng cao)**: chỉ sửa khi bạn nắm rõ. Mặc định là vận tốc nước ≤ 1,5 m/s, dao động áp trong khu ≤ 20%, tổn thất cho phép ống chính 2 m/100 m.

---

## 8. Đọc kết quả

### 8.1 Ô tóm tắt (trên cùng)
Phương án đang xem cho biết:

- **bơm**: lưu lượng, cột áp, số HP nên chọn;
- **tiền đầu tư**: ống chính, ống nhánh và bơm;
- **thời gian tưới xong 1 vòng**;
- **tiền điện mỗi năm**.

### 8.2 Bảng tra nhu cầu nước (17 loại cây)
Bảng cho mỗi cây: lít/cây/ngày, lít/cây/lần, m³/ha/ngày, đầu tưới gợi ý, số ngày đất giữ ẩm tối đa, lưu ý canh tác. Bấm **“Dùng”** để áp cây đó cho khu đang sửa.

### 8.3 So sánh phương án: bơm lớn 1 lượt ↔ bơm nhỏ nhiều lượt
- **Biểu đồ cột** tổng chi phí N năm, chia thành tiền ống, tiền bơm và tiền điện. Rê chuột hoặc chạm vào cột để xem số.
- **Bảng** cho mỗi phương án: lưu lượng, cột áp, HP của bơm; tiền ống; tiền bơm; thời gian tưới 1 vòng; điện/năm; tổng chi phí.
- **★** là phương án rẻ nhất mà vẫn đạt điều kiện. **⚠** là phương án không đạt: vượt nguồn nước, hoặc không tưới kịp trong chu kỳ.
- **Bấm vào một phương án** để xem chi tiết phía dưới.

### 8.4 Ống chính & nhánh của phương án đang xem
- **Lịch tưới**: mỗi lượt mở những khu nào, lưu lượng, cột áp bơm, công suất, thời gian.
- **Cỡ ống từng đoạn**: ví dụ “Bơm → Đ1: **Ø90** 150 m”. Một đoạn có thể có 2 cỡ, to trước rồi nhỏ dần. Kèm theo là **cấp áp PN** nên mua và tiền ống. App so sánh với cách đi một cỡ suốt tuyến để cho biết **tiết kiệm được bao nhiêu**.
- **Mặt cắt dọc**: chọn **Tuyến** và **Lượt**. Đường xanh dương là áp trong ống, đường cam là độ cao ống. Chấm xanh lá (áp cần tại khu) phải nằm **dưới** đường xanh dương. Rê chuột hoặc chạm để xem áp từng chỗ.
- **Bảng các điểm**: áp lúc tưới, áp cần, và ghi chú lắp **van xả khí** (điểm cao), **van xả cặn** (điểm trũng, cuối nhánh), **van điều áp** (khu dư áp).
- **So sánh tổn thất cho phép ↔ tiền ống ↔ bơm ↔ tiền điện**: cho thấy đi ống nhỏ hơn thì bơm phải mạnh hơn và tốn điện hơn bao nhiêu.

### 8.5 Các khu tưới
- **Bảng tổng hợp** từng khu: cây trồng, số cây, diện tích, lít/cây/ngày, lít/cây/lần, giờ mỗi lần tưới, phi ống tưới, phi ống nhánh, lưu lượng, áp cần, lượt, trạng thái.
- **Bấm tên khu** để xem chi tiết:
  - thẻ **Nhu cầu nước**: cách tính, số ngày đất giữ ẩm, lưu ý canh tác;
  - thẻ **Ống tưới** và **Ống nhánh cấp 2**, có bảng so sánh các cỡ ống.

---

## 9. Cảnh báo thường gặp và cách xử lý

| Cảnh báo | Cách xử lý |
|---|---|
| Chu kỳ … dài hơn khả năng giữ ẩm của đất | Giảm chu kỳ tưới, hoặc thêm đầu tưới / dùng béc để làm ướt rộng hơn |
| Đầu tưới chỉ làm ướt X% diện tích | Tăng số đầu tưới mỗi cây (nên ướt ≥ 1/3 diện tích) |
| Mỗi lần tưới khu này mất X giờ, quá số giờ bơm/ngày | Tăng số đầu hoặc lưu lượng đầu tưới, rút ngắn chu kỳ, hoặc chia nhỏ khu |
| Lượng tự nhập chỉ đáp ứng X% nhu cầu | Tăng lượng nước, hoặc chuyển sang “Theo nhu cầu cây” |
| Ống tưới / ống nhánh “Không cỡ nào đạt” | Thường do dốc: dùng đầu bù áp, đi ống theo đường đồng mức, rút ngắn hàng, cấp nước từ đầu cao |
| ⚠ vượt nguồn nước | Tăng số lượt tưới (mỗi lượt mở ít khu hơn) |
| ⚠ không kịp tưới hết vườn trong chu kỳ | Giảm số lượt (bơm lớn hơn), tăng giờ bơm/ngày, hoặc tăng chu kỳ nếu đất giữ ẩm cho phép |
| Dư tới X m: lắp van điều áp | Lắp van điều áp đầu khu, hoặc khóa bớt van khu |
| Cột áp bơm khá cao | Đặt bơm tăng áp giữa tuyến, chia khu theo độ cao, hoặc tăng cỡ ống chính |

---

## 10. Tính nhanh 1 đoạn

Dùng khi chỉ cần chọn phi cho một đoạn ống:

1. Chọn cách nhập lưu lượng: **số đầu tưới × lưu lượng 1 đầu**, hoặc nhập thẳng **m³/giờ**.
2. Nhập chiều dài, kiểu chia nước (nhiều cửa ra rải đều, hoặc dẫn thẳng ra 1 điểm), chênh cao cuối − đầu, áp cần ở cuối đoạn, vật liệu, vận tốc tối đa. Nếu muốn, nhập thêm tổn thất ma sát tối đa.
3. App cho ra: phi ống phù hợp, đường kính trong tối thiểu, **áp cần ở đầu đoạn**, và bảng so sánh các cỡ ống.

---

## 11. Ví dụ mẫu có sẵn

Mạng 4 đoạn như hình ở mục 2, với 5 khu: Cà phê A, Cà phê C ở Đ2; Cà phê B ở Đ3; Sầu riêng và Tiêu ở Đ4. Tây Nguyên, đất bazan, chu kỳ 3 ngày.

| Phương án | Bơm | Tưới 1 vòng | Tổng 10 năm |
|---|---|---|---|
| 1 lượt (mở cả 5 khu) | 76,7 m³/h · 20 HP | 7 giờ | 208 triệu |
| 3 lượt | 36,7 m³/h · 10 HP | 21 giờ | 158 triệu |
| **5 lượt ★** | 24 m³/h · 7,5 HP | 31 giờ | **139 triệu** |

Với phương án 5 lượt:

- **Ống**: Bơm → Đ1 Ø90; Đ1 → Đ2 Ø75; Đ2 → Đ3 Ø60; Đ1 → Đ4 Ø90.
- **Nước**: cà phê vối 37 lít/cây/ngày (111 lít/lần); sầu riêng 256 lít/cây/ngày; tiêu 19 lít/trụ/ngày.

---

## 12. Đơn vị và quy đổi

- 1 bar ≈ 10,2 m cột nước; 1 kg/cm² ≈ 10 m.
- 1 m³/giờ = 1.000 lít/giờ ≈ 0,28 lít/giây.
- Độ dốc 1% = chênh 1 m trên 100 m.
- 1 HP ≈ 0,75 kW.

## 13. Lưu ý quan trọng

- Kết quả dùng cho **thiết kế sơ bộ**. Trước khi mua vật tư, đối chiếu catalogue ống (Bình Minh, Tiền Phong, Đạt Hòa…), đường đặc tính của bơm, và báo giá thực tế.
- **Nhu cầu nước** tính theo phương pháp FAO-56. Hệ số cây trồng của một số cây là giá trị tham khảo. Thời điểm siết nước, xử lý ra hoa… nên làm theo khuyến cáo khuyến nông địa phương.
- ETo theo vùng là giá trị ước tính lúc cao điểm mùa khô. Có số liệu trạm khí tượng gần vườn thì dùng số đó.
