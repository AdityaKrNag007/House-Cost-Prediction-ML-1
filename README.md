# House Price Prediction (Advanced ML Pipeline with Boosting)

## Objective
Predict house prices using advanced regression techniques and build a robust, well-evaluated ML pipeline.

## Dataset
Kaggle - House Prices: Advanced Regression Techniques

---

## Approach

### Data Processing
- Selected key numerical features (area, rooms, quality, garage)
- Handled missing values using median imputation

### Feature Engineering
- Created derived features:
  - HouseAge = CurrentYear - YearBuilt
  - TotalSF = 1stFlrSF + 2ndFlrSF
  - TotalRooms = TotalRooms + Bedrooms
- Added high-impact features:
  - OverallQual
  - GarageCars
- Explored interaction feature:
  - Qual_GrLiv = OverallQual × GrLivArea

---

## Model Development

### Models Used
- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor (final model)

### Evaluation Strategy
- Split data into:
  - Train set → model training
  - Validation set → tuning and model selection
  - Test set → final unbiased evaluation
- Metric used: Mean Absolute Error (MAE)

---

## Results

| Model | Validation MAE | Test MAE |
|------|---------------|----------|
| Linear Regression | ~23.1k | ~23k |
| Random Forest | ~19.6k | ~19.2k |
| Gradient Boosting (default) | ~18.6k | ~19.3k |
| Gradient Boosting (tuned) | **~18.7k** | **~18.9k** |

---

## Key Improvements
- Reduced MAE from ~29k → ~18.9k through iterative improvements
- Controlled overfitting using validation-based tuning
- Improved generalization using lower learning rate in boosting
- Identified performance plateau in Random Forest and overcame it using boosting

---

## Key Learnings
- Feature engineering has the highest impact on model performance
- Boosting models outperform bagging methods when tuned properly
- Learning rate plays a critical role in controlling overfitting in boosting
- Validation set is essential for reliable model improvement
- Error analysis helps identify model limitations (e.g., regression-to-mean effect)

---

## Conclusion
Built a robust ML pipeline with strong generalization performance, demonstrating the transition from basic modeling to advanced model optimization and evaluation.
