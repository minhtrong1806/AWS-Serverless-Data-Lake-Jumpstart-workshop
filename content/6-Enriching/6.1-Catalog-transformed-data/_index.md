---
title : "Catalog transformed data"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 6.1. </b> "
---

### Tạo một Glue Crawler

1. Vào **AWS Glue Console**.
![001](../../images/6.enriching/6.1/001.png)

2. Trong menu điều hướng bên trái, chọn **Crawlers**.
![002](../../images/6.enriching/6.1/002.png)

3. Trên trang Crawlers, nhấn **Create crawler**.
![003](../../images/6.enriching/6.1/003.png)

4. Đặt tên crawler là `nyc-yellow-tripdata-parquet-crawler`, sau đó nhấn **Next**.
![004](../../images/6.enriching/6.1/004.png)

5. Trên màn hình **Choose data sources and classifiers**, nhập các thông tin sau và nhấn **Next**.
    - Nhấn **Add a data source**.
    ![005-1](../../images/6.enriching/6.1/005-1.png)
    - Chọn **Data source – S3**.
    - Chọn **Location of S3 data - In this account**.
    - Nhập **Include S3 path**: `s3://serverlessanalytics-[your-account-id]-transformed/nyc-taxi/yellow-tripdata`.
    - Đối với các lần chạy crawler tiếp theo, chọn **Crawl all sub-folders**.
    - Nhấn **Add an S3 data source**.
    ![005-2](../../images/6.enriching/6.1/005-2.png)

6. Trên màn hình **Configure security settings**, chọn **ServerlessAnalyticsRole** từ IAM role hiện có, sau đó nhấn **Next**.
![006](../../images/6.enriching/6.1/006.png)

7. Trên màn hình **Set output and scheduling**, chọn **nyctaxi_db** là database.
8. Để **Crawler schedule**, chọn tần suất là **On demand**, sau đó nhấn **Next**.
![007](../../images/6.enriching/6.1/007.png)

9. Xem lại các thông tin của crawler và nhấn **Create crawler**.
![008](../../images/6.enriching/6.1/008.png)

10. Trên trang **Crawlers**, chọn **nyc-yellow-tripdata-parquet-crawler**, sau đó nhấn **Run crawler**.
![009](../../images/6.enriching/6.1/009.png)