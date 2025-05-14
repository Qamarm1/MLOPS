# 🧪 Diabetes Progression Prediction with MLflow

This project demonstrates a complete machine learning lifecycle using **MLflow**. It builds and evaluates a model to predict diabetes disease progression based on scikit-learn’s diabetes dataset.

## 📌 Features

- Data loading and exploration with `pandas`
- Model training using `scikit-learn`
- Experiment tracking and logging with `MLflow`
- Hyperparameter tuning using `Hyperopt`
- Model evaluation and visualization
- MLflow UI deployment with `ngrok`

## 🛠️ Installation

```bash
pip install mlflow==2.9.2 scikit-learn pandas matplotlib hyperopt pyngrok
```

## 🚀 Usage

Run the notebook:

```bash
jupyter notebook
```

To launch the MLflow tracking UI:

```bash
mlflow ui --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns --port 5000
```

Use `ngrok` to expose the MLflow UI (if running on Colab or a remote server):

```python
from pyngrok import ngrok
public_url = ngrok.connect(5000).public_url
print(f"MLflow UI is available at: {public_url}")
```

## 📈 Model

- **Algorithm:** Linear Regression
- **Dataset:** Diabetes dataset from `sklearn.datasets`
- **Metrics Tracked:** RMSE, MAE, R²

## 📂 Artifacts

MLflow stores runs, parameters, metrics, and artifacts under the `mlruns/` directory.

## 📄 License

This project is licensed under the MIT License.
