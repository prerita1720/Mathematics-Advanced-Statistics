# Calculative Foundation

### Linear Algebra Analysis on Student Performance Dataset

## 📌 Overview
Calculative Foundation is a project that applies core linear algebra concepts to a real-world dataset of student performance. Each student's subject scores are treated as a vector, and the project explores how fundamental math — vectors, matrices, eigenvalues, decompositions, and dimensionality reduction — forms the backbone of machine learning techniques like PCA and LDA.

## 📊 Dataset
**File:** `student_performance.csv`
- 200 students
- Columns: `Student_ID`, `Math`, `Science`, `English`, `History`, `Computer`, `Average_Score`, `Category`
- `Category` labels each student as **Above Average** or **Below Average**

## 🧮 Concepts Covered

### Part A — Vectors
- Representing each student's scores as a 5-element vector
- L1 and L2 norms
- Dot product and angle between vectors
- Cross product (3D subset)
- Vector projection

### Part B — Matrix Operations
- Forming a student × subject score matrix
- Matrix addition and multiplication
- Transpose
- Determinant and inverse

### Part C — Linear Transformations and Geometry
- Line (1D) — single subject
- Plane (2D) — two subjects
- Hyperplane (5D) — all subjects together
- Visualizing 1D, 2D, and 3D representations

### Part D — Eigenvalues and Decomposition
- Eigenvalues and eigenvectors of the covariance matrix
- LU Decomposition (P, L, U)
- Singular Value Decomposition (SVD)

### Part E — Dimensionality Reduction
- **PCA** — unsupervised reduction from 5D to 2D, preserving variance
- **LDA** — supervised reduction that separates Above Average vs Below Average students

## 🛠️ Tech Stack
- Python
- pandas, numpy
- scipy (LU decomposition)
- scikit-learn (PCA, LDA, LabelEncoder)
- matplotlib

## 📁 Project Files
- `Calculative_Foundation.ipynb` — main notebook with all code and visualizations
- `student_performance.csv` — dataset used throughout the project
- `Code_Implementation_Calculative.pdf` — written report explaining each concept with examples

## 🚀 How to Run
1. Install dependencies:
   ```
   pip install pandas numpy scipy scikit-learn matplotlib
   ```
2. Place `student_performance.csv` in the same directory as the notebook
3. Open and run `Calculative_Foundation.ipynb` cell by cell

## 🎯 Key Takeaways
- Real datasets can be represented and manipulated using pure linear algebra
- Eigen-decomposition and SVD reveal the underlying structure of data
- PCA finds patterns without labels; LDA uses labels to maximize class separation
- These same techniques form the mathematical foundation of modern machine learning models
