---
title : "Add a data source"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 5.2. </b> "
---


### Thêm dữ liệu Yellow Trips từ Amazon S3

1. Nhấp vào biểu tượng **Source**, chọn **S3**.
![001](../../images/5.transforming/5.2/001.png)

2. Trong nút **Data source – S3 bucket**, nhập thông tin sau:
   - **Node properties tab**, **Name** – Yellow Trip Data
   - **Data source properties tab**, **Database** – nyctaxi_db
   - **Data source properties tab**, **Table** – raw_yellow_tripdata
   ![002](../../images/5.transforming/5.2/002.png)
3. Nhấp vào **Save**. Nhớ lưu công việc của bạn khi tiến hành xây dựng các bước chuyển đổi dữ liệu.

### Xem xét sơ đồ dữ liệu kết quả và xem trước dữ liệu

4. Truy cập vào tab **Output schema** để xem sơ đồ dữ liệu kết quả.
![003](../../images/5.transforming/5.2/003.png)

5. Truy cập vào tab **Data preview** để kiểm tra mẫu dữ liệu trong khi chỉnh sửa job của bạn.
    - Chọn **ServerlessAnalyticsRole**, nhấp vào **Confirm**.
    - Nhấp vào **Start session**.
    ![004](../../images/5.transforming/5.2/004.png)
    - Xem xét dữ liệu.
    ![005](../../images/5.transforming/5.2/005.png)

{{% notice info %}}
AWS Glue Studio hiện cho phép bạn xem trước dữ liệu tại mỗi bước trong quá trình tạo job trực quan, giúp bạn kiểm tra và gỡ lỗi các chuyển đổi mà không cần lưu hoặc chạy job.
{{% /notice %}}

{{% notice info %}}
Lần đầu tiên bạn chọn tab **Data preview**, bạn sẽ được yêu cầu chọn một IAM role để sử dụng. IAM role bạn chọn phải có quyền truy cập cần thiết để tạo bản xem trước dữ liệu. Đây có thể là cùng một role mà bạn dự định sử dụng cho job của mình, hoặc có thể là một role khác.
{{% /notice %}}

{{% notice info %}}
Sau khi bạn chọn IAM role, sẽ mất khoảng 20 đến 30 giây để dữ liệu xuất hiện. Bạn sẽ bị tính phí khi sử dụng chức năng xem trước dữ liệu ngay sau khi chọn IAM role.
{{% /notice %}}