---
title : "Filter records"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 5.4. </b> "
---

### Lọc các bản ghi để loại bỏ bản ghi có **Pickup DateTime** không hợp lệ

Để tiết kiệm thời gian, chúng ta sẽ lọc các bản ghi trong khoảng thời gian từ tháng 10 năm 2020 đến tháng 12 năm 2020 nhằm giảm thời gian xử lý công việc trong bài lab.

1. Nhấp vào biểu tượng **Transform**, chọn **Filter**.
![001](../../images/5.transforming/5.4/001.png)

2. Nhập thông tin sau:
   - **Node properties tab**, **Name** – `Filter - Yellow Trip Data`
   - **Transform tab**, **Filter condition** – `tpep_pickup_datetime matches ^2020-1`
   ![002](../../images/5.transforming/5.4/002.png)

3. Nhớ lưu công việc của bạn.

### Xem lại mã tự động sinh ra

1. Chuyển đến **Script details tab**.
![003](../../images/5.transforming/5.4/003.png)

2. Quan sát rằng mã của script được tự động sinh ra bởi **Glue Studio**.