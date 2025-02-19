---
title : "Dọn dẹp tài nguyên"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 8. </b> "
---

### Xóa Data catalog
1. Truy cập vào AWS Glue Console
2. Chọn Crawler trong Data Catalog
3. Chọn các crawler đã tạo và **Delete**

### Xóa ETL Jobs
1. Truy cập vào AWS Glue Console
2. Chọn ETL jobs
3. Chọn các Job đã tạo và **Delete**

### Empty S3 bucket
1. Truy cập vào AWS S3 
2. Chọn và Empty lần lượt các bucket đã đc tạo ra.

### Xóa CloudFormation Stack
1. Truy cập vào CloudFormation Management Console
2. Ở thanh bên trái, chọn Stacks.
3. Lần lượt tick các vào CloudFormation Stack liên quan tới bài lab và chọn Delete.
4. Trong prompt, chọn Delete stack.
5. Đọi vài phút cho tới khi CloudFormation xóa bỏ hết tài nguyên.