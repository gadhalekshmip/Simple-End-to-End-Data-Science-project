# End-to-End Data Science Project

This README provides a guide to set up, develop, and deploy an end-to-end data science project pipeline. The workflow includes data ingestion, transformation, training, and evaluation, with a focus on reproducibility and tracking.

---

## **ML Pipeline Workflow**
1. **Data Ingestion**: Collect and validate raw data.
2. **Data Transformation**: Clean and preprocess the data.
3. **Model Trainer**: Train the machine learning model.
4. **Model Evaluation**: Evaluate performance using **MLflow** and **DagsHub**.

---

## **Development Workflow**
### **1. Configurations**
- **`config.yaml`**: Update this file with details about data paths, model parameters, and other pipeline configurations.
- **`schema.yaml`**: Define the schema for the input dataset.
- **`params.yaml`**: Specify hyperparameters and model settings.

### **2. Update the Code**
1. **Entities**:
   - Define the schema for the entities (e.g., datasets, models).
2. **Configuration Manager**:
   - Use a configuration manager in `src/config` to load configurations dynamically.
3. **Components**:
   - Write modular code for pipeline components (e.g., data ingestion, transformation, model training).
4. **Pipeline**:
   - Define the sequence of steps in the pipeline.
5. **Main Application**:
   - Update `main.py` to integrate all components and run the pipeline.

---

## **Environment Setup**
### Create a Conda Environment
```bash
conda create -p venv python==3.10 -y
conda activate ./venv  
```

Project Setup
Initialize Logger: Configure the logger for the project.
Set Constants: Define constants and paths in src/config/constants.py.
Set ConfigBox: Use ConfigBox to manage configurations efficiently.
Set Pipelines:
Define pipelines for training and evaluation.
Setup Flask: Build an API for the project using Flask.

## MLFLOW tracking via dagshub

### **Run app using**
python app.py
