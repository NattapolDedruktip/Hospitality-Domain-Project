# Introduction

This project uses **Power BI** to dive into data from the **hospitality industry in India** over a 3-month period. The goal is to turn raw data into useful insights, focusing on the metrics that matter most to stakeholders. It’s all about spotting trends, patterns, and opportunities to help drive better decisions in the hospitality sector.

What this project does:

- Creates interactive visuals and reports with **Power BI**.
- Focuses on key metrics provided by stakeholders.
- Analyzes 3 months of data to uncover useful insights.


![overview](/assets/overview_DB.gif)


    
# Background

This project focuses on analyzing data from the hospitality industry in India, designed as a practical learning experience guided by an expert resource. The workflow followed a structured process demonstrated in a tutorial, including a mock scenario to simulate real-world stakeholder interactions. Here’s how the project was carried out:

1. **Mock Stakeholder Meeting**
    
    In the first step, a mock meeting was conducted (as part of the tutorial) between the instructor and a simulated stakeholder. This helped demonstrate how to identify key metrics that matter to stakeholders and understand their expectations for insights from the data.
    
2. **Building the Dashboard**
    
    Using the techniques learned from the resource, a **Power BI** dashboard was developed to visualize the metrics identified in the mock meeting. The focus was on creating a clear and interactive design that aligned with stakeholder needs.
    
3. **Collaborative Analysis**
    
    In the final step, the tutorial guided how to analyze the dashboard collaboratively with the stakeholder (in a simulated setup). This step emphasized interpreting the data, spotting trends, and identifying actionable insights in line with stakeholder priorities.
    

This project served as a hands-on application of key data analysis and visualization skills, using a realistic mock scenario to simulate real-world workflows.



