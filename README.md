# Hospital-Operations-and-Financial-Performance-Analytics
The Hospital Performance Analytics Dashboard is an interactive Power BI solution developed to provide a comprehensive view of hospital operations, patient care, workforce performance, ward utilization, and financial performance. The dashboard transforms raw operational data into actionable insights that help hospital management monitor key performance indicators (KPIs), improve patient care, and make informed, data-driven decisions.

## Dataset

The project uses a relational dataset consisting of five worksheets:

1. **Admissions:** Contains patient admission records.
2. **Billing:** Contains hospital financial transactions.
3. **Doctors:** Contains doctor information.
4. **Patients:** Contains patient demographic information.
5. **Wards:** Contains ward information.

---

## Problem Statement

Hospital management requires timely and accurate information to monitor patient admissions, evaluate doctor performance, optimize ward utilization, and improve financial management.

However, operational data is often spread across multiple tables, making it difficult to gain a complete view of hospital performance.

The objective of this project is to consolidate the available data into an interactive dashboard that provides meaningful insights for operational and strategic decision-making.

---

## Business Questions

**Executive Summary**

- How many patients, admissions and doctors does the hospital have?
- How much revenue has the hospital generated?
- What are the monthly admission and revenue trends?
- Which admission types are most common?
- Which doctors manage the highest number of admissions?
- What is the current payment status distribution?

**Patient Analysis**

- What is the gender distribution of patients?
- Which age groups visit the hospital most?
- Which states contribute the highest number of patients?
- What insurance plans are most common?
- How satisfied are patients?
- What is the readmission rate?

**Doctor Analysis**

- Which specializations handle the highest patient volume?
- Which doctors have the highest number of admissions?
- How experienced is the medical workforce?
- How does patient satisfaction vary across doctors?
- What is the average length of stay by doctor?

**Billing & Revenue Analysis**

- How much revenue has been generated?
- How much money has been collected?
- What is the outstanding balance?
- What payment methods are most used?
- How do discounts change over time?
- Which bills have the highest outstanding balances?

**Ward Performance**

- Which wards receive the most admissions?
- Which wards generate the highest revenue?
- Which wards have the highest patient satisfaction?
- What is the average length of stay by ward?
- How effectively are ward resources utilized?

---

## Tools and Methodology

### Tools

- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- Data Modeling

### Methodology

**Step 1 — Data Import**

- Imported all five worksheets into Power BI.
- Verified column names and data types.

**Step 2 — Data Cleaning**

Performed data cleaning using Power Query by:

- Checking for missing values.
- Identifying duplicate records.
- Correcting data types.
- Standardizing date fields.
- Validating primary and foreign keys.
- Identifying orphan billing records.
- Removing billing records with Admission IDs that had no matching admission record to improve data integrity and eliminate blank categories in visuals.

**Step 3 — Data Modeling**

Built relationships between the tables using a star schema approach:

- Patients → Admissions
- Doctors → Admissions
- Wards → Admissions
- Admissions → Billing

This model ensured efficient filtering and prevented ambiguous relationships.

**Step 4 — DAX Measures**

Created measures for:

- Total Patients
- Total Admissions
- Total Doctors
- Total Revenue
- Total Collections
- Outstanding Balance
- Average Bill Amount
- Average Length of Stay
- Average Satisfaction Score
- Readmission Rate
- Payment Completion Rate
- Total Discount
- Active Doctors
- Inactive Doctors
- Revenue per Bed

**Step 5 — Dashboard Development**

Designed five interactive report pages:

- **Executive Summary:** Provides a high-level overview of hospital performance.
- **Patient Analysis:** Analyzes demographics, admissions, satisfaction and insurance coverage.
- **Doctor Analysis:** Evaluates doctor workload, specialization, experience and patient outcomes.
- **Billing & Revenue Analysis:** Monitors revenue, collections, outstanding balances, discounts and payment methods.
- **Ward Performance:** Assesses ward utilization, revenue generation, patient satisfaction and operational efficiency.

**Step 6 — Dashboard Formatting**

