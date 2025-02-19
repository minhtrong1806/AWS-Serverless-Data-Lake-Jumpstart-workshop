---
title : "Transform data and save to target"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 5.8. </b> "
---

### Thay đổi tên cột và kiểu dữ liệu của bộ dữ liệu đã nối

1. Nhấp vào biểu tượng **Transform**, chọn **Change Schema**.
![001](../../images/5.transforming/5.8/001.png)

2. Cung cấp thông tin sau:
   - **Node properties tab**, **Name** – `Change Schema - Joined Data`
   - **Transform tab**, thay đổi **Target key** và **Data type** của các cột sau:
     - **vendorid** thành `vendor_id`
     - **tpep_pickup_datetime** thành `pickup_datetime`, kiểu **string** thành `timestamp`
     - **tpep_dropoff_datetime** thành `dropoff_datetime`, kiểu **string** thành `timestamp`
   - **Transform tab**, xóa các khóa **Source** sau:
     - `pulocationid`
     - `dolocationid`
  ![002](../../images/5.transforming/5.8/002.png)
  ![003](../../images/5.transforming/5.8/003.png)
   
3. Nhớ lưu công việc của bạn.

### Lưu dữ liệu đã biến đổi vào Amazon S3

1. Nhấp vào biểu tượng **Target**, chọn **Amazon S3**.
![004](../../images/5.transforming/5.8/004.png)

2. Cung cấp thông tin sau:
   - **Node properties tab**, **Name** – `Transformed Yellow Trip Data`
   - **Data target properties – S3 tab**, chỉ định các thông tin sau:
     - **Format** – `Parquet`
     - **Compression Type** - `Snappy`
     - **S3 Target Location** – `s3://serverlessanalytics-[your-account-id]-transformed/nyc-taxi/yellow-tripdata/`
  ![005](../../images/5.transforming/5.8/005.png)

3. Nhớ lưu công việc của bạn.
