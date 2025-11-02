COMPANY. CODTECH IT SOLUTIONS

NAME: SANJAY KUMAR SAINI

INTERN ID : CT04DR1297

DOMAIN : MACHINE LEARNING

DURATION: 4 WEEKS

MENTOR : NEELA SANTOSH

# DECISION-TREE-IMPLEMENTATION
Algerian Forest Fires Prediction
This project focuses on building a machine learning model to predict the occurrence of forest fires in two major regions of Algeria using the Algerian Forest Fires Dataset.

 #Project Goal
The primary objective is to develop a Decision Tree Classifier that can accurately predict the Classes (Fire or Not Fire) based on various weather and Fire Weather Index (FWI) components.

#Dataset Information
The dataset includes 244 instances collected over a four-month period (June to September 2012) and covers two regions of Algeria: Bejaia (northeast) and Sidi Bel-abbes (northwest).

The dataset features 11 attributes (features) and 1 output attribute (class).

| No. | **Attribute Name** | **Description**                                                        | **Range / Type**              |
| :-: | :----------------- | :--------------------------------------------------------------------- | :---------------------------- |
|  1  | **Temperature**    | Noon temperature (maximum) in Celsius                                  | 22°C to 42°C                  |
|  2  | **RH**             | Relative Humidity in percentage                                        | 21% to 90%                    |
|  3  | **Ws**             | Wind speed in km/h                                                     | 6 to 29                       |
|  4  | **Rain**           | Total rainfall during the day (mm)                                     | 0 to 16.8                     |
|  5  | **FFMC**           | Fine Fuel Moisture Code (FWI system)                                   | 28.6 to 92.5                  |
|  6  | **DMC**            | Duff Moisture Code (FWI system)                                        | 1.1 to 65.9                   |
|  7  | **DC**             | Drought Code (FWI system)                                              | 7 to 220.4                    |
|  8  | **ISI**            | Initial Spread Index (FWI system)                                      | 0 to 18.5                     |
|  9  | **BUI**            | Buildup Index (FWI system)                                             | 1.1 to 68                     |
|  10 | **FWI**            | Fire Weather Index                                                     | 0 to 31.1                     |
|  11 | **Region**         | Numerical encoding for the two regions: 0 = Bejaia, 1 = Sidi Bel-abbes | Categorical (0 or 1)          |
|  12 | **Classes**        | Target variable indicating fire occurrence                             | Categorical (Fire / Not Fire) |

#Data Preprocessing & Modeling Steps
The analysis and modeling pipeline followed in the Model Training.ipynb notebook consists of the following key steps:

Data Loading and Inspection: The cleaned dataset (Algerian_forest_fires_cleaned_dataset.csv) is loaded into a pandas DataFrame.

Feature Engineering (Drop Columns): The day, month, and year columns were dropped as the data seems to be aggregated or the date itself is not used as a feature in the model.

Target Variable Inspection: The Classes column was analyzed, revealing some minor inconsistencies (e.g., extra spaces) which were handled during encoding.

Feature Encoding:

The categorical Classes column was converted into a binary numerical format: 1 for 'fire' and 0 for 'not fire'.

Splitting Data: The data was split into Independent features (X) and the Dependent feature (y - Classes).

Train-Test Split: The dataset was divided into a training set (75%) and a testing set (25%) using test_size=0.25 and random_state=42 for reproducibility.

Model Training: A Decision Tree Classifier model was initialized and trained on the training data.

Model Evaluation: The model's performance was evaluated on the test set using accuracy score and a classification report.

Model Results
The Decision Tree Classifier demonstrated high performance on the test dataset.
Model Used: DecisionTreeClassifier
Test Size: 25%

Accuracy:0.967 (approx. 96.7%)
