# LOAN-DEFAULT-OVERVIEW
 ## Project Title / Headline
# 🏦 Loan Risk & Portfolio Analytics Dashboard
Empowering banking officials to evaluate applicant reliability, track key lending KPIs, and optimize loan approval decisions using Power BI.

## Short Description / Purpose
The loan default dataset contains information about borrowers who have applied for loans. Each record represents a borrower's details, including financial status, loan characteristics, and repayment behaviour .The purpose of the analysis is to assist bank officials in determining loan approval decisions by identifying patterns and factors that lead to defaults.

## 🛠️ Tech Stack & Tools Used

* 🗄️ **SQL Server** – Source relational database used to store and manage raw loan and borrower records.
* ☁️ **Power BI Service (Dataflows)** – Cloud ETL pipeline used to ingest data from SQL Server, configure **Scheduled Refresh**, and optimize performance using **Incremental Refresh**.
* 📊 **Power BI Desktop** – Core reporting platform used to build interactive visuals, including Donut Charts, Clustered Column Charts, Line Charts, and AI-driven **Decomposition Trees**.
* 📂 **Power Query Editor** – Data profiling and transformation layer used to enforce proper data types, handle missing values, and clean columns prior to modeling.
* 🧠 **DAX (Data Analysis Expressions)** – Used to build dynamic calculations, statistical aggregations, conditional logic, and time-intelligence metrics (`CALCULATE`, `SUMX`, `AVERAGEX`, `MEDIANX`, `FILTER`, `ALLEXCEPT`, `DIVIDE`, `SWITCH`).
* ✅ **Data Validation & QA** – End-to-end verification of DAX measures against source figures across demographic segments and chart visuals.

 ## Data Source

**Source:** Loan & Credit Risk Dataset (https://drive.google.com/file/d/1LxdlX7Yh6IrifvobCMpdk9i0jH-raSqF/view) & Microsoft SQL Server.

Data on **~250,000 loan records** stored in SQL Server and ingested via Power BI Dataflows, including details on loan amounts, purposes, origination years, and default statuses, alongside borrower demographics (age groups, marital status, education, dependents) and financial profiles (income, employment type, credit score categories).

## 📋 Dataset Features & Highlights

* Borrower Information: ~250,000 unique applicant records providing a comprehensive view of the borrower pool across 6 years (2013–2018).
* Financial Status: Annual income levels (~$82K average) and 4 credit score categories (Low, Very Low, Medium, High) used to evaluate repayment capacity.
* Loan Characteristics: Detailed loan amounts ($32.58bn total; ~$127.5K median), interest rates, and terms essential for assessing credit exposure.
* Repayment Behaviour: Historical loan performance and default statuses (Default vs. Non-Default, averaging ~11.6% annual default rate) to evaluate borrower reliability.
* Demographic Factors: 4 age groups (Teens, Adults, Middle-Age Adults, Senior Citizens), 4 education levels (High School to PhD), 4 employment types, 3 marital statuses, dependents, and existing mortgage indicators.
* Loan Purpose: Categorization across 5 borrowing intents (Home, Business, Education, Auto, Other) to uncover purpose-specific risk trends.
* Consigner Information: Binary indicators showing whether an applicant has a consigner as an added layer of loan security.

## Key Questions & Project Objectives

* 1. What is the primary goal of analyzing loan default data?
  To uncover hidden patterns behind loan defaults across ~250,000 records, enabling banks to make data-driven decisions about future lending practices and portfolio risk management.

* 2. Which borrower characteristics correlate with higher default rates?
  Analyzing demographics and financial history—including employment type (Unemployed at 3.39% vs. Full-time at 2.36%), credit score tiers, education level, and marital status—pinpoints which segments carry elevated default risk.

* 3. How can the bank use this data to minimize risk?
  By isolating the attributes of high-risk borrowers (such as Low credit score applicants holding high median loans of $128,397), banking officials can tighten credit policies, adjust loan limits, and target more reliable segments.

* 4. What insights can be drawn from borrower repayment behaviour and historical trends?
  Tracking annual default fluctuations (11.50%–11.75%) and Year-over-Year (YoY) shifts reveals cyclical risk patterns, helping banks structure better loan terms and interest rates during expansion or downturn cycles.

* 5. What are the implications of having a cosigner, mortgage, or dependents on loan performance?
  Evaluating household obligations (such as Middle-Age Adults carrying $3.1bn across mortgage and dependent segments) and cosigner security adds critical context to a borrower's true repayment capacity.
## 🎯 Business Problem

Financial institutions face significant credit risk when approving loan applications across a $32.58bn portfolio without clear visibility into how borrower demographics, income stability, and loan characteristics influence repayment behaviour. With annual default rates fluctuating between 11.50% and 11.75% (2013–2018), high default exposure directly impacts portfolio profitability, making it essential to identify high-risk borrower segments early in the underwriting process.

---

## 🚀 Goal of the Dashboard

The primary goal of this dashboard is to empower banking officials and risk analysts to:
* Monitor overall loan portfolio volume ($32.58bn), median/average loan sizes ($127K–$128K), and historical default rates (11.50%–11.75%).
* Identify key risk drivers across 4 employment types, 4 credit score tiers, 4 age groups, and 5 loan purposes.
* Track Year-over-Year (YoY) and Year-to-Date (YTD) lending trends across 6 years (2013–2018) to support data-driven loan approval and risk mitigation decisions.

---

## 📊 Walkthrough of Key Visuals

* Portfolio Breakdown & Loan Purpose (Area & Stepped Area Charts): Compares total loan volume across 5 purposes—led by Home ($6,545M) and Business ($6,522M)—alongside average income ($82,272–$82,890) and default rates (2.36%–3.39%) by employment type.
* Demographic & Credit Score Distribution (Donut, Clustered Column & Area Charts): Visualizes high-credit average loans by age group and marital status (peaking at $128.75K for Single Adults), adult loan volume by credit tier ($4.6bn in Medium vs. $1.1bn in Low), and Middle-Age Adult loans ($3.1bn each) by mortgage/dependent status.
* Historical Risk & YoY Trends (Area & Ribbon Charts): Tracks annual default rates (2013–2018), YoY loan growth (-1.53% in 2014 to +1.73% in 2018), YoY default shifts (-2.8% in 2017 to +2.7% in 2015), and YTD loan volume across credit bins ($0.17bn–$0.67bn).
* Root-Cause Analysis (Decomposition Tree): Breaks down the $32.58bn total loan amount dynamically across income brackets (High: $21.73bn, Low: $3.63bn) and employment types (Full-time: $5.44bn, Part-time: $5.44bn, Self-employed: $5.43bn) using SWITCH DAX measures.

---

## 💡 Business Impact & Insights

* Targeted Risk Mitigation: Pinpoints that Unemployed borrowers carry a 3.39% default rate (compared to 2.36% for Full-time workers) and Low credit score applicants hold the highest median loan size ($128,397), enabling stricter credit policies for high-risk tiers.
* Optimized Lending Strategy: Highlights stable borrower segments—such as Full-time earners ($82,890 average income) and High/Medium credit adult borrowers ($9.1bn combined volume)—where banks can safely expand loan approvals.
* Automated Reporting Efficiency: Eliminates manual reporting delays across ~250,000+ records by leveraging SQL Server, Power BI Dataflows, and Incremental Refresh for scalable, up-to-date portfolio monitoring.

---
## 📸 Dashboard Walkthrough & Screenshots

### 1. Loan Default & Overview
![Loan Default & Overview](images/01_loan_default_overview.png)

---

