# Noise Pollution Analysis Project  

## 📖 Description  
Noise pollution, also called **environmental noise**, is the unwanted or excessive sound that disrupts the natural balance of the environment.  
It is mainly caused by traffic, industrial activities, construction work, and urban lifestyle.  
Prolonged exposure to high noise levels can lead to **health problems** such as stress, sleep disturbances, hearing loss, and reduced productivity.  

This project aims to:  
- Measure and analyze noise levels across different areas (city center, residential zones, highways, parks, and school zones).  
- Categorize noise levels into **low, moderate, or high**.  
- Provide **visualizations and predictions** using machine learning models.  
- Create awareness about the harmful effects of noise pollution and encourage sustainable urban planning.  

By studying noise patterns, this project contributes to **building quieter and healthier cities**.  

---

## 📂 Repository Contents  
- **dataset.csv** → Synthetic dataset containing noise levels, locations, time, and conditions  
- **notebook.ipynb** → Jupyter Notebook with preprocessing, analysis, visualization, and ML model training  
- **noise_pollution_model.pkl** → Saved Logistic Regression model for classification  
- **README.md** → Project documentation  

---

## ⚙️ Installation & Setup  

### 1️⃣ Clone the Repository  
```bash
git clone https://github.com/your-username/noise-pollution.git
cd noise-pollution
```

### 2️⃣ Install Dependencies  
```bash
pip install -r requirements.txt
```

If `requirements.txt` is not included, install the key libraries manually:  
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 📊 Dataset Description  
The dataset (`dataset.csv`) contains the following columns:  

| Column         | Description |
|----------------|-------------|
| Location       | Area type (City Center, Residential, Highway, Park, School Zone) |
| Date           | Date of recording |
| Time           | Time of measurement |
| Noise_Level    | Measured noise in decibels (dB) |
| Category       | Classified as Low / Moderate / High noise |

---

## 🔍 Features Implemented  
✔️ Data Cleaning (handling missing values, formatting)  
✔️ Exploratory Data Analysis (EDA) with graphs  
✔️ Noise level categorization  
✔️ Logistic Regression Model for prediction  
✔️ Accuracy evaluation  

---

## 🚀 Usage  

1. Open the Jupyter Notebook:  
   ```bash
   jupyter notebook notebook.ipynb
   ```

2. Run all cells to:  
   - Load and preprocess dataset  
   - Visualize trends (noise levels by time & location)  
   - Train and test machine learning model  
   - Save and load trained model  

3. Predict using the trained model (example in Python):  
   ```python
   import joblib
   model = joblib.load("noise_pollution_model.pkl")
   prediction = model.predict([[75]])  # Example input: 75 dB
   print("Predicted Category:", prediction)
   ```

---

## 📈 Example Visualizations  
- Noise levels by location (bar chart)  
- Noise variation over time (line plot)  
- Distribution of noise levels (histogram)  
- Confusion matrix of ML model  

---

## 🎯 Future Enhancements  
- Integrating **real-time IoT sensors** for noise monitoring  
- Building a **dashboard with Plotly/Dash or Streamlit**  
- Deploying the model as a **web app**  
- Expanding dataset with **live recordings**  

---

## 🧑‍💻 Author  
**Achuta**  
📧 Contact: [your-email@example.com]  
🌍 GitHub: [your-profile-link]  
