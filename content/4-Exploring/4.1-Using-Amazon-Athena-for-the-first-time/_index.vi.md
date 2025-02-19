---
title : "Sử dụng Amazon Athena lần đầu tiên"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 4.1. </b> "
---

### Sử dụng Amazon Athena lần đầu tiên

{{% notice info %}}
**Amazon Athena** tự động lưu trữ **kết quả truy vấn** và **thông tin metadata** cho mỗi truy vấn trong một **vị trí kết quả** mà bạn có thể chỉ định trên **Amazon S3**. Nếu cần, bạn có thể truy cập vào thư mục này để làm việc với các tệp dữ liệu hoặc tải trực tiếp kết quả từ **Athena Console**.  
{{% /notice %}}

### **Các bước cấu hình vị trí lưu trữ kết quả truy vấn:**  

1. Truy cập vào **Athena Console**, sau đó nhấp vào **Get Started**.  
![001-1](../../../images/4.exploring/4.1/001-1.png)
![001-2](../../../images/4.exploring/4.1/001-2.png)

2. Trên thanh menu phía trên, nhấp vào **Workgroup: primary**. 
![002](../../../images/4.exploring/4.1/002.png)

3. Chọn **Settings**, sau đó nhấp vào **Browse S3** và chọn đường dẫn:  
![003-1](../../../images/4.exploring/4.1/003-1.png)

   - `s3://serverlessanalytics-[your-account-id]-athena` làm **Location of query result**.  
![003-2](../../../images/4.exploring/4.1/003-2.png)

4. Kéo xuống cuối trang, nhấp vào **Save** để lưu cấu hình.  
5. Trên thanh menu trên cùng, nhấp vào **Editor** để quay lại trang **Query editor**. 🚀
![004](../../../images/4.exploring/4.1/004.png)