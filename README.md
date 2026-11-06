CleanSalone: Community Waste Collection and Reporting System

Course: PROG101 Principles of Programming Logic and Design (Limkokwing University of Creative Technology, Sierra Leone)

Assignment: Individual Assignment 1: Designing Logical Solutions for Sierra Leone Community Challenges

Student: Rhoda Y. Mansaray

Student ID: 905006427

Repository Name: PROG101_Assignment1_RhodaYMansaray_905006427

📌 Project Overview

Many communities in Sierra Leone, especially in dense urban areas like Freetown, face challenges with irregular and unprioritised waste collection. Overflowing bins, uncollected waste near drainage channels, and a lack of structured reporting mechanisms exacerbate flood and public health risks.

CleanSalone is a logical systems design (focusing on analysis, algorithms, and logic rather than source code) for a community reporting and dispatch system. It empowers citizens to report full or hazardous waste sites, validates inputs, classifies urgency using strict boolean logic and decision structures, and dispatches available trucks efficiently.

🌍 Sustainable Development Goals (SDG) Alignment

SDG 11: Sustainable Cities and Communities (Primary) – Target 11.6 focuses on municipal waste management and reducing the environmental impact of cities.

SDG 3: Good Health and Well-being – Prompt removal of overflowing and hazardous waste minimizes disease outbreaks (such as cholera).

SDG 13: Climate Action – Maintaining clear drainage channels mitigates urban flood risks during heavy rainfall seasons.

💡 Open Source & Digital Public Good Justification

CleanSalone is designed under an open-source philosophy (intended for an MIT or Apache 2.0 license) to ensure that local councils, student developers, and municipal workers across Sierra Leone (e.g., Freetown, Bo, Kenema, Makeni, Koidu) can inspect, adapt, translate (into Krio, Mende, Temne), and deploy the system without vendor lock-in or license fees. It incorporates privacy-by-design principles by collecting only necessary location data (community name and zone) and supports open data sharing through anonymized statistics.

📁 Repository File Structure

PROG101_Assignment1_RhodaYMansaray_905006427/
├── docs/
│   ├── algorithm.md
│   ├── problem_analysis.md
│   ├── references.md
│   ├── sample_outputs.md
│   └── sdg_open_source_dpg.md
├── flowcharts/
│   ├── dot_sources/
│   │   ├── 01_main_system.dot
│   │   ├── 02_submit_validate.dot
│   │   ├── 03_classify_priority.dot
│   │   ├── 04_dispatch_trucks.dot
│   │   └── 05_daily_summary.dot
│   ├── 01_main_system.png
│   ├── 02_submit_validate.png
│   ├── 03_classify_priority.png
│   ├── 04_dispatch_trucks.png
│   └── 05_daily_summary.png
├── LICENSE
├── README.md
└── pseudocode.txt


⚙️ System Modules & Logic

The system is broken down into modular, highly testable functions:

main(): Controls the core menu loop and user interaction.

submitReport(): Handles intake of community name, zone, waste type, fill level, days since collection, and drain proximity.

validateReport(): Implements robust input validation checks against empty strings, invalid waste categories, and out-of-range fill percentages ($0 - 100$).

classifyPriority(): Uses boolean logic to categorize reports into CRITICAL, HIGH, MEDIUM, or LOW.

processReports() / findAvailableTruck(): Sorts the queue by urgency and dispatches available zonal trucks.

checkReportStatus(): Allows tracking of individual reports by unique ID.

generateDailySummary(): Computes administrative operational counts and totals.

Priority Rules Summary

Priority

Condition

CRITICAL

Hazardous waste, OR fill $\ge 90\%$ for $\ge 3$ days, OR near a drain and fill $\ge 50\%$

HIGH

Fill $\ge 80\%$ OR $\ge 5$ days since last collection

MEDIUM

Fill $\ge 50\%$

LOW

All other valid reports

📄 Documentation

For the full detailed report covering rationale, computational thinking, step-by-step algorithms, complete pseudocode, flowcharts, and references, please refer to the documentation files inside the docs/ folder or the primary assignment text.
