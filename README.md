# Bipolar Disorder Detection using Machine Learning with Shapley Additive Explanations

This repository contains the final versions of the Jupyter notebooks used in our research aimed at detecting bipolar disorder through crowdsourced symptoms, leveraging machine learning techniques and Shapley Additive Explanations (SHAP) for interpretability.

## Project Overview
Bipolar disorder is a mental health condition characterized by extreme mood swings, ranging from manic highs to depressive lows. Early detection is crucial to prevent the disorder's progression and to ensure timely intervention. This project focuses on building machine learning models that classify whether an individual may have bipolar disorder based on their reported symptoms, which were crowdsourced as free-text responses.

The key objectives of this project include:
- Transforming free-text symptoms into structured binary features using **Natural Language Processing (NLP)** techniques.
- Building machine learning models, such as **Support Vector Machines (SVM)** and **Penalized Logistic Regression (PLR)**, for classification.
- Applying **Shapley Additive Explanations (SHAP)** to make the models interpretable by quantifying the contribution of each feature to the model’s predictions.

## Repository Contents
This repository contains two main Jupyter notebooks:
- **Bipolar_Modelling_final.ipynb**: This notebook includes the final implementation of the machine learning models. Several models were tested, including Support Vector Machines (SVM) with various kernels and Penalized Logistic Regression (PLR) with different regularization techniques.
- **Bipolar_Feature_Extraction_final.ipynb**: This notebook is responsible for feature extraction. It performs natural language processing (NLP) techniques to transform the free-text symptoms into binary feature matrices suitable for input into machine learning models.

## Data and Confidentiality Notice
The dataset used for this project contains sensitive, crowdsourced information about participants' mental health. Due to the confidential nature of the data, it **cannot be shared publicly** in this repository. The data was anonymized following **General Data Protection Regulation (GDPR)** guidelines, ensuring that the participants’ identities remain protected.

If you are interested in using the data for academic research or other legitimate purposes, please contact the project authors directly to discuss access.

## Machine Learning Models
The following models were developed and tested in this project:
- **Support Vector Machine (SVM)**: Various kernels (linear, polynomial, radial basis function, and sigmoid) were used to model the relationship between the features and bipolar disorder classification.
- **Penalized Logistic Regression (PLR)**: PLR models with different regularization techniques, such as L1, L2, and elastic-net penalties, were used to optimize classification performance.
  
The **SVM with a sigmoid kernel** and the **PLR with elastic-net regularization** emerged as the top-performing models, achieving:
- Precision: 0.70
- Recall: 0.78
- F1-Score: 0.74
- Accuracy: 0.88

## Model Performance Results

| Model                  | Precision | Recall | F1 Score | Accuracy |
|------------------------|-----------|--------|----------|----------|
| Logistic Regression     | 0.54      | 0.78   | 0.64     | 0.81     |
| PLR - L1 Penalty        | 0.70      | 0.78   | 0.74     | 0.88     |
| PLR - L2 Penalty        | 0.67      | 0.67   | 0.67     | 0.86     |
| PLR - Elastic-Net       | 0.70      | 0.78   | 0.74     | 0.88     |
| SVM - Linear Kernel     | 0.62      | 0.56   | 0.59     | 0.84     |
| SVM - Polynomial Kernel | 0.67      | 0.22   | 0.33     | 0.81     |
| SVM - RBF Kernel        | 0.83      | 0.56   | 0.67     | 0.88     |
| SVM - Sigmoid Kernel    | 0.70      | 0.78   | 0.74     | 0.88     |

### Key Metrics Explained:
- **Precision**: Measures how many of the predicted positive cases were actually correct.
- **Recall**: Measures how many actual positive cases were correctly identified.
- **F1 Score**: The harmonic mean of precision and recall, offering a balance between the two.
- **Accuracy**: The percentage of total predictions that were correct.

## Explainability with SHAP
In high-stakes fields like healthcare, model explainability is essential. We used **Shapley Additive Explanations (SHAP)** to provide insights into the predictions made by our models. SHAP helps identify which symptoms (features) contributed most to the classification of bipolar disorder.

Key features identified by SHAP include:
- **Depressive symptoms**
- **Unstable mood**
- **Extreme anxiety**
- **Suicidal thoughts**

## Publication and Conference
This research is set to be presented at the **9th International Conference on Computer Science and Computational Intelligence (ICCSCI 2024)**, held on **August 28-29, 2024**. The manuscript associated with this work is currently under review for inclusion in the conference proceedings.

## Acknowledgments
We would like to thank **Meta Lab (PT Meta Lab Nusantara)** for their role in crowdsourcing the mental health symptoms data that made this research possible.

## License
This repository is licensed under the **CC BY-NC-ND 4.0 License**. For more information, please see the [LICENSE](https://creativecommons.org/licenses/by-nc-nd/4.0/) file.
