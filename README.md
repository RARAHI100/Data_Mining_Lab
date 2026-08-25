

# data_mining_lab

🎓 **Data Mining Lab— Tasks & Implementations**

A collection of practical **Data Mining laboratory tasks and implementations** completed during my **3rd Year** as part of the Data Mining course. The repository contains different Jupyter Notebook implementations covering data preprocessing, data visualization, clustering, association rule mining, and ensemble learning.

---

## 📌 Course Information

| Information             | Details                                                                         |
| ----------------------- | ------------------------------------------------------------------------------- |
| Course                  | Data Mining                                                                     |
| Course Type             | Lab                                                                     |
| Academic Level          | 3rd Year                                                                        |
| Programming Language    | Python                                                                          |
| Development Environment | VS Code                                                      |
| Implementation Type     | Laboratory Tasks & Practical Implementations                                    |
| Main Topics             | Preprocessing, Visualization, Clustering, Association Mining, Ensemble Learning |

---

# 📖 About the Repository

This repository contains the **Data Mining laboratory tasks and practical implementations** completed during my 3rd Year.

The purpose of these implementations was to understand and practice different concepts and techniques used in **Data Mining and Machine Learning**.

Each Jupyter Notebook focuses on a particular laboratory topic rather than representing one single software project.

The implementations cover topics such as:

* Data Preprocessing
* Data Visualization
* DBSCAN Clustering
* Apriori / FP-Growth
* Association Rule Mining
* Ensemble Learning

Different datasets are used depending on the laboratory task.

---

# ✨ Laboratory Tasks & Implementations

## 1. 🧹 Data Preprocessing

**Notebook:** `data_preprocessing.ipynb`

This laboratory implementation demonstrates common data preprocessing techniques using the Titanic dataset.

### Topics Covered

* Loading datasets
* Dataset inspection
* Selecting columns
* Checking missing values
* Handling missing values
* Removing unnecessary columns
* Descriptive statistics
* Data normalization
* Data standardization
* Label Encoding
* Ordinal Encoding
* One-Hot Encoding
* Pandas `get_dummies()`

### Dataset

```text
titanic_train.csv
```

### Missing Value Handling

Different approaches for handling missing values are demonstrated, including:

* Mean
* Median
* Mode
* Minimum
* Maximum

### Normalization

Min-Max normalization is demonstrated using:

```python
(df['age'] - df['age'].min()) / (df['age'].max() - df['age'].min())
```

### Standardization

Standardization is demonstrated using:

```python
(df['age'] - df['age'].mean()) / df['age'].std()
```

### Encoding

The implementation demonstrates:

```text
Label Encoding
Ordinal Encoding
One-Hot Encoding
get_dummies()
```

---

# 2. 📊 Data Visualization

**Notebook:** `visualization.ipynb`

This laboratory implementation focuses on **Exploratory Data Analysis and Data Visualization** using the Titanic dataset.

### Libraries Used

* Pandas
* Matplotlib
* Seaborn

### Visualizations Implemented

* Violin Plot
* Bar Plot
* Grouped Bar Plot
* Pair Plot
* Joint Plot
* Histogram
* Scatter Plot
* Correlation Analysis
* Correlation Heatmap

### Dataset

```text
titanic_train.csv
```

### Analysis

The implementation explores relationships between different Titanic features, including:

* Age
* Fare
* Sex
* Passenger Class
* Survival

Correlation between numerical features is also calculated and visualized using a heatmap.

---

# 3. 🔵 DBSCAN Clustering

**Notebook:** `dbscian.ipynb`

This laboratory implementation demonstrates **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**.

DBSCAN is an unsupervised clustering technique that groups data points based on density and identifies points that do not belong to a cluster as noise.

### Dataset

A custom two-dimensional dataset is created inside the notebook.

The dataset contains:

```text
Point
X
Y
```

with 12 sample points.

### DBSCAN Parameters

```python
eps = 1.9
min_samples = 4
```

The DBSCAN algorithm is implemented using Scikit-learn.

### Concepts Demonstrated

