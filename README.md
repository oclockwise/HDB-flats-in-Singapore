# HDB Resale Data Explorer (Singapore)

## Overview
This project develops a relational database and web application to explore HDB resale flat prices in Singapore. It focuses on organizing structured data and enabling users to analyze housing trends through interactive queries.

---

## Objectives
- Design a normalized relational database for HDB resale data  
- Analyze housing trends such as pricing, lease impact, and transaction patterns  
- Build an interactive web application for data exploration  

---

## Dataset
- Source: data.gov.sg (HDB Resale Flat Prices)  
- Timeframe: January 2017 onwards  

**Key attributes:**
- Town, block, street  
- Flat type and floor area  
- Storey range and lease commencement year  
- Resale price  

---

## Database Design

### Entity Structure
The system is built using four main entities:
- Town  
- Block  
- Flat  
- Transaction  

These are connected using one-to-many relationships:
- One town → many blocks  
- One block → many flats  
- One flat → many transactions  

---

### Normalization
- Designed up to **Third Normal Form (3NF)** and **BCNF**  
- Reduces redundancy  
- Ensures data consistency and integrity  

---

## Implementation

### Database
- MySQL relational database  
- Data imported via staging table (CSV)  
- Structured tables with primary and foreign keys  

### Backend
- Node.js  
- Express.js  
- MySQL connection pool  

### Frontend
- EJS templates  
- Dynamic rendering of query results  

---

## Key Features (SQL Queries)

The application allows users to explore:

1. Top towns with highest resale prices (4-room flats)  
2. Price trends over time by flat type  
3. Relationship between lease year and resale price  
4. Impact of storey range on pricing  
5. Transaction counts by town and flat type  

---

## Key Insights
- Newer flats generally have higher resale prices  
- Higher floors tend to command higher prices  
- Pricing trends vary across flat types and years  
- Transaction activity differs by town  

---

## Web Application
- Interactive interface for querying housing data  
- Users can navigate multiple reports easily  
- Modular structure (routes, views, backend logic)  

---

## Tech Stack
- MySQL  
- Node.js  
- Express.js  
- EJS  
- SQL  

---

## How to Run

```bash
git clone <your-repo-link>
cd <your-project-folder>
npm install
node app.js
