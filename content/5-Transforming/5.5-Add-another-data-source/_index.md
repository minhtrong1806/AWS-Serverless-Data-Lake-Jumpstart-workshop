---
title : "Add another data source"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 5.5. </b> "
---

### Thêm bảng tra cứu cho **Taxi Pickup Zone**

1. Quay lại **Visual tab**.
2. Nhấp vào biểu tượng **Source**, chọn **S3**.
![001](../../images/5.transforming/5.5/001.png)

3. Trong **Data source – S3 bucket node**, nhập thông tin sau:
   - **Node properties tab**, **Name** – `Pickup Zone Lookup`
   - **Data source properties tab**, **Database** – `nyctaxi_db`
   - **Data source properties tab**, **Table** – `raw_taxi_zone_lookup`
![002](../../images/5.transforming/5.5/002.png)

5. Nhớ lưu công việc của bạn.

### Chỉnh sửa tên cột của bảng **Pickup Taxi Zone Lookup**

1. Đảm bảo rằng **Amazon S3 - Pickup Zone Lookup node** đã được chọn.
2. Nhấp vào biểu tượng **Transform**, chọn **Change Schema**.
![003](../../images/5.transforming/5.5/003.png)

3. Cung cấp thông tin sau:
   - **Node properties tab**, **Name** – `Change Schema - Pickup Zone Lookup`
   - **Transform tab**, sửa các khóa mục tiêu:
     - **locationid** thành `pu_location_id`
     - **borough** thành `pu_borough`
     - **zone** thành `pu_zone`
     - **service_zone** thành `pu_service_zone`
![004](../../images/5.transforming/5.5/004.png)

4. Nhớ lưu công việc của bạn.