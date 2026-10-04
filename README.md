# Credit Card Fraud Detection using Machine Learning

A Flask-based web application for analyzing credit card transaction data and detecting potentially fraudulent transactions using machine learning classification algorithms.

The application provides a web interface for loading transaction data, preprocessing and viewing the dataset, selecting machine learning models, evaluating their performance, and performing fraud predictions.

## Project Overview

Credit card fraud detection is a binary classification problem where transactions are classified as either:

```text
0 → Normal Transaction
1 → Fraudulent Transaction
```

This project uses machine learning models to identify patterns associated with fraudulent transactions.

## Machine Learning Models

The application supports:

- XGBoost Classifier
- Random Forest Classifier
- Decision Tree Classifier

The models are evaluated using:

- Accuracy
- Precision
- Recall

## Features

- Web-based user interface
- CSV dataset upload
- Dataset preprocessing
- Transaction data visualization
- Machine learning model selection
- Fraud prediction
- Accuracy evaluation
- Precision evaluation
- Recall evaluation
- Graph-based result presentation

## Application Workflow

```text
Upload Dataset
      ↓
Preprocess Data
      ↓
View Data
      ↓
Select Machine Learning Model
      ↓
Train Model
      ↓
Evaluate Performance
      ↓
Fraud Prediction
      ↓
Compare Results
```

## Project Structure

```text
Credit-card-Fraud-Detection-using-Machine-learning/
│
├── app.py
├── README.md
├── update 1.ipynb
├── updates 2.ipynb
│
├── doc/
│   ├── paper.docx
│   └── project report.docx
│
├── ppt/
│   ├── Zeroth Review .pptx
│   ├── 1st reveiw.pptx
│   └── 2nd reveiw.pptx
│
├── static/
│   └── assets/
│
└── templates/
    ├── index.html
    ├── Load Data.html
    ├── Pre-process Data.html
    ├── view data.html
    ├── model.html
    ├── prediction.html
    └── graphs.html
```

## Technologies Used

- Python
- Flask
- NumPy
- Pandas
- Scikit-learn
- XGBoost
- Pygal
- HTML
- CSS
- Bootstrap
- JavaScript

## Requirements

Install the required Python packages:

```bash
pip install flask numpy pandas scikit-learn xgboost pygal
```

## Dataset

The application expects a CSV dataset named:

```text
creditcard.csv
```

The dataset should contain a `Class` column representing the fraud label.

The application also expects the transaction features used by the prediction interface, including:

```text
Time
V1 ... V28
Amount
Class
```

The uploaded repository does not include the `creditcard.csv` dataset, so it must be supplied separately before running the application.

## Running the Application

Place the dataset in the project directory and install the required packages.

Then run:

```bash
python app.py
```

The Flask development server will start and provide a local URL, normally:

```text
http://127.0.0.1:5000/
```

Open that address in a browser.

## Application Pages

### Home

Provides the main interface and navigation.

### Load Data

Allows a CSV file to be uploaded to the application.

### Preprocess Data

Loads the uploaded dataset and performs basic dataset inspection.

### View Data

Displays a sample of transaction records through the web interface.

### Select Model

Allows the user to choose between:

```text
XGBoost
Random Forest
Decision Tree
```

The selected model is trained and its accuracy is displayed.

### Prediction

Provides an input form for transaction features and classifies the transaction as:

```text
Normal
```

or

```text
Fraud
```

### Graphs

Provides a visual comparison of model performance using:

- Accuracy
- Precision
- Recall

## Model Training

The current application samples a portion of the uploaded dataset and separates the features from the target variable.

The model evaluation uses a train/test split with:

```text
Test Size: 30%
Random State: 10
```

The `Time` and `Class` columns are excluded from the features used for model training in the model-selection route.

## Project Objective

The objective of this project is to demonstrate how machine learning can be applied to credit card fraud detection through a web-based application.

The project combines:

- Data preprocessing
- Machine learning
- Model comparison
- Classification
- Web development
- Performance evaluation

## Future Enhancements

Possible improvements include:

- Improved data preprocessing
- Feature scaling
- Handling class imbalance
- Cross-validation
- Hyperparameter tuning
- ROC-AUC evaluation
- Precision-Recall curves
- Model persistence
- Faster prediction using saved models
- Improved input validation
- Real-time transaction monitoring
- Database integration
- Authentication and user management

## Academic Project

This project was developed as a Machine Learning project focused on detecting fraudulent credit card transactions using classification algorithms and a Flask web application.
