
---

🛡️ Malicious URL Dashboard – Simple 6 Steps Guide


---

✅ Step 1: Understand File Structure (Diagram + Purpose)

📁 Project Structure

/project-folder
│   app.py
│   README.md
│   requirements.txt
│
├───models
│       model.pkl
│
├───static
│   └───js
│       dashboard.js
│
├───templates
│       index.html
│
├───training
│       train_model.py
│       notebook.ipynb

📌 Purpose of Each File

File/Folder	Purpose

app.py	Main backend server (Flask API)
models/	Stores trained ML model
dashboard.js	Handles frontend logic and API calls
index.html	Dashboard UI design
train_model.py	Converts notebook into ML model file
notebook.ipynb	Used for training and experimentation
requirements.txt	Stores required libraries



---

✅ Step 2: Design Dashboard (index.html Structure)

Create the frontend layout using:

Bootstrap 5 (layout & responsiveness)

DC.js + D3.js + Crossfilter2 (charts)


📊 Dashboard Layout Diagram

------------------------------------------------------
🛡️ Malicious URL Dashboard
------------------------------------------------------
Sidebar (Navigation Menu)
------------------------------------------------------
Top Section:
[ URL Input ] [ Scan Button ]
[ Prediction Result Card ]
[ Risk Score Indicator ]
------------------------------------------------------
KPI Row:
[ Accuracy ] [ Total URLs ] [ Safe ] [ Malicious ]
------------------------------------------------------
Charts Section:
[ Confusion Matrix ]   [ Feature Importance ]
------------------------------------------------------
Dataset Section:
[ Class Distribution Chart ]
------------------------------------------------------
Bottom Section:
[ Classification Report Table ]
------------------------------------------------------

🎯 Goal

Build a clean dark-themed dashboard

Use Bootstrap grid system

Reserve placeholders for charts (DC.js)



---

✅ Step 3: Create Model Training Script

📌 Task

Convert your .ipynb file into a Python script.

🎯 Purpose

Train ML model (e.g., Random Forest)

Extract features from URLs

Save trained model into:


/models/model.pkl


---

✅ Step 4: Generate Model File

📌 Task

Run the training script.

🎯 Output

A trained model file stored in models folder

This file will be used by the backend API



---

✅ Step 5: Create Backend API (app.py)

📌 Design API Structure (No Coding)

API Name	Route	Purpose

Health Check	/api/v1/health	Check server status
Model Info	/api/v1/model/info	Show model details
Predict URL	/api/v1/predict	Detect Safe/Malicious
Accuracy	/api/v1/metrics/accuracy	Return model accuracy
Confusion Matrix	/api/v1/metrics/confusion-matrix	Provide matrix data
Classification Report	/api/v1/metrics/classification-report	Provide performance metrics
Feature Importance	/api/v1/features/importance	Show important features
Dataset Summary	/api/v1/dataset/summary	Total URLs, counts
Class Distribution	/api/v1/dataset/class-distribution	Safe vs Malicious


🎯 Goal

Connect frontend with ML model

Return JSON data for dashboard



---

✅ Step 6: Create dashboard.js (Frontend Logic)

📌 Responsibilities

dashboard.js connects index.html ↔ app.py

🔧 Tasks

1. On page load:

Fetch dataset summary

Fetch accuracy

Load charts (DC.js)



2. Handle URL Scan:

Send request to /predict

Display:

Prediction result

Risk score

Feature details




3. Render Charts:

Confusion Matrix

Feature Importance

Class Distribution



4. Handle:

Loading states

Errors

Dynamic updates





---

🎯 Final Understanding Flow

User → index.html (UI)
        ↓
dashboard.js (logic)
        ↓
app.py (API)
        ↓
ML Model (prediction)
        ↓
Response → Dashboard Visualization


---
