# Supply Chain – Late Delivery Risk Predictor  

## Overview  
This project develops a predictive model to identify supply chain orders at high risk of being delivered late. By analyzing various attributes of the dataset, the model helps supply chain managers anticipate delays and take proactive measures. The final solution is deployed as a Flask-based web application with both a user interface and a REST API.  

## Objectives  
- Build a predictive model to identify the risk of late deliveries.  
- Analyze features to understand key factors behind delays.  
- Create a Flask web application for interacting with the model.  

## Dataset  
The dataset consists of order, customer, product, and shipping details. The target variable is **`late_delivery_risk`** (0 = On Time, 1 = Late).  

**Examples of attributes used:**  
- Days for shipping (real)  
- Days for shipment (scheduled)  
- Delivery Status  
- Order Status  
- Shipping Mode  
- Category Name, Customer City, Market, Product Name  

## Tech Stack  
- **Languages and Libraries:** Python, scikit-learn, pandas, matplotlib, seaborn  
- **Machine Learning Models:** Logistic Regression, Naive Bayes, KNN, XGBoost, AdaBoost, Decision Tree (final model)  
- **Preprocessing:** category_encoders (TargetEncoder, LabelEncoder), SelectKBest (chi2), MinMaxScaler  
- **Frameworks:** Flask, Jinja2  
- **Frontend:** HTML, CSS, JavaScript  
- **Deployment:** Render  
- **Utilities:** joblib for model persistence  

## Key Features  
- Cleaned and preprocessed dataset (~180K rows, 52 attributes).  
- Automated ML pipeline with encoding, scaling, and feature selection.  
- Compared six ML models; selected **Decision Tree** for deployment based on evaluation metrics.  
- Flask application with HTML templates for input and output (`index.html`, `result.html`, `error.html`, `about_us.html`).  
- REST API endpoint (`/predict`) providing JSON output.  
- Deployed on **Render** for live access.  

## Screenshots  
Add screenshots into a `screenshots/` folder and embed them here. Example:  

![Home Page](screenshots/home.png)  
![Prediction Result](screenshots/result.png)  
![API JSON Output](screenshots/json.png)  

## Setup Instructions  
```bash
git clone https://github.com/22ad085/Supply-Chain-Management-.git
cd Supply-Chain-Management-
pip install -r requirements.txt
python model.py      # trains and saves the model
python app.py        # runs the Flask application
