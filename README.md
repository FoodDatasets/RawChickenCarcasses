# RawChickenCarcasses
## Raw Chicken Carcasses Dataset

## Overview
This dataset contains raw chicken carcass sampling data from various poultry establishments across the United States. The data are analyzed for the presence of Salmonella and Campylobacter, critical for monitoring food safety standards. Additionally, the dataset includes detailed weather data corresponding to the collection dates, providing insights into environmental factors that may influence bacterial detection results.

## Contents
- **Establishment Information**
  - `EstablishmentID`: Identifier for the poultry establishment
  - `EstablishmentNumber`: Number assigned to the establishment
  - `EstablishmentName`: Name of the establishment
  - `State`: State where the establishment is located
- **Project Information**
  - `ProjectCode`: Code related to the sampling project
  - `ProjectName`: Name of the project
- **Sample Information**
  - `CollectionDate`: Date when the sample was collected
  - `SampleSource`: Source description of the sample
  - `SalmonellaSPAnalysis`: Salmonella analysis results (Positive/Negative)
  - `CampylobacterAnalysis1ml`: Campylobacter analysis results for 1ml sample
- **Weather Data** (Corresponding to the collection date)
  - `MaxTemp_Day0`, `MinTemp_Day0`, `AverageTemp_Day0`: Temperature data
  - `Humidity_Day0`, `Precipitation_Day0`: Humidity and precipitation
  - `WindSpeed_Day0`, `WindDirection_Day0`: Wind speed and direction
- **Weekday Data**
  - `Weekday`: Day of the week when the sample was collected

## Data Source
This dataset is provided by the USDA's Food Safety and Inspection Service (FSIS). All data have been collected under strict quality control and assurance procedures to ensure their accuracy and reliability.

## Usage
This dataset is intended for researchers and professionals in food safety, public health monitoring, and environmental science. It allows for the analysis of bacterial contamination in raw chicken and understanding how various environmental factors might impact such results.

# Machine Learning Model Runner

## Description
This Python script facilitates the running of various machine learning models on a specified dataset. It supports logistic regression, MLP classifiers, decision trees, SVM, K-Nearest Neighbors, and Gradient Boosting Machines. Features include handling imbalanced datasets using techniques like Random Over Sampler and SMOTE, configurable model parameters through command-line arguments, and the display of feature importance for applicable models.

## Features
- **Multiple Machine Learning Models:** Choose from several models to train on your data.
- **Configurable Parameters:** Customize model parameters directly via command-line.
- **Feature Importance Display:** For models that support it, display the importance of each feature in the model.
- **Data Preprocessing:** Includes standard scaling and handling missing values.
- **Imbalance Handling:** Options to apply oversampling techniques to balance dataset classes.

## Prerequisites
To use this script, you'll need Python 3.x and several libraries installed on your system:
- **Pandas**
- **Scikit-learn**
- **Imbalanced-learn**

You can install the necessary Python libraries using pip:
```bash
pip install pandas scikit-learn imbalanced-learn
```
## Installation
To install this script, clone this repository to your local machine using

## Usage
Run the script from the command line, specifying the path to your dataset along with options to configure the model:
```bash
python filename.py <path_to_dataset> --model <model_name> --target <target_column> [other options]
```

## Command-line Arguments
- ` --filepath`: Mandatory. The path to the dataset file.
- ` --model`: Optional. Choose the machine learning model. Default is 'logistic_regression'.
- ` --target`: Optional. Specify the target variable column. Default is 'target'.
- ` --lr_C`: Optional. Regularization strength for logistic regression (inverse of lambda). Default is 1.0.
- ` --lr_max_iter`: Optional. Maximum iterations for logistic regression. Default is 100.
- ` --mlp_max_iter`: Optional. Maximum iterations for MLP classifier. Default is 200.
- ` --dt_max_depth`: Optional. Maximum depth for the decision tree. Use 'None' for no limit. Default is 'None'.
- ` --svm_C`: Optional. Regularization parameter for SVM. Default is 1.0.
- ` --svm_kernel`: Optional. Kernel type for SVM. Default is 'rbf'.
- ` --knn_n_neighbors`: Optional. Number of neighbors for KNN. Default is 5.
- ` --gbm_n_estimators`: Optional. Number of boosting stages for GBM. Default is 100.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# LAZY PREDICT METHOD
## Dependencies

- Python 3.7+
- pandas
- scikit-learn
- imbalanced-learn
- LazyPredict

``` bash
pip install pandas scikit-learn imbalanced-learn lazypredict
```
## Usage
1. Prepare your dataset file
2. Run the script with the dataset file and target column:

```bash
python LazyChicken.py /path/to/Dataset_RawChickenCarcasses.xlsx --target SalmonellaSPAnalysis( CampylobacterAnalysis30ml)
```

3. The script will output the number of positive cases for the target variable and evaluate various machine learning models.

## Example Output

### SalmonellaSPAnalysis
#### Model Performance Table

![Model Performance Table](Images/model_performance_table.png)

#### Model Accuracy Comparison

![Model Accuracy Comparison](Images/model_performance_bar.png)

### CampylobacterAnalysis30ml
#### Model Performance Table

![Model Performance Table](Images/model_performance_table_C.png)

#### Model Accuracy Comparison

![Model Accuracy Comparison](Images/model_performance_bar_C.png)




