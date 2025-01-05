# Customer Churn Prediction Using Artificial Neural Network (ANN)

This project uses an Artificial Neural Network (ANN) to predict customer churn based on historical data. The model is trained on a dataset containing 10,000 customer entries, achieving an accuracy of 87.5%.

## Features

The dataset contains the following features:

- **CreditScore**: Credit score of the customer.
- **Geography**: Country of the customer.
- **Gender**: Gender of the customer.
- **Age**: Age of the customer.
- **Tenure**: Number of years the customer has been with the bank.
- **Balance**: Bank account balance of the customer.
- **NumOfProducts**: Number of bank products held by the customer.
- **HasCrCard**: Whether the customer has a credit card (1 = Yes, 0 = No).
- **IsActiveMember**: Whether the customer is an active member (1 = Yes, 0 = No).
- **EstimatedSalary**: Estimated annual salary of the customer.
- **Exited**: Whether the customer has churned (1 = Yes, 0 = No).

## Model Architecture

The model is a Sequential ANN built with the following layers:

1. **Input Layer**  
   - Input shape: `(12,)` (12 features from the dataset).

2. **Hidden Layer 1 (HL1)**  
   - **Dense Layer**: 64 units  
   - **Activation Function**: ReLU

3. **Hidden Layer 2 (HL2)**  
   - **Dense Layer**: 32 units  
   - **Activation Function**: ReLU

4. **Output Layer**  
   - **Dense Layer**: 1 unit  
   - **Activation Function**: Sigmoid (for binary classification)

### Model Details

- **Epochs**: 20
- **Batch Size**: 32
- **Accuracy**: 87.5% on test data
- **Saved Model**: `First.h5`

## Project Structure

The project contains the following files:

1. **ChurnANN.ipynb**  
   The main Jupyter notebook where the ANN model is defined, trained, and evaluated.

2. **Churn_Modelling.csv**  
   The dataset containing customer details and churn labels.

3. **First.h5**  
   The trained ANN model saved in H5 format, used for predictions.

4. **Prediction_on_test_data.ipynb**  
   A notebook for making predictions on test data using the trained ANN model.

5. **README.md**  
   This file, providing an overview of the project.

6. **label_enc_gender.pkl**  
   A saved pickle file for the label encoder used for encoding the `Gender` feature.

7. **one_hot_geo.pkl**  
   A saved pickle file for the one-hot encoder used for encoding the `Geography` feature.

8. **scaler.pkl**  
   A saved pickle file for the scaler used to normalize numerical features.

9. **requirements.txt**  
   Contains all the dependencies required to run the project.

## Requirements

To run the project, install the dependencies from `requirements.txt`:

```bash
pip install -r requirements.txt
```
Usage
1. Running the Jupyter Notebooks
You can open the following notebooks to see the workflow:

ChurnANN.ipynb: Train and evaluate the ANN model on the dataset.
Prediction_on_test_data.ipynb: Make predictions on test data using the trained ANN model.

2. Prediction with Trained Model
To make predictions on new customer data, ensure the required .pkl files (label_enc_gender.pkl, one_hot_geo.pkl, and scaler.pkl) and the trained model (First.h5) are loaded properly.

## Run App.py for running streamlit web app
```bash
streamit run App.py
```
