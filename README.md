# 🍷 Wine Type Prediction

A **Machine Learning classification project** that predicts whether a wine is **Red Wine** or **White Wine** based on its physicochemical properties.

The model is deployed as an interactive **Streamlit web application**, allowing users to enter wine characteristics and receive a prediction.

---

## 📌 Project Overview

Wine classification can be performed using various physicochemical properties of wine.

This project uses a trained Machine Learning model to classify wine into two categories:

* 🍷 **Red Wine**
* 🥂 **White Wine**

The application takes **12 input features** related to the wine's chemical properties and quality, processes them through the trained model, and displays the predicted wine type.

---

## 🎯 Objective

The main objective of this project is to build and deploy a Machine Learning classification model that can:

* Analyze wine characteristics
* Process multiple physicochemical features
* Predict the type of wine
* Provide an easy-to-use web interface
* Demonstrate Machine Learning model deployment using Streamlit

---

## ✨ Features

* 🍷 Red Wine / White Wine classification
* 🤖 Machine Learning-based prediction
* 🖥️ Interactive Streamlit interface
* 📊 12 wine-related input features
* ⚡ Fast prediction
* 📦 Pre-trained model stored using Joblib
* 🌐 Ready for web deployment
* 🍽️ Potential application in the Food & Beverage industry

---

## 📊 Input Features

The application uses the following **12 features**:

| #  | Feature              | Description                                  |
| -- | -------------------- | -------------------------------------------- |
| 1  | Fixed Acidity        | Amount of fixed acids present in the wine    |
| 2  | Volatile Acidity     | Amount of volatile acids present             |
| 3  | Citric Acid          | Citric acid concentration                    |
| 4  | Residual Sugar       | Amount of sugar remaining after fermentation |
| 5  | Chlorides            | Chloride concentration                       |
| 6  | Free Sulfur Dioxide  | Free sulfur dioxide level                    |
| 7  | Total Sulfur Dioxide | Total sulfur dioxide level                   |
| 8  | Density              | Density of the wine                          |
| 9  | pH                   | Acidity/basicity measurement                 |
| 10 | Sulphates            | Sulphate concentration                       |
| 11 | Alcohol              | Alcohol content                              |
| 12 | Quality              | Wine quality score                           |

The Streamlit application collects these values using numerical input fields.

---

## 🧠 Machine Learning Workflow

The project follows a standard Machine Learning workflow:

```text
Wine Dataset
     ↓
Data Preprocessing
     ↓
Feature Selection
     ↓
Model Training
     ↓
Model Evaluation
     ↓
Model Serialization
     ↓
Streamlit Deployment
     ↓
User Input
     ↓
Wine Type Prediction
```

---

## 🤖 Model

The trained classification model is stored in:

```text
wine_type_prediction.pkl
```

The model is loaded into the application using **Joblib**:

```python
model = joblib.load("wine_type_prediction.pkl")
```

The deployment code then passes the user-provided values to the model for prediction.

---

## 🔮 Prediction

After entering the required wine characteristics, the user clicks:

```text
Predict Wine Type
```

The model generates a classification prediction.

The application displays:

```text
0 → 🍷 Red Wine
1 → 🥂 White Wine
```

The prediction is generated using:

```python
prediction = model.predict(df)[0]
```

and the result is displayed in the Streamlit interface.

---

# 🍽️ Food & Beverage (F&B) Industry Application

This project can be applied to the **Food & Beverage (F&B) industry**, particularly in areas related to wine classification and product analysis.

### 💡 Potential F&B Use Cases

#### 🍷 1. Wine Classification

The model can automatically classify a wine as:

* Red Wine
* White Wine

based on its physicochemical properties.

#### 📦 2. Inventory Categorization

Restaurants, hotels, wine stores, and other F&B businesses could use classification systems to organize wine products according to their type.

#### 🏨 3. Hospitality Industry

Hotels and restaurants could potentially integrate wine classification into their internal food and beverage management systems.

#### 🛒 4. Wine Retail

Wine retailers could use automated classification as part of product categorization and inventory management.

#### 📊 5. F&B Analytics

Wine-related data can be analyzed to identify patterns between:

* Alcohol content
* Acidity
* Sugar
* pH
* Sulphates
* Quality
* Wine type

#### 🎓 6. Educational Application

The project demonstrates how Machine Learning can be applied to a real-world **Food & Beverage** problem.

---

## 🔄 F&B Prediction Workflow

