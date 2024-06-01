# Electric Vehicle Charging Station Data Analysis

This project aims to analyze and predict the total cost of electric vehicle charging sessions using various machine learning models. The dataset used contains information about different charging sessions, including total kWh consumed, distance traveled, and the associated costs in dollars.

## Project Overview

The primary goal is to build models that can accurately predict the cost of charging sessions (`dollars`) based on other features in the dataset. We evaluate three machine learning models:

1. **Random Forest Regressor**
2. **Linear Regression**
3. **XGBoost Regressor**

We compare their performance using metrics such as Mean Squared Error (MSE) and R-squared (R²).

## Dataset

The dataset includes the following columns:

- `sessionId`: Unique identifier for each charging session
- `kwhTotal`: Total kWh consumed during the session
- `dollars`: Cost of the session in dollars (target variable)
- `platform`: Charging platform used
- `distance`: Distance traveled to the charging station
- `userId`: Unique identifier for the user
- `stationId`: Unique identifier for the charging station
- `locationId`: Location identifier of the station
- `managerVehicle`: Indicates if the vehicle is managed by a fleet
- `facilityType`: Type of facility where the charging station is located
- `reportedZip`: Zip code where the charging session was reported

## Data Preprocessing

1. **Loading Data**: The data is loaded from a CSV file into a pandas DataFrame.
2. **Handling Missing Values**: Rows with missing values are dropped.
3. **Feature Selection**: The target variable (`dollars`) is separated from the features.
4. **Encoding Categorical Variables**: Non-numeric columns are converted to a one-hot encoded format for model compatibility.

## Model Training and Evaluation

1. **Random Forest Regressor**:
   - A robust ensemble model that reduces overfitting and improves accuracy by combining multiple decision trees.
   - Achieved good performance with an MSE of approximately 0.042.

2. **Linear Regression**:
   - A simple yet effective model for predicting continuous values.
   - Provides a baseline for comparison against more complex models.

3. **XGBoost Regressor**:
   - An optimized gradient boosting model that handles large datasets efficiently and provides high accuracy.
   - Requires careful tuning of hyperparameters for optimal performance.

## Performance Metrics

- **Mean Squared Error (MSE)**: Measures the average of the squares of the errors, providing an indication of the model's accuracy.
- **R-squared (R²)**: Indicates the proportion of the variance in the dependent variable that is predictable from the independent variables.

## Results

The models' performances are visualized using a bar graph that compares their R-squared values and Mean Squared Errors. This helps in understanding the effectiveness of each model in predicting the cost of charging sessions.

## Conclusion

The project demonstrates the use of various machine learning techniques to predict the cost of electric vehicle charging sessions. By comparing different models, we can select the most suitable one for deployment based on performance metrics.

## Future Work

- **Hyperparameter Tuning**: Further optimize model parameters to enhance prediction accuracy.
- **Feature Engineering**: Explore additional features or transformations to improve model performance.
- **Real-time Prediction**: Develop a real-time prediction system for practical applications.

## Repository Structure

- `data/`: Directory containing the dataset.
- `notebooks/`: Jupyter notebooks with data exploration, preprocessing, and model training.
- `scripts/`: Python scripts for data preprocessing and model training.
- `results/`: Directory to save model evaluation results and visualizations.
- `README.md`: Project overview and instructions.

## Getting Started

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/ev-charging-analysis.git
   cd ev-charging-analysis
   ```
2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Notebook**:
   Open the Jupyter notebook in the `notebooks/` directory to explore the data and run the models.


## Acknowledgements

- The dataset used in this project is sourced from [Dataverse](https://dataverse.org/).
- This project utilizes libraries such as pandas, scikit-learn, XGBoost, and matplotlib for data analysis and machine learning.
