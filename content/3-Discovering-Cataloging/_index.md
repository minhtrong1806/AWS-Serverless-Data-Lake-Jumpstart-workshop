---
title : "Discovering and Cataloging Data"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 3. </b> "
---
## **Tổng quan**  

Với sự đa dạng của các nguồn dữ liệu và định dạng trong **data lake**, việc **khám phá và lập danh mục dữ liệu** là rất quan trọng. Điều này không chỉ giúp bạn hiểu rõ hơn về dữ liệu hiện có mà còn giúp tích hợp dễ dàng với các dịch vụ phân tích AWS chuyên biệt khác.  

Trong bài lab này, chúng ta sẽ tạo một **AWS Glue Crawler** để tự động phát hiện **schema** của dữ liệu được lưu trữ trong **Amazon S3**. Thông tin khám phá được sẽ được đăng ký vào **AWS Glue Catalog**, giúp AWS Glue sử dụng dữ liệu này cho các quy trình **ETL (Extract, Transform, Load)**. Đồng thời, các dịch vụ khác như **Amazon Athena** có thể tận dụng dữ liệu trong **S3** để thực thi truy vấn một cách dễ dàng.  

![datalake](../images/3.discovering-cataloging/001-arc.png)
---

## **Giới thiệu AWS Glue**  

**AWS Glue** là một dịch vụ **ETL không máy chủ (serverless ETL)** được quản lý hoàn toàn, giúp đơn giản hóa và tối ưu chi phí khi **phân loại, làm sạch, làm giàu và di chuyển dữ liệu** giữa các hệ thống lưu trữ khác nhau. AWS Glue bao gồm các thành phần chính sau:  

- **Data Catalog** – Kho lưu trữ trung tâm chứa **metadata** về cấu trúc và hoạt động của dữ liệu.  
- **ETL Engine** – Tự động tạo mã **Scala hoặc Python** để xử lý dữ liệu.  
- **Jobs System** – Hệ thống quản lý hạ tầng để điều phối các quy trình ETL.  

Ngoài ra, AWS Glue còn cung cấp các thành phần bổ sung như:  

- **AWS Glue DataBrew** – Công cụ trực quan giúp các nhà phân tích và khoa học dữ liệu **chuẩn bị dữ liệu** bằng giao diện kéo-thả mà không cần viết mã.  
- **AWS Glue Elastic Views** – Cho phép xây dựng **materialized views** để kết hợp và sao chép dữ liệu từ nhiều nguồn mà không cần viết mã tùy chỉnh.  

Tất cả các thành phần này giúp **tự động hóa phần lớn các công việc nặng nhọc** liên quan đến **khám phá, phân loại, làm sạch, làm giàu và di chuyển dữ liệu**, cho phép bạn tập trung nhiều hơn vào việc **phân tích dữ liệu** để đưa ra những quyết định chiến lược. 🚀

### Content
1. [Create a Glue Crawler](3.1-Create-a-Glue-Crawler/)
2. [Run the Glue Crawler](3.2-Run-the-Glue-Crawler/)
3. [Review the metadata in Glue Data Catalog](3.3-Review-the-metadata-in-Glue-Data-Catalog/)
