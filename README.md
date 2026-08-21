# 🚗 Tata Motors Integrated Operations Analysis

## 📌 Project Overview

**Tata Motors Integrated Operations Analysis** is an end-to-end **Manufacturing & Supply Chain Analytics** project designed to analyze logistics operations, shipment performance, payment activity, customer behavior, and operational efficiency.

The project integrates **SQL ETL, Excel Exploratory Data Analysis, Power BI dashboards, and GenAI-powered n8n automation** into a unified analytics ecosystem.

The solution demonstrates how data engineering, business intelligence, and generative AI can be combined to transform operational data into actionable business insights.

---

## 🎯 Business Problem

Large-scale automotive manufacturing and logistics operations generate data across multiple business functions, including:

* 🚚 Shipment Tracking
* 🏢 Dealer Distribution
* 👥 Customer Management
* 💳 Payment Processing
* 👨‍💼 Employee Operations
* 📦 Supply Chain Management
* 📊 Operational Reporting

Fragmented datasets and manual reporting can make it difficult for operations teams to monitor performance, identify bottlenecks, and respond quickly to operational exceptions.

### Objective

Build a centralized analytics solution that enables:

* Operational visibility
* Logistics performance monitoring
* Customer and payment analysis
* Data-driven decision-making
* Automated operational reporting
* AI-powered exception analysis

---

# 🏗️ Project Objectives

## 1. SQL ETL Pipeline

* Designed a relational database schema for operational data
* Loaded datasets into PostgreSQL
* Performed data cleaning and transformation
* Created analytical datasets using SQL
* Developed queries for logistics, payment, customer, and employee analysis

## 2. Excel Exploratory Data Analysis

Performed exploratory analysis across:

* Customer Analytics
* Shipment Analysis
* Payment Analysis
* Logistics Performance
* Membership Analysis
* Revenue Analysis

## 3. Power BI Dashboard

Developed interactive dashboards for:

* Customer Insights
* Shipment Operations
* Financial Health
* Logistics Performance
* Revenue Contribution

## 4. GenAI + n8n Automation

Built AI-powered workflows for:

* Daily logistics summaries
* Shipment exception analysis
* Payment issue explanations
* Operational reporting automation

---

# 🛠️ Technology Stack

| Technology             | Purpose                                      |
| ---------------------- | -------------------------------------------- |
| **PostgreSQL**         | Database Management & Data Storage           |
| **SQL**                | ETL, Data Cleaning & Business Analysis       |
| **Microsoft Excel**    | Exploratory Data Analysis                    |
| **Power BI**           | Interactive Business Intelligence Dashboards |
| **n8n**                | Workflow Automation                          |
| **Groq Llama 3.3 70B** | Generative AI Analysis                       |
| **Postman**            | API Testing                                  |

---

# 🗄️ Database Architecture

The project integrates **seven operational datasets**:

1. **Customer**
2. **Membership**
3. **Employee Details**
4. **Shipment Details**
5. **Payment Details**
6. **Shipment Status**
7. **Employee Shipment Mapping**

### Data Flow

```text
Operational Datasets
        ↓
    PostgreSQL
        ↓
   SQL ETL Pipeline
        ↓
 Analytical Datasets
        ↓
 ┌───────────────┬────────────────┐
 ↓               ↓                ↓
Excel          Power BI        n8n + GenAI
EDA            Dashboards      Automation
 ↓               ↓                ↓
Business       Visual          Automated
Insights       Insights        Reporting
```

---

# 📊 Key Business Insights

## 🚚 Logistics Performance

* Domestic shipments have an average delivery time of **117.98 days**.
* International shipments have an average delivery time of **96.26 days**.
* Regional bottlenecks were identified within domestic distribution networks.
* Shipment performance analysis highlights opportunities for logistics optimization.

## 💳 Payment Analytics

* **Cash on Delivery (COD)** transactions average approximately **₹49,578.86**.
* **Card payments** average approximately **₹45,039.89**.
* The analysis indicates significant dependency on COD-based payment workflows.
* Payment monitoring can help identify recovery and collection opportunities.

## 📦 Cargo Operations

* More than **60% of shipments are classified as Heavy Cargo**.
* High heavy-cargo volume increases transportation and warehousing complexity.
* Cargo classification can support better logistics planning and resource allocation.

## 👥 Customer Analytics

* Retail customers represent approximately **39% of the customer base**.
* Membership analysis identifies expired memberships and potential customer-retention opportunities.
* Customer segmentation enables better understanding of revenue contribution and customer behavior.

---

# 📈 Power BI Dashboard Modules

## 👥 Customer Insights Dashboard

Key analysis includes:

* Customer Segmentation
* Customer Type Distribution
* Membership Analysis
* Membership Status
* Revenue Contribution
* Customer-Level Performance

---

## 🚚 Shipment Operations Dashboard

Key analysis includes:

