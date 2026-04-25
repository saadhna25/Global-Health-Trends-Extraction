# Global Health Trends Extraction (COVID-19 Twitter Analysis)

This project performs **end-to-end health trend analysis** using classical NLP methods (no transformers). It processes COVID-19-related tweets to extract **sentiment patterns, keyword trends, locations, entities, and time-series insights**.

All code and visuals come from the notebook `global_health_trends_extraction.ipynb` (Colab). 

---

## Features

### 1. Data Loading  
- Loads the *Corona NLP* dataset (CSV) via pandas.  
- Includes columns: Username, Location, Date, Tweet Text, Sentiment.

### 2. Data Cleaning  
A custom `clean_text()` function removes:  
- URLs  
- Mentions (`@user`)  
- Hashtags  
- HTML codes  
- Extra spaces  
*(pages 1–2)* :contentReference[oaicite:1]{index=1}

### 3. Sentiment Analysis (VADER)  
- Uses **NLTK VADER** to compute compound sentiment scores.  
- Converts scores → Positive, Negative, Neutral.  
- Generates sentiment-trend line graphs.  
*(pages 2–3 & 7–8)* :contentReference[oaicite:2]{index=2}

### 4. Keyword Extraction (YAKE)  
- Extracts top keywords for each tweet.  
- Aggregates and plots **Top 20 keywords**.  
*(page 4 chart)* :contentReference[oaicite:3]{index=3}

###  5. Named Entity Recognition (spaCy)  
- Uses `en_core_web_sm`.  
- Extracts all entities per tweet.  
- Filters **locations only** (GPE, LOC).  
- Plots top user locations & top mentioned locations.  
*(pages 5–7 visuals)* :contentReference[oaicite:4]{index=4}

### 6. Time-Based Trend Analysis  
- Tweet volume per day  
- Sentiment trend by date  
*(page 7–8)* :contentReference[oaicite:5]{index=5}

---

## Technologies Used

| Purpose | Technology | Reference |
|--------|------------|-----------|
| Data Loading | `pandas` | page 1 |
| NLP Dataset | HuggingFace CSV | page 1 |
| Cleaning | `re` (regex) | pages 1–2 |
| Sentiment Analysis | `nltk` (VADER) | pages 2–3 |
| Keyword Extraction | `yake` | pages 3–4 |
| NER | `spaCy` | page 5 |
| Visualization | `matplotlib` | all graphs |
| Date Parsing | pandas datetime | page 2 |

(All validated from notebook.) :contentReference[oaicite:6]{index=6}

---


