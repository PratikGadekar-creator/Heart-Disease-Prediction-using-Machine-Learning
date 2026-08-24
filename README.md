# Heart-Disease-Prediction-using-Machine-Learning

# ❤️ Heart Disease Prediction using Machine Learning

## 📌 About the Project

I recently started learning Machine Learning, and this is one of the projects I built while learning classification algorithms.

The main goal of this project is to predict whether a person is likely to have heart disease based on different health-related features such as age, blood pressure, cholesterol, chest pain type, maximum heart rate, and other factors.

Along with the ML model, I also created a simple **Streamlit web application** where users can enter their details and get a prediction.

This project helped me understand the complete Machine Learning workflow, from exploring the data to deploying a trained model.

---

## 🔄 What I Did in This Project

The project follows these main steps:

**Data Collection → Data Cleaning → EDA → Preprocessing → Model Training → Model Evaluation → Model Saving → Streamlit Deployment**

### 1. Exploring the Dataset

The dataset contains **918 records and 12 features** related to heart health.

I started by understanding:

* The structure of the dataset
* Data types
* Missing values
* Duplicate records
* Basic statistical information
* Distribution of different features

I also checked for duplicate records, and there were no duplicates in the dataset.

---

## 📊 Exploratory Data Analysis

I used different visualizations to understand the data better, including:

* Histograms
* Count plots
* Box plots
* Violin plots
* Correlation heatmap

For example, I looked at how features such as **Age, RestingBP, Cholesterol, and MaxHR** were distributed.

I also explored the relationship between some features and the target variable `HeartDisease`.

---

## 🧹 Data Preprocessing

While exploring the dataset, I found some `0` values in columns such as `Cholesterol` and `RestingBP`.

Instead of keeping those values, I replaced them with the mean calculated from the non-zero values.

For categorical variables such as `Sex`, `ChestPainType`, `RestingECG`, and others, I used one-hot encoding with `drop_first=True`.

I then split the data into training and testing sets and used `StandardScaler` to scale the features.

---

## 🤖 Machine Learning Models

Since this is a classification problem, I experimented with several classification algorithms:

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Gaussian Naive Bayes
* Decision Tree
* Support Vector Machine (SVM)

I evaluated the models using **Accuracy and F1 Score**.

After comparing the models, I used the **KNN model** for the Streamlit application.

---

## 🌐 Streamlit Web Application

After training the model, I wanted to take the project one step further instead of only keeping it inside a Jupyter/Colab notebook.

So I created a simple Streamlit interface.

The user can enter:

* Age
* Sex
* Chest Pain Type
* Resting Blood Pressure
* Cholesterol
* Fasting Blood Sugar
* Resting ECG
* Maximum Heart Rate
* Exercise-Induced Angina
* Oldpeak
* ST Slope

When the user clicks **Predict**, the application:

1. Takes the user's input
2. Converts it into the same feature format used during training
3. Applies the saved scaler
4. Loads the trained KNN model
5. Makes a prediction
6. Displays the result on the screen

The application shows either:

**✅ Low Risk of Heart Disease**

or

**⚠️ High Risk of Heart Disease**

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* Streamlit

---

## 📁 Project Structure

```text
Heart-Disease-Prediction/
│
├── data/
│   └── heart.csv
│
├── notebook/
│   └── Heart_Disease_Prediction.ipynb
│
├── app/
│   └── app.py
│
├── models/
│   ├── knn_heart_model.pkl
│   ├── heart_scaler.pkl
│   └── heart_columns.pkl
│
├── screenshots/
│   └── streamlit_app.png
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## ▶️ How to Run the Project

First, clone the repository:

```bash
git clone <your-repository-url>
```

Move into the project folder:

```bash
cd Heart-Disease-Prediction
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

Run the Streamlit application:

```bash
streamlit run app/app.py
```

---

## 💡 What I Learned

This project was mainly about learning by actually building something.

While working on it, I got more comfortable with:

* Understanding a real dataset
* Performing EDA
* Handling data issues
* Encoding categorical variables
* Feature scaling
* Splitting data into training and testing sets
* Training different classification models
* Comparing ML models
* Saving trained models using Joblib
* Connecting a trained ML model with a frontend
* Building a simple ML application using Streamlit

It also helped me understand that building an ML project isn't just about training a model — you also need to think about how the model will actually be used.

---

## 🚀 Future Improvements

There are still several things I want to improve in this project:

* Hyperparameter tuning
* Cross-validation
* Adding a confusion matrix
* Adding precision, recall and ROC-AUC
* Improving the Streamlit UI
* Deploying the application online
* Improving the model performance

---

## ⚠️ Disclaimer

This project was created for **learning and educational purposes**.

The predictions from this application should not be treated as medical advice or used as a replacement for professional medical diagnosis.
