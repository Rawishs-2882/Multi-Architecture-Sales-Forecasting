<div align="center">

![header](https://capsule-render.vercel.app/api?type=waving&color=0:F8BBD0,50:CE93D8,100:B39DDB&height=180&section=header&text=Sales%20Forecasting&fontSize=36&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=LSTM%20vs%20GRU%20vs%20BiLSTM%20vs%20Transformer&descAlignY=58&descSize=15)

</div>

## Overview

This project puts four deep learning architectures side by side on the same forecasting problem: Stacked LSTM, GRU, Bidirectional LSTM, and a Transformer with multi head self attention, all trained on the M5 Walmart Forecasting dataset covering 3,049 products across 1,913 days.

## Key Features

### Four architectures, one benchmark
Every model is trained and evaluated on identical splits and preprocessing, so the comparison reflects architectural differences rather than data handling differences.

### Sliding window pipeline
A 30 day input window is used to forecast a 7 day horizon, which is built with a reusable windowing utility so new architectures can be dropped in easily.

### Careful normalization and splitting
MinMaxScaler normalization is applied consistently, with a 70 percent train, 20 percent validation and 10 percent test split.

### Regularization against overfitting
Dropout, EarlyStopping, BatchNormalization and LayerNormalization are used to keep the larger architectures, especially the Transformer, from overfitting on a relatively noisy retail dataset.

### Rigorous evaluation
RMSE and MAE are reported for every model, along with residual analysis and an extended optimizer comparison experiment to see how architecture choice interacts with optimizer choice.


## Tech Stack

<div align="center">
<img src="https://skillicons.dev/icons?i=tensorflow,python,pandas,numpy" />
</div>

TensorFlow and Keras for model definition and training, Pandas and NumPy for data wrangling, and Scikit-learn for scaling and evaluation utilities.

## How It Works

Raw M5 sales data is aggregated per product, windowed into 30 day input and 7 day target sequences, then scaled. Each architecture is trained on the same windows with matching callbacks, and predictions are inverse transformed before RMSE, MAE and residual analysis are computed.

## Setup and Run

1. Install dependencies with `pip install -r requirements.txt`.
2. Place the M5 Walmart dataset CSVs in `/data`.
3. Run `python preprocess.py` to build the sliding window dataset.
4. Run `python train.py --model {lstm,gru,bilstm,transformer}` to train and evaluate a given architecture.
5. Run `python compare.py` to generate the RMSE and MAE comparison table across all four models.

## Roadmap

- Add a hybrid CNN plus attention architecture
- Extend the forecast horizon beyond 7 days
- Package the best model behind a small inference API

## Status

> **Status:** This repository was scaffolded from the project description on the author's resume. Source code is being migrated and added here in stages. Reach out using the contact links below if you would like early access to the implementation.

## Let's Connect

<div align="center">

[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:rawish0922@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/rawishsarfraz)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Rawishs-2882)
[![Phone](https://img.shields.io/badge/Call-+92--332--8747138-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](tel:+923328747138)

</div>

<div align="center">

![footer](https://capsule-render.vercel.app/api?type=waving&color=0:B39DDB,50:CE93D8,100:F8BBD0&height=80&section=footer)

</div>
