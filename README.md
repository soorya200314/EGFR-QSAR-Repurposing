# EGFR-QSAR-Repurposing
# EGFR-Inhibitor-Discovery-ML
An intermediate QSAR project using XGBoost to predict IC50 values and repurpose FDA-approved drugs for EGFR inhibition.

## 📊 Project Overview
This project uses bioactivity data from the ChEMBL database to train a machine learning model capable of predicting the potency (pIC50) of small molecules against the Epidermal Growth Factor Receptor (EGFR). The screening was done on chembl itself for drugs on phase 3 clinical trials. Searched for smiles which is already on the training data for screening, and removed them for data integrity.

### Key Metrics
- **R-squared:** 0.519
- **RMSE:** 1.09
- **Algorithm:** XGBoost Regressor
- **Features:** Morgan Fingerprints (2048-bit) + RDKit Physicochemical Descriptors

## 🧬 Virtual Screening Results
The model screened ~2,000 clinical-stage molecules. Top hits identified include:
1. **Salmeterol Xinafoate** (pIC50: 9.09)
2. **Zanamivir** (pIC50: 9.03)
3. **Olsalazine** (pIC50: 8.94)

*Note: The model also identified high-sugar molecules (Sucrose/Lactulose) as hits, likely due to feature overlap in polyhydroxy groups. This highlights the importance of post-prediction chemical intuition.*

## 🚀 How to Run
1. Clone the repo: `git clone https://github.com/YOUR_USERNAME/EGFR-QSAR-Repurposing.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the notebook in Google Colab or Jupyter.
