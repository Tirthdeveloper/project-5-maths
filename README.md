# 📘 Project 5 - Mathematics Using Python

## 📌 Project Overview
This project demonstrates various Mathematics and Linear Algebra concepts using Python with an Employee Dataset.

The project is implemented in Jupyter Notebook (`pr5.ipynb`) using:
- NumPy
- Pandas
- Scikit-learn
- SciPy

It covers vector operations, matrix operations, decomposition techniques, PCA, and LDA.

---

# 📂 Dataset Used

**Dataset Name:** `combined_employee_dataset_1.csv`

### Features Used
- age
- years_experience
- performance_score

---

# 🛠️ Technologies & Libraries

```python
import numpy as np
import pandas as pd
from sklearn.decomposition import PCA
from sklearn.discriminant_analysis import LinearDiscriminantAnalysis
from scipy.linalg import lu
```

---

# 📊 Concepts Implemented

## ✅ Vector Creation

```python
employee1 = df.loc[0, ['age','years_experience','performance_score']].values
employee2 = df.loc[1, ['age','years_experience','performance_score']].values
```

---

## ✅ Norm Calculations

### L1 Norm

```python
np.linalg.norm(employee1, ord=1)
```

### L2 Norm

```python
np.linalg.norm(employee1)
```

---

## ✅ Dot Product

```python
np.dot(employee1, employee2)
```

---

## ✅ Angle Between Two Vectors

```python
cos_theta = np.dot(employee1, employee2) / (np.linalg.norm(employee1) * np.linalg.norm(employee2))
angle = np.degrees(np.arccos(cos_theta))
```

---

## ✅ Vector Projection

```python
projection = (np.dot(employee1, employee2) / np.dot(employee2, employee2)) * employee2
```

---

# 🧮 Matrix Operations

## ✅ Matrix Creation

```python
A = df[['age','years_experience','performance_score']].head(5).values
```

---

## ✅ Matrix Addition

```python
addition = A + B
```

---

## ✅ Matrix Multiplication

```python
multiplication = np.matmul(A, B)
```

---

## ✅ Matrix Transpose

```python
transpose = A.T
```

---

## ✅ Determinant

```python
A = df[['age','years_experience','performance_score']].head(3).values

determinant = np.linalg.det(A)

print("Determinant :", determinant)
```

---

## ✅ Inverse Matrix

```python
inverse = np.linalg.inv(A)
```

---

# 📈 Advanced Mathematics Concepts

## ✅ Covariance Matrix

```python
cov_matrix = np.cov(A.T)
```

---

## ✅ Eigenvalues & Eigenvectors

```python
eigenvalues, eigenvectors = np.linalg.eig(cov_matrix)
```

---

## ✅ LU Decomposition

```python
from scipy.linalg import lu

P, L, U = lu(A)
```

---

## ✅ Singular Value Decomposition (SVD)

```python
U, S, VT = np.linalg.svd(A)
```

---

# 🤖 Machine Learning Concepts

## ✅ Principal Component Analysis (PCA)

```python
from sklearn.decomposition import PCA

X = df[['age','years_experience','performance_score']]

pca = PCA(n_components=2)

pca_result = pca.fit_transform(X)

print(pca_result)
```

---

## ✅ Linear Discriminant Analysis (LDA)

```python
from sklearn.discriminant_analysis import LinearDiscriminantAnalysis

X = df[['age','years_experience','performance_score']]

y = df['department']

lda = LinearDiscriminantAnalysis(n_components=1)

lda_result = lda.fit_transform(X, y)

print(lda_result)
```

---

# ▶️ How to Run Project

## Step 1: Install Libraries

```bash
pip install numpy pandas scipy scikit-learn matplotlib
```

---

## Step 2: Open Jupyter Notebook

```bash
jupyter notebook
```

---

## Step 3: Run Notebook

```bash
Open pr5.ipynb
```

Run all cells.

---

# 📷 Output

The notebook generates:
- Vector calculations
- Matrix transformations
- PCA transformed data
- LDA transformed data
- Eigenvalues & Eigenvectors

---

# 👨‍💻 Author

Tirth Patel

---

# ⭐ GitHub Repository

https://github.com/Tirthdeveloper/project-5-maths
