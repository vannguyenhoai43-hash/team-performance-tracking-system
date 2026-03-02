# Project : team-performance-tracking-system

## 1. **Giới thiệu dự án** 
Dự án xây dựng hệ thống theo dõi hiệu suất (Performance Tracking System) cho team thông qua Google Sheets, cho phép:

- Theo dõi hiệu suất theo ngày, tuần, tháng của từng thành viên và của cả team
- Giám sát tiến độ công việc và trạng thái task
- Tự động tính toán KPI và dashboard tổng hợp
- Hỗ trợ quản lý ra quyết định nhanh chóng

Toàn bộ dữ liệu trong dashboard là dữ liệu mô phỏng dựa trên cấu trúc thực tế, không sử dụng dữ liệu nhạy cảm.

## **2. Cấu trúc hệ thống Sheet** 

### **Sheet 1 – Data Input** 

Cập nhật dữ liệu hiệu suất KPI hàng ngày hoặc hàng tuần Khi dữ liệu được cập nhật:

Các sheet dashboard tự động cập nhật theo công thức

### **Sheet 2 – Dashboard Tổng quan** 

Dashboard tổng quan hiệu suất toàn team theo tháng. 

Dashboard hiển thị: 

  - Tổng số task và trạng thái thực hiện 
  - KPI Score và Efficiency của toàn team và theo từng PIC
  - Phân bổ công việc theo nhóm / loại task
  - Người dùng có thể tương tác thông qua bộ lọc theo thời gian và tên PIC để theo dõi hiệu suất linh hoạt.

[overview](images/overview_tracker.png)
    
### **Sheet 4 – Theo dõi Task** 

Task Tracker là trung tâm quản lý và giám sát toàn bộ công việc của team theo ngày, tuần, tháng. 

Sheet bao gồm bảng mô tả task chi tiết kết hợp với dashboard tổng hợp nhằm:

- Theo dõi tiến độ thực hiện và tình trạng deadline
- Đánh giá hiệu suất của toàn team và từng PIC
- Phân tích workload và mức độ hoàn thành theo thời gian
- Phân loại công việc theo mức độ ưu tiên và nhóm nhiệm vụ

[task_tracker](images/task_tracker.png)

### **Sheet 5 – Hiệu suất KPI của thành viên**

Sheet dùng để đánh giá hiệu suất theo từng thành viên hoặc toàn team theo tháng hoặc quý, đồng thời dự báo khả năng đạt KPI vào cuối kỳ.

#### 1. Phân tích KPI của từng thành viên và toàn team

  Phần này theo dõi bộ KPI gồm Orders, AdGMV, Paid Ads, Livestream và Video.
  
  Người dùng có thể chọn theo tháng, theo quý, theo từng thành viên hoặc toàn team, số liệu và biểu đồ sẽ tự động cập nhật.
  
  Dashboard giúp:
   - So sánh mức độ hoàn thành KPI theo thành viên và toàn team
   - Phân tích nguyên nhân thiếu hụt theo shop phụ trách
   - Theo dõi xu hướng 3 tháng gần nhất

[pfm_PIC](images/pfm_pic_tracker.png)

#### 2. Dự đoán hiệu suất KPI
   
Dự báo khả năng hoàn thành KPI vào cuối tháng dựa trên:

- Runrate thực tế tại thời điểm hiện tại

- So sánh với cùng kỳ và tháng trước

- Phân bổ theo xu hướng các ngày còn lại của 3 tháng gần nhất

Kết quả forecast được đối chiếu với target để đánh giá mức độ hoàn thành và phát hiện sớm rủi ro không đạt KPI.

[pfm_PIC](images/forecast_tracker.png)

### Sheet 6 – Hiệu suất theo shop

Sheet theo dõi hiệu suất từng shop theo bộ KPI của thành viên phụ trách. 
Dashboard tự động cập nhật theo shop và thành viên được chọn.

**Khối 1: Phân tích hiệu suất tương quan** 
- ADO và GMV
- Paid Ads và Impression
- CPC và CTR
  
**Khối 2: Phân tích theo doanh thu và đơn hàng**
- Trend theo ngày
- Cơ cấu đóng góp
- Phân bổ theo sub-category
  
**Khối 3: Phân tích theo kênh bán hàng: Livestream và Video**
- Xu hướng đơn hàng theo kênh
- Lượt thêm vào giỏ hàng theo kênh
- Khả năng ra đơn hàng theo các ngày trong tuần

[pfm_shop](images/pfm_shop.png)

**FILE CHI TIẾT** [TẠI ĐÂY](https://docs.google.com/spreadsheets/d/1Yenltej4gWU9nJimhRiPbkxyMMUPeSArb9E1LzAAtMI/edit?gid=1802438500#gid=1802438500)

## 4. Giá trị hệ thống

- Xây dựng framework theo dõi hiệu suất đa tầng từ Task → Member → Shop

- Chuẩn hóa cách đo lường KPI trong team

- Tích hợp performance tracking và forecasting trong cùng một hệ thống

- Hỗ trợ ra quyết định dựa trên dữ liệu thay vì báo cáo thủ công
