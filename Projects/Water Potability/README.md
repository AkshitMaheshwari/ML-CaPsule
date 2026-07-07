# Water Potability Prediction (ML)

## Project Overview

This project predicts whether a water sample is **potable (safe to drink)** using its **physicochemical properties**. It demonstrates an end-to-end **binary classification** machine learning workflow, from data preprocessing to model evaluation and prediction.

---

## Features

- Data preprocessing and cleaning
- Exploratory Data Analysis (EDA)
- Feature engineering
- Feature scaling
- Comparison of multiple classification models
- Model evaluation using:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - ROC-AUC
- Water potability prediction

---

## Dataset

This project uses the **Water Potability** dataset, which contains physicochemical properties of water samples along with their potability labels.

---

## Project Structure

```text
Projects/
└── Water Potability/
    ├── water_potability.ipynb
    ├── README.md
    ├── Water_Potability_Report.pdf

```

---

## Project Report

A detailed report containing the project methodology, data preprocessing, exploratory data analysis, model comparison, evaluation metrics, visualizations, and conclusions is available here:

**📄 [Water_Potability_Report.pdf](Water_Potability_Report.pdf)**

---

## Results

The notebook compares multiple machine learning models and evaluates them using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

The best-performing model is selected based on **ROC-AUC** and **F1-Score**.

---

## How to Run

1. Clone the repository.
2. Open `water_potability.ipynb` in Jupyter Notebook or VS Code.
3. Install the required Python libraries.
4. Run all notebook cells from top to bottom.
5. Refer to **Water_Potability_Report.pdf** for detailed analysis and results.

---

## Conclusion

- Missing values are handled appropriately.
- Feature scaling is applied where required.
- Multiple machine learning algorithms are compared.
- Performance is evaluated using standard classification metrics.
- The workflow demonstrates a complete machine learning classification pipeline.

---

## License

This project is licensed under the **MIT License**.