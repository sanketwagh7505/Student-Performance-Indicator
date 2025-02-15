# Student Performance Prediction

## Overview
This project predicts student performance based on various features such as gender, parental education level, lunch type, test preparation course, and scores in reading and writing. It uses machine learning models to analyze the data and provide predictions.

## Project Structure
```
Student_Performance_Prediction/
│── src/
│   ├── components/
│   │   ├── __init__.py
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   ├── model_trainer.py
│   ├── pipelines/
│   │   ├── __init__.py
│   │   ├── predict_pipeline.py
│   │   ├── train_pipeline.py
│   ├── exception.py
│   ├── logger.py
│   ├── utils.py
│── notebook/
│   ├── data/
│   │   ├── stud.csv
│   ├── 1. EDA STUDENT PERFORMANCE.ipynb
│   ├── 2. MODEL TRAINING.ipynb
│── artifacts/
│   ├── data.csv
│   ├── model.pkl
│   ├── preprocessor.pkl
│   ├── test_data.csv
│   ├── train_data.csv
│── templates/
│   ├── home.html
│   ├── index.html
│── application.py
│── README.md
```

## Components
### 1. Data Ingestion (`data_ingestion.py`)
- Reads the student dataset from `notebook/data/stud.csv`.
- Splits the data into training and testing sets.
- Stores the split datasets in the `artifacts` directory.

### 2. Data Transformation (`data_transformation.py`)
- Handles missing values and categorical encoding.
- Standardizes numerical features.
- Saves the preprocessing object as `preprocessor.pkl`.

### 3. Model Training (`model_trainer.py`)
- Trains multiple regression models including RandomForest, DecisionTree, GradientBoosting, XGBoost, CatBoost, and AdaBoost.
- Selects the best model based on R² score.
- Saves the trained model as `model.pkl`.

### 4. Prediction Pipeline (`predict_pipeline.py`)
- Loads the trained model and preprocessor.
- Takes input from a web form, processes it, and makes predictions.

### 5. Flask Web Application (`application.py`)
- Provides a web interface to input student data.
- Displays the predicted student performance.

## Installation
### Prerequisites
- Python 3.8+
- Flask
- Scikit-learn
- Pandas
- NumPy
- CatBoost
- XGBoost

### Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo-link
   cd Student_Performance_Prediction
   ```
2. Create a virtual environment:
   ```sh
   python -m venv venv
   source venv/bin/activate  # For Linux/macOS
   venv\Scripts\activate  # For Windows
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Run the application:
   ```sh
   python application.py
   ```

## Usage
- Navigate to `http://127.0.0.1:5000/` in your browser.
- Enter student details in the form.
- Click "Predict" to get the performance prediction.

## Author
**Sanket Yuvraj Wagh**  
Fresher in Data Science  

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

