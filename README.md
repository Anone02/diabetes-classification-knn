Diabetes Classification using K-Nearest Neighbors (KNN)
Description

This project builds a machine learning model to classify whether a patient has diabetes based on medical attributes. The model uses the K-Nearest Neighbors (KNN) algorithm and includes data exploration, preprocessing, training, and evaluation.

Dataset

The dataset contains medical features such as:

Glucose
Blood Pressure
BMI
Age
Insulin
Pregnancies

Target variable:

Outcome (0 = No Diabetes, 1 = Diabetes)
Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Project Workflow
1. Data Exploration
Display dataset (head, shape)
Check data types and missing values (info)
Statistical summary (describe)
2. Data Visualization
Pairplot with outcome separation
Correlation heatmap
Boxplot (Age distribution)
Histogram for all features
Bar chart for Outcome distribution
3. Data Preprocessing
Separate features and target:
X = features
y = target (Outcome)
Train-test split (80% training, 20% testing)
Feature scaling using StandardScaler
4. Model Training

KNN model is trained using:

from sklearn.neighbors import KNeighborsClassifier

knn = KNeighborsClassifier(n_neighbors=k)
knn.fit(X_train, y_train)
5. Model Evaluation
Accuracy Score
Confusion Matrix
Classification Report (precision, recall, f1-score)
6. Hyperparameter Tuning
Tested values of K from 1 to 40
Selected optimal K based on lowest error rate
Optimal value found around: k = 18
Results
The model achieved good classification performance on test data
Optimal K improves model accuracy and reduces error
Visualization helps understand feature relationships and data distribution
Project Structure
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
How to Run
Clone the repository:
git clone https://github.com/your-username/diabetes-knn-classification.git
Install dependencies:
pip install -r requirements.txt
Run the notebook:
jupyter notebook
Future Improvements
Try other models (Logistic Regression, Random Forest)
Perform feature selection
Use cross-validation
Deploy as a web app (Streamlit or API)
