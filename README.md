# Multi-Architecture-Sales-Forecasting

Comparison of four deep learning architectures — Stacked LSTM, GRU, Bidirectional LSTM, and Transformer with multi-head self-attention — for multi-step time-series sales forecasting on the M5 Walmart dataset (3,049 products, 1,913 days).

## Features
- Sliding-window pipeline: 30-day input to 7-day forecast horizon
- MinMaxScaler normalization with a 70/20/10 train/validation/test split
- Dropout, EarlyStopping, BatchNormalization, and LayerNormalization to address overfitting and vanishing gradients
- RMSE/MAE evaluation with residual analysis and an extended optimizer comparison experiment

## Tech Stack
TensorFlow/Keras, Pandas / NumPy, Scikit-learn

## Setup & Run
1. `pip install -r requirements.txt`
2. Place the M5 Walmart dataset CSVs in `/data`.
3. Run `python preprocess.py` to build sliding windows.
4. Run `python train.py --model {lstm|gru|bilstm|transformer}` to train and evaluate a given architecture.

## Status
This repository was scaffolded from the project description in the author's resume. Source code is being migrated/added here — check back for updates, or reach out below.

## 📫 Contact
- **Email:** rawish0922@gmail.com
- **Phone:** +92-332-8747138
- **LinkedIn:** [linkedin.com/in/rawishsarfraz](https://linkedin.com/in/rawishsarfraz)
- **GitHub:** [github.com/Rawishs-2882](https://github.com/Rawishs-2882)

