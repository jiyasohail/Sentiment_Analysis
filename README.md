# 🐦 Twitter Airline Sentiment Analysis

> An NLP project that analyzes the sentiment of airline-related tweets using TextBlob, with visualizations including bar charts, pie charts, confusion matrices, and word clouds.

---

## 💡 What This Project Does

This project takes real tweets directed at US airlines and automatically classifies each one as **positive**, **negative**, or **neutral** using TextBlob's sentiment polarity scoring. Results are then compared against the true human-labeled sentiments to evaluate accuracy.

---

## 🔍 How It Works

**Step 1 — Load Data**
The Twitter US Airline Sentiment dataset is loaded (source: Kaggle). It contains tweets with human-labeled sentiments (`airline_sentiment` column).

**Step 2 — Text Cleaning**
Each tweet is cleaned using regex: URLs, @mentions, special characters, and extra whitespace are removed and text is lowercased.

**Step 3 — Sentiment Scoring with TextBlob**
TextBlob calculates a **polarity score** between -1 (very negative) and +1 (very positive) for each cleaned tweet. Scores are then bucketed:
- `> 0` → Positive
- `< 0` → Negative  
- `= 0` → Neutral

**Step 4 — Evaluation**
Predicted sentiments are compared against the true labels using a confusion matrix and accuracy score.

**Step 5 — Word Clouds**
Separate word clouds are generated for positive, negative, and neutral tweets to reveal the most common words in each category.

---

## 📊 Visualizations

- Bar chart of predicted sentiment distribution
- Pie chart of sentiment proportions
- Confusion matrix (predicted vs. true labels)
- Word clouds for positive, negative, and neutral tweets

---

## 🛠️ Tech Stack

- **Python**
- **Pandas** — Data loading and manipulation
- **TextBlob** — Sentiment polarity scoring
- **Matplotlib & Seaborn** — Charts and confusion matrix
- **WordCloud** — Word cloud generation
- **scikit-learn** — Confusion matrix and accuracy score
- **re** — Regex text cleaning

---

## 🗂️ Project Structure

```
├── Sentiment_analysis.ipynb    # Main notebook
├── Tweets.csv                  # Dataset (source: Kaggle)
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/jiyasohail/twitter-sentiment-analysis.git
cd twitter-sentiment-analysis
```

### 2. Install dependencies

```bash
pip install pandas matplotlib seaborn scikit-learn textblob wordcloud
```

### 3. Run the notebook

Open `Sentiment_analysis.ipynb` in Jupyter or Google Colab and run all cells.

---

## 💡 Key Findings

Negative tweets dominate the airline dataset — a common pattern in customer service data where people are more likely to tweet complaints than praise. TextBlob performs reasonably on clear positive/negative language but struggles with neutral tweets, which tend to be factual statements that don't carry obvious emotional tone. The word clouds for negative tweets prominently feature words like "delay", "cancelled", and "hours", while positive tweets contain "thank", "great", and "love".

---

## 👩‍💼 Author

**Javariya Sohail** — Computer Science Graduate & Data Enthusiast

