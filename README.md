# Analysis and Insights in the Hospitality Domain

## Overview
This project is a **Power BI-based hospitality analytics dashboard** designed to generate business insights from hotel booking data.  
It focuses on analyzing booking behavior, hotel performance, room-category trends, and revenue realization across multiple hotel properties.

The solution walks through the full analytics workflow:
- **Data loading and transformation**
- **Data modeling**
- **DAX measure creation**
- **Dashboard and visual design**
- **Business insight generation**

---

## Problem Statement
The hospitality industry generates large volumes of booking and revenue data, but raw records alone do not help management make quick decisions.  
This project transforms booking-level and aggregated hotel data into an interactive dashboard that helps stakeholders monitor performance and identify improvement areas.

The dashboard can support decisions around:
- Revenue performance
- Booking trends
- Room-category demand
- Property-level comparisons
- Booking platform contribution
- Occupancy and capacity utilization
- Cancellation and no-show impact

---

## Dataset Information
The project uses **5 core CSV files**:

### 1. `dim_date`
Contains date-related attributes such as:
- Date
- Month-Year
- Week number
- Day type

### 2. `dim_hotels`
Contains hotel/property information:
- Property ID
- Property name
- Category
- City

### 3. `dim_rooms`
Contains room mapping:
- Room ID
- Room class

### 4. `fact_aggregated_bookings`
Contains aggregated booking information:
- Property ID
- Check-in date
- Room category
- Successful bookings
- Capacity

### 5. `fact_bookings`
Contains booking-level transaction details:
- Booking ID
- Property ID
- Booking date
- Check-in date
- Check-out date
- Number of guests
- Room category
- Booking platform
- Ratings given
- Booking status
- Revenue generated
- Revenue realized

---

## Business Context
The dataset represents hotel operations across multiple cities and properties, including:
- **Luxury** and **Business** hotel categories
- Cities such as **Delhi, Mumbai, Hyderabad, and Bangalore**
- Room classes such as **Standard, Elite, Premium, and Presidential**

The time period covered in the data is:
- **May 2022 to July 2022**

---

## Project Workflow

### Stage 1: Power Query / Data Preparation
The raw CSV files were loaded into Power BI and transformed using Power Query.

Key preparation work includes:
- Importing multiple CSV datasets
- Structuring dimension and fact tables
- Standardizing fields
- Rebuilding business-friendly date logic where required

A notable adjustment in the data-prep stage was the recreation of the `day_type` field based on business feedback.

### Stage 2: DAX Measures
The data model was extended with DAX measures to support performance analysis and KPI tracking.

Typical measures in this type of hospitality dashboard may include:
- Total bookings
- Successful bookings
- Occupancy %
- Cancellation %
- Revenue generated
- Revenue realized
- Average rating
- RevPAR / ADR-style hotel KPIs

### Stage 3: Dashboard & Visual Creation
The final dashboard is designed to present key insights in a clear and interactive format.

Possible visual sections include:
- Revenue trends over time
- Property-wise performance
- City-wise analysis
- Room-class contribution
- Booking platform breakdown
- Booking status analysis
- Ratings and customer experience trends

---

## Repository Structure

```bash
Analysis-And-Insights-in-Hospital-Domain/
│
├── Revenue-Insights-in-the-Hospitality-Domain.pbix
├── stage1_power_query.pbix
├── stage2_dax_measures.pbix
├── stage3_visual_creation_demo.pbix
│
├── dim_date.csv
├── dim_hotels.csv
├── dim_rooms.csv
├── fact_aggregated_bookings.csv
├── fact_bookings.csv
│
├── meta_data_hospitality.txt
├── stage1_power_query_doc.txt
├── metrics-list.xlsx
└── Mini Porject-ER and Visualizations.docx
