# House Price Prediction (Advanced)

## Objective
Predict house prices using regression models and improve performance through feature engineering and model comparison.

## Dataset
Kaggle - House Prices: Advanced Regression Techniques

## Approach
- Selected multiple numerical features (area, rooms, garage, quality)
- Handled missing values using median imputation
- Performed feature engineering (HouseAge, TotalSF, TotalRooms)
- Added high-impact features (OverallQual, GarageCars)
- Split data into training and testing sets

## Models Used
- Linear Regression
- Random Forest Regressor

## Results
- Linear Regression MAE: ~23162
- Random Forest MAE: ~18816
- Tuned Random Forest MAE: ~18914

## Key Improvements
- Feature engineering had the biggest impact on performance
- Adding domain-relevant features significantly reduced error (~21k → ~18.8k)
- Model tuning gave smaller gains compared to feature improvements

## Key Learnings
- Random Forest handles non-linear relationships better than Linear Regression
- Not all feature engineering is useful — quality of features matters
- Real performance gains come from better data representation, not just tuning
