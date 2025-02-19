---
title : "Exploring Data"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

## Tổng quan

Trong bài lab này, chúng ta sẽ sử dụng **Amazon Athena** để khám phá dữ liệu và xác định các vấn đề về **chất lượng dữ liệu**. Ngoài ra, chúng ta cũng sẽ tìm hiểu cách cập nhật **thuộc tính bảng** trong **AWS Glue Catalog**.  

![data-lake](../images/4.exploring/001-arc-exploring.png)

---

## Giới thiệu Amazon Athena 

**Amazon Athena** là một dịch vụ **truy vấn tương tác** giúp bạn dễ dàng phân tích dữ liệu được lưu trữ trong **Amazon S3** bằng **SQL tiêu chuẩn**. Athena là một dịch vụ **serverless**, tức là không yêu cầu thiết lập hoặc quản lý hạ tầng, cho phép bạn bắt đầu phân tích dữ liệu ngay lập tức.  

Điểm đặc biệt là bạn không cần tải dữ liệu vào Athena, mà nó có thể hoạt động **trực tiếp** với dữ liệu được lưu trữ trong **S3**. Điều này giúp tối ưu hóa hiệu suất truy vấn và giảm thiểu các bước xử lý trung gian. 🚀

### Content
1. [Using Amazon Athena for the first time](4.1-Using-Amazon-Athena-for-the-first-time/)
2. [Preview table data](4.2-Preview-table-data/)
3. [Working with CSV data enclosed in quotes](4.3-Working-with-CSV-data-enclosed-in-quotes/)
4. [Run SQL queries to explore the data](4.4-Run-SQL-queries-to-explore-the-data/)