# Diabetes Classification using K-Nearest Neighbors (KNN)

## Description
This project builds a machine learning model to classify whether a patient has diabetes based on medical attributes. The model uses the K-Nearest Neighbors (KNN) algorithm and includes data exploration, preprocessing, training, and evaluation.

## Dataset
The dataset contains medical features such as:
- Glucose
- Blood Pressure
- BMI
- Age
- Insulin
- Pregnancies

Target variable:
- Outcome (0 = No Diabetes, 1 = Diabetes)

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Project Workflow

### 1. Data Exploration
- Display dataset (head, shape)
- Check data types and missing values (info)
- Statistical summary (describe)

### 2. Data Visualization
- Pairplot with outcome separation
- Correlation heatmap
- Boxplot (Age distribution)
- Histogram for all features
- Bar chart for Outcome distribution

### 3. Data Preprocessing
- Separate features and target:
  X = features
  y = target (Outcome)
- Train-test split (80% training, 20% testing)
- Feature scaling using StandardScaler

### 4. Model Training
Using K-Nearest Neighbors:
from sklearn.neighbors import KNeighborsClassifier

knn = KNeighborsClassifier(n_neighbors=k)
knn.fit(X_train, y_train)

### 5. Model Evaluation
- Accuracy Score
- Confusion Matrix
- Classification Report (precision, recall, f1-score)

### 6. Hyperparameter Tuning
- Tested K values from 1 to 40
- Selected optimal K based on lowest error rate
- Optimal K found around k = 18

## Results
- Model achieved good classification performance
- Optimal K improves accuracy and reduces error
- Visualizations help understand the dataset

## Project Structure
diabetes-knn-classification/
│
├── data/
│   └── diabetes.csv
│
├── notebook/
│   └── diabetes_knn.ipynb
│
├── README.md
└── requirements.txt

## How to Run

1. Clone repository:
git clone https://github.com/your-username/diabetes-knn-classification.git

2. Install dependencies:
pip install -r requirements.txt

3. Run notebook:
jupyter notebook

## Future Improvements
- Try other models (Logistic Regression, Random Forest)
- Feature selection
- Cross-validation
- Deployment (Streamlit / API)
