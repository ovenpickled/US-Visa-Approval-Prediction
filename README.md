# US Visa Approval Prediction

A machine learning project that predicts US visa application outcomes using historical visa application data through an automated ML pipeline with MLOps best practices.

## Project Overview

This project implements an end-to-end machine learning solution for predicting US visa application approvals. It uses historical visa application data to train various ML models and provides predictions through a FastAPI service. The system includes comprehensive MLOps practices such as data validation, model monitoring, and containerized deployment.

## Features

- Complete ML Pipeline:
  - Automated data ingestion from MongoDB
  - Data validation and quality checks
  - Feature engineering and transformation
  - Model training and hyperparameter tuning
  - Model evaluation and selection
  - Automated model deployment
- Production-ready API service using FastAPI
- Comprehensive logging and exception handling
- Docker containerization
- Model monitoring using Evidently
- Cloud storage integration (AWS S3)

## Directory Structure

```
└── ovenpickled-US-Visa-Approval-Prediction/
    ├── us_visa/                     # Main package directory
    │   ├── components/              # ML pipeline components
    │   ├── data_access/            # Database interaction modules
    │   ├── configuration/          # System configuration
    │   ├── constants/              # Project constants
    │   ├── entity/                 # Data entities
    │   ├── exception/              # Custom exception handling
    │   ├── logger/                 # Logging functionality
    │   ├── pipeline/               # Training and prediction pipelines
    │   └── utils/                  # Utility functions
    ├── dataset/                    # Raw data storage
    ├── notebook/                   # Jupyter notebooks for EDA
    ├── config/                     # Configuration files
    └── [Other root level files]    # Setup and deployment files
```

## Tech Stack

- **Programming Language:** Python 3.x
- **ML Libraries:**
  - scikit-learn
  - XGBoost
  - CatBoost
  - imbalanced-learn
- **Data Processing:**
  - Pandas
  - NumPy
  - SciPy
- **Visualization:**
  - Matplotlib
  - Seaborn
  - Plotly
- **MLOps Tools:**
  - Evidently (Model Monitoring)
  - MongoDB (Data Storage)
  - AWS S3 (Artifact Storage)
- **Web Framework:** FastAPI
- **Others:**
  - PyYAML (Configuration)
  - dill (Serialization)
  - Docker (Containerization)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/ovenpickled/US-Visa-Approval-Prediction.git
cd US-Visa-Approval-Prediction
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or
venv\Scripts\activate     # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Install the package in development mode:
```bash
pip install -e .
```

## Usage

### Training Pipeline

Run the training pipeline:
```python
from us_visa.pipeline.training_pipeline import TrainPipeline

pipeline = TrainPipeline()
pipeline.run_pipeline()
```

### API Service

Start the FastAPI service:
```bash
uvicorn app:app --reload
```

### Docker Deployment

Build and run using Docker:
```bash
docker build -t us-visa-prediction .
docker run -p 8000:8000 us-visa-prediction
```

## Environment Variables

Create a `.env` file in the root directory with:
```
MONGODB_URL=your_mongodb_connection_string
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
```

## Project Notebooks

- `notebook/EDA.ipynb`: Exploratory Data Analysis
- `notebook/Feature Engineering and Model Training.ipynb`: Feature development and initial model experiments

## Contributing

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/YourFeature`
3. Commit your changes: `git commit -m 'Add YourFeature'`
4. Push to the branch: `git push origin feature/YourFeature`
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

- **Aryan**
- Email: aryanghate29@gmail.com

## Acknowledgments

- Thanks to all contributors who have helped with the development
- Special thanks to the open-source community for the tools and libraries used in this project