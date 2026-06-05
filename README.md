<img width="103" height="67" alt="image" src="https://github.com/user-attachments/assets/74ecf65c-c8f2-4999-9599-e3a5b941ca74" /># Carbon-Capture
This project analyzes CO₂ data across the Bangchak refinery in Bangkok from September 2025 to March 2026 based on pilot scale.  The dataset, sourced from PLC machine(already uploaded in repositories), was cleaned and merged into a single table to track key performance indicators like CO₂ Capture, CO₂ Recovery, CO₂ Capture Efficiency, and CO₂ Recovery Efficiency. The standard mandates that CO₂ Capture Efficiency and CO₂ Recovery Efficiency should be 99%+ and 95%+ respectively. This dashboard helps assess performance across half years.

Insights and recommendations are provided on the following key areas:

Category 1: CO₂ Capture

Category 2: CO₂ Recovery

Category 3: CO₂ Capture Efficiency 

Category 4: CO₂ Recovery Efficiency

The dataset was cleaned, aggregated, and analyzed in Excel, and Power Query before being visualized in Power BI.

<a href="Carbon-Capture Dashboard.pdf" target="_blank" class="btn btn-secondary">View Dashboard</a>

# Dataset Description
The data model comprises three tables capturing NHS A&E performance across time, geography, providers, and metrics, totaling 151,270 records

## Tables
* AE_Activity_Fact: Main fact table with A&E activity data (categories, timeframes, date, provider, region, value).
* DateTable: Date dimension for filtering and time analysis (date, month, quarter, year).
* Trends Selector: Helper table for trend slicers (selector name, field mapping, order).
  
### Calculated Measures
* Emergency Admission Measures: Calculated columns/measures for emergency admissions.
* DAX Measures: Pre-calculated KPIs (e.g., % Seen after 4 hours).
  
![image](https://github.com/user-attachments/assets/b2450f01-f074-4e75-a70e-275de9d03bd4)

# Executive Summary
## Overview of Findings
Between 2021 and 2025, the NHS experienced a substantial increase in A&E attendances, but performance against the 4-hour target consistently fell short of the 95% standard. Emergency admissions rose sharply, and some providers showed significantly higher volumes and delays.

* Total A&E attendances rose from 22.8M in 2021 to 27.4M in 2024.
* Only 69.14% of patients were seen within 4 hours as of 2024, well below the 95% target.
* Emergency admissions surged to 25M from 2021 to January 2025.
* Major A&E departments are responsible for the majority of delays.
# Insights Deep Dive
## Category 1: Total A&E Attendances
* Attendance increased 20% from 22.8M in 2021 to 27.4M in 2024.
* Major trusts like Barts Health NHS Trust and Manchester University NHS Foundation Trust recorded over 2M attendances each.
* The rise in attendance reflects increased pressure on emergency services post-pandemic.

![image](https://github.com/user-attachments/assets/d780664f-0fbf-4ed9-b703-98c52e71ff5a)

## Category 2: 4-Hour Standard Compliance
* The 4-hour performance rate dropped below 70%, far short of the 95% NHS benchmark.
* A&E departments managed to see only 69.14% of patients within 4 hours in 2024.
* Patients waiting more than 4 hours rose to over 18M annually.
* Minor Injury Units performed better, while Major A&Es saw significant backlogs.

![image](https://github.com/user-attachments/assets/d72c7c2f-f368-43f4-bdaa-d0199444ff3d)

## Category 3: Emergency Admissions
* Emergency admissions climbed from 6M in 2021 to 6.6M in 2024.
* Breakdown shows >4h and >12h delays contributing significantly to strain.
* University Hospitals Birmingham had the highest emergency admissions volume (~0.74M).

![image](https://github.com/user-attachments/assets/818cd3e8-d327-4d71-b4c8-e1a4122a7161)

## Category 4: Provider-Level and Departmental Trends
* Top 10 providers accounted for over 15M attendances cumulatively.
* Major A&E departments showed the worst performance in meeting the 4-hour rule.
* Only 2.53% of attendances were seen in single-specialty departments within 4 hours.
* These trusts are not underperforming in the traditional sense but are operating under disproportionate pressure with limited resources.
* The gap between patients seen in <4h vs >4h widened steadily from 2021 to 2024.
* High-volume providers like Barts Health and Manchester University NHS Trust see over 2 million attendances annually, which puts immense strain on staff and physical infrastructure.
* The performance gap is systemic, rooted in national workforce shortages, seasonal surges, and post-pandemic demand increases.

![image](https://github.com/user-attachments/assets/9b4caa6e-9735-4407-9907-88cf56ec0a52)

# Recommendations
* Capacity-Driven Support: Instead of penalizing trusts with low 4-hour compliance, identify them as high-pressure sites and prioritize them for additional staffing, funding, and infrastructure support.
* Resource Scaling: Invest in scalable A&E surge capacity, including temporary staff pools and modular treatment spaces, particularly for trusts facing sustained high volumes.
* Workforce Strategy: Expand recruitment, retention, and upskilling initiatives to alleviate shortages in critical roles (A&E doctors, nurses, porters).
* Intelligent Triage & Flow Management: Deploy digital triage tools and discharge planning systems to reduce bottlenecks and free up beds faster.
* Public Health & Diversion Initiatives: Strengthen urgent treatment centres (UTCs) and 111 services to redirect non-critical cases before they reach A&E.

# Assumptions
* Data completeness from NHS England is assumed post-cleaning.
* All KPIs calculated based on provided categories without imputation.
* Data filtered for completeness across Jan 2021–Jan 2025 only.
* Departmental breakdowns used NHS classification of major/minor/specialty A&Es.
