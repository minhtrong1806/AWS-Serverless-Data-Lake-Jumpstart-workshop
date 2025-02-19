---
title : "Kết nối với nguồn dữ liệu"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 7.2. </b> "
---

**Kết nối với nguồn dữ liệu**  
1. Trên trang QuickSight, nhấp vào **Datasets** trong bảng điều hướng bên trái.  
![001](../../../images/7.visualizing/7.2/001.png)

2. Ở góc trên bên phải màn hình, nhấp vào **new dataset**.  
![002](../../../images/7.visualizing/7.2/002.png)

3. Chọn **Athena**.  
![003](../../../images/7.visualizing/7.2/003.png)

4. Trong cửa sổ **New Athena data source**, điền thông tin sau:  
   - Tên nguồn dữ liệu – `Athena - SDL Jumpstart`  
   - Workgroup Athena – `primary`  
   - Nhấp **Create Data Source**.  
![004](../../../images/7.visualizing/7.2/004.png)

5. Trong cửa sổ **Choose your table**, điền thông tin sau:  
   - Catalog – `AwsDataCatalog`  
   - Database – `nyctaxi_db`  
   - Tables – `v_yellow_tripdata`  
   - Nhấp **Select**.  
![005](../../../images/7.visualizing/7.2/005.png)

{{% notice info %}}
Nếu không không hiện database, chọn lại region của QuickSign cho cùng với region của Athena
{{% /notice %}}

6. Trong cửa sổ **Finish dataset creation**, điền thông tin sau:  
   - **Import to SPICE for quicker analytics**  
   - Nhấp **Edit/Preview data**.  
![006](../../../images/7.visualizing/7.2/006.png)

{{% notice info %}}
SPICE là viết tắt của **Super-fast, Parallel, In-memory Calculation Engine**. Nó được thiết kế để thực hiện các phép tính nâng cao một cách nhanh chóng và phục vụ dữ liệu. Dung lượng SPICE được chia sẻ cho tất cả những người dùng QuickSight trong một vùng AWS duy nhất.
{{% /notice %}}