# Ice Hockey Match Analytics & Winner Prediction

An end-to-end sports analytics project using historical ice hockey match data. It includes data quality checks, exploratory data analysis, visualizations, pre-match team-form feature engineering, and a comparison of machine-learning classifiers.

## Dataset
`Ice Hockey Dataset.xlsx` contains 9,282 match records and 30 columns, including dates, home/away teams, final scores, period scores, overtime fields, and winner.

## Project questions
- How do total goals and scoring patterns vary over time?
- How frequently does the home team win?
- What can historical team form tell us about home-win outcomes?
- How do Logistic Regression and Random Forest compare on a chronological holdout?

## Visual preview

![EDA preview](assets/eda_preview.png)

![Model comparison](assets/model_comparison.png)

## Reference model metrics

A reference run on a chronological holdout produced the following results. Re-run the notebook to regenerate metrics in your environment.

| Model | Accuracy | F1 | ROC-AUC |
|---|---:|---:|---:|
| Logistic Regression | 0.590 | 0.605 | 0.641 |
| Random Forest | 0.617 | 0.673 | 0.653 |

The performance is moderate, so describe it as a demonstration of an end-to-end workflow rather than a production-ready prediction service.

## Methods
- Python, pandas, NumPy
- Matplotlib and Seaborn for visualization
- scikit-learn preprocessing pipelines
- Logistic Regression and Random Forest
- Chronological train/test split
- Prior-history features based only on games before the match date
- Accuracy, precision, recall, F1-score, ROC-AUC, and confusion matrix

## Run in Google Colab
1. Upload this repository to GitHub or download the notebook.
2. Open `Ice_Hockey_Match_Analytics.ipynb` in Google Colab.
3. Run all cells. If prompted, upload `Ice Hockey Dataset.xlsx`.
4. Review the charts, metrics, and generated files in `outputs/`.

## Run locally
```bash
pip install -r requirements.txt
jupyter notebook Ice_Hockey_Match_Analytics.ipynb
```

## Important methodology note
The target `HomeWin` is derived from final scores, but final scores, winner, and post-match fields are not used as prediction features. Team form is computed from games dated strictly before the target match date. Games on the same date share the same prior-history snapshot. The test set uses the newest 20% of dates to better simulate forecasting future games.

## Limitations
This is a historical demonstration, not a guarantee of future outcomes or a betting recommendation. The dataset lacks player lineups, injuries, goalie information, rest/travel context, and other potentially important predictors. Performance can change across seasons.

## Suggested repository structure
```text
ice-hockey-match-analytics/
├── Ice Hockey Dataset.xlsx
├── Ice_Hockey_Match_Analytics.ipynb
├── README.md
├── requirements.txt
├── .gitignore
├── PROJECT_SUMMARY.md
├── LINKEDIN_POST.md
└── UPWORK_PORTFOLIO_DESCRIPTION.md
```

## Portfolio skills demonstrated
Data cleaning, exploratory data analysis, exploratory data visualization, feature engineering, classification, model evaluation, reproducible notebooks, and project documentation.
