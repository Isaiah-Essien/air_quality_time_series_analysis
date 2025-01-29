# Air Quality Time Series Forecasting with LSTM

## Project Overview
This project focuses on forecasting PM2.5 air pollution levels using **Long Short-Term Memory (LSTM)** recurrent neural networks. The dataset consists of historical air quality data from Beijing, including meteorological variables and pollutant concentrations. The goal is to build an optimized deep learning model to accurately predict air quality trends and inform pollution control strategies.

## Findings
Through multiple experiments, the **best-performing model** was identified as follows:
- **Model Architecture:** Three LSTM layers (128, 64, and 32 units) with a single dense output layer
- **Optimizer:** Adam
- **Learning Rate:** 0.0003
- **Batch Normalization:** Applied to stabilize training
- **Dropout:** 0.25 in the first LSTM layer, 0.3 in the others
- **Epochs:** 70
- **Batch Size:** 32
- **Loss Function:** Mean Squared Error (MSE)
- **Performance Metric:** Root Mean Squared Error (RMSE) = **67.5**

Despite achieving strong predictive performance, some challenges included:
- Overfitting due to outliers in PM2.5 values
- The vanishing gradient problem with tanh activation, leading to the preference for ReLU
- Missing values in the dataset requiring careful handling (bfill/ffill imputation)
- Lack of a validation set for implementing early stopping

## Repository Structure
```
├── data/                   # Dataset files
├── notebook/              # Jupyter Notebooks for data exploration and modeling               # Saved trained models
├── submissions/                # Evaluation metrics and model outputs
├── README.md               # Project documentation
```

## 🔧 Installation & Setup
To reproduce this project, follow these steps:
- Clone the repo and run the notebook

### 1️⃣
This will train the LSTM model with the optimal parameters found in the experiments.

## Contributing
If you'd like to contribute to this project, feel free to fork the repository and submit a pull request!