Applied a healthcare-themed design by:

- Adding KPI cards with icons.
- Using consistent fonts and spacing.
- Applying slicers for interactive filtering.
- Formatting currency and percentage values appropriately.

---

## Key Insights

#### **Executive Summary**

- The hospital recorded 200 unique patients across 485 admissions, indicating that many patients had multiple hospital visits.
- The hospital generated approximately ₦236.01 million in total revenue.
- Collections declined over the reporting period, suggesting slower payment recovery despite continued service delivery.
- Elective admissions accounted for the largest share (54.64%), followed by Emergency (35.05%) and Out-Patient (10.31%).
- 61.24% of bills were fully paid, while 38.76% were either partially paid or unpaid, highlighting opportunities to improve collections.
- Dr. Musa Garba managed the highest number of admissions (45), followed closely by several other doctors with over 40 admissions.

#### Patient Analysis

- The patient population was almost evenly split by gender, with 102 males (51%) and 98 females (49%).
- Patients aged 36–50 years represented the largest age group, indicating higher healthcare utilization among middle-aged adults.
- Ibadan contributed the highest number of patients, followed by Kano and Sokoto.
- HMO insurance was the most common payment coverage, suggesting that insured patients formed a significant portion of hospital visits.
- Average patient satisfaction remained relatively consistent across gender and age groups, with scores around 3.0–3.6, indicating moderate patient satisfaction.

#### Doctor Analysis

- The hospital employed 20 active doctors with no inactive staff during the reporting period.
- Admissions were distributed across multiple specializations, reflecting a diverse range of healthcare services.
- Dr. Musa Garba recorded the highest patient workload with 45 admissions.
- The largest proportion of doctors had 6–10 years of experience, providing a balanced mix of experience within the workforce.
- Some doctors recorded readmission rates above 70%, which may warrant further investigation into patient follow-up and treatment outcomes.

#### Ward Performance Analysis

- Urology and Dermatology recorded the highest admission volumes among all wards.
- Dermatology generated the highest revenue (approximately ₦29 million), making it the hospital's top-performing ward financially.
- Average length of stay varied across wards, ranging from approximately 9 to 12 days, indicating differences in treatment complexity.
- Patient satisfaction remained fairly consistent across wards, although Paediatrics recorded comparatively lower satisfaction scores.
- Bed capacity varied between wards, which can help management assess whether capacity aligns with patient demand.

#### Billing & Revenue Analysis

- Total revenue reached approximately ₦236.01 million, while total collections amounted to approximately ₦197.43 million.
- The hospital has an outstanding balance of approximately ₦38.58 million, representing revenue yet to be collected.
- Partial-payment accounts contributed the largest share of outstanding balances, followed by unpaid bills.
- NHIS generated the highest revenue among payment methods, followed by Cash and HMO.
- Revenue from Elective admissions significantly exceeded Emergency and Out-Patient services.
- The average discount ranged between 3% and 4% across the reporting period, indicating relatively stable discounting practices.

- ## Challenges and Solutions

**Challenge:** Ambiguous relationships between Doctors and Wards in the data model.
**Solution:** Implemented a star schema and used DAX where appropriate instead of introducing ambiguous relationships.
**Challenge:** Orphan billing records created blank categories in visuals.
**Solution:** Identified unmatched Admission IDs and removed them to ensure accurate reporting.

---

## Recommendations

1. Monitor outstanding balances regularly and strengthen payment follow-up procedures.
2. Use admission trends to improve staffing and resource planning during high-demand periods.
3. Review patient satisfaction scores to identify opportunities for service improvement.
4. Balance workloads across doctors and specializations where necessary.
5. Optimize bed allocation and ward capacity based on admission trends.
6. Introduce automated scheduling and resource planning to improve ward and staff utilization.
7. Implement routine data quality checks to prevent orphan records and maintain reliable reporting.

---

## Conclusion

By integrating operational, clinical and financial data into a single dashboard, stakeholders can monitor performance, identify trends and make informed decisions that improve patient care, operational efficiency and financial sustainability.
