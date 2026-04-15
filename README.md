# 🛡️ Network Security Phishing Detection (End-to-End MLOps)

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.9+-blue.svg" alt="Python Version">
  <img src="https://img.shields.io/badge/FastAPI-0.100+-009688.svg?logo=fastapi" alt="FastAPI">
  <img src="https://img.shields.io/badge/MongoDB-Atlas-47A248.svg?logo=mongodb" alt="MongoDB">
  <img src="https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-F7931E.svg?logo=scikit-learn" alt="Scikit-Learn">
  <img src="https://img.shields.io/badge/Status-Production%20Ready-success.svg" alt="Status">
</div>

<br>

##  Project Overview
This project is an **End-to-End MLOps Pipeline** designed to detect and classify phishing websites based on network security and structural data. It features a fully automated pipeline for data ingestion, preprocessing, model training, and a high-performance **FastAPI backend** for bulk batch predictions.

---

##  Key Features
* **Automated Data Pipeline:** Fetches raw data securely from MongoDB Atlas.
* **Robust Preprocessing:** Handles missing values, scaling, and feature engineering automatically via serialized `.pkl` pipelines.
* **Batch Inference:** Upload a `.csv` file with thousands of records, and the system processes it instantly.
* **Optimized UI Rendering:** Prevents browser crashes by returning a lightweight HTML preview (Top 20 rows) while securely saving the complete prediction dataset locally.

---

##  How to Run This Project Locally

Follow these steps to set up and run the project on your local machine.

### Prerequisites
Make sure you have the following installed:
* [Python 3.9+](https://www.python.org/downloads/)
* [Git](https://git-scm.com/)
* A MongoDB Atlas account (or local MongoDB server)

### Step 1: Clone the Repository
Bash
git clone [https://github.com/your-username/network-security-mlops-pipeline.git](https://github.com/your-username/network-security-mlops-pipeline.git)
cd network-security-mlops-pipeline

### Step 2: Create a Virtual Environment
Using a virtual environment ensures clean dependency management.

Bash
# Using Python venv
python -m venv venv

# Activate the environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

### Step 3: Install Dependencies
Bash
pip install -r requirements.txt

### Step 4: Configure Environment Variables
The system requires a database connection string. Create a .env file in the root directory:

Bash
# Create the file (Linux/Mac)
touch .env

Open the .env file and add your secure MongoDB connection URL:

Code snippet
MONGODB_URL_KEY="mongodb+srv://<username>:<password>@cluster0.mongodb.net/?retryWrites=true&w=majority"