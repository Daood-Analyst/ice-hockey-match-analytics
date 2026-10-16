# Portfolio Case Study: Ice Hockey Match Analytics

## Problem
Turn historical ice hockey match records into useful visual analysis and test whether match-level pre-game information can help classify home-team wins.

## Dataset
9,282 matches across 2008–2019, with 30 original columns. The dataset includes team names, dates, scores, period scoring, and overtime information.

## Approach
- Reviewed data types, missing values, duplicates, and date coverage.
- Explored total-goal distributions, home-team outcomes, year-level scoring, and period scoring.
- Engineered prior team win rates and average goals for/against using only matches from earlier dates.
- Split the data chronologically: 6,989 training matches and 2,293 test matches in the reference run.
- Compared Logistic Regression and Random Forest with accuracy, precision, recall, F1-score, ROC-AUC, and a confusion matrix.

## Reference results
| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.590 | 0.644 | 0.570 | 0.605 | 0.641 |
| Random Forest | 0.617 | 0.634 | 0.717 | 0.673 | 0.653 |

In this run, Random Forest had the higher F1-score and ROC-AUC. These are reference results from one environment and may vary with package versions or data handling. The model is not highly predictive and should not be marketed as a reliable outcome guarantee.

## What I learned / demonstrated
Data cleaning, exploratory data analysis, visualization, historical feature engineering, leakage-aware validation, scikit-learn pipelines, classification metrics, and communicating limitations.

## Next steps
Add a majority-class baseline, rolling-origin cross-validation, probability calibration, and richer pre-game context such as rest days, goalie availability, lineups, and team-specific home/away form.
