# Netflix Trend Forecasting

## Project Overview
Netflix Trend Forecasting is a machine learning and time series analysis project that studies historical Netflix content additions and generates exploratory forecasts of future additions.

The project uses the `date_added` column to identify the year each title was added to Netflix. It analyzes yearly trends, compares forecasting approaches, and produces predictions for future years.

## Objectives
- Analyze yearly Netflix content additions.
- Identify trends and changes in content additions over time.
- Compare forecasting methods using evaluation metrics.
- Generate exploratory forecasts for future years.
- Visualize historical trends and forecast results.

## Dataset
The project uses a Netflix titles dataset containing information about movies and TV shows.

**Dataset columns include:**
- `show_id` — Unique identifier for each title.
- `type` — Movie or TV Show.
- `title` — Title name.
- `director` — Director of the title.
- `country` — Country associated with the title.
- `date_added` — Date the title was added to Netflix.
- `release_year` — Original release year of the title.
- `rating` — Content rating.
- `duration` — Movie duration or TV show seasons.
- `listed_in` — Content genres or categories.

The dataset contains **8,790 records and 10 columns**. The available `date_added` data covers the years 2008–2021.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Statsmodels
- Google Colab

## Methodology
1. Load and inspect the Netflix dataset.
2. Convert `date_added` into a datetime format.
3. Extract the year each title was added.
4. Group the records by year and count the titles added.
5. Split the historical data chronologically into training and testing periods.
6. Evaluate forecasting methods using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R² score.
7. Compare the model results.
8. Generate exploratory forecasts for future years.
9. Visualize yearly additions and forecast results.

## Forecasting Methods
The project experiments with the following methods:

- **Previous-Year Baseline:** Uses the previous observed year's count as a reference for forecasting.
- **Moving Average:** Uses the average of recent yearly counts.
- **Linear Regression:** Models a linear relationship between year and yearly additions.
- **Holt's Exponential Smoothing:** Tests level and trend-based forecasting approaches.

## Model Evaluation
The forecasting methods are compared using:

- **MAE:** Measures the average absolute difference between actual and predicted values.
- **RMSE:** Measures prediction errors while penalizing larger errors more heavily.
- **R² Score:** Indicates how well predictions explain variation in the test data.

In the fixed-origin evaluation for 2018–2021, the previous-year baseline achieved an MAE of **575.25** and an RMSE of **609.21**, outperforming the tested moving-average and Holt trend approaches on those metrics.

## Project Outputs
The project is intended to produce the following files:

- `Netflix_Yearly_Additions.csv` — Year-wise Netflix title additions.
- `Netflix_Model_Comparison.csv` — Comparison of forecasting methods and evaluation metrics.
- `Netflix_Trend_Forecast.csv` — Exploratory forecasts for future years.
- `Netflix_Actual_vs_Predicted.png` — Visualization comparing actual and predicted values.
- `Netflix_Trend_Forecast.png` — Visualization of historical trends and future forecasts.

**Note:** These filenames describe the planned outputs. Include only files that have actually been generated in the project folder.

## Limitations
- The dataset covers only the years available in the supplied Netflix titles data.
- The dataset may not represent the complete Netflix catalogue or all regional content additions.
- The historical dataset contains a limited number of yearly observations.
- Netflix content additions can change due to licensing, regional availability, and business decisions.
- Forecasts are exploratory estimates and should not be treated as official Netflix predictions.

## How to Run
1. Install the required Python libraries.
2. Place the dataset in the `Dataset` folder.
3. Open `Netflix_Trend_Forecasting.ipynb` in Google Colab or Jupyter Notebook.
4. Update the dataset path if necessary.
5. Run the notebook cells in order.
6. Save the generated CSV files and visualizations in the `Results` folder.

## Installation
Install the required libraries using:

```bash
pip install pandas numpy matplotlib scikit-learn statsmodels
```

## Conclusion
This project demonstrates how historical Netflix content additions can be analyzed using Python and basic time series forecasting techniques. By comparing forecasting methods, it highlights the importance of evaluating predictions against historical data and understanding the limitations of small datasets.

The results provide an exploratory view of content addition trends rather than a reliable prediction of Netflix's actual future catalogue.