* Domestic vs International Shipments
* Delivery Performance
* Shipment Status
* Service Type Analysis
* Cargo Classification
* Logistics Performance
* Shipment Trends

---

## 💰 Financial Health Dashboard

Key analysis includes:

* Revenue Trends
* Payment Method Analysis
* Payment Recovery
* Customer Revenue Contribution
* Payment Performance
* Financial KPIs

---

# 🤖 GenAI + n8n Automation

## Automation 1 — Daily Logistics Operations Summary

### Business Problem

Operations managers cannot continuously monitor dashboards throughout the day. Important changes in shipment and payment metrics may therefore go unnoticed.

### Solution

An automated workflow retrieves operational KPIs, sends them to a Generative AI model, and generates a concise business-friendly logistics summary.

### Workflow

```text
        Cron Trigger
             ↓
    SQL Metrics Extraction
             ↓
       Operational KPIs
             ↓
      GenAI Analysis
             ↓
    Summary Generation
             ↓
       Email Report
```

### Output

The generated report can summarize:

* Shipment performance
* Delivery delays
* Payment trends
* Operational exceptions
* Key business metrics
* Areas requiring attention

---

# 🤖 Automation 2 — Shipment & Payment Issue Explanation System

### Business Problem

Operations teams may require immediate explanations for shipment delays, payment issues, or employee-related operational exceptions.

Manually investigating multiple tables can increase response time.

### Solution

An AI-powered n8n workflow retrieves relevant operational records and generates a business-friendly explanation of the identified issue.

### Workflow

```text
       Webhook Input
             ↓
      Shipment Lookup
             ↓
     SQL Data Retrieval
             ↓
 Shipment + Payment Data
             ↓
       GenAI Reasoning
             ↓
 Operational Explanation
```

### Example Use Cases

* Explain why a shipment was delayed
* Identify payment-related issues
* Retrieve shipment details
* Analyze employee shipment assignments
* Generate operational recommendations

---

# 🔄 End-to-End Architecture

```text
                    ┌─────────────────────┐
                    │ Operational Data    │
                    │ Customer            │
                    │ Shipment            │
                    │ Payment             │
                    │ Employee            │
                    │ Membership          │
                    └──────────┬──────────┘
                               ↓
                    ┌─────────────────────┐
                    │    PostgreSQL       │
                    │    SQL ETL          │
                    └──────────┬──────────┘
                               ↓
                    ┌─────────────────────┐
                    │ Analytical Dataset  │
                    └──────────┬──────────┘
                               ↓
              ┌────────────────┼────────────────┐
              ↓                ↓                ↓
       ┌─────────────┐  ┌─────────────┐  ┌─────────────┐
       │    Excel    │  │  Power BI   │  │     n8n     │
       │     EDA     │  │ Dashboards  │  │ Automation  │
       └──────┬──────┘  └──────┬──────┘  └──────┬──────┘
              ↓                ↓                ↓
       ┌─────────────────────────────────────────────┐
       │          Business Intelligence              │
       │          & Operational Insights             │
       └──────────────────────┬──────────────────────┘
                              ↓
                       ┌──────────────┐
                       │ GenAI Layer  │
                       │ Groq Llama   │
                       └──────┬───────┘
                              ↓
                    Automated Reporting
                    & Issue Explanation
```

---

# 📊 Estimated Business Impact

| Initiative                        | Expected Improvement |
| --------------------------------- | -------------------: |
| Predictive Maintenance            |                   8% |
| Defect Reduction                  |                   5% |
| Inventory Optimization            |                   4% |
| EV Expansion                      |                   6% |
| Supply Chain Optimization         |                   3% |
| **Overall Estimated Improvement** |              **26%** |

> **Note:** These figures represent estimated/projected business impact rather than measured results from a production deployment.

---

# 💡 Key Project Outcomes

This project demonstrates the ability to:

* Build relational databases using PostgreSQL
* Develop SQL-based ETL pipelines
* Perform exploratory data analysis using Excel
* Build interactive Power BI dashboards
* Analyze logistics and supply chain performance
* Perform customer and payment analytics
* Automate operational workflows using n8n
* Integrate Generative AI into business processes
* Design AI-powered operational reporting systems
* Convert raw operational data into actionable business insights

---

# 🎯 Project Outcome

The project demonstrates how **SQL ETL, Excel Analytics, Power BI, and GenAI Automation** can be integrated into a unified manufacturing analytics ecosystem.

The solution provides a framework for improving:

* 📊 Operational visibility
* 🚚 Logistics monitoring
* 💰 Payment analysis
* 👥 Customer intelligence
* 📦 Supply chain efficiency
* 🤖 Reporting automation
* ⚡ Data-driven decision-making

---

# 👩‍💻 Author

**Neha Lahane**

### Skills Demonstrated

`SQL` `PostgreSQL` `Excel` `Power BI` `Data Analytics` `ETL` `Business Intelligence` `n8n` `Generative AI` `Llama 3.3` `API Integration`

---
