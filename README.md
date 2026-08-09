# Kenneth Odoh Chidiebere

**Computational Chemist | Cheminformatics | ML-Guided Drug Discovery**

B.Sc. Chemistry, First Class Honours — Best Graduating Student, Department and Faculty  
Air Force Institute of Technology (AFIT), Kaduna, Nigeria

[![LinkedIn](https://img.shields.io/badge/LinkedIn-kennethodoh-blue?logo=linkedin)](https://linkedin.com/in/kennethodoh)
[![GitHub](https://img.shields.io/badge/GitHub-KennethOdoh157-black?logo=github)](https://github.com/KennethOdoh157)

---

## About

I build end-to-end computational drug discovery pipelines that connect large natural product databases to molecular-level mechanistic insight. My independent research applies machine learning, structure-based virtual screening, and molecular dynamics to identify novel inhibitor scaffolds against drug-resistant parasitic targets, with a particular focus on African natural product chemical space.

My work sits at the intersection of cheminformatics, medicinal chemistry, and data science. I design reproducible, open-source workflows using Python, RDKit, GROMACS, and AutoDock Vina, and I am actively preparing peer-reviewed manuscripts from completed pipelines.

---

## Featured Research

### Computational Discovery of PfDHFR Inhibitors from African Natural Products

> *An integrated QSAR, virtual screening, molecular docking and molecular dynamics pipeline targeting pyrimethamine-resistant* Plasmodium falciparum

[![Repo](https://img.shields.io/badge/Repository-pfdhfr--inhibitor--discovery-black?logo=github)](https://github.com/KennethOdoh157/pfdhfr-inhibitor-discovery)
![Status](https://img.shields.io/badge/Status-Complete-success)
![Manuscript](https://img.shields.io/badge/Manuscript-In%20Preparation-orange)

Pyrimethamine-resistant malaria caused by the K1 quadruple mutant (*Pf*DHFR; N51I/C59R/S108N/I164L) remains one of the most urgent unmet needs in antimalarial drug discovery. This project is the first systematic computational evaluation of African natural products from the COCONUT database against this resistant target, building a complete pipeline from database construction through 100 ns GPU molecular dynamics simulations.

**Pipeline summary**

| Stage | Method | Output |
|-------|--------|--------|
| Database construction | COCONUT Oct 2024, NPASS 3.0, AfroDb annotation | 695,133 compounds indexed |
| QSAR modeling | Random Forest, XGBoost, SVM, stacking ensemble on ChEMBL DHFR bioactivity | AUC-ROC = 0.861, MCC = 0.583 |
| Virtual screening | 5-stage cascade with tiered African NP threshold | 302 docking candidates |
| Molecular docking | AutoDock Vina 1.2.5 against PDB 1J3I (K1 resistant strain) | Best hit -11.86 kcal/mol |
| Molecular dynamics | GROMACS 2023.3, AMBER99SB-ILDN + GAFF2, 100 ns, T4 GPU | All hits stable; ASP54 H-bond at 94.2% occupancy |

**Key findings**

- All 10 top-ranked docking hits are African natural products (Mann-Whitney p = 0.0049)
- Best hit CNP0286261 achieves -11.86 kcal/mol versus pyrimethamine at -6.90 kcal/mol
- A methodological finding with broader implications: no African natural product in COCONUT exceeded p(active) = 0.50 under a standard QSAR filter, reflecting a genuine chemical space gap between African secondary metabolites and synthetic antifolate training data; a tiered threshold strategy was developed and validated as the solution
- CNP0539885 maintains ASP54:OD2 hydrogen bond at 94.2% occupancy, far exceeding pyrimethamine's top contact at 31.7%
- CNP0286261 engages the ASN51 resistance mutation site at 73% contact frequency, suggesting a mechanism for exploiting rather than avoiding the resistant active site

**Tools and stack**

RDKit 2024.03.6, scikit-learn, XGBoost, SHAP, AutoDock Vina 1.2.5, Meeko, ACPYPE, GROMACS 2023.3 (CUDA), MDAnalysis 2.10.0, PyMOL 3.1.0, ffmpeg, Python 3.11

---

## Other Projects

### Drug-Likeness and Toxicity Prediction Pipeline

[![Repo](https://img.shields.io/badge/Repository-view%20project-black?logo=github)](https://github.com/KennethOdoh157)
![Status](https://img.shields.io/badge/Status-Complete-success)

An end-to-end cheminformatics and machine learning pipeline for early-stage compound prioritisation using the Tox21 dataset. Twelve assay-specific toxicity classifiers were trained and integrated with Lipinski's Rule of Five and QED drug-likeness scoring to identify compounds in a high drug-likeness, low-toxicity region of chemical space.

- 12 binary assay-specific classifiers (Random Forest) trained on Tox21
- Top assay performance: SR-MMP AUC = 0.93, NR-AhR AUC = 0.84
- SHAP feature importance for model interpretability
- Integration of ML predictions with medicinal chemistry heuristics for risk-aware compound prioritisation

**Tools:** RDKit, scikit-learn, SHAP, pandas, matplotlib, Python 3.10

---

### E-Commerce Data Analytics Pipeline

An analytics engineering pipeline covering dimensional modeling, data warehousing, and business insight generation from raw transactional data.

- Star schema dimensional modeling in T-SQL
- Power BI dashboards for business-oriented reporting
- End-to-end from raw data ingestion to actionable insight

**Tools:** SQL (T-SQL), Power BI, Python, pandas

---

## Technical Skills

**Computational chemistry and cheminformatics**
RDKit, AutoDock Vina, GROMACS, MDAnalysis, ACPYPE, Meeko, PyMOL, SHAP, OpenBabel, MGLTools

**Machine learning and data science**
scikit-learn, XGBoost, Random Forest, SVM, stacking ensembles, SHAP interpretability, pandas, NumPy, matplotlib, seaborn

**Programming and tools**
Python 3.11, SQL (T-SQL), Jupyter Notebooks, VS Code, Git, Google Colab Pro, conda environment management

**Databases and resources**
COCONUT, NPASS, AfroDb, ChEMBL, PubChem, PDB

---

## Education

**M.Sc. Chemistry** (in progress)
Air Force Institute of Technology (AFIT), Kaduna, Nigeria

**B.Sc. Chemistry, First Class Honours**
Air Force Institute of Technology (AFIT), Kaduna, Nigeria
CGPA: 4.82/5.00 — Best Graduating Student, Department of Chemistry and Faculty of Science

---

## Research Interests

- Computational drug discovery against neglected tropical diseases and drug-resistant pathogens
- Machine learning for bioactivity prediction and natural product virtual screening
- African natural product databases as sources of structurally novel lead compounds
- Reproducible, open-source cheminformatics workflows

---

## Contact

Open to PhD opportunities, research collaborations, and computational chemistry roles.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://linkedin.com/in/kennethodoh)
