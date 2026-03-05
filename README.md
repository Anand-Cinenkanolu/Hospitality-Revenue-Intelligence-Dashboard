# 🏨 Grand Hotel's Revenue Recovery Analysis

📊 **Data-Driven Insights for Strategic Hotel Revenue Optimization**

---

## 📌 Project Overview

AtliQ Grands is a 20-year-old luxury hotel chain operating across 4 major Indian cities. Facing pressure from competitors and declining revenue, the managing director decided to adopt business intelligence to recover market share. With no in-house analytics team, a third-party analyst was brought in to deliver insights from historical booking data.

---

## 🎯 Objective

Analyze 130,000+ hotel booking records and build an executive-ready Power BI dashboard that tracks key hospitality KPIs, identifies revenue opportunities, and supports strategic pricing and performance decisions.

---

## 💡 Key Business Insights

- **Mumbai leads all cities** with ₹660M in revenue, making it the most critical strategic market
- **AtliQ Exotica Mumbai** is the top-performing property at ₹210M, outperforming all other hotels
- **Weekend occupancy (62.6%)** outperforms **weekday occupancy (55.8%)** — a 6.8% gap that directly supports dynamic pricing strategy
- **Third-party platforms** (Others + MakeMyTrip) drive 60%+ of total bookings at ₹690M and ₹337M respectively, exposing a direct channel dependency risk
- **AtliQ Blu** leads occupancy performance at **66.19%**, reflecting strong capacity utilization
- **Realization rate** holds at **70.14%** across all platforms, with Logtrip and Journey delivering the highest booking quality
- **₹298M lost to cancellations** — Elite rooms show the highest cancellation rate, signaling a need for policy revision

---

## 📂 Dataset Overview

| File | Type | Description |
|------|------|-------------|
| dim_hotels | Dimension | Hotel name, city, category |
| dim_rooms | Dimension | Room class and type |
| dim_date | Dimension | Date, week number, day type |
| fact_bookings | Fact | All booking transactions |
| fact_aggregated_bookings | Fact | Aggregated room availability and utilization |

- **Total Records:** 130,000+
- **Source:** Codebasics Resume Challenge
- **Format:** CSV files loaded into Power BI

---

## 🧮 Key Metrics Built

| Metric | Formula |
|--------|---------|
| **RevPAR** | Total Revenue / Total Available Rooms |
| **ADR** | Total Room Revenue / Number of Rooms Sold |
| **Occupancy %** | Occupied Rooms / Total Available Rooms |
| **Realization %** | Revenue Realized / Revenue Generated |
| **DSRN** | Daily Sellable Room Nights |
| **DBRN** | Daily Booked Room Nights |
| **DURN** | Daily Utilized Room Nights |

---

## 🛠️ Tools & Techniques

- **Power BI Desktop** - Report design and DAX development
- **Power Query** - Data cleaning, transformation, and normalization
- **DAX** - Calculated columns, measures, time intelligence functions
- **Data Modeling** - Snowflake schema with fact and dimension tables
- **Power BI Service** - Live deployment and stakeholder sharing

---


## 💡 Key Business Insights

- **Mumbai leads revenue**: ₹669M total  
- **AtliQ Exotica = highest revenue & booking share**  
- **Week 24 was the peak revenue period**  
- **High cancellation impact**: ₹298M lost due to cancellations  
- **Elite rooms = high demand but high cancellation %**  
- **OTA platforms (e.g., MakeMyTrip, LogTrip)** are strong revenue drivers  

---

## 🧠 Metrics & Measures

Over **20 custom DAX measures** including:

- ADR (Average Daily Rate)  
- RevPAR (Revenue Per Available Room)  
- Occupancy %  
- Cancellation Rate  
- Revenue Lost from Cancellations  
- Booking Share by Platform  
- Week-over-Week Revenue Trends  

---

### 👨🏻‍💼 How to Use This Dashboard
- **Whether you're a stakeholder, analyst, or manager, this dashboard is designed to make exploration intuitive.

Here’s how you can navigate and interact with it:

