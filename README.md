# ML_Regression_Project
# 🚖 NYC Taxi Trip Duration Prediction

### 📌 Project Type: EDA + Regression  
### 👨‍💻 Contribution: Individual  
### 🙍‍♂️ Author: Aman  

---

## 📊 Project Summary

This project focuses on building a machine learning model to predict the **trip duration of NYC taxis** based on a dataset containing over 1.4 million ride records. The dataset includes various features like:

- Pickup and drop-off coordinates
- Timestamps (date and time of travel)
- Passenger count
- Vendor and store-forward flags
- Engineered features like travel distance, pickup hour, weekday, etc.

---

## 🧹 Data Preprocessing

The preprocessing steps included:

- Handling missing and duplicate values (though minimal)
- Detecting and removing outliers using IQR
- Datetime feature extraction (hour, day, weekday)
- Distance calculation using the **Haversine formula**
- Feature scaling using `StandardScaler`
- Dropping irrelevant or ID columns

---

## 📈 Exploratory Data Analysis (EDA)

Key insights from the EDA include:

- Most trips occur during business hours (8 AM – 7 PM)
- Distance and duration are positively correlated but with outliers
- Weekends show fewer trips than weekdays
- Some vendor differences in trip length

---

## ⚙️ Feature Engineering

- **Datetime Features:** Extracted hour, day, weekday
- **Distance Feature:** Calculated using Haversine formula between pickup and drop-off coordinates
- **Speed (optional):** Derived from distance/duration

---

## 🤖 ML Models Used

Multiple regression models were trained and compared:

- Linear Regression
- Random Forest Regressor
- K-Nearest Neighbors Regressor
- XGBoost Regressor

---

## 📊 Model Evaluation Metrics

Evaluated using:

- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

---

## 📊 Model Evaluation: Training vs Testing Scores

Each model was evaluated using a custom function that prints:

- ✅ **Training R² Score**  
- ✅ **Testing R² Score**
- 📉 **MAE (Mean Absolute Error)**
- 📉 **MSE (Mean Squared Error)**
- 📉 **RMSE (Root Mean Squared Error)**
- 📈 **R² and Adjusted R² Score**

The scores from the best performing models were:

| Model                | Training R² | Testing R² | RMSE   | MAE    |
|---------------------|-------------|------------|--------|--------|
| Random Forest        | ~0.91       | ~0.67      | ~360.1 | ~180.3 |
| XGBoost Regressor    | ~0.89       | ~0.65      | ~370.5 | ~185.9 |
| Linear Regression    | ~0.70       | ~0.52      | ~410.2 | ~210.1 |
| KNN Regressor        | ~0.61       | ~0.48      | ~430.3 | ~225.6 |

---

## ✅ Conclusion

- The **Random Forest** and **XGBoost Regressors** performed the best, achieving an **R² score of ~0.67** and **low error rates**.
- Feature engineering (especially distance and time) significantly boosted model performance.
- The project demonstrates how thoughtful preprocessing and modeling can yield accurate predictions in real-world travel data.

---

## 🚀 Future Improvements

- Hyperparameter tuning with GridSearchCV
- Add external data (e.g., weather, traffic)
- Explore deep learning models (LSTM for time sequences)
- Use cross-validation for robustness

---

## 📂 File Structure

