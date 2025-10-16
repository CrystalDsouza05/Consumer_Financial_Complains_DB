# 🧭 Consumer Financial Complaints Analytics Dashboard  
### Onyx Data x ZoomCharts Mini Challenge | October 2025  

**Author:** Crystal Andrea Dsouza  

[Dashboard Link](https://app.powerbi.com/view?r=eyJrIjoiMzk2YTA5YWMtZGRmMi00ZjA0LWI1YWYtZmIyODJkZTdlMDU0IiwidCI6IjQ2NTRiNmYxLTBlNDctNDU3OS1hOGExLTAyZmU5ZDk0M2M3YiIsImMiOjl9)
---

## 📖 Project Overview  
This project was created for the **Onyx Data x ZoomCharts Mini Challenge (October 2025)**.  

The challenge placed participants in the role of a **Data Analyst at the Consumer Financial Protection Bureau (CFPB)**—a U.S. government agency that ensures transparency and fairness in the financial sector.  

The CFPB collects consumer complaints related to financial products and services, tracking each complaint from submission through the company’s response.  
The goal of this dashboard is to analyze complaint patterns, response efficiency, and company performance to identify trends and insights valuable to both regulators and consumers.

---

## 🧩 Dataset Overview  
The dataset comprises two main tables:  

- **Complaints (Fact Table):** Complaint ID, Product, Sub-product, Issue, State, Date Submitted, Date Received, Response Time (Days), Timely Response indicator, and related fields.  
- **Company (Dimension Table):** Company ID, Market Share %, Reputation Score, Enforcement History, Company Size Tier, Complaint Count, and Timely Response Rate.  

A **Date Table** was created in Power BI using DAX to enable monthly, quarterly, and yearly trend analysis.

---

## 📊 Dashboard Design  

The Power BI report consists of **two interactive pages**, designed using **ZoomCharts PRO visuals** for dynamic drill-downs, combined with selected Matrix visuals for detail-level insights.

---

### 📍 Page 1 – Complaint Overview  
Provides an overall picture of complaint distribution, submission channels, and geographical trends.

**Visuals Used**  
- **ZoomCharts Donut Chart (Product → Sub-Product → Issue → Sub-Issue):**  
  Displays complaints across product categories and subcategories.  
- **ZoomCharts Timeline Chart:**  
  Shows complaint trends over time and highlights changes in volume or response patterns.  
- **ZoomCharts Combo Column Chart (Submission Channel):**  
  Compares the proportion of complaints by submission mode such as Web, Referral, or Phone.  
- **ZoomCharts Map:**  
  Shows complaint density and distribution across U.S. states and census regions.  

**KPI Cards**  
- Average Complaints per Company  
- Average Response Time (Days)  
- Company Count  
- Total Complaint Count  
- Complaint YoY Growth %  
- Timely Response %  
- Average Market Share %

---

### 🏢 Page 2 – Company Performance Insights  
Focuses on evaluating company performance, responsiveness, and reputation relative to market share.

**Visuals Used**  
- **ZoomCharts Scatter Chart:**  
  - **X-axis:** Market Share %  
  - **Y-axis:** Reputation Score  
  - **Bubble Color:** Company Size Tier  
  Each point represents a company, allowing analysis of the relationship between market size and reputation.  

- **ZoomCharts Donut Chart:**  
  Groups companies based on reputation score or size tier, illustrating company distribution by performance level.  

- **ZoomCharts Combo Bar Chart:**  
  Compares companies’ average response time and timely response rate side by side for performance benchmarking.  

- **Matrix Visuals (3):**  
  1. Provide detailed company-level metrics such as Complaint Count, Market Share %, Avg Response Time, Timely Response %, and Enforcement History.
  2. Complaint Status Tracker
  3. Company's public response regarding complaints. 

---

## 🎛️ Interactive Filter Pane  
A **custom filter pane** is placed on the right side of the dashboard for user flexibility.  

**Filters Available**  
- Date Range  
- Product / Sub-Product  
- Company Name  

**Dynamic Date Range Card**  
Displays the currently selected period using DAX:  
```DAX
Date Range =
": " &
FORMAT(MIN('DateTable'[Date]), "dd MMM yyyy") &
" - " &
FORMAT(MAX('DateTable'[Date]), "dd MMM yyyy")
```

---

## 🧮 Key DAX Measures  
- Complaint Count
- Company Count
- Average Response Time (Days)  
- Timely Response Rate (%)  
- Average Complaints per Company  
- Complaint YoY Growth %  
- Average Market Share (%)  
- Complaints per 1% Market Share  
- Dynamic Date Range Card  

---

## 🧠 Summary  
This dashboard enables users to explore complaint behavior across products, channels, and regions while analyzing company-level response efficiency and reputation.  
Interactive drill-downs and filter options make it easy to identify key performance patterns and areas for improvement in complaint management.

---

## 🛠️ Tools & Features Used  
- **Power BI Desktop**  
- **ZoomCharts Drill Down PRO Visuals:** Donut, Timeline, Combo, Map, Scatter  
- **Matrix Visuals** for detailed company-level insights  
- **Custom Filter Pane** for interactive exploration  
- **DAX** for KPIs and dynamic calculations
- **Figma & PowerPoint** for dashboard design.  

---

## Dashboard Images
Page 1: Complaints Overview
<img width="1761" height="988" alt="image" src="https://github.com/user-attachments/assets/440a214c-4fcb-4620-8b2c-6895e326bc9c" />

Page 2: Company Performance Insights
<img width="1755" height="985" alt="image" src="https://github.com/user-attachments/assets/e4dc1722-09fe-4afe-a201-31acbc19e9b8" />

Data Model: 
<img width="1611" height="714" alt="image" src="https://github.com/user-attachments/assets/83027534-a712-45b0-a6f4-c374d60e9f94" />


Filter Pane:

<img width="418" height="845" alt="image" src="https://github.com/user-attachments/assets/d0c790c2-184e-4def-8b04-286821ca143c" />
