# Sphingolipid Remodeling Regulates TRPV6 Activity in TNBC  
**A Machine-Learning & Single-Cell Transcriptomic Analysis**

## 🚀 Project Overview
This project investigates the relationship between **sphingolipid pathway activity** and **TRPV6 expression** in tumor cells from **triple-negative breast cancer (TNBC)** patients. Using **single-cell RNA-seq data**, we identify tumor cell subpopulations, compute sphingolipid scores, and build **explainable machine learning models** to predict TRPV6-high cells.

---

## 🎯 Aim & Hypotheses

**Aim:**  
Identify tumor cell subpopulations in TNBC where TRPV6 is overexpressed, test whether sphingolipid-pathway activity predicts TRPV6-high states, and build explainable ML models that reveal lipid-gene drivers.

**Hypotheses:**  
- **H1:** A sphingolipid gene expression signature (sphingolipid score) is positively associated with TRPV6 expression in a subset of tumor cells.  
- **H2:** An ML model trained on sphingolipid genes can predict TRPV6-high cells with biologically meaningful feature importance (e.g., SGMS2, CERS family).  
- **H3 (exploratory):** TRPV6-high/sphingolipid-high cells show aggressive phenotypes (proliferation, EMT, stemness).

---

## 🧩 Project Phases

**PHASE 0 — Environment Setup**  
- Install packages, create folder structure, set global paths

**PHASE 1 — Load Raw Data**  
- Load GSE176078 scRNA-seq data (genes, barcodes, matrix)  
- Convert to AnnData and merge all samples  

**PHASE 2 — Quality Control**  
- Filter cells and genes, compute mitochondrial percentage, remove low-quality cells  

**PHASE 3 — Normalization + HVGs**  
- Normalize counts, log-transform, identify 3,000 highly variable genes (HVGs)  

**PHASE 4 — Integration / Batch Correction**  
- Run Harmony (or BBKNN), PCA, neighbors, UMAP  

**PHASE 5 — Clustering**  
- Leiden clustering at multiple resolutions  

**PHASE 6 — Cell-Type Annotation**  
- Identify epithelial/tumor cells using marker genes  

**PHASE 7 — TRPV6 Expression Analysis**  
- Extract TRPV6 expression, define TRPV6-high cells, visualize UMAPs and violin plots  

**PHASE 8 — Sphingolipid Score**  
- Define sphingolipid gene list, score cells, correlate with TRPV6  

**PHASE 9 — Exploratory Analysis**  
- Correlation analysis, differential expression, pathway enrichment  

**PHASE 10 — Machine Learning**  
- Prepare features & labels, patient-aware cross-validation, train ML models, evaluate performance (AUROC, AUPRC), SHAP feature importance  

**PHASE 11 — Robustness Tests**  
- Permutation tests, ablation of genes, validation with external TNBC datasets  

**PHASE 12 — Final Outputs**  
- All processed `.h5ad` files, figures, summary PDF, GitHub repository

---

## 🛠️ Technologies & Tools
- **Python** (Scanpy, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SHAP)  
- **Single-cell RNA-seq** (AnnData, GSE176078 dataset)  
- **Machine Learning** (Gradient Boosting, Random Forest, XGBoost)  
- **Visualization** (UMAP, Violin plots, Heatmaps)  

## 📈 Expected Outcomes
- Identification of TRPV6-high tumor subpopulations  
- Sphingolipid score correlations with TRPV6  
- Explainable ML models highlighting key lipid-gene drivers  
- Figures and outputs ready for publication or portfolio showcase  

---

## 📜 References
- GSE176078 dataset  
- Relevant literature on TRPV6, sphingolipids, TNBC  

---

## ⚡ Author
**Fakhia Mubashir** – B.Sc. Zoology, Molecular Biology & Bioinformatics Research  
