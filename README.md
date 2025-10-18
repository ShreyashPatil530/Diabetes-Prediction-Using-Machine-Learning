# 🏥 Diabetes Prediction Using Machine Learning

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Kaggle](https://img.shields.io/badge/Kaggle-View%20Notebook-20BEFF)](https://www.kaggle.com/code/shreyashpatil217/diabetes-prediction-using-machine-learning)

> A comprehensive end-to-end machine learning project for predicting diabetes in patients using the Pima Indians Diabetes Database.


---

## 📋 Table of Contents
- [Overview](#-overview)
- [Features](#-features)
- [Dataset](#-dataset)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Model Performance](#-model-performance)
- [Results](#-results)
- [Technologies Used](#-technologies-used)
- [Future Improvements](#-future-improvements)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🎯 Overview

This project implements a complete machine learning pipeline to predict diabetes in patients based on diagnostic measurements. The goal is to diagnostically predict whether a patient has diabetes based on certain diagnostic measurements included in the dataset.

### Key Highlights:
- ✅ Comprehensive Exploratory Data Analysis (EDA)
- ✅ Advanced Feature Engineering
- ✅ Multiple ML Model Comparison (7 algorithms)
- ✅ Hyperparameter Optimization using Grid Search
- ✅ Production-Ready Model Deployment
- ✅ Professional Visualizations
- ✅ Detailed Documentation

---

## ✨ Features

- **Data Preprocessing**: Handling missing values, outlier detection, and feature scaling
- **Feature Engineering**: Created new features to improve model performance
- **Model Training**: Trained and evaluated 7 different ML algorithms
- **Hyperparameter Tuning**: Optimized best model using Grid Search CV
- **Model Evaluation**: Comprehensive metrics including ROC-AUC, Precision, Recall, F1-Score
- **Visualization**: Beautiful plots and charts for data insights
- **Model Persistence**: Save and load trained models for deployment

---

## 📊 Dataset

**Source**: [Pima Indians Diabetes Database](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database) from UCI Machine Learning Repository

### Dataset Information:
- **Instances**: 768 patients
- **Features**: 8 medical predictor variables
- **Target Variable**: Diabetes outcome (0 = No Diabetes, 1 = Diabetes)
- **Class Distribution**: 
  - No Diabetes: 500 (65.1%)
  - Diabetes: 268 (34.9%)

### Features Description:
| Feature | Description | Type |
|---------|-------------|------|
| Pregnancies | Number of times pregnant | Numeric |
| Glucose | Plasma glucose concentration | Numeric |
| BloodPressure | Diastolic blood pressure (mm Hg) | Numeric |
| SkinThickness | Triceps skin fold thickness (mm) | Numeric |
| Insulin | 2-Hour serum insulin (mu U/ml) | Numeric |
| BMI | Body mass index (weight in kg/(height in m)^2) | Numeric |
| DiabetesPedigreeFunction | Diabetes pedigree function | Numeric |
| Age | Age (years) | Numeric |
| Outcome | Class variable (0 or 1) | Binary |

---

## 🔧 Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Step 1: Clone the Repository
```bash
git clone https://github.com/ShreyashPatil530/Diabetes-Prediction-Using-Machine-Learning.git
cd diabetes-prediction-ml
```

### Step 2: Create Virtual Environment (Recommended)
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Mac/Linux
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Required Libraries
```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

### Option 1: Run Jupyter Notebook
```bash
jupyter notebook diabetes_prediction.ipynb
```

### Option 2: Run Python Script
```bash
python diabetes_prediction.py
```

### Option 3: Google Colab
1. Upload `diabetes_prediction.ipynb` to Google Colab
2. Upload the dataset or use Kaggle API
3. Run all cells

### Making Predictions
```python
import pickle
import numpy as np

# Load the trained model
with open('models/diabetes_model.pkl', 'rb') as f:
    model = pickle.load(f)

# Load the scaler
with open('models/scaler.pkl', 'rb') as f:
    scaler = pickle.load(f)

# Example patient data
patient_data = np.array([[6, 148, 72, 35, 0, 33.6, 0.627, 50]])

# Scale the data
patient_scaled = scaler.transform(patient_data)

# Make prediction
prediction = model.predict(patient_scaled)
probability = model.predict_proba(patient_scaled)

print(f"Prediction: {'Diabetes' if prediction[0] == 1 else 'No Diabetes'}")
print(f"Probability: {probability[0][1]*100:.2f}%")
```

---

## 📁 Project Structure

```
diabetes-prediction-ml/
│
├── README.md                          # Project documentation
├── LICENSE                            # MIT License
├── requirements.txt                   # Python dependencies
├── .gitignore                        # Git ignore file
│
├── diabetes_prediction.ipynb          # Main Jupyter notebook
├── diabetes_prediction.py             # Python script version
│
├── data/
│   └── diabetes.csv                  # Dataset
│
├── models/
│   ├── diabetes_model.pkl            # Trained model
│   └── scaler.pkl                    # Feature scaler
│
├── images/
│   ├── correlation_heatmap.png       # Visualizations
│   ├── model_comparison.png
│   ├── final_evaluation.png
│   └── banner.png
│
└── notebooks/
    └── exploratory_analysis.ipynb    # Detailed EDA
```

---

## 📈 Model Performance

### Models Evaluated:
1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier ⭐ **Best Model**
4. Gradient Boosting Classifier
5. Support Vector Machine (SVM)
6. K-Nearest Neighbors (KNN)
7. Naive Bayes

### Best Model Results:
| Metric | Score |
|--------|-------|
| **Accuracy** | 78.57% |
| **Precision** | 76.32% |
| **Recall** | 72.50% |
| **F1-Score** | 74.36% |
| **ROC-AUC** | 0.8245 |

---

## 🔬 Results

### Key Findings:
1. **Glucose Level** is the strongest predictor of diabetes (correlation: 0.47)
2. **BMI** and **Age** are also significant indicators
3. **Random Forest** achieved the best overall performance
4. Feature engineering improved model accuracy by ~3%
5. The model can identify high-risk patients with 82% confidence



### Business Impact:
- Early identification of high-risk patients
- Reduced healthcare costs through preventive care
- Better resource allocation in healthcare facilities
- Data-driven clinical decision support

---

## 🛠️ Technologies Used

### Programming Language:
- **Python 3.8+**

### Libraries & Frameworks:
- **Data Manipulation**: Pandas, NumPy
- **Machine Learning**: Scikit-learn
- **Visualization**: Matplotlib, Seaborn
- **Model Persistence**: Pickle
- **Development Environment**: Jupyter Notebook, Google Colab

### Machine Learning Algorithms:
- Logistic Regression
- Decision Trees
- Random Forest
- Gradient Boosting
- Support Vector Machines
- K-Nearest Neighbors
- Naive Bayes

### Techniques Applied:
- Cross-Validation
- Grid Search Hyperparameter Tuning
- Feature Engineering
- Feature Scaling (StandardScaler)
- Stratified Train-Test Split

---

## 🚀 Future Improvements

- [ ] Implement Deep Learning models (Neural Networks)
- [ ] Add SHAP values for model explainability
- [ ] Create a web application using Flask/Streamlit
- [ ] Deploy model to cloud (AWS/Azure/GCP)
- [ ] Collect more diverse patient data
- [ ] Implement real-time prediction API
- [ ] Add automated model retraining pipeline
- [ ] Create mobile app for patient risk assessment

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### How to Contribute:
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

##  Contact

**Shreyash Patil**
- 📧 Email: shreyashpatil530@gmail.com
- 💼 LinkedIn: [LinkedIn](https://linkedin.com/in/yourprofile)
- 🐱 GitHub: [sp](https://github.com/ShreyashPatil530/Diabetes-Prediction-Using-Machine-Learning)
- 📊 Kaggle: [Kaggle](https://www.kaggle.com/code/shreyashpatil217/diabetes-prediction-using-machine-learning)
- 🌐 Portfolio: [website.com](https://shreyash-patil-portfolio1.netlify.app/)

---

## 🙏 Acknowledgments

- Dataset provided by the National Institute of Diabetes and Digestive and Kidney Diseases
- UCI Machine Learning Repository
- Kaggle Community
- Scikit-learn Documentation

---

## ⭐ Star this Repository

If you find this project helpful, please consider giving it a star! ⭐

---

## 📊 Project Statistics

![GitHub stars](https://img.shields.io/github/stars/yourusername/diabetes-prediction-ml?style=social)
![GitHub forks](https://img.shields.io/github/forks/yourusername/diabetes-prediction-ml?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/yourusername/diabetes-prediction-ml?style=social)

---

**Made with  by Shreyash Patil**

*Last Updated: 18 October 2025*