```text
Wine Characteristics
        ↓
Data Processing
        ↓
Machine Learning Model
        ↓
Wine Classification
        ↓
┌─────────────────────┐
│                     │
│   🍷 Red Wine       │
│         OR          │
│   🥂 White Wine     │
│                     │
└─────────────────────┘
```

---

# 🖥️ Streamlit Application

The application is developed using **Streamlit**.

The interface provides input fields for all 12 wine characteristics and a prediction button.

The application collects the inputs and creates a Pandas DataFrame before sending the data to the trained model.

---

## 🛠️ Technologies Used

| Technology      | Purpose                         |
| --------------- | ------------------------------- |
| 🐍 Python       | Programming language            |
| 🤖 XGBoost      | Machine Learning classification |
| 📊 Pandas       | Data manipulation               |
| 🔢 NumPy        | Numerical operations            |
| 🧠 Scikit-learn | Machine Learning utilities      |
| 💾 Joblib       | Model serialization/loading     |
| 🌐 Streamlit    | Web application and deployment  |

The project's dependency file includes Streamlit, Pandas, NumPy, Scikit-learn, Joblib, and XGBoost.

---

# 📁 Project Structure

```text
Wine-Type-Prediction/
│
├── wine_type_prediction_model_deployment.py
├── wine_type_prediction.pkl
├── requirements.txt
└── README.md
```

### 📄 File Description

#### `wine_type_prediction_model_deployment.py`

Contains the Streamlit application, user input fields, DataFrame creation, and prediction logic.

#### `wine_type_prediction.pkl`

Contains the trained Machine Learning classification model.

#### `requirements.txt`

Contains the Python libraries required to run the application.

#### `README.md`

Contains the complete project documentation.

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone https://github.com/your-username/wine-type-prediction.git
```

## 2. Navigate to the Project

```bash
cd wine-type-prediction
```

## 3. Create a Virtual Environment

```bash
python -m venv venv
```

## 4. Activate the Environment

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

## 5. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Run the Application

Run the following command:

```bash
streamlit run wine_type_prediction_model_deployment.py
```

After running the command, Streamlit will provide a local address, normally:

```text
http://localhost:8501
```

Open this address in your browser to use the application.

---

# 🖥️ How to Use

### Step 1

Launch the Streamlit application.

### Step 2

Enter the required wine characteristics:

```text
Fixed Acidity
Volatile Acidity
Citric Acid
Residual Sugar
Chlorides
Free Sulfur Dioxide
Total Sulfur Dioxide
Density
pH
Sulphates
Alcohol
Quality
```

### Step 3

Click:

```text
Predict Wine Type
```

### Step 4

The application displays the predicted wine type:

```text
🍷 Red Wine
```

or

```text
🥂 White Wine
```

---

# 🌐 Deployment

The application can be deployed on a cloud platform that supports Streamlit applications.

Before deployment, make sure the repository contains:

```text
wine_type_prediction_model_deployment.py
wine_type_prediction.pkl
requirements.txt
README.md
```

After deployment, users can access the application through the generated web URL.

---

# 📦 Requirements

The project uses the following Python libraries:

```text
streamlit
pandas
numpy
scikit-learn
joblib
xgboost
```

---

# 🔮 Future Improvements

The project can be further improved by adding:

* 📈 Prediction probability
* 📊 Interactive data visualizations
* 🎨 Improved Streamlit UI
* ✅ Input validation
* 📋 Prediction history
* 📊 Model performance metrics
* 🔍 Feature importance visualization
* 🤖 Model comparison
* 📱 Improved responsive interface
* 🌐 Public cloud deployment
* 📊 F&B business analytics dashboard

---

# ⚠️ Disclaimer

This project is developed for **educational and demonstration purposes**.

The prediction should not be considered a replacement for professional wine testing, laboratory analysis, or expert Food & Beverage assessment.

---

# 👨‍💻 Author

## Aman Yadav

**B.Sc. Data Science & AI Student**

### Technical Skills Demonstrated

* Python
* Machine Learning
* Data Analysis
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Joblib
* Streamlit
* Machine Learning Deployment

---

# ⭐ Project Highlights

```text
🍷 Wine Type Prediction
🤖 Machine Learning Classification
📊 12 Wine Features
🌐 Streamlit Web Application
🍽️ Food & Beverage Industry Application
💾 Trained Model Deployment
```

> **A Machine Learning-powered Wine Classification application designed to demonstrate the practical use of Data Science and AI in the Food & Beverage industry.**

---

# 📄 License

This project is created for **educational and learning purposes**.
