# ***Project 1: Predicting Machine Downtime - The story of improving Manufacturing supply chain***

## **About this project:** 
I started this project as the first step in my Supply Chain Analyst journey. The project delved into the different characteristics and performance metrics of 3 machine models - from which I extracted the information to gain future glimpse of the machine downtime. 

By understanding and predicting this unfortunate trend, as a Supply Chain Analyst, my insights can contribute to preventing the machines from breaking down, maintaining smooth manufacturing operations, and preventing stock-out. 

## **Project Context:** 
The data explored the features of three machines - which are mainly used to prepare components used in aerospace, automotives, and medical device applications. 

**From the mechanic perspective, the features of the machine can be summed up as:** 
> Power: Components such as Voltage, Torque, Spindle_Speed → Most likely to impact the operation of the machines <br>

> Fluid Systems: Hydraulic Pressure, Coolant Pressure, Air System Pressure and Coolant Temperature as well as Hydraulic Oil Temperature <br>

> Mechanical Health: Determined by Spindle Bearing Temp, Spindle Vibration and Tool Vibration <br>

> Cutting and End Process Performance: Cutting <br>

## **Project Objectives:**
- Identify the pattern of Machine Downtime 
- Identify the components that affect the chances of the machine being down 
- Plan the maintenance of machines to ensure future operations. 

## **Data Description:** 
- Source: machine_downtime.csv  
- Size: 2500 observations
- Features:
- Numerical: Torque, Spindle Speed, Vibration, Pressure, Voltage, Temperature, Cutting Force
- Categorical: Machine ID, Assembly Line
- Target: Downtime (Binary: Failure vs No Failure)

## **Methodology:** 
### _Data Preprocessing_
- Missing value imputation using KNN from fancyimpute 
- Feature scaling with StandardScaler
- Encoding target variable using pd.get_dummies

### _Exploratory Data Analysis_
- Box Plots, line charts, correlation matrices
- Chi-square test for categorical impact

### _Modeling_
- Baseline: Logistic Regression
- Final: Random Forest Classifier (99% accuracy)

### _Interpretability_
- Feature importance (built-in + permutation)
- SHAP values to understand feature influence


## ***Key Insights*** 
**- Top 5 predictors**: Torque, Cutting Force, Hydraulic Pressure, Coolant Pressure and Spindle Speed

**- High torque** = lower failure probability

**- Random Forest** outperformed logistic regression **(99% vs 84%)**

**- Categorical features (machine ID, assembly line)** showed no significant impact

## _**Supply Chain Relevance**_
> **- Improved Production Planning:** Align maintenance windows with demand cycles
> 
> **- Reduced Safety Stock:** More confidence in uptime means leaner inventory
> 
> **- Fewer Disruptions:** Smoother material flow, better OTIF performance
> 
> **- Higher Asset Utilization:** Maximize equipment ROI through uptime extension

## Illustrations: 
![image](https://github.com/user-attachments/assets/e0cd1c9d-21b4-4e29-9740-b1e8f54e7a4d)
![image](https://github.com/user-attachments/assets/a51c41f4-0e34-4039-9cd0-56b5374e6ebd)
![image](https://github.com/user-attachments/assets/e047dae1-c1c7-454f-b86d-5e1d62d9f65d)
![image](https://github.com/user-attachments/assets/a8bb38c5-efed-4b0a-9fe1-fcdfebeabfad)


