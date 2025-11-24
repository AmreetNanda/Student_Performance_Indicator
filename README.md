# Student Performance Prediction App (Machine Learning + Flask + Docker)

The Student Performance Prediction Web App is an interactive, user-friendly online tool that predicts a student's math exam score based on attributes like reading & writing scores, gender, ethnicity, and parental education. This project demonstrates how machine learning modelS can be integrated with a web interface to provide a smooth, dashboard-like experience.

It includes:

- A complete machine learning pipeline
- A Flask web UI for prediction
- A fully modular ML codebase
- Optional Docker container for deployment

---

## Features

- **Input Form:** Users can enter a student's demographic details, parental education, lunch type, test preparation, and reading/writing scores.  
- **Machine Learning Prediction:** Predicts the Math score based on the given attributes.  
- **Interactive Dashboard:** After submission, the dashboard displays:
  - Predicted Math Score
  - Gauge meter
  - Radar chart comparing Reading, Writing & Math
  - Bar chart and Donut chart of score distribution
- **User-Friendly Interface:** Clean, pastel-colored cards and responsive layout.

---

## Attributes in the Dataset:

- `gender`: Student gender (male/female)  
- `race_ethnicity`: Ethnic group of the student (Group A–E)  
- `parental_level_of_education`: Highest parental education level  
- `lunch`: Lunch type (standard/free-reduced)  
- `test_preparation_course`: Completion status of test prep course  
- `reading_score`: Reading exam score (0–100)  
- `writing_score`: Writing exam score (0–100)  
- `math_score`: Math exam score (predicted)

---

## Technologies Used:

- **Front-End:** HTML, CSS, Chart.js  
- **Back-End:** Python (Flask)  
- **Machine Learning:** Random Forest, Decision Tree, Gradient Boosting, Linear Regression, XBGRegressor, CatBoosting Regressor, Adaboost Regressor

---

## Project Structure

```bash
Student_Performance_Prediction/
│
├── app.py                   # Flask app
├── Template/
│   ├── index.html            # Landing page
│   └── home.html             # Prediction form + Dashboard
├── src/
│   ├── pipeline/
│   │   ├── __init__.py
│   │   ├── predict_pipeline.py
│   │   └── training_pipeline.py
│   ├── components/
│   │   ├── __init__.py
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   ├── Exception.py
│   ├── Logger.py
│   └── Utils.py
├── requirements.txt          # Python dependencies
├── Dockerfile                # Docker container
├── run.sh                    # Optional run script
└── setup.py                  # Optional setup
```
```
## Installation

## 🛠 Installation (without Docker)

### 1. Clone the repo
```bash
git clone https://github.com/AmreetNanda/Student_Performance_Indicator.git
cd Student_Performance_Indicator
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run Flask app
```bash
run app.py
```
Open in your browser:
👉 http://127.0.0.1:5000/
👉 Click on button
👉 Enter student details
👉 click "Predict Math Score" button
👉 Receive the predicted math score of the student with view interactive dashboard

## 🐳 Running with Docker (optional)
### Build the image
```bash
docker build -t student-performance-indicator .
```

### Run the container
```bash
docker run -p 8501:8501 student-performance-indicator
```
Open: 👉 http://localhost:8501


## Screenshots

##### Home page
![App Screenshot](https://github.com/AmreetNanda/Student_Performance_Indicator/blob/main/Student_Performance_Indicator_1.png)

##### Predict page
![App Screenshot](https://github.com/AmreetNanda/Student_Performance_Indicator/blob/main/Student_Performance_Indicator_2.png)

## Demo
https://github.com/user-attachments/assets/a15b3a94-9727-40f2-8556-c8a666fad884

## License

[MIT](https://choosealicense.com/licenses/mit/)
