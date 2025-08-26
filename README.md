# 🏦 Fake Currency Detection  

A machine learning project that leverages **XGBoost** to detect counterfeit currency notes using physical and security-based features. The model is trained to distinguish genuine notes from fake ones with high accuracy.  

---

## 📂 Dataset  

Each note in the dataset is described by:  

- **Country** – Issuing country  
- **Denomination** – Value of the note (e.g., $100, €20)  
- **SecurityFeatures** – Encoded presence of holograms, watermarks, security threads, etc.  
- **Weight, Length, Width, Thickness** – Physical attributes of the note  
- **Counterfeit (Target)** – `0 = Genuine`, `1 = Fake`  

> **Note**: Serial numbers are excluded since they are not generalizable features.  

---

## ⚙️ Methodology  

1. **Data Preprocessing**  
   - Dropped non-generalizable identifiers (e.g., SerialNumber)  
   - One-Hot Encoding for categorical variables (Country, Denomination, SecurityFeatures)  
   - Standardization for numerical features  
   - Stratified split: 80% training / 20% testing  

2. **Modeling**  
   - **XGBoost Classifier** chosen for high performance on structured data  
   - Trained on preprocessed features  

3. **Evaluation**  
   - **Accuracy Score** – Overall performance  
   - **Classification Report** – Precision, Recall, F1-score  
   - **Confusion Matrix** – Distribution of predictions vs actuals  

---

## 🚀 How to Run  

1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/fake-currency-detection.git
   cd fake-currency-detection
