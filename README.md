# Project : team-performance-tracking-system

## 1. **Giới thiệu dự án** 
Dự án xây dựng hệ thống theo dõi hiệu suất (Performance Tracking System) cho team thông qua Google Sheets, cho phép:

- Theo dõi hiệu suất theo ngày, tuần, tháng của từng thành viên và của cả team
- Giám sát tiến độ công việc và trạng thái task
- Hỗ trợ quản lý ra quyết định nhanh chóng
Toàn bộ dữ liệu trong dashboard là dữ liệu mô phỏng dựa trên cấu trúc thực tế, không sử dụng dữ liệu nhạy cảm.
  
## **2. Mục tiêu** 
- Chuẩn hóa cấu trúc nhập liệu 
- Tự động hóa tính toán KPI & hiệu suất
- Tạo dashboard tổng quan đến dashboard chi tiết
- Giảm thao tác tổng hợp thủ công
  
## **3. Cấu trúc hệ thống Sheet** 

### **Sheet 1 – Data Input** 
Cập nhật dữ liệu hiệu suất KPI hàng ngày hoặc hàng tuần Khi dữ liệu được cập nhật:

=> Các sheet dashboard tự động cập nhật theo công thức

### **Sheet 2 – Overview PFM (Home Dashboard)** 

Dashboard tổng quan hiệu suất toàn team theo tháng. 

Dashboard hiển thị: 

  - Tổng số task và trạng thái thực hiện 
  - KPI Score và Efficiency của toàn team và theo từng PIC
  - Phân bổ công việc theo nhóm / loại task
  - Người dùng có thể tương tác thông qua bộ lọc theo **thời gian và tên PIC** để theo dõi hiệu suất linh hoạt.
  
Hỗ trợ quản lý:

  - Nắm nhanh tình hình thực hiện KPI
  - So sánh hiệu suất giữa các thành viên
  - Phát hiện điểm nghẽn trong phân bổ công việc

[overview](images/overview_tracker)
    
### **Sheet 4 – Task Tracker** 

Task Tracker là trung tâm quản lý và giám sát toàn bộ công việc của team theo ngày, tuần, tháng. 

Sheet bao gồm bảng mô tả task chi tiết kết hợp với dashboard tổng hợp nhằm:

- Theo dõi tiến độ thực hiện và tình trạng deadline
- Đánh giá hiệu suất của toàn team và từng PIC
- Phân tích workload và mức độ hoàn thành theo thời gian
- Phân loại công việc theo mức độ ưu tiên và nhóm nhiệm vụ

Sheet này giúp quản lý nắm nhanh tình hình vận hành, đánh giá hiệu quả phân bổ nguồn lực và kịp thời phát hiện các điểm nghẽn trong quy trình làm việc.

[task_tracker](images/task_tracker)

### **Sheet 5 – Hiệu suất KPI của thành viên**

Sheet dùng để đánh giá hiệu suất theo từng thành viên hoặc toàn team theo tháng hoặc quý, đồng thời dự báo khả năng đạt KPI vào cuối kỳ.

1. Phân tích KPI của từng thành viên và toàn toàn team

  Phần này theo dõi bộ KPI gồm Orders, AdGMV, Paid Ads, Livestream và Video.
  
  Người dùng có thể chọn theo tháng, theo quý, theo từng thành viên hoặc toàn team, số liệu và biểu đồ sẽ tự động cập nhật.
  
  Dashboard giúp:

   - Xác định metric nào đang vượt target hoặc chưa đạt
   - Với từng thành viên, chỉ ra metric thiếu hụt đến từ shop nào
   - Với toàn team, xác định thành viên nào đang kéo giảm metric chung
   - Theo dõi xu hướng 3 tháng gần nhất để đánh giá độ ổn định hiệu suất

=> Hỗ trợ đánh giá năng lực cá nhân và phân tích nguyên nhân gốc của sự thiếu hụt KPI.

[pfm_PIC](images/pfm_pic_tracker)

2. Dự đoán hiệu suất KPI
   
Dự báo khả năng hoàn thành KPI vào cuối tháng dựa trên:

- Runrate thực tế tại thời điểm hiện tại

- So sánh với cùng kỳ và tháng trước

- Phân bổ theo xu hướng các ngày còn lại của 3 tháng gần nhất

Kết quả forecast được đối chiếu với target để đánh giá mức độ hoàn thành và phát hiện sớm rủi ro không đạt KPI.

[pfm_PIC](images/forcast_tracker)

### Sheet 6 – Hiệu suất theo shop

- Sheet dùng để theo dõi hiệu suất của từng shop theo bộ KPI của thành viên đảm nhiệm shop đó. 
- Người dùng có thể chọn theo thành viên để hiển thị danh sách các shop phụ trách. 
- Toàn bộ chỉ số KPI và biểu đồ sẽ tự động cập nhật theo shop được chọn.

**Khối 1: Phân tích hiệu suất tương quan** 
- ADO và GMV
- Paid Ads và Impression
- CPC và CTR
  
=> Khối này giúp đánh giá hiệu quả vận hành và quảng cáo, xác định liệu tăng trưởng đến từ nhu cầu tự nhiên hay từ hoạt động trả phí.
  
**Khối 2: Phân tích theo doanh thu và đơn hàng**
- Trend theo ngày
- Cơ cấu đóng góp
- Phân bổ theo sub-category
  
=> Mục tiêu là xác định nguồn tăng trưởng chính và nhóm sản phẩm đóng góp lớn vào doanh thu.
  
**Khối 3: Phân tích theo kênh bán hàng: Livestream và Video**
- Xu hướng đơn hàng theo kênh
- Lượt thêm vào giỏ hàng theo kênh
- Khả năng ra đơn hàng theo các ngày trong tuần

=> Giúp đánh giá mức độ hiệu quả của hoạt động livestream và video trong việc thúc đẩy chuyển đổi.

[pfm_shop](images/pfm_shop)

FILE CHI TIẾT  [TẠI ĐÂY](images/full_tracker)

## 4. Giá trị hệ thống

- Tạo một framework theo dõi hiệu suất đa tầng từ Task đến Shop
- Chuẩn hóa cách đo lường KPI giữa các thành viên
- Giúp quản lý theo dõi hiệu suất và rủi ro target theo thời gian thực
- Hỗ trợ ra quyết định dựa trên dữ liệu thay vì tổng hợp thủ công
