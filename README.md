# Evaluation and Ranking of Text Classification (Sentiment Analysis) Models

## Overview

This code assesses sentiment analysis models using a preprocessed IMDb test dataset loaded from a Parquet file. Performance metrics like accuracy, precision, recall, and F1 score are utilized for evaluation. Following evaluation, the models are ranked using the TOPSIS method based on these metrics.

## Dependencies

Ensure the installation of the following libraries:

```bash
pip install torch transformers datasets scikit-learn pandas numpy pyarrow
```

## Data

The dataset's format is illustrated below:
![Dataset](https://github.com/kunalarora0930/Topsis-for-Pretrained-Models/blob/main/Images/data.png)

![Bar Chart](https://github.com/kunalarora0930/Topsis-for-Pretrained-Models/blob/main/Images/barchart.png)

## Usage

1. Load instances of the IMDb Test Dataset.

2. Pretrained Models for Sentiment Analysis:
    Four pretrained models are employed for sentiment analysis.
    Models:
      - cardiffnlp/twitter-roberta-base-sentiment (Model_0)
      - textattack/bert-base-uncased-SST-2 (Model_1)
      - aychang/roberta-base-imdb (Model_2)
      - t5-small (Model_3)

3. Tokenization and Prediction:
    Each model tokenizes the text data and generates predictions.

4. Model Evaluation:
  Various metrics such as accuracy, precision, recall, and F1 score are computed for each model.

5. TOPSIS Ranking:
  A TOPSIS function is defined to rank models based on their evaluation metrics.
  Weights and signs are assigned for each metric.
  The ranked array includes model names, metrics, TOPSIS scores, and ranks.

## Evaluation Metrics / Performance
![Performance Metrics](https://github.com/kunalarora0930/Topsis-for-Pretrained-Models/blob/main/Images/performance.png)

![Performance Chart](https://github.com/kunalarora0930/Topsis-for-Pretrained-Models/blob/main/Images/performance-chart.png)

## TOPSIS Scores and Ranking
![TOPSIS Scores and Ranking](https://github.com/kunalarora0930/Topsis-for-Pretrained-Models/blob/main/Images/result.png)