* Density-based clustering
* Cluster identification
* Noise detection
* DBSCAN parameters
* Cluster labels
* Scatter plot visualization

DBSCAN assigns:

```text
-1
```

to points identified as noise.

The resulting clusters and noise points are visualized using a scatter plot.

---

# 4. 🛒 Apriori / FP-Growth

**Notebook:** `apriori_fpgrowth.ipynb`

This laboratory implementation demonstrates **Association Rule Mining** using transaction data.

The implementation focuses on finding frequent itemsets and generating association rules from transactional data.

### Dataset

```text
transaction_data.csv
```

### Libraries Used

* Pandas
* NumPy
* SciPy
* Scikit-learn
* MLxtend

### Main Steps

1. Load transaction data
2. Handle missing values
3. Remove unnecessary transaction information
4. Encode transactions
5. Generate a Boolean transaction matrix
6. Find frequent itemsets
7. Generate association rules

### Transaction Encoding

The implementation uses:

```python
TransactionEncoder()
```

to convert transaction data into a Boolean representation.

### FP-Growth

Frequent itemsets are generated using FP-Growth with:

```python
fpgrowth(
    transc_df,
    min_support=0.6,
    use_colnames=True
)
```

### Association Rules

Association rules are generated using a minimum threshold of:

```text
0.8
```

### Concepts Demonstrated

* Transaction data preprocessing
* Transaction encoding
* Frequent itemsets
* Support
* Association rules
* FP-Growth
* Apriori concept

---

# 5. 🤖 Ensemble Learning

**Notebook:** `ensemble_learning.ipynb`

This laboratory implementation demonstrates different **Ensemble Learning and Classification techniques** using the Pima Indians Diabetes Dataset.

### Dataset

```text
pima-indians-diabetes.csv
```

The dataset contains:

```text
Pregnancies
Glucose
BloodPressure
SkinThickness
Insulin
BMI
DiabetesPedigreeFunction
Age
Outcome
```

The target variable is:

```text
Outcome
```

### Train-Test Split

