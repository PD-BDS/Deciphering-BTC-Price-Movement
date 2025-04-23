# Deciphering BTC Price Movement

This project explores the predictive relationship between public sentiment and Bitcoin price movement using deep learning. By leveraging sentiment indicators derived from **Twitter**, **Google Trends**, and the **Crypto Fear and Greed Index (CFGI)**, we assess their influence on BTC's volatile price action. Advanced NLP models such as **BERT** and **FinBERT** are used for sentiment extraction, while **LSTM** models forecast short and long-term price direction.

---

## 🧠 Abstract

Bitcoin, since its inception in 2008, has remained the leading decentralized cryptocurrency, influencing global finance with its transparency and volatility. This study investigates how sentiment metrics from online platforms impact Bitcoin's price movement. Using **BERT** and **FinBERT** to analyze text data and extract sentiment signals, and **LSTM** for time-series prediction, the project demonstrates:

- **Daily prediction accuracy**:  
  - BERT-LSTM: 85%  
  - FinBERT-LSTM: 86%
- **Monthly prediction accuracy**:  
  - BERT-LSTM: 94%  
  - FinBERT-LSTM: 93%

While sentiment features significantly improved prediction performance on **weekly and monthly horizons**, the results did **not show a major advantage** of FinBERT over BERT in Twitter sentiment extraction.

---

## 🧰 Tools & Technologies

- **Python**, **Jupyter Notebooks**
- **Pandas, NumPy, Matplotlib, Seaborn**
- **TensorFlow / Keras** for LSTM modeling
- **Transformers** (HuggingFace) for BERT & FinBERT
- **Tweepy**, **Google Trends API**, **CFGI Scraping**
- **Sklearn** for preprocessing and evaluation

---

## 📦 Project Structure

```
📁 Deciphering-BTC-Price-Movement
├── Data Collection.ipynb               # Scraping and preparing sentiment data
├── Data Preparation and Machine Learning Model Implementation.ipynb
│                                       # Feature engineering, model training & evaluation
├── requirements.txt
├── README.md
```

---

## 🧪 Methodology

### 1. **Data Collection**
- **Twitter**: Sentiment-extracted tweets using BERT & FinBERT
- **Google Trends**: Keyword searches like "Bitcoin", "BTC", "crypto"
- **CFGI**: Historical fear and greed scores

### 2. **Sentiment Analysis**
- **BERT** and **FinBERT** models converted tweet text into sentiment labels/scores.
- Results used as features for predictive modeling.

### 3. **Time-Series Prediction**
- Combined features fed into **LSTM networks** to forecast:
  - **Next Day**
  - **Next Week**
  - **Next Month** price movement (up/down)

---

## 📈 Results

| Time Horizon | Model         | Accuracy |
|--------------|---------------|----------|
| Daily        | BERT + LSTM   | 0.85     |
| Daily        | FinBERT + LSTM| 0.86     |
| Monthly      | BERT + LSTM   | 0.94     |
| Monthly      | FinBERT + LSTM| 0.93     |

- Sentiment signals significantly improved long-term price movement predictions.
- No substantial gain from FinBERT over BERT for tweet sentiment analysis.

---

## 🚀 Getting Started

1. Clone this repo:
   ```bash
   git clone https://github.com/pd-bds/Deciphering-BTC-Price-Movement.git
   cd Deciphering-BTC-Price-Movement
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run notebooks:
   - `Data Collection.ipynb` to fetch and clean raw sentiment data
   - `Data Preparation and Machine Learning Model Implementation.ipynb` for model training and evaluation

---

## 💡 Keywords

Bitcoin, Cryptocurrency, Sentiment Analysis, Deep Learning, LSTM, BERT, FinBERT, Price Prediction

---

## 📚 References

- [BERT: Pre-training of Deep Bidirectional Transformers](https://arxiv.org/abs/1810.04805)
- [FinBERT: Financial Sentiment Analysis](https://arxiv.org/abs/1908.10063)
- [Crypto Fear and Greed Index](https://alternative.me/crypto/fear-and-greed-index/)
