# Mammographic Mass Classification via Soft Computing

## 1. Project Overview
This project compares three soft computing techniques—**Fuzzy Logic**, **Evolutionary Algorithm (GA)**, and a **Hybrid GA–Fuzzy approach**—for classifying mammographic masses as benign or malignant.  
The comparison is conducted from a **No Free Lunch (NFL) Theorem perspective**, highlighting trade-offs between accuracy, sensitivity, and interpretability.

---

## 2. Dataset Information
- Dataset: **Mammographic Mass Dataset**
- Source: **KEEL repository**
- Total instances used: **830** (after removing records with missing values)
- Task: Binary classification (Benign vs Malignant)

### Features
- BI-RADS
- Age
- Shape
- Margin
- Density

**Target Variable**
- Severity  
  - 0: Benign  
  - 1: Malignant  

---

## 3. Performance Summary

| Algorithm | Accuracy | Precision | Recall | F1-Score |
|---------|----------|-----------|--------|----------|
| Fuzzy Logic (Baseline) | 77.35% | 76.00% | 78.00% | 77.00% |
| Evolutionary (GA) | 77.51% | 69.14% | **91.66%** | 78.83% |
| Hybrid (GA–Fuzzy) | **81.66%** | **86.92%** | 70.45% | **77.82%** |

---

## 4. Key Findings (Simplified)

- **No Free Lunch Principle Confirmed**  
  No single algorithm performs best across all metrics.

- **Fuzzy Logic**
  - Moderate accuracy
  - Balanced recall
  - High interpretability
  - Suitable as a transparent baseline

- **Evolutionary Algorithm (GA)**
  - Extremely high recall (very sensitive to malignant cases)
  - Low precision and overall accuracy
  - Tends to over-predict malignant cases

- **Hybrid GA–Fuzzy**
  - Achieves the highest accuracy
  - Benefits from optimization while retaining fuzzy structure
  - Demonstrates the best performance trade-off

---

## 5. Software and Environment
- Language: Python 3.12
- Libraries: pandas, numpy, scikit-learn, scikit-fuzzy, matplotlib
- Platform: **Google Colab** (primary)

---

## 6. Project Structure
- `mammographic.dat`  
  Raw dataset file

- `mammographic (2).ipynb`  
  Baseline fuzzy classification implementation (Jain & Abraham, 2004)

- `GA_and_Hybrid_Mammographic_Mass.ipynb`  
  Genetic Algorithm and Hybrid GA–Fuzzy implementation

---

## 7. How to Run (Step-by-Step)

1. Open **Google Colab**
2. Upload the dataset:
   - Click the **file explorer icon** on the left panel
   - Upload `mammographic.dat`
3. Upload and open the desired notebook:
   - `mammographic (2).ipynb` for fuzzy baseline
   - `GA_and_Hybrid_Mammographic_Mass.ipynb` for GA and Hybrid models
4. Run all cells from top to bottom
5. Outputs include:
   - Accuracy
   - Precision, Recall, F1-score
   - Confusion Matrix and Heatmap

---

## 8. Reference
Jain, R., & Abraham, A. (2004).  
*A comparative study of fuzzy classification methods on breast cancer data*.  
Australasian Physical & Engineering Sciences in Medicine, 27(4), 213–218.
