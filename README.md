# Training Amharic Text Embedding Models for Passage Retrieval

This repo contains code for training Amharic Text Embedding models based on 3 Encoder Base models 
- RoBERTa Base Amharic
- RoBERTa Medium Amharic
- BERT Medium Amharic

We also Evaluate existing multilingual embedding models form that rank high in the MTEB Leaderboard using the same test set as our embedding models.

# Results
Our largest embedding model, RoBERTa-Base-Amharic-Embed beats all of the multilingual embedding models on the MRR@10, NDCG@10 and Recall metrics while having 1/5th of their param count.

|Model | Params | MRR@10 | NDCG@10 | Recall@10 | Recall@50 | Recall@100 |
|------|--------|--------|---------|-----------|-----------|------------|
|gte-modernbert-base | 149M | 0.019 | 0.022 | 0.030 | 0.054 | 0.065 |
|gte-multilingual-base | 305M | 0.649 | 0.684 | 0.794 | 0.876 | 0.904 |
|multilingual-e5-large-instruct | 560M | 0.713 | 0.747 | 0.853 | 0.924 | 0.946 |
|snowflake-arctic-embed-l-v2.0 | 568M | 0.719 | 0.755 | 0.868 | 0.941 | 0.957 |
|BERT-Medium-Amharic-Embed | 40M | 0.657 | 0.696 | 0.817 | 0.916 | 0.945 |
|RoBERTa-Medium-Amharic-Embed | 42M | 0.707 | 0.744 | 0.861 | 0.941 | 0.963 |
|RoBERTa-Base-Amharic-Embed | 110M | **0.755** |**0.790** | **0.897** | **0.957** | **0.971** |

# Code

The training and eval code can be found in the `notebooks` folder.