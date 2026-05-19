# ML_Projects/EDA


# Titanic_Analysis
# Titanic Dataset Analysis

## 1. Problem Statement

The goal of this project is to analyze the famous Titanic disaster dataset to understand the factors that influenced passenger survival. Specifically, we aim to:
- Identify patterns and characteristics of passengers.
- Analyze survival rates based on various features like gender, age, and passenger class.
- Extract business insights that explain why certain groups had higher or lower chances of survival.

## 2. Dataset Description

The dataset used for this analysis is the Kaggle Titanic dataset, which contains information about passengers aboard the Titanic. Key features include:
- `PassengerId`: A unique identifier for each passenger.
- `Survived`: Survival status (0 = No, 1 = Yes) - **Target Variable**.
- `Pclass`: Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd) - proxy for socio-economic status.
- `Name`: Passenger's name.
- `Sex`: Passenger's gender.
- `Age`: Passenger's age in years.
- `SibSp`: Number of siblings/spouses aboard the Titanic.
- `Parch`: Number of parents/children aboard the Titanic.
- `Ticket`: Ticket number.
- `Fare`: Passenger fare.
- `Cabin`: Cabin number.
- `Embarked`: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

## 3. Key Observations

Based on our initial data exploration and missing value analysis:
-   **Dataset Size**: 891 entries and 12 columns.
-   **Missing Values**: Significant missing data in `Cabin` (77.1%), `Age` (19.9%), and minor missingness in `Embarked` (0.22%). `Cabin` might be too sparse for direct use without heavy feature engineering or removal.
-   **Data Types**: A mix of numerical (`int64`, `float64`) and categorical (`object`) data types. Categorical features like `Sex` and `Embarked` will need encoding for modeling.
-   **Age Distribution**: A diverse age range from 0.42 to 80 years, with a mean of ~29.7 years, indicating a large population of young adults.
-   **Fare Distribution**: Skewed distribution, with a mean of ~32.2 but a maximum of 512.33, suggesting some very high-fare tickets.
-   **Overall Survival Rate**: Approximately **38.4%** of passengers survived.

## 4. Charts Generated

To visualize the data and our findings, the following charts were generated:
-   **Distribution of Passenger Ages (Histogram)**: Shows the frequency of passengers across different age groups.
-   <img width="841" height="547" alt="image" src="https://github.com/user-attachments/assets/62832107-6deb-4f69-b519-e5a3bb74a216" />

-   **Distribution of Passenger Classes (Bar Chart)**: Illustrates the count of passengers in 1st, 2nd, and 3rd classes.
-   <img width="695" height="470" alt="image" src="https://github.com/user-attachments/assets/448ec162-b321-4b24-8f09-24530db5df1a" />

-   **Survival Count (Bar Chart)**: Compares the number of passengers who survived versus those who did not.
-   <img width="695" height="470" alt="image" src="https://github.com/user-attachments/assets/7be4571d-cdc5-4cd5-a2dd-f31dd9d6c316" />


## 5. Conclusions

Our analysis revealed several critical insights into the Titanic disaster:
-   **Gender played a dominant role in survival**: Women had a significantly higher survival rate (74.2%) compared to men (18.9%). This strongly supports the 'women and children first' rescue protocol.
-   **Passenger Class likely influenced survival**: The majority of passengers were in 3rd class, and given historical context, it is highly probable that lower-class passengers had less access to lifeboats and lower survival chances. (Further analysis would confirm this direct correlation).
-   **Age distribution suggests a diverse passenger group**: The presence of many young adults and children indicates a broad demographic affected by the tragedy.
-   **High overall casualty rate**: The low overall survival rate (38.4%) highlights the immense loss of life and the catastrophic nature of the event.
-   **Data Quality Challenges**: Handling missing `Age` and `Cabin` data would be crucial for building predictive models.

This preliminary analysis provides a strong foundation for further predictive modeling or deeper inferential studies into the factors determining survival on the Titanic.
