# Unsupervised Learning: University Clustering & Data Quality Checks

Applied K-Means clustering to group universities based on financial and academic features, with a focus on data cleaning, anomaly detection, and model interpretation.

---

## Project Motivation
I completed this project to better understand how unsupervised learning can identify patterns in data without predefined labels. The goal was to see whether a clustering algorithm could separate public and private universities based only on numerical features, similar to how clustering can be used in finance to flag unusual behaviour or segment customers.

---

## Data Exploration and Cleaning
Before modelling, I performed exploratory data analysis and basic data validation to ensure the dataset was reliable.

### Identifying Data Errors
![Corrected Grad Rate](corrected_grad_rate.png)

During EDA, I identified a university (Cazenovia College) with a reported graduation rate greater than 100%, which is not possible.

- **Correction:** The graduation rate was capped at 100%.
- **Reasoning:** Cleaning obvious data errors helps prevent misleading model results and is a necessary step before any form of modelling.

---

## Clustering Analysis
I applied **K-Means clustering** to a dataset of 777 universities using 18 numerical features, including tuition fees, room and board costs, graduation rates, and faculty qualifications.

### 1. Feature Separation
![Tuition Distribution](tuition_distribution.png)

Out-of-state tuition was analysed as a key variable contributing to separation between clusters, showing clear differences between university types.

### 2. Comparing Clusters to Known Labels
![Cluster Comparison](cluster_comparison.png)

Although K-Means is an unsupervised algorithm, the dataset contained known labels. This allowed me to compare the resulting clusters against the true public/private classifications to assess how well the model performed.

---

## Model Evaluation
![K-Means Confusion Matrix](kmeans_confusion_matrix.png)

To evaluate performance, I mapped cluster labels to known categories and generated a confusion matrix.

- The results showed that the model captured the overall structure of the data well.
- Some overlap between clusters highlights the limits of separating institutions using only numerical features.

---

## Key Takeaways
- Unsupervised learning can uncover meaningful structure in data without labelled outcomes.
- Data cleaning and validation are essential before applying any machine learning model.
- Visualisation is critical for interpreting clustering results and communicating findings clearly.

---

## How to Run
1. Install dependencies:
```bash
pip install -r requirements.txt

