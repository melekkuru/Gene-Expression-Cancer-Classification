# Gene Expression Analysis for Cancer Classification

Statistical learning and machine learning techniques applied to classify invasive vs. noninvasive breast cancer using gene expression data from 78 patients and 4,948 genes.

>  Developed as part of the **Applied Statistics (MA321)** module at the University of Essex.

---

## Overview

This project explores the Gene Expression Cancer dataset through two complementary analyses:

**Part 1 — Individual analysis** on a random subset of 10 genes, covering variance/covariance analysis, PCA, MANOVA, LDA, QDA, and median-based classification.

**Part 2 — Group analysis** on a random subset of 2,000 genes, applying a comprehensive pipeline of unsupervised and supervised learning methods including K-means, Hierarchical Clustering, Logistic Regression, LDA, QDA, KNN, Random Forest, SVM, and Decision Trees.

The goal is to identify which statistical and ML methods best classify cancer types from high-dimensional gene expression data.

---

## Methods & Results

### Unsupervised learning

| Method | Key finding |
|--------|-------------|
| PCA | 2,000 genes reduced to 4 principal components capturing majority of variance |
| K-means clustering | Optimal at K=6 with WCSS of 784.97 on first 4 PCs |
| Hierarchical clustering | Complete linkage with 2 clusters outperforms K-means (silhouette: 0.472) |

### Supervised learning

| Method | Accuracy | Notes |
|--------|----------|-------|
| Logistic Regression (L1) | 100% | Perfect classification on test set |
| Decision Tree | 100% | Perfect classification, simple and interpretable |
| Random Forest | 64.3% | Best feature importance insights |
| LDA | 71.4% | Moderate; sensitivity 66.7%, specificity 75% |
| QDA | 57.1% | Fair; limited by high dimensionality |
| KNN (k=13) | 64.3% | Moderate; high specificity (87.5%) |
| SVM | 50% | Poor; failed to identify invasive cases |

**Best models:** Logistic Regression and Decision Tree achieved perfect accuracy on the test set.

---

## Project structure

```
Gene-Expression-Cancer-Classification/
├── individual/
│   └── Gene_Expression_Analysis.R        # Individual analysis (10 genes)
├── group/
│   ├── MA321_Group_Project.Rmd           # Group analysis (2,000 genes)
│   └── MA321_Group_Project_Report.pdf    # Full report with results
├── data/
│   └── gene-expression-invasive-vs-noninvasive-cancer.csv
├── results/                              # Generated plots and figures
├── .gitignore
└── README.md
```

---

## Getting started

**Prerequisites:** R (4.0+) and RStudio

```r
# Install required packages
install.packages(c("ggplot2", "MASS", "cluster", "factoextra",
                   "caret", "glmnet", "e1071", "randomForest",
                   "rpart", "rpart.plot", "pROC", "fpc", "clValid"))
```

Open the `.R` or `.Rmd` files in RStudio to run the analyses.

---

## My contribution

- **Individual analysis:** Full pipeline — data exploration, PCA, MANOVA, LDA, QDA, classification
- **Group project:** K-means clustering implementation and analysis, appendix preparation
- Group project completed in collaboration with 4 team members under Dr. Berthold Lausen

---

## Technologies

R · ggplot2 · caret · MASS · glmnet · e1071 · randomForest · rpart · factoextra

---

## License

This project is for educational purposes. Feel free to use it as a reference.
