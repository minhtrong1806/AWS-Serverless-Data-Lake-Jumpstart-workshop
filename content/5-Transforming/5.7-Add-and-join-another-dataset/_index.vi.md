---
title : "Thêm và kết hợp một tập dữ liệu khác"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : " <b> 5.7. </b> "
---

### Thêm bảng tra cứu cho Taxi Drop-off Zone

1. Nhấp vào biểu tượng **Source**, chọn **S3**.
![001](../../../images/5.transforming/5.7/001.png)

2. Trong nút **Data source – S3 bucket**, cung cấp thông tin sau:
   - **Node properties tab**, **Name** – `Dropoff Zone Lookup`
   - **Data source properties tab**, **Database** – `nyctaxi_db`
   - **Data source properties tab**, **Table** – `raw_taxi_zone_lookup`
![002](../../../images/5.transforming/5.7/002.png)

3. Nhớ lưu công việc của bạn.

### Chỉnh sửa tên cột của bảng Drop-off Taxi Zone Lookup

1. Đảm bảo rằng nút **Amazon S3 - Dropoff Zone Lookup** đã được chọn.
2. Nhấp vào biểu tượng **Transform**, chọn **Change Schema**.
![003](../../../images/5.transforming/5.7/003.png)

3. Cung cấp thông tin sau:
   - **Node properties tab**, **Name** – `Change Schema - Dropoff Zone Lookup`
   - **Transform tab**, sửa các khóa mục tiêu:
     - **locationid** thành `do_location_id`
     - **borough** thành `do_borough`
     - **zone** thành `do_zone`
     - **service_zone** thành `do_service_zone`
![004](../../../images/5.transforming/5.7/004.png)

4. Nhớ lưu công việc của bạn.

### Kết nối dữ liệu Yellow Trips và Dropoff Taxi Zone Lookup

1. Nhấp vào biểu tượng **Transform**, chọn **Join**.
![005](../../../images/5.transforming/5.7/005.png)

2. Cung cấp thông tin sau:
   - **Node properties tab**, **Name** – `Yellow Trips Data + Pickup Zone Lookup + Dropoff Zone Lookup`
   - **Node properties tab**, **Node Parents**:
     - Change Schema - Dropoff Zone Lookup
     - Yellow Trips Data + Pickup Zone Lookup
   - **Transform properties tab**, dưới **Join conditions**, chọn các khóa sau:
     - Change Schema - Dropoff Zone Lookup – `do_location_id`
     - Yellow Trips Data + Pickup Zone Lookup – `dolocationid`
   ![006](../../../images/5.transforming/5.7/006.png)

3. Nhớ lưu công việc của bạn.