The dataset is divided into training and testing data using:

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=2
)
```

This creates:

```text
80% → Training Data
20% → Testing Data
```

---

## 🗳️ Hard Voting Classifier

The implementation combines multiple classifiers using a **Hard Voting Classifier**.

The classifiers include:

* Decision Tree
* Logistic Regression
* Support Vector Machine

The final prediction is based on majority voting.

---

## 🌳 Bagging

Bagging is implemented using a Decision Tree classifier.

The implementation uses parameters including:

```text
n_estimators = 100
max_samples = 0.8
oob_score = True
random_state = 81
```

Both test performance and Out-of-Bag (OOB) performance are considered.

---

## 📈 Logistic Regression

Logistic Regression is implemented as a classification model and used to make predictions on the test dataset.

---

## 🌲 Random Forest

Random Forest classification is also implemented.

The model uses:

```text
n_estimators = 50
```

and its performance is evaluated on the test dataset.

---

# 🧠 Concepts Implemented

The Data Mining laboratory tasks cover the following concepts:

### Data Preprocessing

```text
Data Cleaning
Missing Value Handling
Normalization
Standardization
Encoding
Feature Transformation
```

### Data Visualization

```text
Exploratory Data Analysis
Violin Plot
Bar Plot
Pair Plot
Joint Plot
Histogram
Scatter Plot
Correlation
Heatmap
```

### Clustering

```text
DBSCAN
Density-Based Clustering
Cluster Identification
Noise Detection
```

### Association Rule Mining

```text
Apriori
FP-Growth
Frequent Itemsets
Association Rules
Support
```

### Classification & Ensemble Learning

```text
Decision Tree
Logistic Regression
Support Vector Machine
Hard Voting
Bagging
Random Forest
```

---

# 📁 Repository Structure

```text
data_mining_lab/
│
├── apriori_fpgrowth.ipynb
├── data_preprocessing.ipynb
├── dbscian.ipynb
├── ensemble_learning.ipynb
├── visualization.ipynb
│
├── transaction_data.csv
├── titanic_train.csv
├── pima-indians-diabetes.csv
│
└── README.md
```

---

# 📄 File Description

| File                        | Description                                                  |
| --------------------------- | ------------------------------------------------------------ |
| `data_preprocessing.ipynb`  | Data preprocessing and transformation implementations        |
| `visualization.ipynb`       | Data visualization and exploratory analysis implementations  |
| `dbscian.ipynb`             | DBSCAN clustering implementation                             |
| `apriori_fpgrowth.ipynb`    | Apriori/FP-Growth and association rule mining implementation |
| `ensemble_learning.ipynb`   | Ensemble learning and classification implementations         |
| `titanic_train.csv`         | Dataset used for preprocessing and visualization             |
| `transaction_data.csv`      | Transaction dataset used for association rule mining         |
| `pima-indians-diabetes.csv` | Dataset used for ensemble learning                           |
| `README.md`                 | Documentation of the laboratory tasks                        |

---

# ⚙️ How to Run the Implementations

## Step 1: Install Python

Install Python 3.x.

Check the installed version:

```bash
python --version
```

---

## Step 2: Install Required Libraries

Open a terminal and run:

```bash
pip install pandas numpy scipy scikit-learn matplotlib seaborn mlxtend jupyter
```

---

## Step 3: Open the Repository

Open the `data_mining_lab` folder using **Visual Studio Code**.

Make sure the required datasets are available in the repository directory.

---

## Step 4: Run Jupyter Notebooks

The notebooks can be opened and executed directly in VS Code using the Jupyter extension.

Alternatively:

```bash
jupyter notebook
```

Then open the required `.ipynb` file.

---

# 🖥️ Laboratory Implementation Flow

The overall Data Mining laboratory implementations can be viewed as:

```text
                 DATA MINING LAB
                       │
        ┌──────────────┼──────────────┐
        │              │              │
        ▼              ▼              ▼
   Preprocessing   Visualization   Data Mining
        │                             │
        │                    ┌────────┴────────┐
        │                    │                 │
        ▼                    ▼                 ▼
   Data Cleaning          DBSCAN        Association Mining
   Encoding              Clustering       │
   Scaling                   │             ├── Apriori
                             │             └── FP-Growth
                             │
                             ▼
                           Noise
                               
                       Classification
                             │
                             ▼
                     Ensemble Learning
                             │
              ┌──────────────┼──────────────┐
              ▼              ▼              ▼
           Voting          Bagging      Random Forest
```

---

# 🎯 Learning Objectives

The main objective of these laboratory implementations was to gain practical understanding of important **Data Mining concepts and algorithms**.

Through these tasks, I practiced:

* Preparing raw datasets for analysis
* Handling missing data
* Transforming numerical features
* Encoding categorical features
* Exploring datasets visually
* Understanding correlations
* Performing density-based clustering
* Identifying noise and clusters
* Finding frequent itemsets
* Generating association rules
* Understanding ensemble learning
* Combining multiple machine learning models
* Applying classification algorithms to real-world datasets

---

# 🎓 Academic Information

| Information    | Details                                 |
| -------------- | --------------------------------------- |
| Student        | Md Raihan Alam                          |
| Program        | BSc in Computer Science and Engineering |
| Institution    | Green University of Bangladesh          |
| Academic Level | 3rd Year                                |
| Course         | Data Mining                             |
| Course Type    | Laboratory                              |
| Work Type      | Laboratory Tasks & Implementations      |

---

# 🏁 Conclusion

This repository contains the practical **Data Mining laboratory tasks and implementations** completed during my 3rd Year.

The implementations cover several important topics, starting from **data preprocessing and visualization** and progressing to **clustering, association rule mining, and ensemble learning**.

Each notebook represents a separate laboratory implementation designed to provide hands-on experience with Data Mining concepts and algorithms.

These laboratory exercises helped me develop a practical understanding of how data can be **preprocessed, explored, clustered, analyzed for associations, and used with machine learning techniques**.

---

# ⭐ Course Work Status

**Completed — 3rd Year Data Mining Laboratory Tasks & Implementations**

These implementations were completed for academic and educational purposes as part of the **Data Mining Laboratory course**.
