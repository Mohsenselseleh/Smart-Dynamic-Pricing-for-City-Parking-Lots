# Smart-Dynamic-Pricing-for-City-Parking-Lots
Smart Dynamic Pricing for City Parking Lots for Capstone Project for Summer Analytics 2025 Presented by the Consulting &amp; Analytics Club × Pathway
Dynamic Pricing for Urban Parking Lots
Overview
This project implements a real-time dynamic pricing engine for urban parking spaces. The solution utilizes economic theory and machine learning to simulate demand-based, real-time pricing for multiple parking lots using live data streams. It aims to optimize utilization, prevent over- or under-crowding, and ensure fair pricing for users, leveraging Python, Pandas, NumPy, and Pathway for real-time data handling and modeling.

Tech Stack Used
•	Python 3
•	Pandas (data manipulation and analysis)
•	NumPy (numerical operations)
•	Pathway (real-time data streaming and simulation)
•	scikit-learn (for normalization/scaling)
•	matplotlib / seaborn / bokeh (visualization)
•	Google Colab (execution environment)

Architecture Diagram
mermaid
CopyEdit
flowchart LR
    Dataset[Urban Parking Dataset (CSV)]
    Pathway[Pathway Streaming & Simulation]
    Model1[Baseline Linear Model]
    Model2[Demand-Based Model]
    Model3[Competitive Pricing Model]
    Visualization[Bokeh/Matplotlib/Seaborn Plots]
    
    Dataset -->|Ingestion| Pathway
    Pathway -->|Streaming Data| Model1
    Pathway --> Model2
    Pathway --> Model3
    Model1 --> Visualization
    Model2 --> Visualization
    Model3 --> Visualization

Project Architecture and Workflow
1.	Data Ingestion:
o	Input data includes occupancy, queue, vehicle type, traffic, and timestamps for multiple parking lots, streamed via Pathway.
2.	Feature Engineering:
o	Calculate occupancy rate, normalize traffic, assign vehicle type weights, etc.
3.	Modeling Stages:
o	Baseline Linear Model: Simple price adjustment based on current occupancy.
o	Demand-Based Model: Dynamic price using occupancy, queue length, traffic, special days, and vehicle type.
o	Competitive Model: Incorporates spatial proximity and competitor pricing using geographic calculations.
4.	Real-Time Simulation:
o	All logic runs in streaming mode with Pathway to mimic real-time data updates.
5.	Visualization:
o	Real-time price and occupancy plots for each lot, with competitor comparisons.
6.	Output:
o	Results are saved to CSV and visualized as required.

How to Run
•	Open the provided Jupyter/Colab notebook (Final.ipynb or Sample_Notebook.ipynb)
•	Make sure dataset.csv is uploaded in your environment.
•	Run the notebook cells step by step to see data loading, preprocessing, modeling, and visualization.

Example Results
•	Line plots for pricing and occupancy over time for each lot
•	Demand-based vs. competitive price visualizations
•	Code for calculating baseline, demand, and competitor prices included



