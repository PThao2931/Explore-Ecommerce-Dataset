# Ecommerce Project Instruction

## ** Query 1: Monthly Traffic Overview (Q1 2017)***

## What does it is: ## Tracks total visits, pageviews, and transactions across January-March 2017. Aggregates data at monthly level

Key Insights:

Trend Analysis: Identifies whether traffic is growing or declining month-over-month
Seasonality Pattern: Q1 typically shows post-holiday traffic patterns
Volume Baseline: Establishes baseline metrics for comparison with other periods
Transaction Rate: Can calculate conversion rate (transactions/visits) to measure sales efficiency


Business Impact:

Helps forecast resource allocation for peak periods
Identifies if marketing campaigns in Q1 were effective
Provides historical benchmarks for year-over-year comparisons

![result](https://github.com/PThao2931/Explore-Ecommerce-Dataset/blob/main/query1.png)


## **📊 Main Insights:**

### **1. Strong Quarter-End Performance**
- March showed the best performance across all metrics
- Visits increased 12.4% from February to March
- Transactions surged 35.5% (733 → 993), significantly outpacing traffic growth
- This indicates improving conversion efficiency, not just more traffic

### **2. Improving Conversion Rate Trend**
- January: 1.10% conversion rate (713/64,694)
- February: 1.18% conversion rate (733/62,192) 
- March: 1.42% conversion rate (993/69,931)
- **29% improvement** from January to March shows successful optimization efforts or better quality traffic

### **3. February Seasonal Dip is Normal**
- February visits dropped 3.9% from January
- This is expected due to fewer calendar days (28 vs 31)
- When adjusted for days: Feb actually had 2,221 visits/day vs Jan's 2,087/day
- The monthly totals are misleading - daily performance actually improved

### **4. Declining User Engagement**
- Pages per visit decreased from 3.98 (Jan) → 3.75 (Feb) → 3.71 (Mar)
- 6.8% decline over the quarter
- This could indicate: better site navigation (positive), increasing mobile traffic (neutral), or declining content quality (negative)
- Requires further investigation to determine root cause

### **5. Q1 Overall: Positive Trajectory**
- Total Q1: 197,017 visits | 850,603 pageviews | 2,439 transactions
- Quarter ended 8.1% higher in visits than it started
- Transaction growth (39% from Jan to Mar) far exceeded traffic growth
- Revenue efficiency is improving - getting more value from each visit

---

## **⚠️ Key Concern:**

The **pages/visit decline** is the only negative trend and needs attention. While conversion is improving, users are browsing less deeply, which could impact future sales if it continues.

---

## **🎯 Bottom Line:**

Q1 2017 shows **healthy growth with improving conversion efficiency**. March's exceptional performance (35% transaction growth vs 12% traffic growth) suggests either successful marketing campaigns, better product-market fit, or effective UX improvements. The company is moving in the right direction, converting traffic more efficiently each month.

##Query 2: Phân tích Bounce Rate theo nguồn traffic (Tháng 7/2017)
Làm gì:

Tính tổng visits và bounces từ mỗi nguồn traffic (Google, direct, referral...)
Tính bounce rate = (số bounces / tổng visits) × 100

Insight: Nguồn traffic nào có bounce rate cao → chất lượng traffic kém, cần tối ưu

Query 3: Doanh thu theo nguồn traffic (Tháng 6/2017)
Làm gì:

Tính revenue từng nguồn traffic theo 2 góc độ: theo tháng và theo tuần
Sử dụng UNION ALL để gộp 2 cách nhìn

Insight: Xác định nguồn traffic nào mang lại doanh thu cao nhất, có xu hướng tăng/giảm theo tuần

Query 4: So sánh hành vi người mua vs không mua (Jun-Jul 2017)
Làm gì:

Tính trung bình số pageviews/user cho 2 nhóm:

Nhóm có mua hàng (có revenue, có transaction)
Nhóm không mua (không có revenue, không có transaction)



Insight: Người mua thường xem nhiều trang hơn → hiểu journey của khách hàng

Query 5: Trung bình số giao dịch/user (Tháng 7/2017)
Làm gì: Tính số transactions trung bình trên mỗi user có mua hàng
Insight: Đo lường loyalty - user có xu hướng mua nhiều lần không?

Query 6: Doanh thu trung bình/visit (Tháng 7/2017)
Làm gì: Tính revenue trung bình cho mỗi visit có phát sinh giao dịch
Insight: Giá trị đơn hàng trung bình - metric quan trọng để tính ROI marketing

Query 7: Sản phẩm hay mua cùng (Cross-selling - Tháng 7/2017)
Làm gì:

Tìm những user đã mua "YouTube Men's Vintage Henley"
Xem họ còn mua sản phẩm gì khác nữa

Insight: Phát hiện cơ hội cross-sell, bundle products, hoặc upsell

Query 8: Funnel chuyển đổi E-commerce (Q1/2017)
Làm gì:

Đếm số user ở 3 bước:

View product (action_type = 2)
Add to cart (action_type = 3)
Purchase (action_type = 6)


Tính tỷ lệ chuyển đổi giữa các bước

Insight: Phát hiện "nút thắt cổ chai" trong funnel - ví dụ nhiều người add to cart nhưng ít người checkout → cần tối ưu trang thanh toán

Tổng kết Insight chính:
Bộ queries này đang phân tích hiệu quả kinh doanh E-commerce từ nhiều góc độ:

Traffic & Engagement (Q1, Q2)
Revenue Analysis (Q3, Q6)
Customer Behavior (Q4, Q5, Q7)
Conversion Optimization (Q8)
