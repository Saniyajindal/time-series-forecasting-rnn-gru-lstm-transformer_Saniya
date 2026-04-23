# time-series-forecasting-rnn-gru-lstm-transformer_Saniya
# Time Series Forecasting using RNN, MLP, LSTM and Transformer

## 📌 Overview

This project implements a complete time-series forecasting pipeline from scratch. The goal is to understand how sequence data is processed and how different models perform on time-series prediction tasks.

The implementation includes:

* Custom RNN (from scratch)
* MLP baseline
* LSTM (prebuilt)
* Transformer (prebuilt)

---

## ⚙️ Parameter Setup (Roll Number Based)

Parameters are derived from roll number:

* **Window Size** = (sum of digits) % 10 + 8
* **Prediction Horizon** = (last 2 digits) % 3 + 1
* **Hidden Size** = (first 3 digits) % 16 + 8

These ensure personalized configuration for each student.

---

## 📊 Dataset

Two datasets are used:

1. Synthetic dataset (sine wave) for initial testing
2. Real-world electricity consumption dataset (time-series)

---

## 🔄 Data Preprocessing

Time-series data is converted into supervised learning format using windowing:

* Input: Past `window_size` values
* Output: Next `prediction_horizon` values

This allows models to learn temporal dependencies.

---

## 🧠 Models Implemented

### 1. MLP (Baseline)

* Fully connected neural network
* Does not capture temporal dependencies
* Input is flattened

---

### 2. Custom RNN (From Scratch)

* Implements hidden state manually
* Captures sequential patterns
* Hidden state acts as memory

---

### 3. LSTM (Prebuilt)

* Handles long-term dependencies
* Uses gating mechanism

---

### 4. Transformer (Prebuilt)

* Uses attention mechanism
* Captures global dependencies

---

## 📈 Training & Evaluation

Models are trained using:

* Mean Squared Error (MSE) loss
* Adam optimizer

Evaluation metrics:

* MSE
* MAE
* RMSE

---

## 📉 Results

* RNN performs better than MLP due to sequence awareness
* LSTM improves performance on longer dependencies
* Transformer captures global patterns but requires more data

---

## 🔬 Ablation Study

Model performance is tested with:

* Original window size
* Half window size
* Double window size

This shows how context length affects prediction.

---

## ⚠️ Failure Analysis

* Models struggle with sudden spikes
* Short window sizes fail to capture long-term trends
* Large window sizes may lead to overfitting

---

## ▶️ How to Run

1. Open the notebook
2. Run all cells sequentially
3. Ensure dataset is loaded correctly
4. View plots and metrics

---

## 📌 Conclusion

This project demonstrates how different models handle time-series data and highlights the importance of temporal dependencies in forecasting tasks.

---

## 🔗 Submission

* GitHub Repository: [Add Link]
* YouTube Explanation: [Add Link]
