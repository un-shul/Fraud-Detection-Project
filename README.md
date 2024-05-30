# Fraud Detection Project

This project aims to build a robust fraud detection system using various machine learning models to identify fraudulent transactions. The models used include Logistic Regression, Decision Tree, K-Nearest Neighbors, Support Vector Machine, and a Neural Network.

## Project Structure

- `FraudDetection.ipynb`: The Jupyter Notebook containing the entire workflow of the project, including data preprocessing, model training, evaluation, and results.
- `data/`: Directory containing the dataset used for this project.
- `images/`: Directory containing images and visualizations used in the notebook.

## Dataset

The dataset used for this project contains information on financial transactions, including features such as transaction amount, old and new balances for the origin and destination accounts, and the type of transaction. The target variable is `isFraud`, indicating whether a transaction is fraudulent.

## Data Cleaning and Preprocessing

1. **Handling Missing Values**: Missing values were filled with the mean for numeric columns.
2. **Outliers**: Outliers were removed using the Interquartile Range (IQR) method.
3. **Multi-Collinearity**: Highly correlated features were identified and handled to reduce redundancy.
4. **Feature Engineering**: New features such as balance differences (`balance_orig_diff` and `balance_dest_diff`) were created. The `type` column was one-hot encoded into multiple binary columns.
5. **Class Imbalance Handling**: The NearMiss technique was used to address the imbalance in the dataset.

## Models Used

The following models were trained and evaluated:
1. Logistic Regression
2. Decision Tree
3. K-Nearest Neighbors
4. Support Vector Machine
5. Neural Network

## Model Evaluation

Each model was evaluated based on Accuracy, F1 Score, and Confusion Matrix.

### Accuracy Scores
| Model                    | Accuracy   |
|--------------------------|------------|
| Logistic Regression      | 0.867652   |
| Decision Tree            | 0.934783   |
| K-Nearest Neighbors      | 0.983826   |
| Support Vector Machine   | 0.968522   |
| Neural Network           | 0.976348   |

### F1 Scores
| Model                    | F1 Score   |
|--------------------------|------------|
| Logistic Regression      | 0.869580   |
| Decision Tree            | 0.937965   |
| K-Nearest Neighbors      | 0.983704   |
| Support Vector Machine   | 0.967753   |
| Neural Network           | 0.976307   |

### Confusion Matrices
| Model                    | True Positive | True Negative | False Positive | False Negative |
|--------------------------|---------------|---------------|----------------|----------------|
| Logistic Regression      | 2537          | 2452          | 423            | 338            |
| Decision Tree            | 2835          | 2540          | 335            | 40             |
| K-Nearest Neighbors      | 2807          | 2850          | 25             | 68             |
| Support Vector Machine   | 2716          | 2853          | 22             | 159            |
| Neural Network           | 2802          | 2812          | 63             | 73             |

