# 🛡️ DDoS Attack Detection using Machine Learning (SDN + Healthcare IoT)

This repository contains Jupyter Notebooks and code for training and evaluating **machine learning models** on **two real-world datasets**:  
- **SNT (Social Network Traffic)** → representing **SDN networks**  
- **UL-ECE-UDP-DDoS-H-IoT2025** → representing **Healthcare IoT traffic**  

The goal is to detect and mitigate **Distributed Denial of Service (DDoS) attacks** in **different network domains** (SDN + IoT), while comparing performance and feature importance across them.  

---

## 🌐 About the Project  

The rise of **DDoS attacks** threatens both **programmable SDN controllers** and **critical IoT devices** in healthcare environments.  
This project builds **end-to-end ML pipelines** to:  
- **Identify malicious traffic** quickly and reliably  
- **Differentiate multiple attack types** (not just binary)  
- **Compare detection methods across domains** (SDN vs. IoT)  
- Support **real-time proactive mitigation**  

---

## 🚀 Features  

- Dual-dataset pipelines:
  - 📡 **SDN traffic (SNT dataset)** → flow-level features  
  - 🏥 **Healthcare IoT UDP traffic (UL-ECE-UDP-DDoS-H-IoT2025)** → device-level features  
- Preprocessing:
  - Handling missing values  
  - Normalization + encoding  
  - Feature engineering for IoT traffic  
- Imbalance handling with undersampling  
- ML Models implemented:
  - 🌲 Random Forest  
  - 🌳 Decision Tree  
  - 📈 Logistic Regression  
  - ⚡ XGBoost  
  - 🔎 SVM (Healthcare IoT only)  
  - 📊 Gradient Boosting (Healthcare IoT only)  
- Evaluation metrics:
  - ✅ Accuracy  
  - 🎯 Precision, Recall, F1 (binary + weighted multiclass)  
  - 📊 ROC-AUC  
  - 🔍 Feature importance ranking  
  - 📉 Confusion matrices  
- Designed to handle **millions of network records efficiently**  

---

## 📂 Datasets  

### 1. **SNT (Social Network Traffic)**  
- Represents SDN traffic  
- Contains normal + malicious flows (DDoS, botnet, etc.)  
- Features: packet/flow-level statistics  
- Targets:  
  - `y_binary` → 0 = Benign, 1 = Attack  
  - `y_multiclass` → Benign, DDoS, Botnet, etc.  

### 2. **UL-ECE-UDP-DDoS-H-IoT2025**  
- Healthcare IoT dataset with UDP-based traffic  
- Contains both normal and DDoS attack flows  
- Features include:  
  - Temporal (e.g., `time_elapsed`, `frequency`)  
  - Network (`node_id`, `protocol`, IPs)  
  - Traffic (`payload_size`, `total_messages`)  
  - Monitoring (`monitoring_total_messages`)  
- Target:  
  - `outcome` → Normal vs Attack  

---

## 🔬 Methodology  

- **Two parallel pipelines** (SDN + IoT) with similar structures:  
  - Data preprocessing  
  - Feature selection/engineering  
  - Model training  
  - Evaluation (metrics + visualization)  
- **Cross-domain analysis** performed to check if detection methods generalize between SDN and IoT.  

---

## 📊 Results (Highlights)  

- Both pipelines achieved **95%+ accuracy** in binary classification.  
- **Random Forest** consistently gave the best performance across both datasets.  
- Multiclass classification also performed well, though slightly lower than binary.  
- Feature importance analysis revealed different critical features in SDN vs. IoT.  

---
