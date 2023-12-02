# Project Name

Credit Card Approval Prediction

## Dataset Overview

The dataset used in this project is sourced from Kaggle, consisting of two files: `credit_record.csv` and `application_record.csv`. These files contain information about clients, including their demographics, financial details, and credit history.

### Metadata: credit_record.csv
ID:	Client number	
CODE_GENDER:	Gender	
FLAG_OWN_CAR:	Is there a car	
FLAG_OWN_REALTY:	Is there a property	
CNT_CHILDREN:	Number of children	
AMT_INCOME_TOTAL:	Annual income	
NAME_INCOME_TYPE:	Income category	
NAME_EDUCATION_TYPE:	Education level	
NAME_FAMILY_STATUS:	Marital status	
NAME_HOUSING_TYPE:	Way of living	
DAYS_BIRTH:	Birthday	Count backwards from current day (0), -1 means yesterday
DAYS_EMPLOYED:	Start date of employment	Count backwards from current day(0). If positive, it means the person currently unemployed.
FLAG_MOBIL:	Is there a mobile phone	
FLAG_WORK_PHONE:	Is there a work phone	
FLAG_PHONE:	Is there a phone	
FLAG_EMAIL:	Is there an email	
OCCUPATION_TYPE:	Occupation	
CNT_FAM_MEMBERS:	Family size

#### Metadata: application_record.csv

- **ID:** ID associated with a client
- **MONTHS_BALANCE:** The month of the extracted data
- **STATUS:** Credit status codes

## Vintage Analysis

A vintage analysis was performed to understand client behavior after an account was opened. Labels were generated based on the sum of the client's status, marking them as good or bad clients.

## Data Exploration
- Pie chart depicting the distribution of good and bad clients.
- Heatmap showing null values in the dataset.
- Correlation plot for continuous variables.

## Data Pre-processing

### Treating Missing Values

Due to missing values in the occupation type attribute, a machine learning model was trained using the Random Forest algorithm to predict the occupation type.

## Predictive Modeling

### Models Explored

- Random Forest Classifier
- Support Vector Machine (SVM)
- XGBoost

### Model Evaluation

SVM yielded the best results with an F1 score of 77%, a balanced accuracy of 62%, and precision of 72% on the test data.

## Techniques Used

- Principal Component Analysis (PCA)
- t-Distributed Stochastic Neighbor Embedding (t-SNE)
- Standard Scaler
- Synthetic Minority Over-sampling Technique (SMOTE)

## Results

SVM outperformed other models, achieving a balanced trade-off between precision and recall. The F1 score of 77% indicates a 5.48% improvement compared to other classifiers.

## Conclusion

In conclusion, this project provided hands-on experience in predictive modeling and showcased the effectiveness of different techniques and algorithms in credit risk prediction.

## Getting Started

To get started with this project, follow the steps below:

### Prerequisites

Make sure you have the following installed on your machine:

- [Python](https://www.python.org/) (version x.x.x)
- Required Python packages: `sklearn`, `plotly`, `matplotlib`, `xgboost`, `pandas`, `numpy`


## References
- [XGBoost Introduction](https://medium.com/analytics-vidhya/introduction-to-xgboost-algorithm-d2e7fad76b04)
- [Random Forest Introduction](https://www.analyticsvidhya.com/blog/2021/10/an-introduction-to-random-forest-algorithm-for-beginners/)
- [scikit-learn Documentation](https://scikit-learn.org/stable/supervised_learning.html)
