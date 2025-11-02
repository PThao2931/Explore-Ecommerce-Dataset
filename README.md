# Ecommerce Project Instruction

## Query 1: Monthly Traffic Overview (Q1 2017) 

### Key Insights:
The report highlights monthly traffic trends for Q1 2017, showing post-holiday fluctuations and seasonal patterns. It establishes baseline metrics for visits, pageviews, and transactions, enabling conversion rate analysis to assess sales performance and user behavior.

### Out come
![result](https://github.com/PThao2931/Explore-Ecommerce-Dataset/blob/main/query1.png)
### The growth rate is given by: 

Transaction

$$
\frac{993 - 733}{733} \times 100 = 35,5\%
$$ 

Traffic

$$
\frac{69931 - 62192}{62192} \times 100 = 12.4\%
$$

### Key Concern:
The **pages/visit decline** is the only **negative** trend and needs attention. While conversion is improving, users may be browsing less deeply, possibly due to **content relevance or site navigation issues**, which could impact future sales if it continues.

### Bottom Line:
Q1 2017 shows **healthy growth with improving conversion efficiency**. March's exceptional performance (35,5% transaction growth vs 12.4% traffic growth) suggests either successful marketing campaigns, better product-market fit, or effective UX improvements. The company is moving in the right direction, converting traffic more efficiently each month, and should focus next on enhancing engagement depth to maximize long-term value per visitor.

### Action Items:
- Investigate declining pages/visit trend through content relevance and UX path analysis.
- Refine landing page messaging and on-site navigation to deepen engagement.
- Use Q1 conversion insights to optimize Q2 campaigns for retention and repeat purchase.
- Set monthly conversion benchmarks for continuous monitoring and improvement.

---

## Query 2: Bounce Rate by Traffic Source (July 2017)
### Key Insights:
This query explores how user engagement differs across traffic sources, by comparing the proportion of single-page sessions (bounces) against total visits.
It helps identify which channels bring high-intent, engaged visitors, and which ones may attract unqualified or poorly targeted traffic — guiding both marketing optimization and budget allocation decisions.

### Out come
![result](https://github.com/PThao2931/Explore-Ecommerce-Dataset/blob/main/query2.png)
(Top 10 traffic sources by visit volume)

### Top & Bottom Performers:
#### High Engagement (Lowest Bounce Rate):
- mail.google.com: 24.752% (101 visits)
- reddit.com: 28.571% (189 visits)
- blog.golang.org: 29.231% (65 visits)
#### Low Engagement (Highest Bounce Rate - significant traffic):
- duckduckgo.com: 87.5% (16 visits)
- l.facebook.com: 88.235% (51 visits)
- youtube.com: 66.73% (6,351 visits)
### Key Concern:
**YouTube's traffic quality** requires immediate attention. Despite being the 3rd largest traffic source (6,351 visits), it has a high bounce rate (66.73%), indicating content or landing page misalignment with user expectations from YouTube. This represents significant untapped potential requiring optimization.
### Bottom Line:
**Direct and organic search traffic** deliver the best quality with bounce rates under 52%. **Reddit and email referrals** show exceptional engagement (bounce rates <30%), indicating high-quality traffic worth increased investment. **Social media traffic** (YouTube, Facebook) shows elevated bounce rates (>53%), requiring landing page and content strategy optimization to improve conversion efficiency.
### Business Impact:
A consistently high bounce rate across paid or referral channels translates into lost conversion opportunities and wasted ad spend.
Improving landing page alignment for just one high-volume source (e.g., YouTube) could recover thousands of engaged sessions per month, directly improving ROI and reducing acquisition cost per qualified visit.
### Action Items:
- Sources with >70% bounce rate need landing page optimization
- Low bounce + high volume sources deserve increased investment
- Redesign or A/B test landing pages for YouTube and Facebook campaigns — focus on faster load times, clearer headlines, and stronger call-to-action relevance.
- Shift investment toward low-bounce, high-performing channels (Google, Direct) to maximize marketing efficiency.
- Refine audience targeting for high-bounce channels to attract more relevant users.
- Monitor bounce trends monthly to measure the effect of landing page and targeting optimizations.

## Query 3: Revenue by Traffic Source (June 2017)
### Key Insights:
This analysis examines revenue generation across traffic sources in June 2017, showing both monthly and weekly patterns. Direct traffic dominates at $97,333 (76% of total revenue), while Google and DFA contribute $27,619 combined (22%).
### Out come

### Key Concern:
Over-dependence on direct traffic (76%) creates attribution blindness and scaling limitations. Week 24's anomalous spike to $42.5K (double normal weeks) requires investigation—understanding this surge is critical for replication.
### Bottom Line:
June 2017 generated $128K in revenue with extreme concentration in direct traffic. While this indicates strong brand loyalty, only 21% comes from measurable, scalable paid channels. Week 24's performance shows 60-70% revenue upside potential if consistently achieved across all channels.
### Business Impact:
Heavy direct traffic reliance limits marketing optimization and creates revenue volatility ($10K-$42K weekly swings). If Week 24 performance were sustained, monthly revenue could reach $170K—a 33% increase. Current attribution gaps prevent identifying and scaling successful tactics.
### Action Items:
Investigate Week 24 spike to identify replicable drivers (promotions, campaigns, seasonality)
Implement UTM tracking to properly attribute direct traffic to original marketing sources
Increase investment in Google/DFA channels to diversify from 76% direct to 60% target
Set $25K weekly baseline with strategies to achieve consistent Week 24-level performance
Segment direct traffic by customer type and device to optimize high-value segments
Test budget allocation on underperforming channels (YouTube, Bing) for expansion opportunities
Làm gì:

Tính revenue từng nguồn traffic theo 2 góc độ: theo tháng và theo tuần
Sử dụng UNION ALL để gộp 2 cách nhìn

Insight: Xác định nguồn traffic nào mang lại doanh thu cao nhất, có xu hướng tăng/giảm theo tuần
Query 3: 
What it does:

Shows revenue contribution from each traffic source
Provides both monthly and weekly granularity via UNION ALL
Enables time-series revenue analysis

Key Insights:

Revenue Attribution: Identifies which channels drive actual sales, not just traffic
ROI Calculation: Essential for calculating Cost Per Acquisition (CPA) and Return on Ad Spend (ROAS)
Channel Mix Optimization: Reveals over/under-investment in specific channels
Weekly Volatility: Week-over-week view helps identify campaign spikes or drops

Strategic Value:

A channel with high traffic but low revenue = poor targeting
A channel with low traffic but high revenue = scale opportunity
Compare with Query 2: Low bounce rate + high revenue = ideal channel

## Query 4: Pageview Behavior - Purchasers vs Non-Purchasers (Jun-Jul 2017
Làm gì:

Tính trung bình số pageviews/user cho 2 nhóm:

Nhóm có mua hàng (có revenue, có transaction)
Nhóm không mua (không có revenue, không có transaction)

Insight: Người mua thường xem nhiều trang hơn → hiểu journey của khách hàng

What it does:
- Compares average pageviews per user between two cohorts:
  - Users who made purchases
  - Users who didn't purchase

Key Insights:
- **Purchase Intent Signal**: Purchasers typically view 2-4x more pages than browsers
- **Content Engagement**: High pageviews before purchase indicate strong product research behavior
- **Funnel Depth**: Helps understand how much browsing is needed before conversion
- **User Experience Quality**: Extreme gaps may indicate friction in the buyer journey

Typical Findings
- **Purchasers**: 8-15 pageviews on average (browsing multiple products, reviews, comparisons)
- **Non-purchasers**: 2-5 pageviews (quick look, then bounce)

Business Applications:
- **Remarketing Strategy**: Target users with 5-10 pageviews (high intent but didn't convert)
- **Content Optimization**: If purchasers need 15+ pages, simplify navigation
- **Predictive Analytics**: Use pageview count as a conversion likelihood indicator


## Query 5: Average Transactions Per User (July 2017)
Làm gì: Tính số transactions trung bình trên mỗi user có mua hàng
Insight: Đo lường loyalty - user có xu hướng mua nhiều lần không?
**

**What it does:**
- Calculates how many transactions each purchasing user completes on average
- Filters only users who made at least one purchase

**Key Insights:**
- **Repeat Purchase Rate**: Values >1.2 indicate good customer retention
- **Cart Behavior**: Multiple transactions might indicate:
  - Split purchases due to payment issues
  - Intentional separate orders (gifts, different addresses)
  - Abandoned carts that reconverted
- **Customer Lifetime Value (CLV)**: Foundation metric for calculating long-term customer worth

**Benchmarks:**
- **<1.05**: Rare repeat purchases (luxury items, infrequent needs)
- **1.1-1.3**: Healthy repeat rate (standard e-commerce)
- **>1.5**: Excellent loyalty or subscription-like behavior

**Action Items:**
- Low ratio? Implement:
  - Post-purchase email campaigns
  - Loyalty programs
  - Bundle discounts for repeat purchases

    

## Query 6: Average Revenue Per Visit (July 2017)
Làm gì: Tính revenue trung bình cho mỗi visit có phát sinh giao dịch
Insight: Giá trị đơn hàng trung bình - metric quan trọng để tính ROI marketing
**

**What it does:**
- Calculates average order value (AOV) per visit that resulted in a transaction
- Measures monetary value per converting visit

**Key Insights:**
- **Pricing Strategy Effectiveness**: Tracks if customers are buying high-margin items
- **Upsell/Cross-sell Performance**: Increasing AOV means bundling strategies work
- **Market Positioning**: High AOV = premium positioning; Low AOV = volume play
- **Campaign ROI**: If Customer Acquisition Cost (CAC) = $30 and AOV = $25, you're losing money

**Optimization Strategies:**
- **Low AOV (<$50)**: Add "Frequently Bought Together" bundles, minimum free shipping thresholds
- **Medium AOV ($50-$150)**: Implement tiered discounts ("Spend $100, save 10%")
- **High AOV (>$200)**: Focus on VIP service, premium packaging, extended warranties



If AOV = $75 and conversion rate = 2%
→ Revenue per visit (all traffic) = $75 × 0.02 = $1.50
→ Must acquire traffic for <$1.50 to be profitable

## Query 7: Product Affinity Analysis (July 2017)
Làm gì:

Tìm những user đã mua "YouTube Men's Vintage Henley"
Xem họ còn mua sản phẩm gì khác nữa

Insight: Phát hiện cơ hội cross-sell, bundle products, hoặc upsell

**What it does:**
- Identifies products frequently purchased together with "YouTube Men's Vintage Henley"
- Classic market basket analysis

**Key Insights:**
- **Cross-Sell Opportunities**: "Customers who bought X also bought Y"
- **Product Bundling**: Create pre-packaged bundles of frequently paired items
- **Merchandising Strategy**: Place related products near each other on site/in emails
- **Inventory Planning**: Stock complementary products proportionally

**Real-World Applications:**
- **Recommendation Engines**: Power "You May Also Like" sections
- **Email Marketing**: Send targeted product suggestions post-purchase
- **Category Management**: Understand product category relationships

**Example Findings:**
```
Users who bought "YouTube Men's Vintage Henley" also bought:
1. YouTube Logo T-Shirt (Qty: 45) → Same brand loyalty
2. Android Sticker Pack (Qty: 32) → Tech enthusiast profile
3. Google Water Bottle (Qty: 28) → Lifestyle accessories
```

**Action**: Create a "Tech Brand Fan Bundle" with 10% discount

## Query 8: E-commerce Conversion Funnel (Q1 2017
Làm gì:

Đếm số user ở 3 bước:

View product (action_type = 2)
Add to cart (action_type = 3)
Purchase (action_type = 6)


Tính tỷ lệ chuyển đổi giữa các bước

Insight: Phát hiện "nút thắt cổ chai" trong funnel - ví dụ nhiều người add to cart nhưng ít người checkout → cần tối ưu trang thanh toán
E-commerce Conversion Funnel (Q1 2017)**

**What it does:**
- Tracks user progression through three key stages:
  1. **Product View** (action_type = 2)
  2. **Add to Cart** (action_type = 3)
  3. **Purchase** (action_type = 6)
- Calculates conversion rates between stages

**Key Insights:**
- **Bottleneck Identification**: Pinpoints where users drop off
- **Funnel Health Score**: Healthy funnels typically show:
  - **View → Add to Cart**: 5-15%
  - **Add to Cart → Purchase**: 30-50%
  - **View → Purchase**: 2-5%

**Critical Metrics:**
```
Example Funnel:
10,000 Product Views
→ 1,000 Add to Cart (10% add-to-cart rate) ✅ Healthy
→ 200 Purchases (20% purchase rate from cart) ⚠️ Below average


Diagnosis: Cart abandonment issue
```

**Common Problems & Solutions:**

| Low Rate | Problem | Solution |
|----------|---------|----------|
| **<5% Add-to-Cart** | Product page issues | Better images, reviews, descriptions, clear CTAs |
| **<25% Purchase from Cart** | Checkout friction | Simplify checkout, add guest checkout, show trust badges |
| **High cart abandonment** | Unexpected costs | Show total cost early, reduce shipping fees |

**Strategic Value:**
- **Week-over-week monitoring**: Detect technical issues (broken checkout) immediately
- **A/B testing validation**: Measure impact of UX changes on conversion rates
- **Budget allocation**: If top-of-funnel is strong but conversion is weak, invest in checkout optimization instead of more traffic

Tổng kết Insight chính:
Bộ queries này đang phân tích hiệu quả kinh doanh E-commerce từ nhiều góc độ:

Traffic & Engagement (Q1, Q2)
Revenue Analysis (Q3, Q6)
Customer Behavior (Q4, Q5, Q7)
Conversion Optimization (Q8)
