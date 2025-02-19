---
title : "Xem lại metadata trong Glue Data Catalog"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 3.3. </b> "
---

### Xem lại metadata trong Glue Data Catalog

{{% notice info %}}
**Glue Data Catalog** chứa các tham chiếu đến dữ liệu được sử dụng làm **nguồn** và **đích** cho các tác vụ **ETL (Extract, Transform, Load)** trong **AWS Glue**. Ngoài ra, nó còn duy trì một cái nhìn thống nhất về dữ liệu và cho phép các dịch vụ AWS khác như **Athena, EMR và Redshift Spectrum** truy cập dữ liệu một cách dễ dàng.
{{% /notice %}}

1. Trong menu điều hướng bên trái, nhấp vào **Tables**.  
![001](../../../images/3.discovering-cataloging/3.3/001.png)

2. Trên trang **Tables**, nhấp vào tên **raw_yellow_tripdata** để xem thông tin **metadata** và **schema** của bảng.
![002](../../../images/3.discovering-cataloging/3.3/002.png)
![003](../../../images/3.discovering-cataloging/3.3/003.png)
![004](../../../images/3.discovering-cataloging/3.3/004.png)