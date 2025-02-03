# 🚀 Credit Card Fraud Detection using Machine Learning  

## 📌 Overview  
Credit card fraud is a significant financial risk, and detecting fraudulent transactions is crucial for banks and financial institutions. This project leverages **Machine Learning** techniques to classify fraudulent and legitimate transactions using the **Credit Card Fraud Dataset**.  

The dataset is highly **imbalanced**, with fraudulent transactions being rare. To address this, we applied **undersampling** techniques and trained a **Logistic Regression** model to detect fraud effectively.  

## 📂 Dataset  
The dataset used is the **Credit Card Fraud Dataset** from [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). It contains **284,807 transactions**, with only **492 fraud cases (~0.17%)**. Features are numerical and derived using **PCA (Principal Component Analysis)** for anonymization.  

**Columns:**  
- `Time`: Time elapsed from the first transaction  
- `V1, V2, ..., V28`: Principal components after PCA transformation  
- `Amount`: Transaction amount  
- `Class`: **Target Variable** (0 = Legitimate, 1 = Fraudulent)  

---

## 🛠 Tech Stack  
- **Python**  
- **Pandas, NumPy** (Data Processing)  
- **Scikit-learn** (Machine Learning)  
- **Matplotlib, Seaborn** (Data Visualization)  

---

## 📊 Process Flow  
### **1️⃣ Data Preprocessing**  
- Loaded the dataset using Pandas  
- Checked for missing values (none found)  
- Analyzed class distribution (highly imbalanced)  
- Performed exploratory data analysis (EDA)  
- Separated **fraudulent** and **legitimate** transactions  

### **2️⃣ Handling Imbalanced Data**  
Since fraud cases are rare, a **random undersampling** approach was used:  
- Selected a **random sample of 492** legitimate transactions (equal to fraud cases)  
- Created a new balanced dataset for training  

### **3️⃣ Model Training**  
We trained a **Logistic Regression** model using Scikit-learn:  
- **Features (`X`)**: All columns except `Class`  
- **Target (`Y`)**: `Class` column (0 or 1)  
- **Data Split**: 80% training, 20% testing (`train_test_split`)  
- **Training**: Fitted Logistic Regression on `X_train, Y_train`  

### **4️⃣ Model Evaluation**  
- **Accuracy Score**: Evaluated the model’s overall performance  
- **Confusion Matrix**: Checked False Positives & False Negatives  
- **Classification Report**: Analyzed Precision, Recall & F1-score  

---

## 📈 Results & Insights  
- **Accuracy Score**: Achieved a reasonable accuracy  
- **Class Imbalance Effect**: Accuracy alone is misleading due to imbalance  
- **Recall & Precision Tradeoff**: Focused on **Recall** to minimize fraud cases going undetected  

🔹 **Next Steps & Improvements**  
✔ Feature Scaling (Standardization for better results)  
✔ Try **Random Forest, XGBoost, or Neural Networks**  
✔ Fine-tune hyperparameters for better detection  

---

## 🔗 Resources  
- **Dataset**: [Credit Card Fraud Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)    
- **Scikit-learn Documentation**: [https://scikit-learn.org](https://scikit-learn.org)   
---

🚀 **If you found this useful, consider giving it a ⭐ on GitHub!**  

