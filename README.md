# 🎶 Analysis and Modeling of Taylor Swift's Spotify Data

This project explores the musical characteristics of Taylor Swift's discography using a Spotify dataset. The objective is to uncover trends in her music and build predictive models to estimate song popularity based on audio features.

---

## 📁 Project Structure

This notebook follows a classic Data Science workflow:

### 1. **Importing Libraries**
Key libraries used:
- `pandas`, `numpy` for data manipulation
- `matplotlib`, `seaborn` for visualizations
- `scikit-learn`, `xgboost` for modeling

---

### 2. **Data Loading & Preparation**
- Loads a CSV dataset containing detailed information on Taylor Swift’s songs.
- Drops unnecessary columns (e.g., `Unnamed: 0`).
- Converts date formats (e.g., release dates).
- Encodes categorical variables (e.g., album names) for use in machine learning.

---

### 3. **Exploratory Data Analysis (EDA)**
- Displays basic statistics and checks for missing values.
- Visualizes:
  - Distribution of BPM, popularity, tempo, danceability...
  - Correlation heatmaps
  - Feature evolution over time (e.g., tempo and popularity)
  - Comparisons across albums (acoustic vs. electronic, fast vs. slow)

---

### 4. **Model Preparation**
- Selects relevant features:  
  `danceability`, `energy`, `valence`, `tempo`, `acousticness`, `speechiness`, `liveness`
- Encodes albums using one-hot encoding
- Normalizes numerical values with `StandardScaler`
- Splits the data into training and test sets (80/20)

---

### 5. **Modeling & Evaluation**
Tested models include:
- **Linear Regression**
- **Random Forest Regressor**
- **XGBoost Regressor**

Metrics used:
- **MAE**: Mean Absolute Error  
- **RMSE**: Root Mean Squared Error  
- **R² Score**: Variance explained by the model

---

## 📈 Results & Insights

- **Most popular songs** are not necessarily tied to high tempo or energy.
- **Speechiness** and **energy** emerged as the most important features for predicting popularity.
- The **album** a song belongs to is a major predictor of popularity, outperforming audio features alone.
- **Random Forest** and **XGBoost** models performed better than linear regression (R² ≈ 0.20 vs ≈ 0).
- Using album encoding dramatically improved linear regression's performance (R² went from 0.02 → 0.82).
- **Cluster analysis** (K-means) revealed two dominant musical styles: upbeat/electronic vs. calm/acoustic.

---

## ▶️ How to Run the Notebook

1. **Install dependencies** (if not already installed):
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost


---

## 🧪 Additional Work: Web Scraping

At the beginning of the project, we explored the possibility of building our own dataset via web scraping. This involved collecting song titles, album names, and other metadata from online sources.

➡️ Although the extracted dataset was useful for learning purposes, it lacked advanced audio features such as energy, valence, or danceability.

We later switched to a more complete dataset found on Kaggle, which provided richer audio features directly from Spotify.

🗂️ The scraping code and the extracted dataset are still included in the `scraping-branch` of this repository, demonstrating our end-to-end data handling skills.







