# ANN Customer Churn Prediction
Customer Churn Prediction using ANN
TensorFlow • Keras • Streamlit

An end-to-end **Artificial Neural Network (ANN)** project that predicts whether a bank customer is likely to churn based on customer and account-related features.

The trained model is integrated into an interactive **Streamlit web application** and deployed online for real-time predictions.

## 🚀 Live Demo  https://ann-churn-pred1.streamlit.app/

**Streamlit App:** https://ann-churn-pred1.streamlit.app/

## 📌 Project Overview

Customer churn is an important problem for businesses, especially in the banking industry. Predicting customers who are likely to leave can help organizations take preventive actions and improve customer retention.

In this project, an Artificial Neural Network is trained to predict customer churn using features such as:

* Credit Score
* Geography
* Gender
* Age
* Tenure
* Account Balance
* Number of Products
* Credit Card Status
* Active Membership Status
* Estimated Salary

The complete workflow covers data preprocessing, feature encoding, scaling, ANN model training, evaluation, model serialization, and deployment.

## 🧠 Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **TensorFlow**
* **Keras**
* **Streamlit**
* **Matplotlib**
* **Jupyter Notebook**
* **Git & GitHub**

## 🔄 Project Workflow

```
Raw Dataset
     ↓
Data Preprocessing
     ↓
Categorical Encoding
     ↓
Feature Scaling
     ↓
Train/Test Split
     ↓
ANN Model
     ↓
Model Training
     ↓
Model Evaluation
     ↓
Save Model + Preprocessors
     ↓
Streamlit Application
     ↓
Deployment
```

## ⚙️ Data Preprocessing

The dataset contains both numerical and categorical features.

### Categorical Features

**Gender** is encoded using `LabelEncoder`.

**Geography** is encoded using `OneHotEncoder`.

### Numerical Features

Numerical features are scaled using `StandardScaler` before being passed to the neural network.

The same trained encoder and scaler are reused during prediction to ensure that new inputs are processed consistently with the training data.

## 🧠 ANN Architecture

The project uses a feed-forward Artificial Neural Network built using TensorFlow/Keras.

The network consists of:

* Input layer
* Fully connected hidden layers
* ReLU activation
* Output layer
* Sigmoid activation for binary classification

The model outputs a probability between 0 and 1 representing the estimated likelihood of customer churn.

## 📊 Prediction

The Streamlit application allows users to enter customer information through an interactive interface.

The application then:

1. Collects the user's input.
2. Encodes categorical features.
3. Combines the encoded features with numerical features.
4. Applies the trained scaler.
5. Passes the processed data to the ANN.
6. Generates a churn probability.
7. Classifies the customer based on the prediction threshold.

Example:

```
Churn Probability: 0.73

The customer is likely to churn.
```

## 🌐 Streamlit Application

The Streamlit interface provides interactive inputs including:

* Geography
* Gender
* Age
* Balance
* Credit Score
* Estimated Salary
* Tenure
* Number of Products
* Credit Card Status
* Active Membership Status

The application provides an immediate churn prediction after the user submits the information.

## 📁 Project Structure

```
ANN-Customer-Churn/
│
├── app.py
├── model.h5
├── scaler.pkl
├── onehot_encoder.pkl
├── label_encoder_gender.pkl
├── requirements.txt
├── README.md
│
└── notebook/
    └── ANN_Customer_Churn.ipynb
```

> File names may differ depending on the implementation.

## 💻 Run Locally

Clone the repository:

```bash
git clone <your-github-repository-url>
```

Navigate into the project:

```bash
cd ANN-Customer-Churn
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the Streamlit application:

```bash
streamlit run app.py
```

The application will open in your browser.

## 📦 Model Files

The repository contains the trained model and preprocessing objects required for inference:

* `model.h5` → Trained ANN model
* `scaler.pkl` → Fitted feature scaler
* `onehot_encoder.pkl` → Fitted Geography encoder
* `label_encoder_gender.pkl` → Fitted Gender encoder

Keeping these preprocessing objects is important because the exact transformations learned during training must also be applied to new predictions.

## 🎯 Key Learning Outcomes

Through this project, I worked with:

* Artificial Neural Networks
* TensorFlow/Keras
* Binary classification
* Feature encoding
* Feature scaling
* Model training and validation
* Model serialization
* Real-time inference
* Streamlit application development
* Git/GitHub
* ML model deployment

## 🔮 Future Improvements

Possible improvements include:

* Hyperparameter tuning
* Cross-validation
* Model explainability using SHAP
* Improved UI/UX
* Probability visualization
* Customer churn risk categories
* Model performance dashboard
* Containerization with Docker

## 👨‍💻 Author

**Harshit**

B.Tech CSE (AI & ML)

---

⭐ If you found this project useful, consider giving the repository a star!
