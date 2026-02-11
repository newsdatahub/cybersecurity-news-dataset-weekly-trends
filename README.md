# Cybersecurity News Coverage (English)
<img width="766" height="437" alt="Screenshot 2026-02-11 at 11 38 19 AM" src="https://github.com/user-attachments/assets/e1aeabb2-7dfd-4f39-902e-90b4758a8de4" />

## Dataset Summary
This dataset contains 3,000 English-language cybersecurity news metadata rows collected from the NewsDataHub API. It is designed for coverage trend analysis and comparative topic visibility over time.

Rows are filtered to enforce completeness and deduplicated by normalized title before export.

## Time Range
Start date: 2025-08-10  
End date: 2026-02-11

## Files
- `cybersecurity-news-en-title-3000.csv`: article-level metadata with mention flags.
- `weekly_counts.csv`: weekly counts by mention flag.
- `weekly_peak_headlines.csv`: representative example headline for each flag's peak week.
- `analysis.ipynb`: interactive analysis notebook.

## Schema
- `id` (string): unique article identifier.
- `title` (string): article title.
- `source_title` (string): publisher/source name.
- `article_link` (string): URL to source article.
- `description` (string): article summary/description.
- `pub_date` (string): publication timestamp.
- `mentions_ransomware` (bool): keyword-based mention flag.
- `mentions_ddos` (bool): keyword-based mention flag.
- `mentions_data_breach` (bool): keyword-based mention flag.
- `mentions_vulnerability` (bool): keyword-based mention flag.
- `mentions_hacking` (bool): keyword-based mention flag.
- `mentions_cyber_attack` (bool): keyword-based mention flag.

## Data Collection And Processing
- Source API: NewsDataHub (`https://newsdatahub.com`)
- Query theme: cybersecurity and related attack/breach/vulnerability terms
- Language filter: English
- Quality filter: drop rows with null/empty values in included columns
- Deduplication: normalized title dedupe first, then key-based fallback
- Mention flags: deterministic keyword matching on title+description

## Intended Use
- Coverage trend analysis
- Weekly visibility comparisons across cybersecurity topic buckets
- Dashboard demos and analytics notebooks

## Not Intended For
- Sentiment analysis
- Causal claims about real-world incident prevalence
- Market/performance predictions

## Limitations
- Mentions are keyword-based and can include incidental references.
- Coverage is influenced by publisher output volume.
- Snapshot dataset unless regenerated.

## License

CC-BY-4.0
This repository contains **article metadata only** and links to original sources.

## Source

Data collected via the **NewsDataHub API**
[https://newsdatahub.com](https://newsdatahub.com/?utm_source=github&utm_medium=repo&utm_campaign=cybersecurity_dataset)

## Hugging Face & Kaggle

The same dataset is available on **Hugging Face**:
[https://huggingface.co/datasets/NewsDataHub/cybersecurity-news-dataset-english-3000](https://huggingface.co/datasets/NewsDataHub/cybersecurity-news-dataset-english-3000)

and **Kaggle**: 
[https://www.kaggle.com/datasets/olgash270/openai-vs-anthropic-news-coverage-last-6-months](https://www.kaggle.com/datasets/olgash270/cybersecurity-news-dataset-english-3000)

## Contact

[support@newsdatahub.com](mailto:support@newsdatahub.com)
