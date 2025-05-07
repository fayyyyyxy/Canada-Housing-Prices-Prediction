# Canada Housing Price Prediction

Final project for **CS 334** at **Emory University**.

**Group Members:**  
- Yaxuan (Lily) Liu  
- Xinyue (Fay) Yan

**Abstract**

This project aims to develop predictive machine learning models for housing prices in Canada using a property-level dataset sourced from Remax Canada. To address geographic features and market heterogeneity, we divided the data into four meaningful subsets: High Population, Resource-Rich, Smaller Population, and Luxury Market. We applied data preprocessing techniques, including encoding and scaling, to ensure consistent model training and a fair comparison, and did feature selection to reduce dimensionality and improve interpretability. We evaluated different models, including Linear Regression, Ridge Regression, Decision Tree, Random Forest, and Gradient Boosting, and developed a stacked meta regressor using the best parameters gained in the hyperparameter tuning process. Our results showed that the meta regressor generated the best performance with high R² and comparatively low RMSE. We found that data segmentation based on market conditions and including informative location features improves predictability. 

**Dataset:**  
Data sourced from Kaggle: [Canada Housing Price Data](https://www.kaggle.com/datasets/kimjihoo/canadian-housing-data)

**Project Structure:**
- `Under.ipynb` – Complete pipeline (preprocessing, feature selection, model training, evaluation, and tuning) for properties priced under 2.5 million CAD. This includes three subsets:
  - **High Population Area**: ON, QC, BC
  - **Resource-Rich Area**: AB, SK, MB
  - **Smaller Population Area**: All other provinces
- `Over.ipynb` – Complete pipeline for the **Luxury Market** subset, which includes all properties priced over 2.5 million CAD.

Both scripts contain code for data preprocessing, model training (linear and ensemble-based), hyperparameter tuning, and evaluation. Each subset is modeled and analyzed separately to capture region- and price-specific dynamics.

**Key Methods:**
- **Subset-specific modeling** – Applied baseline linear regression, regularized linear models (Ridge), and ensemble methods (Decision Tree, Random Forest, Gradient Boosting) across four subsets.
- **Hyperparameter tuning** – Used grid search with cross-validation to optimize model performance.
- **Stacking ensemble (Meta Regressor)** – Combined predictions from base models using a Linear Regression meta-model to improve accuracy and generalization.

**Discussion:**  
See the attached Report for a detailed discussion of methods, model performance, and evaluations.
