
# AI-Driven Solar & Wind Prediction Platform

A full-stack machine-learning platform designed to predict **solar and wind energy potential**, evaluate renewable-energy candidate sites, and compare locations using environmental, geographic, infrastructure, and site-suitability factors.

## ✨ Key Features

- **AI-Powered Energy Prediction**: Predicts annual solar and wind energy generation for candidate locations.
- **Random Forest Regression**: Uses separate Random Forest regression models for solar and wind energy prediction.
- **Multiple Candidate Sites**: Allows users to create projects and add multiple locations for analysis.
- **Site Suitability Analysis**: Evaluates locations using renewable resources, geographic conditions, infrastructure accessibility, environmental impact, and economic feasibility.
- **Site Comparison & Ranking**: Compares multiple candidate locations and ranks them based on their suitability.
- **Interactive Dashboard**: Displays project information, energy predictions, suitability scores, and site comparisons.
- **Analytics & Visualization**: Provides charts for solar energy, wind energy, and predicted renewable-energy results.
- **ML Prediction Dashboard**: Displays model information, input features, predictions, and evaluation metrics.
- **User Authentication**: Supports user registration and login.
- **Project Management**: Allows users to create projects and manage multiple candidate sites.
- **Reports**: Provides structured analysis of projects and candidate locations.

## 🤖 Machine Learning

The platform uses two separate **Random Forest Regression** models:

- **Solar Random Forest Model** – Predicts annual solar energy generation.
- **Wind Random Forest Model** – Predicts annual wind energy generation.

The models use site features including:

- Solar irradiance
- Wind speed
- Wind direction
- Temperature
- Rainfall
- Cloud cover
- Elevation
- Slope
- Vegetation index
- Land area
- Latitude and longitude
- Distance to roads
- Distance to transmission infrastructure

The prediction workflow is:

```text
Site Information
       ↓
Feature Processing
       ↓
Solar Random Forest → Solar Energy Prediction
       +
Wind Random Forest  → Wind Energy Prediction
       ↓
Total Predicted Renewable Energy
````

## 📊 Site Suitability Analysis

The platform evaluates each candidate location using a weighted suitability model:

| Factor                          | Weight |
| ------------------------------- | -----: |
| Renewable Resource Availability |    35% |
| Geographic Suitability          |    25% |
| Infrastructure Accessibility    |    15% |
| Environmental Impact            |    15% |
| Economic Feasibility            |    10% |

The weighted factors are combined to calculate an **overall site suitability score**, which is used for comparing and ranking candidate locations.

## 💡 How It Works

1. **Project Creation**: The user creates a renewable-energy project.
2. **Site Registration**: Multiple candidate locations can be added to the project.
3. **Data Entry**: The user enters geographic, environmental, renewable-resource, land, and infrastructure information.
4. **ML Prediction**: The solar and wind Random Forest models analyse the site information and generate energy predictions.
5. **Suitability Analysis**: The system calculates the overall suitability score.
6. **Site Comparison**: Candidate locations are compared using their energy and suitability results.
7. **Site Ranking**: Locations are ranked according to their suitability.
8. **Result Visualization**: Results are displayed through the dashboard, recommendations, analytics, and reports.

## 🖥️ Application Modules

* **Dashboard** – Provides an overview of projects, sites, predictions, and analysis.
* **Projects & Sites** – Create projects and register multiple candidate locations.
* **Recommendations** – Compare and rank candidate sites.
* **Analytics** – Visualize solar, wind, and renewable-energy results.
* **ML Prediction** – View machine-learning models, inputs, predictions, and evaluation metrics.
* **Reports** – View structured project and site analysis.
* **Profile** – Manage and view user account information.

## 🛠 Tech Stack

* **Frontend**: React.js, Vite, JavaScript, HTML5, CSS3, Tailwind CSS
* **Backend / API**: Python, FastAPI, Uvicorn, REST API
* **Machine Learning**: Scikit-learn, Random Forest Regression, Joblib
* **Data Processing**: Pandas, NumPy
* **Database**: SQLite
* **Authentication**: JWT
* **Data Visualization**: Recharts
* **Icons**: Lucide React

## 📁 Directory Structure

```text
Solar-and-Wind-prediction/
│
└── Solar_and_Wind_Prediction/
    │
    ├── backend/
    │   ├── README.md
    │   ├── auth.py
    │   ├── database.py
    │   ├── main.py
    │   ├── ml_models.py
    │   └── requirements.txt
    │
    ├── frontend/
    │   ├── src/
    │   │   ├── main.jsx
    │   │   └── styles.css
    │   ├── README.md
    │   ├── index.html
    │   ├── package-lock.json
    │   └── package.json
    │
    ├── docs/
    │
    ├── README.md
    ├── RUN_FIRST.txt
    └── .gitignore
```

## 🔄 System Workflow

```text
User
 ↓
Registration / Login
 ↓
Create Project
 ↓
Add Candidate Sites
 ↓
Enter Site Information
 ↓
Machine Learning Prediction
 ├── Solar Random Forest
 └── Wind Random Forest
 ↓
Energy Predictions
 ↓
Site Suitability Scoring
 ↓
Candidate Site Comparison
 ↓
Site Ranking
 ↓
Dashboard & Analytics
 ↓
Decision Support
```

## 📈 Model Evaluation

The regression models are evaluated using **R² (R-squared)** on held-out test data.

Current development results:

* **Solar Model R²:** 0.978
* **Wind Model R²:** 0.993

R² measures how well the model explains the variation in the target energy values.

## 🎯 Project Outcome

The platform combines **machine learning, renewable-energy prediction, geographic analysis, environmental assessment, infrastructure analysis, and multi-factor site suitability scoring** into a single web application.

It provides users with a structured way to analyse candidate locations, predict their solar and wind energy potential, compare sites, and support renewable-energy deployment planning.

