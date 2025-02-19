---
title : "Prepareation"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
## **Triển khai CloudFormation Template**  

Trước tiên, chúng ta sẽ thiết lập các tài nguyên cần thiết cho bài lab này. Cụ thể, chúng ta sẽ tạo các **S3 bucket** để lưu trữ tệp tin và thiết lập các **IAM role** phù hợp cho các dịch vụ sẽ sử dụng. Những tài nguyên này đã được định nghĩa trong một **CloudFormation template**.  

1. Truy cập vào **CloudFormation** trong **AWS Console**. 
![001](../images/2.preparation/001.png)

2. Ở menu điều hướng bên phải, nhấp vào **Create stack, With new resources (standard)**.  
![002](../images/2.preparation/002.png)

3. Tải về tệp: [CFN Template](https://ws-assets-prod-iad-r-pdx-f3b3f9f1a7d6a3d0.s3.us-west-2.amazonaws.com/276faf92-bffc-4843-8a8e-8078add48194/serverless-analytics.yaml).  
4. Chọn **Upload a template file**, sau đó tải lên tệp mà bạn vừa tải xuống.  
5. Nhấp **Next**.  

![003](../images/2.preparation/003.png)

6. Trong mục **Stack name**, nhập **sdlj-workshop**.  
7. Nhấp **Next**.  
![004](../images/2.preparation/004.png)


8. Ở bước **Configure stack options** Chọn vào ô **I Acknowledge that AWS CloudFormation might create IAM resources with custom names**.  
![005](../images/2.preparation/005.png)
![006](../images/2.preparation/006.png)
9. Nhấp **Next** cho đến khi đến trang **Review**.  


10. Nhấp **Submit**.  
![007](../images/2.preparation/007.png)


11. Chờ quá trình khởi tạo tài nguyên hoàn tất.
![008](../images/2.preparation/008.png)