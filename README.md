# 🚗 Car Price Prediction

**Description:**  
Predict car prices by classifying them into low, medium, or high categories using historical car data and machine learning models.

**Author:** Ahib Afnan Siam  
**Date:** 2026-01-25  
**Dataset:** [Car Details from Car Dekho](https://www.kaggle.com/datasets/gokulprasantht/car-details-from-car-dekho)  
**Categories:** Machine Learning, Regression/Classification, Data Analytics

---

## 📝 Project Overview

This project focuses on predicting car prices by classifying them into categories: `low`, `medium`, and `high`. The dataset contains multiple car features such as year, fuel type, seller type, transmission, and ownership history. Machine learning models including **K-Nearest Neighbors (KNN)**, **Logistic Regression**, **SVM**, and **Decision Tree Classifier** are used to train and evaluate the prediction accuracy.

---

## 📊 Dataset

The dataset contains information about cars, including:

- Name of the car
- Year of manufacturing
- Selling price
- Fuel type
- Seller type
- Transmission type
- Owner information
- Kilometers driven

**Important Files:**

| File Name                          | Description                               |
|-----------------------------------|-------------------------------------------|
| CAR DETAILS FROM CAR DEKHO.xlsx    | Original dataset for training and testing |

---

## 🛠 Data Preprocessing

**Steps Taken:**

1. **Handling Missing Values**
   - Dropped rows with missing critical features: `name`, `year`, `selling_price`, `fuel`, `seller_type`, `transmission`, `owner`
   - Imputed missing values in `km_driven` with **mean value**

2. **Label Encoding & Mapping**
   - Categorical columns such as `name` and `transmission` encoded using `LabelEncoder`
   - Ordinal mapping for `owner` and `fuel` types
   - Seller type mapped to numeric codes
   - Selling price binned into 3 categories (`low`, `medium`, `high`) and encoded as 0, 1, 2

3. **Scaling**
   - Applied **MinMaxScaler** and **StandardScaler** for feature scaling
   - Ensured zero-mean and unit-variance scaling for SVM and KNN

4. **Train/Test Split**
   - Split dataset into 70% training and 30% testing

---

## 📈 Data Visualization

- Heatmaps for feature correlations  
- Scatter plots and pair plots for feature interactions  
- Pie chart for distribution of low, medium, high price cars  
- Bar charts for price vs year  

**Example Visualizations:**

```python
sns.heatmap(data.corr(), annot=True)
plt.show()
```

## 🔧 Machine Learning Models

The following models were implemented:

| Model                     | Description                                      |
|---------------------------|--------------------------------------------------|
| K-Nearest Neighbors (KNN) | Classifies car prices based on closest neighbors |
| Logistic Regression       | Predicts categorical price bins                  |
| SVM                       | Support Vector Machine for classification       |
| Decision Tree Classifier  | Tree-based model for classification             |

**Training Steps:**

- Models trained on scaled features after preprocessing
- Evaluated using **accuracy** and **classification reports**
- Confusion matrices generated for visualization

---

## 📊 Evaluation Metrics

**Metrics Used:**

- Accuracy
- Classification Report (Precision, Recall, F1-Score)
- Confusion Matrix

**Model Accuracy Comparison:**

| Model                     | Accuracy |
|---------------------------|----------|
| K-Nearest Neighbors       | 0.XXX    |
| Logistic Regression       | 0.XXX    |
| SVM                       | 0.XXX    |
| Decision Tree Classifier  | 0.XXX    |

*Replace `0.XXX` with your observed accuracy scores.*

**Confusion Matrix Example:**

```python
from sklearn.metrics import confusion_matrix, ConfusionMatrixDisplay

cm = confusion_matrix(y_test, predictions)
disp = ConfusionMatrixDisplay(confusion_matrix=cm)
disp.plot()
plt.show()
```

## 🔑 Key Findings

- Oversampling balances the dataset across **low**, **medium**, and **high** car price categories
- Features such as **year**, **fuel type**, and **seller type** influence price prediction
- **Decision Tree** and **KNN** models performed well on scaled datasets
- Feature correlations help identify key predictors for car price

---

## 🚀 Usage

1. **Clone the repository:**

```bash
git clone <repository_url>
cd car-price-prediction
```

## 2. Train Models and Evaluate Predictions

Run the models on your dataset and check the accuracy, classification reports, and confusion matrices as demonstrated in the notebook or script.

---

## 🗂 Project Structure

car-price-prediction/
│
├── CAR DETAILS FROM CAR DEKHO.xlsx   # Dataset
├── main.py                           # Main script
├── notebook.ipynb                    # Jupyter Notebook
├── requirements.txt                  # Python dependencies
└── README.md                         # Project documentation
