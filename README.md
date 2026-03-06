# 🛡️ Mini Project Assignment

# Predicting Malicious URLs Dashboard

### (Frontend + Flask API Integration)

---

## 📌 Project Title

**Machine Learning-Based Malicious URL Detection Dashboard**

---

## 🎯 Project Objective

Student must design and implement a **Cybersecurity Dashboard** that connects a **Flask Machine Learning API** to a professional frontend built using:

* ✅ Bootstrap 5
* ✅ DC.js
* ✅ Crossfilter2
* ✅ D3.js
* ✅ Dark Cybersecurity Theme

The system must allow users to scan URLs and visualize model insights.

---

# 🧠 Backend Overview 

The Flask backend provides the following REST API endpoints:

```
GET  /api/v1/health
GET  /api/v1/model/info
POST /api/v1/predict
GET  /api/v1/metrics/accuracy
GET  /api/v1/metrics/confusion-matrix
GET  /api/v1/metrics/classification-report
GET  /api/v1/features/importance
GET  /api/v1/dataset/summary
GET  /api/v1/dataset/class-distribution
```

Students must integrate these endpoints into the frontend.

---

# 🖥️ Dashboard Layout Requirements

The dashboard must follow this structured layout:

```
------------------------------------------------------
🛡️ Predicting Malicious URLs Dashboard
------------------------------------------------------
Sidebar Navigation (Left Panel)
------------------------------------------------------
Top Section:
- URL Input Box
- Scan Button
- Prediction Result Card
- Risk Score Display
------------------------------------------------------
KPI Cards Row:
- Accuracy
- Total URLs
- Malicious Count
- Safe Count
------------------------------------------------------
Charts Row:
- Confusion Matrix (DC.js)
- Feature Importance (DC.js)
------------------------------------------------------
Dataset Section:
- Class Distribution Chart (DC.js)
------------------------------------------------------
Bottom Section:
- Classification Report Table
------------------------------------------------------
```

---

# 🎨 UI Design Requirements

### Dark Cybersecurity Theme

| Component           | Color     |
| ------------------- | --------- |
| Background          | `#0f172a` |
| Cards               | `#1e293b` |
| Safe Indicator      | `#22c55e` |
| Malicious Indicator | `#ef4444` |
| Text                | White     |

### Additional UI Requirements

* Fully responsive (Bootstrap Grid)
* Sidebar navigation
* Loading spinner during API calls
* Error handling messages
* Clean professional layout

---

# ⚙️ Functional Requirements

## 1️⃣ On Page Load

The dashboard must automatically:

* Fetch dataset summary
* Fetch model accuracy
* Fetch confusion matrix
* Fetch feature importance
* Fetch class distribution

All charts must render using DC.js.

---

## 2️⃣ URL Scanning Feature

When the user enters a URL and clicks **Scan URL**:

### The system must:

1. Send POST request to:

   ```
   /api/v1/predict
   ```

2. Display:

   * Prediction (Safe / Malicious)
   * Confidence score
   * Extracted features:

     * URL length
     * Dot count
     * Hyphen count
     * HTTPS presence
     * IP presence
   * Risk level indicator (color-coded)

---

# 📊 Chart Requirements (DC.js Only)

Students must use:

* **DC.js**
* **D3.js**
* **Crossfilter2**

### ❌ Do NOT use:

* Chart.js
* Any other chart library

---

## Required Charts

### 1️⃣ Confusion Matrix

* Display as heatmap-style chart
* Show:

  * True Positive
  * True Negative
  * False Positive
  * False Negative

---

### 2️⃣ Feature Importance

* Bar chart
* X-axis → Feature Names
* Y-axis → Importance Values

---

### 3️⃣ Class Distribution

* Pie chart or bar chart
* Show:

  * Malicious count
  * Safe count

---

# 📑 Classification Report Section

Display the following as a table:

| Class | Precision | Recall | F1-Score | Support |
| ----- | --------- | ------ | -------- | ------- |

Include:

* Macro Average
* Weighted Average
* Overall Accuracy

---

# 🗂️ File Structure Requirement

Students must submit:

```
/project-folder
│
├── index.html
├── script.js
├── styles.css (optional)
```

### Rules:

* JavaScript must be in a separate file (script.js)
* Use async fetch API
* Clean modular code structure
* Comment important sections

---

# 🔄 API to Dashboard Mapping

| Dashboard Component   | API Endpoint                       |
| --------------------- | ---------------------------------- |
| Health Status         | GET /health                        |
| KPI Cards             | GET /dataset/summary               |
| Accuracy              | GET /metrics/accuracy              |
| Confusion Matrix      | GET /metrics/confusion-matrix      |
| Feature Importance    | GET /features/importance           |
| Class Distribution    | GET /dataset/class-distribution    |
| URL Scanner           | POST /predict                      |
| Classification Report | GET /metrics/classification-report |

---

# 🧪 Testing Requirements

Student must:

* Test with at least 3 sample URLs
* Show Safe and Malicious predictions
* Demonstrate charts updating properly
* Handle API failure gracefully

---

# 📦 Deliverables

Students must submit:

1. Complete frontend code
2. Screenshots of:

   * Dashboard UI
   * URL prediction example
   * All charts working
3. Short documentation including:

   * Architecture diagram
   * API integration explanation
   * Crossfilter + DC.js explanation
   * Challenges faced

---

# 🏗️ Architecture Diagram (Conceptual)

```
User → Frontend (Bootstrap + DC.js)
        ↓
    Flask API
        ↓
RandomForest ML Model
        ↓
Prediction + Metrics
        ↓
Frontend Visualization
```

---

# 📊 Evaluation Rubric

| Criteria                    | Marks |
| --------------------------- | ----- |
| UI Design & Layout          | 10    |
| API Integration             | 15    |
| DC.js Charts Implementation | 15    |
| URL Scanner Functionality   | 10    |
| Code Quality & Structure    | 10    |
| Documentation               | 10    |
| Total                       | 70    |

---

# 🚀 Bonus (Optional Advanced Features)

* Risk Score Meter
* URL Scan History Table
* Model Info Modal
* Export Report as PDF
* Retrain Model Button (API integration)

---



**End of Assignment**
