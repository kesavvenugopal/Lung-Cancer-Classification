# 🩺 Lung Cancer Prediction

## 📌 Overview
This project aims to develop a **machine learning (XGBoost)** and **deep learning (MLP - Neural Network)** model for predicting lung cancer based on various health and lifestyle factors. Given the **severe class imbalance** in the dataset, resampling techniques like **SMOTE** were applied to improve the model's ability to detect cancer cases accurately.

---

## 📊 Dataset & Preprocessing
- The dataset contains various features related to lung cancer risk factors.
- Some columns were removed due to irrelevance to the prediction task.
- **Handling class imbalance:** The dataset had a **95% majority class**, leading to misleading accuracy scores. **SMOTE** was applied to balance the dataset.
- Encoding: **Label Encoding** for binary categorical features and **One-Hot Encoding** for multi-class categorical features.
- Feature scaling: **StandardScaler** was used to normalize numerical features.

---

## 🚀 Models Implemented
### 1️⃣ XGBoost Model (Baseline)
- Achieved **99.3% accuracy**, but suffered from poor recall for the minority class.
- Hyperparameter tuning using **RandomizedSearchCV**.
- Pickled and saved for future use.

### 2️⃣ Neural Network (MLP) Model
- **3-layer MLP with ReLU activations** and a **sigmoid output** for binary classification.
- Applied **SMOTE** to improve recall for cancer cases.
- Adjusted **decision threshold** to 0.325 for better false-negative reduction.
- Achieved better recall compared to XGBoost.
- Saved in **.keras format** for future use.

---

## 🔍 Key Observations
- The original model **misclassified 25% of cancer cases as non-cancer**, making accuracy misleading.
- **After SMOTE and threshold tuning**, the false negatives **dropped to 12%** while maintaining reasonable precision.
- **Confusion matrix analysis** confirmed that the neural network outperformed XGBoost in detecting cancer cases.

---

## 📂 Repository Structure
📄 **Lung_Cancer_Prediction.ipynb** - Contains the full **EDA, preprocessing, model building, evaluation, and results.**  
📁 **Saved Models** - Pre-trained models available for usage by anyone.  

---

## 📌 Future Improvements
✔️ Explore **ADASYN** or hybrid resampling techniques.  
✔️ Experiment with **more advanced deep learning architectures** (CNNs, transformers).  
✔️ Fine-tune the **decision threshold further** for better medical usability.  

---






### 📢 Feel free to explore the notebook and models! 🏥💡