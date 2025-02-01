# Delivery Time Prediction - Data Analysis & Machine Learning

## 📌 Project Overview
This project focuses on predicting delivery times based on various factors such as weather conditions, traffic density, order type, and delivery distance. It involves **data preprocessing, feature engineering, exploratory data analysis (EDA), and machine learning model building** to enhance delivery time estimation accuracy.

## 📁 Dataset
The dataset contains information related to deliveries, including:
- **Delivery_Order_ID**
- **Delivery_Person_ID**
- **Delivery_Person_Age**
- **Delivery_Person_Ratings**
- **Restaurant_Latitude & Longitude**
- **Delivery_Location_Latitude & Longitude**
- **Order_Date, Time_Ordered, Time_Picked**
- **Weather_Conditions, Road_Traffic_Density, Vehicle_Condition**
- **Type_of_Order, Type_of_Vehicle, Multiple_Deliveries**
- **Festival, City, Time_Taken (min)**

---
## 🚀 Project Workflow
### 1️⃣ Data Preprocessing
- **Handling Missing Values**: Imputation for numerical and categorical variables.
- **Data Type Correction**: Ensuring numerical and categorical features are in the correct format.
- **Outlier Detection & Removal**: Identifying outliers using IQR and valid geographical ranges.
- **Duplicate Removal**: Eliminating redundant rows.
- **Datetime Processing**: Converting `Order_Date`, `Time_Ordered`, and `Time_Picked` into consistent formats.

### 2️⃣ Feature Engineering
- **Extracting Date Features**: Day, month, quarter, year, weekday, and weekend.
- **Calculating Time Features**:
  - `Order_Preparation_Time` = Time_Picked - Time_Ordered
  - `Travel_Time` = Time_Taken - Order_Preparation_Time
- **Distance Calculation**: Using the Haversine formula to compute delivery distances.
- **Speed Calculation**: `Distance / Time_Taken`
- **Binning Continuous Features**: Categorizing `Order_Preparation_Time`, `Distance`, and `Time_of_Day`.
- **Handling Negative Travel Times**: Correcting or imputing invalid values.

### 3️⃣ Exploratory Data Analysis (EDA)
- **Correlation Analysis**: Heatmaps to identify relationships between variables.
- **ANOVA for Categorical Features**: Evaluating statistical significance.
- **Visualizations**:
  - Boxplots for `Time_Taken` vs. `Weather_Conditions`, `Road_Traffic_Density`, etc.
  - Distribution plots for understanding feature impact.

### 4️⃣ Model Building
#### 🔹 Data Encoding & Transformation
- **One-Hot Encoding** for categorical features.
- **Label Encoding** for ordered categories (`City_Code`, `Vehicle_Condition`).
- **Boolean Conversion**: `True/False` → `1/0`.
- **Feature Selection**: Choosing relevant columns for training.

#### 🔹 Model Selection & Evaluation
- **Splitting Data**: 80% training, 20% testing.
- **Algorithms Used**:
  - **Linear Regression**
  - **Random Forest Regressor**
  - **Gradient Boosting**
  - **XGBoost**
- **Evaluation Metrics**:
  - Mean Absolute Error (MAE)
  - Mean Squared Error (MSE)
  - R-Squared (R²)

---
## 💻 Installation & Setup
### Prerequisites
Ensure you have Python installed along with the required libraries.
```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

### Running the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/delivery-time-prediction.git
   ```
2. Navigate to the project folder:
   ```bash
   cd delivery-time-prediction
   ```
3. Run the preprocessing script:
   ```bash
   python preprocess.py
   ```
4. Train the model:
   ```bash
   python train_model.py
   ```
5. Evaluate the model:
   ```bash
   python evaluate.py
   ```

---
## 📊 Results & Insights
- The best-performing model was **XGBoost**, achieving an R² score of **0.92**.
- **Feature Importance Analysis** revealed that **distance, road traffic density, and order preparation time** were key predictors of delivery time.
- Further improvements can be made by incorporating **real-time traffic data** and **delivery personnel speed trends**.

---
## 📌 Future Enhancements
- Implement **deep learning models** for time series forecasting.
- Use **real-time GPS tracking data** for dynamic ETA predictions.
- Develop a **web-based dashboard** for live monitoring of delivery predictions.

---
## 🤝 Contributing
Contributions are welcome! Feel free to submit pull requests or open issues.

---
## 📄 License
This project is licensed under the **MIT License**.

---
## 📬 Contact
For any queries, feel free to reach out:
- **GitHub**: [yourusername](https://github.com/yourusername)
- **LinkedIn**: [Vigneshwaran](https://www.linkedin.com/in/vigneshwaran-datascientist/)

