# bsc-thesis-roc-heart-disease
# Study of the ROC curve and its application to the diagnosis of heart disease using machine learning

This repository contains the code for the practical section of the Bachelor's Thesis (TFG) for the Degree in Computational Mathematics at Universitat Jaume I (UJI). 

The main objective of this code is to evaluate the performance of different binary classification models applied to clinical diagnosis, with a special focus on ROC curve analysis, the binormal assumption, and the optimization of the clinical decision threshold using the Generalized Youden Index ($J_r$).

## 🛠️ Technologies and dependencies

The project is developed in **Python**. The main libraries used are:
* `pandas` and `numpy` for data processing and manipulation.
* `scikit-learn` for model training, metrics, and ROC curve calculations.
* `scipy` for calculating statistics under the normality assumption (binormal ROC curve).
* `matplotlib` for plotting graphs.
* `joblib` for persisting the trained models.

To install the dependencies, it is recommended to use a virtual environment and run:
```bash
pip install pandas numpy scikit-learn scipy matplotlib joblib
📂 Repository Structureheart.csv: Original dataset used for the study, extracted from the Heart Disease Prediction using Machine Learning dataset.codigo_principal.py: Main script that runs the data pipeline, training, and evaluation of the models.modelo_arbol.pkl: Trained and exported Decision Tree model, ready to be loaded into production systems.arbol_entrenado_tfg.png: Visual representation of the rules extracted by the decision tree in its first levels.🚀 Execution InstructionsClone this repository to your local machine:Bash   git clone [INSERT_YOUR_REPOSITORY_LINK_HERE]
Make sure the heart.csv file is in the same directory as the script.Run the main script from the terminal:Bash   python codigo_principal.py
Note: The execution will sequentially generate the ROC curve graphs (empirical and binormal), the Gaussian distribution bells, and the tree structure, in addition to printing the statistics and confusion matrices to the console.📊 Summary of Key ResultsThe code trains two predictive models: Logistic Regression and Decision Tree. The Decision Tree model achieved the best overall performance with an Area Under the Curve (AUC) of 0.9334.One of the key contributions of the project is the application of asymmetric costs to the diagnosis. Given a cost ratio of $C_{FP}/C_{FN} = 0.2$ and the parameter $r \approx 0.2134$, the application of the Generalized Youden Index proved to be vital:Standard threshold (0.5): 18 False Negatives.Optimal generalized threshold (0.1739): 6 False Negatives.This drastic reduction in the false negative rate prioritizes the detection of the disease, adjusting to the clinical reality required for heart diseases.📄 Thesis DocumentThe complete document of the Bachelor's Thesis can be viewed and downloaded through the official UJI library repository at the following link:👉 Link to the Thesis Document👨‍🎓 AuthorshipAuthor: Àngel Queral Castell
