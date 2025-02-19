---
title : "Create a job using Glue Studio"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 5.1. </b> "
---

### Kế hoạch các bước chuyển đổi dữ liệu

1. Đọc dữ liệu chuyến taxi vàng từ S3, bảng `raw_yellow_tripdata`.
2. Làm sạch dữ liệu chuyến taxi vàng:
   - Loại bỏ các bản ghi có giá trị NULL (vendorid, payment_type, passenger_count, ratecodeid).
   - Lọc các bản ghi trong một khoảng thời gian (loại bỏ bản ghi có thời gian pickup datetime không hợp lệ, thu hẹp phạm vi dữ liệu cần xử lý).
3. Kết hợp dữ liệu chuyến taxi vàng với bảng tra cứu khu vực để lấy thông tin về vị trí đón khách:
   - Đọc dữ liệu tra cứu từ S3, bảng `raw_taxi_zone_lookup`.
   - Đổi tên các cột của bảng tra cứu để phân biệt thông tin về vị trí đón khách và vị trí trả khách.
   - Thực hiện kết hợp dữ liệu.
4. Kết hợp dữ liệu chuyến taxi vàng với bảng tra cứu khu vực để lấy thông tin về vị trí trả khách:
   - Đọc dữ liệu tra cứu từ S3, bảng `raw_taxi_zone_lookup`.
   - Đổi tên các cột của bảng tra cứu để phân biệt thông tin về vị trí trả khách và vị trí đón khách.
   - Thực hiện kết hợp dữ liệu.
5. Thực hiện chuyển đổi dữ liệu trên bộ dữ liệu đã kết hợp:
   - Đổi tên các cột.
   - Đặt các kiểu dữ liệu phù hợp.
   - Loại bỏ các cột thừa do kết quả của các phép kết hợp bảng.
6. Lưu bộ dữ liệu đã xử lý vào S3 ở định dạng tối ưu hóa cho truy vấn.

### Tạo một job sử dụng Glue Studio

1. Truy cập vào Glue console.
![001](../../../images/5.transforming/5.1/001.png)

2. Trong thanh điều hướng bên trái, nhấp vào **ETL jobs**.
![002](../../../images/5.transforming/5.1/002.png)

3. Trên trang AWS Glue Studio, nhấp vào **Visual ETL**.
![003](../../../images/5.transforming/5.1/003.png)

4. Trên trang chỉnh sửa Glue Studio, vào tab **Job details**, thiết lập cấu hình sau:
   - **Name** – `Transform NYC Taxi Trip Data`
   - **IAM Role** – ServerlessAnalyticsRole
   - **Job bookmark** – Disable
   - **Number of retries** – 0
   ![004-1](../../../images/5.transforming/5.1/004-1.png)
   ![004-2](../../../images/5.transforming/5.1/004-2.png)

{{% notice info %}}
Tính năng job bookmark của AWS Glue giúp duy trì thông tin trạng thái và ngăn ngừa việc xử lý lại dữ liệu cũ. Nó cho phép job chỉ xử lý dữ liệu mới khi chạy lại theo lịch trình.
{{% /notice %}}

5. Nhấp vào **Save**. Quay lại tab **Visual**.