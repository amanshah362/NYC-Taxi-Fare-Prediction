# 🚕 NYC Taxi Fare Prediction – Multiple Linear Regression (MLR)

This project predicts **NYC Yellow Taxi fare amounts** using historical trip data from the  
**New York City Taxi & Limousine Commission (TLC)**.  
The goal is to build a **Multiple Linear Regression (MLR)** model that can estimate taxi fares based on trip details such as pickup/dropoff locations, trip distance, time of day, and more.

---

## 📊 Project Overview
The dataset contains **NYC yellow taxi trip records for 2017**, including timestamps, locations, and fare amounts.  
The project follows a complete **Data Science Workflow**:
1. **Data Cleaning & Preprocessing**  
   - Handling missing values & duplicates  
   - Outlier detection using IQR  
   - Datetime conversion and duration calculation  

2. **Feature Engineering**  
   - Trip duration (minutes)  
   - Day of week & month extraction  
   - Rush-hour indicator  
   - Pickup–Dropoff group mean duration  
   - Dummy encoding of categorical variables

3. **Exploratory Data Analysis (EDA)**  
   - Boxplots, scatterplots, pairplots, and correlation heatmaps  
   - Detection of relationships between fare amount, distance, and time features

4. **Modeling**
   - **Multiple Linear Regression (MLR)** using `sklearn`  
   - Train/Test split with **StandardScaler**  
   - Evaluation metrics:
     - R² (Coefficient of Determination)
     - Mean Absolute Error (MAE)
     - Mean Squared Error (MSE)
     - Root Mean Squared Error (RMSE)

5. **Business Logic**
   - Special handling for `RatecodeID == 2` to account for flat-rate JFK trips.

---

## 📈 Key Insights
- Strong positive correlation between **trip duration/distance** and fare amount.  
- Rush-hour periods impact fare predictions significantly.  
- Outlier handling and feature scaling improved model accuracy.

---

## 🧮 Tech Stack
- **Language:** Python  
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn  
- **IDE/Tools:** Jupyter Lab

---

## ⚡ Results
| Metric | Training | Test |
|-------|---------|------|
| R² | ~0.83 | ~0.86 |
| RMSE | ≈ \$4.2 | ≈ \$3.6 |

*(Values may vary slightly depending on the dataset sample and hyperparameters)*

