# LinkedIn project post

I’m sharing a sports analytics project built with Python and machine learning: **Ice Hockey Match Analytics & Winner Prediction**.

Using a historical dataset of 9,282 matches, I built a workflow covering:
- Data quality checks and exploratory data analysis
- Visualizations of scoring patterns and home-team outcomes
- Pre-match team-form feature engineering
- Logistic Regression and Random Forest classification
- Chronological model evaluation using precision, recall, F1-score, ROC-AUC, and a confusion matrix

One important design choice was avoiding target leakage: final scores and winner information are used to define/evaluate the target, not as model inputs. Team-form features are built from games played before the match date.

This project helped me practice turning raw sports data into an analysis workflow that is reproducible and easier to communicate.

Tools: Python, pandas, NumPy, Matplotlib, Seaborn, scikit-learn, Google Colab.

#Python #DataAnalytics #MachineLearning #SportsAnalytics #DataScience #PortfolioProject
