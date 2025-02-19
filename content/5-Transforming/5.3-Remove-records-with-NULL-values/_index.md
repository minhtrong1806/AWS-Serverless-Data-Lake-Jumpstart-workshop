---
title : "Remove records with NULL values"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

### Xóa các bản ghi có giá trị NULL

1. Nhấp vào biểu tượng **Transform**, chọn **Custom transform**.
![001](../../images/5.transforming/5.3/001.png)

2. Trong nút **Transform – Custom code**, nhập thông tin sau:
   - **Node properties tab**, **Name** – `Remove Records with NULL`
   - Thêm đoạn mã sau vào khối mã (Code block):

```python
def MyTransform (glueContext, dfc) -> DynamicFrameCollection:
    df = dfc.select(list(dfc.keys())[0]).toDF().na.drop()
    results = DynamicFrame.fromDF(df, glueContext, "results")
    return DynamicFrameCollection({"results": results}, glueContext)
```

![002](../../images/5.transforming/5.3/002.png)

3. Nhấp vào biểu tượng **Transform**, chọn **SelectFromCollection**.
![003](../../images/5.transforming/5.3/003.png)

4. Nhập thông tin sau:
   - **Node properties tab**, **Name** – `SelectFromCollection`
   - **Transform tab**, **Frame index** – `0`

![004](../../images/5.transforming/5.3/004.png)

5. Nhớ lưu công việc của bạn.