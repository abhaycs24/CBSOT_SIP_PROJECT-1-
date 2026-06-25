# System Architecture Diagram

```text
[ Raw Telco Dataset ]
         │
         ▼
[ Data Engineering ] ──► (String Sanitization, Median Imputation, Scaling)
           │
           ▼
┌────────┴───────────────────────────────────────┐
▼                                                        ▼
[ Unsupervised Branch ]                      [ Supervised Branch ]
K-Means Clustering (K=4)                 Tuned Random Forest Classifier
        │                                           |
        ▼                                          ▼
Customer Profiling Dashboard         ROC-AUC & Feature Importances
