# ⚽ Football Betting Odds Prediction Using Machine Learning

## Overview <br>

This project was developed as part of my Master's thesis in Business Informatics and investigates whether machine learning models can accurately estimate football match outcome probabilities and generate betting odds that are competitive with those offered by professional bookmakers. <br>
<br>
Using historical data from the **Slovenian First Football League**, four supervised machine learning algorithms were trained and evaluated using **nested cross-validation**. The predicted probabilities were converted into decimal betting odds and compared against the market odds offered by **1XBet** and **William Hill** in terms of predictive accuracy and simulated betting profitability. <br>
<br>
This project demonstrates the complete machine learning workflow, from data preprocessing and feature engineering to model evaluation, probability estimation, odds generation, and profitability analysis. <br>
<br>

## Project Objectives

The primary objectives of this project were to: <br>
<br>
* Develop machine learning models capable of predicting football match outcomes. <br>
* Compare the predictive performance of multiple classification algorithms. <br>
* Convert predicted probabilities into decimal betting odds. <br>
* Compare the generated odds with bookmaker odds. <br>
* Evaluate whether value betting opportunities can be identified using machine learning. <br>
* Analyze the profitability of betting strategies based on the generated odds. <br>
<br>

## Dataset

The project uses historical match data from the **Slovenian First Football League** covering the **2005/06–2023/24** seasons. <br>

### Training Data

* Seasons: **2005/06–2022/23** <br>
* Matches: **3,240** <br>

### Test Data

* Season: **2023/24** <br>
* Matches: **180** <br>

Each match contains numerous pre-match variables describing both teams, including performance statistics, financial indicators, squad values, and historical performance metrics. <br>
<br>
The bookmaker odds (1XBet and William Hill) were available for evaluation purposes and were used only during the comparison stage. <br>
<br>

## Technologies Used

* Python <br>
* Pandas <br>
* NumPy <br>
* Scikit-learn <br>
* XGBoost <br>
* Matplotlib <br>
* Jupyter Notebook <br>
<br>

## Machine Learning Workflow

The project follows the workflow below: <br>

Historical Match Data <br>
&emsp;&emsp;│ <br>
&emsp;&emsp;▼ <br>
Data Cleaning & Preprocessing <br>
&emsp;&emsp;│ <br>
&emsp;&emsp;▼ <br>
Feature Engineering <br>
&emsp;&emsp;│ <br>
&emsp;&emsp;▼ <br>
Nested Cross-Validation <br>
&emsp;&emsp;│ <br>
&emsp;&emsp;▼ <br>
Hyperparameter Optimization <br>
&emsp;&emsp;│ <br>
&emsp;&emsp;▼ <br>
Model Selection <br>
&emsp;&emsp;│ <br>
&emsp;&emsp;▼ <br>
Probability Prediction <br>
&emsp;&emsp;│ <br>
&emsp;&emsp;▼ <br>
Decimal Odds Calculation <br>
&emsp;&emsp;│ <br>
&emsp;&emsp;▼ <br>
Comparison with Bookmaker Odds <br>
&emsp;&emsp;│ <br>
&emsp;&emsp;▼ <br>
Profitability Simulation <br>
<br>

## Machine Learning Models

Four classification algorithms were evaluated: <br>
<br>
* Logistic Regression <br>
* Support Vector Machine (SVM) <br>
* Gradient Boosted Trees <br>
* Extreme Gradient Boosting (XGBoost) <br>
<br>
Nested Cross-Validation was used for unbiased model comparison and hyperparameter tuning. <br>
<br>
After selecting the best-performing algorithm, a final model was trained using standard k-fold cross-validation before evaluation on the unseen 2023/24 season. <br>
<br>

## Model Evaluation

The models were evaluated using several classification metrics, including: <br>
<br>
* Accuracy <br>
* Precision <br>
* Recall <br>
* F1-score <br>
* ROC AUC <br>
* Log Loss <br>
<br>
The final evaluation was performed on an unseen test season to simulate real-world prediction performance. <br>
<br>

## Results

Among the evaluated algorithms, **Logistic Regression** achieved the strongest overall performance. <br>
<br>
### Final Test Performance <br>
<br>
| Metric    | Value | <br>
| --------- | ----- | <br>
| Accuracy  | 73.8% | <br>
| Precision | 69.9% | <br>
| Recall    | 74.8% | <br>
| F1 Score  | 72.3% | <br>
| ROC AUC   | 0.753 | <br>
| Log Loss  | 0.589 | <br>
<br>
The generated probabilities were converted into decimal betting odds and compared with the odds offered by 1XBet and William Hill. <br>
<br>
The comparison demonstrated that the machine learning model was capable of producing competitive probabilities while also identifying situations where the market may have undervalued or overvalued certain outcomes. <br>
<br>

## Repository Structure

football-odds-prediction-ml <br>
│ <br>
├── README.md <br>
├── LICENSE <br>
│ <br>
├── data/ <br>
│ &emsp;   └── Database - 3 sheets.xlsx <br>
│ <br>
├── notebooks/ <br>
│ &emsp;  ├── MV_Thesis_Bet_1.ipynb <br>
│ &emsp;  ├── MV_Thesis_Bet_2.ipynb <br>
│ &emsp;  └── MV_Thesis_Bet_X.ipynb <br>
│ <br>
├── images/
│ &emsp;  ├── Correlation matrix (initial set).png <br>
│ &emsp;  ├── Correlation matrix (final set).png <br>
│ &emsp;  ├── Example of the matchday 1 odds.pdf <br>
│ &emsp;  ├── List of features.pdf <br>
│ &emsp;  └── Nested cross-validation results.pdf <br>
│ <br>
└── master thesis/ <br>
&emsp;&emsp;└── Master Thesis - Mario Vežić (post-thesis' defence).docx <br>

## Key Findings

* Logistic Regression outperformed the more complex machine learning algorithms on this dataset. <br>
* Nested Cross-Validation provided an unbiased framework for model selection and hyperparameter optimization. <br>
* The generated probabilities closely aligned with bookmaker estimates while identifying potential value betting opportunities. <br>
* The project illustrates the importance of evaluating machine learning models not only through predictive metrics but also through practical financial outcomes. <br>
<br>

## Future Improvements

Possible extensions of this project include: <br>
<br>
* Including expected goals (xG) and advanced football statistics. <br>
* Evaluating deep learning approaches. <br>
* Expanding the methodology to additional football leagues. <br>
* Developing a fully automated betting pipeline using live data. <br>
<br>

## Related Projects

This project is part of a larger football betting analytics portfolio. <br>
<br>
### Football Betting SQL Analysis [sql-football-betting-analysis](https://github.com/mario-vezic/sql-football-betting-analysis)  <br>

A PostgreSQL project that evaluates the profitability of the generated betting odds using various betting strategies, bookmaker margins, expected value calculations, and return-on-investment analysis. <br>

### Slovenian League Tableau Dashboard [tableau-football-league-dashboard](https://github.com/mario-vezic/tableau-football-league-dashboard) <br>

An interactive Tableau dashboard that visualizes league statistics, betting performance, model predictions, bookmaker comparisons, and profitability metrics. <br>
<br>

## About Me

I am a Master's graduate in Business Informatics with a background in Psychology and a strong interest in machine learning, sports analytics, predictive modeling, and business intelligence. <br>
<br>
This project reflects my passion for combining data science with football analytics and demonstrates practical applications of machine learning in decision support and betting market analysis.<br>
<br>
