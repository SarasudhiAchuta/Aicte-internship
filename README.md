# 💧 Water Potability Dataset Project

## 📌 Overview
This project works with the **Water Potability dataset** from Kaggle to analyze the quality of water samples and determine whether they are safe for human consumption.  

The dataset includes various water quality parameters such as pH, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic Carbon, Trihalomethanes, Turbidity, and a target column `Potability` (0 = Not Potable, 1 = Potable).

---

## 📂 Dataset Details
- **Source:** [Kaggle - Water Potability Dataset](https://www.kaggle.com/datasets/adityakadiwal/water-potability)  
- **File Name:** `water_potability.csv`  
- **Rows:** ~3,276  
- **Columns:** 10  

### Features
- `ph` – pH value of water  
- `Hardness` – Capacity of water to precipitate soap  
- `Solids` – Total dissolved solids in ppm  
- `Chloramines` – Amount of Chloramines in ppm  
- `Sulfate` – Amount of Sulfates dissolved in mg/L  
- `Conductivity` – Electrical conductivity of water in μS/cm  
- `Organic_carbon` – Organic carbon in ppm  
- `Trihalomethanes` – Trihalomethanes in μg/L  
- `Turbidity` – Turbidity of water in NTU  
- `Potability` – (Target) 1 if water is safe to drink, 0 otherwise  

---

## ⚙️ Preprocessing Workflow
1. **Load Dataset** from KaggleHub cache.  
2. **Basic Cleaning**  
   - Remove missing values (`dropna()`).  
   - (Optional) Impute missing values with mean/median.  
3. **Check Data Types** of all columns.  
4. **Encode Categorical Columns** (not needed here since all columns are numeric).  
5. **Save Processed Dataset** as `processed_water_potability.csv`.  

---

## 🖥️ Example Code

```python
import pandas as pd
import os

# Path to dataset
path = "/root/.cache/kagglehub/datasets/adityakadiwal/water-potability/versions/3"
csv_file = os.path.join(path, "water_potability.csv")

# Step 1: Load dataset
df = pd.read_csv(csv_file)

# Step 2: Basic cleaning
print("\nBefore cleaning:", df.shape)
df_clean = df.dropna()
print("After cleaning:", df_clean.shape)

# Step 3: Encode categorical columns (not required, but included for consistency)
df_processed = pd.get_dummies(df_clean, drop_first=True)

# Step 4: Save preprocessed dataset
processed_file = "processed_water_potability.csv"
df_processed.to_csv(processed_file, index=False)

print(f"\n✅ Preprocessed dataset saved as {processed_file}")
```

---

## 📊 Next Steps
- Perform **Exploratory Data Analysis (EDA)** to understand distributions & correlations.  
- Apply **scaling/normalization** (e.g., StandardScaler, MinMaxScaler).  
- Train **classification models** (Logistic Regression, Random Forest, XGBoost, etc.) to predict potability.  

---

## ✅ Output
After preprocessing, the cleaned dataset is saved as:

```
processed_water_potability.csv
```

---

## 👨‍💻 Author
Project prepared using **KaggleHub + Pandas** for dataset preprocessing.
