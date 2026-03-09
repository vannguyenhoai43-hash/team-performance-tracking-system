# Hệ thống Theo dõi Hiệu suất Nhóm - Google Sheet

Đọc bằng: [English](README.md) | **Tiếng Việt**


## Tổng quan dự án

**Theo dõi hiệu suất đội nhóm bằng cách thủ công thường bị “gãy” khi quản lý cần nhìn cùng lúc tiến độ công việc, mức độ hoàn thành KPI, và hiệu suất shop.** Trong thực tế, task, KPI cá nhân, và kết quả shop thường nằm ở các file hoặc góc nhìn tách rời nhau, khiến việc review định kỳ chậm, rời rạc, và khó hành động.

Dự án này xây dựng một **hệ thống theo dõi hiệu suất trên Google Sheets** kết nối theo 3 lớp **Task → Member → Shop** trong cùng một workflow giám sát.

Thay vì duy trì nhiều tracker riêng lẻ, hệ thống sử dụng **một lớp input trung tâm** để tự động cập nhật các dashboard, KPI view, và logic forecast. File được thiết kế để phục vụ **review định kỳ**, cho phép lọc theo **tháng, thành viên, và shop** nhưng vẫn giữ cùng một cấu trúc báo cáo xuyên suốt.

---

## Phạm vi hệ thống

Hệ thống hỗ trợ lọc động theo tháng, thành viên, và shop, giúp:

- **theo dõi task theo ngày, tuần, tháng**
- **theo dõi KPI ở cấp cá nhân và toàn team**
- **dự báo khả năng hoàn thành KPI cuối kỳ**
- **đánh giá hiệu suất ở cấp shop**

Toàn bộ dữ liệu trong file là **dữ liệu mô phỏng theo cấu trúc thực tế** và không chứa thông tin nhạy cảm.

---

## Tôi đã xây dựng gì

- Xây dựng **hệ thống theo dõi hiệu suất trên Google Sheets** với một lớp input và nhiều dashboard liên kết
- Thiết kế logic theo dõi theo cấu trúc **Task → Member → Shop**
- Thiết lập các công thức tự động để tính KPI summary, dashboard metrics, và forecast view
- Xây dựng các dashboard cho **tổng quan team, task tracking, hiệu suất KPI thành viên, forecast KPI, và hiệu suất shop**
- Thiết kế cơ chế lọc động để người dùng có thể chuyển theo **tháng, thành viên, và shop** mà không cần chỉnh sửa công thức thủ công

---

## Logic phân tích

Hệ thống được xây quanh 3 câu hỏi quản lý liên kết với nhau:

### 1. Kiểm soát thực thi
Ở **cấp task**, hệ thống theo dõi tiến độ, trạng thái, deadline, mức độ ưu tiên, và workload để giúp quản lý nhìn nhanh phần nào đang trễ, quá tải, hoặc lệch kế hoạch.

![task_tracker](images/task_tracker.png)

### 2. Trách nhiệm KPI
Ở **cấp thành viên**, hệ thống so sánh tiến độ KPI giữa từng PIC và toàn team, giúp xác định ai đang đạt mục tiêu, ai đang chậm, và khoảng cách đến từ đâu.

![pfm_PIC](images/pfm_pic_tracker.png)

### 3. Tác động kinh doanh
Ở **cấp shop**, hệ thống kết nối việc thực thi của team với kết quả kinh doanh bằng cách theo dõi các nhóm KPI như **Orders, Ad GMV, Paid Ads, Livestream, và Video** theo shop được phân công.

![pfm_shop](images/pfm_shop.png)

Nhờ đó, file này không chỉ là một task tracker, mà trở thành một **hệ thống giám sát nhiều lớp** liên kết giữa thực thi công việc và hiệu suất kinh doanh.

---

## Thành phần cốt lõi

Hệ thống gồm 5 thành phần chính:

- **Data Input trung tâm**: một lớp cập nhật chung cho task và KPI
- **Theo dõi team & task**: tiến độ, deadline, workload, completion rate, và priority
- **Hiệu suất KPI thành viên**: theo dõi KPI theo thành viên, team, tháng, và quý
- **Dự báo KPI**: ước tính khả năng hoàn thành cuối kỳ dựa trên run rate và xu hướng gần nhất
- **Hiệu suất shop**: theo dõi KPI, kênh bán, và xu hướng kinh doanh theo shop và member được chọn

---

## Ví dụ use case

- Một thành viên có thể vẫn đạt tiến độ **task completion**, nhưng vẫn hụt KPI vì shop được phụ trách đang underperform ở **Paid Ads** hoặc **Livestream**.
- Một shop có thể giữ được kết quả topline ổn định, nhưng lớp forecast vẫn cảnh báo **rủi ro hụt KPI cuối kỳ** dựa trên run rate hiện tại và phân bổ phần việc còn lại.
- Khoảng cách KPI ở cấp team có thể được truy ngược về tổ hợp cụ thể giữa **độ trễ thực thi, hiệu suất thành viên, và hiệu suất shop**, thay vì phải review từng phần rời rạc.

Chính các use case này làm cho hệ thống hữu ích hơn một task tracker thông thường hoặc một dashboard tĩnh.

---

## Tác động vận hành

- Thay thế cách theo dõi rời rạc giữa **task, member, và shop** bằng một cấu trúc review liên kết
- Giảm phụ thuộc vào follow-up thủ công nhờ gom cập nhật về một lớp input trung tâm
- Tăng khả năng nhìn thấy **trạng thái thực thi, khoảng cách KPI, và rủi ro underperformance** trong cùng một luồng theo dõi
- Hỗ trợ review định kỳ bằng cơ chế lọc động theo **tháng, thành viên, và shop**, thay vì phải tạo lại nhiều góc nhìn riêng

---

## Phạm vi và giới hạn

Dự án này được thiết kế cho mục tiêu **theo dõi hiệu suất và giám sát vận hành**, không nhằm thay thế các mô hình dự báo nâng cao hay xử lý dữ liệu quy mô lớn.

Điểm mạnh của hệ thống nằm ở tính dễ dùng, minh bạch, và khả năng tái sử dụng logic review ngay trong **Google Sheets**. Đổi lại, hệ thống phù hợp nhất với bài toán theo dõi team có cấu trúc, hơn là các workflow dữ liệu lớn.

---

## Đầu ra chính

- **Hệ thống theo dõi hiệu suất trên Google Sheets**
- **Dashboard tổng quan team**
- **Dashboard theo dõi task**
- **Dashboard KPI thành viên**
- **Forecast KPI**
- **Dashboard hiệu suất shop**

**FILE CHI TIẾT** [TẠI ĐÂY](https://docs.google.com/spreadsheets/d/1Yenltej4gWU9nJimhRiPbkxyMMUPeSArb9E1LzAAtMI/edit?gid=1802438500#gid=1802438500)
