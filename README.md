# Odoh Kenneth Chidiebere

**Computational Chemist | Cheminformatics | ML-Guided Drug Discovery**

B.Sc. Chemistry, First Class Honours (Best Graduating Student, Department and Faculty)
Graduate Assistant Lecturer and M.Sc. Chemistry candidate, Air Force Institute of Technology (AFIT), Kaduna, Nigeria

[![LinkedIn](https://img.shields.io/badge/LinkedIn-kennethodoh-blue?logo=linkedin)](https://linkedin.com/in/kennethodoh)
[![GitHub](https://img.shields.io/badge/GitHub-KennethOdoh157-black?logo=github)](https://github.com/KennethOdoh157)
[![Email](https://img.shields.io/badge/Email-kennethodoh36%40gmail.com-lightgrey?logo=gmail)](mailto:kennethodoh36@gmail.com)

---

## About

I build end-to-end computational drug discovery pipelines that connect large natural product databases to molecular-level mechanistic insight. My independent research applies machine learning, structure-based virtual screening, molecular dynamics, and binding free energy calculation to identify candidate inhibitor scaffolds against drug-resistant parasitic targets, with a particular focus on African natural product chemical space.

My work sits at the intersection of cheminformatics, medicinal chemistry, and data science. I design reproducible, open-source workflows using Python, RDKit, GROMACS, AutoDock Vina, and AMBER tools, and two peer-reviewed manuscripts from this research programme are currently under review at PLOS Computational Biology.

In 2026 I was selected as an i-Scholar Initiative (iSI) Scholarship Awardee, one of 100 outstanding young Nigerians nationally supported toward international postgraduate applications.

---

## Featured Research

### Computational Discovery of Candidate PfDHFR Inhibitors from African Natural Products

> *Two linked manuscripts spanning QSAR modelling, virtual screening, molecular docking, molecular dynamics, binding free energy calculation, and ADMET profiling, targeting pyrimethamine-resistant* Plasmodium falciparum

[![Repo](https://img.shields.io/badge/Repository-pfdhfr--inhibitor--discovery-black?logo=github)](https://github.com/KennethOdoh157/pfdhfr-inhibitor-discovery)
![Status](https://img.shields.io/badge/Status-Complete-success)
![Manuscripts](https://img.shields.io/badge/Manuscripts-Under%20Review%20at%20PLOS%20Comp%20Biol-orange)

Pyrimethamine-resistant malaria caused by the K1 quadruple mutant (*Pf*DHFR; N51I/C59R/S108N/I164L) remains one of the most urgent unmet needs in antimalarial drug discovery. This work provides a systematic computational evaluation of African natural products from the COCONUT database against this resistant target, building a complete pipeline from database construction through molecular dynamics, binding free energy calculation, and pharmacokinetic screening.

**Pipeline summary**

| Stage | Method | Output |
|-------|--------|--------|
| Database construction | COCONUT Oct 2024, NPASS 3.0, AfroDb annotation | 695,133 compounds indexed |
| QSAR modeling | Random Forest, XGBoost, SVM, stacking ensemble on ChEMBL DHFR bioactivity | AUC-ROC = 0.861, MCC = 0.583 |
| Virtual screening | 5-stage cascade with tiered African NP threshold | 302 docking candidates |
| Molecular docking | AutoDock Vina 1.2.5 against PDB 1J3I (K1 resistant strain) | Best score minus 11.86 kcal/mol |
| Molecular dynamics | GROMACS 2023.3, AMBER99SB-ILDN + GAFF2, 100 ns, T4 GPU | All hits stable; ASP54 H-bond at 94.2% occupancy |
| Binding free energy | gmx_MMPBSA, single-trajectory MM-GBSA and MM-PBSA, per-residue decomposition | 2 of 3 hits exceed pyrimethamine in binding enthalpy |
| ADMET and toxicity | ADMET-AI, 98 endpoints across 13 compounds | Strongest binder shows weakest predicted absorption |

**Key findings**

- All 10 top-ranked docking hits are African natural products (Mann-Whitney p = 0.0049, effect size modest at r = 0.188)
- Best hit CNP0286261 achieves a predicted docking score of minus 11.86 kcal/mol versus minus 6.90 kcal/mol for pyrimethamine
- A methodological finding with broader implications: no African natural product in COCONUT exceeded p(active) = 0.50 under a standard QSAR filter, reflecting a genuine chemical space gap between African secondary metabolites and synthetic antifolate training data; a tiered threshold strategy was developed and validated as the solution
- CNP0539885 maintains an ASP54:OD2 hydrogen bond at 94.2% occupancy during molecular dynamics, markedly more persistent than pyrimethamine's top contact at 31.7% under the same simulated conditions
- Binding free energy calculation confirms two of three lead compounds exceed pyrimethamine in binding enthalpy, with CNP0539885 reaching minus 33.89 kcal/mol by MM-GBSA
- Per-residue energy decomposition shows all three natural product hits, but not pyrimethamine, contact ASN51, the K1 resistance mutation site, within the binding pocket, a structural rationale for retained activity against a resistance-compromised target
- ADMET profiling reveals that predicted binding strength does not track with predicted drug developability: the strongest binder carries the highest predicted toxicity risk and weakest predicted oral absorption of the three leads, demonstrating that binding free energy and ADMET screening are necessary complements rather than substitutes

**Tools and stack**

RDKit 2024.03.6, scikit-learn, XGBoost, SHAP, AutoDock Vina 1.2.5, Meeko, ACPYPE, GROMACS 2023.3 (CUDA), gmx_MMPBSA, AmberTools, MDAnalysis 2.10.0, ADMET-AI, Chemprop, PyMOL 3.1.0, ffmpeg, Python 3.11, WSL2 Ubuntu

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
RDKit, AutoDock Vina, GROMACS, gmx_MMPBSA, AmberTools, MDAnalysis, ACPYPE, Meeko, PyMOL, ADMET-AI, Chemprop, SHAP, OpenBabel, MGLTools

**Machine learning and data science**
scikit-learn, XGBoost, Random Forest, SVM, stacking ensembles, SHAP interpretability, pandas, NumPy, matplotlib, seaborn

**Programming and tools**
Python 3.11, SQL (T-SQL), Jupyter Notebooks, VS Code, Git, WSL2 Ubuntu, Google Colab Pro, conda environment management

**Databases and resources**
COCONUT, NPASS, AfroDb, ChEMBL, PubChem, PDB, Therapeutics Data Commons

---

## Education and Appointments

**Graduate Assistant Lecturer**, Department of Chemistry
Air Force Institute of Technology (AFIT), Kaduna, Nigeria (appointed on merit, 2026)

**M.Sc. Chemistry** (in progress, 2025/2026 to 2026/2027)
Air Force Institute of Technology (AFIT), Kaduna, Nigeria

**B.Sc. Chemistry, First Class Honours**
Air Force Institute of Technology (AFIT), Kaduna, Nigeria
CGPA: 4.82/5.00, Best Graduating Student, Department of Chemistry and Faculty of Science

**i-Scholar Initiative (iSI) 2026 Scholarship Awardee**
One of 100 outstanding young Nigerians selected nationally for the iSI Scholarship and Mentorship Programme

---

## Research Interests

- Computational drug discovery against neglected tropical diseases and drug-resistant pathogens
- Binding free energy calculation and ADMET screening as complementary stages in candidate prioritisation
- Machine learning for bioactivity prediction and natural product virtual screening
- African natural product databases as sources of structurally distinct lead compounds
- Reproducible, open-source cheminformatics workflows

---

## Contact

Open to PhD opportunities, research collaborations, and computational chemistry roles.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://linkedin.com/in/kennethodoh)
[![Email](https://img.shields.io/badge/Email-kennethodoh36%40gmail.com-lightgrey?logo=gmail)](mailto:kennethodoh36@gmail.com)