![Dashboard Walkthrough](https://github.com/Anand-Cinenkanolu/AtliQ-Hotels/blob/main/Files/Dashboard%20images/Dashboard.gif)


-----------

## Home / Landing Page
![Home Page](https://github.com/Anand-Cinenkanolu/AtliQ-Hotels/blob/main/Files/Dashboard%20images/Home%20Page.jpg)

## 📊 Dashboard Previews

### 🧭 Overview View

Quick snapshot of business health across all hotel properties:

A single-page health check for hotel revenue, occupancy, and booking performance across all properties.

- **KPI Cards** tracking Revenue, RevPAR, DSRN, Occupancy %, ADR, and Realization % with week-on-week change indicators
- **Luxury vs Business Revenue Split** showing which category drives more revenue across the portfolio
- **Weekly Metric Trend** for RevPAR, ADR, and Occupancy % to surface seasonal patterns and performance dips
- **Platform Efficiency View** comparing Realization % and ADR across booking channels to identify which OTAs bring volume and which bring value
- **Property Scorecard** ranking all hotels by Revenue, RevPAR, Occupancy %, ADR, Booking Nights, Cancellation %, and Guest Ratings

![Overview View](https://github.com/Anand-Cinenkanolu/AtliQ-Hotels/blob/main/Files/Dashboard%20images/OverView.jpg)

---

### 🏢 Executive View

Built for leadership-level analysis with drill-through capability across cities, properties, and room classes.

- **Decomposition Tree** breaking revenue hierarchically from City → Property → Room Class → Category, pinpointing exactly where revenue is won or lost
- **Booking Platform Treemap** visualizing channel contribution at a glance, with MakeMyTrip and Logtrip as top-volume platforms
- **City Revenue Ranking** comparing Mumbai, Bangalore, Hyderabad, and Delhi to identify key strategic markets
- **Weekday vs Weekend Occupancy** revealing a 6.8% gap that signals dynamic pricing opportunity
- **Monthly Revenue Trend** tracking performance curves across May, June, and July with custom visual for pattern recognition

![Executive View](https://github.com/Anand-Cinenkanolu/AtliQ-Hotels/blob/main/Files/Dashboard%20images/Executive%20View.jpg)

### Data Modeling

---

## 🧱 Data Model & Structure

📌 Snowflake schema implemented for clean filtering, accurate cross-table calculations, and faster query performance.

![Data Model](https://github.com/Anand-Cinenkanolu/AtliQ-Hotels/blob/main/Files/Dashboard%20images/Data%20Modeling.png)

### Dimension Tables

| Table | Key Fields |
|-------|-----------|
| `Dim_Date` | date, week, month, day_type |
| `Dim_Hotels` | property_id, city, property_name, category |
| `Dim_Rooms` | room_id, room_class |

### Fact Tables

| Table | Description |
|-------|-------------|
| `Fact_Bookings` | All booking transactions including revenue, room type, platform, and dates |
| `Fact_Aggregated` | Daily room capacity, sellable nights, and utilization rates |

---

## 🔍 Business Recommendations

- **Revise cancellation policy for Elite rooms** - highest demand but highest cancellation rate, directly impacting ₹298M in lost revenue
- **Invest in direct booking channels** - over 60% of bookings flow through third-party OTAs, reducing margin and increasing platform dependency
- **Implement dynamic weekend pricing** - 6.8% occupancy gap between weekends and weekdays is an untapped revenue lever
- **Focus retention strategy on Mumbai and AtliQ Exotica** — both are the highest revenue contributors and deserve priority resource allocation

---

## 🛠️ Tech Stack

| Area | Tools / Concepts |
|------|-----------------|
| BI Tool | Power BI Desktop + Power BI Service |
| Data Transformation | Power Query, ETL |
| Calculations | DAX, Time Intelligence Functions |
| Data Modeling | Snowflake Schema, Fact & Dimension Tables |
| UX Features | Conditional Formatting Theme Toggle, Slicers, Bookmarks, KPI Cards |
| Deployment | Published to Power BI Service for live stakeholder access |

---

## ✨ Special Features

- **Dark / Light Theme Toggle** - Built using native Power BI conditional formatting (no third-party plugin), switching the entire report between dark and light mode based on viewer preference
- **Live Deployment** - Report published to Power BI Service for interactive, shareable access without requiring desktop software
- **Role-Based Pages** - Overview page designed for operations teams, Executive View designed for leadership and revenue managers

---

## 🎓 What I Learned

- **Hospitality Domain Knowledge** Gained a solid understanding of revenue KPIs specific to the hotel industry, including how RevPAR, ADR, and realization rate interact to tell the full revenue story
- **Advanced DAX** - Built dynamic measures for week-over-week trends, day-type segmentation, and platform-level performance comparisons
- **Data Modeling** - Designed a snowflake schema that made cross-table filtering faster and more reliable across 130,000+ records
- **UI/UX Thinking** - Went beyond building a functional dashboard to designing one that works for different viewers, including a native dark-light theme toggle built without any external plugin
- **Stakeholder-First Design** - Structured the report into two distinct views so operations teams and executives each get the level of detail they actually need

---

## 📂 Project Structure

```
atliq-grand-hotels-analysis/
│
├── assets/
│   ├── Overview.png
│   └── Executive_View.png
│
├── data/
│   ├── dim_hotels.csv
│   ├── dim_rooms.csv
│   ├── dim_date.csv
│   ├── fact_bookings.csv
│   └── fact_aggregated_bookings.csv
│
├── AtliQ_Hotels_Dashboard.pbix
└── README.md
```

---

🔗 **Live Power BI Dashboard**: [View Report](https://app.powerbi.com/view?r=eyJrIjoiMjNmNGIwMDMtZDk5ZS00NDVhLTk3NzEtYWNiNDYyYjFiOWMyIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)


---

## 📣 Author Contact's 

**Anand Cinenkanolu**
Aspiring Data Analyst | Power BI Developer
For queries, collaboration opportunities, or feedback, feel free to reach out:

- 📧 [**Email**](anandcinenkanolu@gmail.com)
- 💼 [**LinkedIn**](https://www.linkedin.com/in/Anand-Cinenkanolu/)
- 🗂️ [**Portfolio**](https://codebasics.io/portfolio/Anand-Cinenkanolu)

💼 Always open to feedback, collaboration, or job opportunities in data analytics!

---

## 📄 License

This project is for educational purposes. Dataset sourced from [Codebasics Resume Challenge](https://codebasics.io/).
