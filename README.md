# IncodeVision-internship


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

 
 
💡 Key Learning Outcomes
- Reading CSV files with Pandas.
- Inspecting datasets with common DataFrame methods.
- Detecting and handling missing values.
- Using mode imputation for selected categorical columns.
- Creating scatter plots and bar charts with Matplotlib.


# Task 2 ( House_Price_Prediction ) .

House Price Prediction 🏠

📌 Project Overview

This project uses a Linear Regression model to predict house prices from a dataset loaded from data.csv. The notebook explores the data, converts selected categorical columns into numeric features, trains and evaluates the model, and visualizes prediction results.


🎯 Objectives
- Explore and inspect the house-price dataset.
- Check data types, dataset dimensions, summary statistics, and missing values.
- Separate price as the target variable.
- Convert categorical features into numeric dummy variables.
- Train a Linear Regression model.
- Evaluate predictions using MAE, MSE, and R².
- Visualize the price distribution and actual-versus-predicted prices.

  
🛠️ Technologies & Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

  
📂 Project Structure

House-Price-Prediction/

├── house_prediction.ipynb

├── data.csv

├── outliers.png

└── actual_vs_predicted.png      



🔄 Project Workflow
1. Import Libraries
The notebook imports Pandas and NumPy for data handling, Matplotlib and Seaborn for visualization, and Scikit-learn for model training and evaluation.
2. Load and Explore Data
The dataset is loaded using:
df = pd.read_csv("data.csv")
The notebook inspects data types, the last few rows, dataset information, descriptive statistics, dataset shape, and missing-value counts.
3. Prepare Features and Target
The target variable is price, while the remaining columns are used as input features:
y = df["price"]
x = df.drop(["price"], axis=1)
4. Encode Categorical Features
The notebook uses pd.get_dummies() with drop_first=True on these columns:
- date
- street
- city
- statezip
- country
This converts the selected categorical columns into numeric indicator columns that the model can use.
5. Split the Dataset
The data is split into training and testing sets with an 80/20 split and random_state=42.
6. Train the Model
A LinearRegression model is fitted using the training features and target values.
7. Evaluate the Model
Predictions are generated for the test set and evaluated with:
- MAE (Mean Absolute Error): average absolute difference between actual and predicted prices.
- MSE (Mean Squared Error): average squared prediction error.
- R² (R-squared): indicates how well the model explains variation in the target on the evaluated data.
The actual metric values depend on the dataset and the results produced when the notebook is run.
8. Visualize Results
- Price box plot: visual inspection of the price distribution and potential outliers.
- Actual vs. Predicted scatter plot: compares actual test prices with model predictions.




▶️ How to Run the Project
1. Download or clone this repository.
2. Install Python if it is not already installed.
3. Install the required packages:pip nstall pandas numpy matplotlib seaborn scikit




# Task 3 (Email_Spam_Prediction ) .

readme = """# Email Spam Detection using Deep Learning 📧

## 📌 Project Overview


This project builds a binary email classification model to identify spam and non-spam emails. The notebook loads `spam_email_dataset.csv`, prepares the features, trains a neural network using TensorFlow/Keras, and evaluates its predictions with common classification metrics.

## 🎯 Objectives
- Load and inspect an email dataset.
- Separate the target label from the input features.
- Convert selected categorical/text columns into numeric dummy features.
- Split the data into training and testing sets.
- Scale the features.
- Train a feed-forward neural network for binary classification.
- Evaluate the model using accuracy, precision, recall, and F1-score.

## 🛠️ Technologies & Libraries
- Python
- Pandas and NumPy — data handling
- Scikit-learn — preprocessing, train-test split, and evaluation metrics
- TensorFlow / Keras — neural network model
- Matplotlib and Seaborn — visualization libraries imported in the notebook

## 📂 Project Structure
```text
Email-Spam-Detection/
├── Email_detection.ipynb
└── spam_email_dataset.csv
```

Keep `spam_email_dataset.csv` in the same directory as the notebook, or change the file path in the code.

## 🔄 Workflow

### 1. Load the Dataset
The notebook loads the CSV file:
```python
df = pd.read_csv("spam_email_dataset.csv")
```
It then checks the dataset's information, summary statistics, column names, shape, missing values, data types, and first rows.

### 2. Select Features and Target
The notebook uses `label` as the target:
```python
y = df["label"]
x = df.drop(["label"], axis=1)
```

### 3. Encode Features
The notebook applies `pd.get_dummies()` to `subject`, `email_text`, `sender_email`, and `sender_domain`, with `drop_first=True`, to convert these columns into numeric indicator features.

### 4. Split the Dataset
The data is split into training and testing sets using an 80/20 split, `random_state=42`, and stratification by `label`.

### 5. Scale Features
`StandardScaler` is fitted on the training features and then applied to the test features.

### 6. Build and Train the Neural Network
The model is a feed-forward neural network with:
- Input layer followed by a Dense layer with 128 units and ReLU activation
- Dense hidden layer with 64 units and ReLU activation
- Output layer with 1 unit and sigmoid activation

The model is compiled with the Adam optimizer, binary cross-entropy loss, and accuracy as a training metric. It is trained for 50 epochs with a batch size of 32 and uses 20% of the training data for validation.

### 7. Evaluate the Model
The notebook predicts labels for the test set using a threshold of 0.5 and calculates:
- **Accuracy:** overall proportion of correct predictions.
- **Precision:** proportion of predicted spam-positive cases that are correct.
- **Recall:** proportion of actual positive cases identified.
- **F1-score:** harmonic mean of precision and recall.

The notebook calculates these metrics when run. No specific performance score is stated here because results depend on the dataset and execution.



## ▶️ How to Run
1. Download or clone this repository.
2. Install Python.
3. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter
   ```
4. Put `spam_email_dataset.csv` in the project folder.
5. Start Jupyter:
   ```bash
   jupyter notebook
   ```
6. Open `Email_detection.ipynb` and run cells from top to bot

## ⚠️ Notes and Limitations
- The notebook uses `pd.get_dummies()` on `email_text` and other high-cardinality fields. This can create a very large feature matrix and does not capture text similarity in the same way as a TF-IDF representation. `TfidfVectorizer` is imported but is not used in the current notebook.
- `StandardScaler` may be inefficient for a very wide sparse feature matrix; a sparse-friendly text preprocessing pipeline may be more suitable.
- Confirm how the dataset encodes `label` (for example, 0 and 1) before interpreting precision and recall as spam-specific.
- The notebook evaluates the model but does not save the trained model for later use.

## 👤 Author
Add your name and GitHub profile here.

## 📄 License
Add a license if you want others to reuse this project.
"""
path="/mnt/data/README_email_spam_detection.md"
with open(path,"w",encoding="utf-8") as f:
    f.write(readme)
