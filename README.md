 PrognosAI

AI-Based Predictive Maintenance & Health Prognostics System

 Project Overview

PrognosAI is an AI-driven prognostics and health management (PHM) system designed to predict the health status and degradation trends of complex systems using time-series sensor data.
The project leverages deep learning (GRU – Gated Recurrent Units) trained on the NASA C-MAPSS dataset to model failure patterns and enable early fault prediction.

This system is particularly applicable to predictive maintenance, where timely detection of degradation can reduce downtime, maintenance costs, and unexpected failures.

 Dataset Used
NASA C-MAPSS (Commercial Modular Aero-Propulsion System Simulation)

Public benchmark dataset provided by NASA

Simulates degradation of aircraft engines

Contains multivariate time-series sensor data

Widely used in Remaining Useful Life (RUL) and predictive maintenance research

Subsets used in this project:

FD001

FD002

FD003

FD004

Each subset represents different operating conditions and fault modes.

 System Architecture (High Level)

Data Ingestion

Load raw sensor data from NASA C-MAPSS dataset

Preprocessing

Data cleaning

Normalization using scalers

Time-window segmentation

Model Inference

GRU model captures temporal degradation patterns

Predicts system health trends

Health Evaluation

Threshold-based logic to classify health status

Backend Interface

Modular backend code for loading models, preprocessing, and prediction

🧩 Project Structure
backend/
│
├── app.py                 # Backend entry point
├── data_loader.py         # Dataset loading logic
├── preprocessing.py       # Data preprocessing pipeline
├── model_loader.py        # Loads trained GRU model & scaler
├── predictor.py           # Prediction logic
├── threshold.py           # Health status classification
├── requirements.txt       # Project dependencies
│
├── data/                  # Dataset files
├── models/                # Trained GRU models
├── scalers/               # Saved scalers
│
├── fd001.ipynb            # Training & experiments (FD001)
├── fd002.ipynb            # Training & experiments (FD002)
├── fd003.ipynb            # Training & experiments (FD003)
├── fd004.ipynb            # Training & experiments (FD004)

 Machine Learning Model

Model Type: Gated Recurrent Unit (GRU)

Reason for GRU:

Efficient for time-series data

Captures long-term dependencies

Less complex than LSTM while maintaining performance

 Tech Stack

Programming Language: Python

ML / DL: NumPy, Pandas, Scikit-learn

Deep Learning: GRU (Recurrent Neural Network)

Data Handling: Time-series preprocessing & scaling

Backend: Python-based modular backend

Version Control: Git & GitHub

🚀 How to Run the Project
1️⃣ Clone the Repository
git clone https://github.com/nikita09-lab/Nikita_project_submission.git
cd Nikita_project_submission/backend
