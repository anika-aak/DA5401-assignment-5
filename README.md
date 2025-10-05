# DA5401-assignment-5
# DA5401 Assignment 5 — Manifold Visualization and Data Veracity

> **Note:** Apologies for the slight delay in submission. The extended runtime for manifold embeddings and verification plots required additional validation to ensure reproducible and interpretable results.

---

## Overview

This notebook fulfills all objectives of **DA5401 – Assignment 5: Manifold Visualization**, applied on the **Yeast multi-label dataset**.  
It demonstrates the role of **non-linear dimensionality reduction** (t-SNE, Isomap) in exploring label veracity issues such as **outliers, ambiguity,** and **hard-to-learn samples**.

The notebook is structured to be completely reproducible in **Google Colab**.

---

## Contents

| Section | Description |
|----------|--------------|
| **0. Upload & Setup** | Upload `yeast.arff` and import libraries. |
| **1. Data Loading** | Reads ARFF, splits 103 features + 14 labels, verifies schema. |
| **2. Category Construction** | Builds 4-way simplified categories: Top Single A, Top Single B, Top Multi-label Combo, and Other. |
| **3. Scaling** | Standardizes all features (mean 0, std 1) before manifold learning. |
| **4. t-SNE Exploration** | Visualizes data at perplexities 5, 30, 50 → final at 30. |
| **5. Veracity Inspection** | Qualitative analysis of noisy/ambiguous/outlier zones in t-SNE plots. |
| **6. Isomap Embedding** | Preserves global geodesic structure; compared against t-SNE. |
| **7. Automated Diagnostics** | Adds quantitative veracity analysis: LOF outliers, neighbor mismatch ambiguity, local label entropy. |
| **8. Visualization Overlays** | Overlays all diagnostics on t-SNE embedding with annotated legends. |
| **9. Discussion Prompts** | Markdown cells for interpretation and report notes. |



---

## Key Features

- **Upload Flexibility:** Works with both `yeast.arff` and `yeast.csv` formats.  
- **Dimensionality Reduction:** Implements t-SNE (3 perplexities) + Isomap (k = 10).  
- **Veracity Metrics:**
  - **Local Outlier Factor (LOF)** – detects anomalies in feature space.  
  - **Ambiguity Score** – measures neighborhood label mismatch in t-SNE space.  
  - **Local Label Entropy** – quantifies “hard-to-learn” zones with mixed labels.  
- **Overlay Plot:** Visual comparison of outliers, ambiguous points, and high-entropy samples.  
- **Reproducibility:** All random seeds fixed (`random_state = 42`).  

## Deliverables

- **Visual Evidence:** Comparative t-SNE and Isomap plots with clear legends.  
- **Quantitative Diagnostics:** LOF outlier indices, ambiguous sample count, entropy threshold.  
- **Interpretive Write-up:**  
  - Discussion of noisy / ambiguous / hard-to-learn regions.  
  - Comparative insight on global vs local manifold structure.  
 
**Submission Date:** October 5, 2025
