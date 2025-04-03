# Energy Efficiency Analysis

This project focuses on predicting the heating and cooling loads of buildings based on their architectural characteristics. The analysis uses a dataset of 768 building shapes simulated in Ecotect, with 8 initial features.

## Dataset
- Source: [ENB2012_data.xlsx](https://github.com/JielingChen/building_energy_efficiency_prediction/raw/main/ENB2012_data.xlsx)
- Features: relative_compactness, surface_area, wall_area, roof_area, overall_height, orientation, glazing_area, glazing_area_distribution
- Targets: heating_load, cooling_load

## Analysis Performed
1. **Data Preprocessing**:
   - Renamed columns for clarity
   - Converted categorical variables
   - Dropped less relevant features (surface_area, orientation)
   - Binarized glazing_area_distribution

2. **Exploratory Analysis**:
   - Correlation heatmap
   - Boxplots for categorical vs target relationships
   - Scatter plots for glazing_area interactions

3. **Modeling**:
   - Implemented Linear Regression, Decision Tree and XGBoost models
   - Evaluated using:
     - Adjusted R² score
     - MSE, RMSE, MAE
   - Analyzed feature importance/coefficients

4. **Visualization**:
   - Model coefficient plots
   - Decision tree structures (limited to depth 3 for readability)

## Results
The models predict both heating and cooling loads with their performance metrics documented in the code. Key findings include:
- Relative compactness and overall height were among the most influential features
- Glazing characteristics showed non-linear relationships with targets
