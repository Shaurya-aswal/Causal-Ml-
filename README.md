# Causal ML

This repository contains a small causal machine learning project built around hotel booking cancellation analysis and uplift modeling.

The work is organized into two main parts:

- a causal uplift modeling experiment in [causalml_experiment/casual_uplift_model.ipynb](causalml_experiment/casual_uplift_model.ipynb)
- a booking cancellation prediction workflow in [inference/casual_ml_prediction_model.ipynb](inference/casual_ml_prediction_model.ipynb) and [inference/Project Notebook.ipynb](inference/Project%20Notebook.ipynb)

The goal is to understand not only whether a booking is likely to cancel, but also how different treatment/control-style interventions can affect outcomes.

## Project Highlights

- Uses hotel booking data stored in [data/H1.csv](data/H1.csv) and [data/H2.csv](data/H2.csv).
- Explores uplift modeling with the `causalml` library.
- Builds classical machine learning and statistical baselines for cancellation prediction.
- Includes notebook-based analysis with charts, evaluation metrics, and interpretability steps.

## Repository Structure

```text
causal ml/
├── causalml_experiment/
│   └── casual_uplift_model.ipynb
├── data/
│   ├── H1.csv
│   └── H2.csv
└── inference/
	├── casual_ml_prediction_model.ipynb
	└── Project Notebook.ipynb
```

## What Each Notebook Does

### [causalml_experiment/casual_uplift_model.ipynb](causalml_experiment/casual_uplift_model.ipynb)

This notebook focuses on uplift modeling and causal inference ideas. It uses the `causalml` package to experiment with treatment and control groups, train uplift-style models, and inspect how different customer segments respond to an intervention.

### [inference/casual_ml_prediction_model.ipynb](inference/casual_ml_prediction_model.ipynb)

This notebook is a booking cancellation prediction workflow. It includes data preparation, feature engineering, model training, and evaluation with metrics such as ROC AUC. It also uses statistical modeling ideas for comparison.

### [inference/Project Notebook.ipynb](inference/Project%20Notebook.ipynb)

This notebook appears to be a broader project notebook that expands the cancellation analysis with more preprocessing, model comparison, and interpretation of the most important drivers of cancellation behavior.

## Requirements

The notebooks rely on the standard Python data-science stack. A typical environment should include:

- Python 3.10 or newer
- Jupyter or VS Code Notebook support
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `statsmodels`
- `causalml`
- `xgboost`
- `lightgbm`
- `shap`
- `kmodes`

If you need to install the common packages quickly, use:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels causalml xgboost lightgbm shap kmodes
```

## How To Run

1. Clone the repository.
2. Open the workspace in VS Code or Jupyter.
3. Install the dependencies listed above.
4. Open any notebook and run the cells from top to bottom.

Example:

```bash
git clone https://github.com/Shaurya-aswal/Causal-Ml-.git
cd Causal-Ml-
```

## Data Notes

- `H1.csv` and `H2.csv` are the raw datasets used by the notebooks.
- The analysis is notebook-driven, so feature engineering and modeling steps are performed directly in the notebooks.
- Some cells may take time to run because they train multiple models or generate plots.

## Methodology In Brief

- Clean and prepare hotel booking data.
- Build predictive features from the raw inputs.
- Train baseline models and compare performance.
- Use uplift/causal modeling to study the effect of an intervention.
- Inspect model outputs and interpretation results to identify important factors.

## Outputs You Can Expect

- Prediction metrics such as confusion matrices and ROC AUC.
- Feature engineering summaries.
- Visualizations and exploratory plots.
- Uplift modeling outputs and treatment effect exploration.

## Notes

- This repository is notebook-first, so it is best viewed in VS Code or Jupyter.
- Some notebooks may contain exploratory cells and longer-running model training sections.
- If you want a cleaned production version later, the next step would be to extract reusable Python modules from the notebooks.
