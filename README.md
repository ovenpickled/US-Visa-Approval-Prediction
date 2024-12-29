# 🌍 US Visa Approval Prediction

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![AWS](https://img.shields.io/badge/AWS-Deployed-FF9900?style=for-the-badge&logo=amazon-aws)](https://aws.amazon.com/)
[![Docker](https://img.shields.io/badge/Docker-Available-2496ED?style=for-the-badge&logo=docker)](https://www.docker.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb)](https://www.mongodb.com/)
[![MIT License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://choosealicense.com/licenses/mit/)

A machine learning system that predicts US visa application outcomes using historical data. The project implements a complete ML pipeline from data ingestion to model deployment with monitoring capabilities.

## 🎯 Project Overview

This project aims to streamline the US visa application process by providing data-driven predictions on visa approval likelihood. The system uses historical visa application data to train machine learning models that can predict the outcome of new applications.

### ✨ Key Features

- End-to-end ML pipeline implementation
- Real-time prediction capabilities
- Automated model training and evaluation
- AWS S3 integration for model and artifact storage
- MongoDB integration for data management
- Docker support for containerization
- Web interface for easy interaction

## 🛠️ Tech Stack

| Category | Technologies |
|----------|--------------|
| Frontend | ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3) |
| Backend | ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python) ![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask) |
| Database | ![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb) |
| ML Libraries | ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy) |
| Cloud | ![AWS](https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazon-aws) |
| DevOps | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions) |

## 🏗️ Project Structure

```
ovenpickled-US-Visa-Approval-Prediction/
├── 📁 us_visa/                  # Main package directory
│   ├── 📁 components/          # Core ML pipeline components
│   ├── 📁 entity/             # Data entities and configurations
│   ├── 📁 cloud_storage/      # AWS S3 integration
│   ├── 📁 pipeline/           # Training and prediction pipelines
│   └── 📁 utils/              # Utility functions
├── 📁 dataset/                # Raw data storage
├── 📁 config/                 # Configuration files
├── 📁 notebook/               # Jupyter notebooks for analysis
└── 📁 templates/              # Web interface templates
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Docker (optional)
- AWS Account (for S3 storage)
- MongoDB Atlas Account

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/ovenpickled-US-Visa-Approval-Prediction.git
cd ovenpickled-US-Visa-Approval-Prediction
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Set up environment variables:
```bash
export AWS_ACCESS_KEY_ID=<your-access-key>
export AWS_SECRET_ACCESS_KEY=<your-secret-key>
export MONGODB_URL=<your-mongodb-url>
```

### Running the Application

#### Using Python
```bash
python app.py
```

#### Using Docker
```bash
docker build -t visa-prediction .
docker run -p 8080:8080 visa-prediction
```

## 🔄 ML Pipeline Components

1. **Data Ingestion** (`data_ingestion.py`)
   - Handles data collection and initial preprocessing
   - Splits data into training and testing sets

2. **Data Validation** (`data_validation.py`)
   - Validates incoming data against predefined schema
   - Ensures data quality and consistency

3. **Data Transformation** (`data_transformation.py`)
   - Feature engineering
   - Data preprocessing and scaling
   - Handles categorical variables

4. **Model Training** (`model_trainer.py`)
   - Trains the ML model using processed data
   - Implements various algorithms and hyperparameter tuning

5. **Model Evaluation** (`model_evaluation.py`)
   - Evaluates model performance
   - Generates performance metrics

6. **Model Pusher** (`model_pusher.py`)
   - Handles model versioning and deployment
   - Pushes models to production

## 📊 Data Analysis

The `notebook/` directory contains Jupyter notebooks with:
- Exploratory Data Analysis (EDA.ipynb)
- Feature Engineering and Model Training experiments

## 🌐 Web Interface

The project includes a web interface for easy interaction:
- Access the application at `http://localhost:8080`
- Upload visa application details
- Get real-time predictions

## 🔧 Configuration

- `config/schema.yaml`: Defines data schema and validation rules
- `config/model.yaml`: Contains model configuration parameters

## 🌐 Live Demo

View the deployed project here:
- **Deployed URL**: [https://us-visa-approval-prediction-s2me.onrender.com/](https://us-visa-approval-prediction-s2me.onrender.com/)

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the terms of the license included in the repository.

## 🙏 Acknowledgments

- Thanks to all contributors who have helped with the development
- Special thanks to the open-source community for the tools and libraries used in this project

## 📞 Contact

For questions and feedback, please open an issue in the repository or contact the maintainers.

---
Made with ❤️ by Aryan