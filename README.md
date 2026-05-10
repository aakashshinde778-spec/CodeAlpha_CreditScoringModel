# CodeAlpha_CreditScoringModel

Credit Score Prediction using Logistic Regression
This project aims to classify an individual’s credit score into categories (High, Average, or Low) based on demographic and financial data. The repository includes a complete data science workflow, from Exploratory Data Analysis (EDA) and preprocessing to model training and deployment.

🚀 Project Overview
The model uses a Logistic Regression algorithm to predict creditworthiness. It achieves an training accuracy of approximately 94.3%, making it a reliable tool for preliminary financial assessments.

📊 Dataset Features
The model is trained on the following features:
•	Numerical: Age, Income, and Number of Children.
•	Categorical: Gender, Education, Marital Status, and Home Ownership.

Preprocessing Steps
To ensure the model performs optimally, the following transformations are applied:
1.	Imputation: Missing values are handled using SimpleImputer.
2.	Scaling: Numerical features are normalized using MinMaxScaler.
3.	Encoding: * OrdinalEncoder is used for features like Marital Status and Home Ownership.
o	OneHotEncoder is used for the Education category to create dummy variables.

🛠️ Installation & Setup
To run this project locally, follow these steps:
1.	Clone the repository:
 	git clone https://github.com/yourusername/credit-score-prediction.git
cd credit-score-prediction
2.	Create a virtual environment:
 	python -m venv venv
source venv/bin/activate # On Windows: venv\Scripts\activate
3.	Install dependencies:
 	pip install -r requirements.txt

📁 Repository Structure
├── models/
│ └── credit_score_model.joblib # Pre-trained Logistic Regression model
├── notebooks/
│ └── creditscorelogisticreg.ipynb # Comprehensive EDA and training notebook
├── data/
│ └── Credit Score Classification Dataset.csv # Source data
├── app.py # (Optional) Deployment script (e.g., Streamlit)
├── requirements.txt # List of required Python libraries
└── README.md # Project documentation

📈 Model Performance
Metric	Score
Training Accuracy	~94.3%
Algorithm	Logistic Regression
💻 Usage

To use the pre-trained model for new predictions, you can load it using joblib:
import joblib
import pandas as pd

# Load the model
model = joblib.load('models/credit_score_model.joblib')

# Prepare your processed input data (X_new)
# prediction = model.predict(X_new)
