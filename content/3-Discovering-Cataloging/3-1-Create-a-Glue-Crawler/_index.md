---
title : "Create a Glue Crawler"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 3.1. </b> "
---

## Tạo Glue Crawler

{{% notice info %}}
**Glue Crawler** là một tính năng giúp tự động suy luận **schema của cơ sở dữ liệu và bảng** từ dữ liệu nguồn, sau đó lưu trữ **metadata** tương ứng trong **AWS Glue Data Catalog**.  
{{% /notice %}}

1. Truy cập vào **AWS Glue Console**.  
![001](../../../images/3.discovering-cataloging/3.1/001.png)

2. Ở menu điều hướng bên trái, nhấp vào **Crawlers**.  
![002](../../../images/3.discovering-cataloging/3.1/002.png)

3. Trên trang **Crawlers**, nhấp vào **Create a crawler**.  
![003](../../../images/3.discovering-cataloging/3.1/003.png)

4. Trong mục đặt tên, nhập `nyc-taxi-crawler` rồi nhấp **Next**.  
![004](../../../images/3.discovering-cataloging/3.1/004.png)

5. Ở màn hình **Choose data sources and classifiers**, điền các thông tin sau và nhấp **Next**:  
   - Nhấp vào **Add a data source**.  
   ![005-1](../../../images/3.discovering-cataloging/3.1/005-1.png)
   - Chọn **Data source** → **S3**.  
   - Chọn **Location of S3 data** → **In this account**.  
   - Nhập đường dẫn S3: `s3://serverlessanalytics-[your-account-id]-raw/nyc-taxi/`.  
   - Trong mục **Subsequent crawler runs**, chọn **Crawl all sub-folders**.  
   - Nhấp **Add an S3 data source**. 
   ![005-2](../../../images/3.discovering-cataloging/3.1/005-2.png)

6. Ở màn hình **Configure security settings**, chọn **ServerlessAnalyticsRole** trong danh sách **Existing IAM role**, sau đó nhấp **Next**. 
![006](../../../images/3.discovering-cataloging/3.1/006.png)

7. Ở màn hình **Set output and scheduling**, nhấp vào **Add database**.  
![007-1](../../../images/3.discovering-cataloging/3.1/007-1.png)
   - Nhập `nyctaxi_db` làm tên cơ sở dữ liệu.  
   - Nhấp **Create database**.  
![007-2](../../../images/3.discovering-cataloging/3.1/007-2.png)
8. Quay lại tab trước (**Set output and scheduling**), nhấp **Refresh** trong mục **Target database** và chọn **nyctaxi_db** vừa tạo.  
9. Trong mục **Table name prefix**, nhập **raw_** (tùy chọn).  
10. Ở mục **Crawler schedule**, giữ nguyên tần suất **On demand**, sau đó nhấp **Next**.  
![007-3](../../../images/3.discovering-cataloging/3.1/007-3.png)

11. Xem lại thông tin, sau đó nhấp **Create crawler** để hoàn tất. 🚀
![008](../../../images/3.discovering-cataloging/3.1/008.png)