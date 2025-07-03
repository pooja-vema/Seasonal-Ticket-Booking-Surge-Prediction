# Seasonal-Ticket-Booking-Surge-Prediction

A machine learning project that predicts seasonal surges in Indian railway ticket bookings using historical and categorical data. This solution supports railway operators in proactive planning, improving customer satisfaction, and optimizing resources during peak seasons.

📌 Problem Statement
Railway ticket bookings experience dramatic fluctuations during holidays, festivals, and weekends. This surge causes:
1. Overbooking and long waitlists.
2. Operational inefficiencies
3. Passenger inconvenience
4. The goal is to predict whether a booking surge will occur based on key features like travel dates, quotas, train types, and booking channels.

🎯 Objectives
Build a classification model to predict booking surges.
Identify key surge-influencing factors (e.g., holidays, class of travel).
Compare ML models to determine the best-performing one.
Provide actionable insights for railway operators.
🧠 Hypothesis

Surges are likely driven by:
Seasonal patterns (festivals, long weekends)
Premium train services (Rajdhani, Shatabdi)
Booking urgency (seat availability, waitlist length)

📊 Dataset
📁 Source: Kaggle
📌 Size: 18,000 rows × 21 columns
🔢 Data Types:
15 categorical features (e.g., Train Type, Quota)
6 numerical features (e.g., Seat Availability, Travel Distance)
Data Preprocessing Highlights:
Missing values handled via mode/mean or set to 'None' where needed.
Outliers analyzed using boxplots (no removals required).
Features normalized (MinMaxScaler, log transform).
Categorical data encoded via Label and One-Hot Encoding.
Feature engineering: Days before travel, Booking Demand Index, grouped travel classes.

⚙️ Methodology
Models Used:
Logistic Regression
  Interpretable, probabilistic, regularized
  Good baseline model
Random Forest
  Captures non-linear patterns
  Higher recall and F1-score
  Handles feature importance automatically
  
Model Evaluation:
Metric	      Logistic Regression	  Random Forest
Accuracy	        94.46%	              96.6%
F1 Score    	    0.9393                Higher
AUC-ROC	          0.9734	              Higher
False Negatives    170	                  83
📌 Random Forest was selected as the final model due to superior performance and lower error rates.

📈 Results
Random Forest achieved outstanding accuracy, especially in identifying true surge periods.
Confusion matrix and classification reports confirmed its reliability in minimizing both false positives and negatives.
Feature importance analysis provided explainability for decision-makers.

🚀 Future Enhancements
Integrate time-series models (e.g., LSTM, ARIMA).
Include external data like weather, holidays, and events.
Use SMOTE/class weighting for imbalance handling.
Deploy as a real-time API or dashboard.
Incorporate geospatial route analysis for regional trends.

🛠️ Tech Stack
Python
Scikit-learn
Pandas
Matplotlib / Seaborn
Jupyter Notebook

📚 References
Kaggle dataset
Scikit-learn documentation
Research papers on demand forecasting and classification models
upGrad modules and LPU academic support
