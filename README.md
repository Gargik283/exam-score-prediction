# 🎓 Exam Score Prediction using XGBoost

A machine learning web application that predicts a student's **exam score** based on study habits, class attendance, sleep patterns, study method, and facility rating.

The application is built using **Python, XGBoost, Pandas, Pickle, and Streamlit** and provides an interactive interface where users can enter student details and receive an estimated exam score.

---

## 📌 Project Overview

Student academic performance can be influenced by several factors such as study hours, class attendance, sleep, study methods, and learning environment.

This project uses a trained **XGBoost regression model** to predict a student's exam score from selected academic and lifestyle features.

The trained model and label encoders are saved as `.pkl` files and loaded by the Streamlit application to make real-time predictions.

---

## 🚀 Features

* Interactive Streamlit web interface
* Exam score prediction using XGBoost
* Numerical input using sliders
* Categorical input using dropdown menus
* Pre-trained XGBoost model loaded from a pickle file
* Label encoders loaded from a pickle file
* Real-time prediction
* Simple and user-friendly interface
* Error handling for missing model or encoder files

---

## 🛠️ Technologies Used

* **Python**
* **Streamlit**
* **Pandas**
* **XGBoost**
* **Pickle**
* **Machine Learning**
* **Git & GitHub**

---

## 📊 Dataset

The project uses the `Exam_Score_Prediction.csv` dataset.

### Dataset Information

* **Records:** 20,000
* **Features:** 13
* **Target Variable:** `exam_score`

### Dataset Columns

| Column             | Description                                |
| ------------------ | ------------------------------------------ |
| `student_id`       | Unique identifier for each student         |
| `age`              | Student's age                              |
| `gender`           | Student's gender                           |
| `course`           | Student's course                           |
| `study_hours`      | Number of hours spent studying             |
| `class_attendance` | Class attendance percentage                |
| `internet_access`  | Availability of internet access            |
| `sleep_hours`      | Average sleep duration                     |
| `sleep_quality`    | Quality of sleep                           |
| `study_method`     | Preferred study method                     |
| `facility_rating`  | Rating of available educational facilities |
| `exam_difficulty`  | Difficulty level of the examination        |
| `exam_score`       | Student's exam score                       |

---

## 🤖 Machine Learning Model

The project uses **XGBoost** for exam score prediction.

XGBoost is a gradient boosting algorithm that performs well on structured and tabular datasets.

The trained model is stored as:

```text
xgb_tuned_model.pkl
```

Categorical variables used by the application are transformed using previously trained label encoders stored as:

```text
label_encoders.pkl
```

---

## 🎯 Prediction Features

The Streamlit application uses the following features as model inputs:

### Numerical Features

* Study Hours
* Class Attendance
* Sleep Hours

### Categorical Features

* Sleep Quality
* Study Method
* Facility Rating

The categorical features are converted into numerical values using the saved label encoders before being passed to the XGBoost model.

---

## 🖥️ Application Workflow

```text
User Input
    ↓
Streamlit Interface
    ↓
Categorical Feature Encoding
    ↓
Input DataFrame Creation
    ↓
Trained XGBoost Model
    ↓
Exam Score Prediction
    ↓
Predicted Exam Score
```

---

## 📂 Project Structure

```text
Exam-Score-Prediction/
│
├── app.py
├── Exam_Score_Prediction.csv
├── xgb_tuned_model.pkl
├── label_encoders.pkl
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git
```

Move into the project directory:

```bash
cd YOUR-REPOSITORY-NAME
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

### 3. Activate the Virtual Environment

#### Windows

```bash
venv\Scripts\activate
```

#### macOS / Linux

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 📦 Requirements

The `requirements.txt` file should contain the libraries required to run the application:

```text
streamlit
pandas
xgboost
```

`pickle` does not need to be installed separately because it is included in Python's standard library.

---

## ▶️ Run the Application

After installing the dependencies, run:

```bash
streamlit run app.py
```

The Streamlit application will open in your browser.

---

## 🧪 How to Use

1. Launch the Streamlit application.
2. Enter the student's **Study Hours**.
3. Select the student's **Class Attendance**.
4. Enter the student's **Sleep Hours**.
5. Select the appropriate **Sleep Quality**.
6. Select the student's **Study Method**.
7. Select the **Facility Rating**.
8. Click **Predict Exam Score**.
9. The application displays the predicted exam score.

Example output:

```text
Predicted Exam Score: 78.42
```

---

## 🔐 Model & Encoder Files

The application requires the following trained files:

```text
xgb_tuned_model.pkl
label_encoders.pkl
```

These files must be present in the same directory as `app.py`.

The application loads them using Python's `pickle` module.

```python
with open('xgb_tuned_model.pkl', 'rb') as f:
    xgb_tuned = pickle.load(f)

with open('label_encoders.pkl', 'rb') as f:
    label_encoders = pickle.load(f)
```

---

## 🧠 Key Machine Learning Concepts Demonstrated

This project demonstrates practical knowledge of:

* Supervised Machine Learning
* Regression
* XGBoost
* Feature preprocessing
* Label encoding
* Model serialization using Pickle
* Prediction pipelines
* Pandas DataFrames
* Streamlit application development
* Model deployment concepts

---

## 📈 Future Improvements

Possible improvements include:

* Add model evaluation metrics such as MAE, MSE, RMSE, and R²
* Display model performance on the Streamlit interface
* Add exploratory data analysis
* Add prediction history
* Add visualizations for important features
* Add feature importance using XGBoost
* Improve UI design
* Deploy the application using Streamlit Community Cloud
* Add input validation
* Add support for additional student features

---

## 🌐 Deployment

The application can be deployed using **Streamlit Community Cloud**.

The GitHub repository should contain:

```text
app.py
xgb_tuned_model.pkl
label_encoders.pkl
requirements.txt
README.md
```

After connecting the GitHub repository to Streamlit Community Cloud, select `app.py` as the main application file.

---

## ⚠️ Disclaimer

This project is intended for **educational and demonstration purposes**.

The predicted exam score is an estimate generated by a machine learning model and should not be considered an official academic evaluation.

---

## 👩‍💻 Author

**Gargi Kundu**

B.Tech — Electronics and Communication Engineering (VLSI Design)

Interested in **Data Analytics, Machine Learning, Python, SQL, and Business Intelligence**.

---

## ⭐ Project Highlights

* Built an end-to-end machine learning prediction application.
* Used **XGBoost** for regression-based exam score prediction.
* Implemented categorical feature encoding using saved label encoders.
* Serialized and loaded trained ML artifacts using Pickle.
* Developed an interactive prediction interface using Streamlit.
* Structured the project for GitHub and deployment.

---

## 📄 License

This project is created for educational and portfolio purposes.
