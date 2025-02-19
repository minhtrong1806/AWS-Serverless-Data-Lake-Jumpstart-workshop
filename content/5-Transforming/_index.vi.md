---
title : "Chuyển đổi dữ liệu"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

### Tổng quan

Enrichment dữ liệu là quá trình cải thiện dữ liệu hiện có bằng cách bổ sung dữ liệu từ các nguồn khác để cung cấp thêm ngữ cảnh hoặc ý nghĩa. Điều này làm cho dữ liệu trở nên hữu ích và mang lại cái nhìn sâu sắc hơn trong quá trình phân tích.

![data-lake](../../images/5.transforming/001-arc-transforming.png)

### Giới thiệu về AWS Glue Studio

AWS Glue Studio là một giao diện đồ họa giúp đơn giản hóa việc tạo, chạy và giám sát các job ETL (extract, transform, load) trong AWS Glue. Bạn có thể tạo các workflow chuyển đổi dữ liệu một cách trực quan, AWS Glue Studio sẽ tự động tạo mã Apache Spark thay cho bạn và cho phép chạy chúng trên động cơ ETL không máy chủ của AWS Glue sử dụng Apache Spark.

### Nội dung
1. [Tạo một job bằng Glue Studio](5.1-Create-a-job-using-Glue-Studio/)
2. [Thêm nguồn dữ liệu](5.2-Add-a-data-source/)
3. [Loại bỏ các bản ghi có giá trị NULL](5.3-Remove-records-with-NULL-values/)
4. [Lọc dữ liệu](5.4-Filter-records/)
5. [Thêm một nguồn dữ liệu khác](5.5-Add-another-data-source/)
6. [Kết hợp dữ liệu](5.6-Join-data/)
7. [Thêm và kết hợp một tập dữ liệu khác](5.7-Add-and-join-another-dataset/)
8. [Chuyển đổi dữ liệu và lưu vào đích](5.8-Transform-data-and-save-to-target/)
9. [Chạy job](5.9-Run-the-job/)

