# Cảm biến âm thanh MKE-S06 Sound Sensor

## Giới thiệu

**MKE-S06 Sound Sensor** là cảm biến âm thanh sử dụng **electret microphone** để thu nhận âm thanh trong môi trường. Cảm biến chuyển đổi sự thay đổi của âm thanh thành tín hiệu điện áp Analog, giúp các hệ thống vi điều khiển đọc và xử lý dữ liệu theo mức tín hiệu âm thanh thực tế, thay vì chỉ nhận trạng thái bật/tắt (Digital) như nhiều loại cảm biến âm thanh phổ biến trên thị trường.

Sản phẩm phù hợp cho nhiều ứng dụng như: đo và giám sát mức âm thanh, hệ thống cảnh báo bằng âm thanh, robot tương tác, thiết bị IoT và các dự án STEM. Mạch được thiết kế tối ưu nhằm tăng độ ổn định tín hiệu và khả năng chống nhiễu, đảm bảo tín hiệu đầu ra ổn định trong quá trình học tập, nghiên cứu và phát triển các ứng dụng thực tế.

Cảm biến **MKE-S06 Sound Sensor** hỗ trợ điện áp giao tiếp 3.3V và 5VDC, cho phép kết nối trực tiếp và an toàn với hầu hết các bo mạch điều khiển phổ biến hiện nay như Arduino, Raspberry Pi, Jetson Nano, Micro:bit và nhiều nền tảng khác. Sản phẩm đi kèm cáp kết nối 3P XH2.54 – Dupont, đảm bảo kết nối chắc chắn, ổn định và thuận tiện trong quá trình sử dụng.

## Nguyên lý hoạt động

**MKE-S06 Sound Sensor** sử dụng **electret microphone** để thu nhận các dao động âm thanh trong môi trường và chuyển đổi chúng thành tín hiệu điện. Khi có âm thanh tác động lên microphone, cảm biến tạo ra **tín hiệu Analog tương ứng với âm thanh thu được**. Tín hiệu này sau đó được **xử lý và khuếch đại**, đưa ra chân tín hiệu `S` để vi điều khiển có thể đọc.

Tín hiệu tại chân `S` có điện áp trong khoảng:

```text
0VDC ~ 3.3VDC
```

Vi điều khiển có thể kết nối chân `S` với ngõ vào **ADC (Analog to Digital Converter)** để chuyển đổi tín hiệu Analog thành giá trị số. Dựa trên giá trị ADC thu được, chương trình có thể **phân tích và xác định mức tín hiệu âm thanh** từ môi trường.

## Thông số kỹ thuật
- Điện áp cấp nguồn: 5VDC
- Chuẩn tín hiệu giao tiếp: Analog
- Điện áp giao tiếp: 0~3.3VDC
- Đo cường độ âm thanh bằng electret microphone
- Khả năng tương thích:
  - Arduino
  - Raspberry Pi
  - Jetson Nano
  - Micro:bit
  - Và các board điều khiển 3.3/5VDC khác
- Thiết kế mạch:
  - Ổn định, chống nhiễu
  - Phù hợp cho ứng dụng học tập và thực tế
- Đi kèm cáp kết nối: 3P XH2.54–Dupont

## Các chân tín hiệu
<table><thead>
  <tr>
    <th>MKE-S06</th>
    <th>Ghi chú</th>
  </tr></thead>
<tbody>
  <tr>
    <td>-</td>
    <td>Chân cấp nguồn âm 0VDC</td>
  </tr>
  <tr>
    <td>+</td>
    <td>Chân cấp nguồn dương 5VDC</td>
  </tr>
  <tr>
    <td>S</td>
    <td>Chân tín hiệu Analog Out</td>
  </tr>
</tbody>
</table>

## Hướng dẫn sử dụng
### Hướng dẫn kết nối
- Cấp nguồn 5VDC cho mạch qua hai chân - và +.
- Nhận tín hiệu của cảm biến qua chân S (SIGNAL).
<table><thead>
  <tr>
    <th>SIGNAL (Analog Out)</th>
    <th>Trạng thái</th>
  </tr></thead>
<tbody>
  <tr>
    <td>Max</td>
    <td>3.3VDC</td>
  </tr>
  <tr>
    <td>Min</td>
    <td>0VDC</td>
  </tr>
</tbody>
</table>

### Hướng dẫn sử dụng với Arduino Uno / Vietduino Uno / ESP32
- Trong **Tools / Library Manager**, tìm và cài đặt bộ thư viện tổng hợp **"MKE_ONE" by MakerEdu.vn**
- Mở chương trình mẫu tại **File / Examples / MKE_ONE / Sensor / MKE_S06_SOUND**
- Cấu hình board mạch tương ứng là **Arduino Uno / ESP32**, chọn đúng cổng **COM Port** của mạch và nhấn **Upload** để nạp chương trình.
- Cấp nguồn 5VDC cho mạch, kết nối chân S (SIGNAL) của sensor với chân điều khiển được khai báo trong chương trình.
- Xem kết quả mạch hoạt động theo chương trình đã nạp.

### Hướng dẫn lập trình với Micro:bit (kéo thả khối)

- Khởi động [Microsoft MakeCode](https://makecode.microbit.org/) và **Import** chương trình theo đường link sau: `https://github.com/makereduvn/mke_s06_sound_microbit/`
- Kết nối mạch Micro:bit và **Download** chương trình.
- Cấp nguồn 5VDC cho mạch, kết nối chân S (SIGNAL) của sensor với chân điều khiển được khai báo trong chương trình.
- Xem kết quả mạch hoạt động theo chương trình đã nạp.

Nếu bắt đầu tự án mới cần cài đặt Extension **MKE_ONE_MICROBIT** trên [Microsoft MakeCode](https://makecode.microbit.org/) theo [hướng dẫn tại đây](https://github.com/makereduvn/MKE_ONE_MICROBIT). Sau khi cài đặt thành công, các khối lệnh của Extension **MKE_ONE_MICROBIT** sẽ xuất hiện trong danh sách block và sẵn sàng để sử dụng.

## Kích thước sản phẩm
![MKE-S06 LDR_LIGHT](/extras/MKE-S06_1.jpg)

## Hình ảnh sản phẩm
![MKE-S06 LDR_LIGHT](/extras/MKE-S06_2.png)
![MKE-S06 LDR_LIGHT](/extras/MKE-S06_3.png)

## Miễn trừ trách nhiệm
Sản phẩm này là bo mạch phát triển được thiết kế phục vụ cho mục đích nghiên cứu, thử nghiệm và học tập, không phải là một thiết bị hoàn chỉnh. Trong trường hợp người dùng kết hợp mạch này với các linh kiện, thiết bị hoặc phần mềm khác để tạo thành một hệ thống hoặc sản phẩm hoàn chỉnh, mọi chức năng và tính phù hợp của sản phẩm sau cùng đều thuộc trách nhiệm của người dùng.
