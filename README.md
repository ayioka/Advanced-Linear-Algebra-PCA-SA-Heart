
# Advanced Linear Algebra – Principal Component Analysis (PCA)

 Project Overview
This project implements **Principal Component Analysis (PCA) from scratch** using concepts from **advanced linear algebra**, including covariance matrices, eigenvalues, and eigenvectors. The goal is to reduce the dimensionality of a real-world, Africanized dataset while preserving as much variance as possible.

The implementation strictly avoids high-level PCA libraries and focuses on the mathematical foundations of PCA.

---

 Dataset
**Dataset:** South African Heart Disease Dataset (`SA_heart.csv`)

**Why this dataset was chosen:**
- African health context
- Contains **missing values**
- Includes **non-numeric (categorical) data**
- More than 10 features
- Suitable for demonstrating real-world PCA preprocessing challenges

---
 Data Preprocessing
The following preprocessing steps were applied:
- Handling missing values:
  - Median imputation for skewed numerical features
  - Mean imputation where appropriate
  - Mode imputation for categorical variables
- Encoding categorical data (`famhist`)
- Removal of index-like identifiers (`ind`)
- Standardization using NumPy only:
  \[
  z = \frac{x - \mu}{\sigma}
  \]

---

PCA Implementation (From Scratch)
The PCA pipeline includes:
1. Data standardization
2. Covariance matrix computation
3. Eigendecomposition of the covariance matrix
4. Sorting eigenvalues and eigenvectors in descending order
5. Selection of principal components
6. Projection of data onto lower-dimensional space

No PCA functions from `scikit-learn` were used.

---

##  Explained Variance
Explained variance is calculated using eigenvalues to determine how much information each principal component retains. The principal components are ordered by descending eigenvalues to ensure that the most informative components are selected first.

---

##  Visualization
The notebook includes:
- A scatter plot of the **original standardized feature space**
- A scatter plot of the **PCA-transformed data (PC1 vs PC2)**

These visualizations demonstrate how PCA rotates the data and concentrates variance along the first principal component.

---

##  Repository Structure
```

Advanced-Linear-Algebra-PCA-SA-Heart/
├── notebook/
│   └── Template_PCA_Formative_1.ipynb
├── README.md
└── requirements.txt

````

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/ayioka/Advanced-Linear-Algebra-PCA-SA-Heart.git
````

2. Navigate into the project:

   ```bash
   cd Advanced-Linear-Algebra-PCA-SA-Heart
   ```
3. Open the notebook:

   ```bash
   jupyter notebook
   ```
4. Run all cells in order to view outputs and visualizations.

---

##  Requirements

Install dependencies using:

```bash
pip install numpy pandas matplotlib seaborn
```

---

##  Course Information

**Course:** Advanced Linear Algebra
**Assignment:** Formative 1 – Principal Component Analysis
**Student:** Shem Ayioka
**Facilitator** Marvin
---


