# 🛡️ network-security-mlops-pipeline

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.9+-blue.svg" alt="Python Version">
  <img src="https://img.shields.io/badge/FastAPI-0.100+-009688.svg?logo=fastapi" alt="FastAPI">
  <img src="https://img.shields.io/badge/DagsHub-MLOps-65ADF1.svg?logo=dagshub" alt="DagsHub">
  <img src="https://img.shields.io/badge/MLflow-Tracking-0194E2.svg?logo=mlflow" alt="MLflow">
  <img src="https://img.shields.io/badge/MongoDB-Atlas-47A248.svg?logo=mongodb" alt="MongoDB">
  <img src="https://img.shields.io/badge/Status-Production%20Ready-success.svg" alt="Status">
</div>

<br>

##  Project Overview
This is a professional **End-to-End MLOps Pipeline** built to detect phishing websites. It leverages **DagsHub** for experiment tracking and data versioning, ensuring a reproducible and collaborative machine learning environment. The project automates everything from MongoDB data ingestion to bulk inference via a **FastAPI** backend.

---

##  Advanced MLOps Features
* **Experiment Tracking (MLflow):** Integrated with DagsHub to track model metrics, parameters, and artifacts in real-time.
* **Data Versioning (DVC):** Uses DagsHub as a remote storage for handling large datasets without bloating the Git repository.
* **Modular Pipeline:** Separate components for Ingestion, Transformation, and Training following SOLID principles.
* **Optimized Batch Inference:** Processes thousands of records and provides a lightweight 20-row UI preview while saving full results in `prediction_output/`.

---

##  Tech Stack
* **Language:** Python 3.9+
* **Framework:** FastAPI
* **Database:** MongoDB Atlas
* **MLOps Tools:** DagsHub, MLflow, DVC
* **ML Libraries:** Scikit-Learn, Pandas, NumPy
* **Logging:** Custom Exception & Centralized Logger

---

##  Project Workflow

1.  **Ingestion:** Data is pulled from MongoDB Atlas via secure TLS.
2.  **Versioning:** Datasets are tracked using **DVC** with DagsHub as the remote backend.
3.  **Transformation:** Data cleaning and feature scaling via a serialized preprocessing pipeline.
4.  **Training & Tracking:** Models are trained, and performance metrics are logged to **MLflow on DagsHub**.
5.  **Inference:** The FastAPI `/predict` route handles CSV uploads and returns phishing predictions.

---

##  Installation & Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/Tulsi14/network-security-mlops-pipeline.git](https://github.com/Tulsi14/network-security-mlops-pipeline.git)
cd network-security-mlops-pipeline
```

### Step 2: Create a Virtual Environment
Using a virtual environment ensures clean dependency management.

```bash
# Using Python venv
python -m venv venv

# Activate the environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### Step 3: Install Dependencies
```Bash
pip install -r requirements.txt
```

### Step 4: Configure Environment Variables
The system requires a database connection string. Create a .env file in the root directory:


```Bash
# Create the file (Linux/Mac)
touch .env
```

### Open the .env file and add your secure MongoDB connection URL:

``` Code snippet
MONGODB_URL_KEY="mongodb+srv://<username>:<password>@cluster0.mongodb.net/?retryWrites=true&w=majority"
```