# Carbon-Capture
This project analyzes CO₂ data across the Bangchak refinery in Bangkok from September 2025 to March 2026 based on pilot scale.  The dataset, sourced from PLC machine(already uploaded in repositories), was cleaned and merged into a single table to track key performance indicators like CO₂ Capture, CO₂ Recovery, CO₂ Capture Efficiency, and CO₂ Recovery Efficiency. The standard mandates that CO₂ Capture Efficiency and CO₂ Recovery Efficiency should be 99%+ and 95%+ respectively. This dashboard helps assess performance across half years.

Insights and recommendations are provided on the following key areas:

Category 1: CO₂ Capture

Category 2: CO₂ Recovery

Category 3: CO₂ Capture Efficiency 

Category 4: CO₂ Recovery Efficiency

The dataset was cleaned, aggregated, and analyzed in Excel, and Power Query before being visualized in Power BI.

📊<a href="Carbon-Capture Dashboard.pdf" target="_blank" class="btn btn-secondary">View Dashboard</a>

# Dataset Description
The data model comprises six tables capturing CO₂ capture and recovery performance across experimental runs, cycles, and efficiency metrics, totaling 363,330 records.

## Tables
* CO₂ Capture & Recovery: Main fact table with raw experimental data (CO₂ capture in kg, CO₂ recovery in kg, run number).
* CO₂ Capture Cumulatives: Aggregated table tracking cumulative CO₂ captured over time (cumulative value in kg).
*	CO₂ Recovery Cumulatives: Aggregated table tracking cumulative CO₂ recovered over time (cumulative value in kg).
* CO₂ Capture Efficiency: Measure table for capture efficiency calculations (percentage).
* CO₂ Recovery Efficiency: Measure table for recovery efficiency calculations (percentage).
* CO₂ Capture Efficiency (by Cycle): Helper table for cycle-level efficiency breakdown (% captured, cycle number).
* CO₂ Capture Recovery (by Cycle): Helper table for cycle-level recovery breakdown (% recovery, cycle number).

  
![image](https://github.com/user-attachments/assets/b2450f01-f074-4e75-a70e-275de9d03bd4)

# Executive Summary
## Overview of Findings
Across five experimental runs, the CO₂ capture system demonstrated consistently high capture efficiency but variable recovery performance depending on sorbent generation and configuration. Zeolite-based runs showed significantly lower capture volumes, while Gen 1 sorbent runs dominated total throughput.

* Total CO₂ captured across all runs reached 449.80 kg, with Run 1 Gen 1 contributing the highest volume at 173.89 kg.
*	CO₂ Capture Efficiency averaged 99.54%, indicating near-complete adsorption performance across cycles.
*	Total CO₂ recovered was 70.54 kg, reflecting an overall Recovery Efficiency of only 41.41%.
*	Run 3 (Zeolite only) recorded the lowest capture and recovery, suggesting limited sorbent effectiveness under tested conditions.
*	Significantly detected Gen 2 sorbent inefficiency normally it should be better than Gen 1 and determined it as the root cause of operational issues, and drove cost savings by discontinuing its production.

# Insights 
## Category 1: CO₂ Capture 
*	Capture volume varied significantly across runs, ranging from 5.86 kg (Run 3 Zeolite) to 173.89 kg (Run 1 Gen 1).
*	Runs using Gen 1 sorbent alone or in combination consistently outperformed Zeolite-only configurations.
*	Run 2 Gen 1 + Gen 2 by half-half capture around 164.26 kg. It should be better than pure Gen 1
*	The high capture efficiency (~99.54%) across most cycles confirms the adsorption stage is operating effectively.


![image](https://github.com/user-attachments/assets/d780664f-0fbf-4ed9-b703-98c52e71ff5a)

## Category 2: CO₂ Recovery 
*	Run 3 (Zeolite) recorded the lowest total recovery at 1.16 kg, while Run 2 Gen 1+2 achieved the highest at 20.35 kg.
*	Recovery efficiency showed high variability across cycles, with values ranging from near 0% to 100% within individual runs.
*	The scatter pattern in the Recovery Efficiency chart suggests desorption performance is sensitive to cycle conditions and sorbent type.


![image](https://github.com/user-attachments/assets/d72c7c2f-f368-43f4-bdaa-d0199444ff3d)

## Category 3: Capture vs. Recovery Gap
*	A significant gap exists between capture (449.80 kg) and recovery (70.54 kg), indicating that while CO₂ is effectively adsorbed, a large portion is not successfully desorbed and collected.
*	Optimizing the desorption phase particularly may be key to improving overall system efficiency.


![image](https://github.com/user-attachments/assets/818cd3e8-d327-4d71-b4c8-e1a4122a7161)


# Recommendations
*	Desorption Optimization: Given the large gap between capture efficiency (99.54%) and recovery efficiency (41.41%), further investigation into the desorption phase is critical. Temperature swing parameters and heating duration should be systematically varied to improve CO₂ release from the sorbent bed.
*	Scaling for Higher Throughput: Run 1 and Run 2 demonstrated the highest capture volumes (173.89 kg and 164.26 kg respectively). These configurations should be prioritized as the baseline for scaled-up pilot testing, with attention to maintaining efficiency at larger sorbent bed volumes.
*	Run Monitoring & Real-Time Diagnostics: Deploy cycle-level monitoring dashboards to detect early signs of sorbent degradation or performance drops, enabling proactive intervention before efficiency losses accumulate across long runs.