print(path, os.path.getsize(p


# Task 4 (Churn_Prediction )  .


readme = """# Customer Churn Prediction 📊

## 📌 Project Overview
This project uses machine learning to predict customer churn from a customer dataset. The notebook explores the data, prepares categorical features, trains a Random Forest Classifier, evaluates predictions, and creates visualizations to explore how selected customer attributes relate to the `Exited` target.

## 🎯 Objectives
- Inspect and understand the customer dataset.
- Check data types, summary statistics, missing values, and duplicate rows.
- Separate the target variable (`Exited`) from input features.
- Encode selected categorical columns.
- Train a Random Forest classification model.
- Evaluate the model using Accuracy, Recall, and ROC AUC.
- Visualize Credit Score, Balance, and Active Member status by churn label.

## 🛠️ Technologies & Libraries
- Python
- Pandas and NumPy — data handling
- Matplotlib and Seaborn — data visualization
- Scikit-learn — model training, splitting, and evaluation

## 📂 Project Structure
```text
Customer-Churn-Prediction/
├── churn.ipynb
├── Churn_dataset.csv
├── creditscore.png
├── balance.png
├── Isactivemember.png
└── EstimatedSalary vs Tenure.png
```

The CSV file is required to run the notebook. The PNG files are generated by the visualization cells when those cells run; add them to the repository only if you want to display the charts directly on GitHub.

## 🔄 Workflow

### 1. Import Libraries
The notebook imports Pandas, NumPy, Matplotlib, Seaborn, `RandomForestClassifier`, `train_test_split`, and classification evaluation metrics.

### 2. Load and Explore the Dataset
The notebook loads `Churn_dataset.csv` and inspects:
- First and last rows
- Dataset information and descriptive statistics
- Dataset shape and data types
- Missing-value counts
- Duplicate-row count

### 3. Separate Features and Target
The target is `Exited`; the remaining columns are used as input features:
```python
y = df["Exited"]
x = df.drop(["Exited"], axis=1)
```

### 4. Encode Categorical Columns
The notebook uses `pd.get_dummies()` with `drop_first=True` on:
- `Surname`
- `Geography`
- `Gender`

This converts those categorical columns into numeric indicator features.

### 5. Split the Dataset
The data is split into training and test sets with an 80/20 split and `random_state=42`.

### 6. Train the Model
A `RandomForestClassifier` is trained on the training data using Scikit-learn's default model settings.

### 7. Evaluate the Model
The notebook calculates:
- **Accuracy:** fraction of test examples classified correctly.
- **Recall:** fraction of actual positive (`Exited = 1`) examples identified by the model.
- **ROC AUC:** in the current notebook, this is calculated using predicted class labels (`y_pred`), rather than predicted probabilities or decision scores.

The actual metric values depend on the dataset and the results produced when the notebook is run.

### 8. Visualize Relationships
The notebook creates:
- Box plot of `CreditScore` by `Exited`
- Box plot of `Balance` by `Exited`
- Box plot of `IsActiveMember` by `Exited`
- Scatter plot of `EstimatedSalary` against `Tenure`

- 

## ▶️ How to Run
1. Download or clone this repository.
2. Install Python.
3. Install the required packages:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```
4. Place `Churn_dataset.csv` in the same directory as `churn.ipynb`.
5. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
6. Open `churn.ipynb` and run the cells from top to bottom.

## ⚠️ Notes and Limitations
- The notebook checks for missing values and duplicate rows but does not remove or impute them.
- `Surname` is included as a model feature after one-hot encoding. Depending on the dataset, it may add many features and may not generalize well.
- The notebook uses the default Random Forest settings and does not include hyperparameter tuning or cross-validation.
- ROC AUC is more informative when calculated from predicted probabilities, for example `model.predict_proba(x_test)[:, 1]`, rather than hard class labels.
- The notebook does not currently save the trained model for reuse.

## 👤 Author
Add your name and GitHub profile here.

## 📄 License
Add a license if you want others to reuse this project.
"""
path="/mnt/data/README_customer_churn_prediction.md"
with open(path,"w",encoding="utf-8") as f:
    f.write(readme)
print(path, os.path.getsiz
