This project analyzes hotel booking data to understand cancellation behavior and revenue exposure.
The objective is to identify high-risk booking patterns and customer segments that contribute disproportionately to revenue loss due to cancellations.

The analysis focuses on:

Booking lead time

Cancellation rates

Revenue at risk

Market segments and distribution channels

📂 Dataset

Source: Hotel booking dataset (City Hotel & Resort Hotel)

Records: ~119,000 bookings

Granularity: Individual booking level

Key Fields Used

is_canceled

lead_time

adr

stays_in_week_nights, stays_in_weekend_nights

market_segment

distribution_channel

🧹 Data Preparation & Feature Engineering

All data preparation was performed in Excel.

Engineered Features

Total Nights

total_nights = stays_in_week_nights + stays_in_weekend_nights


Booking Revenue

booking_revenue = adr × total_nights


Estimated Revenue at Risk

Revenue associated with canceled bookings

Lead Time Buckets

0–7 Days

8–30 Days

31–90 Days

90+ Days

Notes

Bookings with zero nights and zero revenue were retained as valid booking records.

Very small or undefined segments were excluded from final visuals to avoid misleading interpretations.

📊 Analysis & Visualizations
1. Cancellation Rate by Lead Time

Cancellation likelihood increases sharply with longer lead times.

Bookings made 90+ days in advance have a cancellation rate above 50%.

Insight: Early bookings drive volume but significantly increase cancellation risk.

2. Revenue at Risk (%) by Lead Time

Revenue exposure follows the same pattern as cancellation rates.

Nearly half of the revenue from bookings made 90+ days in advance is at risk.

Insight: Long lead-time bookings represent the highest financial risk.

3. Revenue at Risk (%) by Market Segment

Group and Online TA segments show the highest revenue risk percentages.

Corporate and Direct segments are comparatively more stable.

Insight: High-volume segments also carry disproportionate cancellation-related revenue exposure.

4. Revenue at Risk (%) by Distribution Channel

OTA / Travel Agent channels dominate revenue risk.

Direct and Corporate channels exhibit lower relative risk.

Insight: Channel mix plays a critical role in revenue stability.

🔑 Key Insights (Summary)

Cancellation probability increases with booking lead time.

Long lead-time bookings expose a significantly larger share of revenue to risk.

OTA and Group segments combine high revenue volume with high cancellation exposure.

Revenue risk is concentrated in specific customer segments and channels, not evenly distributed.

📌 Business Implications

Consider stricter cancellation or deposit policies for long lead-time bookings.

Reevaluate OTA and Group channel strategies to balance volume and risk.

Use lead time as a key input for demand and revenue risk management.

🛠 Tools Used

Excel

Data cleaning & feature engineering

Pivot tables for aggregation

Charts for visualization and insight communication

📎 Project Structure
├── Hotel_Booking_Analysis.xlsx
│   ├── hotel_bookings        (cleaned data)
│   ├── Pivot table           (aggregations & metrics)
│   └── Step 3 Visuals        (final charts)
└── README.md
