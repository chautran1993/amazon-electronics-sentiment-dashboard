# Amazon Electronics Sentiment Dashboard

Streamlit dashboard demo for a 3-class sentiment analysis project on Amazon Electronics reviews.

## Included

- `app.py`: single-file Streamlit dashboard
- `requirements.txt`: minimal dependencies for the dashboard
- `data/processed/amazon_reviews_2023_electronics_labeled.csv`
- `outputs/model_comparison/model_comparison.csv`
- `outputs/amazon_reviews_2023/amazon_reviews_2023_product_ranking.csv`
- `models/bert/` tokenizer + config metadata

## Not included

The BERT weight file is intentionally excluded from Git because it is very large:

- `models/bert/model.safetensors`

The app will still run without it and automatically switch to a clear demo fallback predictor.

If you want real BERT inference, copy your checkpoint weight file back into:

- `models/bert/model.safetensors`

## Run locally

```powershell
python -m venv .venv
.\.venv\Scripts\activate
pip install -r requirements.txt
streamlit run app.py
```

## Project structure

```text
amazon-electronics-sentiment-dashboard/
|-- app.py
|-- requirements.txt
|-- README.md
|-- .gitignore
|-- data/
|   `-- processed/
|       `-- amazon_reviews_2023_electronics_labeled.csv
|-- outputs/
|   |-- amazon_reviews_2023/
|   |   `-- amazon_reviews_2023_product_ranking.csv
|   `-- model_comparison/
|       `-- model_comparison.csv
`-- models/
    `-- bert/
        |-- config.json
        |-- tokenizer.json
        |-- tokenizer_config.json
        `-- training_history.json
```

## Push to Git

```powershell
cd "C:\Users\vungo\OneDrive\Documents\New project\amazon-electronics-sentiment-dashboard"
git init
git add .
git commit -m "Initial Streamlit sentiment dashboard"
```
