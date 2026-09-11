Medical Insurance Cost Prediction using Random Forest Regressor


<img width="812" height="718" alt="Insurance Prediction" src="https://github.com/user-attachments/assets/78b464f1-a839-40f0-8cc8-785ee2dbe02c" />



**Project Overview**

This project predicts medical insurance charges using a Random Forest Regressor. The model uses demographic and health-related attributes such as age, BMI, smoking status, region, gender, and number of dependents to estimate expected insurance costs.
  
The goal is to support insurance providers, healthcare analysts, and customers by delivering a data-driven estimate of medical expenses and highlighting the factors that most influence cost variation.

**Business Problem**

Insurance companies need reliable cost prediction models to improve pricing strategies, assess customer risk profiles, reduce manual underwriting effort, and provide more personalized premium estimates.
  
  Improve pricing strategies
  Assess customer risk profiles
  Reduce underwriting effort
  Enhance customer experience through personalized premium estimates
  
  Traditional methods often fail to capture complex nonlinear relationships within healthcare data. Machine Learning provides a data-driven approach for more accurate predictions.

**Dataset**

The dataset contains demographic and health-related information of insured individuals.

**Features**

  Feature	Descriptionage	Age of the beneficiary
  sex	Gender of the individual
  bmi	Body Mass Index
  children	Number of dependents covered
  smoker	Smoking status
  region	Residential area
  charges	Insurance cost (Target Variable)
  Sample Data
  Age	Sex	BMI	Children	Smoker	Region	Charges19	Female	27.9	0	Yes	Southwest	16884.92
  45	Male	30.5	2	No	Southeast	8569.86


**Technology Stack**

  Python
  Pandas
  NumPy
  Scikit-Learn
  Matplotlib
  Seaborn
  Joblib
  Jupyter Notebook

**Machine Learning Workflow**

1. Data Collection

  Loaded the insurance dataset into Pandas DataFrame and performed initial data exploration.

2. Data Preprocessing
  Checked missing values
  Handled categorical variables using encoding techniques
  Feature transformation
  Data type validation

3. Exploratory Data Analysis (EDA)
   
  Conducted analysis to understand:
    Distribution of insurance charges
    Impact of smoking on costs
    BMI vs Charges relationship
    Age vs Charges correlation
    Regional insurance cost variations
<img width="1069" height="986" alt="image" src="https://github.com/user-attachments/assets/f8921ecd-9c52-435d-a2a9-d75d9343c45b" />

4. Train-Test Split

    Training Data: 80%
    Testing Data: 20%

6. Model Development

   Implemented Random Forest Regressor to capture nonlinear relationships between predictors and insurance charges.


7. Model Evaluation

    Evaluation metrics used:
    R² Score
    Mean Absolute Error (MAE)
    Mean Squared Error (MSE)
    Root Mean Squared Error (RMSE
<img width="543" height="407" alt="Corr Matrix" src="https://github.com/user-attachments/assets/90540996-4b9d-4efb-b58e-be93c1507482" />

<img width="632" height="472" alt="image" src="https://github.com/user-attachments/assets/36aeb9f5-8d72-4d4b-b1b3-1771cc2ddb38" />


7.Results

  The Random Forest Regressor demonstrated strong predictive performance by accurately estimating insurance expenses from customer 
  demographic and health-related factors.
    
  Example metrics:
       
  r2_score : 0.92
        
  MSE: 3149705.2
        
  RMSE : 1774.7
        
  MAE : 1270.5


**Key Insights**
    
  Smoking Significantly Increases Insurance Costs
  
  Smokers incur substantially higher medical charges compared to non-smokers.
  
  Age Positively Correlates With Charges
  
  Older individuals generally have higher insurance expenses.
  
  BMI Influences Healthcare Costs 
  
  Higher BMI values often contribute to increased medical costs.
  
  Dependents Have Moderate Impact
  
  The number of children affects insurance charges but less significantly than smoking status and age.

**Feature Importance**

  Random Forest provides feature importance scores, helping identify the most influential variables.
  
  Typical ranking:
    
  Smoker
  
  Age
  
  BMI 
    
  Children
  
  Region
  
  Sex

**Model Deployment**

After successfully training and evaluating the Random Forest Regressor model, 
the solution was deployed as an interactive web application, enabling users to predict medical insurance costs in real time.

**Web Application Development**

   A user-friendly interface was developed using Streamlit, allowing users to enter:
    Age
    Gender
    BMI
    Number of Children
    Smoking Status
    Region
    The application processes the inputs and generates an estimated insurance cost instantly.
