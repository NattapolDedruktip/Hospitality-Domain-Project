# Introduction

This project uses **Power BI** to dive into data from the **hospitality industry in India** over a 3-month period. The goal is to turn raw data into useful insights, focusing on the metrics that matter most to stakeholders. It’s all about spotting trends, patterns, and opportunities to help drive better decisions in the hospitality sector.

What this project does:

- Creates interactive visuals and reports with **Power BI**.
- Focuses on key metrics provided by stakeholders.
- Analyzes 3 months of data to uncover useful insights.


![overview](/assets/overview_DB.gif)


    
### Background

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

# Metrics list

| Measure | Description | DAX Formula |
| --- | --- | --- |
| Revenue | To get the total revenue realized | `SUM(Sales[Revenue])` |
| Occupancy % | The ratio of successful bookings to total room capacity. | `DIVIDE(SUM(Bookings[SuccessfulBookings]), SUM(Rooms[TotalCapacity]))` |
| ADR | Average Daily Rate: Ratio of revenue to rooms sold.     It is the measure of the average paid for rooms sold in a given time period | `DIVIDE(SUM(Sales[Revenue]), SUM(Bookings[RoomsSold]))` |
| Realisation % | Successful "checked out" percentage over all bookings. | `DIVIDE(SUM(Bookings[CheckedOut]), SUM(Bookings[TotalBookings]))` |
| DSRN | Daily Sellable Room Nights: Average rooms ready to sell per day over a specific period. | `AVERAGEX(CalendarTable, SUM(Rooms[AvailableRooms]))` |
| RavPAR | Revenue per Available Room. RevPAR can help hotels measure themselves against other properties or brands. | `DIVIDE(SUM(Sales[Revenue]), SUM(Rooms[AvailableRooms]))` |