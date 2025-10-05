# 🏏 IPL Score Prediction  

## 📌 Project Overview  
This project predicts the total score of a cricket team at the end of their innings during an IPL (Indian Premier League) match.  
The model is trained on historical IPL data from seasons 1–9 (2008–2016) and tested on season 10 (2017). It uses match statistics like batting/bowling teams, overs, runs, wickets, and performance in the last 5 overs to make predictions.  

---

## 📂 Dataset Overview  

The dataset (`ipl.csv`) contains ball-by-ball IPL match data, including:  

- Batting team  
- Bowling team  
- Overs (current over in the match)  
- Runs scored in that over  
- Wickets taken in that over  
- Runs in last 5 overs  
- Wickets in last 5 overs  
- Total score of the batting team at the end of the innings  
- Date of the match  

---

## ⚙️ Data Preprocessing  

- **Removed irrelevant columns** (match ID, venue, batsman, bowler, striker, etc.)  
- **Filtered consistent teams** (e.g., CSK, MI, RCB, etc.)  
- **Removed early overs** (first 5 overs dropped for better relevance)  
- **Converted date column** into datetime format  
- **One-Hot Encoding** applied to categorical variables (`bat_team`, `bowl_team`)  
- **Train/Test Split:**  
  - Training: IPL 2008–2016  
  - Testing: IPL 2017  

---

## 🤖 Model Building  

The following regression models were implemented:  

- Linear Regression  
- Decision Tree Regression  
- Random Forest Regression  
- AdaBoost Regressor (with Linear Regression as base learner)  

### 🔍 Model Evaluation Metrics  
- Mean Absolute Error (MAE)  
- Mean Squared Error (MSE)  
- Root Mean Squared Error (RMSE)  

**Result:** Linear Regression performed the best and was selected as the final model.  

---

## 🎯 Predictions  

Example predictions made for IPL seasons 11 & 12 (2018–2019):  

- **KKR vs. Delhi Daredevils (2018, Match 13)** → Predicted Score: `200/9`  
- **SRH vs. RCB (2018, Match 39)** → Predicted Score: `146/10`  
- **MI vs. KXIP (2019, Match 59 – Eliminator)** → Predicted Score: `186/8`  
- **RR vs. CSK (2019, Match 25)** → Predicted Score: `151/7`  

---

## 📊 Conclusion  

- Linear Regression emerged as the best-performing model.  
- The project demonstrates the feasibility of predicting IPL match scores using machine learning.  

### 🚀 Future Work  
- Improve feature engineering & hyperparameter tuning.  
- Add more data from newer IPL seasons.  
- Try advanced models like XGBoost or Neural Networks.  

---

## 🛠️ Tools & Libraries  
- **Language:** Python  
- **Libraries:** pandas, numpy, scikit-learn, seaborn, matplotlib  

---

## 📁 Repository Structure  

```bash
IPL-Score-Prediction/
│
├── data/
│   └── ipl.csv                   # Dataset file
│
├── notebook/
│   └── IPL_Prediction.ipynb      # Jupyter notebook with code
│
└── README.md                     # Project documentation
