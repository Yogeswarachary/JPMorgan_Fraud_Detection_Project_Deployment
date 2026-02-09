# 🏦 JP Morgan Fraud Detection – Capstone Project

## 📘 Overview
- This repository contains my JP Morgan Fraud Detection Capstone Project, developed as part of my Data Science training program.
- The primary goal is to detect fraudulent financial transactions using advanced machine learning techniques.
- The model has been successfully developed and tested locally. However, cloud deployment faced challenges due to large dataset size and free-tier resource limitations on Streamlit Cloud and Hugging Face Spaces.

## 🚨 Problem Statement
- The deployment issues are primarily caused by the size of the original dataset and project structure:
- The raw dataset contains over 6 million rows (~480 MB CSV, ~250 MB Parquet).
- Cloud platforms (free tier) have limited memory and file-size capacity, preventing full dataset uploads and execution.
- The repository initially included the entire raw data, EDA notebooks, and model training scripts, resulting in excessive deployment load.
- As a result, although the project runs locally without issues, it cannot be rendered on Streamlit Cloud or Hugging Face due to these limitations.

## 💡 Solution
- After consulting data science professionals and industry experts (via Reddit), the recommended solution is:
- Use a sample dataset (1,000 – 10,000 rows) for deployment.
- Load the trained model pickle file (.pkl) on this smaller dataset to simulate predictions.
- Deploy the lightweight version using Streamlit Cloud or Hugging Face Spaces, ensuring smooth rendering and responsiveness.
- The smaller dataset retains the same schema and feature structure as the full dataset, allowing the model to demonstrate fraud prediction functionality effectively.
> ✅ This approach ensures compatibility with free-tier deployment limits while maintaining model accuracy for demonstration purposes.

## 🧠 Technical Details
| Component                | Description                                                    |
| ------------------------ | -------------------------------------------------------------- |
| **Programming Language** | Python 3.10+                                                   |
| **Libraries Used**       | pandas, numpy, scikit-learn, seaborn, matplotlib, streamlit    |
| **Model Used**           | Random Forest Classifier (optimized for imbalanced data)       |
| **Deployment Tools**     | Streamlit Cloud / Hugging Face Spaces                          |
| **Data Source**          | Synthetic dataset generated with NumPy (no real JPMorgan data) |


## 🧩 Dataset Information
- Since real JPMorgan data is not publicly available, a synthetic dataset was generated using Python and NumPy to replicate realistic transaction patterns.
This dataset includes both legitimate and fraudulent transactions for model evaluation.
🔗 Sample dataset link: https://drive.google.com/file/d/1ZoIf2OqlD8mGvwKc3bPcV4Q1gDH0JgJC/view?usp=sharing

## ⚙️ How to Run the Project Locally
1️⃣ Clone the Repository
git clone https://github.com/your-username/jpmorgan-fraud-detection.git
cd jpmorgan-fraud-detection

2️⃣ Install Dependencies
pip install -r requirements.txt

3️⃣ Run the Streamlit App
streamlit run app.py

4️⃣ Access the App

Once the app starts, open your browser and go to:
👉 http://localhost:8501

## 🚀 Deployment Recommendations
- To ensure smooth deployment on Streamlit Cloud or Hugging Face Spaces:
- Use sample datasets instead of full raw data.
- Remove large files (datasets, EDA notebooks, temporary logs).
- Keep deployment-specific code (like app.py, model .pkl, and sample data).
- Add a .gitignore file to exclude unnecessary files and folders.

## 🏁 Summary
✅ Aspect	💡 Recommendation
- Data Handling	Use sample data (1k – 10k rows)
- Deployment	Streamlit Cloud / Hugging Face (Free Tier)
- Model	Load pre-trained .pkl for prediction
- Goal	Lightweight, functional demo for recruiters and reviewers

## 🙏 Acknowledgements
Special thanks to:

- Data Science mentors and Reddit community for deployment insights.
- Open-source contributors and AI tools that provided troubleshooting guidance.
