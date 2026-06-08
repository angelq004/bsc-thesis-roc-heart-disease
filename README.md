# Study of the ROC curve and its application to the diagnosis of heart disease using machine learning

This repository contains the code for the practical section of the Bachelor's Thesis (TFG) for the Degree in Computational Mathematics at Universitat Jaume I (UJI). 

The main objective of this code is to evaluate the performance of different binary classification models applied to clinical diagnosis, with a special focus on ROC curve analysis, the binormal assumption, and the optimization of the clinical decision threshold using the Generalized Youden Index ($J_r$).

## 🛠️ Technologies and Dependencies

The project is developed in **Python** using **Jupyter Notebook**. The main libraries used are:
* `pandas` and `numpy` for data processing and manipulation.
* `scikit-learn` for model training, metrics, and ROC curve calculations.
* `scipy` for calculating statistics under the normality assumption (binormal ROC curve).
* `matplotlib` for plotting graphs.
* `joblib` for persisting the trained models.

To install the dependencies, it is recommended to use a virtual environment and run:
```bash
pip install pandas numpy scikit-learn scipy matplotlib joblib jupyter
```

## 📂 Repository Structure

* `heart.csv`: Original dataset used for the study, extracted from the **[Heart Disease Prediction using Machine Learning](https://www.kaggle.com/code/tushardobal/heart-disease-prediction-using-machine-learning)** dataset.
* `heart_disease_classifier.ipynb`: Main Jupyter Notebook that contains the data pipeline, training, evaluation of the models, and visual outputs.
* `modelo_arbol.pkl`: Trained and exported Decision Tree model, ready to be loaded into production systems.

## 🚀 Execution Instructions

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/angelquecas/bsc-thesis-roc-heart-disease.git
   ```
2. Make sure the `heart.csv` file is in the same directory as the notebook.
3. Launch Jupyter Notebook or JupyterLab from your terminal:
   ```bash
   jupyter notebook
   ```
4. Open the `heart_disease_classifier.ipynb` file and run all the cells sequentially. 
   *Note: The execution will generate the ROC curve graphs (empirical and binormal), the Gaussian distribution bells, and the tree structure directly within the notebook, in addition to printing the statistics and confusion matrices.*

## 📊 Summary of Key Results

The code trains two predictive models: **Logistic Regression** and **Decision Tree**. The Decision Tree model achieved the best overall performance with an Area Under the Curve (AUC) of **0.9334**.

One of the key contributions of the project is the application of asymmetric costs to the diagnosis. Given a cost ratio of $C_{FP}/C_{FN} = 0.2$ and the parameter $r \approx 0.2134$, the application of the **Generalized Youden Index** proved to be vital:
* **Standard threshold (0.5):** 18 False Negatives.
* **Optimal generalized threshold (0.1739):** 6 False Negatives.

This drastic reduction in the false negative rate prioritizes the detection of the disease, adjusting to the clinical reality required for heart diseases.

## 📄 Thesis Document

The complete document of the Bachelor's Thesis will be available through the official UJI library repository once officially published.

👉 **[Currently pending publication]**

## 👨‍🎓 Authorship
 Àngel Queral Castell
