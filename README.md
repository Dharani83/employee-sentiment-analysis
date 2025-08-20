# Employee Sentiment Analysis - Final Assessment

## 📌 Project Overview
This project analyzes employee email communications to extract sentiment insights, measure engagement, detect flight risks, and model sentiment trends over time.

The objectives are:

Sentiment analysis of employee messages.
Engagement scoring and trend detection.
Identification of high-risk employees (flight risk).
Predictive modeling of sentiment trends.

## 🛠 Methodology
1.Data Preprocessing
•	Source: test.xlsx (employee communications)
•	Steps: handled missing values, extracted email text, parsed dates, generated features (word counts, message counts).

2.Sentiment Labeling
•	Tool: TextBlob for polarity scoring
•	Labels: Positive (+1), Negative (–1), Neutral (0)

3.Exploratory Data Analysis (EDA)
•	Sentiment distribution
•	Word count patterns
•	Monthly sentiment trends

4.Scoring & Ranking
•	Monthly employee sentiment scores
•	Top 3 positive & top 3 negative employees

5.Flight Risk Definition
•	Employees with ≥ 4 negative messages in 30 days

6.Predictive Model
•	Linear Regression
•	Features: word count, message frequency, sentiment polarity
•	Split: 70% train / 30% test

## 📊 Key Outputs
- **Visualizations**: sentiment distribution, word counts, monthly trends.  
- **Reports**: output/labeled.csv → sentiment-labeled dataset, output/flight_risks.csv → list of high-risk employees, output/model_summary.txt → regression performance .
- **Findings**: Ranking of top positive & negative employees , Flight risk employee list with names & emails.

### ✅ Results Summary
- **Top 3 Positive Employees**
  - lydia.delgado@enron.com (score: 6)  
  - patti.thompson@enron.com (score: 6)  
  - kayne.coulter@enron.com (score: 5)

- **Top 3 Negative Employees**
  - bobette.riner@ipgdirect.com (score: 1)  
  - johnny.palmer@enron.com (score: 2)  
  - eric.bass@enron.com (score: 3)

- **Flight Risk Employees (≥ 4 negatives in 30 days)**  
  bobette.riner@ipgdirect.com, eric.bass@enron.com, john.arnold@enron.com, johnny.palmer@enron.com, lydia.delgado@enron.com, patti.thompson@enron.com, rhonda.denton@enron.com, sally.beck@enron.com

- **EDA Insights**
  - ~65% positive, ~20% neutral, ~15% negative.  
  - Negativity spiked in March.  
  - Word count correlated with message polarity.

- **Model Performance**
  - Linear Regression → R² = –8.45, RMSE ≈ 0.034  
  - Interpretation: weak fit → advanced NLP models needed.


## 📂 Repo Structure
LLM_Final_Assessment_Dharani/
│── data/                         # Input dataset
│   └── test.xlsx
│── output/                       # Results, CSVs, plots
│   ├── flight_risks.csv
│   ├── labeled.csv
│   ├── monthly_scores.csv
│   ├── summary.txt
│   ├── model_summary.txt
│   └── visualizations/           # Charts
│       ├── sentiment_dist.png
│       ├── wordcount_dist.png
│       └── monthly_counts.png
│── notebook.ipynb                # Main analysis notebook
│── Dharani kousalya penta-Final_Report_Employee_Sentiment.docx
│── requirements.txt               # Dependencies

## Limitations and Next steps

1.TextBlob lacks nuance (cannot detect sarcasm, subtle tones).
2.Model performance is weak (negative R²).
3.Future improvements:
    i.Use advanced NLP models (e.g., BERT, RoBERTa)
    ii.Topic modeling for thematic analysis
    iii.Richer features (e.g., sender/recipient metadata, communication frequency trends)

## 👤 Author
**Dharani Kousalya**
