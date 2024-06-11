# Machine Learning Model for Text Classification

In this project, the data has been preprocessed using techniques such as Bag of Words, TF-IDF vectorization, and word embedding. The objective is to build a machine learning model to predict the probabilities for a multilabel classification problem.

## Project Structure

- `train.csv`: Contains the training data with features.
- `trainLabels.csv`: Contains the labels for the training data.
- `test.csv`: Contains the test data for which predictions need to be made.
- `sampleSubmission.csv`: Example of the expected output format for the test predictions.

- `Aiqod_submission.xlsx`: Output file containing the predictions in the required format.


## Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn
- lightgbm

## Installation

To set up the environment and install all the necessary packages, run the following commands:

```bash
pip install pandas
pip install lightgbm
pip install scikit-learn 

```

## Explanation 

### 1. Data Loading and Preprocessing:
- The training features, test features, and training labels are loaded from CSV files.
- I identified a categorical column and used a Label Encoder to convert the data into numerical values.
- I identified the hash value column and used the hashlib library to convert the data into numerical values.  I then applied the hash function to the hash columns in both the training and testing datasets.

### 2. Data Cleaning and Alignment:
- I removed the duplicates and aligned the indices for the training features and labels.

### 3. Model Training:
- Since the model is a multilabel model, I used MultiOutputClassifier and LightGBM to build a model.
- I evaluated the model for each target separately using Classification Report.
- Predictions were made using the test_df.

### 4. Save the Model and Prediction:
- The model is saved using the pickle module after it is trained.
- The formatted predictions are saved to Aiqod_submission.csv and Aiqod_submission.xlsx


