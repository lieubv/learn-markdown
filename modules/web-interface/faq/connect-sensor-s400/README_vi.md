# Cấu hình cảm biến nhiên liệu với thiết bị GPS S200/S400

### Bước 1 : Hiệu chỉnh cảm biến

Bạn có thể tham khảo [tại đây](vi/modules/web-interface/devices/calib-sensor/#calib)

### Bước 2 : Nối dây cảm biến với bộ theo dõi GPS 
    
* RX của Cảm Biến --> TX của S200/S400: Màu vàng
* TX của Cảm Biến --> RX của S200/S400: Màu Xanh

### Bước 3 :  Cấu hình 

- Cảm biến soji bán ra nước ngoài dùng baudrate 19200

    **Rs232,0,2,19200#**

-  Cảm biến soji bán tại Việt Nam dùng baudrate 9600

    **Rs232,0,2,9600#**

### Bước 4 : Reset cấu hình

Gửi lệnh **reset#** để lưu và cập nhật cấu hình

### Bước 5 : Đợi vài phút để kiểm tra
    
**view,comm#**

### Bước 6 : Cấu hình trên Platform

- Đầu tiên , chọn xe muốn cấu hình.
  **1.** Click vào tab <span class="icon-left svg-filter-info">![Ok](/docs/assets/images/web-interface/icon/SVG/file-alt.svg)  **Thông tin** của xe đó. Hoặc click vào icon <span class="icon-left svg-filter-info">![Ok](/docs/assets/images/web-interface/icon/SVG/file-alt.svg)  trong hộp thông tin thiết bị
    
    <span style="display:block;text-align:left">![Manage device ](/docs/assets/images/web-interface/faq/add-sensor.jpg)
  
  **2.** Click vào  <span class="icon-left svg-filter-tick">![Ok](/docs/assets/images/web-interface/icon/SVG/plus.svg)**Thêm cảm biến** , sẽ xuất hiện hộp thoại như sau:  

    <span style="display:block;text-align:left">![Manage device ](/docs/assets/images/web-interface/faq/add-sensor-2.jpg)

  **3.** Điền các thông tin vào hộp thoại :

  - ***Cơ bản*** 
    - **Tên cảm biến** : Đặt tên cảm biến cho dễ nhớ, dễ nhìn. 
    - **Phương pháp tính**: Chọn 1 trong 3 phương pháp:  Calibration (Hiệuchuẩn), Linear (tuyến tính), Original (Nguyên bản). 
    - **Tham số**: Chọn tham số tương ứng.
    - **Đơn vị**: Chọn đơn vị cần đo .
    - **Loại cảm biến** : Chọn loại cảm biến tương ứng với đơn vị đo. 
    - **Hiệu chuẩn**  : Nhập giá trị đúng như ví dụ (Chỉ xuất hiện khi chọn phương pháp  Calibration (Hiệu chuẩn)
    **Công thức** : Nhập giá trị đúng như ví dụ (Chỉ xuất hiện khi chọn phương pháp  Linear (tuyến tính), Original (Nguyên bản)
    - **Tối thiểu**  : Nhập giá trị nhỏ nhất của hiệu chuẩn.
    - **Tối đa**: Nhập giá trị lớn nhất của hiệu chuẩn.
  
  -  ***Nâng cao*** : 
     -  **Tăng tối thiểu** : Nhập giá trị cảm biến thay đổi khi tăng bất thường.
     -  **Giảm tối thiểu** : Nhập giá trị cảm biến thay đổi khi giảm bất thường.
     -  **Cân đối bù trừ** : Nhập giá trị chỉnh "không" khi tính toán ra ADC để xuất ra giá trị nhiệt độ(loại cảm biến) đúng.
     - **Làm tròn** : Làm tròn giá trị cảm biến bao nhiêu đó sau dấu (,).
     - **Sắp xếp**: Sắp xếp giá trị cảm biến thay đổi lên vị trí nào. 
     - **Mô tả** : Có thể ghi thêm thông tin về cảm biến,...
     - **Hiển thị bản đồ trên map** : Bật / tắt để hiển thị / không hiển thị tên cảm biến trên bản đồ. 

  **4.** Click **Thêm** để lưu cảm biến. 
  
  **5.** Click **Lưu thay đổi** để hoàn thành thao tác khi sửa thiết bị.