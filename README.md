# 🛡️ DDoS Attack Detection using Machine Learning (SNT Dataset)

This repository contains a Jupyter Notebook for training and evaluating **machine learning models** on the **Social Network Traffic (SNT) dataset**, with the primary focus on **detecting and preventing Distributed Denial of Service (DDoS) attacks**.  

The notebook demonstrates both **binary classification** (Attack vs. Benign) and **multiclass classification** (different types of attacks), optimized for **fast execution** and **high accuracy**.

---

## 🌐 About the Project  

The rise of **DDoS attacks** in modern networks poses serious threats to availability and security.  
This project uses the **SNT dataset**, which includes real-world traffic patterns, to build models capable of:  
- **Identifying malicious traffic** early  
- **Differentiating between multiple attack types**  
- Supporting **proactive DDoS mitigation** in social and enterprise networks  

---

## 🚀 Features  

- Preprocessing with **scaling & stratified splits**  
- **Class imbalance handling** with undersampling (fast and effective for large data)  
- Training and evaluation of state-of-the-art models:  
  - 🌲 Random Forest  
  - 🌳 Decision Tree  
  - 📈 Logistic Regression  
  - ⚡ XGBoost (with optional GPU acceleration)  
- Performance metrics:  
  - ✅ Accuracy  
  - 🎯 F1-score (binary & weighted multiclass)  
  - 📊 ROC-AUC (for better attack detection evaluation)  
- Designed to handle **millions of traffic records efficiently**  

---

## 📂 Dataset  

We use the **SNT (Social Network Traffic) dataset**, which contains:  
- Normal (benign) traffic flows  
- Malicious traffic from **DDoS and related attacks**  
- Features representing packet-level and flow-level characteristics  

**Targets:**  
- `y_binary` → Binary classification (0 = Benign, 1 = Attack)  
- `y_multiclass` → Multiclass classification (Benign, DDoS, Botnet, etc.)  

---

