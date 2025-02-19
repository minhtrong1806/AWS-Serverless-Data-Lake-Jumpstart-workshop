---
title : "Run SQL queries to explore the data"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4.4. </b> "
---


### Chạy truy vấn SQL để khám phá dữ liệu

1. Kiểm tra số lượng bản ghi của yellow taxi  
```sql
SELECT COUNT(*) "Count" FROM raw_yellow_tripdata;
```
![001](../../images/4.exploring/4.4/001.png)

2. Khám phá các danh mục dữ liệu 

```sql
SELECT vendorid, COUNT(*) "Count"
FROM  raw_yellow_tripdata
GROUP BY vendorid
ORDER BY 1;
```
![002-1](../../images/4.exploring/4.4/002-1.png)

```sql
SELECT pulocationid, COUNT(*) "Count"
FROM   raw_yellow_tripdata
GROUP BY pulocationid
ORDER BY 1;
```
![002-2](../../images/4.exploring/4.4/002-2.png)

```sql
SELECT payment_type, COUNT(*) "Count"
FROM   raw_yellow_tripdata
GROUP BY payment_type
ORDER BY 1;
```
![002-3](../../images/4.exploring/4.4/002-3.png)

3. Tìm các bản ghi có Vendor ID là NULL
```sql
SELECT * 
FROM raw_yellow_tripdata
WHERE vendorid IS NULL
LIMIT 100;
```
![003](../../images/4.exploring/4.4/003.png)

4. Phân tích bản ghi theo khoảng thời gian
```sql
SELECT SUBSTR(tpep_pickup_datetime, 1, 7) "Period", COUNT(*) "Total Records"
FROM raw_yellow_tripdata
GROUP BY SUBSTR(tpep_pickup_datetime, 1, 7) 
ORDER BY 1;
```
![004](../../images/4.exploring/4.4/004.png)

5. Đếm số bản ghi có thời gian không thuộc năm 2020
```sql
SELECT COUNT(*) "Count"
FROM raw_yellow_tripdata 
WHERE SUBSTR(tpep_pickup_datetime, 1, 7) NOT LIKE '2020%';
```
![005](../../images/4.exploring/4.4/005.png)

6. Đếm số bản ghi có Vendor ID là NULL trong năm 2020
```sql
SELECT COUNT(*) "Count"
FROM raw_yellow_tripdata
WHERE vendorid IS NULL
AND SUBSTR(tpep_pickup_datetime, 1, 7) LIKE '2020%';
```
![006](../../images/4.exploring/4.4/006.png)

7. Đếm số bản ghi trong quý IV năm 2020, loại trừ Vendor ID NULL
```sql
SELECT COUNT(*) "Count"
FROM raw_yellow_tripdata
WHERE vendorid IS NOT NULL
AND SUBSTR(tpep_pickup_datetime, 1, 7) LIKE '2020-1%';
```
![007](../../images/4.exploring/4.4/007.png)

8. Kết hợp dữ liệu chuyến taxi với bảng tra cứu khu vực 
```sql
SELECT td.*, pu.*, do.*
FROM raw_yellow_tripdata td, 
     raw_taxi_zone_lookup pu, 
     raw_taxi_zone_lookup do 
WHERE td.pulocationid = pu.locationid 
AND td.pulocationid = do.locationid 
AND vendorid IS NOT NULL 
AND SUBSTR(tpep_pickup_datetime, 1, 7) LIKE '2020-1%'
LIMIT 100;
```
![008-1](../../images/4.exploring/4.4/008-1.png)

```sql
SELECT COUNT(*) "Count"
FROM raw_yellow_tripdata td, 
     raw_taxi_zone_lookup pu, 
     raw_taxi_zone_lookup do 
WHERE td.pulocationid = pu.locationid 
AND td.pulocationid = do.locationid 
AND vendorid IS NOT NULL 
AND SUBSTR(tpep_pickup_datetime, 1, 7) LIKE '2020-1%';
```
![008-2](../../images/4.exploring/4.4/008-2.png)