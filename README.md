# Parallel Processing-Based Weather Forecasting Model

## Overview
This project implements a parallel processing approach inspired by pitch estimators, utilizing three distinct models—SARIMAX, Random Forest (with lag features), and LSTM—to improve weather forecasting accuracy. By leveraging parallel model execution and a selection mechanism, the approach ensures robustness and adaptability in predictions.

## Motivation
Parallel processing techniques in pitch estimation utilize multiple estimators to refine results. Similarly, this project applies the same principle to time series forecasting, combining different models to optimize accuracy and stability.

## Models Used
1. **SARIMAX (Seasonal AutoRegressive Integrated Moving Average with eXogenous factors)**
   - Handles time series data with seasonality and exogenous inputs.
   - Effective in capturing long-term dependencies.

2. **Random Forest (with lag features)**
   - A tree-based ensemble method.
   - Uses past values (lags) as features to capture non-linear relationships.

3. **LSTM (Long Short-Term Memory Network)**
   - A deep learning approach suitable for sequential data.
   - Captures temporal dependencies effectively using memory cells.

## Methodology
1. **Parallel Model Execution**
   - All three models run in parallel, processing the input data simultaneously.
   
2. **MSE-Based Selection Mechanism**
   - Mean Squared Error (MSE) is used to evaluate each model.
   - A logic gate selects the best-performing model dynamically.
   
3. **Weighted Score Calculation**
   - Model complexity and stability are considered in the final score.
   - Lower MSE and stable variance contribute to higher selection probability.
   
4. **Final Model Selection**
   - The model with the lowest adjusted score is chosen for prediction.
   
## Dataset
The dataset includes meteorological parameters such as:
- Temperature
- Humidity
- Wind Speed
- Atmospheric Pressure
- Other relevant climate variables

## Implementation Details
- **Libraries Used**: NumPy, SciPy, scikit-learn, TensorFlow/Keras, statsmodels.
- **Cross-validation**: K-Fold method applied to evaluate model consistency.
- **Normalization**: MSE values are normalized for fair comparison.

## Results & Evaluation
- The parallel processing approach ensures robust model selection.
- Improved accuracy over standalone models.
- Dynamic adaptation based on model performance trends.

## Future Scope
- Integration of additional machine learning models for enhanced performance.
- Expansion to real-time forecasting with live weather data streams.
- Optimization of computational efficiency for large-scale deployment.

## Conclusion
This project successfully implements a parallel model processing strategy for time series forecasting, leveraging concepts from pitch estimation techniques to enhance predictive accuracy and model reliability.