The data was sourced from the YouTube channel [codebasics](https://www.youtube.com/@codebasics)

[reference tutorial](https://www.youtube.com/watch?v=tT4V7zguCnc&list=PLeo1K3hjS3uv_e0HUEu1CVCOikPay64p8)

# Metrics List

| Measure | Description | DAX Formula |
| --- | --- | --- |
| Revenue | To get the total revenue realized | `SUM(Sales[Revenue])` |
| Occupancy % | The ratio of successful bookings to total room capacity. | `DIVIDE(SUM(Bookings[SuccessfulBookings]), SUM(Rooms[TotalCapacity]))` |
| ADR | Average Daily Rate: Ratio of revenue to rooms sold.     It is the measure of the average paid for rooms sold in a given time period | `DIVIDE(SUM(Sales[Revenue]), SUM(Bookings[RoomsSold]))` |
| Realisation % | Successful "checked out" percentage over all bookings. | `DIVIDE(SUM(Bookings[CheckedOut]), SUM(Bookings[TotalBookings]))` |
| DSRN | Daily Sellable Room Nights: Average rooms ready to sell per day over a specific period. | `AVERAGEX(CalendarTable, SUM(Rooms[AvailableRooms]))` |
| RavPAR | Revenue per Available Room. RevPAR can help hotels measure themselves against other properties or brands. | `DIVIDE(SUM(Sales[Revenue]), SUM(Rooms[AvailableRooms]))` |

# Visualization


![filter](/assets/filter.JPG)

At the top of the dashboard, there are three types of filters available for better data exploration and analysis:

- **Filter by City**: Allows users to focus on data from specific cities.
- **Filter by Room Type**: Includes two filters for room type (added as a mock-up to accommodate potential future enhancements).
- **Filter by Time Period**: Enables filtering by time frames, such as month or week, to analyze trends over specific periods.

## Key Metrics

![key metrics](/assets/keyMetrics.JPG)

In the middle left section of the visualization, there are **six key metrics** provided by the stakeholders.

- Below each metric, there is a **percentage change** that compares the current value to the **previous week**.
- Beneath these six metrics, a table breaks down the data **by type of day** (weekday vs. weekend), showing key figures for each day type.

![hover key metric](/assets/hoverKeyMetric.JPG)
- You can hover over any key metric to see its trend over time, allowing for a better understanding of how it has changed across different periods.

## Charts

### Donut Chart

![donut chart](/assets/donut.JPG)

- The donut chart in the middle displays the occupancy percentage for each hotel category based on the selected time period from the filters.

### Line Chart

![line Chart](/assets/lineChart.JPG)

- The line chart in the middle right of the visualization displays RevPAR, ADR, and Occupancy %. It illustrates the trend over time, showing variations across different months.

### Combo Chart (Bar And Line)

![Bar Chart](/assets/barchart.JPG)


- The chart in the bottom left of the visualization displays ADR (Average Daily Rate) for each booking platform, helping to compare performance across different platforms.

![table](/assets/table.JPG)

- The table in the bottom right of the visualization displays all key metrics, along with additional information such as average ratings for different properties. It is especially useful when comparing properties against each other.


# Analysis

![lineChart Analysis](/assets/lineChartAnalysis.JPG)

There are many ways to increase revenue in the hospitality industry, and **pricing strategy** is one of the most effective approaches.

From this line chart, we can observe two key metrics:

- **ADR (Average Daily Rate)** – This represents the **average revenue per room sold**, reflecting the pricing strategy of the hotel.
- **Occupancy %** – This indicates the **ratio of successful bookings to total room capacity**, showing the demand for rooms during a specific period.

Looking at the trends over the **three-month period**, we can see that while **occupancy % fluctuates significantly**, **ADR remains relatively stable**. This suggests that these hotels **may not be implementing any dynamic pricing strategies**

![weekday weekend Analysis](/assets/weekDayWeekEndAnalysis.JPG)

- The data above compares **Week 30 to Week 31**. One key observation is that while **weekend occupancy rates are 7% higher than weekdays**, the **ADR (Average Daily Rate) difference is only around 50**.

- According to the stakeholders, this suggests that **the same pricing strategy is being applied to both weekdays and weekends**

![platform analysis](/assets/platfromAnalysis.JPG)
- Normally, ADR from direct offline bookings is expected to be the highest, while direct online bookings should have the lowest ADR. However, based on the data, the **gap is only around 150**, which stakeholders feel is too small.

- Stakeholders **recommend focusing on direct online bookings to increase revenue**. However, they also advise **not to set different prices across platforms**, as this could **negatively impact hotel rankings and even lead to removal from some platforms**.

- Instead, the recommended approach is to **keep the same price across all platforms** and give them discount codes but use **higher discount codes for direct online bookings** to encourage more bookings through this channel.


![table analysis](/assets/tableAnalysis.JPG)
- From the data, it seems that **Occupancy %, Average Rating, and Revenue are correlated**. This suggests that hotels with **higher ratings tend to generate more revenue and have better occupancy rates**.

- To dive deeper, a **Level 2 analysis** would be needed to understand **why some hotels have lower ratings** and how improving these ratings could lead to higher revenue. However, at this stage, we **don’t have enough data** to determine the specific reasons behind the lower ratings.

- To move forward, collecting more data on **guest reviews, service quality, and customer feedback** would help identify areas for improvement and drive better performance.

# Solutions

Stakeholders mentioned that hotels usually follow one of these three pricing models:

1. **Flat Pricing** – Same price every day.
2. **Weekend/Weekday Pricing** – Different prices for weekends and weekdays.
3. **Dynamic Pricing** – Prices change based on demand, season, or other factors.

Looking at the dashboard data, it seems like these hotels are using **Flat Pricing**, since **ADR stays almost the same** even though **weekend occupancy is higher than weekdays**.


- Based on just the data we have here, **switching to a Weekend/Weekday Pricing model would make sense**. It’s a simple change but could help **bring in more revenue on high-demand days** without making pricing too complicated.




- **Increase Direct Booking Revenue**: Offer **exclusive incentives** (e.g., discounts, loyalty points, extra perks) to encourage bookings through the hotel’s own platform. Enhance the **user experience** for seamless direct booking, implement **targeted promotions** to attract repeat customers, and reduce reliance on OTA commissions.

- **Conduct Level 2 Analysis on Low-Performing Hotels**: Focus on the **five lowest-performing properties**, analyzing why they have **lower ratings** and how improvements could lead to higher revenue. Gather insights from **customer feedback, service quality, location, and pricing strategies**, then apply targeted improvements to enhance guest satisfaction and boost performance.



## Acknowledgment

This project could not have been completed without the guidance and support the valuable tutorials on  [codebasics](https://www.youtube.com/@codebasics)
