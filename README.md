# Machine Learning Tasks Collection

This repository contains three machine learning projects implemented in
Python using Jupyter Notebooks. The tasks cover **credit default
prediction**, **handwritten character recognition**, and **heart disease
prediction**.

## Projects

### 1. Credit Scoring Model

**Folder:** `Credit_Scoring_Model`

This project predicts whether a credit card customer is likely to
default on their next payment.

#### Dataset

-   File: `default of credit card clients.xls`
-   Records: 30,000
-   Features after feature engineering: 26
-   Target: `default payment next month`

#### Methodology

-   Loaded the Excel dataset using Pandas
-   Checked dataset information, missing values, and duplicates
-   Removed duplicate records
-   Created:
    -   `TOTAL_BILL_AMT`
    -   `TOTAL_PAY_AMT`
-   Split the data into training and testing sets using an 80/20 split
-   Applied `StandardScaler`
-   Trained a **Logistic Regression** model
-   Evaluated the model using accuracy, precision, recall, F1-score,
    ROC-AUC, confusion matrix, and ROC curve
-   Tested the model with a sample customer

#### Results

  Metric                  Result
  --------------------- --------
  Accuracy                80.82%
  Precision (Default)     68.97%
  Recall (Default)        24.11%
  F1-Score (Default)      35.73%
  ROC-AUC                 70.78%

------------------------------------------------------------------------

### 2. Handwritten Character Recognition

**Folder:** `Handwritten Character Recognition`

This project uses a **Convolutional Neural Network (CNN)** to recognize
handwritten characters/digits from 28×28 pixel images.

#### Dataset

-   File: `train.csv`
-   Records: 42,000
-   Input features: 784 pixel values
-   Image size: 28×28
-   Number of classes: 10

#### Methodology

-   Loaded the image dataset using Pandas
-   Separated labels and pixel features
-   Reshaped the 784 pixels into 28×28 grayscale images
-   Normalized pixel values to the range 0--1
-   Encoded the target labels using one-hot encoding
-   Split the dataset into training and testing sets
-   Built a CNN using:
    -   Convolutional layers
    -   Max Pooling layers
    -   Flatten layer
    -   Dense layer
    -   Dropout
    -   Softmax output layer
-   Trained the model for 10 epochs
-   Evaluated the model using test accuracy and classification metrics
-   Generated a confusion matrix and sample predictions
-   Saved the trained model as `handwritten_character_cnn.keras`

#### Results

  Metric            Result
  --------------- --------
  Test Accuracy     99.01%
  Test Loss         0.0369
  Test Samples       8,400

The model achieved approximately **99% test accuracy** after 10 epochs.

------------------------------------------------------------------------

### 3. Disease Prediction from Medical Data

**Folder:** `Disease Prediction from Medical Data`

This project predicts the presence or absence of heart disease using
medical patient data and compares three machine learning algorithms.

#### Dataset

-   File: `heart-disease-cleveland.csv`
-   Records: 303
-   Features: 13
-   Target: `diagnosis`

The original target contains multiple disease levels. It is converted
into a binary classification problem:

-   `0` → No Disease
-   `1` → Disease

#### Models Used

-   Logistic Regression
-   Random Forest
-   Support Vector Machine (SVM)

#### Methodology

-   Loaded the CSV dataset
-   Checked missing values and dataset information
-   Replaced `?` values with missing values
-   Converted columns to numeric values
-   Cleaned column names
-   Converted the target into binary classes
-   Filled missing feature values using median imputation
-   Split the data into training and testing sets
-   Applied feature scaling for Logistic Regression and SVM
-   Trained and evaluated all three models
-   Compared model accuracies
-   Selected the best-performing model
-   Generated a confusion matrix and classification report
-   Tested the final model on a sample patient

#### Results

  Model                     Accuracy
  --------------------- ------------
  Logistic Regression         86.89%
  Random Forest           **88.52%**
  SVM                         85.25%

**Best Model:** Random Forest\
**Best Accuracy:** **88.52%**

------------------------------------------------------------------------

## Project Structure

``` text
code alpha/
│
├── README.md
│
├── Credit_Scoring_Model/
│   ├── Task1.ipynb
│   └── default of credit card clients.xls
│
├── Handwritten Character Recognition/
│   ├── task3.ipynb
│   ├── train.csv
│   └── handwritten_character_cnn.keras
│
└── Disease Prediction from Medical Data/
    ├── task4.ipynb
    └── heart-disease-cleveland.csv
```

> `.ipynb_checkpoints` folders are generated automatically by Jupyter
> and are not required to run the projects.

## Technologies Used

-   Python
-   Jupyter Notebook
-   Pandas
-   NumPy
-   Matplotlib
-   Scikit-learn
-   TensorFlow / Keras
-   Excel dataset (`.xls`)
-   CSV datasets

## Installation

Make sure Python is installed on your system. Then install the required
libraries:

``` bash
pip install pandas numpy matplotlib scikit-learn tensorflow xlrd jupyter
```

Alternatively, if you are using Anaconda, you can install the packages
through Anaconda/conda and run the notebooks using Jupyter Notebook.

## How to Run

1.  Download or clone this project.
2.  Open the project folder in Jupyter Notebook or JupyterLab.
3.  Open the required task notebook.
4.  Make sure the corresponding dataset is in the same folder as the
    notebook.
5.  Run the notebook cells from top to bottom.

### Task 1

Open:

``` text
Credit_Scoring_Model/Task1.ipynb
```

Make sure this dataset is present:

``` text
Credit_Scoring_Model/default of credit card clients.xls
```

### Task 3

Open:

``` text
Handwritten Character Recognition/task3.ipynb
```

Make sure this dataset is present:

``` text
Handwritten Character Recognition/train.csv
```

The notebook trains the CNN and saves the trained model as:

``` text
handwritten_character_cnn.keras
```

### Task 4

Open:

``` text
Disease Prediction from Medical Data/task4.ipynb
```

Make sure this dataset is present:

``` text
Disease Prediction from Medical Data/heart-disease-cleveland.csv
```

## Evaluation Summary

  Task     Project                             Main Technique                   Result
  -------- ----------------------------------- --------------------- -----------------
  Task 1   Credit Scoring                      Logistic Regression     80.82% Accuracy
  Task 3   Handwritten Character Recognition   CNN                     99.01% Accuracy
  Task 4   Disease Prediction                  Random Forest           88.52% Accuracy

## Important Notes

-   The notebooks contain the complete data preprocessing, model
    training, evaluation, and prediction workflow.
-   Results can vary slightly when the notebooks are retrained in a
    different environment or with different library versions.
-   The disease prediction project is an educational machine learning
    project and should not be used as a substitute for professional
    medical diagnosis.
-   The credit scoring model is also intended for educational purposes
    and should not be treated as a production financial decision system
    without further validation.

## Author

**Muhammad Khursheed**

**BSCS --- Minhaj University Lahore**

## License

This project is intended for educational and academic purposes.
