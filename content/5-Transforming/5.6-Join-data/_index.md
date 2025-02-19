---
title : "Join data"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 5.6. </b> "
---

### Kết hợp dữ liệu Yellow Trips với dữ liệu Pickup Taxi Zone Lookup

1. Nhấp vào biểu tượng **Transform**, chọn **Join**.
![001](../../images/5.transforming/5.6/001.png)

2. Cung cấp thông tin sau:
   - **Node properties tab**, **Name** – `Yellow Trips Data + Pickup Zone Lookup`
   - **Node properties tab**, **Node Parents**:
     - **Change Schema - Pickup Zone Lookup**
     - **Filter - Yellow Trip Data**
   - **Transform properties tab**, dưới phần **Join conditions**, chọn các khóa sau:
     - **Change Schema - Pickup Zone Lookup** - `pu_location_id`
     - **Filter - Yellow Trip Data** - `pulocationid`
  ![002](../../images/5.transforming/5.6/002.png)

   
3. Nhớ lưu công việc của bạn.

