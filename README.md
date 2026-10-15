# IncodeVision-internship

This repository is for my internship tasks where i upload all my internship. 


# Task 1 ( EDA and Data Cleaning ) .

Road Accident Data Analysis in India 🚗
📌 Project Overview
This project explores road accident data in India using Python. It focuses on understanding the dataset, checking data quality, handling missing values, and visualizing relationships between selected accident-related variables.
🎯 Objectives
- Load and inspect the road accident dataset.
- Perform basic exploratory data analysis (EDA).
- Identify and handle missing or unknown values.
- Visualize the relationship between speed limits and number of fatalities.
- Plot month and year data for an initial overview.
🛠️ Tools & Libraries
- Python
- Pandas — data loading and manipulation
- NumPy — numerical operations
- Matplotlib — charts and plots
- Seaborn — visualization library imported in the notebook
📂 Project Structure
Road-Accident-Data-Analysis/
├── task_1.ipynb
├── accident_prediction_india.csv
├── speed limit vs no. of fatalities.png
└── months vs years.png
Note: Add the CSV and plot images to your repository if you want this structure to match your uploaded project files.
🔍 Workflow
1. Import libraries — import Pandas, NumPy, Matplotlib, and Seaborn.
2. Load the dataset — read accident_prediction_india.csv into a Pandas DataFrame.
3. Inspect the data — use info(), describe(), head(), tail(), and shape to understand the dataset.
4. Handle missing values — replace "Unknown" in City Name with a missing value, then fill missing values in Traffic Control Presence, Driver License Status, and City Name using each column's mode.
5. Visualize the data — create a scatter plot of Speed Limit (km/h) against Number of Fatalities, and a bar chart using Month and Year.
📊 Visualizations
Speed Limit vs Number of Fatalities
A scatter plot is used to explore the relationship between speed limits and the number of fatalities. The plot alone does not establish causation.
Month vs Year
A bar chart is created using the Month and Year columns as coded in the notebook. For a more meaningful time-based analysis, consider plotting accident counts by month or year if the dataset contains an accident count or suitable record-level rows.
▶️ How to Run
1. Clone or download this repository.
2. Make sure Python is installed.
3. Install the required libraries:pip install pandas numpy matplotlib seaborn jupyter
4. Place accident_prediction_india.csv in the same folder as the notebook.
5. Open Jupyter Notebook:jupyter notebook
6. Open task_1.ipynb and run the cells in order.
💡 Key Learning Outcomes
- Reading CSV files with Pandas.
- Inspecting datasets with common DataFrame methods.
- Detecting and handling missing values.
- Using mode imputation for selected categorical columns.
- Creating scatter plots and bar charts with Matplotlib.
⚠️ Notes
- Results depend on the dataset's quality and contents.
- Filling missing values with the mode is a simple baseline approach; check whether it is appropriate for each column before using the data for further analysis.
- This notebook performs data analysis and visualization. It does not currently train or evaluate a machine-learning accident prediction model.
👤 Author
Add your name and GitHub profile here.
📄 License
Add a license if you intend to make this project reusable by others.


# Task 2 ( House_Price_Prediction ) .



# Task 3 (Email_Spam_Prediction ) .



# Task 4 (Churn_Prediction )  .
