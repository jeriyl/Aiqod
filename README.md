# Machine Learning Model for Text Classification

This project involves building a machine learning model to predict the probability that a piece of text belongs to a particular class. The model is trained using various features extracted from the text, including Bag of Words, TF-IDF vectorization, and word embedding techniques.

## Project Structure

- `train.csv`: Contains the training data with features.
- `trainLabels.csv`: Contains the labels for the training data.
- `test.csv`: Contains the test data for which predictions need to be made.
- `sampleSubmission.csv`: Example of the expected output format for the test predictions.

- `Aiqod_submission.csv`: Output file containing the predictions in the required format.


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
- Load Data: The training features, test features, and training labels are loaded from CSV files.
- Identify Hash Columns: Define a function to identify hash columns and filter them out for separate handling.
- Label Encoding: Apply label encoding to non-hash categorical columns in both train and test data.
- Hash Encoding: Apply a hash function to hash columns in both train and test data.

### 2. Data Cleaning and Alignment:
- Remove Duplicates and Align Indices: Ensure there are no duplicate rows and align indices between training features and labels.

### 3. Model Training:
- Split Data: Split the training data into training and validation sets.
- Initialize and Train Model: Initialize a LightGBM classifier and wrap it with MultiOutputClassifier to handle multi-label classification.

### 4. Generating Predictions
- Predict on Test Data: Generate predictions on the test data.

### 5. Save the Model and Prediction:
- The model is saved using the pickle module after it is trained.
- The formatted predictions are saved to Aiqod_submission.csv.


