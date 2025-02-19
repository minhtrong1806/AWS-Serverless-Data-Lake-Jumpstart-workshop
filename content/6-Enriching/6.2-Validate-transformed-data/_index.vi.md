---
title : "Xác thực dữ liệu đã được chuyển đổi"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 6.2. </b> "
---

### Xác minh dữ liệu đã chuyển đổi

1. Vào **Athena console**.
![001](../../../images/6.enriching/6.2/001.png)

2. Chọn **Preview table** để kiểm tra dữ liệu trong bảng `yellow_tripdata`.
![002](../../../images/6.enriching/6.2/002.png)
![003](../../../images/6.enriching/6.2/003.png)

3. Trên trang **Query editor**, chạy các câu truy vấn sau để kiểm tra dữ liệu:

```sql
SELECT COUNT(*) "Count"
FROM   yellow_tripdata;
```
![004](../../../images/6.enriching/6.2/004.png)

```sql
SELECT DATE_TRUNC('month', pickup_datetime) "Period", 
       COUNT(*) "Total Records"
FROM   yellow_tripdata
GROUP BY DATE_TRUNC('month', pickup_datetime)
ORDER BY 1;
```
![005](../../../images/6.enriching/6.2/005.png)