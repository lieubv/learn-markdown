
# Cấu hình nhận ảnh gửi từ thiết bị S200/S400

### 1. Nối dây

* RX của MDVR--> TX của S200/S400: Màu vàng
* TX của MDVR--> RX của S200/S400: Màu Xanh

### 2. Cấu hình trên thiết bị

- Cổng rs232

    **rs232,0,9,115200#**

- Tần suất chụp: 300 giây

    **rs232para,0,300,0#**

- Server và đường dẫn upload ảnh:

    **server,file,photos.gotrack365.com,80#** 

    **server,path,/api/receive-photos#**

    **reset#**
