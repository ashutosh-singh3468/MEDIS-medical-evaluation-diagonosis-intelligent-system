# MEDIS - Medical Diagnosis Prediction System

## Description
MEDIS is a Medical Diagnosis Prediction System that aims to assist users in identifying potential diseases based on their symptoms. 

The system utilizes machine learning models and provides treatment recommendations.

## Project Components
The project consists of the following main components:

-   **Frontend:** User interface for interacting with the system (developed by other team members).
-   **Backend:** Handles API requests, server logic, and database interaction.
-   **Machine Learning:** Contains models and scripts for disease prediction.
-   **Recommendations:** Provides treatment and medicine recommendations.
-   **Database:** Stores user history and other necessary data.
-   **Configuration & Logging:** Project configuration and error logging.

## Project Structure
```
MEDIS/
├── frontend/                    # A's Work - Frontend Development
│   ├── templates/              # HTML templates
│   ├── static/                 # CSS, JS, images
│   ├── server.py              # Flask server
│   └── auth/                  # Authentication
│
├── backend/                    # B's Work - Backend Development
│   ├── api/                   # API endpoints
│   ├── routes/               # Route handlers
│   └── app.py                # Main backend app
│
├── ml/                        # J's Work - ML & Disease Prediction
│   ├── models/               # ML models
│   │   ├── disease_prediction_v2.py
│   │   ├── model_training.py
│   │   └── generate_models.py
│   ├── data/                 # Data processing
│   │   ├── data_ingestion.py
│   │   ├── datatransformation.py
│   │   ├── fix_dataset.py
│   │   └── extract_symptoms.py
│   └── tests/                # ML tests
│       ├── test_symptoms.py
│       ├── test_prediction.py
│       └── test_cases.py
│
├── recommendations/           # M's Work - Treatment Recommendations
│   ├── models/
│   │   ├── integrated_recommendation_model.py
│   │   └── medicine_recommendation.py
│   ├── data/
│   │   ├── merge_diseases.py
│   │   └── merge_new_diseases.py
│   └── tests/
│       └── test_recommendations.py
│
├── database/                  # Shared - Database
│   ├── models.py
│   ├── init_db.py
│   └── user_history.db
│
├── config/                    # Shared - Configuration
│   └── config.py
│
├── logs/                      # Shared - Logs
│   └── error.log
│
├── requirements.txt           # Shared - Dependencies
└── README.md                 # Shared - Documentation
```

## Features
- Disease prediction with confidence scoring
- Comprehensive disease profiles
- Age-specific symptom analysis
- Seasonal factor consideration
- Treatment recommendations
- Prevention guidelines
- Complication warnings

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/MEDIS.git
cd MEDIS
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### Running the System
```python
from ml.models.disease_prediction_v2 import predict_diseases

# Example usage
symptoms = ["fever", "cough", "fatigue"]
age_group = "ADULT"  # Options: INFANT, CHILD, TEEN, ADULT, ELDERLY
season = "SUMMER"    # Options: SUMMER, WINTER, MONSOON, SPRING

predictions = predict_diseases(symptoms, age_group, season)
```
## Contributing
1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## Disclaimer
This system is designed to assist in preliminary diagnosis and should not replace professional medical advice. Always consult with healthcare professionals for proper medical diagnosis and treatment.
