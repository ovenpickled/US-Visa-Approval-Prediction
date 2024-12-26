# US Visa Approval Prediction

A machine learning project to predict US visa application approval outcomes using historical visa application data.

## Project Overview

This project implements an end-to-end machine learning pipeline for predicting whether a US visa application will be approved or denied. The system uses historical visa application data to train various models and make predictions on new applications.

## Features

- Complete ML pipeline implementation including:
  - Data ingestion from multiple sources
  - Data validation and cleaning
  - Data transformation and feature engineering
  - Model training with multiple algorithms
  - Model evaluation and selection
  - Model deployment and prediction pipeline
- Logging and exception handling
- FastAPI-based REST API for predictions
- Docker containerization support
- Comprehensive testing and validation

## Tech Stack

- Python 3.x
- Machine Learning Libraries:
  - scikit-learn
  - XGBoost
  - CatBoost
  - imbalanced-learn
- Data Processing:
  - Pandas
  - NumPy
  - SciPy
- Visualization:
  - Matplotlib
  - Seaborn
  - Plotly
- MLOps Tools:
  - Evidently (for model monitoring)
  - MongoDB (for data storage)
  - AWS S3 (for artifact storage)
- Web Framework:
  - FastAPI
  - Uvicorn
- Others:
  - PyYAML (configuration management)
  - dill (object serialization)
  - from_root (path management)

## Project Structure

```
└── us_visa/
    ├── components/           # Core ML pipeline components
    ├── configuration/        # Configuration management
    ├── constants/           # Project constants
    ├── entity/              # Data entities and artifacts
    ├── exception/           # Custom exception handling
    ├── logger/              # Logging functionality
    ├── pipeline/            # Training and prediction pipelines
    └── utils/               # Utility functions
```

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

1. Training Pipeline:
```python
from us_visa.pipeline.training_pipeline import TrainPipeline

pipeline = TrainPipeline()
pipeline.run_pipeline()
```

2. Prediction Pipeline:
```python
from us_visa.pipeline.prediction_pipeline import PredictionPipeline

pipeline = PredictionPipeline()
prediction = pipeline.make_prediction(input_data)
```

3. API Service:
```bash
uvicorn app:app --reload
```

## Docker Support

Build and run the Docker container:

```bash
docker build -t us-visa-prediction .
docker run -p 8000:8000 us-visa-prediction
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

- **Aryan**
- Email: aryanghate29@gmail.com

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request