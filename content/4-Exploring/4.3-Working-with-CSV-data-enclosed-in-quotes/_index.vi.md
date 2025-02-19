---
title : "Làm việc với dữ liệu CSV được bao trong dấu nháy kép"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 4.3. </b> "
---

### Làm việc với dữ liệu CSV được bao trong dấu nháy kép

{{% notice info %}}
Các tệp **CSV** đôi khi chứa dấu **ngoặc kép ("")** bao quanh các giá trị dữ liệu, nhưng những dấu này không phải là một phần của dữ liệu cần phân tích. Để đọc đúng tệp **CSV**, chúng ta có thể cập nhật **thuộc tính bảng** trong **AWS Glue** để sử dụng **OpenCSVSerDe**.  
{{% /notice %}}

1. Truy cập vào **AWS Glue Console**.  
![001](../../../images/4.exploring/4.3/001.png)

2. Trong menu điều hướng bên trái, nhấp vào **Tables** trong mục **Data Catalog**.  
![002](../../../images/4.exploring/4.3/002.png)

3. Trên màn hình **Tables**, nhấp vào bảng **taxi_zone_lookup**. 
![003](../../../images/4.exploring/4.3/003.png)

4. Nhấp vào **Actions**, sau đó chọn **Edit table**.  
![004](../../../images/4.exploring/4.3/004.png)

5. Cập nhật **Serialization lib** thành: `org.apache.hadoop.hive.serde2.OpenCSVSerde`
![005](../../../images/4.exploring/4.3/005.png)

6. Xóa các **Serde parameters** hiện có và thêm các giá trị sau:  
   - **escapeChar**: nhập một dấu gạch chéo ngược `\`  
   - **quoteChar**: nhập dấu nháy kép `"`  
   - **separatorChar**: nhập dấu phẩy `,`  
   ![006](../../../images/4.exploring/4.3/006.png)

7. Nhấp vào **Save** để lưu thay đổi.  
![007](../../../images/4.exploring/4.3/007.png)

8. Quay lại **Athena Console**.  
9. Trên trang **Query editor**, nhấp vào biểu tượng **⋮ (Actions menu)** bên cạnh bảng **taxi_zone_lookup**, sau đó chọn **Preview table**.  
![008](../../../images/4.exploring/4.3/008.png)
![009](../../../images/4.exploring/4.3/009.png)

10. Kiểm tra kết quả và quan sát rằng các giá trị chuỗi **không còn bị bao quanh bởi dấu ngoặc kép** (`"`). 🚀