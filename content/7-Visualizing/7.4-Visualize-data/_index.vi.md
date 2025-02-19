---
title : "Trực quan hóa dữ liệu"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 7.4 </b> "
---

**Trực quan hóa dữ liệu của bạn**  
1. QuickSight sẽ cố gắng tải dữ liệu vào SPICE, vui lòng chờ vài phút.  
![001](../../../images/7.visualizing/7.4/001.png)

2. Chọn loại hình trực quan **Sankey**, sau đó chỉ định các thông tin sau trong **Field wells**:  
   - **Source** – `pu_borough`  
   - **Destination** – `do_borough` 
   ![002](../../../images/7.visualizing/7.4/002.png)
3. Bạn có thể nhấp vào tiêu đề loại hình trực quan và thay đổi nó thành **Taxi Trips Flow**.  

**Lọc dữ liệu**  
1. Tạo bộ lọc tập trung vào các chuyến taxi xuất phát từ Manhattan.  
2. Nhập `pu_borough` và sau đó chọn nó.  
![003](../../../images/7.visualizing/7.4/003.png)

3. Nhấp vào menu bên cạnh bộ lọc **pu_borough**, chọn **Edit**.  
![004](../../../images/7.visualizing/7.4/004.png)

4. Chọn **Manhattan** trong danh sách bộ lọc, sau đó nhấp vào **Apply**.  
![005](../../../images/7.visualizing/7.4/005.png)

5. Khám phá luồng chuyến taxi dựa trên khu vực đón khách và khu vực trả khách.  
6. Quan sát các mô hình luồng giao thông.