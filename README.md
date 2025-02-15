# Student Performance Prediction

## Overview
This project predicts students' math scores based on various features such as gender, race/ethnicity, parental education, lunch type, and test preparation. It is built using machine learning and follows an end-to-end data pipeline, including data ingestion, transformation, model training, and prediction.

## Features
- **Data Ingestion**: Loads and splits the dataset.
- **Data Transformation**: Applies feature engineering and preprocessing.
- **Model Training**: Trains multiple machine learning models and selects the best one.
- **Prediction Pipeline**: Makes predictions based on new student data.
- **Flask Web App**: Provides a user-friendly interface for predictions.
- **AWS Deployment Ready**: Configured for easy deployment on AWS.

## Technologies Used
- Python
- Pandas, NumPy, Scikit-learn
- Flask (for web app)
- CatBoost, XGBoost, RandomForest
- AWS (for deployment readiness)

## Project Structure
```
├── artifacts/                # Contains model and preprocessor files
├── notebooks/                # Jupyter notebooks for EDA and training
├── src/                      # Source code
│   ├── components/           # Data processing and model scripts
│   ├── pipelines/            # Training and prediction pipelines
│   ├── exception.py          # Custom exception handling
│   ├── logger.py             # Logging setup
│   ├── utils.py              # Utility functions
├── templates/                # HTML files for Flask app
├── static/                   # Static assets (CSS, JS)
├── application.py            # Flask application entry point
├── requirements.txt          # Dependencies list
├── README.md                 # Project documentation
```

## How to Run Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo.git
   cd your-repo
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the application:
   ```bash
   python application.py
   ```
4. Open `http://127.0.0.1:5000/` in your browser.

## Deployment on AWS
The project is **AWS deployment ready**. To deploy:
1. **Create an EC2 instance** (Ubuntu or Amazon Linux).
2. **Transfer project files** using SCP or Git.
3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
4. **Run the Flask app** using Gunicorn or a similar WSGI server:
   ```bash
   gunicorn --bind 0.0.0.0:5000 application:app
   ```
5. **Configure AWS security groups** to allow traffic on port 5000.
6. **Use an Elastic Load Balancer** (optional) for scalability.

## Author
**Sanket Yuvraj Wagh**  
Data Scientist | AI Enthusiast  
Vyara, Gujarat, India  

## License
This project is licensed under the MIT License.

