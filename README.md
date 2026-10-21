# Lead Conversion Prediction (Random Forest)

Can we predict which sales leads will convert? A full machine learning workflow, ending with an honest deployment decision.

## Data
`lead_conversion_dataset.csv`: 10,000 leads with Age, Income, Website_Visits, Calls, Previous_Purchase, and Converted (45% Yes, 55% No).

## Steps
1. Explore the data: shape, types, missing values, class balance
2. Encode Yes/No columns as 1/0
3. Split 80/20 with stratification
4. Train a Random Forest (100 trees)
5. Evaluate with accuracy, precision, recall, F1, and a confusion matrix
6. Rank feature importance

## Results
| Metric | Score |
|---|---|
| Accuracy | 60.5% |
| Precision | 56.4% |
| Recall | 51.7% |
| F1 | 53.9% |

* A simple rule that predicts No for everyone already scores **55.2%**, so the model adds only about 5 points
* Income (45%) and Age (27%) drive most of the predictions

## Recommendation
**Not ready for production.** The lift over the baseline is small and the model misses almost half of the real buyers. Next steps: richer features (lead source, email engagement), gradient boosting, and hyperparameter tuning.

*Tools: Python, pandas, scikit-learn, Matplotlib, Seaborn. Herzing College coursework, May 2026.*
