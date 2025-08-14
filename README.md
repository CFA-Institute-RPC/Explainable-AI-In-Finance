# 🧠 Explainable AI in Finance: Fundamental Factor Modeling

This repository explores how Explainable Artificial Intelligence (XAI) methods can be applied to machine learning models used for a case study in fundamental factor investing. It accompanies the [CFA Institute's report on 'Explainable AI in Finance: Addressing the Needs of Diverse Stakeholders' (2025)](https://rpc.cfainstitute.org/research/reports/2025/explainable-ai-in-finance), illustrating the practical use of post-hoc explainability tools in financial modeling.

## 📊 Project Overview

We implement a supervised learning workflow to predict monthly excess returns of stocks based on fundamental factor exposures using the `XGBRegressor` model from XGBoost. Our dataset contains normalized exposures to six BARRA-style factors across 218 stocks over a 100-month period starting in February 2008. We thank Bloomberg LP for use of the price and factor loadings data in this case study.

## 🧪 Workflow

1. **Data Preprocessing**  
   The data provided has already been re-scaled.

2. **Model Training**  
   - Split data into training and test sets  
   - Use cross-validation to optimize hyperparameters  
   - Train final model on full training set  

3. **Model Evaluation**  
   Assess predictive performance using root mean squared error (RMSE).

4. **Explainability Methods**  
   We apply multiple XAI methods to understand model behavior:
   - **Feature Importance**: Gain-based feature ranking from XGBoost
   - **Partial Dependence Plots (PDP)**: Global sensitivity to features
   - **Individual Conditional Expectation (ICE)**: Instance-level visual insights
   - **SHAP (SHapley Additive Explanations)**: Local and global contribution of features
   - **LIME (Local Interpretable Model-agnostic Explanations)**: Simplified local explanations

Each technique aligns with post-hoc explainability practices identified in the CFA Institute's XAI report and provides a unique lens into model transparency.

## 🔍 Key Themes

- **Post-Hoc Explainability**: Applied to an ensemble model (XGBoost), demonstrating outcome-based and instance-level interpretability.
- **Financial Relevance**: The model emulates a factor-investing strategy, a common use case in portfolio construction and performance attribution.
- **Stakeholder Interpretability**: Tools used here can support explainability needs for different users, such as quantitative analysts, model validators, and regulators.

## 🧰 Tech Stack

- Python 3.x  
- Jupyter Notebook  
- XGBoost  
- SHAP  
- LIME  
- Scikit-learn  
- Matplotlib

## 📁 Files

- `Notebook.ipynb`: Main notebook demonstrating modeling and explainability
- `data/`: Folder containing processed datasets
- `Plots/`: Folder containing SVG files of the Notebook plots
- `README.md`: Project overview and usage guide

## 📘 Reference

This notebook was developed to complement the CFA Institute’s research on human-centered AI systems in finance, particularly:

> *"Explainable AI in Finance: Addressing the Needs of Diverse Stakeholders (CFA Institute, 2025)"*

## 🤝 Contributing

Feel free to open issues or contribute improvements to expand examples, integrate more models (e.g., linear regression, neural networks), or include additional XAI methods (e.g., counterfactuals, rule-based models).

## 📜 License

MIT License

