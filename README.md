# Ecommerce Project Instruction

## Query 1: Monthly Traffic Overview (Q1 2017) 

### Key Insights:
The report highlights monthly traffic trends for Q1 2017, showing post-holiday fluctuations and seasonal patterns. It establishes baseline metrics for visits, pageviews, and transactions, enabling conversion rate analysis to assess sales performance and user behavior.

### Business Impact:
This analysis supports resource planning for peak periods, evaluates Q1 marketing effectiveness, and provides historical benchmarks for year-over-year performance tracking.

### Out come

![result](https://github.com/PThao2931/Explore-Ecommerce-Dataset/blob/main/query1.png)

$$
\frac{993 - 733}{733} \times 100 = 35,5\%
$$ 

The growth rate is given by: 
$\left( \dfrac{69931 - 62192}{62192} \times 100 = 12.4\% \right)$

### Key Concern:

The **pages/visit decline** is the only **negative** trend and needs attention. While conversion is improving, users are browsing less deeply, which could impact future sales if it continues.

### Bottom Line:

Q1 2017 shows **healthy growth with improving conversion efficiency**. March's exceptional performance (35,5% transaction growth vs 12.4% traffic growth) suggests either successful marketing campaigns, better product-market fit, or effective UX improvements. The company is moving in the right direction, converting traffic more efficiently each month.

---

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
